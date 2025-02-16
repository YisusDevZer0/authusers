# authusers
 Uso de redux


 
🛠️ Instrucciones para iniciar el proyecto authusers en React desde GitHub
1️⃣ Clonar el repositorio
Abre tu terminal y ejecuta el siguiente comando para clonar el proyecto desde GitHub:

bash
Copiar
Editar
git clone https://github.com/YisusDevZer0/authusers.git
cd authusers
2️⃣ Instalar las dependencias
Una vez dentro de la carpeta del proyecto, instala todas las dependencias que están listadas en el archivo package.json con el siguiente comando:

bash
Copiar
Editar
npm install
3️⃣ Iniciar el proyecto con compatibilidad para OpenSSL
Debido a un problema de compatibilidad entre Node.js y Webpack, es necesario agregar una variable de entorno para que el proyecto funcione correctamente. Ejecuta el siguiente comando:

bash
Copiar
Editar
set NODE_OPTIONS=--openssl-legacy-provider
npm start
Esto abrirá automáticamente la aplicación en tu navegador en la dirección:
http://localhost:3000

Nota: Si usas Linux o Mac, el comando es:

bash
Copiar
Editar
export NODE_OPTIONS=--openssl-legacy-provider
npm start
4️⃣ Opcional: Agregar el ajuste permanente en package.json
Si deseas evitar escribir el comando cada vez, edita el archivo package.json y busca esta sección:

json
Copiar
Editar
"scripts": {
  "start": "react-scripts start"
}
Reemplázala por:

json
Copiar
Editar
"scripts": {
  "start": "set NODE_OPTIONS=--openssl-legacy-provider && react-scripts start"
}
Así, cada vez que ejecutes npm start, el ajuste se aplicará automáticamente.

🔍 Verificar configuración (opcional)
Si encuentras algún error adicional al iniciar el proyecto, revisa lo siguiente:

✅ Versión de Node.js: Se recomienda tener >= 16.x y < 18.x.
🔑 Variables de entorno: Si existe un archivo llamado .env.example, cópialo y renómbralo a .env para configurar las variables necesarias.
