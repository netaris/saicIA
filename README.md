# AcreditIA

Autoinforme y plan de mejora de un título, con evidencias verificadas. Aplicación web de un solo fichero.

**Usar la app:** https://fborrasumh.github.io/acreditia/

[![DOI](https://zenodo.org/badge/DOI/10.5281/zenodo.23276225.svg)](https://doi.org/10.5281/zenodo.23276225)

**Idiomas:** español (por defecto), inglés, portugués y las lenguas cooficiales de España: català/valencià, galego y euskara; selector en la barra superior (o `?lang=en` / `?lang=pt` en la URL).

## Qué hace

- Recibe las siete clases de evidencia de un título de grado (encuestas, indicadores, quejas y felicitaciones, plan de mejoras, auditoría interna, informes de seguimiento o reacreditación y actas) en Word, PDF, PowerPoint, Excel, texto o pegado, y una tabla de indicadores por plantilla CSV/Excel.
- **Subida por carpeta, ZIP o arrastrando la carpeta:** lee cada documento y lo propone en su categoría según el nombre de la carpeta (peso 3), el del fichero (2) y su contenido (1), en seis idiomas; una tabla CSV/Excel con formato de indicadores se reconoce como tal. La persona revisa y corrige la propuesta antes de importar; se ignoran ficheros ocultos, temporales e imágenes; máximo 300 ficheros por carga. Arrastrar carpetas no se ha probado en pruebas automáticas (sí la elección de carpeta y de ZIP).
- Marcos (v1.1): ANECA/ACREDITA grado, **máster** y **doctorado** (estructura de 3 dimensiones y 7 criterios de la guía ACREDITA DOCTORADO v3.0 de ANECA, 2024), ESG 2015, ARCU-SUR, **EUR-ACE** (EAFSG 2021, 6 criterios) y **ABET** (8 criterios generales, ciclos 2019-2025), un marco común iberoamericano propio (no oficial) y uno personalizado. Los de máster, EUR-ACE y ABET son resúmenes de AcreditIA, no texto oficial: contrasta con la guía vigente de tu agencia.
- **Cargar los criterios de tu agencia:** sube su guía (Word, PDF o texto) o pega el capítulo de criterios; el código detecta dimensiones y criterios por su estructura («Criterio 1. …», «Standard 1.1 …», «1.1 Título»), opcionalmente la IA completa lo que falte (cada criterio debe traer una cita literal que el código comprueba; los que no la tienen quedan marcados y sin incluir), la persona revisa y edita la tabla, lo guarda como marco y puede **exportarlo e importarlo como perfil JSON** para compartirlo entre universidades. No hay perfiles oficiales incluidos de CNA, CONEAU, SINAES, A3ES u otras: se cargan desde su propia guía.
- 19 agentes en 5 fases (lectura, diagnóstico, redacción, plan de mejora, revisión). Los de IA tienen instrucción editable; los de código son deterministas.
- **El código** calcula valor, variación, tendencia y cumplimiento de cada indicador; verifica que cada cita literal exista en su pasaje; detecta cifras sin respaldo, referencias inexistentes y expresiones triunfalistas; limita la valoración propuesta por la IA con reglas objetivas; prioriza las debilidades y valida el plan (cargo, plazo dentro del curso, indicador, meta numérica).
- **La persona** confirma la valoración de cada criterio; queda registrada en una cadena de huellas SHA-256.
- Salidas: autoinforme en Word y Markdown, plan de mejora en Word y CSV, proyecto en JSON.
- Ejemplo ficticio con una IA de demostración (sin clave ni conexión); incluye una cita inventada a propósito para ver cómo el código la descarta.

## Cómo se usa la IA

Con la propia clave de OpenAI, Google Gemini o Anthropic Claude (se guarda solo en el navegador). No hace falta servidor.

## Privacidad

Evidencias, indicadores y resultados se guardan solo en este navegador (IndexedDB). Con un proveedor en la nube salen los pasajes necesarios con correos, DNI/NIE, teléfonos, tratamientos («Dr. …») y los nombres indicados enmascarados, tras un aviso previo con muestra. El JSON exportado incluye el texto de las evidencias y no incluye claves.

## Límites

No hace OCR ni lee imágenes. No sustituye el juicio del comité ni la guía de la agencia ni comprueba el cumplimiento normativo. La IA puede equivocarse: la persona debe revisar cada valoración, texto y acción. Probado con IA simulada; no se ha probado con claves reales.

## Traducciones

Las versiones en catalán/valenciano (formas valencianas), gallego y euskera las ha redactado una IA y **no han sido revisadas por hablantes nativos**: conviene una revisión antes de usarlas en documentos oficiales. El aranés no está incluido.

## Autoría

Fernando Borrás Rocher (Universidad Miguel Hernández de Elche) y David León Espí (Director del Servicio de Calidad, Universidad Miguel Hernández de Elche).

ORCID: Fernando Borrás Rocher [0000-0002-5519-4573](https://orcid.org/0000-0002-5519-4573). David León Espí: sin ORCID por ahora (se añadirá en una versión nueva).

## Cómo citar

Borrás Rocher, F., & León Espí, D. (2026). *AcreditIA* (v1.0.0) [Software]. DOI: [10.5281/zenodo.23276225](https://doi.org/10.5281/zenodo.23276225)

## Licencia

MIT. Véase [LICENSE](LICENSE).
