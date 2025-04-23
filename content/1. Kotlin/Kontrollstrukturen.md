# Kontrollstrukturen in Kotlin

## 🔹 if / else
- Verwendet zur bedingten Ausführung von Code.
- `if` ist ein Ausdruck – gibt also einen Wert zurück.

> [!example] Beispiel: if / else
> ```kotlin
> val a = 10
> val b = 20
> val max = if (a > b) a else b
> println("Größere Zahl: $max")
> ```

## 🔹 when
- Kotlin-Alternative zum klassischen `switch`.
- Sehr flexibel: Werte, Bereiche, Bedingungen möglich.

> [!example] Beispiel: when-Ausdruck
> ```kotlin
> val note = 1
> val bewertung = when (note) {
>     1 -> "Sehr gut"
>     2 -> "Gut"
>     3 -> "Befriedigend"
>     4 -> "Ausreichend"
>     5, 6 -> "Nicht bestanden"
>     else -> "Ungültig"
> }
> println(bewertung)
> ```

## 🔹 while-Schleife
- Führt Code aus, solange eine Bedingung wahr ist.

> [!example] Beispiel: while-Schleife
> ```kotlin
> var count = 0
> while (count < 5) {
>     println("Wert: $count")
>     count++
> }
> ```

## 🔹 do-while-Schleife
- Führt Code **mindestens einmal** aus, bevor die Bedingung geprüft wird.

> [!example] Beispiel: do-while-Schleife
> ```kotlin
> var x = 0
> do {
>     println("x ist $x")
>     x++
> } while (x < 3)
> ```

## 🔹 for-Schleife
- Wird für Iteration über Bereiche, Arrays oder Listen verwendet.

> [!example] Beispiel: for-Schleife mit Range
> ```kotlin
> for (i in 1..5) {
>     println("i = $i")
> }
> ```

> [!example] Beispiel: for-Schleife über Liste
> ```kotlin
> val namen = listOf("Anna", "Ben", "Clara")
> for (name in namen) {
>     println(name)
> }
> ```

## 🔹 break und continue
- `break` → bricht die Schleife komplett ab.
- `continue` → überspringt die aktuelle Iteration.

> [!example] Beispiel: break und continue
> ```kotlin
> for (i in 1..5) {
>     if (i == 3) continue  // überspringt 3
>     if (i == 5) break     // bricht bei 5 ab
>     println(i)
> }
> ```

## 🔹 Siehe auch
- [[Operatoren]]
- [[Funktionen ]]
