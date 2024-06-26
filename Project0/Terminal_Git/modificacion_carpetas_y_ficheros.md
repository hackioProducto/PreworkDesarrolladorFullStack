<div style="text-align: center;">
  <img src="https://github.com/Hack-io-Data/Imagenes/blob/main/01-LogosHackio/logo_celeste@4x.png?raw=true" alt="logo hack(io)" />
</div>

# Modificación de carpetas y ficheros

## Modificar carpetas y ficheros en Windows (Command Prompt)

---

**Abrir Command Prompt:**

1. Presiona `Win + R`, escribe `cmd` y presiona `Enter`.

**Comandos básicos para modificar carpetas y ficheros:**

- `ren [nombre_actual] [nuevo_nombre]`: Renombra un fichero o carpeta.
- `move [nombre_del_fichero] [nueva_ruta]`: Mueve un fichero a otra ubicación.
- `copy [nombre_del_fichero] [nueva_ruta]`: Copia un fichero a otra ubicación.
- `attrib +r/-r [nombre_del_fichero]`: Establece o elimina el atributo de solo lectura de un fichero.

**Ejemplos:**

1. Para renombrar un fichero llamado `nota.txt` a `nota_nueva.txt`:

   ```bash
   ren nota.txt nota_nueva.txt
   ```

2. Para mover un fichero llamado `nota.txt` a la carpeta `Documentos`:

   ```bash
   move nota.txt Documentos
   ```

3. Para copiar un fichero llamado `nota.txt` a la carpeta `Documentos`:

   ```bash
   copy nota.txt Documentos
   ```

4. Para establecer el atributo de solo lectura en un fichero llamado `nota.txt`:

   ```bash
   attrib +r nota.txt
   ```

5. Para eliminar el atributo de solo lectura en un fichero llamado `nota.txt`:

   ```bash
   attrib -r nota.txt
   ```

## Modificar carpetas y ficheros en macOS (Terminal)

---

**Abrir Terminal:**

1. Presiona `Command + Espacio`, escribe `Terminal` y presiona `Enter`.

**Comandos básicos para modificar carpetas y ficheros:**

- `mv [nombre_actual] [nuevo_nombre]`: Renombra un fichero o carpeta.
- `mv [nombre_del_fichero] [nueva_ruta]`: Mueve un fichero a otra ubicación.
- `cp [nombre_del_fichero] [nueva_ruta]`: Copia un fichero a otra ubicación.
- `chmod [permisos] [nombre_del_fichero]`: Cambia los permisos de un fichero.

**Ejemplos:**

1. Para renombrar un fichero llamado `nota.txt` a `nota_nueva.txt`:

   ```bash
   mv nota.txt nota_nueva.txt
   ```

2. Para mover un fichero llamado `nota.txt` a la carpeta `Documentos`:

   ```bash
   mv nota.txt Documentos
   ```

3. Para copiar un fichero llamado `nota.txt` a la carpeta `Documentos`:

   ```bash
   cp nota.txt Documentos
   ```

4. Para cambiar los permisos de un fichero llamado `nota.txt` a solo lectura:

   ```bash
   chmod 444 nota.txt
   ```

5. Para cambiar los permisos de un fichero llamado `nota.txt` a lectura y escritura:

   ```bash
   chmod 644 nota.txt
   ```

### Tip:

Practica estos comandos regularmente para mejorar tu fluidez en el uso de la terminal, pese a que los Sistemas Operativos actualmente nos evita tener que hacer uso de ellas para estas tareas.

Ten cuidado con la asignación de permisos a según que ficheros, prueba con archivos efímeros para empezar.

## Reto coding

---

**Ejercicio en Windows:**

1. Abre `Command Prompt`.
2. Crea un fichero llamado `test.txt` (puedes usar el comando `echo`).
3. Renombra el fichero a `test_nuevo.txt`.
4. Mueve el fichero a una nueva carpeta llamada `Documentos` (créala si es necesario).
5. Establece el atributo de solo lectura en `test_nuevo.txt` → `attrib +r test_nuevo.txt`.

**Ejercicio en macOS:**

1. Abre `Terminal`.
2. Crea un fichero llamado `test.txt` (puedes usar el comando `echo`).
3. Renombra el fichero a `test_nuevo.txt`.
4. Mueve el fichero a una nueva carpeta llamada `Documentos` (créala si es necesario).
5. Cambia los permisos de `test_nuevo.txt` a solo lectura → `chmod 444 test_nuevo.txt`.
