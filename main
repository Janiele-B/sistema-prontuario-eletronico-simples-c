#include <stdio.h>
#include <string.h>
#include <locale.h>

int main() {

    setlocale(LC_ALL, "Portuguese");
    // Declarando as variáveis
    char nome[1000][30], data_nasc[1000][15];
    char busca[20], CPF[1000][20]; // formato xxx.xxx.xxx-xx
    int idade[1000], resposta, i = 0, Pacientes = 0, encontrado, j;
    char Sexo[1000]; // M ou F
    char contato[1000][20]; // formato (xx)xxxxx-xxxx
    char historico[1000][100], exames[1000][100], data[1000][15]; 
    char resultado[1000][100], observacao[1000][100], recomendacao[1000][100], continuar;

    do {
        printf("\n------------------------------\n");
        printf("PRONTUARIO ELETRONICO\n");
        printf("------------------------------\n");
        printf("MENU:\n");
        printf("1- Cadastrar um novo Prontuario\n");
        printf("2- Listar todos os Prontuarios\n");
        printf("3- Buscar um Prontuario\n");
        printf("4- Alterar Prontuario existente\n");
        printf("5- Remover Prontuario\n");
        printf("6- Sair\n");
        printf("------------------------------\n");

        printf("\nO que deseja fazer no sistema? ");
        scanf("%d", &resposta);
        getchar(); // Limpar o buffer do teclado

        switch (resposta) {
            case 1:
                do {
                    printf("------------------------------\n");
                    printf("\nCadastro de novo prontuario\n");
                    printf("------------------------------\n");

                    printf("Nome do Paciente: ");
                    fgets(nome[Pacientes], sizeof(nome[Pacientes]), stdin);
                    nome[Pacientes][strcspn(nome[Pacientes], "\n")] = '\0';

                    printf("CPF (xxx.xxx.xxx-xx): ");
                    fgets(CPF[Pacientes], sizeof(CPF[Pacientes]), stdin);
                    CPF[Pacientes][strcspn(CPF[Pacientes], "\n")] = '\0';

                    printf("Data de nascimento (dd/mm/aaaa): ");
                    fgets(data_nasc[Pacientes], sizeof(data_nasc[Pacientes]), stdin);
                    data_nasc[Pacientes][strcspn(data_nasc[Pacientes], "\n")] = '\0';

                    printf("Idade: ");
                    scanf("%d", &idade[Pacientes]);
                    getchar();

                    printf("Sexo (M/F): ");
                    scanf("%c", &Sexo[Pacientes]);
                    getchar();

                    printf("Telefone para contato (xx)xxxxx-xxxx: ");
                    fgets(contato[Pacientes], sizeof(contato[Pacientes]), stdin);
                    contato[Pacientes][strcspn(contato[Pacientes], "\n")] = '\0';

                    printf("Historico medico: ");
                    fgets(historico[Pacientes], sizeof(historico[Pacientes]), stdin);
                    historico[Pacientes][strcspn(historico[Pacientes], "\n")] = '\0';

                    printf("Exames realizados: ");
                    fgets(exames[Pacientes], sizeof(exames[Pacientes]), stdin);
                    exames[Pacientes][strcspn(exames[Pacientes], "\n")] = '\0';

                    printf("Data da realizacao dos exames: ");
                    fgets(data[Pacientes], sizeof(data[Pacientes]), stdin);
                    data[Pacientes][strcspn(data[Pacientes], "\n")] = '\0';

                    printf("Resultado dos exames: ");
                    fgets(resultado[Pacientes], sizeof(resultado[Pacientes]), stdin);
                    resultado[Pacientes][strcspn(resultado[Pacientes], "\n")] = '\0';

                    printf("Observacao: ");
                    fgets(observacao[Pacientes], sizeof(observacao[Pacientes]), stdin);
                    observacao[Pacientes][strcspn(observacao[Pacientes], "\n")] = '\0';

                    printf("Recomendacao medica: ");
                    fgets(recomendacao[Pacientes], sizeof(recomendacao[Pacientes]), stdin);
                    recomendacao[Pacientes][strcspn(recomendacao[Pacientes], "\n")] = '\0';

                    Pacientes++;
                    printf("\nProntuário cadastrado com sucesso!\n");

                    printf("\nDeseja cadastrar um novo prontuario? (S/N): ");
                    scanf(" %c", &continuar);
                    getchar();
                } while(continuar == 'S' || continuar == 's');
                break;

            case 2:
                printf("------------------------------\n");
                printf("\nLISTA DE PRONTUARIOS:\n");
                printf("------------------------------\n");
                if (Pacientes == 0) {
                    printf("Nenhum prontuario cadastrado.\n");
                }
                for (i = 0; i < Pacientes; i++) {
                    printf("\n------------------------------\n");
                    printf("Nome do paciente: %s\n", nome[i]);
                    printf("CPF: %s\n", CPF[i]);
                    printf("Data de nascimento: %s\n", data_nasc[i]);
                    printf("Idade: %d\n", idade[i]);
                    printf("Sexo: %c\n", Sexo[i]);
                    printf("Contato: %s\n", contato[i]);
                    printf("Historico medico: %s\n", historico[i]);
                    printf("Exames realizados: %s\n", exames[i]);
                    printf("Data da realizacao dos exames: %s\n", data[i]);
                    printf("Resultado dos exames: %s\n", resultado[i]);
                    printf("Observacao: %s\n", observacao[i]);
                    printf("Recomendacao medica: %s\n", recomendacao[i]);
                    printf("------------------------------\n");
                }
                break;

            case 3:
                do {
                    printf("------------------------------\n");
                    printf("\nBUSCANDO PRONTUARIO\n");
                    printf("------------------------------\n");
                    encontrado = 0;
        
                    printf("Digite o CPF do paciente que deseja encontrar (xxx.xxx.xxx-xx): ");
                    fgets(busca, sizeof(busca), stdin);
                    busca[strcspn(busca, "\n")] = '\0';

                    for(i = 0; i < Pacientes; i++) {  
                        if(strcmp(busca, CPF[i]) == 0) {
                            printf("\n------------------------------\n");
                            printf("Nome do paciente: %s\n", nome[i]);
                            printf("CPF: %s\n", CPF[i]);
                            printf("Data de nascimento: %s\n", data_nasc[i]);
                            printf("Idade: %d\n", idade[i]);
                            printf("Sexo: %c\n", Sexo[i]);
                            printf("Contato: %s\n", contato[i]);
                            printf("Historico medico: %s\n", historico[i]);
                            printf("Exames realizados: %s\n", exames[i]);
                            printf("Data da realizacao dos exames: %s\n", data[i]);
                            printf("Resultado dos exames: %s\n", resultado[i]);
                            printf("Observacao: %s\n", observacao[i]);
                            printf("Recomendacao medica: %s\n", recomendacao[i]);
                            printf("------------------------------\n");
                            encontrado = 1;
                        }
                    }
                    if(encontrado == 0) {
                        printf("Prontuario nao cadastrado no sistema!\n");
                    }
                    printf("\nDeseja buscar outro prontuario? (S/N): ");
                    scanf(" %c", &continuar);
                    getchar();
                } while(continuar == 'S' || continuar == 's');
                break;

            case 4:
                // ALTERAR UM PRONTUÁRIO EXISTENTE
                do {
                    printf("------------------------------\n");
                    printf("\nALTERANDO PRONTUARIO\n");
                    printf("------------------------------\n");
                    encontrado = 0;

                    printf("Digite o CPF do paciente que deseja alterar (xxx.xxx.xxx-xx): ");
                    fgets(busca, sizeof(busca), stdin);
                    busca[strcspn(busca, "\n")] = '\0';

                    for(i = 0; i < Pacientes; i++) {
                        if(strcmp(busca, CPF[i]) == 0) {
                            encontrado = 1;
                            printf("\nPaciente encontrado: %s. Insira os novos dados:\n", nome[i]);
                            
                            printf("Novo Nome: ");
                            fgets(nome[i], sizeof(nome[i]), stdin);
                            nome[i][strcspn(nome[i], "\n")] = '\0';

                            printf("Nova Idade: ");
                            scanf("%d", &idade[i]);
                            getchar();

                            printf("Novo Telefone: ");
                            fgets(contato[i], sizeof(contato[i]), stdin);
                            contato[i][strcspn(contato[i], "\n")] = '\0';

                            printf("Novo Historico medico: ");
                            fgets(historico[i], sizeof(historico[i]), stdin);
                            historico[i][strcspn(historico[i], "\n")] = '\0';

                            printf("Nova Recomendacao medica: ");
                            fgets(recomendacao[i], sizeof(recomendacao[i]), stdin);
                            recomendacao[i][strcspn(recomendacao[i], "\n")] = '\0';

                            printf("\nProntuario alterado com sucesso!\n");
                        }
                    }
                    if(!encontrado) {
                        printf("Prontuario nao encontrado para alteracao.\n");
                    }
                    printf("\nDeseja alterar outro prontuario? (S/N): ");
                    scanf(" %c", &continuar);
                    getchar();
                } while(continuar == 'S' || continuar == 's');
                break;

            case 5:
                // REMOVER UM PRONTUÁRIO
                do {
                    printf("------------------------------\n");
                    printf("\nREMOVER PRONTUARIO\n");
                    printf("------------------------------\n");
                    encontrado = 0;

                    printf("Digite o CPF do paciente que deseja remover (xxx.xxx.xxx-xx): ");
                    fgets(busca, sizeof(busca), stdin);
                    busca[strcspn(busca, "\n")] = '\0';

                    for(i = 0; i < Pacientes; i++) {
                        if(strcmp(busca, CPF[i]) == 0) {
                            encontrado = 1;
                            
                            // Move todos os elementos seguintes uma posição para trás
                            for(j = i; j < Pacientes - 1; j++) {
                                strcpy(nome[j], nome[j+1]);
                                strcpy(CPF[j], CPF[j+1]);
                                strcpy(data_nasc[j], data_nasc[j+1]);
                                idade[j] = idade[j+1];
                                Sexo[j] = Sexo[j+1];
                                strcpy(contato[j], contato[j+1]);
                                strcpy(historico[j], historico[j+1]);
                                strcpy(exames[j], exames[j+1]);
                                strcpy(data[j], data[j+1]);
                                strcpy(resultado[j], resultado[j+1]);
                                strcpy(observacao[j], observacao[j+1]);
                                strcpy(recomendacao[j], recomendacao[j+1]);
                            }
                            
                            // Diminui a quantidade total de pacientes cadastrados
                            Pacientes--;
                            printf("\nProntuario removido com sucesso!\n");
                            break; 
                        }
                    }
                    if(!encontrado) {
                        printf("Prontuario nao encontrado para remocao.\n");
                    }
                    printf("\nDeseja remover outro prontuario? (S/N): ");
                    scanf(" %c", &continuar);
                    getchar();
                } while(continuar == 'S' || continuar == 's');
                break;

            case 6:
                printf("\nSaindo do sistema... Obrigado!\n");
                break;

            default:
                printf("\nOpcao invalida! Tente novamente.\n");
        }

    } while (resposta != 6);

    return 0;
}
