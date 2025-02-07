 Historias de Usuario Clave

1. Historia: Como Data Partner, quiero subir imágenes anonimizadas a STA

Criterios de Aceptación:
  - El sistema debe recibir imágenes en formato DICOM.
  - Debe ejecutar un proceso automático de anonimización.
  - Los datos anonimizados deben almacenarse correctamente.

2.  Historia: Como Científico de Datos, quiero acceder a imágenes médicas para entrenar modelos de IA

Criterios de Aceptación:
   -El usuario debe poder filtrar imágenes según modalidad, patología y región anatómica.
   -La descarga debe estar disponible en DICOM o JSON.
   -Debe existir una API para consultas avanzadas.

3. Historia: Como Responsable de Cumplimiento, quiero asegurarme de que todas las imágenes sean anonimizadas conforme a HIPAA

Criterios de Aceptación:
 - El sistema debe detectar y eliminar automáticamente cualquier información sensible.
 - Se debe generar un reporte de auditoría tras el proceso de anonimización.
 - No debe existir forma de recuperar datos identificables de un paciente.


**Punto de vista de contexto** 

Identificar requerimeinto de calidad
