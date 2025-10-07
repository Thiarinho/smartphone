# 1. Utiliser une image de base complète (pas Alpine)
FROM node:18

# 2. Créer un dossier de travail dans le conteneur
WORKDIR /app

# 3. Copier uniquement les fichiers de dépendances
COPY package*.json ./

# 4. Installer les dépendances en mode production
RUN npm install --production

# 5. Copier le reste du code source
COPY . .

# 6. Définir les variables d'environnement par défaut
ENV PORT=5000
ENV MONGO_URI=mongodb://mongo:27017/smartphoneDB
ENV DELETE_CODE=123

# 7. Ouvrir le port du backend
EXPOSE 5000

# 8. Commande pour démarrer ton serveur Express
CMD ["npm", "start"]
