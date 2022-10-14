## Introducción a Git
### ¿Por qué usar un sistema de control de versiones como Git?
**Sistema de control de versiones** solamente guardan los cambios en los documentos, dejando un registro de donde, cuando ocurrieron, quien los hizo...

### ¿Qué es Git?
*Es un control de versiones distribuido* se basa en la *eficiencia* y la *confiabilidad* 
- Git está optimizado para guardar cambios de fotma incremental.
- Tiene un historial, permite un flujo entre versiones y agregar funcionalidades.
- Lleva un registro de los cambios que otras personas realicen a los archivos

- La mayor eficiencia se obtiene usando archivos de texto plano.

**Caracteristicas de Git**
+ Almacena la información como un conjunto de archivos.
+ No pasa absolutamente nada sin que Git lo entero.
+ Git cuanta con tres estados, donde se localizan los archivos: *Staged* - *Modified* - *Committed*

#### ¿Qué es GitHub?
Es una plataforma de desarrollo colaborativo para alojar proyectos usando Git. Para los programadores en ocaciones se ve como un *Curriculum vitae*

**Caracteristicas de GitHub**
- Tiene plan gratituo y pago
- Facilidad para compartir proyectos
- Ayuda a reducir significativamente los errores humanos, tener un mejor mantenimiento de distintos entornos y detectar fallos de forma rápida y eficiente.
  
### Instalando Git y GitBash en Windows
*Nota: Para Yeremi*

### Instalando Git en OSX

### Instalando Git en Linux

### Editores de código, archivos y de texto plano
*NOTA: Para Yeremi*

**Tipos de archivos y sus diferencias**
- *Archivos de texto (.txt):* Texto plano normal y sin nada de especial. 
- *Archivos RTF (.rtf):* Permite guardar texto con diferentes tamaños, estilos y colores. Más complejo que el texto plano, pues guarda ls estilos del texto. 
- *Archivos de Word  .docx():* Permite guardar imagenes y textos con diferentes tamaños, estilos y colores. (Visto desde un editor de texto, es un archivo binario.)


**Conceptos importantes de Git**
- *Checkout:* Acción de descargarse una rama del repositorio Git local o del remoto.
- *Fech:* Actualiza el repositorio local bajando datos del remoto sin actualizar el local, es decir guarda una copia del remoto en el local.

### Introducción a la terminal y línea de comandos
*NOTA: Para Yerimi*

- **ls:** listar archivos 
    + **ls -a** mostrar archivos ocultos
    + **ls -al** listar archivos ocultos
 
## Comandos básicos de Git
### Crea un repositorio de Git y Ha tu primer commit
*NOTA: Para Yerimi*

+ **SHA (Secure Hash Algorithm):** Id de 4o caracteres que se crea para cada commit

- **git log:** se usa para ver la historia de nuestros archivos, los commits, el usuario que lo cambio...

### Analizar cambios en los archivos de tu proyecto con Git

### ¿Qué es el staging?
ESta hubicada en la memoria ram, es donde se guardan los cambios con el comando **git add**. En esta area el archivo esta a espera de ser enviado al repsoitorio. Se puede quidar del **staging** usando el comando **git rm**.

Si todo lo que quiero esta bien, con el comando **git commit** lo mando al repositorio, por defecto es la rama master.

- Con git **checkout** puedo traer un estado particular del repositorio a mi carpeta (zona de trabajo)

### ¿Qué es branch (rama) y cómo funciona un Merge en Git?
Cuando creas tu repositorio en tu carpeta de trabajo se crea por defecto una rama principal llamada **master**

#### Ramas habituales 
- **Master:** todo lo que esta en esta rama va a producción
- **DEvelopment:** Las nuevas features, caracteristicas y experimentos
- **HotFix:** Aqui van los errores se solucionan tan pronto como sea posible

