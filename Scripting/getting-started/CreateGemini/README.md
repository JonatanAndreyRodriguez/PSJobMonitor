Este proceso, puede realizar las siguientes tareas con respecto al Gemini y al Job:

- Crear un Gemini a un Job que no tenga uno asociado.
- Añadir un comentario a un Gemini no cerrado.
- Registrar un Job en la base de datos de Monitoreo, cuando no exista debido a que fue creado de forma posterior
  a la ejecución de la función Import-MonitoredJob
- Actualizar el estado del Gemini asociado a un Job en la base de datos, cuando este ya se ha cerrado.
- Hacer envío de notificación Push a dispositivos móviles debido a un Job reportado como fallido, cuando está 
  categorizado como crítico y, siempre y cuando sea en la fase de creación de Gemini.
  