# Instalación y configuración local con ProperDocs

## 1. Git instalado y configurado

Ejecuto el comando: "git config --global --list", en el terminal del VSCode.

![Git instalado y configurado](img/git-configurado.png)

## 2. GitHub CLI configurado

Se instaló GitHub CLI y se comprobó la autenticación con:
R
```bash
gh auth status
```

![GitHub CLI configurado](img/gh-auth-status.png)

## 3. Herd con PHP 8.4

Se instaló Herd y se seleccionó la versión PHP 8.4.

![Herd con PHP 8.4](img/herd-php-84.png)

## 4. Repositorio clonado

Se clonó el repositorio `misitio` en local:

```bash
git remote -v
```

![Repositorio misitio clonado](img/misitio-clonado.png)

## 5. Sitio enlazado y servido con HTTPS

Se enlazó la carpeta `misitio` con Herd y se comprobó que el sitio se sirve mediante HTTPS.

![misitio servido por Herd mediante HTTPS](img/herd-misitio-https.png)

## Resumen de Read the Docs

Se utilizaron títulos, texto, bloques de código e imágenes Markdown. Read the Docs aporta el tema, la navegación y la organización de la documentación. No se necesitan plugins adicionales para este contenido.
