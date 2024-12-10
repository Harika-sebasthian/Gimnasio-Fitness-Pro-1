## Polimorfismo
_Se refiere a la capacidad de los objetos de una misma jerarquía de
clases para responder de manera diferente a un mismo mensaje. Esto permite
escribir código genérico que puede funcionar con varios tipos de objetos,
promoviendo la flexibilidad y la extensibilidad del sistema._

## [Ejemplo en el proyecto](https://drive.google.com/file/d/15NHUlOJtmb2XdZPlsFhqAkpmp87AWfAW/view?usp=sharing)
![Diagram 2024-12-09 21-51-47](https://github.com/user-attachments/assets/04e490c5-9dc2-4401-8dca-90b217c0cb6d)



El polimorfismo permite que objetos de diferentes clases respondan al mismo mensaje (método) de diferentes maneras.
La clase Notificador ejemplifica este principio, ya que diferentes tipos de notificaciones (Email, SMS) implementan el mismo método enviarNotificacion() con comportamientos específicos.
## Ejemplo de Código
    public interface Notificador {
    void enviarNotificacion(String mensaje);
    }

    public class NotificadorEmail implements Notificador {

    public void enviarNotificacion(String mensaje) {
        System.out.println("Enviando Email: " + mensaje);
    }
    }

    public class NotificadorSMS implements Notificador {
    public void enviarNotificacion(String mensaje) {
        System.out.println("Enviando SMS: " + mensaje);
    }
     }
