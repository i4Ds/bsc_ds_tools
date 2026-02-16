# Python Kurzreferenz - Einstieg Data Science & AI

### 1. Grundrechnungen & Zuweisung

Rechnen in Python (als Taschenrechner):

```python
12 + 3   # Addition
12 - 3   # Subtraktion
12 * 3   # Multiplikation
12 / 3   # Division (gibt float zurück)
12 // 3  # Ganzzahldivision
```

Zuweisung an Variablen:

```python
number_1 = 100
number_2 = 50
number_1 * number_2
```

- `=` weist den Wert rechts der Variable links zu
- Variablennamen ohne Leerzeichen, z.B. `anzahl_passagiere`, `mean_age`

### 2. Text (Strings)

Text ausgeben & speichern:

```python
print("Willkommen im Studiengang Data Science & AI")
text = "Willkommen im Studiengang Data Science & AI"
print(text)
```

Funktionen auf Text anwenden:

```python
text.lower()   # alles klein
text.upper()   # alles GROSS
```

### 3. Funktionen

Eigene Funktion definieren & aufrufen:

```python
def add_numbers(a, b):
    return a + b

add_numbers(10, 12)
```

Allgemeines Muster:

```python
def name_der_funktion(arg1, arg2):
    # Python-Code
    return ergebnis
```

### 4. Bedingungen (if / else)

```python
number_3 = 40   # diese Variable kann verändert werden

if number_3 == 40:
    print("Die Zahl beträgt 40")
else:
    print("Die Zahl beträgt nicht 40")
```

- `==` Gleichheit, `!=` Ungleichheit
- `<`, `>`, `<=`, `>=` Vergleichsoperatoren
- `and`, `or`, `not` für logische Verknüpfungen

### 5. Vektoren mit NumPy

```python
import numpy as np

arr = np.array([1, 2, 3, 4])                 # numerisches Array
arr[0]                                       # erstes Element
arr + np.array([10, 20, 30, 40])             # elementweise Addition
vector = np.array(["A", "B"])
np.char.lower(vector)                        # Zeichenketten-Array
```

### 6. Packages / Libraries

```python
# uv add pandas seaborn
import pandas as pd
import seaborn as sns
```

- `uv add paketname` installiert ein Package
- `import paketname` macht das Package in deinem Skript nutzbar
