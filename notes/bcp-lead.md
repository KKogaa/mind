---
title: BCP Lead
tags: [work, project, bcp]
up: "[[goals]]"
---

# BCP Lead

Alcance funcional y preguntas abiertas para el lead financiero.

## Funcionalidades

- registro de usuario
	- formulario de registro (controlado por BCP)
- validacion de KYC
	- validacion de datos
		- widget: escaner de documentos
		- widget: formulario de verificacion de datos
	- validacion biometrica
		- widget: captura facial
- cotizacion (falta en el mockup una calculadora)
	- conversion de divisas
- remesador
	- widget: selector de envio
- pago
	- widget: pasarela de pago
- detalle de la transferencia
	- widget: resumen de pago
- contactos
	- widget: seleccionador de contacto
- rastreo de transferencias
- cupones/puntos/promociones (no cuentan)
- pago de servicios

## Preguntas a lead financiero
- Podrían compartir la documentación técnica completa de la lista de widgets disponibles?
- Cuáles son los formatos de datos de entrada y salida para cada widget?
- Se pueden hacer modificaciones (agregar o remover) sobre los campos de entrada o salida de cada widget?
- Qué nivel de personalización visual permiten los widgets?
- Cómo se integran los widgets con su sistema de autenticación ?
- Cuanto tiempo de duracion tiene la autenticacion de los widgets? 
- El widget de registro de usuario es desacoplable de la biometria y kyc? 
- Tienen apis/webhooks para revisar el estado de las transacciones?

## Notas

- integracion servidor a servidor para asegurar prueba de vida

## Related

- [[work-things-todo]] — day-to-day work items.
- [[career-roadmap]] — current client work.
