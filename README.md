# Tuffting Raymo

Application web responsive en français pour créer des patrons de tufting à partir d'images.

## Fonctions
- Import d'images, extraction de palette de couleurs et génération de patron en grille.
- Dimensions personnalisées et formats prédéfinis.
- Calques par couleur, export PNG et impression en PDF.
- Sauvegarde locale et synchronisation cloud avec Supabase Auth, Database et Storage.

## Supabase
Projet configuré dans supabase-config.js avec une clé publishable côté navigateur.
Table attendue : public.tuffting_projects.
Bucket privé : tuffting-files.
Les politiques RLS doivent limiter chaque ligne à auth.uid() = user_id et les objets au dossier UID de l'utilisateur.

## Déploiement Cloudflare Pages
Framework preset : None ; Build command : vide ; Build output directory : /.

## Limites
Le patron généré est une grille de couleurs préparatoire. Le rendu photoréaliste de fibres et l'estimation des quantités de fil ne sont pas inclus.