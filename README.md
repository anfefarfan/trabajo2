//# trabajo2
//Trabajo 2 con punteros
	/*
	* Porgrama: Menu de ejecicios con punteros
	* Fecha: 4 de Septiembre del 2017
	* Elaborado por: Andres Felipe Farfan Hernandez
	*/
	
	#include <stdio.h>
	#include <conio.h>
	#include <stdlib.h>
	#include <string.h>
	#include <time.h>
	
	// Funcion principal del programa
	int main() 
	{ 
		int n;
		
		do
		{
			// Opciones del menu
			printf("************MENU************\n");
			printf("1.Arreglos con punteros\n");
			printf("2.Matrices con punteros\n");
			printf("3.Ejercicios con punteros\n");
			printf("4.Estructuras con punteros\n");
			printf("0.Salir\n");
			printf("*****************************\n");
			printf("Ingrese una opcion: ");
			scanf("%d",&n);
			
			switch(n)
			{
				char p;
			case 1:
			{
				
				do
				{
					// Opciones de arreglo con punteros
					fflush(stdin);  
					printf("************Arreglos con punteros************\n");
					printf("a.Declara un array de numéricos decimales e introduce en él cuatro elementos que sean...\n");
					printf("b.Pedirle al usuario que ingrese dos valores, y de acuerdo a los valores ingresado, mostrar en pantalla...\n");
					printf("c.Crear un arreglo de dimensión 4x4, y pedirle al usuario que ingrese 4 números. En la primera columna mostrar los números ingresados por el usuario...\n");
					printf("s.SALIR\n");
					printf("*************************************\n");
					printf("Ingrese una opcion: ");
					scanf("%c",&p);
					
					
					switch(p)
					{
					case 'a':
					{
						float a[]={32.583,11.239,45.781,22.237};
		                float *b;
		                b = a;
		                int i;
		
		                 for(i=0;i<4;i++)
		                   {
			                  printf("el valor del arreglo a es: %.3f",*(a+i) );
			                   printf("\n");
			
		                   }
						break;
						
					}
					
					case 'b':
					{
						 int i,n,m,k,j,band=0,band1=0;
		                 int matriz[100][100];
		                 int *p_matriz = &matriz[0][0];
		                 printf("ingrese el valor de las filas: ");
		                 scanf("%d",&n);
		                 printf("ingrese el valor de las columnas: ");
		                 scanf("%d",&m);
		
			            for(k=0;k<(m*n);k++)
			               {
				
			                    if(band==0&&band1==0)
			                       {
			                        	*(p_matriz+k)=0;
			                              band=1;
				                         band1=1;
				
			                       }
			
			                    else
			                       {
			                        	*(p_matriz+k)=1;
			                           	  band=0;
				                          band1=0;
			                       }
			               }
	
		               for(j=0;j<(n*m);j++)
	                    	{
			                  printf("%d",*(p_matriz+j));
			
		                    }	
		                printf("\n");
						break;
						
					}
					
					case 'c':
					{
							int a[4][4];
	                        int m,j,k;
	                        int *p_a = &a[0][0];
	
	
	
	                        for(k=0;k<=3;k++)
	                          {
		                         printf("ingresar los numeros: ");
		                         scanf("%d",&(*(p_a+k)));
		
	                          }
	                        int y=0;
	                        for(j=1;j<=(4*4);j+=4)
	                          {		
			                      *(p_a+j) = *(p_a+y) * *(p_a+y);
			                      *(p_a+j+1) =*(p_a+y) * *(p_a+y)* *(p_a+y);
			                      *(p_a+j+2) = *(p_a+y) * *(p_a+y)* *(p_a+y)* *(p_a+y);
			                        y+=4;
		
	                          }
	                        int l=0;
	                        for(m=0;m<(4*4);m++)
	                         {
		                         printf("mostrar datos ingresados %d",*(p_a+m) );
		                         printf("\n");
		                         printf("mostrar datos ingresados al cuadrado %d",*(p_a+m)+1 );
		                         printf("\n");
		                         printf("mostrar datos ingresados al cubo %d",*(p_a+m)+2 );
		                         printf("\n");
		                         printf("mostrar datos ingresados elevado a la cuarta %d",*(p_a+m)+3 );
		                         printf("\n");
		                         l+=4;
	                         }
						break;
						
					}
					case 's':
					{
						break;  
					}
					
					
					default:
					{
						printf("Error al digitar\n");
					}
					
					}
				}while(p != 's'); 
				break;
			}
			case 2:
			{
				
				do
				{
					// Opciones de matrices con punteros
					fflush(stdin);
					printf("************Matrices con Punteros************\n");
					printf("a.Crear una matriz de 3x3 donde el usuario completa sus valores desde el teclado y al final imprimir...\n");
					printf("b.Crear una matriz de 3x3 y llenarla de manera automática por el sistema\n");
					printf("c.Crear una matriz de 3x3 y llenarla de manera automática por el sistema con números primos.\n");
					printf("s.SALIR\n");
					printf("*************************************\n");
					printf("Ingrese una opcion: ");
					scanf("%c",&p);
					
					
					switch(p)
					{
					case 'a':
					{
							int a[3][3];
	                        int i,m,j,k,cont=0;
	                        int *p_a = &a[0][0];
	                        int *p_cont = &cont;
	                       //for(j=0;j<=2;j++)
	                        //{ 
		                    for(k=0;k<=(3*3)-1;k++)
		                      {
			
			                     printf("ingresar los numeros: ");
			                     scanf("%d",&(*(p_a+k)));
			                     //fflush(stdin);
			
		                      }
                         	//}
	
	                        for(i=0;i<=2;i++)
	                          { 
		                         for(m=0;m<=2;m++)
		                             {
			                              *p_cont = *((p_a+i)+m) + *p_cont;
			                               printf("conteo de posiciones: %d\n",*p_cont);
			
		                             }
	                          }
						    break;
						
					}
					
					case 'b':
					{
						int a[3][3];
		                int m,k;
		                int *p_a = &a[0][0];
		
		                srand(time(NULL));
		
	
			            for(k=0;k<=(3*3)-1;k++)
			              {
				             *(p_a+k) = 1+rand()%100;
				
			              }
	
			            for(m=0;m<=(3*3)-1;m++)
			            {
				           printf("%d\n",*(p_a+m));
			            }
						break;
						
					}
					
					case 'c':
					{
						int pri[8],i,a,j,p,k,m,h;
	                    int matriz[3][3];
	                    int *p_primo = &pri[0],*p_matriz = &matriz[0][0];
	
	                    srand(time(NULL));
	
	                    a=0; 
	
	                    for(j=0;j<=8;j++)
	                      {
		                     a=0;
		
		                     *(p_primo+j)=1+rand()%50;
		
		
		                         for(i=1;i<=*(p_primo+j);i++)
		                              {
			                             if(*(p_primo+j)%i==0)
		 	                                  {
				                                  a++;
			                                  }
		                              }                   
		
		
		                if(a==2)
		                   {
			                  printf("El número %d es primo\n",*(p_primo+j));
		
		                   }
		                else
		                  {
			                 j--;
		                  }
		
	                      }
	
	                   j=0;
	                   //for(p=0;p<=2;p++)
                       //{ 
		               for(k=0;k<=(3*3)-1;k++)
		                 {
			                 *(p_matriz+k) = *(p_primo+j);
			                  j+=1;
		                 }
	                   //}	
	
	                    j=0;
	                   //for(h=0;h<=2;h++)
	                   //{ 
		               for(m=0;m<=(3*3)-1;m++)
		                  {
			                 printf("Posicion %d = %d\n",j,*p_matriz);
			                 j++;
	                      }
	                   //}
						break;
					}
					case 's':
					{
						break;  
					}
					
					default:
					{
						printf("Error al digitar\n");
					}
					
					}
				}while(p != 's'); 
				break;
			}
			case 3:
			{
				
				do
				{
					// Ejercicio con punteros
					fflush(stdin);
					printf("************Ejercicio con Punteros************\n");
					printf("a.Comprobar si un número es par o impar, y senalar la posicion de memoria donde se esta guardando el número. Con punteros.\n");
					printf("b.Determinar si un número es primo o no, con puteros y además indicar en que posición de memoria se guardo el número\n");
					printf("c.Rellenar un array de 10 números, posteriormente utilizando punteros indicar cuales son números pares y su posición en memoria.\n");
					printf("d.Rellenar un arreglo con n números, posteriormente utilizando punteros determinar el menor elemento del vector\n");
					printf("e.Pedir su nombre al usuario y devolver el número de vocales que hay\n");
					printf("f.Pedir una cadena de caracteres (string) al usuario, e indicar cuantas veces aparece la vocal a,e,i,o,u; en la cadena de caracteres\n");
					printf("g.Hacer una estructura llamada alumno, en la cual se tendrán los siguientes Campos: Nombre, edad, promedio...\n");
					printf("h.Defina una estructura que indique el tiempo empleado por un ciclista en recorrer una etapa. La estructura debe tener...\n");
					printf("s.SALIR\n");
					printf("*************************************\n");
					printf("Ingrese una opcion: ");
					scanf("%c",&p);
					
					
					switch(p)
					{
					case 'a':
					{
						int x, *p_x;
		
		                printf("Digite un numero: "); 
		                scanf("%d",&x);
		
		                p_x = &x;  
		
		                if(*p_x%2==0){ 
			              printf("El numero %d es par\n",*p_x);
			              printf("La posicion de memoria es: %p\n",p_x); 
	                 	}
		                else{
			             printf("El numero %d es impar\n",*p_x);
			             printf("La posicion de memoria es: %p\n",p_x);	
		                }
						break;
						
					}
					
					case 'b':
					{
						int pri,i,a=0;
		                int *p_primo;
		
			            printf("Ingrese un numero: ");
			            scanf("&d",&pri);
			
			            p_primo = &pri;
	
					
		            	for(i=1;i<=*p_primo;i++)
			             {
				             if(*p_primo%i==0)
				                 {
					                a++;
				                 }
			             }
				
				         fflush(stdin);
			
			
			
			            if(a==2) 
			             {
			                printf("El número %d es primo\n",*p_primo);
			
			             }
			            else
			             {
			            	printf("El número %d no es primo\n",*p_primo);
		               	 }
						break;	
						
					}
					
					case 'c':
					{
						int x[10]={20,30,40,55,60,65,79,46,87,38},i, *p_x;
		
		                p_x = &x[0];  
		
		                for(i=0;i<10;i++)
		                 {
			                *(p_x+i) = x[i]; 
			
		                 }
		
		                for(i=0;i<10;i++)
		                 {
		
		                  if(*(p_x+i)%2==0){ 
			                 printf("El numero %d es par\n",*(p_x+i));
			                 printf("La posicion de memoria es: %p\n",(&p_x+i)); 
		                   }
		                 } 
						
						break;	
					}
					
					case 'd':
					{
							int x[100],i,n,*p_x;
		
		                    printf("Ingrese la cantidad de numeros: ", &n);
		                    scanf("%d",&n);
		
		                    p_x = &x[0];  
		
		                    for(i=0;i<n;i++)
		                     {
			                     printf("Por favor digitar los numeros: ", *(p_x+i));
			                     scanf("%d",(p_x+i));
		                     }
		                    int menor;
		
		                    for(i=0;i<n;i++)
		                    {
			
			                  if(menor > *(p_x+i)){ 
				
				               menor = *(p_x+i);
	
			                  }
		                    }
		
		                    printf("\nEl menor elemento es el numero %d \n",menor);
						    break;	
					}
					
					case 'e':
					{
						char nombre[30];
		                char *p_nom;
		                int cont=0; 
		
		                printf("Digite su nombre: ");
		                fgets(nombre,30,stdin);
		
		                p_nom = &nombre[0];
		
		                while(*p_nom){
			              switch(*p_nom){
			              case 'a':
			              case 'e':
			              case 'i':
			              case 'o':
			              case 'u':	cont++;
			            }
			            p_nom++;
			
		                }
		
		                printf("El numero de vocales son %d \n", cont);
						break;	
					}
					
					case 'f':
					{
						char nombre[50];
		                char *p_nomA,*p_nomE,*p_nomI,*p_nomO,*p_nomU;
		                int contA=0,contE=0,contI=0,contO=0,contU=0; 
		
		                printf("Digite su nombre: ");
		                fgets(nombre,50,stdin);
		                fflush(stdin);
		
		                p_nomA = &nombre[0];
		                p_nomE = &nombre[0];
		                p_nomI = &nombre[0];
		                p_nomO = &nombre[0];
		                p_nomU = &nombre[0];
		
		                while(*p_nomA){
			
			              switch(*p_nomA){
			                  case 'a':{
				                   contA++;
				
			                   }
			               }
			               p_nomA++;
			
		                 }
		
	                  	 while(*p_nomE){
			
			                  switch(*p_nomE){
			                     case 'e':{
				                      contE++;
			                       }
			                   }
			                   p_nomE++;
			
		                   }
		
		
		                 while(*p_nomI){
			
			                  switch(*p_nomI){
			                      case 'i':{
				                      contI++;
			                       }
			                   }
			                   p_nomI++;
		                   }
		
		                 while(*p_nomO){
			
			                   switch(*p_nomO){
			                      case 'o':{
				                     contO++;
			                       }
			                   }
			                   p_nomO++;
		                    }
		
		                  while(*p_nomU){
			
			                 switch(*p_nomU){
			                     case 'u':{
				                     contU++;
			 	
			                        }
			                       p_nomU++;
		                       }
	                        }
		
		                printf("El numero de veces que aparecer la vocal A es %d\n", contA);
		                printf("El numero de veces que aparecer la vocal E es %d\n", contE);
		                printf("El numero de veces que aparecer la vocal I es %d\n", contI);
		                printf("El numero de veces que aparecer la vocal O es %d\n", contO);
		                printf("El numero de veces que aparecer la vocal U es %d\n", contU);
						break;	
					}
					
					case 'g':
					{
						struct alumno{
	                      char nombre[30];
	                      int edad;
	                      float promedio;
                        }alumno[3],*p_alumno=alumno;
                        
                        int i;
	                    for(i=0;i<3;i++)
	                       {
		                       fflush(stdin);
		                       printf("Ingrese su nombre:");
		                       fgets((p_alumno+i)->nombre,30,stdin);
		                       printf("Ingrese su edad:");
		                       scanf("%d",&(p_alumno+i)->edad);
		                       printf("Ingrese su promedio:");
		                       scanf("%f",&(p_alumno+i)->promedio);
		 
	                       }
	
	                    float m=0.00;
	                    int unico;
	                      for(i=0;i<3;i++)
	                        {
		                        if((p_alumno+i)->promedio>m)
	                         	{
		 	                         m=(p_alumno+i)->promedio;
			                         unico=i;
		                        }
	                        }
	                    printf("El del alumno %s con edad de %d obtuvo el mejor promedio con un puntaje de %.2f\n",(p_alumno+unico)->nombre,(p_alumno+unico)->edad,m);
	
						break;	
					}
					
					case 'h':
					{
						struct recorrer{
	                      int hora;
	                      int minutos;
	                      int segundos;
                        }ciclistas[3], *p_ciclistas=ciclistas;
                        
                        for(int i=0;i<3;i++){
		
		                     printf("Ingrese la hora del ciclista # %d: ", i+1);
		                     scanf("%d",&(p_ciclistas+i)->hora);
	 	                     printf("Ingrese los minutos del ciclista # %d: ", i+1);
		                     scanf("%d", &(p_ciclistas+i)->minutos);
		                     printf("Ingrese horas del ciclista # %d: ", i+1);
		                     scanf("%d",&(p_ciclistas+i)->segundos);
		                     printf("\n");
	                       }
	
	                    int hor=0,min=0,seg=0;
	
	
	                    for(int i=0;i<3;i++){
		                     seg+=(p_ciclistas+i)->segundos;
		                     min+=(p_ciclistas+i)->minutos;
		                     hor+=(p_ciclistas+i)->hora;
		                     if (seg>=60){
			                     min+=1;
			                     seg-=60;
		                       }
		                     if(min>=60){
			                     hor+=1;
			                     min-=60;
		                       }
	                        }
	                    printf("El tiempo fue de:  %d Horas %d Minutos %d Segundos\n",hor,min,seg);
						break;	
					}
					
					
					case 's':
					{
						break;  
					}
					
					default:
					{
						printf("Error al digitar\n");
					}
					
					}
				}while(p != 's'); 
				break;
			}
			case 4:
			{
				do
				{   
					// Estructuras con punteros
					fflush(stdin);
					printf("************Estructuras con Punteros************\n");
					printf("a.Hacer una estructura llamada competidor, en la cual se tendrán los siguientes campos: Nombre, edad, sexo, club...\n");
					printf("b.Hacer una estructura llamada estudiante, en la cual se tendrán los siguientes Campos: Nombre, edad, Grado, promedio, pedir...\n");
					printf("c.Realizar un programa que lea un arreglo de estructuras los datos de N trabajadores de la empresa y que imprima los datos del trabajador...\n");
					printf("d.Hacer 2 estructuras una llamada promedio que tendrá los siguientes campos:nota1, nota2, nota3; y otro llamada...\n");
					printf("e.Hacer el mismo ejercicio anterior pero esta vez para N alumnos y que retorne el mejor promedio y menor promedio...\n");
					printf("f.Defina una estructura que sirva para representar a una persona. La estructura debe contener dos campos: el nombre de la persona...\n");
					printf("s.SALIR\n");
					printf("*************************************\n");
					printf("Ingrese una opcion: ");
					scanf("%c",&p);
					
					
					switch(p)
					{
					case 'a':
					{
						struct competidor
                         {
	                         char nombre[20];
	                         int edad;
                             char sexo[10];
	                         char club[20];
	
                         }deportista,*p_deportista=&deportista;
                          
                         char categoria[9];

	                     printf("ingresar el nombre :");
	                     fgets(p_deportista->nombre,20,stdin);
	                     printf("ingresar la edad :");
	                     scanf("%d",&p_deportista->edad);
	                     fflush(stdin);
	                     printf("ingresar Sexo :");
	                     fgets(p_deportista->sexo,10,stdin);
	                     fflush(stdin);
	                     printf("ingresar el Club :");
	                     fgets(p_deportista->club,20,stdin);
	                     fflush(stdin);
	
	
	                     if(p_deportista->edad<=15)
	                         {
		                         strcpy(categoria,"Juvenil");
	                         }
	                     if(p_deportista->edad <= 30 && p_deportista->edad > 15 )
	                         {
		                         strcpy(categoria,"Joven");
	                         }
	                     if(p_deportista->edad > 30)
	                         {
		                         strcpy(categoria,"Mayor");
	                         }
	
	                     fflush(stdin);
	                     printf("El competidor %s con edad de %d, de sexo %s, del club %s esta en la caetegoria %s", p_deportista->nombre,p_deportista->edad,p_deportista->sexo,p_deportista->club,categoria);
	
						break;
					}
					case 'b':
					{
						struct estudiante{
	                     char nombre[30];
	                     int edad;
	                     char grado[10];
	                     float promedio;
                        }alumno[3],*p_alumno=alumno;
                        
                        int i;
	                    for(i=0;i<3;i++)
	                      {
		                     fflush(stdin);
		                     printf("Ingrese su nombre:");
		                     fgets((p_alumno+i)->nombre,30,stdin);
		                     printf("Ingrese su edad:");
		                     scanf("%d",&(p_alumno+i)->edad);
		                     fflush(stdin);
		                     printf("Ingrese su grado:");
		                     fgets((p_alumno+i)->grado,10,stdin);
		                     printf("Ingrese su promedio:");
		                     scanf("%f",&(p_alumno+i)->promedio);
		                     printf("\n");
		
	                      }
	
	                    float m=0.00;
	                    int unico;
	                    for(i=0;i<3;i++)
	                      {
		                     if((p_alumno+i)->promedio>m)
		                         {
			                         m=(p_alumno+i)->promedio;
			                         unico=i;
		                         }
	                      }
	                     printf("El del alumno %s con edad de %d, que esta en el grado %s, obtuvo el mejor promedio con un puntaje de %.2f",(p_alumno+unico)->nombre,(p_alumno+unico)->edad,(p_alumno+unico)->grado,m);
	
						break;
					}
					
					case 'c':
					{ 
						struct datos_empleados
                         {
	                         char cedula[12];
	                         char nombre_y_apellido[50];
	                         int edad;
	                         long salario;
	
                         }trabajador[1000],*p_trabajador=trabajador;
                         
                         int i,x,j;
	                     int unico_mayor,unico_menor;
	
	                     printf("Cuantos trabajadores va a ingresar: ");
	                     scanf("%d",&x);
	
	                     long mayor = 000000, menor = 100000000;
	
	
	                     for(i=0;i<=x-1;i++)
	                         {
		                         fflush (stdin);
		                         printf("Ingrese la cedula del trabajador: ");
		                         fgets((p_trabajador+i)->cedula,12,stdin);
		                         printf("Ingrese el nombre del trabajador: ");
		                         fgets((p_trabajador+i)->nombre_y_apellido,50,stdin);
		                         fflush (stdin);
		                         printf("Ingrese la edad del trabajador: ");
		                         scanf("%d",&(p_trabajador+i)->edad);
		                         fflush (stdin);
		                         printf("Ingrese el salario del trabajador: ");
		                         scanf("%d",&(p_trabajador+i)->salario);
		                         fflush (stdin);
		                         printf("\n\n");
			
	                         }
	
	                     for(j=0;j<=x-1;j++)
	                         {
		                         if(mayor < (p_trabajador+j)->salario)
		                             {
			                             mayor = (p_trabajador+j)->salario;
			                             unico_mayor=j;
		                             }
		
		                         if(menor > (p_trabajador+j)->salario)
		                             {
			                             menor = (p_trabajador+j)->salario;
			                             unico_menor=j;
		                             }
		
	                         }
	                     printf("El trabajador %s con la cedula %s tiene una edad de %d, tiene el mayor salario con un valor de %d\n",(p_trabajador+unico_mayor)->nombre_y_apellido,(p_trabajador+unico_mayor)->cedula,(p_trabajador+unico_mayor)->edad,mayor);
                         printf("El trabajador %s con la cedula %s tiene una edad de %d, tiene el menor salario con un valor de %d\n",(p_trabajador+unico_menor)->nombre_y_apellido,(p_trabajador+unico_menor)->cedula,(p_trabajador+unico_menor)->edad,menor);

						break;
						
					}
					
					case 'd':
					{
						struct promedio
                         {
	                         float nota1;
	                         float nota2;
	                         float nota3;
	
                         };

                        struct alumno
                         {
	                         char nombre[20];
	                         char sexo[10];
	                         int edad;
	                         struct promedio persona;
                         }estu,*p_estu=&estu;
                         
                        float div=0;
	
	                    printf("Ingrese el Nombre de Alumno: ");
	                    fgets(p_estu->nombre,20,stdin);
	                    printf("Ingrese su Sexo: ");
	                    fgets(p_estu->sexo,10,stdin);
	                    fflush (stdin);
	                    printf("Ingrese su Edad: ");
	                    scanf("%d",&p_estu->edad);
	                    fflush (stdin);
	                    printf("Ingrese la nota 1: ");
	                    scanf("%f",&p_estu->persona.nota1);
	                    fflush (stdin);
	                    printf("Ingrese la nota 2: ");
	                    scanf("%f",&p_estu->persona.nota2);
	                    fflush (stdin);
	                    printf("Ingrese la nota 3: ");
	                    scanf("%f",&p_estu->persona.nota3);
	                    fflush (stdin);
	
	                    div = (p_estu->persona.nota1 + p_estu->persona.nota2 + p_estu->persona.nota3)/3;
	
	                    printf("El alumno %s con sexo %s tiene una edad de %d, con un promedio de %.2f",p_estu->nombre,p_estu->sexo,p_estu->edad,div);
	
						break;
						
					}
					
					case 'e':
					{
						struct promedio
                         {
	                         float nota1;
	                         float nota2;
	                         float nota3;
	
                         };

                        struct alumno
                         {
	                         char nombre[20];
	                         char sexo[10];
	                         int edad;
	                         struct promedio persona;
                         }estu[1000],*p_estu=estu;
                         
                         int i,x,j,k=0;
 	                     int unico_mayor,unico_menor;
	
	                     printf("Cuantos Alumnos va a ingresar: ");
	                     scanf("%d",&x);
	
	                     float div[1000];
	                     float mayor = 0.00, menor = 9.99;
	
	
	                     for(i=0;i<=x-1;i++)
	                         {
		                         fflush (stdin);
		                         printf("Ingrese el Nombre de Alumno: ");
		                         fgets((p_estu+i)->nombre,20,stdin);
		                         printf("Ingrese su Sexo: ");
		                         fgets((p_estu+i)->sexo,10,stdin);
		                         fflush (stdin);
		                         printf("Ingrese su Edad: ");
		                         scanf("%i",&(p_estu+i)->edad);
		                         fflush (stdin);
		                         printf("Ingrese la nota 1: ");
		                         scanf("%f",&(p_estu+i)->persona.nota1);
		                         fflush (stdin);
		                         printf("Ingrese la nota 2: ");
		                         scanf("%f",&(p_estu+i)->persona.nota2);
		                         fflush (stdin);
		                         printf("Ingrese la nota 3: ");
		                         scanf("%f",&(p_estu+i)->persona.nota3);
		                         fflush (stdin);
		
		                         div[i] = ((p_estu+i)->persona.nota1 + (p_estu+i)->persona.nota2 + (p_estu+i)->persona.nota3)/3;
		 	
                            }
	
	                     for(j=0;j<=x-1;j++)
	                         {
		                         if(mayor < div[j])
		                             {
			                             mayor = div[j];
			                             unico_mayor=j;
		                             }
		                         k=j;
		                         if(menor > div[k])
		                             {
			
			                             menor = div[j];
			                             unico_menor=k;
		                             }
		
	                         }
	                      printf("El alumno %s con sexo %s tiene una edad de %d, con el mayor promedio de %.2f\n",(p_estu+unico_mayor)->nombre,(p_estu+unico_mayor)->sexo,(p_estu+unico_mayor)->edad,div[unico_mayor]);
	                      printf("El alumno %s con sexo %s tiene una edad de %d, con el menor promedio de %.2f\n",(p_estu+unico_menor)->nombre,(p_estu+unico_menor)->sexo,(p_estu+unico_menor)->edad,div[unico_menor]);
	
						break;
						
					}
					
					case 'f':
					{
						
						break;
						
					}
					case 's':
					{
						break;  
					}
					
					default:
					{
						printf("Error al digitar\n");
						break;
					}
					break;
					}
				}while(p != 's'); 
				break;
			}
			
				
			case 0:
			{
				break;
			}
			default:
			{
				printf("Error al digitar\n");
				break;
			}
			}
			}
			
			
		 while(n != 0);
		
		return 0;
	}
	
	
