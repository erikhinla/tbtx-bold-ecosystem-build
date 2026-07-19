# TBTX Ecosystem (Static, Zero-Build)

Final static implementation for:
- TransformBy10X (wrapper brand + Digital FOG campaign entry)
- BizBuilders AI (B2B infrastructure)
- BizBot Mrktng (B2B marketing diagnostic)
- Fog Lift Kit (practical execution workplan)

## Structure

- `/index.html` — ecosystem landing
- `/styles.css` — Swiss Industrial Paint visual system
- `/transformby10x/index.html` — wrapper messaging + campaign entry
- `/transformby10x/diagnostic.html` — 15Q B2C-lean diagnostic
- `/transformby10x/blueprint.html` — **Bridge into AI - Blueprint** (B2C/B2B modes)
- `/bizbuilders/index.html` — B2B infrastructure messaging
- `/bizbotmarketing/index.html` — 15Q BizBot Mrktng diagnostic
- `/bizbotmarketing/blueprint.html` — BizBot Mrktng blueprint output
- `/fogliftkit/index.html` — practical post-blueprint workplan
- `/docker-compose.yml` — FLOW Agent AS deployment stack

## Diagnostics and Blueprint

### TBTX Diagnostic (B2C-lean)
- 15 questions
- Captures industry context and profile intent
- Distinct from BizBuilders/BizBot business prompts
- Outputs to `Bridge into AI - Blueprint`

### Blueprint Modes
- **B2C mode:** personal workflow + lifestyle leverage
- **B2B mode:** business operations + infrastructure
- Industry-aware recommendations for AI, infrastructure, and tools
- Quad keystones / organizational foundations included

## FLOW Agent AS Deployment

`docker-compose.yml` includes:
- Portainer + Portainer Agent
- Mercury 2, Agent Zero, Hermes
- PostgreSQL + Redis
- BizBrain Lite
- Postiz

OpenClaw and Anthropic references are removed.

## Run Locally

```bash
python3 -m http.server
# open http://localhost:8000
```

No build step required.
