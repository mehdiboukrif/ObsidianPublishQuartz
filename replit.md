# Projet Quartz v4 - Jardin Numérique

## Vue d'ensemble

Ce projet utilise Quartz v4 pour transformer votre coffre Obsidian en un site web statique entièrement fonctionnel. Quartz est un générateur de site statique rapide qui prend en charge les fonctionnalités Obsidian comme les liens wiki, les backlinks, la recherche en texte intégral et plus encore.

## État actuel

**Date de configuration:** 10 novembre 2025

Le projet est configuré et fonctionne sur Replit avec :
- Node.js v22 (requis par Quartz v4)
- Port 5000 (au lieu du port par défaut 8080)
- Serveur configuré pour écouter sur 0.0.0.0 (compatible Replit)
- Workflow `quartz-dev` pour le serveur de développement

## Structure du projet

```
.
├── content/              # Vos fichiers Markdown (coffre Obsidian)
│   └── index.md          # Page d'accueil
├── public/               # Site généré (ignoré par Git)
├── quartz/               # Code source de Quartz
│   ├── cli/              # Interface en ligne de commande
│   ├── components/       # Composants de page
│   └── plugins/          # Plugins de transformation
├── quartz.config.ts      # Configuration de Quartz
└── quartz.layout.ts      # Configuration de la mise en page
```

## Modifications Replit

Pour que Quartz fonctionne correctement sur Replit, les modifications suivantes ont été apportées :

1. **Port par défaut:** Changé de 8080 à 5000 dans `quartz/cli/args.js`
2. **Bind address:** Le serveur écoute sur `0.0.0.0` au lieu de `localhost` dans `quartz/cli/handlers.js`

Ces modifications permettent au site d'être accessible via l'interface web de Replit.

## Utilisation

### Ajouter du contenu

1. Ajoutez vos fichiers Markdown dans le répertoire `content/`
2. Utilisez la syntaxe Markdown et Obsidian (liens wiki, backlinks, etc.)
3. Le serveur rechargera automatiquement vos modifications

### Commandes disponibles

- **Démarrer le serveur de développement:** Le workflow `quartz-dev` le fait automatiquement
- **Build manuel:** `npx quartz build`
- **Build + Preview:** `npx quartz build --serve`
- **Sync avec Git:** `npx quartz sync`

### Workflow

Le workflow `quartz-dev` est configuré pour :
- Commande: `npx quartz build --serve`
- Port: 5000
- Type: webview (affichage dans l'interface Replit)

## Configuration

### Configuration Quartz

Modifiez `quartz.config.ts` pour personnaliser :
- Métadonnées du site (titre, description, auteur)
- Langue et région
- Plugins activés
- Thème et apparence

### Configuration de la mise en page

Modifiez `quartz.layout.ts` pour personnaliser :
- Composants affichés sur chaque page
- Position des composants (gauche, droite, pied de page)
- Ordre d'affichage

## Fonctionnalités Quartz

- ✅ Compatibilité Obsidian complète
- ✅ Recherche en texte intégral
- ✅ Vue graphique des notes
- ✅ Liens wiki et transclusions
- ✅ Backlinks automatiques
- ✅ Support LaTeX
- ✅ Coloration syntaxique du code
- ✅ Aperçus popup
- ✅ Rechargement à chaud

## Prochaines étapes

1. **Ajouter votre contenu:** Copiez vos fichiers Markdown depuis votre coffre Obsidian vers `content/`
2. **Personnaliser la configuration:** Modifiez `quartz.config.ts` et `quartz.layout.ts`
3. **Tester localement:** Vérifiez que tout fonctionne dans l'aperçu Replit
4. **Déployer:** Utilisez le bouton "Publish" de Replit pour mettre en ligne

## Ressources

- [Documentation officielle Quartz](https://quartz.jzhao.xyz/)
- [Configuration](https://quartz.jzhao.xyz/configuration)
- [Mise en page](https://quartz.jzhao.xyz/layout)
- [Hébergement](https://quartz.jzhao.xyz/hosting)
- [Dépôt GitHub](https://github.com/jackyzha0/quartz)

## Notes techniques

- **Version Node.js:** v22+ (minimum requis)
- **Version npm:** v10.9.2+ (minimum requis)
- **Version Quartz:** v4.5.2
- **Port WebSocket:** 3001 (pour le rechargement à chaud)

## Préférences utilisateur

- Configuration par défaut de Quartz (standard)
- Langue: Français
- Prêt pour l'ajout de fichiers Obsidian existants
