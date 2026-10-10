## 1. Análisis de Requerimientos y Actores

### Actores del Sistema
* *Administrador:* Encargado de la gestión de la plataforma, evaluación y aprobación/rechazo de las solicitudes de adopción.
* *Rescatista / Voluntario:* Responsable del registro y actualización del estado de salud y adopción de las mascotas rescatadas.
* *Adoptante:* Usuario interesado en buscar, filtrar e iniciar solicitudes de adopción de mascotas.

### Casos de Uso Principales
* UC01 - Registrarse / Iniciar Sesión
* UC02 - Registrar Animal Rescatado
* UC03 - Buscar y Filtrar Mascotas
* UC04 - Enviar Solicitud de Adopción
* UC05 - Gestionar y Evaluar Solicitudes

---

## 2. Diagramas UML

El proyecto incluye los diagramas de modelado del sistema elaborados en estándar UML:
1. *Diagrama de Casos de Uso:* Muestra la interacción entre los actores (Administrador, Voluntario, Adoptante) y los módulos de la plataforma.
2. *Diagrama de Clases:* Define las entidades principales (Usuario, Adoptante, Administrador, Animal y SolicitudAdopcion), sus atributos, operaciones, herencia y cardinalidades.

---

## 3. Patrones de Diseño Aplicados

Para garantizar una arquitectura escalable, mantenible y de bajo acoplamiento, se definieron tres patrones de diseño:

1. *Factory Method (Creacional):*
   * Encapsula la creación de los distintos tipos de usuarios (Adoptante, Administrador, Rescatista) sin acoplar el código de autenticación a clases concretas.
2. *Adapter (Estructural):*
   * Adapta servicios externos (como APIs de notificaciones por WhatsApp/SMS) a una interfaz estándar de notificaciones del sistema.
3. *Observer (Comportamiento):*
   * Permite que el estado de la SolicitudAdopcion notifique automáticamente a los observadores (Adoptante y Administrador) cuando cambia de estado (Pendiente, Aprobada, Rechazada).

---

## 4. Estrategia de Ramificación (Gitflow)

El desarrollo del proyecto se gestionó mediante el flujo de trabajo Gitflow utilizando las siguientes ramas:
* main: Rama de producción con las versiones finales de la documentación.
* develop: Rama de integración de características.
* feature/analisis-requerimientos: Levantamiento y análisis de casos de uso.
* feature/modelado-uml: Construcción y exportación de diagramas UML.
* feature/patrones-diseno: Documentación de patrones creacionales, estructurales y de comportamiento.
