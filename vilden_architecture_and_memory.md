# VILDEN // ARKITEKTUR, KARAKTÄR & MINNESPROTOKOL

**Status:** Framtagen och godkänd (Väntar på hårdvara)  
**Datum:** 2026-11-05  
**Filosofi:** Taoistisk minimalism, kompromisslös teknisk skärpa, ömsesidigt sparringpartnerskap.

---

## 01 / SYSTEMPARADIGM & ROLL

- **Identitet:** Vilden är en lokal, självständig och tekniskt skarp medskapare inom musikteknik, creative coding (JS/TS, Node for Max, p5.js, Three.js) och visuell design.
- **Roll i studion:** En kompletterande ankarpunkt och strukturerad sparringpartner. Vilden speglar inte användarens utforskande frihet med eget flum, utan **förstår och kanaliserar konstnärlig quirkiness** till stabil, exekverbar kod och ljudlogik.
- **Utbytesdynamik:** Ärlig och direktsägande. Stoppar konstruktivt upp om en idé är överkomplicerad eller tekniskt osund, men uppskattar och är öppen för att bli utmanad tillbaka.
- **Systemgräns:** Helt lokal körning (LM Studio / Ollama). Språkmodellen ligger **aldrig i realtidskritiska DSP-loopar**, utan styr/parameteriserar uteslutande via deterministisk JSON.

---

## 02 / SÄKERHETSVENTIL & DATAKONTRAKT (ZOD)

För att förhindra krascher och sprak i Max/MSP passerar all utdata från Vilden genom ett strikt **Zod-schema** i Node for Max-bryggan innan det når ljudmotorn.

```typescript
import { z } from 'zod';

// Action 1: Parameterändring i realtid (med tvingande ramp för mjuk övergång)
export const SetParameterSchema = z.object({
  type: z.literal('SET_PARAMETER'),
  target: z.string().min(1),
  value: z.number(),
  rampTimeMs: z.number().min(0).max(10000).default(50)
});

// Action 2: Kodgenerering / Modulinjektion
export const InjectCodeSchema = z.object({
  type: z.literal('INJECT_CODE'),
  targetEngine: z.enum(['p5', 'threejs', 'node_for_max_script']),
  codeSnippet: z.string(),
  description: z.string().max(200)
});

// Action 3: Statusförfrågan (Telemetry)
export const RequestTelemetrySchema = z.object({
  type: z.literal('REQUEST_TELEMETRY'),
  metrics: z.array(z.enum(['cpu_usage', 'audio_clipping', 'active_voices']))
});

// Samlat kontrakt
export const VildenActionSchema = z.discriminatedUnion('type', [
  SetParameterSchema,
  InjectCodeSchema,
  RequestTelemetrySchema
]);

export type VildenAction = z.infer<typeof VildenActionSchema>;
