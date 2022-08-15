# Portafolio de evidencias.

## Semana 5.
Lo que aprendí esta semana son como es fue realizar otro pequeño ejercicio mu parecido a otro que hice anterior mente en donde cree un base de datos para una escuela pero con casi la misma estructura nada más que le agregue los datos que pedía el problema para la empresa por lo que no se me dificulto mucho por lo que les muestro el codigo en el siguiente

// primer ejercicio
 
#include <iostream>

using namespace std;

struct registro {
    char nombre[35];
    string correo, telefono, pais;
    int edad;
};

registro persona[10];

void listado();
void registrar();
int i = 0;


int main()
{
    int op, op1;
    do {
        cout << "\t\n\tMenu\n\n";
        cout << "1.Registrar persona " << endl;
        cout << "2.ver listado " << endl;
        cout << "3.Salir " << endl;
        cout << "Escoja una opcion: " << endl;
        cin >> op;
        //system("cls");
        switch (op) {
        case 1:
            registrar();
            //system("cls");
            break;
        case 2:
            listado();
            break;
        case 3:
            cout << "\t\n\tSALIENDO\n\n";
            return 0;
            break;
        default:
            cout << "\t\n\tError de opcion\n\n";
            break;
        }
        cout << "Desea regresar al menu\n" << endl;
        cout << "1.SI/2.NO" << endl;
        cin >> op1;
    } while (op1 == 1);

    getchar();

    return 0;
}

void listado() {
    int j;

    for (j = 0; j < i; j++) {
        cout << "NOMBRE: " << persona[j].nombre << endl;
        cout << "EDAD: " << persona[j].edad << endl;
        cout << "TELEFONO: " << persona[j].telefono << endl;
        cout << "CORREO: " << persona[j].correo << endl;
        cout << "PAIS: " << persona[j].pais << endl;
    }
}

void registrar() {
    int n;
    cout << "Cuantas personas desea registrar: ";
    cin >> n;
    for (i = 0; i < n; i++) {
        cout << "Registro " << endl;
        cout << "ingrese el nombre completo: \n";
        cin.getline(persona[i].nombre, 35);
        cin.getline(persona[i].nombre, 35);
        cout << "Ingrese la edad: \n";
        cin >> persona[i].edad;
        cout << "Ingrese el numero telefonico: \n";
        cin >> persona[i].telefono;
        cout << "Ingrese su correo electronico: \n";
        cin >> persona[i].correo;
        cout << "Ingrese su pais de procedencia: \n";
        cin >> persona[i].pais;
    }
}
	// IMAGENES DE EJEMPLOS:
	
![image](https://user-images.githubusercontent.com/58115753/184575996-a85cd18e-964c-4540-aa55-f4ffb01699d2.png)
![image](https://user-images.githubusercontent.com/58115753/184576069-b0ef1436-766c-4b76-8b89-2234b5907616.png)
![image](https://user-images.githubusercontent.com/58115753/184576148-1d6d04cb-1a87-4c6e-86c2-4046eb1fd76c.png)


  por lo que el anterior codigo  como segunda actividad se hizo un código para sacar la raíz de cualquier número x después que ese eleve al cuadrado y que se reste 1 y por ultimo que el resultado 1 se divida entre el segundo el cual seria el sigueinte
	
	
int main(){ // no se cuenta esto del codigo	

#include <iostrea>	
#include <math.h>

using namespace std;

int main() {
	float n = 0, m = 0, resultado = 0;

	// Raiz quinta de 100;
	n = 100;
	m = 5;
	resultado = pow(n, (1 / m));
	cout << "La raiz quinta de 100 es: " << resultado;

	cout << endl << endl;

	// 5 a la potencia 24.
	n = 5;
	m = 24;
	resultado = pow(n, m);
	cout << "5 a la potencia 24: " << resultado;

	return 0;
} 
 }
  
  como se puede ver este es mas corto pero saca la raiz de los numero especificados 

