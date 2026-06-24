
# ControlStore

# instrucciones del repositorio 

lo primero que se debe hacer es clonar el repositorio 
"git clone https://github.com/maicolMC/ControlStore.git"
luego de deberan cambiarse a la rama develop que es la rama donde estaremos trabajando el codigo mientras esta en fase de pruebas 
usando este comando " git checkout develop " para verificar que estas en la rama correcta usen este codigo " git branch "
deben de tener instalado git y docker desktop 

despues que tengamos clonado el repositorio 
iran a la direccion en donde copiaron el repositorio
y crearan un archivo .env usando este comando :
" Set-Content -Path .env -Value 'POSTGRES_DB=controlstore
POSTGRES_USER=postgres
POSTGRES_PASSWORD=postgres
POSTGRES_HOST=postgres_db
POSTGRES_PORT=5432

REDIS_HOST=redis_cache
REDIS_PORT=6379' "
Esto generará el archivo .env con todo el contenido de una sola vez.

Para construir y levantar los contenedores con Docker
usan este comando " docker-compose up --build "
Esto iniciará tres servicios:
PostgreSQL en el puerto 5432
Redis en el puerto 6379
Django backend en el puerto 8000

cuando vayan a crear o añadir un cambio o una funcion nueva al codigo se hara todo en la rama develop hasta que pasen las pruebas de calidad 
despues que terminen de crear la nueva funcionalidad o parte del codigo en la rama principal del proyecto ponen este codigo esto preparara los cambios que han hecho para subirlos al repositorio de prueba 
" git add .
git commit -m "Descripción clara del cambio" "

y con este ya subiran su codigo al repositorio en la rama de developt 
" git push origin develop "
cuando pase la fase de pruebas se hara un pull request desde github para implementar en la rama main los cambios que se aprobaron de la rama de desarrollo 
