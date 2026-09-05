Módulo 1: Git, GitHub y el arte de no romper todo 🚀
Bienvenidos al control de versiones. Acá es donde dejamos atrás el clásico "trabajo_final_v3_definitivo_ahora_si.docx" para empezar a trabajar como profesionales.

🧭 Paso 0: ¿En qué sistema operativo estás parada?
Antes de tocar una sola línea de código, hay que entender dónde estamos parados. Si estás arrancando en IT, la realidad es implacable: la gran mayoría de quienes dan sus primeros pasos usan Windows.

El gran problema histórico es que la terminal por defecto de Windows (Command Prompt o PowerShell clásica) no habla el mismo idioma que Linux y Git, lo que suele generar errores crípticos. Vamos a solucionarlo desde el minuto uno.

Si estás en Windows:

Entrá a git-scm.com y descargá el instalador.

Durante la instalación, dejá todo por defecto (Next, Next, Next), excepto asegurate de tildar la opción "Git from the command line and also from 3rd-party software" y elegí Git Bash como la terminal por defecto.

Una vez instalado, abrilos buscando Git Bash en tu menú de inicio. Verás una ventana negra y limpia: a partir de ahora, cada comando de este módulo lo corrés ahí adentro.

Si estás en Mac o Linux:

Podés usar tu terminal nativa de confianza (Terminal en Mac o tu consola habitual en Linux) asegurándote de tener Git instalado.

🧠 1. Conceptos clave sin vueltas
Antes de ejecutar comandos a ciegas, entendamos qué estamos haciendo:

Repositorio (Repo): Es la carpeta de tu proyecto, pero con superpoderes. Guarda la "película" completa de cada cambio que hiciste, no solo la foto actual.

Commit: Es como apretar Guardar partida en un videojuego. Guarda una foto de tus archivos en ese instante junto a un mensaje que explica qué cambiaste.

Branch (Rama): Es una línea de trabajo paralela. Te permite experimentar, romper o probar algo nuevo sin alterar el proyecto principal (main).

Pull Request (PR): Es el puente de la colaboración. Es proponer tus cambios para que el equipo los revise y los sume al proyecto oficial.

🛠️ 2. Manos a la obra: Tu primer flujo con Git
Abrí tu Git Bash (o terminal) y hagamos el recorrido completo:

A. Configurar tu identidad (Para que Git sepa quién sos)
Ejecutá estos dos comandos con tus datos reales (los mismos de tu cuenta de GitHub):

Bash
git config --global user.name "Tu Nombre Apellido"
git config --global user.email "tu_correo@example.com"
B. Clonar el repositorio (Traer la copia a tu compu)
Andá a la página principal de este repositorio en GitHub, hacé clic en el botón verde Code y copiá la URL (HTTPS).

En tu terminal, elegí dónde querés guardar tus proyectos (por ejemplo, cd Documentos) y escribí:

Bash
git clone <pegas-aqui-la-url-que-copiaste>
Entrá a la carpeta que se acaba de descargar:

Bash
cd mis-primeros-pasos-en-it
C. Crear tu rama de trabajo
Nunca trabajamos directo sobre la rama principal (main). Creá tu propio espacio seguro:

Bash
git checkout -b feature/tu-nombre
D. El ciclo sagrado de Git
Cada vez que hagas un cambio en los archivos, vas a repetir estos tres pasos mentales:

Mirar el estado:

Bash
git status
(Te muestra qué archivos modificaste).

Preparar los cambios (Add):

Bash
git add .
(Empaqueta todo lo modificado).

Guardar la foto (Commit):

Bash
git commit -m "docs: agrega mi primer aporte al repositorio"
E. Subir los cambios a GitHub (Push)
Mandá tu rama de vuelta a la nube:

Bash
git push origin feature/tu-nombre
Una vez que hacés el push, vas a entrar a GitHub y vas a ver un botón amarillo o verde que dice Compare & pull request. Hacé clic ahí, envianos tu propuesta y ¡listo! Habrás completado tu primer ciclo colaborativo real.
