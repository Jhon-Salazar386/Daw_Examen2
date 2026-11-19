# Pruebas del examen

## 1-Construccion de la imagen

Modificacion del index.html para colocar mi puesto p12
<img width="768" height="412" alt="image" src="https://github.com/user-attachments/assets/e475f784-9f19-45cd-a3a8-b9eedc8cba5e" />

Imagen final del Dockerfile

<img width="632" height="169" alt="image" src="https://github.com/user-attachments/assets/00a59d4b-8a17-4dac-a626-2431975bc494" />

Prueba de la construccion de la imagen

<img width="974" height="113" alt="image" src="https://github.com/user-attachments/assets/fb555857-9467-451d-b512-7af570cf05b8" />

## 2-Red y despliegue

ip y mascara de red de ambos escritorios

<img width="646" height="183" alt="image" src="https://github.com/user-attachments/assets/4729b6e7-590c-4710-87f0-dc960c0b75d6" />

<img width="799" height="172" alt="image" src="https://github.com/user-attachments/assets/5cc66d9c-0c2c-416b-85f1-eb5a8be8b6a9" />

<hr>

Configuracion del docker compose

<img width="1084" height="713" alt="image" src="https://github.com/user-attachments/assets/565a7c6c-cb24-4598-91e0-303fe05a8db7" />

<img width="1850" height="806" alt="image" src="https://github.com/user-attachments/assets/367cc816-4dc4-4cb5-9511-d9770592e4ba" />

Tuve que cambiar los permisos del index.html para poder realizar la lectura sobre el archivo y evitar error 403

he usado sudo chmod 644 archivo para darle los permisos necesario y posterior mente monte el contenedor usando --build para reconstruir la imagen

desde cliente:

<img width="800" height="622" alt="image" src="https://github.com/user-attachments/assets/b9a37059-544c-41c1-a449-955dac5b64cb" />

<img width="463" height="191" alt="image" src="https://github.com/user-attachments/assets/cdaf787c-7689-433a-bffb-397be5b08f49" />

justificacion de puertos: 

se ha optado por usar la ip del host del servidor para poder servir los archivos html y que puedan ser accesibles en el puerto 8080 del host y 80(por defecto de apache) del contenedor

## 3-Actualizacion de portal

<img width="1136" height="808" alt="image" src="https://github.com/user-attachments/assets/e586f4eb-ff5e-4c96-801e-b0d147e2fb9a" />

<img width="963" height="147" alt="image" src="https://github.com/user-attachments/assets/640c0cc1-303b-41b1-ba28-207b6931a06e" />

<img width="815" height="112" alt="image" src="https://github.com/user-attachments/assets/e0f82158-f2e4-44b1-b8eb-e7ba56efdb09" />

<img width="1336" height="111" alt="image" src="https://github.com/user-attachments/assets/76a01601-bef1-45c6-9869-c9c3dac640e1" />

<img width="1839" height="627" alt="image" src="https://github.com/user-attachments/assets/24f55937-3faa-4f54-b5c3-f079f5e334bd" />

en el cliente:

<img width="700" height="239" alt="image" src="https://github.com/user-attachments/assets/070ddb3d-558c-4a69-b11c-6fca6ee6a1e9" />

<img width="797" height="511" alt="image" src="https://github.com/user-attachments/assets/1b21d4f3-8a54-42f3-8d87-bd6677ef3461" />


## 4-Acceso por dns

<img width="687" height="156" alt="image" src="https://github.com/user-attachments/assets/c9151a78-4610-424b-9b96-e66a1631de48" />

<img width="769" height="182" alt="image" src="https://github.com/user-attachments/assets/7b15a619-51e9-49b6-96bd-4482299986ec" />

<img width="800" height="222" alt="image" src="https://github.com/user-attachments/assets/7f6f4df0-9cb2-4140-b686-effd425ae6f1" />

<img width="791" height="500" alt="image" src="https://github.com/user-attachments/assets/1a1d7ca0-32c7-480f-9777-161238c52a54" />

<img width="600" height="172" alt="image" src="https://github.com/user-attachments/assets/666ea2c8-470e-433d-830e-d2d6a7a5c22b" />

<img width="637" height="236" alt="image" src="https://github.com/user-attachments/assets/970f2206-35a6-46da-8908-2ab7f6c0404a" />

Confirmaciones con comando dig

<img width="797" height="538" alt="image" src="https://github.com/user-attachments/assets/b291f773-9f86-4ae9-964c-a68a1f4c0830" />

<img width="795" height="463" alt="image" src="https://github.com/user-attachments/assets/d170c06a-9cb8-4dbd-83c7-c03356688502" />

Accediendo a la web mediante sus alias

<img width="1918" height="944" alt="image" src="https://github.com/user-attachments/assets/63fc7a8c-1802-41d6-ad7f-46c877f5e4ca" />

<img width="1913" height="910" alt="image" src="https://github.com/user-attachments/assets/c135c658-45cf-4117-9d68-ee9a197f70ce" />


## 5-Diagnostico de una incidencia

### ¿Que pasaba?

La ip de publicacion asignada era localhost, por lo que solo apuntaba al mismo contenedor docker

<img width="283" height="122" alt="image" src="https://github.com/user-attachments/assets/b22360ea-0a43-4535-8174-4eb85656935b" />

La ruta en donde se alojaba estado.html no era accesible y aparecia error 404

<img width="602" height="105" alt="image" src="https://github.com/user-attachments/assets/8e090ddb-4d3b-4789-8ad7-666c0c003c50" />

El archivo index.html no tenia permisos de lectura para todos, lo que ocacionaba un error 403

<img width="789" height="356" alt="image" src="https://github.com/user-attachments/assets/72c424ab-6774-470c-81a8-4a0efcac3d1a" />


### Solucion

Cambiar el puerto publicado al del host, para evitar que apunte al contenedor de docker

<img width="797" height="404" alt="image" src="https://github.com/user-attachments/assets/a5339ebc-e913-4f2f-a100-f59343b75586" />

Elimine de la ruta de copiado del archivo estado.html, eliminando la carpeta intermedia recursos dejandola en /usr/local/apache2/htdocs(Solo fue una alternativa)

<img width="613" height="105" alt="image" src="https://github.com/user-attachments/assets/9e69f2b1-0300-4f3a-a255-123c13361021" />

Cambiar los permisos de los archivos html para poder leerlos

<img width="1116" height="82" alt="image" src="https://github.com/user-attachments/assets/fcbaccc8-401b-4ecc-8f62-12c50072bf23" />

### Resultado

Ambas paginas ya son accesibles

<img width="792" height="510" alt="image" src="https://github.com/user-attachments/assets/06dfd4cf-4e26-4b38-b909-6e8ed360c286" />

<img width="796" height="532" alt="image" src="https://github.com/user-attachments/assets/e438b054-d925-4549-8248-c2e54d5131bf" />

<img width="1172" height="447" alt="image" src="https://github.com/user-attachments/assets/15a3d364-0788-4bcd-a82f-789fdeaf925f" />

<img width="1220" height="435" alt="image" src="https://github.com/user-attachments/assets/5b2bf750-446e-4d88-a507-71e408ae518c" />



