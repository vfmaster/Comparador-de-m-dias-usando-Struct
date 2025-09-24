# Comparador-de-medias-usando-Struct
Tarefa da faculdade de ciência da computação

#include <stdio.h>
#include <string.h>

int main(){
	
	int opcao;
	int maiorMedia;
	
	
	struct Avaliacao{
		float nota1;
		float nota2;
		int media;
		char disciplina[50];
	};
	
	
	do{
		printf("====Menu====\n");
		printf("1. Comparar nota\n");
		printf("2. Sair\n");
		struct Avaliacao primeiraDisciplina;
		struct Avaliacao segundaDisciplina;
	
		printf("Faca sua escolha: ");
		scanf("%d", &opcao);
		getchar();
		printf("Digite a primeira disciplina: ");
		fgets(primeiraDisciplina.disciplina, sizeof(primeiraDisciplina.disciplina), stdin);
		printf("Digite a segunda disciplina: ");
		fgets(segundaDisciplina.disciplina, sizeof(segundaDisciplina.disciplina), stdin);
		printf("Digite a nota1 da primeira disciplina: ");
		scanf("%f", &primeiraDisciplina.nota1);
		printf("Digite a nota2 da primeira disciplina: ");
		scanf("%f", &primeiraDisciplina.nota2);
		printf("Digite a nota1 da segunda disciplina: ");
		scanf("%f", &segundaDisciplina.nota1);
		printf("Digite a nota2 da segunda disciplina: ");
		scanf("%f", &segundaDisciplina.nota2);
	
	
		primeiraDisciplina.media = (primeiraDisciplina.nota1 + primeiraDisciplina.nota2) / 2;
		segundaDisciplina.media = (segundaDisciplina.nota1 + segundaDisciplina.nota2) / 2;
	
	if(primeiraDisciplina.media > segundaDisciplina.media){
		printf("A disciplina %s tem uma media maior que a disciplina %s", primeiraDisciplina.disciplina, segundaDisciplina.disciplina);
	}
	else if(primeiraDisciplina.media == segundaDisciplina.media){
		printf("As duas medias sao iguais\n");
	}else{
		printf("A disciplina %s tem uma media maior que a disciplina %s", segundaDisciplina.disciplina, primeiraDisciplina.disciplina);
	}
	
	
}while(opcao == 1);
	
	if(opcao ==2){
		printf("Saindo do jogo...");
	}
	
	
	return 0;
}
