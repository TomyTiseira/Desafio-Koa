# Inicio de sesión

Implementar un mecanismo de autenticación.

Se incluirá una vista de registro, en donde se pidan email y contraseña. Estos datos se persistirán usando MongoDb, en una (nueva) colección de usuarios, cuidando que la contraseña quede encriptada (sugerencia: usar la librería bcrypt).

Cada una de las vistas (logueo - registro) deberá tener un botón para ser redirigido a la otra.

Una vez logueado el usuario, se lo redirigirá al inicio, el cual ahora mostrará también su email, y un botón para desolguearse.

Además, se activará un espacio de sesión controlado por la sesión de passport. Esta estará activa por 10 minutos y en cada acceso se recargará este tiempo.

Agregar también vistas de error para login (credenciales no válidas) y registro (usuario ya registrado).

# Dotenv

Mover todas las claves y credenciales utilizadas a un archivo .env, y cargarlo mediante la librería dotenv.


# Dividir en Capas el Proyecto

Dividir en capas el proyecto entregable que se viene realizando, agrupando apropiadamente las capas de ruteo, controlador, lógica de negocio y persistencia.
Agrupar las rutas por funcionalidad, con sus controladores, lógica de negocio con los casos de uso, y capa de persistencia.

La capa de persistencia contendrá los métodos necesarios para atender la interacción de la lógica de negocio con los propios datos.

# Mejorar la arquitectura de la API

- Modificar la capa de persistencia incorporando los conceptos de Factory, DAO, y DTO.
- Los DAOs deben presentar la misma interfaz hacia la lógica de negocio de nuestro servidor.
- El DAO seleccionado (por un parámetro en línea de comandos como lo hicimos anteriormente) será devuelto por una Factory para que la capa de negocio opere con el.
- Cada uno de estos casos de persistencia, deberán ser implementados usando el patrón singleton que impida crear nuevas instancias de estos mecanismos de acceso a los datos.
- Comprobar que si llamo a la factory dos veces, con una misma opción elegida, devuelva la misma instancia.

# Reformar para usae otro framework

Elegir uno de los frameworks vistos (Adonis, Nest, Sails, Koa) y trasladar a esta nueva plataforma el proyecto.

Verificar el correcto funcionamiento del servidor a nivel de sus rutas, vistas, lógica de negocio y persistencia.
