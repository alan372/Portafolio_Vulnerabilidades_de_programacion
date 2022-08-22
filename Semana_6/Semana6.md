# Portafolio de evidencias.

## Semana 6.

Lo que aprendí esta semana fue a cómo usar la integración de herencia y colecciones, Modificación de clases, Herencia de clases, Utilización de colecciones entre otras cosas para hacer una base de datos más sofisticada dividida por partes con la lista de profesores y los cursos esta vez llenando con datos para que se pueda diferenciar que alumnos ya estaban registrados y cuales no por lo que es mejor base de datos ya que cada uno está ya registrado desde el código y se va registrando, también agrega una base que busca si pones el nombre especifico conforme se registren más a continuación mi código y después capturas de como se ve. 

#Imagenes de ejemplo


#include <iostream>
#include <string.h>
#include <windows.h>

using namespace std;



#define max 100   //valor maximo que se les dara a los profesores y alumnos



void principal(string title)
{
	int val, i;
	
	val = title.length();
	
	val = val + 20;
	
	
	//imprime asteriscos
	for(i=0; i <=val; i++)
	{
		cout << "*";
	}
	cout << "\n\n";
	
	
	//imprimir titulo
	for(i=0; i <=val; i++)
	{
		cout << " ";
		if(i == 5)
		{
			cout << title;
		}
		cout << " ";
	}
	
	cout << "\n";
	
	
	//imprimir asteriscos
	for(i=0; i <=val; i++)
	{
		cout << "*";
	}
	
	cout << "\n \n \n";
	
}





//VARIABLES GENERALES
string bs;
int result;

int alumno = 2;
int maestro = 10;
int curso = 0;
int matricula =0;

int capacidadcurso = 5;
int cantidadmatricula = 0;

string tipobusqueda;



//estructuras
struct maestros
{
	string codprof, prof;
	string salario;
}profesores[max];



struct alumnos
{
	string codalumno, alumno, empresa, ruc, tel1, tel2, direccion;
}estudiantes[max];

struct catedras
{
	string codcurso, creditos, nrodehoras, semestre, nombre, cantMatri;
	int capacidad;

	
}cursos[max];


struct fichas
{
	string codalumno, codcurso;
}matriculas[max];




//prototipos

void error();

void agregaralumnos(int al);
void menuverificacion();
void verificacion(string cod, boolean st);
void buscaralumnos();
void menubuscaralumnos();

void profagrega(int tl);
void verprof(string codigo);
void menuprof();

void agregarcurso(int cr);
void vercurso(string codigo);
void menucurso();

void agregarmatricula(int mr);
void verificadatos(string codigo, boolean st);
void menumatricula();

void listar(string nom);




//iniciar datos cargados

