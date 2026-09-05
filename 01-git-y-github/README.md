# Módulo 1: Git, GitHub y el arte de no romper todo 🚀

> *Bienvenidos al control de versiones. Acá es donde dejamos atrás el clásico "trabajo_final_v3_definitivo_ahora_si.docx" para empezar a trabajar como profesionales.*

---

## Paso 0: ¿En qué sistema operativo estás parada?

Antes de tocar una sola línea de código, hay que entender dónde estamos parados. Si estás arrancando en IT, la realidad es implacable: **la gran mayoría de quienes dan sus primeros pasos usan Windows**. 

El gran problema histórico es que la terminal por defecto de Windows (*Command Prompt* o *PowerShell* clásica) no habla el mismo idioma que Linux y Git, lo que suele generar errores crípticos. Vamos a solucionarlo desde el minuto uno.

* **Si estás en Windows:** 
  1. Entrá a [git-scm.com](https://git-scm.com) y descargá el instalador.
  2. Durante la instalación, dejá todo por defecto (Next, Next, Next), **excepto** asegurate de tildar la opción **"Git from the command line and also from 3rd-party software"** y elegí **Git Bash** como la terminal por defecto.
  3. Una vez instalado, abrilos buscando **Git Bash** en tu menú de inicio. Verás una ventana negra y limpia: **a partir de ahora, cada comando de este módulo lo corrés ahí adentro**.
* **Si estás en Mac o Linux:** 
  * Podés usar tu terminal nativa de confianza (`Terminal` en Mac o tu consola habitual en Linux) asegurándote de tener Git instalado.

---

## Paso 1: Conceptos clave sin vueltas

Antes de ejecutar comandos a ciegas, entendamos qué estamos haciendo:

* **Repositorio (*Repo*):** Es la carpeta de tu proyecto, pero con superpoderes. Guarda la "película" completa de cada cambio que hiciste, no solo la foto actual.
* **Commit:** Es como apretar *Guardar partida* en un videojuego. Guarda una foto de tus archivos en ese instante junto a un mensaje que explica qué cambiaste.
* **Branch (Rama):** Es una línea de trabajo paralela. Te permite experimentar, romper o probar algo nuevo sin alterar el proyecto principal (`main`).
* **Pull Request (PR):** Es el puente de la colaboración. Es proponer tus cambios para que el equipo los revise y los sume al proyecto oficial.

---

## Paso 2: Configurar tu identidad en la terminal

Para que Git sepa quién firma cada cambio, abrí tu **Git Bash** (o terminal) y ejecutá estos dos comandos con tus datos reales (los mismos de tu cuenta de GitHub):

```bash
git config --global user.name "Tu Nombre Apellido"
git config --global user.email "tu_correo@example.com"
```

---

## Paso 3: Clonar el repositorio

Traigamos la copia del proyecto a tu computadora:

1. Andá a la página principal de este repositorio en GitHub, hacé clic en el botón verde **Code** y copiá la URL (HTTPS).
2. En tu terminal, elegí dónde querés guardar tus proyectos (por ejemplo, ejecutando `cd Documentos`), y luego escribí:

```bash
git clone <url-que-copiaste>
```

3. Entrá a la carpeta que se acaba de descargar con el siguiente comando:

```bash
cd mis-primeros-pasos-en-it
```

---

## Paso 4: Crear tu rama de trabajo

Nunca trabajamos directo sobre la rama principal (`main`). Creá tu propio espacio seguro ejecutando:

```bash
git checkout -b feature/tu-nombre
```

---

## Paso 5: El ciclo sagrado de Git (Guardar y empaquetar)

Cada vez que hagas un cambio en los archivos, vas a repetir estos tres pasos mentales en tu terminal:

1. **Mirar el estado:** 
   ```bash
   git status
   ```
   *(Te muestra qué archivos modificaste).*
2. **Preparar los cambios:**
   ```bash
   git add .
   ```
   *(Empaqueta todo lo modificado).*
3. **Guardar la foto (Commit):**
   ```bash
   git commit -m "docs: agrega mi primer aporte al repositorio"
   ```

---

## Paso 6: Subir los cambios a GitHub (Push)

Mandá tu rama de vuelta a la nube ejecutando:

```bash
git push origin feature/tu-nombre
```

Una vez que hacés el push, vas a entrar a GitHub y vas a ver un botón amarillo o verde que dice **Compare & pull request**. 
Hacé clic ahí, envianos tu propuesta y ¡listo! Habrás completado tu primer ciclo colaborativo real.

