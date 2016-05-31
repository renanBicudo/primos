# primos
trabalho de arquitetura
#include <iostream>
#include <time.h>
#include <math.h>
using namespace std;

int dividePrimo(int num){
        int divide = 2;

        while(divide<=sqrt(num)){  //testa todos os numeros ate a raiz quadrada do numero testado
            if(num%divide==0){ //se tiver qlqr divisor para o numero, ele retorna zero, e nao incrementa o contador de primos
                return 0;
            }
            divide++;
        }
    return 1;// se nao tiver achado nenhum dividor ele retorna um e incrementa o contador
}

int main()
{
    int numero = 3,contadordePrimos = 1,numeroPrimo = 2;
    clock_t time = 0;
    time = clock();

    while(time<=60000){
            contadordePrimos + dividePrimo(numero);
            numeroPrimo = numero;
    }
        numero = numero+2;
        time = clock();
    cout<<"qtd total de primos: "<<contadordePrimos;
    cout<<endl<<"ultimo primo encontrado: "<<numeroPrimo;
}
