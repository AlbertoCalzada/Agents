# PROYECTO 2 — AGENTIC SDD / COPILOT

## Checklist completa de instalación y configuración

**Objective:** montar workspace profesional con SDD + Spec Kit + agentes especializados + skills + Orchestrator + guardrails.

**Rule:** execute in order; don’t skip; review prior result.

---

# FASE 0 — PREPARACIÓN

## 0.1 — Crear rama

**Terminal:**

```bash
git checkout -b ai/agentic-sdd
git branch --show-current
```

**Expected:**

```text
ai/agentic-sdd
```

## 0.2 — Comprobar Spec Kit

**Terminal:**

```bash
specify --version
specify check
```

## 0.3 — Inicializar

**Copilot chat:**

```text
/init
```

## 0.4 — Analizar lo generado

**Copilot:**

```text
Analiza la configuración que acabas de generar para este repositorio.

No modifiques ningún archivo.

Indícame:

1. Qué archivos y carpetas relacionados con Copilot, agentes, skills, instrucciones y Spec Kit existen.
2. Para qué sirve cada uno.
3. Qué partes son generadas por Spec Kit.
4. Qué partes deberíamos mantener.
5. Qué partes deberíamos modificar posteriormente para construir nuestro sistema Agentic SDD.

No crees archivos nuevos ni hagas cambios.
```

## 0.5 — Revisar

Guardar el resumen de Copilot. No modificar nada todavía.

---

# FASE 1 — INSTRUCCIONES GLOBALES

## 1.1 — Crear instrucciones globales

**Copilot:**

```text
Analiza el repositorio y crea unas instrucciones globales para GitHub Copilot que definan las reglas generales de desarrollo de este proyecto.

Quiero que sean concisas y no contengan información específica que debería pertenecer a documentación, skills o agentes especializados.

Incluye únicamente reglas globales como:
- principios de desarrollo
- seguridad
- calidad
- mantener el scope solicitado
- no inventar información
- respetar la arquitectura existente
- cuándo pedir aclaraciones
- cuándo solicitar aprobación humana

No inventes convenciones que no puedas verificar en el repositorio.

Crea o modifica únicamente el archivo de instrucciones globales correspondiente.
```

## 1.2 — Revisar instrucciones

**Copilot:**

```text
Revisa las instrucciones globales que acabas de crear.

Comprueba que:
- no contienen información duplicada que debería estar en documentación
- no contienen procedimientos que deberían ser skills
- no contienen responsabilidades específicas de un agente
- no contienen información inventada
- son aplicables a todo el proyecto

Si encuentras problemas, corrígelos.
```

---

# FASE 2 — DOCUMENTACIÓN

## 2.1 — Analizar documentación

**Copilot:**

```text
Analiza toda la documentación existente del repositorio.

No modifiques ningún archivo.

Identifica:
- documentación oficial
- documentación técnica
- documentación experimental o personal
- documentación obsoleta
- información útil para agentes de IA
- información importante que actualmente no está documentada

No inventes información.
```

## 2.2 — Diseñar estructura

**Copilot:**

```text
Basándote en el análisis anterior, propón una estructura de documentación adecuada para este proyecto.

La documentación debe servir tanto a desarrolladores como a agentes de IA.

Separa conceptualmente:
- arquitectura
- dominio y funcionalidades
- desarrollo
- testing
- operaciones/troubleshooting
- cualquier otra categoría que realmente sea necesaria

No muevas, borres ni modifiques archivos existentes.

No crees archivos nuevos todavía.
```

## 2.3 — Crear documentación base

**Copilot:**

```text
Implementa la estructura de documentación que hemos definido.

Utiliza únicamente información verificable del repositorio.

No inventes información.

No sobrescribas documentación existente sin necesidad.

Cuando exista información incompleta o dudosa, indícalo en lugar de asumirla.
```

---

# FASE 3 — INSTRUCCIONES ESPECÍFICAS

## 3.1 — Backend

**Copilot:**

```text
Analiza cómo está desarrollado actualmente el backend de este proyecto.

Crea las instrucciones específicas que deberá seguir un agente especializado en backend.

Incluye únicamente convenciones verificables del proyecto:
- arquitectura
- estructura
- patrones
- acceso a datos
- errores
- logging
- async
- testing
- seguridad
- convenciones de código

No inventes reglas.

Estas instrucciones deben complementar las instrucciones globales, no duplicarlas.
```

## 3.2 — Frontend

**Copilot:**

```text
Analiza el frontend del proyecto y crea las instrucciones específicas para un agente especializado en frontend.

Incluye únicamente convenciones verificables sobre:
- arquitectura
- componentes
- servicios
- estado
- comunicación con backend
- testing
- estilos
- estructura

No inventes información ni dupliques las instrucciones globales.
```

## 3.3 — Testing

**Copilot:**

```text
Analiza cómo se realizan actualmente los tests en este proyecto.

Crea instrucciones específicas para un agente especializado en testing.

Incluye:
- frameworks utilizados
- ubicación de tests
- tipos de tests
- convenciones
- criterios de validación
- comandos existentes

No inventes información.
```

---

# FASE 4 — SKILLS

