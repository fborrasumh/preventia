# PreventIA

Sistema de aprendizaje de la asignatura **1963 Medicina Preventiva y Salud Pública** (5.º del Grado en Medicina, Universidad Miguel Hernández de Elche), construido a partir de su Guía Docente 2026-2027. Aplicación web de un solo fichero: funciona en el navegador, sin servidor y, salvo la IA, sin conexión.

**Usar la app:** https://fborrasumh.github.io/preventia/

[![DOI](https://zenodo.org/badge/DOI/10.5281/zenodo.24492190.svg)](https://doi.org/10.5281/zenodo.24492190)

**Idiomas:** español (por defecto), inglés y portugués; selector en la barra superior (o `?lang=en` / `?lang=pt` en la URL).

## Qué hace

- **Ruta adaptativa** sobre los 19 resultados de aprendizaje (RA) de la guía: diagnóstico inicial, dominio por RA con olvido (Elo), repaso espaciado (Leitner), intercalado de temas, registro de seguridad (seguro/dudo/adivino) y las razones de cada elección a la vista.
- **134 preguntas** (opción múltiple, verdadero/falso, emparejar, ordenar) con feedback elaborado.
- **18 generadores de problemas y gráficos con solución calculada por código** (VPP/VPN, NNT, estandarización directa, tasas de ataque y RR, inmunidad de grupo, efectividad vacunal, fracción atribuible, AVAD, RCEI, DDD/100 estancias, bacteriemias por 1000 días de catéter, higiene de manos, desigualdades; curvas epidémicas, forest plots, pirámides y gradientes sociales). Ejemplos resueltos que se retiran y diagnóstico del error típico.
- **Laboratorio de población:** cribado y Bayes con 10 000 personas y predicción previa, modelo SIR con reto de cobertura mínima, paradoja de Rose (estrategia poblacional frente a alto riesgo) y sesgo de adelanto.
- **Brote en directo:** investigación de un brote alimentario con datos distintos en cada partida (aviso, definición de caso, curva epidémica, agente, cohorte retrospectiva con RR, medidas de control).
- **Consulta preventiva:** ocho personas; se puntúa lo que se olvida y lo que se hace de más (cribados de la cartera común, vacunas, consejo, equidad y prevención cuaternaria).
- **Hospital seguro:** aislamientos por mecanismo de transmisión, los 5 momentos de la higiene de manos, casos de PROA y análisis de un evento adverso.
- **Preguntas de desarrollo** con rúbrica: el código señala palabras clave como pista, el estudiante se autoevalúa y puede entregar sus respuestas al profesorado, que las valora en su panel.
- **Simulacro** con el formato de la guía: test de 4 opciones con −0,25 por error y desarrollo; hay que aprobar cada parte; análisis de si convino responder al adivinar.
- **Tutor socrático** (con clave de IA) que conoce los RA más débiles y los últimos errores.
- **Panel del profesorado:** análisis de la guía, matriz de alineación RA ↔ temas ↔ actividades, analítica de ítems (dificultad, discriminación, distractores), revisión de respuestas de desarrollo y exportación a Moodle XML, GIFT y CSV.

## Cómo se usa la IA

Solo en el tutor y en el comentario de las preguntas de desarrollo, con la propia clave de OpenAI, Google Gemini o Anthropic Claude. La IA nunca pone nota: el código elimina frases con notas o porcentajes y comprueba que cada cita que atribuye al estudiante aparece literalmente en su texto; si no, la marca como «sin evidencia».

## Privacidad

Todo (respuestas, progreso, textos, clave) se guarda en el navegador. Solo sale hacia el proveedor de IA lo que el estudiante envía al tutor o a un comentario, con datos personales enmascarados y tras un aviso con muestra. La exportación de datos para el profesorado es voluntaria y anónima (seudónimo, sin textos libres); la de respuestas de desarrollo incluye los textos y solo se descarga si el estudiante lo decide.

## Límites

- El dominio por RA es una estimación para orientar, no una calificación. El peso de cada RA es una aproximación: la guía no da cifras («proporcional al peso de los temas»).
- Los modelos de población (SIR, Rose) son didácticos, con parámetros ficticios.
- Programas y recomendaciones de España en 2026; algunos (vacunas del adulto) varían entre comunidades autónomas.
- La app no produce evidencia por sí sola. Investigar con sus datos requiere aprobación del comité de ética (OEP de la UMH), consentimiento informado y RGPD.
- La IA puede equivocarse; no se ha probado con claves reales, solo con respuestas simuladas.

## Adoptarla en otra asignatura o universidad

Editar `src/curriculum.js` (ficha, temas y RA literales), `src/items.js`, `src/items2.js` y `src/desarrollo.js` (preguntas y rúbricas), y `ASIG.eval` (formato de evaluación). Después, `python3 build.py`.

## Autoría

Fernando Borrás Rocher, María Asunción Pastor Valero (profesora responsable de la asignatura), María Teresa Gea Velázquez de Castro y Juana Requena Puche, de la Universidad Miguel Hernández de Elche. Las cuatro personas autoras aceptan publicar su aportación bajo licencia MIT.

ORCID: Fernando Borrás Rocher [0000-0002-5519-4573](https://orcid.org/0000-0002-5519-4573) · María Asunción Pastor Valero [0000-0001-9282-5787](https://orcid.org/0000-0001-9282-5787) · María Teresa Gea Velázquez de Castro y Juana Requena Puche: ORCID pendiente

## Cómo citar

Borrás Rocher, F., Pastor Valero, M. A., Gea Velázquez de Castro, M. T. y Requena Puche, J. (2026). *PreventIA* (v1.1.0) [Software]. DOI: [10.5281/zenodo.24492190](https://doi.org/10.5281/zenodo.24492190)

## Licencia

MIT. Véase [LICENSE](LICENSE). Para los contenidos docentes (preguntas, casos, rúbricas) los autores pueden optar por CC BY 4.0.
