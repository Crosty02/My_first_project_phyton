# My_first_project_phyton


# Descripción del proyecto
Este proyecto tiene como objetivo realizar pruebas automatizadas sobre un servicio web,
validando la creación de usuarios y la correcta gestión de parámetros asociados, como el firstName. 
Las pruebas cubren tanto escenarios positivos (cuando el servicio responde correctamente) 
como negativos (cuando el servicio devuelve errores debido a datos incorrectos o incompletos).
El propósito es garantizar el correcto funcionamiento del servicio en cuanto a la creación de usuarios 
a través de solicitudes HTTP.

# Estructura del proyecto

├── configuration.py            # Configuración de rutas y URLs del servicio.
├── data.py                     # Datos utilizados en las solicitudes y pruebas.
├── sender_stand_request.py     # Funciones para enviar solicitudes HTTP.
├── create_user_test.py         # Archivo con las pruebas automatizadas.
├── README.md                   # Descripción del proyecto y pasos para ejecutar.
├── .gitignore                  # Archivos y directorios a ignorar por Git.

# Tecnologías utilizadas

Python: Lenguaje de programación utilizado para el desarrollo de las pruebas.
Requests: Biblioteca para realizar solicitudes HTTP.
pytest: Framework utilizado para ejecutar las pruebas automatizadas.
GitHub: Plataforma para gestionar el código y colaborar.

# Instrucciones para ejecutar las pruebas
Clonar el repositorio:

git clone https://github.com/Crosty02/qa-project-Urban-Grocers-app-es.git
Configurar el entorno:
Abre PyCharm o tu editor de preferencia.
Crea un nuevo proyecto Python.
Instala las dependencias necesarias, como requests y pytest:
pip install requests pytest
Dentro de PyCharm, abre el archivo create_user_test.py y ejecuta las pruebas.

# Descripción de los archivos

Configuration.py: Este archivo contiene las configuraciones principales, como la URL base del servicio y las rutas para las solicitudes.
Data.py: Contiene los datos predefinidos para las solicitudes, como el cuerpo de las peticiones (user_body) y los encabezados (headers).
Sender_stand_request.py: Incluye las funciones para enviar las solicitudes HTTP al servicio. Esto incluye la creación de nuevos usuarios y la obtención de la tabla de usuarios.
Create_user_test.py: Este archivo contiene las pruebas automatizadas, organizadas según la lista de comprobación. Cada prueba valida diferentes escenarios de creación de usuarios, con especial atención a las restricciones del parámetro firstName.
README.md: Este archivo explica el propósito del proyecto y proporciona instrucciones detalladas para ejecutarlo.
.gitignore: Define los archivos y directorios que deben ser ignorados por Git (como archivos temporales y dependencias).

# Lista de comprobación de pruebas

Pruebas Positivas:
Nombre con 2 caracteres en firstName:
La creación del usuario debe ser exitosa con un nombre que tenga exactamente 2 caracteres.

Nombre con 15 caracteres en firstName:
La creación del usuario debe ser exitosa con un nombre de 15 caracteres.

Nombre con caracteres latinos en firstName:
El nombre debe ser aceptado si contiene solo caracteres latinos.

Nombre con espacios:
El nombre con espacios debe ser aceptado.

Pruebas Negativas:
Nombre con 1 carácter en firstName:
La creación del usuario debe fallar si el nombre contiene solo 1 carácter.

Nombre con 16 caracteres en firstName:
La creación del usuario debe fallar si el nombre tiene más de 15 caracteres.

Uso de caracteres especiales en firstName:
Los nombres con caracteres especiales deben ser rechazados.

Nombre con números en firstName:
La creación del usuario debe fallar si el nombre contiene números.

Falta el parámetro firstName en la solicitud:
La solicitud debe fallar si el parámetro firstName está ausente.

Nombre vacío:
La creación del usuario debe fallar si el nombre está vacío.

Tipo de dato incorrecto en firstName:
La solicitud debe fallar si el valor de firstName no es una cadena de texto (por ejemplo, un número).


