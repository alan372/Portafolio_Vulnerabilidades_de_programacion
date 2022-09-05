# Portafolio de evidencias.

## Semana 8.

Lo que aprendí esta semana ya fue lo ultimo lo que se vio fue Hacer un programa en C++ para registrar los datos de tres libros como: título, autor, año y color del libro. El color se deberá hacer mediante una enumeración y sólo habrá rojo, verde y azul.
Lo cual se realizo el siguiente código:

#include <iostream>
using namespace std;
enum Color{
 rojo,verde,azul
};
struct Libro{
 char titulo[20],autor[20];
 int anio;
 Color color;
};
void datosLibro(Libro[]);
void mostrarLibro(Libro[]);
int main(){
 Libro libro[3];
 datosLibro(libro);
 mostrarLibro(libro);
   
   return 0;
}

void datosLibro(Libro libro[3]){
 for(int i = 0; i < 3; i++){
  cout <<"Titulo libro " <<i+1 <<endl;
  cin.getline(libro[i].titulo,20);
  cout <<"Autor libro " <<i+1 <<endl;
  cin.getline(libro[i].autor,20);
  cout <<"Año libro " <<i+1 <<endl;
  cin >> libro[i].anio;
  cin.ignore();
 }
 libro[0].color = rojo;
 libro[1].color = verde;
 libro[2].color = azul;
}

void mostrarLibro(Libro libro[3]){
 for(int i = 0; i < 3; i++){
  cout <<"Titulo: " <<libro[i].titulo <<endl;
  cout <<"Autor: " <<libro[i].autor <<endl;
  cout <<"Año: " <<libro[i].anio <<endl;
  
  switch(libro[i].color){
   case rojo: 
    cout <<"Color: Rojo" <<endl; break;
   case verde:
    cout <<"Color: Verde" <<endl; break;
   case azul:
    cout <<"Color: Azul" <<endl; break;
  }
 }
}

lo que vimos fue como se ejecutaba un código que se esta organizando poco a poco para el registro de una biblioteca lo cual da como resultado los libros que hay y se pintaran según estén o no y se acomodaran para el movimiento seguro.

 Tambien enseñaron la importancia de las bibliotecas y por que se deberian de utilizar mas seguido y especificar bien las librerias y para que esl curso no terminara mas rapido dejaron unos ejercicios que hacer solo por lo que estoy aplendiendo a usar una nueva interfaz ya que cambie de sistema operativo y se me esta dificultando las cosas. 
