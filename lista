#include <stdio.h>
#include <stdlib.h> 
 	struct noDaLista
{
char titulo[51];
char autor[51];
int ano;
int quantidade;
noDaLista *prox;
};

typedef struct noDaLista Lista;
Lista *primeiro;
Lista *proximo;
int resp;

  void coletadados(){
   
    primeiro = (Lista*) malloc (sizeof(Lista));
    if(primeiro==NULL){
    	exit(1);
	}
	proximo=primeiro;
	while(1){
	
    printf("\nTitulo: ");
    scanf("%s", &proximo->titulo);
    printf("\nAutor: ");
    scanf("%s", &proximo->autor);
    printf("\nQuantidade: ");
    scanf("%d", &proximo->quantidade);
    printf("\nAno de Lancamento: ");
    scanf("%d", &proximo->ano);
    printf("CONTINUAR?: 1-sim 2-nao ->");
    scanf("%d",&resp);
    if(resp==1){
    	proximo->prox=(Lista*)malloc(sizeof(Lista));
    	proximo=proximo->prox;
	}
	else
	break;
}
}
void imprimir(){
	proximo->prox=NULL;
proximo=primeiro;
while (proximo!=NULL){
	printf("Titulo: %s\n",proximo->titulo);
	printf("Autor: %s\n",proximo->autor);
	printf("Quantidade: %d\n",proximo->quantidade);
	printf("Ano: %d\n",proximo->ano);
	printf("\n");
proximo=proximo->prox;
}
	
}
void somar(){
	Lista *aux=(Lista*)malloc(sizeof(Lista));
	int soma=0;
	aux=primeiro;
	while(aux!=NULL&&proximo->quantidade!=NULL){
		soma=aux->quantidade+soma;
		aux=aux->prox;
	}
	printf("%d",soma);
}


int main() {
coletadados();
imprimir();
somar();


	return 0;
}