void cargadatos()
{
	
	//datos ya ingresados de estudiantes
	estudiantes[0].alumno = "edgar ramirez";
	estudiantes[0].codalumno = "23";
	estudiantes[0].direccion = "GUATEMALA";
	estudiantes[0].ruc = "50";
	estudiantes[0].empresa = "MALINAS";
	estudiantes[0].tel1 = "32233323";
	estudiantes[0].tel2 = "33333333";
	
	estudiantes[1].alumno = "maria solinas";
	estudiantes[1].codalumno = "52";
	estudiantes[1].direccion = "SALVADOR";
	estudiantes[1].ruc = "50";
	estudiantes[1].empresa = "BOTONES";
	estudiantes[1].tel1 = "32233323";
	estudiantes[1].tel2 = "3338075333";
	
	estudiantes[2].alumno = "merry merida";
	estudiantes[2].codalumno = "22";
	estudiantes[2].direccion = "HONDURAS";
	estudiantes[2].ruc = "50";
	estudiantes[2].empresa = "SATINAS";
	estudiantes[2].tel1 = "32288623";
	estudiantes[2].tel2 = "333345443";
	
	
	//DATOS INGRESADOS DE PROFESORES
	profesores[0].codprof = "2334";
	profesores[0].prof = "JOSE ALVARADO";
	profesores[0].salario = "2,000";
	
	profesores[1].codprof = "2334";
	profesores[1].prof = "JOSE ALVARADO";
	profesores[1].salario = "2,000";
	
	profesores[2].codprof = "2334";
	profesores[2].prof = "JOSE ALVARADO";
	profesores[2].salario = "2,000";
	
	profesores[3].codprof = "2334";
	profesores[3].prof = "JOSE ALVARADO";
	profesores[3].salario = "2,000";
	
	profesores[4].codprof = "2334";
	profesores[4].prof = "JOSE ALVARADO";
	profesores[4].salario = "2,000";
	
	profesores[5].codprof = "2334";
	profesores[5].prof = "JOSE ALVARADO";
	profesores[5].salario = "2,000";
	
	profesores[6].codprof = "2334";
	profesores[6].prof = "JOSE ALVARADO";
	profesores[6].salario = "2,000";
	
	profesores[7].codprof = "2334";
	profesores[7].prof = "JOSE ALVARADO";
	profesores[7].salario = "2,000";
	
	profesores[8].codprof = "2334";
	profesores[8].prof = "JOSE ALVARADO";
	profesores[8].salario = "2,000";
	
	profesores[9].codprof = "2334";
	profesores[9].prof = "JOSE ALVARADO";
	profesores[9].salario = "2,000";
	
}

 main()
{
	string op = "";
	
	cargadatos();	
	
	
	system("color 2b");
	system("cls");
	principal("SISTEMA DE MATRICULAS ESCOLARES");
	
	while(true)
	{
		cout << "1.   NUEVOS ALUMNOS \n";
		cout << "2.   BUSCAR ALUMNOS \n";
		cout << "3.   NUEVOS PROFESORES \n";
		cout << "4.   NUEVOS CURSOS \n";
		cout << "5.   MATRICULA \n";
		cout << "6.   LISTA DE ALUMNOS \n";
		cout << "7.   LISTA DE PROFESORES \n";
		cout << "8.   LISTA DE CURSOS \n";
		cout << "9.   SALIR \n \n";
		cin >> op;
		
		if(op == "1")
		{
			alumno++;
			agregaralumnos(alumno);				
			break;
		}
		else if(op == "2")
		{
			buscaralumnos();
			break;
		}
		else if(op == "3")
		{
			profagrega(maestro);
			break;
		}
		else if(op == "4")
		{
			agregarcurso(curso);
			break;
		}
		else if(op=="5")
		{
			agregarmatricula(matricula);
			break;
		}
		else if(op=="6")
		{
			listar("alumno");
			break;
		}
		else if(op=="7")
		{
			listar("profesor");
			break;
		}
		else if(op=="8")
		{
			listar("curso");
			break;
		}
		else if (op == "9")
		{
			return 0;
		}
		else
		{
			//break;
			error();
			return main();
			
			
		}
	}
	
	
}

void error()
{
	system("cls");
	principal("SISTEMA DE MATRICULAS ESCOLARES");
	cout << "ERROR DE OPCION INGRESADA, INTENTA NUEVAMENTE ";
	cout << "\n \n";
	system("pause");
	
}


void verificacion(string cod, boolean st)
{
	int estado = 0;
	int i;
	

	
	if (st == true)
	{
		//Recorre para la busqueda de alumno
		for(i=0; i< alumno; i++ )
		{
			//VERIFICA SI ENCUENTRA LOS DATOS DEL ALUMNO
			if (cod == estudiantes[i].codalumno )
			{
			
				estado = 1;
				
				break;
				
			}
		
		}
		
	}
	else
	{
		for(i=0; i< maestro; i++ )
		{
			//VERIFICA SI ENCUENTRA LOS DATOS DEL PROFESOR
			if (cod == profesores[i].codprof )
			{
			
				estado = 1;
				break;
			}
			
		}
	}
	
	
	result = estado;  //obtenemos el valor para busqueda en opcion de matricula
	
	
	
	//CONFIRMACION SI ENCONTRO LOS DATOS 
	
	if (estado == 0)
	{
		system("cls");
		principal("SISTEMA DE MATRICULAS ESCOLARES");
		
		cout << "EL NUEVO REGISTRO SE AGREGO CORRECTAMENTE ";
		cout << "\n \n";
		system("pause");
		main();
		
	}
	else if (estado == 1)
	{
		system("cls");
		principal("SISTEMA DE MATRICULAS ESCOLARES");
		
		cout << "EL NUEVO REGISTRO YA EXISTE ";
		cout << "\n \n";
		system("pause");
		
		menuverificacion();
		
	}
	
	
}

