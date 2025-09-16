# Actividad Python con Tkinter

Este repositorio contiene dos scripts de Python que implementan aplicaciones de escritorio sencillas utilizando la biblioteca **Tkinter** para la interfaz gráfica de usuario (GUI).

---

## 1. Adivinar número de 1 a 100 (`Adivinar numero de 1 a 100.py`)

### 📝 Descripción

Este programa implementa un **juego de adivinanzas** clásico. Genera un número entero aleatorio entre **1 y 100** y le pide al usuario que lo adivine.

La interfaz de usuario utiliza `tkinter` para:
* Mostrar una etiqueta con instrucciones.
* Proporcionar una caja de texto (`Entry`) para que el usuario ingrese su intento.
* Ofrecer un botón para validar la adivinanza.
* Mostrar mensajes informativos (`messagebox`) indicando si el número secreto es **mayor**, **menor** o si el usuario ha **acertado**.
* Incluye validación para asegurar que la entrada sea un número entero y esté dentro del rango permitido (1 a 100).

### ⚙️ Funcionalidades Principales

* **Generación Aleatoria:** Usa `random.randint(1, 100)` para establecer el número secreto al inicio.
* **Función `adivinar()`:** Maneja la lógica del juego:
    * Captura la entrada del usuario.
    * Maneja errores si la entrada no es un número (`ValueError`).
    * Comprueba si el número está fuera del rango (1-100).
    * Compara la entrada con el número secreto y proporciona pistas.
* **GUI:** Configura la ventana, etiqueta, caja de texto y botón.

---

## 2. Gestor de Recetas (`Recetas.py`)

### 📝 Descripción

Este programa es una aplicación de gestión que permite a los usuarios **agregar**, **ver** y **eliminar** recetas. Cada receta se almacena con un **nombre** y una lista de **ingredientes**. La aplicación también usa `tkinter` para la interfaz y estructuras de datos orientadas a objetos para manejar la información.

### 🧩 Estructura Orientada a Objetos (POO)

El código se organiza con dos clases principales:

1.  **`Receta`**:
    * Representa una receta individual.
    * Atributos: `nombre` (str) e `ingredientes` (list de str).
2.  **`GestorRecetas`**:
    * Maneja la colección de recetas.
    * Almacena las recetas en una lista interna (`self.recetas`).
    * Métodos: `agregar_receta(nombre, ingredientes)` y `eliminar_receta(indice)`.

### ⚙️ Funcionalidades Principales

* **Agregar Receta:** Permite ingresar un nombre y una lista de ingredientes (separados por coma) para añadirlos al gestor y a la lista visible (`Listbox`).
* **Ver Ingredientes:** Muestra los ingredientes de la receta seleccionada en un cuadro de mensaje.
* **Eliminar Receta:** Borra la receta seleccionada del gestor y de la lista visible.
* **Manejo de Errores:** Valida que se ingrese un nombre y al menos un ingrediente al agregar, y que haya una selección al ver o eliminar.
* **Ayuda e Información:** Incluye botones para mostrar instrucciones de uso (`mostrar_ayuda`) e información del programa (`mostrar_informacion`).

### 🖱️ Widgets Utilizados

* **`Frame`:** Contenedor para organizar los botones de ayuda e información.
* **`Label`** y **`Entry`:** Para el título y la entrada de datos (nombre e ingredientes).
* **`Button`:** Para las acciones de "Agregar receta", "Ver ingredientes", "Eliminar receta", "Ayuda" e "Información".
* **`Listbox`:** Muestra la lista de nombres de las recetas agregadas y permite la selección.
* **`messagebox`:** Utilizado para confirmaciones, errores y mostrar los ingredientes/información.
