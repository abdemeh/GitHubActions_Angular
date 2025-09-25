# 🚀 GitHubActions_Angular

[![PR Lint](https://github.com/abdemeh/GitHubActions_Angular/actions/workflows/pr-lint.yml/badge.svg)](https://github.com/abdemeh/GitHubActions_Angular/actions/workflows/pr-lint.yml)
[![Deploy to GitHub Pages](https://github.com/abdemeh/GitHubActions_Angular/actions/workflows/deploy-pages.yml/badge.svg)](https://github.com/abdemeh/GitHubActions_Angular/actions/workflows/deploy-pages.yml)

Un projet de démonstration Angular avec **GitHub Actions** pour mettre en place :
- ✅ Un pipeline de **lint** automatique à chaque Pull Request  
- ✅ Un pipeline de **déploiement** vers **GitHub Pages** après un merge sur `main`

---

## 🌍 Site déployé

👉 [Voir le site en ligne](https://abdemeh.github.io/GitHubActions_Angular/)

---

## 📂 Structure du projet

```
TP-GITHUBACTIONS/
├── .github/
│   └── workflows/
│       ├── deploy-pages.yml     # Déploiement auto sur GitHub Pages
│       └── pr-lint.yml          # Lint du code sur chaque PR
├── dist/
│   └── hello-world/
│       ├── browser/
│       └── server/
├── node_modules/
├── public/
├── src/
│   └── app/
├── .eslintrc.json
├── angular.json
├── eslint.config.js
├── package-lock.json
├── package.json
├── README.md
├── tsconfig.app.json
├── tsconfig.json
└── tsconfig.spec.json
```

---

## ⚙️ Pipelines CI/CD

### 1. **Lint sur Pull Request**
Fichier : `.github/workflows/pr-lint.yml`  
- Déclenché à chaque **pull request** vers `main`  
- Vérifie la qualité du code avec ESLint (`npm run lint`)  
- Bloque la fusion si des erreurs sont détectées  

### 2. **Déploiement sur GitHub Pages**
Fichier : `.github/workflows/deploy-pages.yml`  
- Déclenché après un **merge sur `main`**  
- Construit l'application Angular avec `ng build`  
- Déploie automatiquement le contenu de `dist/` sur **GitHub Pages**  

---

## 🚀 Lancer le projet en local

### 1. Installer les dépendances
```bash
npm install
```

### 2. Lancer en mode développement
```bash
npm start
```
➡️ Le projet sera accessible sur http://localhost:4200/

### 3. Lancer le lint localement
```bash
npm run lint
```

### 4. Build en production
```bash
npm run build -- --configuration=production --base-href "/GitHubActions_Angular/"
```
➡️ Le build est généré dans `dist/`.

---

## 🤝 Contribuer

### Créer une branche de feature
```bash
git checkout -b feature/ma-feature
```

### Commit & push
```bash
git add .
git commit -m "feat: ajout de ma feature"
git push origin feature/ma-feature
```

### Ouvrir une Pull Request → le pipeline PR Lint doit passer ✅
### Après merge → déploiement automatique sur GitHub Pages 🎉

---

## 📌 Liens utiles

- [Documentation Angular](https://angular.io/docs)
- [GitHub Actions](https://docs.github.com/en/actions)
- [GitHub Pages](https://pages.github.com/)