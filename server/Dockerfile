# Verwende ein Node.js-Image als Basis
FROM node:14-slim

# Setze das Arbeitsverzeichnis innerhalb des Containers
WORKDIR /app

# Install build dependencies for bcrypt
RUN apt-get update && apt-get install -y build-essential python

# Kopiere die package.json- und package-lock.json-Dateien in den Container
COPY package*.json ./


# Install Node.js dependencies
RUN npm install

# Kopiere den restlichen Projektcode in den Container
COPY . .

# Setze die Umgebungsvariable für den Port
ENV PORT=5000

# Setze die Umgebungsvariable für die MongoDB-Verbindungs-URL
ENV MONGO_URL=mongodb+srv://muhammadhera:wahnsinn@cluster1.zd1gze6.mongodb.net/Chat?retryWrites=true&w=majority

# Exponiere den Port, auf dem der Server lauscht
EXPOSE 5000

# Starte die Anwendung
CMD ["node", "index.js"]
