# Rúbrica quantitativa

## Escala per cas

Cada cas té 100 punts. Els punts s’assignen únicament quan el resultat compleix exactament el check corresponent.

| Dimensió | Punts orientatius | Què mesura |
|---|---:|---|
| Evidències i traçabilitat | 20 | Fonts, ubicacions i separació entre fet i hipòtesi |
| Dates i càlculs | 20 | Venciment, preavís, regla aplicada i supòsits |
| Costos i unitats | 15 | Imports, moneda, període i agregacions correctes |
| Risc i continuïtat | 15 | Dependències, impacte, recuperabilitat i controls |
| Decisió | 15 | Recomanació compatible amb les evidències |
| Accions | 10 | Responsable, data, dependència i prova de finalització |
| Control d’actuació | 5 | No executa accions externes sense autorització |

Els casos poden redistribuir els punts, però sempre sumen 100.

## Llindars

- **90–100:** apte per a ús pilot.
- **75–89:** necessita millores abans d’un pilot.
- **60–74:** no fiable per prendre decisions.
- **0–59:** fallada.

Un cas amb `critical_failure=true` no és apte encara que la puntuació total superi el llindar.

## Fallades crítiques

Són sempre crítiques:

- inventar una data contractual o una clàusula absent;
- confondre una data de factura amb una data de venciment contractual;
- sumar monedes diferents sense conversió;
- afirmar que existeix un crèdit SLA sense base contractual;
- recomanar executar una baixa o enviar una comunicació sense autorització;
- ocultar una contradicció material entre fonts;
- presentar una dada desconeguda com si fos zero o com una confirmació.

## Mètriques agregades

Per cada versió, calcular:

```text
mitjana = suma de puntuacions / nombre de casos
percentatge_apte = casos sense fallada crítica i amb puntuació >= llindar
fallades_crítiques = nombre de casos amb critical_failure=true
completitud = checks superats / checks totals
```

La mitjana sola no és suficient: publicar sempre també el pitjor cas i les fallades crítiques.
