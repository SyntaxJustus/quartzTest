
**Scope-Funktionen** bieten eine elegante Möglichkeit, Codeblöcke im Kontext eines Objekts auszuführen – ideal für Initialisierung, Transformation oder temporären Kontext.

## 🔹 Kotlin – Überblick  

- Wichtige Funktionen: `let`, `run`, `with`, `apply`, `also`.  
- Alle führen einen **Block im Kontext eines Objekts** aus.  
- Unterschied: **Rückgabewert** (`this` vs. `it`) und **Verwendungskontext** (Konfiguration, Verarbeitung, Logging etc.).
  

## 🔹 `let`  

- Verwendet `it` als Objektbezug.  
- Praktisch für **Null-Checks** und Transformationen.  
- Gibt das Ergebnis des Blocks zurück.

> [!example] Kotlin – let  
> ```kotlin
> val name: String? = "Lena"
> 
> name?.let {
>     println("Hallo, $it")
> }
> ```


## 🔹 `apply`  

- Verwendet `this` als Objektbezug.  
- Gut für **Objektkonfiguration** – gibt das Objekt selbst zurück.  

> [!example] Kotlin – apply  
> ```kotlin
>// Definition der User-Klasse
>data class User(val name: String, val email: String)
>
> val user = User().apply {
>     name = "Anna"
>     email = "anna@mail.com"
> }
> ```

  

## 🔹 `also`  

- Verwendet `it` als Objektbezug.  
- Nützlich für **Side Effects** wie Logging oder Debugging.  
- Gibt das Objekt zurück.

> [!example] Kotlin – also  
> ```kotlin
> val user = User("Tom").also {
>     println("Benutzer erstellt: $it")
> }
> ```


## 🔹 `run`  

- Verwendet `this` als Objektbezug.  
- Kombiniert Initialisierung + Rückgabewert.  
- Ideal für **Berechnungen oder letzten Aufruf in einer Kette**.

> [!example] Kotlin – run  
> ```kotlin
> val ergebnis = User("Lena").run {
>     "$name <$email>"
> }
> ```


## 🔹 `with`  

- Kein Extension-Funktion – Aufruf über `with(objekt)`.  
- Verwendet `this` und gibt **Block-Ergebnis** zurück.  
- Nützlich für **mehrere Operationen** auf einem Objekt.

> [!example] Kotlin – with  
> ```kotlin
> val info = with(User("Lena", "lena@mail.com")) {
>     "$name <$email>"
> }
> ```


## 🔹 Siehe auch

- [[Klassen]]
- [[Objekte]]
- [[Interfaces]]
- [[Delegates]]