### Git reset vs. Git rm
**git rm** sirve para eliminar un archivo sin eliminar su historial del sistema de versiones. Es posible recuperar el archivo. Tenemos dos opciones
- *git rm --cached:* Elimina el archivo de nuestro repositorio local y del área de staging, pero lo mantiene en el disco duro. Le dice a git que deje de seguirlo, dejandolo en un estado de untracked.
- *git rm --force:* Elimina el archivo de Git y del disco duro. Es posible recuperarlo de ser necesario.

**git reset**
Con este comando podemos volver en el tiempo. Pero a diferencia de *git checkout* no hay vuelta atras, eliminamos la historia y toca volverla a escribir. Podemos usar como argumento *--hard* y *--soft**. 
- *git reset --hard:* Borra todo, absolutamente todo. Toda la información de los commits, del área de staging, se borra el historial.
- *git reset --soft:* se borra el historial y los registros de Git, pero se guardan los cambios que tengamos en Stagin, así podemos aplicar las últimas actulizaciones  a un nuevo commit.
- *git reset HEAD:* permite sacar archivos del área de staging. 
 
## Flujo de trabajo básico en Git
### Flujo de trabajo básico con un repositorio remoto

**Directorio local** --> git add --> **Preparación o Staging** --> git commit --> **Repositorio local**  --> git push --> **Repositorio remoto**

**Repositorio remoto** --> git fetch --> **Repositorio local** --> git merge --> **Directorio de trabajo**, (Esto se puede resumir con un git pull)

### Introducción a las ramas o branches de Git
**Nota Yerimi**

- **git commit -am** hace automaticamente los cambios (git add), solo funciona con archivos ya creados.
- **git branch nombre_de_la_rama:** crea una nueva rama, desde donde este parado
- **git checkout nombre_de_la_rama:** permite moverse entre las ramas
- **git checkout -b nombre_de_la_rama:** Crea una nueva rama y voy directamente a está.
  
### Fusión de ramas con Git Merge
Cuando se hace un *merge* no se crea una tercera rama, sino que se une una a otra. El merge sucede en la rama en donde estoy.

### Resolución de conflictos al hacer un merge
Suceden cuando una parte del código cambia en dos archivos, la idea es ver que cambio y ver con que me quedo. Cuando sucede en trabajo en equipo, se soluciona con una buena comunicación entre el equipo.

## Trabajando con repositorios remotos en GitHub
### Cambios en GitHub: de master a main
Hubo un cambio en 2020 de la rama *master* ahora se llama *main*

### Uso de GitHub
**Nota Yerimi**

- **git remote add origin <url>:** Conecta un repositorio en la <url> y da un origen de *repositorio remoto (gitHub)* a nuestro equipo local en *git*
- **git remote -v:** Lista de conexiones existentes. Donde hacer fecth y push 

### Cómo funcionan las llaves públicas y privadas
'La lleve publica permite cifrar un mensaje que solo se puede decifrar con mi llave privada'
**Nota Yerimi**

### Configura tus llaves SSH en local
 **Crear llave ssh**
 ssh-keygen -t rsa -b 4096 -C "tu@email.com"

 **Nota Yerimi:** revisar si el protocolo para crear la llave sigue siendo el rsa, sino actualizarlo
 
### Tags y versiones en Git y GitHub
- git tag
**Nota Yerimi:**

### Configurar multiples colaboratores en un repositorio de GitHub
**Nota Yerimi:**

### Manejo de ramas GitHub

## Flujos de trabajo profesionales
### Haciendo un merge de ramas de desarrollo a master

### Creando un Fork, Contribuyendo a un repositorio
**Fork:** es tomar una copia del estado actual del proyecto y lo creo como un proyecto propio.

*Es bueno solo tener la rama master y develop en el proyecto, las otras deberían desaparecen luego de hacer el merge*

## Multiples entornos de trabajo en Git

## Comandos de Git para casos de emergencia

## Bonus sobre Git y Github