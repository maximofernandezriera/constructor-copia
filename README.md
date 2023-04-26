# El constructor copia

El constructor copia es un tipo de constructor que recibe como parámetro un objeto de la misma clase. En este ejemplo estamos creando objetos de tipo persona, por lo que el constructor recibirá por parámetro un objeto de este tipo.

    public class Persona {
        private String dni;
        private String nombre;
        private int edad;

        // Constructor sin parámentros
        public Persona() {
            this.dni = "";
            this.nombre = "";
            this.edad = 0;
        }

        // Constructor con parámentros
        public Persona(String dni, String nombre, int edad) {
            this.dni = dni;
            this.nombre = nombre;
            this.edad = edad;
        }

        // Constructor copia
        public Persona(Persona objPersona){

            // pasamos a cada variable lo que contiene
            // el cada persona...
            this.dni=objPersona.dni;
            this.nombre=objPersona.nombre;
            this.edad=objPersona.edad;
        }
