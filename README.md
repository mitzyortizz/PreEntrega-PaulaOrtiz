# PreEntrega-PaulaOrtiz
- Se crea el repositorio
	-Se hace publica
	-Se añade el Readme
	Se añada el template Python
- Se clona el powershell
	-Me meto al proyecto creado
	-Abro el proyecto en visual code
- Creo el entorno virtual
	-Lo activo el entorno virtual
- Instalamos Django
- Creamos la carpeta Proyecto con el comando mkdir
	-Accedo a la carpeta Proyecto que acabo de crear
	-Ejecuto el comando: django-admin startprojecto config . para iniciar un nuevo proyecto de Django con ciertas características
- Creo la applicacion con el comando: python .\manage.py startapp servicios
	- Registro la aplicacion que acabo de crear en setting en la parte de installed app
- Dentro de la carpeta Servicios creo otra carpeta llamada Templates
	-Sobre Templates creo otra carpeta con el mismo nombre Servicios
	-Sobre Servicios creo un nuevo archivo llamados base.html y index.html
- La estructura la creamos en base.html usando el autocompletado del !
- El index.html se extiende de base.html
- Renderizamos index.html en Views donde definimos la funcion
- En el archivo url.py importamos de la aplicacion Servicios las vistas
	-Creamos la url para eso nos vamos al archivo url.py y creamos el path dentro urlpatterns
- Probamos hasta aqui con el comando python .\manage.py runserver
- Agregamos una url a en index a home
- Creamos los modelos en models
	-Creamos el modelo Cliente en su respectiva clase
	-Creamos el modelo Servicio en su respectiva clase
	-Creamos el modelo Pedido en su respectiva clase
- Hacemos las migraciones con los comandos "makemigrations" y "migrate"
- Creamos el superusuario
	-El usuario es admin y la contraseña 123
- Registramos los modelos en admin
	-Importamos los modelos Cliente, Servicio, Pedido
- Corremos el servidor y probamos
- Cambiamos el idioma del panel de administracion de django en setting en Languaje_Code
- Modificamos el campo de domicio el Models para que sea obligatorio
	-Volvemos a correr las migraciones con los comandos "makemigrations" y "migrate"
- Personalizamos el panel de administracion en el archivo admin con sus respectivas clases (opcional)
- Creamos las listas y un archivo de registro para cada modelo en Templates
	-Lo extendemos de index los bloques, a las templates que hemos creado
	-Ponemos los titulos
- Creamos las vistas para que lo que hemos creado en panel de administracion podamos verlo en nuestro html, en views
	-Importamos de models los tres modelos
	-Creamos la respectivas funciones y sus query
- Vamos a url y agremos todas las URL de los 3 modelos
 	-Creamos un impervinculo en index, para que cuando hagamos un clic nos redirija a la url correspondiente
	- Corremos el servicio y probamos que nos redirija a las urls correspondientes
- Creamos el archivo navbar.html en la carpeta templates
	-Me saco los botones de index.html y lo paso a navbar
- El menu de navegacion lo incluimos en base.html
	-Creamos la etiqueta <nav> despues del <header>
- Mostramos los registros y para ello nos vamos a cada template.list que creamos de los tres modelos
	-Creo sus for respectivos
	-Probamos y verificamos que muestre los registros
- Personalizamos el metodo Str en cada uno de los templates list de los modelos
- Preparamos para hacer el crud, primero hacemos adicionar
	-Creamos un boton "Crear registro" template de los formularios y ese boton lo hacemos en cada template list
	-En los templates create hacemos el metodo POST
	-Creamos las vistas para llamar para que maneje las respuestas, esto lo hacemos en views con su funcion respectiva de cada models
	-Vamos a las urls y adicionamos los path correspondientes de los tres models
	-En cada template list colocamos las urls que acabamos de crear
- Creamos los formularios, lo hacemos creando un archivo servicios llamado forms.py
	-Importamos los formularios de django
	-Importamos los formularios de los tres modelos
	-Creamos las respectivas clases de formularios
- Importamos los tres formularios en views
	-Modificamos las funciones de los create para manejar la logica
	-Importamos el redirect al lado de render
	-Probamos que se muestren los formularios y que se adicionen a la bd
- Hacemos un git add para agregar todo
- Hacemos un git commit con un comentario
- Hacemos un git push

Pd: Se debe hacer la migracion en cada cambio que se haga en models
