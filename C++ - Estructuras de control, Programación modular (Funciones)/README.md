<div style="text-align: justify">

# C ++ / Estructuras de control - Programación modular (Funciones).

En el lenguaje de programación C++, las funciones son bloques de código que realizan una o varias tareas y pueden ser llamados desde otras partes del programa. Las funciones permiten la modularización del código, mejorando la legibilidad y la reutilización.

## Defición de función.

```C++
void funcion() // Defición de función.
    {
        //Cuerpo de la función.
    }
```
<br>

-------

<br>


**Ejemplo de función simple**:

Realizaremos una función llamada `sumar` que recibirá dos números enteros como parámetros. Estos dos parámetros se sumarán y la función retornara el resultado. Una vez que hayamos definido la función, la utilizaremos en nuestro programa principal.

```C++
#include<iostream>
using namespace std;
int sumar(int a, int b); // Declaración de función.
int main()
    {
        int n1, n2, resultado;
        cin>>n1;
        cin>>n2;
        resultado = sumar(n1,n2); // Invocación de función.
        cout<<"El resultado es: "<<resultado;
        return 0;
    }
int sumar(int a,int b) // Definición de función.
    {
        return a + b;
    }
```
## Funciones sin `Parámetros` y sin `Retorno`.

Las funciones también pueden no recibiir parámetros ni devolver valores. En estos casos, se utiliza `void` como tipo de retorno.

```C++
#include<iostream>
using namespace std;
void saludar(); // Declaración de función.
int main()
    {
        saludar(); // Invocación de función.
        return 0;
    }
void saludar()  // Definición de función.
    {
        cout<<"Hola.";
    }

```
## Funciones con `Parámetros`.

Las funciones pueden recibir parámetros para realizar operaciones. Los parámetros se especifican en la lista de parámetros durante la declaración y definición de la función.

```C++
#include<iostream>
using namespace std;
void escribir(string a); // Declaración de función.
int main()
    {
        escribir("Hola Mundo."); // Invocación función.
        return 0;
    }
void escribir(string a) // Definición de función.
    {
        cout<<a;
    }
```
## Valor de Retorno.

El valor de retorno es el resultado que una función devuelve después de su ejecución. El tipo de retorno debe coincidir con el tipo especificado en la declaración de la función.

```C++
#include<iostream>
using namespace std;
float dividir(float x, float y); // Declaración función.
int main()
    {
        cout<<"El resultado es: "<<dividir(6,3); // Invocación de función.
        return 0;
    }
float dividir(float x, float y) // Definición de función.
    {
        return x / y;
    }
```

**Ejercicios**:

1. Escribe un programa en `C++` que implemente una calculadora básica con un menú que permita al usuario seleccionar la operación deseada ( suma, resta, multiplicación y división). 

2. Desarrolla un programa  en `C++` que simule el control de una máquina industrial básica. El programa debe ofrecer un menú que permita al usuario realizar diversas operaciones de control sobre la máquina, además una vez seleccionado la opción el programa debe consultar al usuario si quiere volver a ejecutar el programa. Entre las operaciones disponibles se encuentra:

- `Encender la máquina`: Esta opción encender la máquina si aún no está encendida. Si la máquina ya está encendida, mostrará un mensaje indicando que ya está en funcionamiento y además tomara una velocidad 2850 RPM.

- `Apagar la máquina`: Esta opción permite apagar la máquina. Al apagarla, también se reinicia la velocidad de la máquina a cero.

- `Consultar estado de la máquina`: Muestra al usuario el estado actual de la máquina, incluyendo si está encendida o apagada y la velocidad actual configurada.

- `Salir del programa`: Finaliza la ejecución del programa de control de la máquina industrial.

El programa debe implementar funciones seperadas para cada una de las operaciones mencionadas.

3. Desarrolle un programa en `C++` que simule el funcionamiento de un cajero automático básico. El programa debe solicitar al usuario que ingrese su número de cuenta, el cual debe tener el formato `0000001`, si ingresa otro numero de cuenta debe avisar que se produjo un `Error` y luego le debe permitir crear una contraseña personal de 4 digitos numéricos para acceder a su cuenta.

Una vez calidado el ingreso, el programa debe ofrecer un menú con diferentes opciones para realizar operaciones típicas de un cajero automático, como consutar saldo, realizar otra operación, depositar dinero, retirar dinero y salir del sistema.

- `Consultar saldo`: Esta opción permite al usuario ver el saldo actual disponible en su cuenta bancaria.

- `Volver a realizar otra operación`: Esta opción permite volver a ejecutar el programa desde el principio.

- `Retirar dinero`: Permite al usuario retirar una cantidad específica de dinero de su  cuenta, siempre y cuando tenga fondos suficientes disponibles.

- `Salir del sistema`: Finaliza la sesión del cajero automático.

El programa debe implementar funciones separadas apra cada una de las operaciones mencionadas.

</div>