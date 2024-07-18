# DJ4H-CPA

Bot de distribution automatique des points pour le jeu des 4 heures du serveur Développons!

Développons! Jeu des 4 Heures - Détection de Points Automatique (DJ4H-CPA)

## Fonctionnement

Le comportement attendu du bot est détaillé dans le 
[cahier des charges](Cahier%20des%20charges%20-%20DJ4H-CPA.pdf).

## Mise en place

### Prérequis

- [Python](https://python.org/)
- [Pycord](https://pycord.dev) (`pip install py-cord`)

### Instructions

1. Ajouter une variable d'environnement nommée `DISCORD_TOKEN` avec votre token du bot comme valeur
2. Démarrer le bot :
```shell
python bot.py
```

## Utilisation

### Installation

Une fois le bot invité sur le serveur, il est nécessaire de le configurer avec la commande 
`/setup [canal] (temps) (historique)`. Cette commande permet de spécifier le canal du serveur dans lequel le jeu aura lieu,
la durée (en heure) minimum entre deux messages pour marquer un point, ainsi que le canal où seront envoyés l'historique 
des gains de points.

Paramètres :
- `canal: discord.TextChannel` (obligatoire) : Le canal textuel dédié au jeu.
- `temps: int` (optionnel) : Durée minimum requise entre deux messages pour marquer un point. Cette valeur doit être 
comprise entre `1`et `10`. La valeur par défaut est `4`.
- `historique: discord.TextChannel` (optionnel) : Un message sera envoyé à chaque fois qu'un nouveau gagnant est désigné.

> **Remarques :**
> - Il n'est possible d'avoir qu'un seul canal dédié au jeu dans un serveur.
> - L'usage de cette commande nécessite la permission "Gérer le serveur".
