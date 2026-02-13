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

   private int partition(int[] arr, int low, int high) {
    int pivot = arr[high];
    int i = low - 1;
    for (int j = low; j < high; j++) {
      if (arr[j] <= pivot) {
        i++;
        int k = arr[i];
        arr[i] = arr[j];
        arr[j] = k;
      } 
    } 
    int temp = arr[i + 1];
    arr[i + 1] = arr[high];
    arr[high] = temp;
    return i + 1;
  }
}
//ESTE IGUAL AUNQUE LA SINTAXIS DE ESTA SI AUN NO LA ENTIENDO MUCHO EN EL SENTIDO DE QUE SE QUE HACE PERO NO LO PODRIA HACERlLO POR MI CUENTA AUN YA QUE ESTE UTILIZA  EL UJLTIMO ELEMMETO COMOO PIVOTE Y REORDENA EL ARREGLO PARA LOS MENORES O = A LA IZQUIERA Y LOS AMYORES A LA DERECHA.


*ENTREGA DEL EJERCICIO*
1. *ALGORITMO EN PSEUDOCODIGO *

    Entrada: arreglo 'numeros_aleatorios'
    Inicia:
       max1 = Declaro el numero menor posible de java, max2 = igual el numero mas grande
       mini1 = numero mas grande, mini2 = el msa grande
       
    Para cada número 'n' tomar de  'numeros_aleatorios':
       // Lógica para los mayores
       Si (n > max1):
           max2 = max1  // El que era 1ro ahora es 2do
           max1 = n     // El nuevo es el 1ro
       Sino si (n > max2 Y n si es diferente de o !=  max1):
           max2 = n     // El nuevo entra al 2do puesto

           
       // Lógica para los menores
       Si (n < min1):
           mini2 = mini1  // El que era el más pequeñp ahora es el 2do más pequeño
           min1 = n     // El nuevo numero mas pequeño
       Sino si (n < min2 Y n != min1):
           min2 = n     // El nuevo entra al 2do puesto de los numeros pequeños
           
    3. Imprimir max2 y mini2
Fin Algoritmo

2. *Explicación breve de por qué el algoritmo funciona correctamente.*/
El algoritmo funciona porque al comparar cada numoer nuevo con el lider por asi decirlo despues de tomarlo del array y meterlo en la variable n nos aseguramos de no perde la referncia del valor anterio con los max1 y mini 1 por ejemplo el caual se desplazan a la segund aposicion.


3. Análisis de complejidad:

   TIEMPO  (NOTACION O) En tiempo pues porque solo hay un bucle que recorre el arreglo  solamenente una vez esto gracias a que se corre un espacio por asi decirlo en cada comparacion.

   ESPACIO : Porque solo use 4 variables lo que me ayuda a dejar por un lado por asi dericlo si el arreglo tiene mas de 20 datos, lo cual esto me ahora memoria.


EVIDENCIA DEL TRABAJO REALIZADO
<img width="896" height="618" alt="image" src="https://github.com/user-attachments/assets/179c01c4-e198-40f2-a475-755fd0c7ec83" />
<img width="896" height="618" alt="image" src="https://github.com/user-attachments/assets/caf930b7-ae48-4c87-b985-4b5c2b33e30b" />


  
