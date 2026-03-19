## 🔧 tradermonty/claude-trading-skills
**URL:** https://github.com/tradermonty/claude-trading-skills  
**Fecha de registro:** 2026-03-19  
**Estado:** ✅ Phase A instalada (~15 skills, no-API) en `~/.claude/skills/`  
**Proyecto local:** `~/Projects/gestion-patrimonial/`

### ¿Qué es?
Colección curada de Claude Skills para inversores y traders en equities. Cada skill empaqueta un `SKILL.md` con workflow estructurado para Claude Code, referencias de dominio y scripts Python opcionales. Filosofía: "empower solo traders" — análisis institucional al alcance de un operador individual.

### Skills instaladas (Phase A – sin API)
| Skill | Utilidad principal |
|---|---|
| Market Breadth Analyzer | Scoring 0-100 de salud del mercado (6 componentes) |
| Breadth Chart Analyst | Análisis visual S&P 500 Breadth Index |
| Market Top Detector | Detección de techo de mercado (O'Neil + Minervini) |
| Macro Regime Detector | Transiciones de régimen macro a 1-2 años |
| Sector Analyst | Rotación sectorial y fase de ciclo de mercado |
| Market Environment Analysis | Briefing global macro estructurado |
| Market News Analyst | Impacto de noticias en equities y commodities |
| Scenario Analyzer | Análisis de escenarios a 18 meses (primario + second opinion) |
| CANSLIM | Metodología O'Neil completa |
| VCP Screener | Volatility Contraction Pattern (Minervini) |
| Position Sizer | Sizing basado en riesgo |
| Backtest Expert | Backtesting sistemático de estrategias |
| Stanley Druckenmiller Investment | Síntesis macro top-down (integra 8 skills upstream) |
| Skill Designer | Diseño de nuevas skills desde especificaciones |
| Skill Idea Miner | Detección de patrones en sesiones para nuevas skills |

### Encaje con mi metodología HTF-first
```
BTC/ETH HTF (12H+) 
  → Market Breadth Analyzer (¿rally con participación real?)
  → Macro Regime Detector (¿en qué régimen operamos?)
  → Sector Analyst (rotación: ¿risk-on o risk-off?)
  → Scenario Analyzer (escenarios para el trade)
  → Position Sizer (sizing correcto antes de entrar)
```

### Roadmap de instalación
- [ ] **Phase B – FMP API:** Value Dividend Screener, FinViz Screener Elite, fundamentals
- [ ] **Phase C – Alpaca + Edge Pipeline:** live data, backtesting automatizado

### Infraestructura relevante del repo (cherry-picking futuro)
- **dual-axis-skill-reviewer:** scorer determinístico 0-100 (metadata, workflow, execution safety, artifacts, tests). Útil como benchmark de calidad para skills propias en `gestion-patrimonial/`.
- **Sistema de auto-mejora diario:** launchd (macOS) → score < 90 → Claude CLI mejora la skill → PR automático. Patrón de automatización replicable.
- **Skill Idea Miner:** escanea logs de Claude Code para detectar patrones que merezcan convertirse en skills. Revisar cuando el volumen de sesiones en `gestion-patrimonial/` sea alto.

### Cuándo revisitar
- [ ] Al conseguir FMP API key → instalar Phase B completa
- [ ] Al activar Alpaca → instalar Phase C
- [ ] Explorar `dual-axis-skill-reviewer` como modelo para puntuar skills propias
- [ ] Monitorear releases: repo activo, auto-mejora continua
