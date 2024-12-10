## Herencia
● Herencia: Es un mecanismo que permite que un objeto herede propiedades y
comportamientos de otro objeto. Esto fomenta la reutilización del código y la
creación de jerarquías de clases, donde las clases secundarias pueden extender o
modificar el comportamiento de las clases primarias.

## [Ejemplo en el proyecto](https://drive.google.com/file/d/1EeUV1WW-8NHXsGkOTU5TqJrCJVEsE9qA/view?usp=sharing)
![Diagram 2024-12-09 21-27-23](https://github.com/user-attachments/assets/6c2986a2-4a08-464d-a3de-6d63ee5d74c1)


La herencia permite reutilizar código al definir atributos y métodos comunes en una clase base. 
En el proyecto, Usuario actúa como clase general con propiedades compartidas como nombre, mail, telefono y dirección,
mientras que las subclases añaden comportamientos específicos como realizarReserva en Socio o dictarClase en Instructor.
## Ejemplo de Código
    public class Usuario {
     private String nombre;
     private String mail;

    public Usuario(String nombre, String mail) {
        this.nombre = nombre;
        this.mail = mail;
    }

    public void modificarDatos(String nuevoMail) {
        this.mail = nuevoMail;
    }
    }

    public class Socio extends Usuario {
    private String tipoMembresia;

    public Socio(String nombre, String mail, String tipoMembresia) {
        super(nombre, mail);
        this.tipoMembresia = tipoMembresia;
    }
    }