void menuverificacion()
{
	string op2;
	system("cls");
	principal("SISTEMA DE MATRICULAS ESCOLARES");
				
		while(true)
		{
			cout << "1. REGISTRAR DE NUEVO \n";
			cout << "2. IR MENU PRINCIPAL \n";
			cout << "\n \n";
			cin >> op2;
				
			if(op2 == "1")
			{
				agregaralumnos(alumno);
				break;
			}
			else if(op2 == "2")
			{
				alumno = alumno -1;
				main();
				break;
			}
			else
			{
				error();
				menuverificacion();
				//break;
			}
		}
}


void agregaralumnos(int al)
{
	

	bs = "";
	system("color 1b");
	system("cls");
	principal("SISTEMA DE MATRICULAS ESCOLARES");
	
	
	if(al >  6)
	{
		cout << "AGENDA LLENA ";
		cout << "\n \n";
		system("pause");
		main();
	}
	else
	{
		
	cout << "INGRESAR CODIGO:  ";
	cin >> estudiantes[al].codalumno ;
	
	cout << "\n";
	
	cout << "INGRESAR NOMBRE:  ";
	cin >> estudiantes[al].alumno;	
	
	cout << "\n";
	
	cout << "INGRESAR RUC:  ";
	cin >> estudiantes[al].ruc ;
	
	cout << "\n";
	
	cout << "INGRESAR EMPRESA:  ";
	cin >> estudiantes[al].empresa ;
	
	cout << "\n";
	
	cout << "INGRESAR DIRECCION:  ";
	cin >> estudiantes[al].direccion  ;
	
	cout << "\n";
	
	cout << "INGRESAR TELEFONO 1:  ";
	cin >> estudiantes[al].tel1  ;
	
	cout << "\n";
	
	cout << "INGRESAR TELEFONO 2:  ";
	cin >> estudiantes[al].tel2  ;
		
	bs = estudiantes[al].codalumno ;

	
	//verificacion(alum[al].codalumno, true );
	verificacion(bs, true );
	//main();
	}
	
	
}



void buscaralumnos()
{
	int i;
	string busca;
	boolean st = false;
	

	
	system("cls");
	principal("SISTEMA DE MATRICULAS ESCOLARES");
	
	cout << "NOMBRE DE ALUMNO PARA BUSCAR :   ";
	cin >> busca;
	
	for(i= 0; i<= alumno; i++)
	{
		if(busca == estudiantes[i].codalumno )
		{
			
			st = true;
			break;
			
		}	
	
	}
	
	cout << "\n";
	
	if (st == true)
	{
		cout << "ENCONTRADO \n \n";
		
		
		cout << "INGRESAR CODIGO:  " << estudiantes[i].codalumno ;	
	
		cout << "\n";
	
		cout << "INGRESAR NOMBRE:  " << estudiantes[i].alumno ;
			
		cout << "\n";
	
		cout << "INGRESAR RUC:  " << estudiantes[i].ruc;	
	
		cout << "\n";
	
		cout << "INGRESAR EMPRESA:  " << estudiantes[i].empresa;
			
		cout << "\n";
	
		cout << "INGRESAR DIRECCION:  " << estudiantes[i].direccion;	
	
		cout << "\n";
	
		cout << "INGRESAR TELEFONO 1:  " << estudiantes[i].tel1;
		
		cout << "\n";
	
		cout << "INGRESAR TELEFONO 2:  " << estudiantes[i].tel2;
		
		cout << "\n \n";
		
		busca = "";
		system("pause");
		
		menubuscaralumnos();
	
	}
	else
	{
		cout << "ALUMNO NO ENCONTRADO \n \n";
		system("pause");
		menubuscaralumnos();
	}
	
	
}


void menubuscaralumnos()
{
	string op2;
	system("cls");
	principal("SISTEMA DE MATRICULAS ESCOLARES");
				
		while(true)
		{
			cout << "1. REALIZAR NUEVA BUSQUEDA \n";
			cout << "2. IR MENU PRINCIPAL \n";
			cout << "\n \n";
			cin >> op2;
				
			if(op2 == "1")
			{
				buscaralumnos();
				break;
			}
			else if(op2 == "2")
			{
				alumno = alumno -1;
				main();
				break;
			}
			else
			{
				error();
				op2 = "";
				menubuscaralumnos();
				//break;
			}
		}
}


