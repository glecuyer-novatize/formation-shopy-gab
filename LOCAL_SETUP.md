# Setup local Shopify

Ce projet part du theme officiel Shopify Horizon.

## 1. Creer le dev store

Dans le portail Partner/Dev Dashboard Shopify:

1. Ouvrir `https://www.shopify.com/ca/partners`.
2. Se connecter au compte Partner.
3. Aller dans Stores.
4. Creer un store de type Dev.
5. Choisir le plan Basic pour un store de base.
6. Noter le domaine `myshopify.com` du store.

Le navigateur integre Codex bloque actuellement `partners.shopify.com`, donc cette etape doit etre faite dans ton navigateur.

## 2. Connecter le theme local

Depuis ce dossier:

```sh
shopify auth login
shopify theme dev --store nom-du-store.myshopify.com
```

La commande `theme dev` cree un theme de developpement et pousse les changements locaux en temps reel.

## 3. Publier ou pousser une version

Pour creer ou mettre a jour un theme distant sans le publier:

```sh
shopify theme push --store nom-du-store.myshopify.com --unpublished --theme "Horizon - development"
```

Pour publier un theme distant, utiliser `shopify theme publish` seulement apres validation.

## 4. Git

Le remote Shopify Horizon est conserve comme `upstream` pour recuperer les mises a jour officielles.
Le remote `origin` est reserve au futur depot client ou au gestionnaire de branches.
