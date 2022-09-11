# Portafolio de evidencias.

## Semana 9.

Lo que estuve aprendiendo esta semana fue a hacer  la base de datos por ejemplo para hacer un .exe y que si estas en una escuela el profesor pase los datos al código y se lo envié a sus alumnos para que todos vean calificaciones tanto propias como la de los demás compañeros claro poniendo un poco al descubierto a ciertas personas  que salieron bajas o quizás ir haciendo un código para cada persona aunque si estaría difícil para el profesor encargado aunque se divide entre empleado, estudiante y asi para ver como quedan y que labores hacen.
Y otro problema que hay es que cambie mi sistema operativo a kali linux y tuve que aprender como instalar las extensiones con ejecutado y que vienen las librerías.
A continuación pongo imágenes de que da el código:

![image](https://user-images.githubusercontent.com/58115753/189552839-74aa418c-ad01-44aa-9309-a5986f3dc195.png)

A continuacion el codigo:

#include <iostream>
class Persona{
    private:
        char *nombre;
        int edad;
    public:
        Persona(char _nombre[],int _edad);
        void mostrarPersona();
};
Persona::Persona(char _nombre[],int _edad){
    nombre=_nombre;
    edad=_edad;
}
void Persona::mostrarPersona(){
    std::cout<<"Nombre:"<<nombre<<"\n";
    std::cout<<"Edad:"<<edad<<"\n";
}
class Empleado:public Persona{
    private:
        float sueldo;
    public:
        Empleado(char _nombre[],int _edad,float _sueldo);
        void mostrarEmpleado();
};
Empleado::Empleado(char _nombre[],int _edad,float _sueldo):Persona(_nombre,_edad){
    sueldo=_sueldo;    
}
void Empleado::mostrarEmpleado(){
    std::cout<<"Sueldo:"<<sueldo<<"\n";
}
class Estudiante:public Persona{
    private:
        float calificacion;
    public:
        Estudiante(char _nombre[],int _edad,float _calificacion);
        void mostrarEstudiante();
};
Estudiante::Estudiante(char _nombre[],int _edad,float _calificacion):Persona(_nombre,_edad){
    calificacion=_calificacion;
}
void Estudiante::mostrarEstudiante(){
    std::cout<<"Calificacion:"<<calificacion<<"\n";
}

class Universitario:public Estudiante{
    private:
        char *carrera;
    public:
        Universitario(char _nombre[],int _edad,float _calificacion,char _carrera[]);
        void mostrarUniversitario();
};
Universitario::Universitario(char _nombre[],int _edad,float _calificacion,char _carrera[]):Estudiante(_nombre,_edad,_calificacion){
    carrera=_carrera;
}
void Universitario::mostrarUniversitario(){
    std::cout<<"Carrera: "<<carrera<<"\n";
}
int main(){
    Persona p1("Alan",20);
    p1.mostrarPersona();
    std::cout<<"________________\n";
    Empleado e1("Yorell",20,15000);
    e1.mostrarPersona();
    e1.mostrarEmpleado();
    std::cout<<"________________\n";
    Estudiante es1("Maria",18,10);
    es1.mostrarPersona();
    es1.mostrarEstudiante();
    std::cout<<"________________\n";
    Universitario u1("Hernesto",25,9,"Vulneravilidad");
    u1.mostrarPersona();
    u1.mostrarEstudiante();
    u1.mostrarUniversitario();
    system("pause");
    return 0;
}
