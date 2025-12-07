# Conflictes en Git

## Entorn de treball

Per fer aquest exercici el recomanat és treballar amb una màquina Debian o Ubuntu, però serveix qualsevol entorn on pugueu executar `git`.

Els conflictes de versions es donen quan dos desenvolupadors han modificat la mateixa línia (o línies) de codi.

Forçarem un conflicte senzill que Git detectarà, provocat per dos desenvolupadors treballant en branques diferents.

---

## Exemple amb una sola màquina

En aquest exemple es fa tot a la mateixa màquina i directori per forçar un conflicte.  
La situació real seria que dos desenvolupadors treballarien en màquines diferents, i el conflicte arribaria quan incorporessin els canvis de l'altre mitjançant un *fetch*.

Suposarem dos desenvolupadors que treballen sobre el codi de l'arxiu `cercle.py`, que és un programa molt senzill en Python per calcular el perímetre d'una circumferència:

```python
#!/usr/bin/env python3

# Arxiu cercle.py : càlcul perímetre d'una circumferència

radi = input("Radi de la circumferència? ")
PI = 3.14
perimetre = 2 * PI * float(radi)
print("El perímetre de la circumferència de radi {} és {}".format(radi, perimetre))
