# Verwende ein Node.js-Image als Basis
FROM node:14-slim

# Setze das Arbeitsverzeichnis innerhalb des Containers
WORKDIR /app

# Kopiere die package.json- und package-lock.json-Dateien in den Container
COPY package*.json ./

# Installiere die Abhängigkeiten
RUN npm install

# Kopiere den restlichen Projektcode in den Container
COPY . .

# Setze die Umgebungsvariable für den Port
ENV PORT=3000

# Exponiere den Port, auf dem der Server lauscht
EXPOSE 3000

# Starte die Anwendung
CMD ["npm", "start"]
