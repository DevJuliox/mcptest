# MCP Test Repository

Este repositorio fue creado como un ejemplo para trabajar con servidores MCP (Model Context Protocol). A continuación, se detalla cómo configurar y trabajar con un servidor MCP desde cero.

## ¿Qué es MCP?
MCP (Model Context Protocol) es un protocolo diseñado para facilitar la interacción entre modelos y contextos en aplicaciones modernas. Los servidores MCP permiten gestionar y ejecutar estas interacciones de manera eficiente.

## Pasos para configurar un servidor MCP desde cero

### 1. Requisitos previos
Antes de comenzar, asegúrate de tener lo siguiente instalado en tu sistema:

- [Node.js](https://nodejs.org/) (versión 16 o superior)
- [Git](https://git-scm.com/)
- Un editor de texto como [Visual Studio Code](https://code.visualstudio.com/)

### 2. Crear un repositorio en GitHub
Este repositorio fue creado utilizando la API de GitHub. Puedes crear uno manualmente siguiendo estos pasos:

1. Ve a [GitHub](https://github.com/) y haz clic en "New Repository".
2. Asigna un nombre al repositorio (por ejemplo, `mcptest`).
3. Configura la visibilidad (público o privado) y haz clic en "Create Repository".

### 3. Configurar un servidor MCP

1. Instala el paquete del servidor MCP de GitHub ejecutando el siguiente comando:

   ```bash
   npx -y @modelcontextprotocol/server-github
   ```

2. Configura tu token de acceso personal de GitHub. Asegúrate de que el token tenga los permisos necesarios para acceder a tus repositorios. Puedes configurarlo en tu entorno de desarrollo agregando una variable de entorno:

   ```bash
   export GITHUB_PERSONAL_ACCESS_TOKEN=tu_token_aqui
   ```

   En Windows, puedes configurarlo en tu archivo de configuración de Visual Studio Code (`settings.json`):

   ```json
   "mcp": {
       "servers": {
           "github": {
               "command": "npx",
               "args": [
                   "-y",
                   "@modelcontextprotocol/server-github"
               ],
               "env": {
                   "GITHUB_PERSONAL_ACCESS_TOKEN": "tu_token_aqui"
               }
           }
       }
   }
   ```

3. Ejecuta el servidor MCP:

   ```bash
   npx @modelcontextprotocol/server-github
   ```

### 4. Probar el servidor MCP

Una vez que el servidor esté en ejecución, puedes interactuar con él utilizando herramientas como `curl` o integrándolo en tu aplicación.

### 5. Recursos adicionales

- [Documentación oficial de MCP](https://modelcontextprotocol.org/)
- [Repositorio de ejemplo de MCP](https://github.com/activepieces/activepieces)

## Contribuciones
Si deseas contribuir a este repositorio, por favor abre un issue o envía un pull request.

---

¡Gracias por explorar MCP con nosotros!