# Algorithm-Challenge-1

Challenge 1
## 1. ¿Cual es la complejidad de tiempo de la función example()?

```c++
int example(int n)
{
  int count = 0;
  for (int i = n; i > 0; i /= 2) // O(log(N)
     for (int j = 0; j < i; j++) // O(N)
        count += 1;
  return count;
}
```
Por lo tanto la complejidad del algoritmos pertenece a O(N*log(N)).

## 2. ¿Cual es la complejidad de tiempo de la función example2()?

```c++
void example2(int n, int arr[])
{
    int i = 0, j = 0;
    for(; i < n; ++i) // O(N)
        while(j < n && arr[i] < arr[j]) // O(N) Cuando arr[] esta ordenado ascendentemente
            j++;
}
```
Complejidad en el mejor caso pertenece a Ω(N), en el peor caso pertenece a O(N^2).

## 3. ¿Cuál es la mejor complejidad de tiempo de bubbleSort?
```c++
void bubbleSort(int n, int arr[])
{
   for (int i = 1; i < n; i++)        
       for (int j = 0; j < n - i; j++) 
           if (arr[j] > arr[j + 1])
              swap(&arr[j], &arr[j + 1]); // swap: intercambiar elementos usando punteros
}
```
La complejidad de bubbleSort pertenece a Θ(N^2) es igual en el mejor y peor caso.