## 4.1 — Analizar skills necesarias

**Copilot:**

```text
Analiza el proyecto y determina qué skills serían realmente útiles para nuestros agentes.

Una skill debe representar un procedimiento reutilizable para realizar una tarea concreta.

No crees ninguna todavía.

Para cada skill propuesta indica:
- nombre
- objetivo
- agente que la utilizaría
- cuándo debería utilizarse
- información del proyecto que necesita
- si debería ser genérica o específica del proyecto

Evita crear skills innecesarias o duplicadas.
```

## 4.2 — Crear skills

**Copilot:**

```text
Crea las skills que hemos aprobado.

Cada skill debe:
- tener un objetivo claro
- indicar cuándo utilizarla
- contener pasos concretos
- utilizar las convenciones reales del proyecto
- evitar duplicar instrucciones globales
- evitar duplicar documentación
- no inventar información

No crees skills adicionales fuera de las aprobadas.
```

---

# FASE 5 — AGENTES

## 5.1 — SDD Orchestrator

**Copilot:**

```text
Crea un agente llamado SDD Orchestrator para este proyecto.

Su responsabilidad será coordinar el desarrollo mediante Spec-Driven Development.

Debe coordinar estas fases:

1. Entender la petición
2. Detectar ambigüedades
3. Specification
4. Clarification
5. Planning
6. Tasks
7. Implementación
8. Testing
9. Review
10. Convergencia

Debe decidir qué agente especializado debe intervenir en cada fase.

Debe utilizar las skills disponibles cuando sean necesarias.

No debe inventar información.

Debe pedir aclaraciones cuando falte información relevante.

Debe mantener el trabajo dentro del scope solicitado.

Debe solicitar aprobación humana en los puntos que hayamos definido.

No implementes funcionalidades de ejemplo. Crea únicamente la configuración del agente.
```

## 5.2 — Backend Agent

**Copilot:**

```text
Crea un agente especializado en backend.

Debe:
- encargarse de cambios backend
- utilizar las instrucciones de backend
- utilizar las skills correspondientes
- respetar la arquitectura existente
- crear/modificar tests cuando corresponda
- no modificar frontend salvo que el Orchestrator se lo indique
- pedir aclaraciones cuando sea necesario
- no inventar APIs, patrones o comportamiento

Debe trabajar como agente especializado dentro del SDD Orchestrator.
```

## 5.3 — Frontend Agent

**Copilot:**

```text
Crea un agente especializado en frontend.

Debe:
- encargarse de cambios frontend
- utilizar las instrucciones de frontend
- utilizar las skills correspondientes
- respetar la arquitectura existente
- crear/modificar tests cuando corresponda
- no modificar backend salvo que el Orchestrator se lo indique
- pedir aclaraciones cuando sea necesario

Debe trabajar como agente especializado dentro del SDD Orchestrator.
```

## 5.4 — Testing Agent

**Copilot:**

```text
Crea un agente especializado en testing.

Debe:
- analizar los requisitos
- diseñar los tests necesarios
- implementar tests
- ejecutar los tests disponibles
- analizar fallos
- comprobar regresiones
- utilizar las instrucciones y skills de testing

Debe trabajar como agente especializado dentro del SDD Orchestrator.
```

## 5.5 — Reviewer Agent

**Copilot:**

```text
Crea un agente especializado en revisión.

Debe revisar:
- cumplimiento de la specification
- implementación
- arquitectura
- calidad del código
- tests
- posibles regresiones
- seguridad
- cambios innecesarios
- cumplimiento del scope

Debe producir problemas concretos y accionables.

No debe realizar cambios automáticamente salvo que el Orchestrator se lo solicite.
```

---

# FASE 6 — AUTOMATIZAR SDD

## 6.1 — Diseñar flujo

**Copilot:**

```text
Analiza la configuración actual de Spec Kit y de nuestros agentes.

Diseña cómo debe funcionar un flujo SDD automatizado en el que el usuario pueda realizar una petición de funcionalidad al SDD Orchestrator sin tener que ejecutar manualmente cada comando de Spec Kit.

El flujo debe cubrir:

Specification
Clarification
Planning
Tasks
Implementation
Testing
Review

Indica exactamente qué agente interviene en cada fase, qué skills utiliza y qué artefactos produce.

No modifiques archivos todavía.
```

## 6.2 — Implementar automatización

**Copilot:**

```text
Implementa el flujo SDD automatizado que hemos aprobado.

El usuario debe poder iniciar el proceso desde el SDD Orchestrator con una petición normal.

El Orchestrator debe coordinar las fases de Spec Kit y los agentes especializados sin requerir que el usuario lance manualmente cada fase.

Respeta los artefactos y convenciones existentes de Spec Kit.

No elimines funcionalidades existentes de Spec Kit.
```

---

# FASE 7 — GUARDRAILS

## 7.1 — Límites de los agentes

**Copilot:**

```text
Revisa todos nuestros agentes, skills e instrucciones.

Define y aplica guardrails para evitar que los agentes:

- inventen información
- trabajen fuera del scope
- modifiquen archivos innecesarios
- ignoren la arquitectura existente
- eliminen información sin aprobación
- realicen cambios destructivos sin aprobación
- salten fases importantes del proceso SDD

Aplica únicamente guardrails coherentes con el proyecto.
```

