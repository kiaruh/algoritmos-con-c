#include <stdio.h>
#include <stdlib.h>

void cargar(int mat[10][10],int dim)
{ int i,j;
    for (i=0;i<dim;i++)
    {
    for (j=0;j<dim;j++)
    {
        printf("ingrese numero ");
        scanf("%d",&mat[i][j]);
    }
    }
}

void mostrar(int mat[10][10],int dim)
{
    int i,j;
    for (i=0;i<dim;i++)
    {
        printf("\n");
        for (j=0;j<dim;j++)
        {
            printf("%d\t",mat[i][j]);
        }
        printf("\n");
    }
}

void comparar (int mat[10][10],int dim)
{
int i,j,sum=0,cont=0;
for(i=0; i<dim; i++)
{
for (j=0; j<dim; j++)
{
if (i==j)
{   sum+=mat[i][j];
}
if ((i>j) || (i<j))
cont=mat[j][i]+mat[i][j];

}
}

if ( cont==0 && sum==0)
 {
printf("es antisimetrica");
}
else
    printf("no es antisimetrica");
}


int main()
{
int mat[10][10],dim;

printf("ingrese dimension");
scanf("%d",&dim);
cargar(mat,dim);
mostrar(mat,dim);
comparar(mat,dim);
}
