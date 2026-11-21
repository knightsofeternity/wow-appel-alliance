# Appel d'Alliance

L'add-on d'appel de groupe partagé par les Knights of Eternity et Les Cassos de la Lumière,
dans WoW Forever. Chaque demande de groupe d'une des deux guildes devient une alerte chez
les autres : un son, une petite fenêtre, un bouton « Intéressé ».

Il ne marche qu'à l'intérieur d'une faction : un canal personnalisé ne traverse pas
Alliance et Horde. Sur un personnage Horde ou hors des deux guildes, il reste inactif.

- [`AppelAlliance/`](AppelAlliance/README.md) : l'add-on (`/alliance`, `/aa`).
- [`AppelAllianceSonde/`](AppelAllianceSonde/README.md) : la sonde du lot 0 (`/aa0`), qui vérifie
  en jeu que les deux guildes peuvent se parler.

Le mot de passe du canal et les liens Discord sont dans `AppelAlliance/Config.lua`.
Ce dépôt est privé pour cette raison.

## Installation

Copier `AppelAlliance/` dans `Interface/AddOns/` de WoW Forever.

## Tests

Bancs hors jeu en Lua 5.1. Sans Lua installé :

```bash
docker run --rm -v "$PWD":/w -w /w alpine:3.20 sh -c "apk add -q lua5.1 >/dev/null 2>&1 && lua5.1 test/alliance.lua && lua5.1 test/sonde.lua"
```
