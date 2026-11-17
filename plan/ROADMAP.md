# Pla de producte: RogexAI Vendor Management

## Objectiu

Convertir la skill en un sistema fiable de control de renovacions i risc de proveïdors, capaç de detectar terminis, costos i dependències i de preparar decisions auditables.

La proposta de valor és:

> Evitar perdre terminis de cancel·lació, detectar costos ocults i preparar decisions de renovació amb evidències verificables.

La skill no s’ha de posicionar com una IA que simplement resumeix proveïdors. El producte ha de reduir risc, temps i costos de decisió.

## Principis de producte

- Separar fets, interpretacions, càlculs, hipòtesis i recomanacions.
- No inventar dades, dates, imports, clàusules ni alternatives.
- Conservar la font i la ubicació de cada afirmació material.
- Mostrar desconeguts, contradiccions i supòsits.
- Bloquejar conclusions quan falti una dada crítica.
- Fer que cada recomanació es converteixi en una acció amb responsable i data.
- Requerir autorització humana abans d’actuar sobre sistemes o tercers.

## Fases prioritzades

### Fase 1 — MVP fiable

**Objectiu:** obtenir revisions consistents i verificables a partir de documents proporcionats per l’usuari.

**Capacitats:**

- model de dades únic per proveïdors, contractes, costos i accions;
- càrrega de contractes, annexos, factures i registres;
- extracció de clàusules, imports, dates, obligacions i dependències;
- cites amb document, pàgina, clàusula, fila, data i limitacions;
- càlcul de venciments i preavisos;
- llista prioritzada d’accions;
- exportació a Markdown, CSV o Excel;
- casos de prova amb documents anonimitzats.

**Criteris d’acceptació:**

- cap conclusió material sense una font o una marca explícita de desconeguda;
- cap data calculada sense regla i supòsits visibles;
- les monedes i periodicitat es conserven sense agregacions incorrectes;
- les contradiccions entre fonts apareixen a la sortida;
- una persona pot revisar i reproduir la decisió a partir de les evidències.

### Fase 2 — Producte operatiu

**Objectiu:** passar d’una revisió puntual a un sistema de seguiment continu.

**Capacitats:**

- calendari de renovacions i alertes;
- detecció de contradiccions entre versions contractuals;
- normalització de costos i períodes;
- risc explicable per impacte, recuperabilitat i controls;
- flux d’aprovació;
- historial de canvis i decisions;
- esborranys de comunicacions i reclamacions pendents d’autorització;
- informes executius i cartera ordenada per urgència.

**Criteris d’acceptació:**

- cap preavís crític depèn d’un informe manual;
- cada alerta mostra origen, data límit i acció esperada;
- qualsevol canvi de dada o decisió queda registrat;
- el risc es pot explicar amb evidències, no només amb una puntuació.

### Fase 3 — Producte defensible

**Objectiu:** crear valor recurrent i una barrera competitiva.

**Capacitats:**

- integracions amb Drive, SharePoint, correu, comptabilitat o gestió contractual;
- permisos per empresa, equip i cartera;
- polítiques internes configurables;
- benchmarks propis;
- detecció anticipada de risc de renovació;
- informes per direcció i auditoria;
- separació estricta de dades entre clients;
- versions, exemples, condicions d’ús i suport.

**Criteris d’acceptació:**

- les integracions respecten permisos i deixen traça;
- les dades d’un client no poden aparèixer en una altra cartera;
- les regles internes són visibles, versionades i revisables;
- el client pot exportar les seves dades i evidències.

## Model de dades mínim

Cada proveïdor hauria d’incloure:

- proveïdor, servei i propietari intern;
- objectiu de negoci i dependències;
- contracte, annexos, versions i vigència;
- cost, moneda, impostos i periodicitat;
- inici, venciment, renovació automàtica i preavís;
- dades tractades i requisits de continuïtat;
- SLA, mètriques i incidents;
- costos de sortida i temps de migració;
- alternatives conegudes;
- risc, confiança i evidències;
- accions, responsables, dates i prova de finalització.

## Motor de càlcul

Els càlculs s’han de fer fora del model de llenguatge i han de ser reproduïbles:

- dates de venciment i preavís;
- dies restants i urgència;
- costos anuals i plurianuals;
- increments percentuals;
- costos de canvi i solapament;
- impacte de renovació automàtica.

Cada resultat ha de mostrar la regla aplicada, la data d’origen, els supòsits i les limitacions. Cal cobrir anys de traspàs, mesos irregulars, dates ambigües, zones horàries i clàusules incompletes.

## Format de decisió

La sortida principal ha de començar per una decisió i no per un resum:

```text
Recomanació:
Motiu principal:
Data límit coneguda:
Confiança:

Evidències:
Desconeguts o contradiccions:
Opcions:
Accions:
Risc si no s’actua:
```

Per a carteres:

| Prioritat | Proveïdor | Acció | Data límit | Responsable | Evidència pendent |
|---|---|---|---|---|---|

## Validació i mètriques

Abans d’escalar, mesurar:

- temps de preparació d’una revisió comparable;
- precisió de dates i càlculs;
- percentatge d’afirmacions amb font verificable;
- contradiccions detectades;
- falsos positius i falsos negatius de preavisos;
- accions completades abans del termini;
- estalvi potencial separat de l’estalvi confirmat;
- decisions canviades després de trobar una dada crítica.

Validar amb contractes anonimitzats i casos de:

- renovació automàtica;
- preavís imminent;
- costos variables;
- monedes diferents;
- dades incompletes;
- conflicte entre contracte i factura;
- servei fiable però sense exportació provada;
- mètrica SLA sota objectiu sense clàusula de crèdit.

## Model comercial

El valor de pagament no és el text de la skill, sinó:

- calendari viu de renovacions;
- detecció de riscos i costos ocults;
- repositori d’evidències;
- flux d’aprovació;
- historial i auditoria;
- integracions;
- configuració segons les polítiques del client.

Oferta inicial recomanada: servei assistit amb una cartera petita, abast tancat i una ronda de revisió. Mesurar el resultat abans d’oferir manteniment recurrent o un paquet autònom.