## 7.2 — Aprobaciones humanas

**Copilot:**

```text
Define el sistema de aprobación humana del SDD Orchestrator.

Quiero aprobación antes de:
- cambios arquitectónicos importantes
- operaciones destructivas
- cambios de base de datos potencialmente peligrosos
- cambios de seguridad relevantes
- modificaciones fuera del scope
- cualquier acción que pueda afectar significativamente al proyecto

Las fases de análisis, specification y planificación deberían poder realizarse sin aprobación siempre que no modifiquen código.

Implementa estas reglas en la configuración de los agentes.
```

### Regla Git

> Los agentes **NO gestionan Git por ahora**. El usuario hace ramas, commits, push, pull, merge y demás operaciones Git. Los agentes trabajan sobre los archivos locales permitidos y el usuario revisa el diff.

---

# FASE 8 — PRIMERA PRUEBA REAL

## 8.1 — Elegir feature

Elegir una funcionalidad pequeña y de bajo riesgo del Proyecto 2.

## 8.2 — Lanzar SDD

**Copilot:**

```text
Quiero implementar [FUNCIONALIDAD].

Utiliza el flujo SDD completo.

No empieces a modificar código hasta completar y presentar:
1. Specification
2. Clarifications necesarias
3. Plan
4. Tasks

Después espera mi aprobación antes de implementar.
```

## 8.3 — Aprobar implementación

**Copilot:**

```text
Aprobado. Continúa con la implementación siguiendo el plan y las tasks aprobadas.
```

## 8.4 — Testing

**Copilot:**

```text
Continúa con la fase de testing.

Ejecuta los tests necesarios, analiza los resultados y corrige los problemas relacionados con la funcionalidad implementada.

No amplíes el scope.
```

## 8.5 — Review

**Copilot:**

```text
Ejecuta la revisión final de la implementación.

Comprueba:
- specification
- plan
- implementación
- tests
- regresiones
- arquitectura
- scope

Si encuentras problemas, indícalos y corrígelos únicamente si están dentro del scope aprobado.
```

---

# FASE 9 — MEJORA DEL SISTEMA

## 9.1 — Analizar problemas

**Copilot:**

```text
Analiza todo el flujo SDD que acabamos de ejecutar.

Identifica:
- pasos innecesarios
- pasos que faltaron
- instrucciones ambiguas
- skills innecesarias
- información duplicada
- problemas del Orchestrator
- problemas de los agentes especializados
- puntos donde fue necesaria intervención manual

No hagas cambios todavía.
```

## 9.2 — Aplicar mejoras

**Copilot:**

```text
Aplica únicamente las mejoras que hemos aprobado.

No cambies el comportamiento general del sistema fuera de esas mejoras.
```

---

# FASE 10 — PROYECTO 1

## 10.1 — Analizar reutilización

**Copilot:**

```text
Compara la configuración Agentic SDD actual con las necesidades de este proyecto.

Identifica qué componentes son reutilizables directamente y cuáles necesitan adaptación.

Separa:
- configuración genérica
- configuración específica del proyecto
- documentación
- skills
- instrucciones
- agentes

No modifiques nada todavía.
```

## 10.2 — Adaptar

Trasladar/adaptar el sistema al Proyecto 1, manteniendo separado el contexto específico de cada proyecto.

---

# CHECKLIST

## FASE 0

- [ ] 0.1 Crear rama
- [ ] 0.2 Comprobar Spec Kit
- [ ] 0.3 `/init`
- [ ] 0.4 Analizar configuración
- [ ] 0.5 Revisar

## FASE 1

- [ ] 1.1 Instrucciones globales
- [ ] 1.2 Revisar

## FASE 2

- [ ] 2.1 Analizar documentación
- [ ] 2.2 Diseñar estructura
- [ ] 2.3 Crear documentación

## FASE 3

- [ ] 3.1 Backend
- [ ] 3.2 Frontend
- [ ] 3.3 Testing

## FASE 4

- [ ] 4.1 Analizar skills
- [ ] 4.2 Crear skills

## FASE 5

- [ ] 5.1 SDD Orchestrator
- [ ] 5.2 Backend Agent
- [ ] 5.3 Frontend Agent
- [ ] 5.4 Testing Agent
- [ ] 5.5 Reviewer Agent

## FASE 6

- [ ] 6.1 Diseñar automatización SDD
- [ ] 6.2 Implementar automatización

## FASE 7

- [ ] 7.1 Guardrails
- [ ] 7.2 Aprobaciones humanas

## FASE 8

- [ ] 8.1 Elegir feature
- [ ] 8.2 Specification / Plan / Tasks
- [ ] 8.3 Implementación
- [ ] 8.4 Testing
- [ ] 8.5 Review

## FASE 9

- [ ] 9.1 Analizar problemas
- [ ] 9.2 Aplicar mejoras

## FASE 10

- [ ] 10.1 Analizar reutilización
- [ ] 10.2 Adaptar al Proyecto 1
