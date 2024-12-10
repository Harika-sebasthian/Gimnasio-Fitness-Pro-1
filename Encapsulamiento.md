## Encapsulamiento

  - Es el proceso de ocultar la implementación interna de un objeto y
exponer sólo las interfaces públicas. Esto permite que los objetos mantengan su
estado interno protegido de accesos no autorizados, promoviendo así la
modularidad y la seguridad del sistema.
## Ejemplo en el proyecto
![Diagram 2024-12-09 21-08-54](https://github.com/user-attachments/assets/bc309dad-36a7-473a-ae47-fa5e9bf64d97)
El encapsulamiento protege los datos de acceso directo externo, permitiendo que sean manipulados solo mediante métodos controlados.
En el caso de la clase Socio, los atributos como tipoMembresia o estadoMembresia están restringidos para garantizar que no se alteren
de forma inconsistente.

## Ejemplo de Código
    public class Socio {
     private String tipoMembresia;
      private String estadoMembresia;
       private int nroCarnet;

    public String getTipoMembresia() {
        return tipoMembresia;
    }

    public void setTipoMembresia(String tipoMembresia) {
        this.tipoMembresia = tipoMembresia;
    }

    public boolean esMembresiaValida() {
        return estadoMembresia.equalsIgnoreCase("Activa");
    }

