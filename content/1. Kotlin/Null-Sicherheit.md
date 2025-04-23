# Null-Sicherheit

## 🔹 Hintergrund
- Kotlin wurde entwickelt, um das klassische **NullPointerException-Problem** zu vermeiden.
- **Jede Variable ist standardmäßig nicht-nullbar**, außer man erlaubt explizit `null`.

## 🔹 Nullable-Typen
- Mit `?` am Typ kann eine Variable `null` sein.
- Beispiel: `String?` ist ein **nullable String**.

> [!example] Beispiel: Nullable vs. Non-Nullable
> ```kotlin
> var name: String = "Anna"
> var optionalName: String? = null
> ```

## 🔹 Zugriff auf Nullable-Werte
### 1. **Sicherer Zugriff mit `?.`**
- Führt Methode/Operation **nur aus, wenn nicht null**.

> [!example] Beispiel: Sichere Methode mit `?.`
> ```kotlin
> val text: String? = "Hallo"
> println(text?.length)  // Gibt Länge oder null zurück
> ```

### 2. **Elvis-Operator `?:`**
- Gibt einen **Standardwert zurück**, wenn die Variable null ist.

> [!example] Beispiel: Elvis-Operator
> ```kotlin
> val name: String? = null
> val displayName = name ?: "Unbekannt"
> println(displayName)  // "Unbekannt"
> ```

### 3. **Nicht-null Assertion `!!`**
- Erzwingt Zugriff → löst **Fehler aus, wenn null**.
- **Vorsicht!** Nur verwenden, wenn man sich 100 % sicher ist.

> [!example] Beispiel: Nicht-null Assertion
> ```kotlin
> val text: String? = null
> println(text!!.length) // → Exception: NullPointerException
> ```

## 🔹 Null-Prüfung mit `if`
- Gängige Möglichkeit, Nullable-Typen abzusichern.

> [!example] Beispiel: Manuelle Null-Prüfung
> ```kotlin
> fun printText(text: String?) {
>     if (text != null) {
>         println(text.uppercase())
>     }
> }
> ```

## 🔹 Safe Cast mit `as?`
- Gibt bei fehlgeschlagenem Cast `null` zurück, anstatt eine Exception zu werfen.

> [!example] Beispiel: Safe Cast
> ```kotlin
> val value: Any = 123
> val text: String? = value as? String  // null
> ```

## 🔹 Best Practices
- Nullable-Typen **nur verwenden, wenn nötig**.
- Möglichst früh prüfen, ob Werte null sein können.
- **Elvis-Operator** bevorzugen statt `!!`.

## 🔹 Siehe auch
- [[Kotlin Grundlagen]]
- [[Datentypen]]
- [[Typecasts]]
