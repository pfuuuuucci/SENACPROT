# SENACPROT
Protótipo do Projeto Integrador do SENAC 


# RESUMO  

## Objetivo
O **Projeto Integrador do Grupo 01** teve, por objetivo, em sua primeira etapa, a modelagem de um sistema **Orientado a Objetos**, voltado à gestão de dados de uma grande universidade.
Utilizamos, como metodologia para a modelagem, o padrão **UML** e, neste documento, serão apresentados os seguintes artefatos:
- Diagrama de Casos de Uso
- Diagrama de Classes
- Descrição dos Cenários de Casos de Uso

## Resultados  
Os principais resultados esperados nessa etapa do projeto são:
- Representação visual dos Casos de Uso do cenário de cadastro de diferentes tipos de pessoas que vão interagir com o sistema;
- Representação visual das Classes a serem implementadas pelo sistema;
- Detalhamento dos cenários principal e alternativos, bem como pré-condição e pós-condição, de cada Caso de Uso relacionado; 

## Considerações Finais
O desenvolvimento deste projeto pretende explorar a metodologia UML e sua utilidade como ferramenta para a Documentação de Software, tanto no que diz respeito ao armazenamento do conhecimento quanto no tocante à especificação de requisitos.

**Palavras-chave:** UML, Diagrama, Classe, Cenário, Caso de Uso, Cadastro, Universidade, Aluno, Professor, Fornecedor.

## INTRODUÇÃO - Visão Geral do Produto 
Este documento reúne os elementos necessários para o desenvolvimento de um produto de software através do paradigma de Orientação a Objetos. Utilizando a metodologia UML, relacionamos aqui os Diagramas de Casos de Uso e de Classes, bem como os artefatos de Descrição de Casos de Uso referentes às funcionalidades descritas na proposta do projeto, compondo o restante da documentação.

