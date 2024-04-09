# Sistema de Notificaciones Persistente para Exámenes de Salud Físico y Médico Dental

## Descripción

Este sistema está diseñado para automatizar el envío de recordatorios por correo electrónico a los padres o tutores de niños que necesitan someterse a una evaluación médico dental. Utilizando Google App Script y Google Forms, el sistema enviará notificaciones en intervalos específicos (30, 15, 5, y 2 días antes del límite de 30 días) después de la inscripción, recordando a los padres sobre la evaluación pendiente.

## Objetivo

El principal objetivo es asegurar que los padres estén informados y tengan suficiente tiempo para completar las evaluaciones requeridas, proporcionándoles recursos útiles y asistencia en caso de necesidades económicas.

## Configuración

### Prerrequisitos

- Una cuenta de Google Workspace.
- Conocimientos básicos de Google App Script y manejo de Google Forms.

### Pasos Iniciales

1. **Crear un Google Form**: Diseñar un formulario para registrar a los padres o tutores, recopilando información esencial como el nombre del niño, el email del padre/tutor, y la fecha de inscripción.
2. **Configurar Google Sheet**: Establecer una hoja de cálculo para recopilar las respuestas del formulario. Esta hoja servirá como base de datos para el envío de notificaciones.

## Implementación

### Google App Script

1. **Script de Notificaciones**: Desarrollar un script en Google App Script que:
   - Lea los registros de la hoja de cálculo.
   - Calcule los días restantes hasta el límite de 30 días desde la fecha de inscripción.
   - Envíe los correos electrónicos de notificación en los días especificados (30, 15, 5, y 2 días antes del límite).

### Lógica del Script

- **Inscripción y activación de notificaciones**: Al registrar a un niño, el sistema activará automáticamente las notificaciones según la fecha de inscripción.
- **Contenido del Correo Electrónico**: Personalizar el mensaje para incluir el número de días restantes, recursos útiles y una lista de bases de datos de asistencia.

### Cron Job

- **Automatización**: Configurar un disparador de tiempo (time-driven trigger) en Google App Script para ejecutar el script de notificación diariamente.

## Uso

### Registro

Los padres o tutores deben llenar el Google Form provisto para iniciar el proceso de notificaciones.

### Recibir Notificaciones

- Las notificaciones se enviarán automáticamente según el cronograma establecido después de la inscripción.
- En caso de no someter la evaluación dentro del límite de tiempo, el sistema puede enviar un formulario adicional para indagar sobre las razones (económicas o de otra índole) y ofrecer asistencia.
