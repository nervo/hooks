# Hooks

## Installation

Après avoir récupéré le code du projet, vous devez executer le script bin/bootstrap, celui-ci va vous ajouter une nouvelle commande git, git install hook.

Ensuite vous prenez un projet sur lequel vous voulez installer les hooks et vous faîtes un

```shell
git-install-hook
```

## Configuration

Au niveau de votre projet vous devez créer un fichier .csconfig qui peut contenir les variables suivantes:

- PHPCS_CODING_STANDARD (PSR2 par défaut)
- PHPCS_IGNORE la liste des fichiers à ignorer ("" par défaut)
- PHPCS_FILE_PATTERN format des fichiers à traiter (par défaut "\.php$"")
- PHPCS_ENCODING (encodage du code, "" par défaut)
- PHPCS_IGNORE_WARNINGS (permet de ne pas bloquer les commit si les erreurs ne sont - que des warnings, par exemple le nombre de caractères par ligne)

Exemple de fichier:

```shell
PHPCS_CODING_STANDARD=PSR2
PHPCS_IGNORE=app/,web/
PHPCS_IGNORE_WARNINGS=1
```
Si vous avez des problèmes lors de l'éxecution des hooks (si vous utilisez un outil comme tower), vous pouvez ajouter un fichier config dans le dossiers .git/hooks, dans lequel vous pouvez définr le chemin version PHP et vers PHPCS

```shell
PHP_BIN=/usr/local/bin/php
PHPCS_BIN=/usr/local/bin/phpcs
```
