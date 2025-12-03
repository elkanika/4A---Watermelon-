# 4A - Watermelon

## 📋 Información del Problema
- **Plataforma:** Codeforces
- **ID:** 4A
- **Nombre:** Watermelon
- **Lenguaje:** Ruby
- **Dificultad:** 800 (Principiante)
- **Link al problema:** [Codeforces 4A](https://codeforces.com/problemset/problem/4/A)

## 📝 Descripción
Pete y Billy quieren dividir una sandía de peso $w$ en dos partes, de tal manera que **ambas partes pesen un número par de kilos**. No es necesario que las partes sean iguales. El programa debe determinar si esta división es posible.

## 💡 Lógica de la Solución
Para resolver este problema, analicé las propiedades de los números pares:
1.  **Paridad:** La suma de dos números pares siempre da un número par. Por lo tanto, el peso total $w$ debe ser par (`w % 2 == 0`).
2.  **Caso Borde (Edge Case):** El número **2**. Aunque es par, la única forma de dividirlo en enteros positivos es $1 + 1$. Como 1 es impar, el número 2 no cumple la condición.

**Conclusión:**
La respuesta es `YES` solo si el número es par **Y** estrictamente mayor que 2. De lo contrario, es `NO`.

## 💻 Código (Ruby)

```ruby
w = gets.to_i

if w % 2 == 0 && w > 2
  puts "YES"
else
  puts "NO"
end
