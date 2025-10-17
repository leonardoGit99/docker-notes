1. Levantar stack al inicio del dia:
	- `docker compose up -d`
		- Levanta todos los contenedores (frontend, backend, base de datos, etc.)
		- -d, detached o segundo plano.
2. Trabajar normalmente:
	- Si cambia algo en el codigo
		- Puedo reconstruir solo el servicio de la imagen que cambió
			- `docker compose build frontend`
			- `docker compose up -d frontend`
3. Al final del dia:
	- Puedo dejar los contenedores corriendo y apagarlos con stop
		- `docker compose stop`
	- La proxima vez que inicie el proyecto, solo hago
		- `docker compose start`

	

---
### Cuando usar `down`

- Cuando quiera limpiar todo:
	- Cambios en la configuracion de la base de datos
	- Cambios en el docker-compose.yml
	- Reiniciar todo desde cero

>  Elimina contenedores, redes y volumenes
	 docker compose down -v
	
>  Recrea todo
	docker compose up -d