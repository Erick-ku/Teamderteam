Descripción General
Esta base de datos forma parte del sistema de asesorías Teamder, diseñado para gestionar el proceso de asesorías académicas entre tutores y usuarios (alumnos).  
Permite administrar solicitudes de asesoría, respuestas de tutores, sesiones realizadas y los temas de interés de los estudiantes.

El modelo relacional busca mantener la integridad de los datos y facilitar el seguimiento del flujo completo desde que un estudiante solicita una tutoría hasta que se realiza.

Estructura Principal

- Entidades y Propósito
| Tabla  |  Descripción |
|--------|--------------|
| Usuario : Contiene los datos personales y académicos de los estudiantes. 
| Interes : Registra las áreas o temas de interés de los usuarios. 
| Especialidad : Define las especialidades disponibles para los tutores. 
| Tutor : Almacena la información de los tutores y su especialidad. 
| Solicitud : Representa las solicitudes de asesoría enviadas por los usuarios. 
| RespuestaTutor : Guarda el estatus y fecha de respuesta del tutor ante una solicitud. 
| TemaAsesoria : Describe los temas que se pueden abordar en las sesiones de asesoría. 
| SesionAsesoria : Contiene la información de las asesorías realizadas (fecha, duración, observaciones). 
| UsuarioSesion : Relaciona a los usuarios con las sesiones de asesoría, permitiendo que varios alumnos participen en una misma sesión (clave primaria compuesta). 

Dependencias y Relaciones Clave

- Un Usuario pertenece a un Interes.  
- Un Tutor pertenece a una Especialidad.  
- Una Solicitud es creada por un Usuario y tiene una posible RespuestaTutor.  
- Una SesionAsesoria está vinculada a un Tutor, una Solicitud y un TemaAsesoria.  
- UsuarioSesion permite que varios usuarios participen en una misma sesión (relación N:M).

# Versión y Mantenimiento

- Versión actual: 1.0.0  
- Última actualización: 06 de noviembre de 2025  
- Autor: Erick, Jefte, Mauro  
- Estado: Activa y en desarrollo inicial