void profagrega(int tl)
{
	bs = "";
	
	system("color 1b");
	system("cls");
	principal("SISTEMA DE MATRICULAS ESCOLARES");
	
	cout << "INGRESAR CODIGO:  ";
	cin >> profesores[tl].codprof ;
	
	cout << "\n";
	
	cout << "INGRESAR PROFESOR:  ";
	cin >> profesores[tl].prof;	
	
	cout << "\n";
	
	cout << "INGRESAR SALARIO:  ";
	cin >> profesores[tl].salario ;
	
	verprof(profesores[tl].codprof);
	
	
}

void verprof(string codigo)
{
	int i;
	result = 0;
	

	//Recorre para revisar si ya existe el profesor
		for (i=0; i < maestro; i++)
		{
			
		
			if (profesores[i].codprof == codigo)
			{
				result = 1;
				break;
			}
			
		}

	
	//verifica el resultado de la busqueda
	if (result == 0)
	{
		system("cls");
		principal("SISTEMA DE MATRICULAS ESCOLARES");
		cout << "LOS DATOS REGISTRADOS CON EXITO ";
		cout << "\n \n";
		maestro ++;
		system("pause");
		main();
	}
	else
	{
		system("cls");
		principal("SISTEMA DE MATRICULAS ESCOLARES");
		cout << "LOS DATOS YA EXISTE INTENTA DE NUEVO";
		cout << "\n \n";
		system("pause");
		menuprof();
	}
	
		
}

void menuprof()
{
	string op2;
	system("cls");
	principal("SISTEMA DE MATRICULAS ESCOLARES");
				
		while(true)
		{
			cout << "1. INGRESAR DE NUEVO \n";
			cout << "2. IR MENU PRINCIPAL \n";
			cout << "\n \n";
			cin >> op2;
				
			if(op2 == "1")
			{
				profagrega(maestro);
				break;
			}
			else if(op2 == "2")
			{
				maestro --;
				main();
				break;
			}
			else
			{
				menuprof();
				//break;
			}
		}
}


void agregarcurso(int cr)
{
	
	bs = "";
	
	if (cantidadmatricula < 5)
	{
		system("color 5b");
		system("cls");
		principal("SISTEMA DE MATRICULAS ESCOLARES");
		
		cout << "INGRESAR CODIGO DE CURSO  :  ";
		cin >> cursos[cr].codcurso ;
		
		cout << "\n";
		
		cout << "INGRESAR CREDITOS  :  ";
		cin >> cursos[cr].creditos;	
		
		cout << "\n";
		
		cout << "INGRESAR NOMBRE DE CURSO  :  ";
		cin >> cursos[cr].nombre ;
		
		cout << "\n";
		
		cout << "INGRESAR HORA DE CURSO  :  ";
		cin >> cursos[cr].nrodehoras;
		
		cout << "\n";
		
		cout << "INGRESAR SEMESTRE  :  ";
		cin >> cursos[cr].semestre ;
		
		cout << "\n";
		
		cout << "INGRESAR CANTIDAD DE MATRICULA  :  ";
		cin >> cursos[cr].cantMatri ;
		
		cout << "\n";
		
		vercurso(cursos[cr].codcurso);
	}
	else
	{
		system("color 5b");
		system("cls");
		principal("SISTEMA DE MATRICULAS ESCOLARES");
		system("pause");
		main();
	}
	
	
	
	
}


void vercurso(string codigo)
{
	int i;
	result = 0;
	

	//Recorre para revisar si ya existe el profesor
		for (i=0; i < curso; i++)
		{
			
		
			if (cursos[i].codcurso == codigo)
			{
				result = 1;
				break;
			}
			
		}

	
	//verifica el resultado de la busqueda
	if (result == 0)
	{
		system("cls");
		principal("SISTEMA DE MATRICULAS ESCOLARES");
		cout << "LOS DATOS REGISTRADOS CON EXITO ";
		cout << "\n \n";
		curso ++;
		system("pause");
		main();
	}
	else
	{
		system("cls");
		principal("SISTEMA DE MATRICULAS ESCOLARES");
		cout << "LOS DATOS YA EXISTE INTENTA DE NUEVO";
		cout << "\n \n";
		system("pause");
		menucurso();
	}
}

