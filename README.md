# Examen_COD

1. Primero hice un clone al repositorio del profesor y entre en la consola para hacer un git clone con el enlace que copie

2. Luego vamos a IDEA y abrimos desde open el repositorio que hemos clonado

3. El siguiente paso es hacer Push y poner el origen para que se enlace con NUESTRO repositorio

## Cuando terminemos esto nos pondremos ahora con el diagrama de flujo

Creamos un draw.io y empezamos a hacer el diagrama de flujo como esta en pantalla
![Captura de pantalla_2024-12-13_09-35-57](https://github.com/user-attachments/assets/6ef9b28d-5160-4edb-9019-5fef78ab905b)

1. Primero cree una tabla llamada "Tablero" y use dos for para recorrer las filas y columnas 

2. Seguido agrege un **if** en caso de que la tabla este vacia y si no, contar tanto las fichas negras y blancas en el tablero.

3. Para terminar agrege un **if else** para determinar si las fichas blancas iban ganando o perdiendo contra las negras y un else por si iban empate

4. Por cada modificaion no olvidarse de hacer GIT y +ADD para luego seleccionar el class con el que estoy trabajando y hacer commit

## Codificacion


        public class Codificacion {
        }
        public class Damas {
            public static void main(String[] args) {
            // Representación del tablero:
            // 'B' = ficha del jugador blanco
            // 'N' = ficha del jugador negro
            // ' ' = casilla vacía
                char[][] tablero = {
                    {'B', ' ', 'B', ' ', 'B', ' ', 'B', ' '},
                    {' ', 'B', ' ', 'B', ' ', 'B', ' ', 'B'},
                    {'B', ' ', 'B', ' ', 'B', ' ', 'B', ' '},
                    {' ', ' ', ' ', ' ', ' ', ' ', ' ', ' '},
                    {' ', ' ', ' ', ' ', ' ', ' ', ' ', ' '},
                    {' ', 'N', ' ', 'N', ' ', 'N', ' ', 'N'},
                    {'N', ' ', 'N', ' ', 'N', ' ', 'N', ' '},
                    {' ', 'N', ' ', 'N', ' ', 'N', ' ', 'N'}
                };
                int contadorBlancas = 0;
                int contadorNegras = 0;

                // Recorrer el tablero
                for (int fila = 0; fila < 8; fila++) {
                    for (int columna = 0; columna < 8; columna++) {
                        char ficha = tablero[fila][columna];

                        if (ficha != ' ') { // Si la casilla no está vacía
                        // Mostrar coordenada y tipo de ficha
                        System.out.println("Casilla ocupada en (" + fila + ", " + columna + ") por una ficha " + (ficha == 'B' ? "blanca" : "negra"));

                        // Contar fichas según el tipo
                        if (ficha == 'B') {
                            contadorBlancas++;
                        } else if (ficha == 'N') {
                            contadorNegras++;
                        }
                    }
                }
            }

            // Mostrar el conteo de fichas
            System.out.println("\nTotal de fichas blancas: " + contadorBlancas);
            System.out.println("Total de fichas negras: " + contadorNegras);

            // Determinar quién va ganando
            if (contadorBlancas > contadorNegras) {
                System.out.println("\nEl jugador blanco va ganando.");
            } else if (contadorNegras > contadorBlancas) {
                System.out.println("\nEl jugador negro va ganando.");
            } else {
                System.out.println("\nAmbos jugadores están empatados.");
            }
        }
    }


## Visualmente se veria algo asi

![Captura de pantalla_2024-12-13_09-09-01](https://github.com/user-attachments/assets/d7b07ae2-8e27-4e6d-93d3-a32c5c3968e7)

