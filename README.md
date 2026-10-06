# Alertas-falsas — Defender XDR Threat Simulator

Simulador visual para seleccionar y descargar escenarios de prueba destinados a generar telemetría y alertas en Microsoft Defender XDR.

> [!CAUTION]
> **NO ejecutes estos scripts en tu computadora principal, equipos de trabajo de usuarios reales, servidores de producción ni dispositivos con datos sensibles.**
>
> Utiliza exclusivamente una **VM, sandbox o equipo dedicado de laboratorio**, dentro de un entorno donde tengas autorización para generar alertas de seguridad.

## Qué hace

La ruleta selecciona escenarios defensivos de laboratorio relacionados con:

- EDR / simulación fileless
- AMSI
- Network Protection / SmartScreen
- PUA
- EICAR
- Behavior Monitoring / masquerading
- Escenario multivector para correlación en Defender XDR

Estas pruebas están diseñadas para provocar detecciones, bloqueos, cuarentenas o incidentes visibles en las herramientas de seguridad.

## Entorno recomendado

Antes de ejecutar cualquier script:

1. Usa Windows dentro de una VM o un endpoint dedicado exclusivamente a pruebas.
2. Crea un snapshot/checkpoint antes de comenzar.
3. No almacenes credenciales, documentos personales ni información corporativa sensible en ese equipo.
4. Usa un tenant/laboratorio de Microsoft Defender donde tengas autorización.
5. Ejecuta una prueba a la vez y revisa los eventos generados antes de continuar.
6. Restaura el snapshot si quieres volver a un estado limpio.

## Advertencias integradas

La interfaz incluye:

- Pantalla de advertencia obligatoria antes de entrar.
- Confirmación explícita de uso en laboratorio.
- Banner persistente indicando que no debe usarse en dispositivos principales.
- Recordatorio visible antes de cada descarga.
- Confirmación final antes de descargar un archivo PowerShell.

## Referencias oficiales

- Microsoft Defender for Endpoint — Demonstration scenarios:
  https://learn.microsoft.com/en-us/defender-endpoint/defender-endpoint-demonstrations
- Microsoft Defender for Endpoint — ASR demonstrations:
  https://learn.microsoft.com/en-us/defender-endpoint/defender-endpoint-demonstration-attack-surface-reduction-rules
- Microsoft Defender for Endpoint — EICAR validation:
  https://learn.microsoft.com/en-us/defender-endpoint/validate-antimalware

## Uso

Abre `index.html` en el navegador dentro de tu entorno de laboratorio y acepta la advertencia inicial.

Selecciona un escenario con la ruleta. Antes de descargar el `.ps1`, la interfaz volverá a pedir confirmación de que estás trabajando en un entorno aislado y autorizado.

## Alcance

Este repositorio es para **simulación defensiva, capacitación y validación de controles de seguridad**. No está diseñado para evasión, persistencia, acceso no autorizado ni ejecución sobre sistemas de terceros.
