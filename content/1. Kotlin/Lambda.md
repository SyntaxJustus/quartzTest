
## 🔹 Überblick
- **Lambdas** sind anonyme Funktionen, die direkt im Code definiert werden können.
- Sie ermöglichen eine elegante und prägnante Art der Funktionsdefinition und -verwendung.
- **Higher-Order Functions** sind Funktionen, die entweder **Funktionen als Parameter** akzeptieren oder **Funktionen zurückgeben**.

## 🔹 Lambda-Ausdrücke
- Ein **Lambda-Ausdruck** ist eine Funktion ohne Namen, die als Wert behandelt wird.
- Sie haben eine kompakte Syntax und können an andere Funktionen übergeben werden.

> [!example] Beispiel: Einfache Lambda-Funktion  
> ```kotlin
> val addiere: (Int, Int) -> Int = { a, b -> a + b }
> println(addiere(2, 3))  // Ausgabe: 5
> ```

- Syntax eines Lambda-Ausdrucks:
  ```kotlin
  {parameter1: Typ1, parameter2: Typ2 -> Rückgabetyp}
  ```

## 🔹 Funktionsaufruf mit Lambda

- Lambdas werden an Funktionen übergeben, die Funktionen als Parameter akzeptieren.

> [!example] Beispiel: Lambda als Parameter
> ```kotlin
> fun berechne(a: Int, b: Int, operation: (Int, Int) -> Int): Int {
>      return operation(a, b) 
>      }
 >val result = berechne(5, 3, { x, y -> x + y }) println(result)  // Ausgabe: 8
 >```

## 🔹 Funktionsreferenzen

- Anstatt einen Lambda-Ausdruck zu schreiben, können auch **Funktionsreferenzen** verwendet werden, um eine bestehende Funktion zu übergeben.
  
> [!example] Beispiel: Funktionsreferenz
> 
> ```kotlin
> fun addiere(a: Int, b: Int): Int {
>      return a + b
>    }
>   val result = berechne(5, 3, ::addiere) println(result)  // Ausgabe: 8
>   ```

## 🔹 Higher-Order Functions

- **Higher-Order Functions** sind Funktionen, die entweder eine **Funktion als Parameter** akzeptieren oder **eine Funktion zurückgeben**.
    
- Sie ermöglichen es, Funktionen flexibler und wiederverwendbarer zu gestalten.
    
