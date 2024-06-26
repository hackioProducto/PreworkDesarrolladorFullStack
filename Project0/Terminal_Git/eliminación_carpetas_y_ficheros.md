<div style="text-align: center;">
  <img src="https://github.com/Hack-io-Data/Imagenes/blob/main/01-LogosHackio/logo_celeste@4x.png?raw=true" alt="logo hack(io)" />
</div>

# Eliminación de carpetas y ficheros

## Eliminar carpetas y ficheros en Windows (Command Prompt)

---

**Abrir Command Prompt:**

1. Presiona `Win + R`, escribe `cmd` y presiona `Enter`.

**Comandos básicos para eliminar carpetas y ficheros:**

- `del [nombre_del_fichero]`: Elimina un fichero.
- `rmdir [nombre_de_la_carpeta]`: Elimina una carpeta vacía.
- `rmdir /s [nombre_de_la_carpeta]`: Elimina una carpeta y su contenido.

**Ejemplos:**

1. Para eliminar un fichero llamado `nota.txt`:
    
    ```bash
    del nota.txt
    ```
    
2. Para eliminar una carpeta vacía llamada `Proyectos`:
    
    ```bash
    rmdir Proyectos
    ```
    
3. Para eliminar una carpeta llamada `Proyectos` y su contenido:Te pedirá confirmación para eliminar, presiona `Y` y luego `Enter` para confirmar.
    
    ```bash
    rmdir /s Proyectos
    ```
    

## Eliminar carpetas y ficheros en macOS (Terminal)

---

**Abrir Terminal:**

1. Presiona `Command + Espacio`, escribe `Terminal` y presiona `Enter`.

**Comandos básicos para eliminar carpetas y ficheros:**

- `rm [nombre_del_fichero]`: Elimina un fichero.
- `rmdir [nombre_de_la_carpeta]`: Elimina una carpeta vacía.
- `rm -r [nombre_de_la_carpeta]`: Elimina una carpeta y su contenido.

**Ejemplos:**

1. Para eliminar un fichero llamado `nota.txt`:
    
    ```bash
    rm nota.txt
    ```
    
2. Para eliminar una carpeta vacía llamada `Proyectos`:
    
    ```bash
    rmdir Proyectos
    ```
    
3. Para eliminar una carpeta llamada `Proyectos` y su contenido:
    
    ```bash
    rm -r Proyectos
    ```
    

### Tip:

Tened especial cuidado con estos comandos, ya que si no controlamos de momento la terminal podemos borrar definitivamente archivos y carpetas que no deseemos. Probad siempre en carpetas y entornos preparados antes de utilizarlos con soltura.


## Reto coding

---

**Ejercicio en Windows:**

1. Abre `Command Prompt`.
2. Crea una carpeta llamada `Ejemplo` y dentro de ella un fichero llamado `test.txt` (puedes usar los comandos `mkdir` y `echo`).
3. Elimina el fichero `test.txt`.
4. Elimina la carpeta `Ejemplo` y su contenido.

**Ejercicio en macOS:**

1. Abre `Terminal`.
2. Crea una carpeta llamada `Ejemplo` y dentro de ella un fichero llamado `test.txt` (puedes usar los comandos `mkdir` y `echo`).
3. Elimina el fichero `test.txt`.
4. Elimina la carpeta `Ejemplo` y su contenido.