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
        
Y ahora por tanto en el método principal, podemos crear una persona y crear con este constructor copia una copia de ese mismo objeto.

        public class Principal {
            public static void main(String[] args) {

                // Creamos tres variables que contendrán el dni
                // el nombre y la edad de la persona
                String valorDNI, valorNombre;
                int valorEdad;

                valorDNI="999777555N";
                valorNombre="María";
                valorEdad=22;

                // Creamos un objeto de tipo persona.
                // Entre los paréntesis del constructor
                // se pasan estas variables.
                Persona miPersona=new Persona(valorDNI,valorNombre,valorEdad);

                // Creamos una copia del objeto miPersona.
                Persona copiaPersona=new Persona(miPersona);
            }
        }
