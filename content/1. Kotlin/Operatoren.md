# Rechen- und Zuweisungsoperatoren

## 🔹 Rechenoperatoren
- Werden verwendet, um mathematische Operationen durchzuführen.
- Unterstützte Operatoren:
  - `+`  Addition
  - `-`  Subtraktion
  - `*`  Multiplikation
  - `/`  Division
  - `%`  Modulo (Restwert)

> [!example] Beispiel: Rechenoperatoren
> ```kotlin
> val a = 10
> val b = 3
> println(a + b) // 13
> println(a - b) // 7
> println(a * b) // 30
> println(a / b) // 3
> println(a % b) // 1
> ```

## 🔹 Zuweisungsoperatoren
- Kombinieren Rechenoperationen mit einer Variablenzuweisung.
- Kurzschreibweisen:
  - `+=`  Addition und Zuweisung
  - `-=`  Subtraktion und Zuweisung
  - `*=`  Multiplikation und Zuweisung
  - `/=`  Division und Zuweisung
  - `%=`  Modulo und Zuweisung

> [!example] Beispiel: Zuweisungsoperatoren
> ```kotlin
> var x = 5
> x += 3  // x = 8
> x -= 2  // x = 6
> x *= 4  // x = 24
> x /= 6  // x = 4
> x %= 3  // x = 1
> ```

## 🔹 Inkrementierung & Dekrementierung
- **`++`** erhöht eine Variable um 1 (Inkrementierung).
- **`--`** verringert eine Variable um 1 (Dekrementierung).
- Gibt es in zwei Varianten:
  - **Präfix** (`++x`, `--x`) → Wert wird **sofort verändert**.
  - **Postfix** (`x++`, `x--`) → aktueller Wert wird **zuerst verwendet**, dann verändert.

> [!example] Beispiel: Inkrementierung & Dekrementierung
> ```kotlin
> var i = 5
> println(++i) // 6 (Präfix: zuerst +1, dann ausgeben)
> println(i++) // 6 (Postfix: zuerst ausgeben, dann +1)
> println(i)   // 7
>
> var j = 3
> println(--j) // 2 (Präfix)
> println(j--) // 2 (Postfix)
> println(j)   // 1
> ```

## 🔹 Besonderheiten
- Division mit Ganzzahlen (`Int`, `Long`) liefert ein ganzzahliges Ergebnis.
- Für genauere Ergebnisse Gleitkommazahlen (`Double`, `Float`) verwenden.

> [!example] Beispiel: Ganzzahl- vs. Gleitkommadivision
> ```kotlin
> val intResult = 7 / 2        // 3
> val doubleResult = 7.0 / 2   // 3.5
> ```

## 🔹 Siehe auch
- [[Kontrollstrukturen in Kotlin]]
- [[Datentypen]]
