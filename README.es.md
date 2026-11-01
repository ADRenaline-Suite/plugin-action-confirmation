<p align="right">Idioma:&emsp;<a href="README.md" style="vertical-align:middle"><img alt="English" src="https://raw.githubusercontent.com/ADRenaline-Suite/.github/main/profile/lang-en-off.svg" align="middle" style="vertical-align:middle"></a> <img alt="Español" src="https://raw.githubusercontent.com/ADRenaline-Suite/.github/main/profile/lang-es-on.svg" align="middle" style="vertical-align:middle"></p>

# Confirmación de acciones (`plugin-action-confirmation`)

Deja pasar una escritura solo cuando este turno contiene la frase allow exacta para ese destino.

Las instrucciones están en inglés. El archivo que guarda el plugin sigue el idioma del pedido. Este plugin no escribe ningún archivo.

## /confirm-action

Una clase, un destino, una escritura. La línea es `allow-<class>: <target> — <what>`. Una insinuación, un plan o «cuando puedas» no es la frase.

## Ayuda

## /confirm-help

El catálogo de este plugin. No escribe un archivo.

## Para quién es

Quien quiere una frase humana antes de una escritura en base, un push, una escritura en GitHub, un despliegue o un cambio de infraestructura. El requisito de seguridad queda en `plugin-security`. La escritura en sí queda en el plugin que la hace. Este plugin no copia sus skills.

## Qué incluye

Portable, para cualquier agente que siga [Agent Skills](https://agentskills.io/specification):

- `confirm-action` comprueba la frase antes de la escritura.

Cursor y Claude Code: los commands de arriba. En Cursor, `/confirm-action`. En Claude Code, `/plugin-action-confirmation:confirm-action`.

Solo Cursor: las rules `output-folder`, `phrase-this-turn`. Claude Code no carga rules. Las mismas restricciones están en los skills.

## Instalar

En Cursor, instala el plugin desde este repositorio en Customize.

En Claude Code:

```text
claude plugin marketplace add ADRenaline-Suite/plugin-action-confirmation
claude plugin install plugin-action-confirmation@plugin-action-confirmation
```

Para probar una copia local, arranca Claude Code con `claude --plugin-dir <ruta de este repositorio>`.

## Ejemplo

Un `UPDATE` en Postgres espera hasta que este turno contenga `allow-db-update: <base> — <qué>`. Un `DELETE` usa `allow-db-delete`. No hay una clase `postgres`. Un `SELECT`, una edición local, `git add` y `git commit` no pasan por la puerta.

## Configuración

Este plugin no escribe archivos y no tiene carpeta de salida. Las clases son `db-update`, `db-delete`, `git-push`, `github-write`, `deploy` e `infra`.

## Licencia

MIT. Copyright (c) 2026 Ricardo Plascencia.

