#include <stdio.h>
#include <stdlib.h>
 void Correr (int CH)
 {
     int cont = 0 ,cont2 = 0 , cont3 = 0;
     while(CH != '.')
    {
        while(CH != ' ' && CH != '.')
        {
            cont++;
            putchar(CH);
            CH = getchar();
        }
        if(cont < cont2)
        {
            cont3++;
            putchar('+');
        }
        putchar(CH);
        while(CH == ' ')
        {
            CH = getchar();
        }
    cont2 = cont;
    cont = 0;
    }
    printf("\n");
    printf("Existen %d palabras con cantidad de letras menores a la cantidad de letras existentes en la palabra anterior." , cont3);

 }

int main()
{
//Leer un texto carácter a carácter terminado en punto. Contar  cuántas palabras tiene menos letras que la
// palabra anterior. A las que tengan menos letras que la palabra anterior insertarles el signo +.
    int CH;
    printf("Ingrese una palabra u oracion terminada en un punto(.) \n");
    CH = getchar();
    Correr(CH);
}
