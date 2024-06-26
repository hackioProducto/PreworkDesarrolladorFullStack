<div style="text-align: center;">
  <img src="https://github.com/Hack-io-Data/Imagenes/blob/main/01-LogosHackio/logo_celeste@4x.png?raw=true" alt="logo hack(io)" />
</div>

# Creación de carpetas y ficheros

## Crear carpetas y ficheros en Windows (Command Prompt)

---

**Abrir Command Prompt:**

1. Presiona `Win + R`, escribe `cmd` y presiona `Enter`.

**Comandos básicos para crear carpetas y ficheros:**

- `mkdir [nombre_de_la_carpeta]`: Crea una nueva carpeta.
- `echo [texto] > [nombre_del_fichero.txt]`: Crea un nuevo fichero de texto con contenido.
- `type nul > [nombre_del_fichero.txt]`: Crea un nuevo fichero de texto vacío.

**Ejemplos:**

1. Para crear una carpeta llamada `Proyectos`:
    
    ```bash
    mkdir Proyectos
    ```
    
2. Para crear un fichero de texto llamado `nota.txt` con el contenido "Hola Mundo":
    
    ```bash
    echo Hola Mundo > nota.txt
    ```
    
3. Para crear un fichero de texto vacío llamado `vacío.txt`:
    
    ```bash
    type nul > vacío.txt
    ```
    

## Crear carpetas y ficheros en macOS (Terminal)

---

**Abrir Terminal:**

1. Presiona `Command + Espacio`, escribe `Terminal` y presiona `Enter`.

**Comandos básicos para crear carpetas y ficheros:**

- `mkdir [nombre_de_la_carpeta]`: Crea una nueva carpeta.
- `echo "[texto]" > [nombre_del_fichero.txt]`: Crea un nuevo fichero de texto con contenido.
- `touch [nombre_del_fichero.txt]`: Crea un nuevo fichero de texto vacío.

**Ejemplos:**

1. Para crear una carpeta llamada `Proyectos`:
    
    ```bash
    mkdir Proyectos
    ```
    
2. Para crear un fichero de texto llamado `nota.txt` con el contenido "Hola Mundo":
    
    ```bash
    echo "Hola Mundo" > nota.txt
    ```
    
3. Para crear un fichero de texto vacío llamado `vacío.txt`:
    
    ```bash
    touch vacío.txt
    ```
    

###  Tip

Practica estos comandos regularmente para mejorar tu fluidez en el uso de la terminal, pese a que los Sistemas Operativos actualmente nos evita tener que hacer uso de ellas para estas tareas.


## Reto coding

---

**Ejercicio en Windows:**

1. Abre `Command Prompt`.
2. Crea una carpeta llamada `Ejemplo`.
3. Navega a la carpeta `Ejemplo`.
4. Crea un fichero de texto llamado `test.txt` con el contenido "Este es un test".
5. Crea un fichero de texto vacío llamado `vacío.txt`.

**Ejercicio en macOS:**

1. Abre `Terminal`.
2. Crea una carpeta llamada `Ejemplo`.
3. Navega a la carpeta `Ejemplo`.
4. Crea un fichero de texto llamado `test.txt` con el contenido "Este es un test".
5. Crea un fichero de texto vacío llamado `vacío.txt`.