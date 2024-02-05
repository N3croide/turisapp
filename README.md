# **TALLER GIT**

------

1. Esta trabajando en un proyecto Git colaborativo con varias ramas y commits. Tu tarea es
   utilizar el comando git log con algunas opciones específicas para obtener un resumen
   gráfico de los últimos 5 commits en todas las ramas.

   ```bash
   git config alias.lg5 "log --all --graph --oneline -n 5"
   ```

   - `--all`: Muestra commits de todas las ramas.

   - `--graph`: Muestra una representación gráfica del historial de commits.

   - `--oneline`: Muestra cada commit en una línea, lo que facilita la visualización.

   - `-n 5`: Limita la salida a los últimos 5 commits.

     

2. Esta trabajando en un proyecto Git colaborativo y necesitas obtener una visión gráfica y
   detallada del historial de commits. Tu tarea es utilizar el comando git log con opciones
   específicas para personalizar el formato y presentación de la salida. La salida debe tener
   las siguientes especificaciones:

   Muestra una representación gráfica del historial de commits

   Muestra el hash corto del commit en color rojo

   Muestra las referencias (ramas o tags) en las que está involucrado el commit en color
   amarillo

   Muestra el mensaje del commit.

   Muestra la fecha relativa del commit en color verde.

   Muestra el hash del commit como un identificador abreviado.

   Muestra las fechas de los commits de forma relativa



```bash
git config alias.lgp2 'log --graph --pretty=format:"%Cred%h%Creset %C(yellow)%d%Creset %s %Cgreen(%ar)%Creset"'
```

- `--graph`: Muestra una representación gráfica del historial de commits.
- `--pretty=format`: Personaliza el formato de salida.
- `%Cred%h%Creset`: Muestra el hash corto del commit en color rojo.
- `%C(yellow)%d%Creset`: Muestra las referencias (ramas o tags) en las que está involucrado el commit en color amarillo.
- `%s`: Muestra el mensaje del commit.
- `%Cgreen(%ar)%Creset`: Muestra la fecha relativa del commit en color verde.





3. Estas trabajas frecuentemente con el comando git log -1 HEAD para obtener detalles sobre
   el último commit en la rama actual. Sin embargo, encuentras que escribir este comando
   completo es un poco tedioso. Quieres simplificarlo creando un alias personalizado.Tu tarea es utilizar el 
   comando git config para crear un alias llamado last que represente el
   comando git log -1 HEAD.

   ```bash
   git config alias.last "log -1 HEAD"
   ```

   1. **`git config`**: Este comando se utiliza para configurar opciones de Git. En este contexto, se utilizará para configurar un alias.

   2. **`alias.last`**: Esto especifica el nombre del alias que estás creando. En este caso, estás creando un alias llamado `last`.

   3. **`"log -1 HEAD"`**: Es el comando que se asociará con el alias. En este caso, estás configurando `last` para ejecutar el comando `git log -1 HEAD`. Explicado detalladamente:

      - **`log`**: Comando de Git para ver el historial de commits.

      - **`-1`**: Limita la salida a mostrar solo el último commit.

      - **`HEAD`**: Indica que se está refiriendo al commit más reciente en la rama actual.

        

4. Imagina que deseas simplificar el proceso de editar la configuración global de Git. Tu tarea
   es utilizar el comando git config para crear un alias que te permita abrir fácilmente la
   configuración global en tu editor de texto preferido. Ejecuta el comando para crear un alias
   llamado ec que cumpla con la especificación dada.

   ```bash
   git config alias.ec "config --global -e"
   ```

   1. **`git config`**: Este comando se utiliza para configurar opciones de Git. En este caso, se utiliza para crear un alias.

   2. **`--global`**: Indica que el alias se configurará de forma global, es decir, a nivel de usuario. Esto significa que el alias estará disponible en todos los repositorios de Git en tu máquina.

   3. **`alias.ec`**: Especifica el nombre del alias que estás creando. Aquí, estás creando un alias llamado `ec`.

   4. **`"config --global -e"`**: Es el comando que se asociará con el alias. Explicado detalladamente:

      - **`config`**: Indica que se está accediendo a la configuración de Git.

      - **`--global`**: Indica que la configuración se aplica a nivel global.

      - **`-e`**: Especifica que se abrirá el archivo de configuración en el editor de texto definido en la variable de entorno `EDITOR` o `VISUAL`.

        

5. Imagina que estás trabajando en un proyecto Git colaborativo con múltiples colaboradores
   y ramas. Tu tarea es utilizar el comando git log con opciones específicas para personalizar
   la salida del historial de commits y resaltar información clave. El resultado de la ejecución
   del comando se debe ve como el ejemplo siguiente:

   ```bash
   git config alias.ult "log --graph --oneline --decorate --all --format='%C(auto)%h%Creset%C(red)%d%Creset%C(red)\%Creset %s%C(blue)\%Creset %C(bold blue)[%an]%Creset'"
   ```

   - `--graph`: Muestra una representación gráfica del historial de commits.
   - `--oneline`: Muestra cada commit en una línea para una visualización más concisa.
   - `--decorate`: Muestra las referencias, como ramas y etiquetas, asociadas con cada commit.
   - `--all`: Incluye todos los refs, no solo los de la rama actual.
   - `--format='%C(auto)%h%Creset%C(red)%d%Creset %s%C(blue)%an%Creset'`: Personaliza el formato de salida con colores y detalles específicos. `%h` es el hash corto, `%d` son las referencias, `%s` es el mensaje del commit, `%an` es el nombre del autor.
