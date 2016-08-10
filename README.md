# practica 
#include <iostream>
#include <stdio.h>

/* run this program using the console pauser or add your own getch, system("pause") or input loop */

int main(int argc, char** argv) {
	int i,n,num,mod=0,pos=0,imp=0,dom=0,mayor=-9999,menor=99999,band;
	float acum=0,cont=0,promedio,acumneg=0,positivos,porcentaje,negatotal,neg=0;
	printf("Total de numeros del conjunto:   ");
	scanf("%d",&n);
	for(i=0;i<n;i++){
		printf("\nNumero %d:    ",i+1);
		scanf("%d",&num);
		if(num>0){
			pos++;
		}
		if(num%2==0){
			mod++;
		}
		if(num%2!=0){
			imp++;
		}
		if(num<0){
			neg++;
			acumneg=acumneg+num;
			band=1;
		}
		if(num>=-30&&num<=30){
			dom++;
		}
		acum=acum+num;
		cont++;
		if(num<menor){
			menor=num;
		}
		if(num>mayor){
			mayor=num;
		}
		
	}
    printf("\nCantidad de numeros negativos: %0.0f",neg);
	printf("\nCantidad de numeros positivos: %d",pos);
	printf("\nCantidad de numeros pares: %d",mod);
	printf("\nCantidad de numeros impares: %d",imp);
	printf("\nCantidad de numeros entre [-30 y 30]:  %d",dom);
	printf("\nSuma total de numeros: %0.0f",acum);
	printf("\nContador de numeros: %0.0f",cont);
	promedio=acum/cont;
	negatotal=cont-neg;
	printf("\nEl promedio de numeros es: %.2f",promedio);
	printf("\nNumero mayor: %d",mayor);
	printf("\nNumero menor: %d",menor);
	printf("\nSuma total de numeros negativos: %0.0f",acumneg);
	porcentaje=(negatotal/acumneg)*100;
	printf("\nPorcentaje es: %.2f ",porcentaje);

	
	return 0;
	
	
	}
