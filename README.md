# Motor de Vacío

[![License: CC BY-NC 4.0](https://img.shields.io/badge/License-CC_BY--NC_4.0-lightgrey.svg)](https://creativecommons.org/licenses/by-nc/4.0/)

**Motor térmico que opera por presión diferencial, no por combustión. Cero emisiones.**

El Motor de Vacío utiliza la presión atmosférica como fuente de energía y el vacío como "combustible" almacenable. Al expandir un gas a presión atmosférica dentro de un cilindro previamente evacuado, se genera movimiento mecánico sin explosión ni combustión.

---

## ¿Cómo funciona?

1. **Acumulador de vacío** mantiene una presión negativa (-50 a -80 kPa relativo).
2. **Válvula de admisión** se abre, permitiendo que el aire a presión atmosférica entre al cilindro.
3. **El pistón se desplaza** por la diferencia de presión, generando trabajo mecánico.
4. **Válvula de escape** libera el aire a presión atmosférica, reiniciando el ciclo.

A diferencia de un motor térmico convencional, no hay explosión, no hay combustión, no hay emisiones.

---

## Principio de operación



┌─────────────────────────────────────────────────────────────┐
│ MOTOR DE VACÍO │
│ │
│ [Acumulador de vacío] ← [Bomba CFM] (mantenimiento)      │
│ │                                                        │
│ ▼                                                        │
│ [Válvula de admisión] (control digital)                  │
│ │                                                        │
│ ▼                                                        │
│ [Cilindro] ← [Pistón] (movido por presión atmosférica)   │
│ │                                                        │
│ ▼                                                        │
│ [Válvula de escape] (solo aire a presión atmosférica)    │
└─────────────────────────────────────────────────────────────┘



---

## Especificaciones técnicas

| Parámetro | Valor | Notas |
|-----------|-------|-------|
| Presión de trabajo | -50 a -80 kPa (relativo) | Vacío parcial, no requiere alto vacío |
| Consumo de vacío | Variable según carga | — |
| Autonomía con acumulador lleno | 2–5 minutos | Sin bomba funcionando |
| Potencia estimada | 1–5 kW | Según cilindrada y presión |
| Emisiones | Cero | No hay combustión |
| Ruido | Bajo | Sin explosiones |

---

## Componentes principales

| Componente | Función | Tecnología / Proveedor |
|------------|---------|------------------------|
| **Bomba CFM** | Mantener vacío en acumulador | Bombas de vacío industriales (ej. Busch, Becker) |
| **Acumulador de vacío** | Almacenar vacío para operación continua | Tanque de presión con válvulas |
| **Válvulas** | Control de admisión y escape | Electroválvulas de respuesta rápida (ej. SMC, Festo) |
| **Cilindro/pistón** | Convertir presión diferencial en movimiento | Diseño adaptado de motores térmicos |
| **Sensores** | Monitoreo de presión absoluta, diferencial, temperatura | Sensores industriales (ej. Honeywell, Siemens) |
| **Centralita (ECU)** | Control digital de tiempos y mapas | Programable con Arduino, Raspberry Pi o PLC industrial |

---

## Ciclo de trabajo

| Fase | Duración | Acción |
|------|----------|--------|
| **1. Admisión** | Variable | Válvula de admisión abre. El aire atmosférico entra al cilindro, empujando el pistón. |
| **2. Expansión** | Variable | El pistón se desplaza hasta el final de carrera. |
| **3. Escape** | Variable | Válvula de escape abre. El aire se libera a la atmósfera. |
| **4. Retorno** | Variable | El pistón retorna por inercia, resorte o mecanismo auxiliar. |

---

## Ventajas diferenciales

| Ventaja | Descripción |
|---------|-------------|
| **Cero emisiones** | No hay combustión. El aire expulsado es el mismo que entró. |
| **Sin combustible fósil** | Funciona con vacío almacenable, que puede generarse con energía renovable. |
| **Funcionamiento silencioso** | Sin explosiones ni detonaciones. Ruido comparable a un compresor. |
| **Posible integración con renovables** | La bomba CFM puede alimentarse con energía solar, eólica o excedentes de red. |

---

## Estado actual

✅ Principio físico validado (presión atmosférica + vacío)  
✅ Bomba CFM: tecnología existente  
✅ Acumulador de vacío: tecnología existente  
✅ Válvulas: tecnología existente  
🔲 Integración del sistema completo  
🔲 Control digital (ECU)  
🔲 Prototipo funcional  
🔲 Pruebas de eficiencia y autonomía

---

## Próximos pasos

1. **Diseño mecánico** — Selección de cilindro/pistón adaptado o diseño propio.
2. **Control digital** — Programación de ECU con mapas de tiempos y sensores.
3. **Prototipo** — Ensamblaje de componentes existentes en un banco de pruebas.
4. **Pruebas** — Medición de potencia, consumo de vacío, autonomía real.
5. **Integración con renovables** — Conexión de bomba CFM a energía solar o eólica.

---

## Proyectos relacionados

- **HidroFix** — seguridad para celdas de hidrógeno  
  [Repositorio](https://github.com/enriqueherbertag-lgtm/Hidrofix)
- **ShieldAir** — torres de producción de oxígeno  
  [Urban](https://github.com/enriqueherbertag-lgtm/ShieldAir-Urban) | [Mars](https://github.com/enriqueherbertag-lgtm/ShieldAir-Mars)

---

## Licencia

Apache 2.0 con restricción de uso comercial.  
*Este es un framework base open-source. El que quiera más precisión, menor latencia o features avanzadas… que lo modifique y contribuya.*

---

## Autor

**Enrique Aguayo H.**  
Investigador independiente, Mackiber Labs  
Contacto: eaguayo@migst.cl  
ORCID: 0009-0004-4615-6825  
GitHub: [@enriqueherbertag-lgtm](https://github.com/enriqueherbertag-lgtm)




