## Herencia
_Es un mecanismo que permite que un objeto herede propiedades y
comportamientos de otro objeto. Esto fomenta la reutilización del código y la
creación de jerarquías de clases, donde las clases secundarias pueden extender o
modificar el comportamiento de las clases primarias._

## [Ejemplo en el proyecto](https://drive.google.com/file/d/1Tr97FGVhkvZFjed8-46HyCpBIMzhlYWD/view?usp=sharing)
![Diagram 2024-12-09 22-05-31](https://github.com/user-attachments/assets/434bff28-3f41-4571-b557-b849708bd172)



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
