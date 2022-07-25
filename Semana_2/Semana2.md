# Portafolio de evidencias.

## Semana 2.

en esta semana entre en un curso de c++ donde me enseñaron lo primero por que es tan importante el c++. despues empesamos con lopractico donde nos muestra como hacer el primer programa y nos explica como funciona.
1.-empezamos con las librerias como funcionan  com iostrea que seria la entrada y salida de datos
2.-int main que es la funcion principal
3.-despues cramos un hola mundo poniendo primero el cout que imprimira todo lo que se escriba
4.-y ponerle return 0 para mostrar que ya esta cerrado.


Programa de hola mundo:

#include <iostream>
using  namespace std;

int main()
{
	cout << "Hola Virginia Hernadez Lagarde" << endl;
	system("pause");
	return 0;

}
  
  despues hubo un ejercicio de variables con enteros y con decimal 
  
  #include <iostream>
  
  int main(){
    int entero=10;
    std::cout<<entero;
    std::cin.get();
    return 0;
  }
  
  en este ejemplo no se pueden agregar decimal y al momento de correr con por ejemplo 6.2 nada mas marca 6.
  
  ahora uno que marca el decimal con el comando flotante
   
  #include <iostream>
  
   int main(){
    int entero=10;
    float flotante=9.99;
    std::cout<<flotante;
    std::cin.get();
    return 0;
  }
  ahora con una letra
  
    
  #include <iostream>
  
   int main(){
    int entero=10;
    float flotante=9.99;
    char caracter=c;
    std::cout<<caracter;
    std::cin.get();
    return 0;
  }
