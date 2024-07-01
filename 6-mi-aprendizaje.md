# COMPLETAR  
Comparando sus conocimientos antes de hacer la práctica con sus conocimientos después de hacer la tarea, explicar los principales aprendizajes logrados para beneficio de su formación profesional.  
Si solucionó un problema presentado al realizar la práctica también se debe documentar.


### Comprensión de Volúmenes en Docker

**Antes de la práctica:** Tenía un conocimiento básico sobre los volúmenes en Docker, pero no comprendía completamente las diferencias entre volúmenes nombrados y anónimos, ni cómo gestionarlos de manera eficaz.

**Después de la práctica:** He adquirido una comprensión clara sobre:

- **Volúmenes Nombrados:** Cómo crear, montar y gestionar volúmenes nombrados para el almacenamiento persistente de datos.
- **Volúmenes Anónimos:** La utilidad de los volúmenes anónimos para almacenamiento temporal y cómo Docker los maneja automáticamente.
- **Gestión de Volúmenes:** La importancia de gestionar volúmenes para evitar la acumulación de datos innecesarios, y cómo eliminar volúmenes no utilizados con `docker volume prune`.

### Creación y Configuración de Redes en Docker

**Antes de la práctica:** Sabía que Docker permitía la creación de redes, pero no tenía experiencia en la configuración detallada y el uso de redes personalizadas para contenedores.

**Después de la práctica:** He aprendido a:

- **Crear Redes Personalizadas:** Crear redes de tipo bridge y conectar múltiples contenedores a una red específica para permitir la comunicación interna entre ellos.
- **Configuración de Redes:** Configurar contenedores para que se comuniquen usando nombres de contenedores en lugar de direcciones IP, mejorando la flexibilidad y la gestión de aplicaciones distribuidas.

### Implementación y Configuración de Servicios Complejos

**Antes de la práctica:** No tenía experiencia práctica en la configuración de servicios complejos en Docker, como bases de datos y servidores web, ni en la integración de estos servicios en una red Docker.

**Después de la práctica:** He adquirido habilidades prácticas en:

- **Configuración de PostgreSQL y pgAdmin:** Configurar y ejecutar contenedores para PostgreSQL y pgAdmin, y vincularlos en una red Docker para la administración de bases de datos.
- **Despliegue de Aplicaciones Web (Drupal):** Implementar y configurar un sitio web Drupal, incluyendo la configuración de volúmenes para almacenamiento de datos persistente y la solución de problemas relacionados con permisos de archivos y directorios.

### Solución de Problemas Presentados

**Problema:** Permisos de Archivos y Directorios en Drupal  
**Situación:** Durante la instalación de Drupal, surgió un error relacionado con los permisos de los directorios necesarios (sites/default/files).

**Solución:**

- **Análisis:** Identifiqué que el problema estaba relacionado con los permisos de escritura del servidor web en los directorios necesarios.
- **Acciones Tomadas:**
  - Ingresar al contenedor de Drupal: Utilicé `docker exec -it server-drupal /bin/bash` para ingresar al contenedor.
  - Crear Directorios Necesarios: Creé manualmente el directorio `translations` usando `mkdir -p /var/www/html/sites/default/files/translations`.
  - Establecer Permisos Correctos: Ajusté los permisos y la propiedad de los directorios usando `chown -R www-data:www-data /var/www/html/sites/default/files` y `chmod -R 755 /var/www/html/sites/default/files`.
- **Resultado:** La configuración correcta de permisos permitió que la instalación de Drupal continuara sin problemas.

### Reflexión Final

La práctica con Docker ha sido extremadamente valiosa para mi formación profesional. No solo he mejorado mis habilidades técnicas en la gestión de contenedores, redes y volúmenes, sino que también he aprendido a resolver problemas prácticos que pueden surgir en un entorno de desarrollo real. Estos aprendizajes son esenciales para mi desarrollo como profesional en el ámbito de DevOps y la administración de sistemas.