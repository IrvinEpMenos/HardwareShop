# Usa una imagen oficial de Node.js
FROM node:18-alpine

# Establece el directorio de trabajo en el contenedor
WORKDIR /app

# Copia el package.json y package-lock.json
COPY package*.json ./

# Instala las dependencias
RUN npm install

# Copia el resto de la aplicación
COPY . .

# Compila la aplicación para producción
RUN npm run build

# Expone el puerto 3000
EXPOSE 3000

# Comando por defecto para ejecutar la app
CMD ["npm", "run", "start"]
