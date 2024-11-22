# Steven Granda Palencia
## java 8 en adelante.
## Visual Studio Code. v.1.95.3
------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
# Gramática y Árboles Sintácticos

Este proyecto en Java tiene como objetivo mostrar los pasos de derivación y los árboles sintácticos generados a partir de una gramática libre de contexto (CFG) y una expresión matemática ingresada por el usuario. La aplicación genera dos tipos de árboles: el árbol de derivación y el árbol de sintaxis abstracta (AST).

## Características

- **Entrada de Gramática y Expresión:** El usuario puede ingresar una gramática en formato BNF (Backus-Naur Form) y una expresión matemática que será procesada.
- **Generación de Árboles Sintácticos:** El programa genera dos árboles sintácticos:
  - Árbol de derivación, que muestra los pasos de la derivación de la expresión.
  - Árbol de sintaxis abstracta (AST), que simplifica la expresión eliminando detalles innecesarios.
- **Interfaz Gráfica:** Interfaz construida con Java Swing, que permite al usuario ingresar la gramática y expresión, seleccionar el tipo de expansión (izquierda o derecha), y visualizar los árboles generados.
- **Derivación Paso a Paso:** Los pasos de derivación de la expresión se muestran en un área de texto.

## Estructura del Proyecto

El proyecto está compuesto por las siguientes clases principales:

### 1. `Arbol` (Interfaz Gráfica)
   Esta clase gestiona la interfaz gráfica del usuario (GUI), donde se muestran los campos de entrada para la gramática y la expresión, así como los resultados de la derivación y los árboles sintácticos. Se encarga de la organización de los componentes visuales y la interacción con el usuario.

### 2. `GrammarProcessor` (Procesador de la Gramática)
   Esta clase se encarga de procesar la gramática ingresada y derivar la expresión paso a paso. También genera los árboles de derivación y de sintaxis abstracta (AST).

### 3. `TreeNode` (Nodo de los Árboles Sintácticos)
   La clase `TreeNode` representa un nodo dentro de los árboles de derivación y de sintaxis abstracta. Cada nodo tiene un valor (símbolo de la gramática) y puede tener nodos hijos izquierdo y derecho.

## Instrucciones de Uso

1. **Ejecutar el Proyecto:**
   - Descarga o clona el repositorio.
   - Abre el proyecto en tu IDE favorito.
   - Ejecuta la clase `GrammarTreeGUI` para iniciar la interfaz gráfica.

2. **Ingreso de Datos:**
   - Ingresa la gramática en el área de texto superior, utilizando la notación de Backus-Naur (BNF). Ejemplo:
     ```
     E -> E + T | T
     T -> T * F | F
     F -> ( E ) | id
     ```
   - Ingresa la expresión a procesar en el campo de texto correspondiente.

3. **Generación de Árboles:**
   - Selecciona el tipo de expansión (izquierda o derecha) en el ComboBox.
   - Haz clic en el botón "Generar Derivación" para ver los pasos de derivación y los árboles sintácticos.

4. **Visualización:**
   - Los pasos de derivación se mostrarán en el área de texto.
   - Los árboles sintácticos (derivación y AST) se dibujarán en los paneles correspondientes.
