Materia: Ingeniería en Sistemas Computacionales
Actividad: Métricas de Calidad en un Proyecto Stellar
Proyecto Analizado: Fluxity (Stellar Community Fund)
Repositorio: https://github.com/luanlabs/fluxity-interface.git

Estudiantes: Cruz Ramírez Jaczibeth - Cruz Ortiz Vanessa - Velasco López Daniel

----------------------------------------------------
Índice

Introducción
Metodología
Fase 1: Selección y Exploración del Proyecto
3.1 Selección del Proyecto
3.2 Exploración del Repositorio
Fase 2: Análisis y Aplicación de Métricas de Calidad
4.1 Cobertura de Pruebas
4.2 Calidad de la Documentación
4.3 Tasa de Resolución de Errores
4.4 Mantenimiento del Código y CI/CD
Discusión Crítica
Fase 3: Conclusiones y Recomendaciones
Referencias

------------------------------------------------------

1. Introducción

La calidad del software es un elemento central en el desarrollo de sistemas confiables, sostenibles y con impacto social. En el contexto de las redes blockchain y de proyectos open-source como los que promueve Stellar Community Fund (SCF), la calidad adquiere mayor relevancia debido a la necesidad de confianza, transparencia y escalabilidad en los servicios financieros descentralizados.

Este informe tiene como propósito aplicar un conjunto de métricas de calidad previamente definidas en un Plan de Calidad académico al análisis de un proyecto real de Stellar. El proyecto seleccionado es Fluxity, una aplicación financiada por SCF cuyo objetivo es construir una interfaz y plataforma de interacción dentro del ecosistema Stellar.

La actividad busca que los estudiantes pasen de la teoría a la práctica, aplicando herramientas de análisis crítico que les permitan identificar el nivel de calidad del software y reflexionar sobre áreas de mejora.


--------------------------------------------------------

2. Metodología

La metodología aplicada en este informe se basó en tres fases principales:

Fase 1: Selección y Exploración -> Se eligió un proyecto de Stellar con repositorio público en GitHub. Se exploró la estructura, archivos clave, historial de commits, PRs, Issues, workflows de CI/CD y documentación.

Fase 2: Análisis de Métricas -> Se aplicaron métricas del Plan de Calidad: cobertura de pruebas, calidad de documentación, tasa de resolución de errores y mantenimiento del código.

Fase 3: Informe y Recomendaciones -> Se redactó un informe con análisis crítico, conclusiones fundamentadas y recomendaciones alineadas a modelos de calidad como CMMI y MoProSoft.

Las métricas se aplicaron de manera cualitativa y cuantitativa, usando la evidencia pública disponible en GitHub.

---------------------------------------------------------

3. Fase 1: Selección y Exploración del Proyecto
3.1 Selección del Proyecto

El proyecto seleccionado es Fluxity, un participante del Stellar Community Fund (SCF). Fue elegido porque:

* Pertenece al ecosistema Stellar.
* Posee un repositorio público en GitHub.
* Presenta actividad en commits, PRs y workflows.
* Su propósito se alinea con el desarrollo de aplicaciones dentro de Soroban y Stellar.

3.2 Exploración del Repositorio

El repositorio luanlabs/fluxity-interface se encuentra en GitHub. La exploración arrojó lo siguiente:
* Lenguaje principal: TypeScript.
* Documentación: Incluye un archivo README.md con descripción inicial del proyecto, aunque breve.
* Estructura: Directorios típicos de interfaz (src/), configuración (package.json, tsconfig.json) y dependencias.
* Historial de PRs: +80 Pull Requests cerradas, con 7 abiertas al momento del análisis.
* Workflows: GitHub Actions activos con al menos 39 ejecuciones (Dependabot + CI).
* Issues: No se observan Issues abiertas en la fecha de análisis.
* Releases: No hay versiones etiquetadas publicadas.

-------------------------------------------------------------

4. Fase 2: Análisis y Aplicación de Métricas de Calidad
4.1 Cobertura de Pruebas
* Evidencia encontrada: No se detectan directorios típicos de testing (tests, jest.config.js, etc.) ni reportes de cobertura en el repo.
* Resultado: Cobertura de pruebas cercana a 0% (no hay test visibles).
* Interpretación: Esto implica un riesgo elevado de defectos no detectados en nuevas versiones.

4.2 Calidad de la Documentación
* Evidencia encontrada: README.md presente, describe de manera básica la instalación y propósito.
* Fortalezas: Incluye instrucciones mínimas para iniciar.
* Debilidades: Falta de documentación extensa (no hay guías de desarrollo, contributing, ni API docs).
* Resultado: Nivel medio-bajo de documentación.

4.3 Tasa de Resolución de Errores
* Evidencia encontrada: No hay Issues abiertas ni histórico visible de resolución. La mayoría del trabajo ocurre en PRs (principalmente Dependabot).
* Resultado: Métrica no cuantificable en términos clásicos (bugs abiertos/cerrados), pero refleja una baja participación comunitaria en reporte de errores.

4.4 Mantenimiento del Código y CI/CD
* Evidencia encontrada: +80 PRs cerradas, 39 ejecuciones de workflows, uso de Dependabot.
* Resultado: Nivel alto de mantenimiento en cuanto a dependencias y flujo de integración.
* Interpretación: El proyecto mantiene un proceso activo de actualización de dependencias, pero depende más de herramientas automatizadas que de testing manual o comunitario.

--------------------------------------------------------------------

5. Discusión Crítica

Los hallazgos muestran un proyecto activo en integración continua y mantenimiento, pero con deficiencias importantes en pruebas y documentación.

Fortalezas:
* Uso de GitHub Actions -> práctica profesional alineada a DevOps.
* Historial de commits y PRs activos -> demuestra mantenimiento.

Debilidades:
* Ausencia de pruebas unitarias -> riesgo de errores en producción.
* Documentación limitada -> barrera de entrada para nuevos colaboradores.
* Falta de Issues abiertos -> refleja baja interacción comunitaria.

El nivel de calidad se percibe aceptable en procesos de integración, pero débil en control de calidad del software.

----------------------------------------------------------------------------

6. Fase 3: Conclusiones y Recomendaciones
Conclusiones:
* Fluxity es un proyecto relevante dentro del ecosistema Stellar, con repositorio activo y procesos de mantenimiento vigentes.
* Las métricas aplicadas muestran que la mayor fortaleza está en la integración continua y actualización de dependencias.

Sin embargo, la calidad general se ve afectada por la falta de pruebas unitarias y documentación sólida.

Recomendaciones que observamos:
* Implementación de pruebas unitarias -> incluir Jest o Mocha con cobertura mínima del 60% (CMMI: nivel 2, MoProSoft: verificación).
* Mejorar documentación -> agregar CONTRIBUTING.md, DEVELOPER_GUIDE.md y ejemplos de uso (CMMI: gestión de procesos, MoProSoft: administración de proyectos).
* Gestión de Issues -> fomentar reporte y resolución de errores para fortalecer retroalimentación (CMMI: soporte, MoProSoft: aseguramiento de calidad).
* Releases semánticas -> etiquetar versiones estables y generar changelogs (CMMI: configuración, MoProSoft: gestión de producto).

------------------------------------------------------------------------------
7. Referencias

* Stellar Community Fund. Fluxity submission. Disponible en: [https://communityfund.stellar.org/dashboard/submissions/recDXtqYuR8g9FMXt]

* GitHub. Fluxity interface repository. Disponible en: [https://github.com/luanlabs/fluxity-interface]
