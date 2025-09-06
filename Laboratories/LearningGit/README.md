# LABORATORIO 1- INTRODUCCIÓN GIT 
## INTEGRANTES
Cesar Andres Borray Suarez

Haider Andres Rodriguez Maldonado

## PARTE II (Trabajo en parejas).
### Creacion Repositorio Compartido

![Repositorio](/Capturas/Captura1.png)
![Contribuidores](/Capturas/Captura2.png)

### Editar el archivo README.md al mismo tiempo

Al editar el archivo README.md y intentar subirlo al repositorio al mismo tiempo, uno de los dos lograba subir el cambio mientras que al otro le aparecia un error al intentar hacer el push debido a que Git detectará que el repositorio remoto ha cambiado (debido al push exitoso del primer usuario).

![Fallo Github](/Capturas/Captura3.png)
![Fallo Consola](/Capturas/Captura4.png)

### Resolucion de conflictos

Si ambos usuarios han editado la misma parte del archivo README.md, el segundo usuario deberá hacer un pull para traer los cambios del repositorio remoto:
```
git pull origin main
```

Durante el pull, Git intentará fusionar los cambios automáticamente, pero si ambos usuarios editaron las mismas líneas, Git generará un conflicto de fusión. El archivo README.md tendrá secciones marcadas como:

![Resolucion VS](/Capturas/Captura5.png)

Aquí, debemos editar el archivo manualmente para combinar o elegir entre los cambios (aqui combinamos los cambios).

![Cambios README](/Capturas/Captura6.png)

Finalmente, el usuario puede intentar hacer el push nuevamente.

## PARTE III (Trabajo de a parejas)

### Mejor forma para no tener conflictos

En lugar de trabajar directamente en la rama main o master, podemos hacer el **uso de ramas (branches)** para el desarrollo, cada desarrollador debe crear una nueva rama para trabajar en una característica o bug específico. Esto aísla los cambios y reduce la probabilidad de conflictos.

###  Pull Request (PR)

**Que es:**
Es una solicitud de fusión de cambios desde una rama de trabajo a otra rama (generalmente main o master) en un repositorio de Git. Es una forma de notificar a otros colaboradores del proyecto que has hecho cambios que te gustaría que se revisaran e integraran en el código principal.

**Como funciona:**
1. **Crear una rama:** Trabajas en una nueva funcionalidad o corrección en una rama separada.
2. **Realizar cambios:** Haces commits de los cambios en esa rama y la subes al repositorio remoto.
3. **Crear el PR:** En la plataforma de Git (GitHub, GitLab, etc.), creas un Pull Request solicitando la fusión de tu rama con la rama principal.
4. **Revisión:** Otros miembros del equipo revisan, comentan y aprueban los cambios.
5. **Fusión:** Si es aprobado, el PR se fusiona con la rama principal y el PR se cierra.

### Creacion de Ramas

![Creacion Ramas](/Capturas/Captura7.png)

### Cambios y Realizacion Pull Request

Se realizan los cambios en el README.md en ambas ramas y lanzamos el pull request.

![Pull Requests](/Capturas/Captura8.png)

Revisamos y aceptamos el primer pull request, posteriormente la rama de desarrollo se borra.

![Pull Requests](/Capturas/Captura9.png)
![Pull Requests](/Capturas/Captura10.png)

Ahora intentamos revisar y hacer el pull request, como en la rama main ya hay cambios que en el pull no se encuentran, debemos modificar el pull para poderlo aceptar y que no genere conflictos.

![Pull Requests](/Capturas/Captura11.png)
![Pull Requests](/Capturas/Captura12.png)

Una vez editado el pull request podremos aceptarlo y finalmente la rama se deberia borrar.

![Pull Requests](/Capturas/Captura13.png)
![Pull Requests](/Capturas/Captura14.png)