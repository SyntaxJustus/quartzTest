## 🔹 Coroutines

- Coroutines sind eine **einfache Möglichkeit zur nebenläufigen Programmierung** in Kotlin.  
- Sie ermöglichen **asynchrone**, **nicht-blockierende** Operationen mit einfacher Syntax.  
- Basieren auf dem Konzept von **suspendierenden Funktionen**.

---

## 🔹 Grundlagen  

- Coroutine-Funktionen werden mit `suspend` gekennzeichnet.  
- Sie können nur von anderen `suspend`-Funktionen oder innerhalb eines Coroutines-Scopes aufgerufen werden.

> [!example] Beispiel: suspend-Funktion  
> ```kotlin
> suspend fun ladeDaten() {
>     delay(1000)  // Simuliert eine nicht-blockierende Verzögerung
>     println("Daten geladen")
> }
> ```

---

## 🔹 Coroutine starten  

- Coroutines werden typischerweise mit einem Scope gestartet, z. B. `runBlocking`, `GlobalScope`, oder einem benutzerdefinierten `CoroutineScope`.

> [!example] Beispiel: Coroutine mit runBlocking  
> ```kotlin
> import kotlinx.coroutines.*
>
> fun main() = runBlocking {
>     launch {
>         delay(500)
>         println("Hallo aus der Coroutine")
>     }
>     println("Programm startet")
> }
> ```

---

## 🔹 launch vs async  

- `launch` → startet eine Coroutine, die keinen Rückgabewert hat (ähnlich wie `void`).  
- `async` → startet eine Coroutine, die ein Ergebnis liefert (ähnlich wie `Future`).

> [!example] Beispiel: async mit Ergebnis  
> ```kotlin
> val result = async {
>     delay(1000)
>     42
> }
> println("Ergebnis: ${result.await()}")
> ```

---

## 🔹 delay vs Thread.sleep  

- `delay()` ist **nicht-blockierend** (suspendierend).  
- `Thread.sleep()` ist **blockierend** – sollte in Coroutines vermieden werden.

---

## 🔹 Strukturierte Nebenläufigkeit  

- Coroutines werden automatisch **abgebrochen**, wenn ihr übergeordneter Scope endet.  
- Verhindert **Memory Leaks** und unkontrollierte Hintergrundprozesse.

---

## 🔹 Siehe auch  

- [[Funktionen]]
