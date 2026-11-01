---
name: confirm-action
description: Comprueba que este turno contiene la frase allow exacta antes de una escritura.
---

<p align="right">Idioma:&emsp;<a href="SKILL.md" style="vertical-align:middle"><img alt="English" src="https://raw.githubusercontent.com/ADRenaline-Suite/.github/main/profile/lang-en-off.svg" align="middle" style="vertical-align:middle"></a> <img alt="Español" src="https://raw.githubusercontent.com/ADRenaline-Suite/.github/main/profile/lang-es-on.svg" align="middle" style="vertical-align:middle"></p>

[🏠 Action Confirmation](../../README.md)

# Comprueba que este turno contiene la frase allow exacta antes de una escritura

Sin frase, no hay escritura. La clase es una de las seis. El destino es el de la frase.

Source: OWASP Top 10 for LLM Applications 2025, LLM06:2025 Excessive Agency. La puerta está fuera del modelo: la frase de la persona, no una oración que el modelo añade.

## Antes de escribir

1. Lee [classes](references/classes.md). Compara la frase de este turno con la escritura que está por ocurrir.

References: [classes](references/classes.md).

## Entrega

Este skill no escribe ningún archivo. Una escritura sigue solo cuando el mensaje de la persona en este turno contiene la frase exacta para ese único destino. No inventes la frase. No reutilices una frase de un turno anterior.

## Done

- [ ] Solo se aplicó la referencia de este command.
- [ ] La carpeta de salida, la subcarpeta del asunto, `ORIGIN.json` y `STATUS.md` coinciden con las reglas de entrega.
- [ ] Un dato obligatorio que falta es un hueco. El archivo sigue `proposed`.

## Example

Un pedido que nombra la pieza y su fuente escribe un archivo. Un pedido sin esa fuente no escribe nada y nombra el hueco.