## 1- DIAGRAMA DE CASO DE USO
![Image](https://github.com/user-attachments/assets/a8cf7252-936e-4ab6-868a-2720ea989df4)

## 1- DIAGRAMA DE CLASSES
![Image](https://github.com/user-attachments/assets/fa6fc242-94a5-4b0b-9cec-1894ee5d3058)

## Caso de Uso 1 – Fazer Login
**Ator Principal:** Usuário do Sistema  
**Pré-condições:**
- Usuário deve possuir credenciais de acesso
- Sistema deve estar operacional

## Cenário Principal:
1. Usuário acessa a tela de login
2. Usuário insere nome de usuário
3. Usuário insere senha
4. Sistema valida as credenciais
5. Sistema libera acesso ao usuário
   
## Cenários Alternativos: Cenário Alternativo 1 - Senha Incorreta:
1. Sistema identifica credenciais inválidas
2. Sistema exibe mensagem de erro
3. Usuário pode tentar novamente
4. Após 3 tentativas, conta é bloqueada
   
## Cenário Alternativo 2 - Recuperação de Senha:
1. Usuário seleciona opção "Esqueci minha senha"
2. Sistema solicita email de cadastro
3. Sistema envia link de recuperação
4. Usuário redefine senha
   
## Pós-condições:
• Usuário autenticado
• Acesso ao sistema liberado

## 4.2. Caso de Uso 2 – Verificar Senha
**Ator Principal:** Sistema 
**Pré-condições:**
• Credenciais fornecidas pelo usuário
• Banco de dados de usuários disponível

## Fluxo Principal:
1. Receber credenciais de login
2. Comparar com registros no banco de dados
3. Validar correspondência
4. Liberar ou negar acesso
   
## Fluxos Alternativos:
• Usuário não encontrado
• Senha incorreta
• Conta bloqueada

## Pós-condições:
• Acesso concedido ou negado

## 4.3. Caso de Uso 3 – Exibir Erro de Login
**Ator Principal:** Sistema
**Fluxo Principal:**
1. Identificar motivo da falha de login
2. Selecionar mensagem de erro apropriada
3. Exibir mensagem clara e objetiva
   
## Mensagens Possíveis:
• O nome de usuário fornecido não existe no banco de dados: **"Usuário não
encontrado"**
• A senha fornecida não corresponde à registrada para o nome de usuário fornecido:
**"Senha incorreta"**
• A conta de usuário está bloqueada devido às múltiplas tentativas mal sucedidas de
login ou outra razão administrativa: **"Conta bloqueada"**
• O usuário excedeu o limite de tentativas permitidas e a conta foi temporariamente
bloqueada: **"Número máximo de tentativas excedido"**

## 4.4. Caso de Uso 4 – Cadastrar Professor
**Ator Principal:** Usuário do Sistema
**Pré-condições:**
• Usuário autenticado
• Permissão para cadastro de docentes
• Dados pessoais e profissionais completos

## Cenário Principal:
1. Usuário do Sistema acessa módulo de cadastro de professores
2. Sistema carrega formulário de cadastro docente
3. Usuário do Sistema preenche informações pessoais
4. Usuário do Sistema registra formação acadêmica
5. Usuário do Sistema define departamento e regime de trabalho
6. Sistema valida todas as informações
7. Sistema gera matrícula funcional
8. Sistema salva registro do professor

## Cenários Alternativos: Cenário Alternativo 1 - Formação Incompleta:
1. Sistema identifica pendências na documentação acadêmica
2. Sistema sinaliza campos não preenchidos
3. Usuário do Sistema complementa informações
4. Processo de cadastro é reiniciado
   
## Cenário Alternativo 2 - Professor Já Existente:
1. Sistema detecta CPF já cadastrado
2. Sistema apresenta registro existente
3. Usuário do Sistema escolhe entre atualizar ou cancelar
4. Se optar por atualizar, inicia processo de modificação
   
## Pós-condições:
• Registro de professor criado
• Matrícula funcional gerada
• Dados salvos no sistema

## 4.5. Caso de Uso 5 – Cadastrar Aluno
**Ator Principal:** Usuário do Sistema
**Pré-condições:**
• Usuário autenticado
• Permissão para cadastro discente
• Documentação do aluno disponível

## Cenário Principal:
1. Usuário do Sistema acessa módulo de cadastro de alunos
2. Sistema apresenta formulário de matrícula
3. Usuário do Sistema preenche dados pessoais
4. Usuário do Sistema registra informações acadêmicas
5. Sistema verifica documentação
6. Sistema gera número de matrícula
7. Sistema confirma cadastro
8. Sistema vincula aluno ao curso
   
## Cenários Alternativos: Cenário Alternativo 1 - Documentação Pendente:
1. Sistema identifica documentos faltantes
2. Sistema bloqueia conclusão do cadastro
3. Sistema lista documentos necessários
4. Usuário do Sistema complementa documentação
   
## Cenário Alternativo 2 - Aluno com Restrições:
1. Sistema detecta pendências anteriores
2. Sistema sinaliza restrições de matrícula
3. Usuário do Sistema verifica histórico
4. Decisão sobre liberação ou bloqueio de cadastro
   
## Pós-condições:
• Registro de aluno criado
• Matrícula acadêmica gerada
• Vínculo com curso estabelecido

## 4.6. Caso de Uso 6 – Cadastrar Fornecedor
**Ator Principal:** Usuário do Sistema
**Pré-condições:**
• Usuário autenticado
• Permissão para cadastro de fornecedores
• Informações corporativas completas

## Cenário Principal:
1. Usuário do Sistema acessa módulo de fornecedores
2. Sistema carrega formulário de cadastro
3. Usuário do Sistema preenche dados da empresa
4. Usuário do Sistema registra produtos/serviços
5. Sistema valida informações corporativas
6. Sistema verifica certidões negativas
7. Sistema registra fornecedor
8. Sistema gera código de fornecedor
   
## Cenários Alternativos: Cenário Alternativo 1 - Certidões Vencidas:
1. Sistema identifica documentações desatualizadas
2. Sistema bloqueia cadastro completo
3. Sistema lista documentos a atualizar
4. Usuário do Sistema providencia documentação
   
## Cenário Alternativo 2 - Fornecedor Já Cadastrado:
1. Sistema detecta CNPJ existente
2. Sistema apresenta registro atual
3. Usuário do Sistema escolhe atualizar ou manter
4. Processo de atualização ou cancelamento
   
## Pós-condições:
• Registro de fornecedor criado
• Código de fornecedor gerado
• Dados salvos no sistema de gestão

## 4.7. Caso de Uso 7 – Cadastrar Pessoa Física
**Ator Principal:** Usuário do Sistema
**Pré-condições:**
• Usuário autenticado no sistema
• Possuir permissão de cadastro

## Cenário Principal:
1. Usuário do Sistema seleciona opção de cadastro
2. Sistema apresenta formulário de cadastro
3. Usuário do Sistema preenche dados pessoais
4. Sistema valida informações
5. Sistema salva cadastro
6. Sistema emite confirmação de cadastro
   
## Cenários Alternativos: Cenário Alternativo 1 - Dados Inválidos:
1. Sistema identifica inconsistências nos dados
2. Sistema destaca campos com erros
3. Usuário do Sistema corrige informações
4. Processo de cadastro é reiniciado
   
## Cenário Alternativo 2 - Cadastro Duplicado:
1. Sistema identifica CPF já cadastrado
2. Sistema bloqueia novo cadastro
3. Sistema apresenta mensagem de duplicidade
4. Usuário do Sistema decide atualizar ou cancelar
   
## Pós-condições:
• Registro de pessoa física criado
• Dados salvos no banco de dados

## 4.8. Caso de Uso 8 – Cadastrar Pessoa Jurídica
**Ator Principal:** Usuário do Sistema
**Pré-condições:**
• Usuário autenticado no sistema
• Possuir permissão de cadastro de pessoas jurídicas
• Acesso ao módulo de cadastro

## Cenário Principal:
1. Usuário do Sistema seleciona opção de cadastro de pessoa jurídica
2. Sistema apresenta formulário específico
3. Usuário do Sistema preenche dados da empresa
4. Sistema valida informações corporativas
5. Sistema verifica documentação
6. Sistema salva cadastro
7. Sistema emite comprovante de registro
   
## Cenários Alternativos: Cenário Alternativo 1 - Documentação Inválida:
1. Sistema detecta inconsistências no CNPJ
2. Sistema bloqueia cadastro
3. Sistema apresenta mensagens de erro específicas
4. Usuário do Sistema corrige informações
   
## Cenário Alternativo 2 - Empresa Já Cadastrada:
1. Sistema identifica CNPJ duplicado
2. Sistema apresenta opção de atualização
3. Usuário do Sistema decide entre atualizar ou cancelar
4. Se optar por atualizar, inicia processo de modificação
   
## Pós-condições:
• Registro de pessoa jurídica criado
• Dados salvos no banco de dados
• Log de cadastro gerado

## CONCLUSÃO
A Metodologia UML nos permite modelar e especificar os requisitos do nosso sistema. Ela tem
muitos benefícios, dentre os quais permitir planejar nosso projeto e validar requisitos com os
usuários, além de especificar tecnicamente o produto de software para os desenvolvedores. 

## PROTÓTIPO
O link para acessar o protótipo é: 
https://www.figma.com/proto/9MxE0q0XmLWvROaSTm3ntZ/Protótipo?node-id=0-1&t=N0vU6iAWRHE6AcbF-1 
