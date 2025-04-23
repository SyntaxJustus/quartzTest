

## 🔹 Was ist Typecasting?

- Typecasting bedeutet, einen Wert **explizit in einen anderen Typ zu überführen**.
- Wird verwendet, wenn der **kompilierte Typ** allgemeiner ist als der tatsächliche Typ zur Laufzeit.

## 🔹 Smart Casts

- Kotlin nutzt **Smart Casts**, um Typen automatisch zu erkennen **nach einer Prüfung mit `is`**.
- Kein explizites Casting notwendig.

> [!example] Beispiel: Smart Cast mit `is`
> ```kotlin
> fun printLength(obj: Any) {
>     if (obj is String) {
>         println(obj.length) // Smart Cast zu String
>     }
> }
> ```

## 🔹 Unsicheres Casten (`as`)

- Mit `as` wird ein Wert **explizit gecastet**.
- Wenn der Cast **fehlschlägt**, wirft Kotlin eine `ClassCastException`.

> [!example] Beispiel: Unsicheres Casting mit `as`
> ```kotlin
> val obj: Any = "Hallo"
> val text: String = obj as String
> println(text.length)
> ```

## 🔹 Sicheres Casten (`as?`)

- Gibt `null` zurück, wenn der Cast nicht möglich ist → **verhindert Ausnahmefehler**.
- Nützlich bei optionalem oder unsicherem Typ.

> [!example] Beispiel: Sicheres Casting mit `as?`
> ```kotlin
> val obj: Any = 42
> val text: String? = obj as? String  // null, kein Fehler
> println(text) // null
> ```

## 🔹 is & !is Operatoren

- `is` prüft, ob ein Objekt einem Typ entspricht.
- `!is` prüft das Gegenteil.

> [!example] Beispiel: Typprüfung mit `is` und `!is`
> ```kotlin
> fun checkType(value: Any) {
>     if (value is Int) {
>         println("Es ist eine Zahl: $value")
>     } else if (value !is String) {
>         println("Weder Zahl noch String.")
>     }
> }
> ```

## 🔹 Best Practices

- **Smart Casts bevorzugen** – sicherer und idiomatischer.
- Unsichere Casts nur verwenden, wenn absolut notwendig.
- Bei komplexeren Objekthierarchien mit Vererbung: auf **Nullprüfungen und Typprüfungen achten**.

## 🔹 Siehe auch

- [[Datentypen]]
- [[Null-Sicherheit]]
- [[Typkonvertierung]]
- [[Kotlin Grundlagen]]