void menucurso()
{
	string op2;
	system("cls");
	principal("SISTEMA DE MATRICULAS ESCOLARES");
				
		while(true)
		{
			cout << "1. INGRESAR DE NUEVO \n";
			cout << "2. IR MENU PRINCIPAL \n";
			cout << "\n \n";
			cin >> op2;
				
			if(op2 == "1")
			{
				agregarcurso(curso);
				break;
			}
			else if(op2 == "2")
			{
				curso --;
				main();
				break;
			}
			else
			{
				menucurso();
				//break;
			}
		}
}


void agregarmatricula(int mr)
{
	string codalumno, codcurso;
	
	
	system("color 5b");
	system("cls");
	principal("SISTEMA DE MATRICULAS ESCOLARES");
		
	cout << "INGRESAR CODIGO DE ALUMNO  :  ";
	cin >> codalumno;
	
	verificadatos(codalumno, true);
	
	if (result == 1)
	{
		cout << "\n";		
		cout << "INGRESAR CODIGO DE CURSO  :  ";
		cin >> codcurso;
		
		verificadatos(codcurso, false);
		
		if (result == 1)
		{
			if(cantidadmatricula < capacidadcurso)
			{
				matriculas[matricula].codalumno;
				matriculas[matricula].codcurso;
				
				
				system("color 5b");
				system("cls");
				principal("SISTEMA DE MATRICULAS ESCOLARES");
				cout<< "EL ALUMNO HA SIDO MATRICULADO";
				cout << "\n \n \n";
				matricula ++;
				system("pause");
				
				main();
			}
		}
		else
		{
			system("color 5b");
			system("cls");
			principal("SISTEMA DE MATRICULAS ESCOLARES");
			cout << "EL CODIGO DE CURSO INGRESADO NO EXISTE ";
			cout << "\n \n \n";
			system("pause");
			menumatricula();
		}
			
	}
	else
	{
		system("color 5b");
		system("cls");
		principal("SISTEMA DE MATRICULAS ESCOLARES");
		cout << "EL CODIGO DE ALUMNO INGRESADO NO EXISTE ";
		cout << "\n \n \n";
		system("pause");
		menumatricula();
	}
		
	
}

void menumatricula()
{
	string op2;
	system("cls");
	principal("SISTEMA DE MATRICULAS ESCOLARES");
				
		while(true)
		{
			cout << "1. INGRESAR DE NUEVO \n";
			cout << "2. IR MENU PRINCIPAL \n";
			cout << "\n \n";
			cin >> op2;
				
			if(op2 == "1")
			{
				agregarmatricula(matricula);
				break;
			}
			else if(op2 == "2")
			{
				if(matricula > 0)
				{
					matricula --;
				}
				main();
				break;
			}
			else
			{
				error();
				menumatricula();
				//break;
			}
		}
}


void verificadatos(string codigo, boolean st)
{
	result = 0;
	int i;
	
	
	if(st == true)
	{
		for(i=0; i<= alumno; i++)
		{
			if(codigo == estudiantes[i].codalumno)
			{
				result = 1;
				break;
			}
		}
	}
	else
	{
		for(i=0; i<= curso; i++)
		{
			if(codigo == cursos[i].codcurso)
			{
				result = 1;
				break;
			}
		}
	}
	
}



