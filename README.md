# Arreglos-y-Algoritmos-en-Java-semana-1

Parte 1: Ingeniería inversa del JAR

¿Qué clases existen?                                                                                                                                                                                                  
R// Las clases que veo en este archivo son la de bubblesort, MegeSortDemo, Quicksort y SumArray.

¿Qué operaciones se realizan sobre los arreglos?                                                                                                                                                                                                                                    

R// Las operaciones que veo son las acumulaciones y que suma esta misma, tambien vi la de swaps que son lo intercambios en  la de mergesort veo la de copyofrange y que este ayuda al poder partir en dos el array para poder hacer este mecanismo de comparacion.

¿Qué algoritmos de ordenamiento se utilizan?


R// Los algoritmos que veo y que me toco investigar es el de la burbuja que es la clase de bubblesort el de merge sort, quicksort y el uso de los arrays sort que por lo que investigue sirve para poder ordenar automaticamente los elementos de un array que generalmente es ascendente.

PARTE DE LA EVIDENCIA 

Fragmentos relevantes del código decompilado:

public void mergeSort(int[] a) {
    if (a.length <= 1)
      return; 
    int mid = a.length / 2;
    int[] left = Arrays.copyOfRange(a, 0, mid);
    int[] right = Arrays.copyOfRange(a, mid, a.length);
    mergeSort(left);
    mergeSort(right);
    merge(a, left, right);
  } //ESTA ME PARECIO RELEVANTE YA QUE NUNCA LO HABIA VISTO ESO DE PARTIR EN 2 UN ARREGLO 

  
  
