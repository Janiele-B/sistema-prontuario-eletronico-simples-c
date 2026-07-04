# 🏥 sistema-prontuário-eletrônico-simples-c

![Linguagem C]

Este é um sistema de **Prontuário Eletrônico** baseado em terminal desenvolvido inteiramente em **Linguagem C**. O projeto foi criado como parte da minha jornada acadêmica durante o **primeiro período da universidade**, servindo para consolidar conceitos fundamentais de lógica de programação e manipulação de estruturas de dados estáticas (vetores e matrizes de caracteres).

## 🚀 Funcionalidades

O sistema simula o gerenciamento de registros médicos de um hospital ou clínica por meio de um menu interativo:

1. **Cadastrar Prontuário**: Permite o registro de até 1000 pacientes contendo:
   - Dados Pessoais: Nome, CPF, Data de Nascimento, Idade, Sexo e Telefone.
   - Dados Médicos: Histórico médico, exames realizados, data do exame, resultado, observações e recomendações.
2. **Listar Todos os Prontuários**: Exibe em tela todos os registros armazenados na memória.
3. **Buscar Prontuário**: Localiza e exibe as informações detalhadas de um paciente específico através da busca por **CPF**.
4. **Alterar Prontuário**: Localiza o registro via CPF e permite atualizar os dados médicos e de contato diretamente.
5. **Remover Prontuário**: Exclui o registro do sistema reposicionando os elementos seguintes do vetor na memória.
6. **Sair**: Encerra a execução do programa com segurança.

## 🛠️ Conceitos Praticados

Por ser um projeto de primeiro período, o código aplica conceitos essenciais da programação estruturada:
- **Estruturas de Repetição**: Uso de laços `do-while` e `for` para controle do menu e buscas.
- **Estruturas Condicionais**: Implementação de `switch-case` para seleção de opções e `if/else` para validações.
- **Vetores e Matrizes (Arrays Multidimensionais)**: Armazenamento em memória de múltiplos dados textuais (Strings) e numéricos associados pelo mesmo índice.
- **Manipulação de Strings**: Utilização de funções da biblioteca `<string.h>` como `fgets()`, `strcspn()` para limpar o buffer de quebra de linha e `strcmp()` para comparação de CPFs.
- **Localização**: Uso da biblioteca `<locale.h>` para garantir a exibição correta de caracteres e acentuações em português.

## ⚙️ Como Executar o Projeto

Você precisará de um compilador GCC instalado no seu computador ou de uma IDE (como VS Code, Code::Blocks ou Dev-C++).

1. **Clone o repositório:**
   ```bash
   git clone https://github.com
   ```
2. **Navegue até a pasta do projeto:**
   ```bash
   cd sistema-prontuario-eletronico-simples-c
   ```
3. **Compile o código:**
   ```bash
   gcc -o prontuario principal.c
   ```
4. **Execute o programa:**
   - **Windows:**
     ```bash
     prontuario.exe
     ```
   - **Linux/Mac:**
     ```bash
     ./prontuario
     ```

## 📝 Notas de Evolução

*Este projeto representa os meus primeiros passos na programação. Ele armazena os dados temporariamente na memória RAM (arrays estáticos), o que significa que os dados são limpos ao fechar o programa. Pretendo evoluir este sistema futuramente adicionando **manipulação de arquivos (TXT/Binários)** para persistência de dados e **alocação dinâmica de memória**.*
