 ##   Anexo - Aplicación de Patrón de Diseño XXXXX

**Patrón de Diseño Seleccionado:**

**Patrón:** Observer

**Motivación:** El patrón Observer es útil para notificar a otros sistemas o módulos cuando hay cambios o eventos importantes en un sistema. En este caso, cuando un socio se registra o cancela una clase, es necesario que el sistema de reservas reciba una actualización sobre ese cambio. Al aplicar el patrón Observer, podemos desacoplar los componentes del sistema y hacer que el sistema sea más modular y flexible, facilitando su mantenimiento y expansión.

**Implementación del patrón:**
El sujeto sería el sistema de gestión reserva de clases (el objeto que maneja las reservas).
Los observadores  serían los sistemas de notificación (por ejemplo, la reserva de una clase o cancelación de la misma y la notificación a otros socios).

**Ventajas del Patrón Observer:**

**Desacoplamiento:** Los observadores no necesitan saber nada acerca del sujeto (socio), solo necesitan implementar el método +actualizar().

**Extensibilidad:** Si en el futuro necesitan agregar más observadores (por ej. un sistema de marketing), pueden hacerlo sin modificar las clases existentes.

**Flexibilidad:** Se puede agregar o quitar observadores fácilmente sin afectar el funcionamiento principal del sistema.
##  [Estructura de Clases](https://drive.google.com/file/d/11IWOFRKximEFkUaB4nRyEx-70ex8tV-f/view?usp=sharing)
![Diagram 2024-11-28 19-29-05](https://github.com/user-attachments/assets/b8a3d7d8-a5cf-41c7-8a4c-9e4709f269ce)
## Ejemplo de Código

        
        Socio socio1 = new Socio("1", "Maria Gonzalez", "mariagonzalez@gmail.com", "1124524523", true);

        
        SistemaDeNotificaciones notificador = new SistemaDeNotificaciones();
      

       
        socio1.agregarObservador(notificador);
        

        
        socio1.registrarClase();

        
        socio1.cancelarReserva();
    }


