## Abstracción
   
_Consiste en simplificar la complejidad del mundo real modelando solo
los aspectos esenciales relevantes para el sistema. Los objetos abstractos
representan entidades del dominio de aplicación y sus interacciones, lo que facilita la
comprensión y el diseño del software._
## [Ejemplo en el proyecto](https://drive.google.com/file/d/1CnJDiuPOrjLsAe-KUfElzPlxJ6EaX53M/view?usp=sharing)
![Diagram 2024-12-09 20-28-45](https://github.com/user-attachments/assets/7ab09734-21a3-4392-84a2-68fe06e20caf)

La clase Clase es un ejemplo, porque encapsula información básica sobre actividades del gimnasio como nombre,
capacidad y nivel de dificultad, dejando los detalles específicos de implementación para las subclases. 
Esto asegura que cualquier clase derivada, como "ClaseBoxeo" o "ClaseCrossFit", pueda añadir comportamientos particulares 
sin alterar el diseño básico.
## Ejemplo de Código
    public abstract class Clase {
       private String nombre;
       private int capacidadMaxima;
       private String nivelDificultad;

    public Clase(String nombre, int capacidadMaxima, String nivelDificultad) {
        this.nombre = nombre;
        this.capacidadMaxima = capacidadMaxima;
        this.nivelDificultad = nivelDificultad;
    }

    public abstract void realizarClase();
    
    public String obtenerInformacion() {
        return "Clase: " + nombre + ", Nivel: " + nivelDificultad;
    }
}