void listar(string nom)
{
	int i;
	

	
	string auxalum[max][10];
	boolean cambios = false;
	string aux[max];
	
	
	system("color 4b");
	system("cls");
	principal("SISTEMA DE MATRICULAS ESCOLARES");
	
	
	if (nom == "alumno")
	{
		system("color 4b");
		//system("cls");
		principal("LISTA DE ALUMNOS");
		
		while(true)
		{
			cambios = false;
			for(i=1; i<= alumno; i++)
			{
				if(estudiantes[i].codalumno < estudiantes[i-1].codalumno)
				{
				
					aux[1] = estudiantes[i].codalumno;
					estudiantes[i].codalumno = estudiantes[i-1].codalumno;
					estudiantes[i-1].codalumno = aux[1];
					
					aux[2] = estudiantes[i].alumno;
					estudiantes[i].alumno = estudiantes[i-1].alumno;
					estudiantes[i-1].alumno = aux[2];
					
					aux[3] = estudiantes[i].direccion;
					estudiantes[i].direccion = estudiantes[i-1].direccion;
					estudiantes[i-1].direccion = aux[3];
					
					aux[4] = estudiantes[i].empresa;
					estudiantes[i].empresa = estudiantes[i-1].empresa;
					estudiantes[i-1].empresa = aux[4];
					
					aux[5] = estudiantes[i].ruc;
					estudiantes[i].ruc = estudiantes[i-1].ruc;
					estudiantes[i-1].ruc = aux[5];
					
					aux[6] = estudiantes[i].tel1;
					estudiantes[i].tel1 = estudiantes[i-1].tel1;
					estudiantes[i-1].tel1 = aux[6];
					
					aux[7] = estudiantes[i].tel2;
					estudiantes[i].tel2 = estudiantes[i-1].tel2;
					estudiantes[i-1].tel2 = aux[7];
					
					
					cambios = true;
					
				}
			}
			
			if(cambios==false)
			{
				break;
			}
		}
		
		
			
		for(i=0; i<=alumno; i++)
		{
			cout << estudiantes[i].codalumno << "  " << estudiantes[i].alumno << "  " << estudiantes[i].direccion << "  " << estudiantes[i].empresa << "  " << estudiantes[i].ruc << "  " << estudiantes[i].tel1 << "  " << estudiantes[i].tel2;
			cout << "\n \n \n";
			
		}
		
				
	}
	
	else if(nom=="profesor")
	{
		system("color 4b");
		//system("cls");
		principal("LISTA DE PROFESORES");
		
		while(true)
		{
			cambios = false;
			for(i=1; i<= maestro; i++)
			{
				if(profesores[i].codprof < profesores[i-1].codprof)
				{
				
					aux[1] = profesores[i].codprof;
					profesores[i].codprof = profesores[i-1].codprof;
					profesores[i-1].codprof = aux[1];
					
					aux[2] = profesores[i].prof;
					profesores[i].prof = profesores[i-1].prof;
					profesores[i-1].prof = aux[2];
					
					aux[3] = profesores[i].salario;
					profesores[i].salario = profesores[i-1].salario;
					profesores[i-1].salario = aux[3];
					
					
					cambios = true;
					
				}
			}
			
			if(cambios==false)
			{
				break;
			}
		}
		
		
			
		for(i=0; i<=maestro; i++)
		{
			cout << profesores[i].codprof << "  " << profesores[i].prof << "  " << profesores[i].salario ;
			cout << "\n \n \n";
			
		}
	}
	else if(nom == "curso")
	{
		system("color 4b");
		//system("cls");
		principal("LISTA DE CURSOS");
		
		while(true)
		{
			cambios = false;
			for(i=1; i<= curso; i++)
			{
				if(cursos[i].semestre > cursos[i-1].semestre)
				{
				
					aux[1] = cursos[i].codcurso;
					cursos[i].codcurso = cursos[i-1].codcurso;
					cursos[i-1].codcurso = aux[1];
					
					aux[2] = cursos[i].creditos;
					cursos[i].creditos = cursos[i-1].creditos;
					cursos[i-1].creditos = aux[2];
					
					aux[3] = cursos[i].nombre;
					cursos[i].nombre = cursos[i-1].nombre;
					cursos[i-1].codcurso = aux[3];
					
					aux[4] = cursos[i].nrodehoras;
					cursos[i].nrodehoras = cursos[i-1].nrodehoras;
					cursos[i-1].nrodehoras = aux[4];
					
					aux[5] = cursos[i].semestre;
					cursos[i].semestre = cursos[i-1].semestre;
					cursos[i-1].semestre = aux[5];
					
					
					aux[6] = cursos[i].cantMatri;
					cursos[i].cantMatri = cursos[i-1].cantMatri;
					cursos[i-1].cantMatri = aux[6];
					
					
					cambios = true;
					
				}
			}
			
			if(cambios==false)
			{
				break;
			}
		}
		
		
			
		for(i=0; i<=curso; i++)
		{
			cout << cursos[i].codcurso << "  " <<cursos[i].semestre << "  " << cursos[i].nombre << "  " << cursos[i].nrodehoras << "  " << cursos[i].creditos << "  " << cursos[i].cantMatri ;
			cout << "\n \n \n";
			
		}
	}
	

	
	
	system("pause");
	main();
}
              
              
              
              
       
