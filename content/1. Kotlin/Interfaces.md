
## 🔹 Überblick

- **Interfaces** in Kotlin sind eine Sammlung von abstrakten Methodensignaturen, die von einer Klasse implementiert werden können.
- **Interfaces** können keine Implementierungen für ihre Methoden bieten, aber sie können standardmäßige Implementierungen für einige Methoden bereitstellen.
- Eine Klasse kann mehrere Interfaces implementieren.

## 🔹 Definition von Interfaces

- Ein **Interface** wird mit dem Schlüsselwort **`interface`** definiert.
- **Methoden** in einem Interface müssen keine Implementierung haben.
- Implementiert eine Klasse ein Interface, müssen alle Methoden aus diesem eine Implementierung haben

> [!example] Beispiel: Ein einfaches Interface  
> ```kotlin
> interface Fahrer {
>     fun fahren()  // Methode ohne Implementierung
> }
> 
> class Auto : Fahrer {
>     override fun fahren() {
>         println("Auto fährt")
>     }
> }
> 
> val auto = Auto()
> auto.fahren()  // Ausgabe: Auto fährt
> ```

## 🔹 Mehrere Interfaces implementieren

- Eine Klasse kann mehrere Interfaces implementieren und muss alle Methoden dieser Interfaces implementieren.

> [!example] Beispiel: Mehrere Interfaces  
> ```kotlin
> interface Fahrer {
>     fun fahren()
> }
> 
> interface Reparierbar {
>     fun reparieren()
> }
> 
> class Auto : Fahrer, Reparierbar {
>     override fun fahren() {
>         println("Auto fährt")
>     }
> 
>     override fun reparieren() {
>         println("Auto wird repariert")
>     }
> }
> 
> val auto = Auto()
> auto.fahren()  // Ausgabe: Auto fährt
> auto.reparieren()  // Ausgabe: Auto wird repariert
> ```

## 🔹 Standardmethoden in Interfaces

- In Kotlin können Interfaces auch **Standardmethoden** haben, die eine Implementierung bereitstellen. Dies ermöglicht es, bestimmte Methoden zu verwenden, ohne sie in der implementierenden Klasse überschreiben zu müssen.

> [!example] Beispiel: Standardmethoden in Interfaces  
> ```kotlin
> interface Fahrer {
>     fun fahren() {
>         println("Standardfahren")
>     }
> }
> 
> class Auto : Fahrer {
>     override fun fahren() {
>         super.fahren()  // Aufruf der Standardimplementierung
>         println("Auto fährt schnell")
>     }
> }
> 
> val auto = Auto()
> auto.fahren()  // Ausgabe: Standardfahren
>                               // Ausgabe: Auto fährt schnell
> ```

## 🔹 Siehe auch

- [[Kotlin Grundlagen]]
- [[Klassen]]
- [[Vererbung]]
- [[Methoden]]
