# Módulo 3: Linux y Máquinas Virtuales (El motor oculto del mundo IT) 🐧

> *Si internet fuera una gran ciudad, Linux y las máquinas virtuales son los cimientos sobre los que se construye todo. Dejemos de temerle a la pantalla negra y empecemos a entender cómo gobernar el sistema.*

---

## Paso 0: ¿Qué es Linux y por qué lo usamos en todos lados?

Cuando pensamos en computadoras, solemos imaginar Windows o macOS en nuestras laptops. Pero cuando subimos una aplicación a la nube (AWS, Azure, Google Cloud) o levantamos un servidor, el sistema operativo que manda es **Linux**.

- **Linux** es un sistema operativo de código abierto, sumamente estable, seguro y liviano.
- No tiene una sola cara (como Windows), sino que se divide en **distribuciones** (o *distros*): versiones adaptadas a distintos usos (como Ubuntu, Debian, CentOS o Amazon Linux).
- **¿Por qué importa?** Porque el 90% de los servidores del planeta corren sobre Linux. Aprender sus comandos básicos no es opcional: es la llave de acceso al mundo real de la infraestructura y el desarrollo.

---

## Paso 1: Entendiendo la estructura de directorios

En Windows estamos acostumbrados a navegar por unidades como `C:` o `D:` y carpetas con interfaces gráficas. En Linux, todo es un **único gran árbol de directorios** que cuelga de una raíz común representada por una barra diagonal (`/`).

- `/` (Root): La raíz del sistema, el punto de partida de todo.
- `/home`: Donde viven las carpetas personales de los usuarios (por ejemplo, tu usuario tendrá su espacio en `/home/tu-usuario`).
- `/etc`: Donde se guardan los archivos de configuración del sistema.
- `/var`: Donde suelen vivir los registros (*logs*) y datos dinámicos.

---

## Paso 2: Movimientos básicos en la terminal

Abrí tu terminal (si estás en Windows con Git Bash, ya tenés un entorno compatible con comandos tipo Unix) y probemos movernos por el sistema:

### 1. Saber dónde estás parada (PWD)

```bash
pwd
```

Muestra la ruta completa del directorio actual.

### 2. Listar archivos y carpetas (LS)

```bash
ls -la
```

Muestra todo lo que hay en la carpeta, incluyendo archivos ocultos y permisos.

### 3. Cambiar de directorio (CD)

```bash
cd /home
```

Para entrar a una carpeta específica, o usar `cd ..` para volver un nivel hacia atrás.

---

## Paso 3: Manipulando archivos y carpetas

Crear, mover y borrar elementos sin usar el mouse es cuestión de conocer los comandos esenciales:

### Crear una carpeta nueva (MKDIR)

```bash
mkdir mi-nueva-carpeta
```

### Crear un archivo vacío o modificar su fecha (TOUCH)

```bash
touch notas.txt
```

### Copiar y mover archivos (CP y MV)

```bash
cp notas.txt respaldo.txt
mv notas.txt /home/tu-usuario/
```

### Eliminar archivos o carpetas (RM)

> ⚠️ **Cuidado:** Linux no tiene papelera de reciclaje por consola, lo que borrás, desaparece.

```bash
rm notas.txt
```

---

## Paso 4: El concepto de Máquinas Virtuales (VMs)

Una **Máquina Virtual (VM)** es, en términos sencillos, una computadora simulada dentro de otra computadora.

- Te permite correr un sistema operativo completo (por ejemplo, Ubuntu Server) dentro de tu propia PC (usando herramientas como VirtualBox o WSL en Windows), aislada del sistema principal.
- **¿Para qué sirve?** Para probar configuraciones, romper cosas sin miedo a arruinar tu equipo real, o simular un entorno de producción idéntico al que vas a usar en la nube.
