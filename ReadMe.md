# Clases de equivalencies:

Avatar: {1 - 4}.

Nivell Maldat: {1000 - 50000}.

Longitud del Nom: {2 - 25}.

Simbols del Nom: {Abecedari}.

Vocals: {a,e,i,o,u}.

# Valors limits:

Avatar: {0, 5}.

Nivell Maldat: {999, 50001}.

Longitud del Nom: {1, 26}.

Simbols del Nom: {@, _, /, \, |}.

# Casos de Proba:

## Rang Avatar:
Entrada 0:
Resultat Esperat: ERROR Repeteix.

Entrada 1:
Resultat Esperat: Bien Segueix.

Entrada 5:
Resultat Esperat: ERROR Repeteix.

## Rang Nivell Maldat:
Entrada 999:
Resultat Esperat: ERROR Repeteix.

Entrada 2000:
Resultat Esperat: Bien Segueix.

Entrada 60000:
Resultat Esperat: ERROR Repeteix.

## Rang Longitud del Nom:

Entrada 1:
Resultat Esperat: ERROR Repeteix.

Entrada Alberto (7 caracteres):
Resultat Esperat: Bien Segueix.

Entrada HolaQueTalComoEstasYoBienYTu (28 caracteres):
Resultat Esperat: ERROR Repeteix.

## Rang Simbols del Nom:

Entrada Alberto@:
Resultat Esperat: ERROR Repeteix.

Entrada Alberto:
Resultat Esperat: Bien Segueix.

## Vocals

Entrada Alberto:
Resultat Esperat: Bien Segueix.
Vocals: 3

Entrada jkhrsx:
Resultat Esperat: Bien Segueix.
Vocals: 0
