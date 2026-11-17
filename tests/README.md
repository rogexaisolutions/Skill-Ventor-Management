# Suite de proves de Vendor Management

Aquesta suite mesura si la skill produeix decisions correctes, traçables i accionables. Els casos són sintètics, però representen situacions habituals de gestió de proveïdors.

## Fitxers

- `cases.json`: casos d’entrada, resultat esperat i punts de cada comprovació.
- `results.csv`: registre append-only de cada execució.
- `rubric.md`: rúbrica comuna i regles de puntuació.

## Procediment d’execució

1. Selecciona un cas de `cases.json`.
2. Dona a la skill únicament el contingut d’`input`.
3. Desa la resposta completa amb l’identificador de la prova.
4. Comprova cada assertion de `checks` com a `pass` o `fail`.
5. Suma els punts dels checks superats i registra el resultat a `results.csv`.
6. Marca `critical_failure=true` si falla qualsevol check crític.
7. Compara la puntuació amb l’última versió de la skill i amb el llindar del cas.

No s’han d’atorgar punts per una resposta que només soni plausible. Cada punt requereix una evidència observable a la resposta.

## Criteri de progrés

Una versió només es considera millor si:

- augmenta la puntuació mitjana sense reduir cap cas crític per sota del seu llindar;
- no introdueix cap fallada crítica nova;
- manté o millora la traçabilitat de les fonts;
- conserva els desconeguts en lloc d’omplir-los amb suposicions.
