---
name: vendor-management-rogexai
description: Prepara revisions de proveïdors i decisions de renovació amb contractes, despesa i evidències de servei. Identifica preavisos, dependències i accions pendents abans de renovar o substituir serveis.
---

# RogexAI Vendor Management

Converteix informació dispersa de proveïdors en decisions traçables sobre renovació, continuïtat i substitució. Respon en l’idioma de l’usuari i adapta el nivell de detall a la decisió que necessita prendre.

## Quan utilitzar-la

Fes-la servir per:

- preparar una revisió d’un proveïdor o d’una cartera;
- identificar venciments, renovacions automàtiques i preavisos;
- comparar renovació, renegociació, investigació o substitució;
- convertir contractes, factures i registres de servei en accions verificables.

## Entrades i abast

1. Identifica la decisió, la data de revisió i el responsable.
2. Accepta documents parcials i pregunta només per dades que bloquegin una conclusió material.
3. Adapta els camps al cas; no exigeixis un catàleg complet per revisar un sol proveïdor.
4. Extreu la informació amb el model de [references/review.md](references/review.md).

## Flux de treball

### 1. Construir la base factual

- Registra fets, fonts localitzables, declaracions del proveïdor, hipòtesis i desconeguts per separat.
- Conserva les discrepàncies entre fonts; no les resolguis amb una suposició.
- Assigna identificadors a les evidències (`E1`, `E2`...) i indica document o URL, pàgina/clàusula/fila, data o període i limitacions.

### 2. Determinar les dates contractuals

- Comprova venciment, renovació automàtica i termini de preavís abans de valorar opcions.
- Calcula dates només quan la clàusula defineixi prou bé el còmput i mostra els supòsits.
- Si falta una dada contractual, deixa la data desconeguda i indica què cal verificar.

### 3. Analitzar el proveïdor

Avalua per separat:

- **Valor obtingut:** adequació al negoci i cost conegut.
- **Qualitat del servei:** mètriques, incidents i compliment verificable.
- **Exposició del negoci:** impacte, recuperabilitat, controls i dependències.

No els fusionis en una puntuació única que pugui amagar una dependència crítica.

### 4. Comparar opcions

Compara, quan siguin aplicables:

- renovar;
- renovar amb condicions;
- investigar abans de decidir;
- preparar una substitució.

Per a cada opció, inclou costos coneguts, costos de canvi, dependències, temps de migració, continuïtat i incerteses. No inventis alternatives comercials ni preus.

### 5. Formular la decisió

Entrega una recomanació amb:

- el principal motiu i les evidències que la sostenen;
- la confiança i la seva justificació;
- les accions prioritzades;
- la dada que podria fer canviar la decisió.

## Regles d’interpretació

- Una dada absent és desconeguda, no zero. Cap incident registrat no prova que no n’hi hagi hagut.
- Mantén identificats import, moneda, impostos i periodicitat. No sumis monedes diferents sense conversió amb font i data.
- Diferencia estalvi recurrent, costos de canvi i estimacions encara no realitzades.
- Compara mètriques amb el sentit correcte: disponibilitat mínima i temps màxim de resposta exigeixen comparacions diferents. No barregis períodes incompatibles.
- Un incompliment no confirma un crèdit SLA: comprova contracte, exclusions, fórmula, evidències i termini. Sense aquestes dades, informa d’una possible reclamació pendent de verificació.
- Les certificacions només aporten evidència dins del seu abast i vigència. No acrediten automàticament compliment normatiu.
- Una dependència crítica pot tenir un bon servei i un risc de continuïtat elevat. Abans de substituir-la, comprova exportació de dades, alternativa operativa, accessos, retenció i recuperació.

## Format de sortida

Obre amb la recomanació, el principal motiu i la data límit coneguda. Inclou només:

- evidències i mancances que afecten la decisió;
- opcions viables amb costos coneguts, condicions i incerteses;
- accions amb responsable o «pendent d’assignar», data o «pendent d’acordar», dependències i prova de finalització;
- confiança **alta**, **mitjana** o **baixa**, amb justificació.

Per a una cartera, presenta una taula ordenada per urgència i exposició i conserva els desconeguts. No omplis un nombre fix de recomanacions si no hi ha evidència suficient.

## Límits d’actuació

Preparar una revisió no autoritza:

- enviar missatges;
- presentar reclamacions;
- executar baixes;
- modificar sistemes externs.

Aquestes accions requereixen autorització explícita de l’usuari per a l’acció concreta.
