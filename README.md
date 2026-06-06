# ATIVIDADE-INDIV-DUAL-TESTE-CAIXA-CINZA-COM-SUPABASE-E-POSTMAN
<img width="1763" height="793" alt="image" src="https://github.com/user-attachments/assets/73bb42f6-41aa-481d-aedf-6f149563b486" />

ALUNO: MURILO DE PAULA VIEIRA
RA: 224108

Este projeto apresenta a configuração e execução de testes de autenticação em uma API utilizando Supabase e Postman. A atividade foi desenvolvida com foco em testes caixa cinza, permitindo a validação do comportamento da API através do conhecimento parcial de sua estrutura, incluindo endpoints, métodos HTTP, headers, body JSON e respostas retornadas.

# Objetivo da Atividade

O objetivo desta atividade foi compreender e aplicar testes caixa cinza em APIs de autenticação utilizando ferramentas amplamente empregadas no mercado.

Durante a atividade foram realizadas as seguintes tarefas:

* Configuração de um ambiente de autenticação no Supabase;
* Criação de usuário para testes;
* Configuração do Postman Desktop;
* Criação e execução de requisições HTTP;
* Validação de respostas da API;
* Registro e documentação dos testes executados.

---

# Configuração do Supabase

## Criação do Projeto

Foi criada uma conta na plataforma Supabase e posteriormente um novo projeto para utilização durante os testes.

### Tipo de autenticação utilizada

Foi utilizada autenticação baseada em e-mail e senha.

### Criação do usuário

O usuário de teste foi criado através da área Authentication > Users do Supabase.

### Objetivo da configuração

A configuração realizada teve como objetivo disponibilizar um ambiente funcional para execução dos testes de autenticação utilizando credenciais válidas e inválidas.

## Dados Utilizados

### API URL

https://cswlbjcsvpdwsreivxtd.supabase.co

### API KEY

eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJpc3MiOiJzdXBhYmFzZSIsInJlZiI6ImNzd2xiamNzdnBkd3NyZWl2eHRkIiwicm9sZSI6ImFub24iLCJpYXQiOjE3ODA3NDkxNTYsImV4cCI6MjA5NjMyNTE1Nn0.oHjDVH6WhlYKTFy1JfCaYNRAnUfNCxJ8YsPBLeephNM

---

## Evidências

PRINT PROJETO CRIADO: <img width="1844" height="1027" alt="image" src="https://github.com/user-attachments/assets/ce125953-be33-4735-ab17-51d8551a9044" />
PAINEL PRINCIAPAL SUPABASE: <img width="1812" height="923" alt="image" src="https://github.com/user-attachments/assets/27123a79-489c-4b8b-aee8-9bc146e7367e" />
PRINT PROVIDERS: <img width="1850" height="962" alt="image" src="https://github.com/user-attachments/assets/f46e0c1b-697e-4968-97a3-9a9ecd00418e" />
### Coloque aqui o print do usuário criado

PRINT configurações api: <img width="1849" height="914" alt="image" src="https://github.com/user-attachments/assets/b9215364-183a-4635-9136-842c8f3b070e" />
PRINT IDENFICAÇÃO <img width="443" height="436" alt="image" src="https://github.com/user-attachments/assets/f4617352-2e4e-49da-aa05-b0c8de472cc2" />
PRINT SUPABASE CRIAÇÃO DE USUARIO <img width="1851" height="892" alt="image" src="https://github.com/user-attachments/assets/65ad1877-f54c-49ed-aebd-025f28f8ceb3" />

# Configuração do Postman

## Workspace

Foi criado um Workspace denominado "Supabase Authentication Tests" para organização das requisições da atividade.

## Environment

Foi criado um Environment denominado "Supabase Environment".

## Variáveis Configuradas

| Variável | Descrição              |
| -------- | ---------------------- |
| base_url | URL da API do Supabase |
| api_key  | Chave pública da API   |
| email    | Usuário criado         |
| password | Senha criada           |

## Finalidade das Variáveis

As variáveis permitem reutilização das informações em diferentes requisições sem necessidade de alterar manualmente os valores.

## Utilização do Postman

O Postman foi utilizado para criar, executar e validar requisições HTTP durante os testes de autenticação.

---

## Evidências

PRINT POSTMAN INSTALADO: <img width="1899" height="1023" alt="image" src="https://github.com/user-attachments/assets/12825c41-e8d0-4c93-9930-37e1a4bace79" />
PRINT WORKSPACE CRIADO: <img width="1896" height="1033" alt="image" src="https://github.com/user-attachments/assets/780ef95f-e841-4491-b91e-72c130b80cc9" />
PRINT ENVIRONMENT COM AS VARIAVEIS CRIADAS: <img width="1895" height="1025" alt="image" src="https://github.com/user-attachments/assets/27bc2eac-76e2-4b44-9329-d5fba679de5c" />
PRINT ORGANIZAÇÃO POSTMAN: <img width="1898" height="1030" alt="image" src="https://github.com/user-attachments/assets/ea5ed5a2-5fcb-420e-b07a-dd5e6f478746" />

---

# Configuração das Requisições

## Endpoint Utilizado

POST /auth/v1/token?grant_type=password

## Método HTTP Utilizado

POST

## Headers Utilizados

| Header        | Valor              |
| ------------- | ------------------ |
| apikey        | {{api_key}}        |
| Authorization | Bearer {{api_key}} |
| Content-Type  | application/json   |

## Body JSON Utilizado

```json
{
  "email": "{{email}}",
  "password": "{{password}}"
}
```

## Finalidade da Requisição

A requisição foi utilizada para autenticar usuários cadastrados no Supabase e obter um access token válido.

PRINT HEADERS POSTMAN: <img width="1901" height="1026" alt="image" src="https://github.com/user-attachments/assets/ea6eb4f8-f5b2-413e-9458-e135daa470dd" />
PRINT BODY POSTMAN: <img width="1915" height="606" alt="image" src="https://github.com/user-attachments/assets/70decb5c-3945-4fc2-96c0-bb5fe887871b" />
PRINT TESTE REALIZADO COM SUCESSO: <img width="1909" height="1036" alt="image" src="https://github.com/user-attachments/assets/c20a5d92-26e0-4ac9-bd35-c8f4e9789fd9" />


# Execução dos Testes

Foram realizados testes caixa cinza para validação da autenticação da API.

## Tabela de Cenários

| Cenário               | Entrada Utilizada        | Resultado Esperado        | Resultado Obtido            | Status |
| --------------------- | ------------------------ | ------------------------- | --------------------------- | ------ |
| Login válido          | Usuário e senha corretos | Status 200 + access token | Login realizado com sucesso | OK     |
| Senha incorreta       | Senha inválida           | Erro autenticação         | Erro retornado              | OK     |
| Usuário inexistente   | E-mail não cadastrado    | Acesso negado             | Acesso negado               | OK     |
| Campos vazios         | Campos vazios            | Erro validação            | Erro retornado              | OK     |
| Credenciais inválidas | Dados inválidos          | Falha autenticação        | Falha autenticação          | OK     |

## Resultados Obtidos

Todos os cenários obrigatórios foram executados e os resultados retornados pela API corresponderam ao comportamento esperado.

## Erros Encontrados

Durante os testes foram observadas mensagens de erro relacionadas à autenticação quando credenciais inválidas foram utilizadas, demonstrando que o mecanismo de segurança estava funcionando corretamente.

---

## Evidências

PRINT Teste SENHA ERRADA: <img width="1919" height="1079" alt="image" src="https://github.com/user-attachments/assets/b75c01b5-e59a-44f9-9149-a874d0c8b47e" />
PRINT TESTE USUARIO ERRADO <img width="1903" height="586" alt="image" src="https://github.com/user-attachments/assets/80ef88dc-956d-4356-97f4-ed20cbbc2fda" />
PRINT TESTE EMAIL E SENHA VAZIO <img width="1905" height="625" alt="image" src="https://github.com/user-attachments/assets/7d9f376d-a3fc-4417-b151-978dda90613f" />
PRINT TESTE EMAIL VAZIO <img width="1906" height="553" alt="image" src="https://github.com/user-attachments/assets/5b3087ec-431c-4de3-9afa-801ab40d366b" />


# Registro dos Testes

Os testes executados foram registrados em uma planilha contendo todos os cenários realizados.

## Como os testes foram registrados

Cada teste recebeu um identificador único contendo cenário, entrada utilizada, resultado esperado, resultado obtido, status e observações.

## Importância da documentação dos testes

A documentação permite rastreabilidade dos testes realizados, facilita futuras validações e auxilia na identificação de possíveis falhas.

## Falhas Identificadas

Não foram identificadas falhas no processo de autenticação durante os testes executados.

---

## Evidências

Print planilha preenchida: <img width="1141" height="140" alt="image" src="https://github.com/user-attachments/assets/9ed444f2-b5ed-402b-9bef-3d61703eb418" />

---

# Resultados Obtidos

Os testes demonstraram que a autenticação implementada pelo Supabase respondeu adequadamente aos diferentes cenários executados.

Foi possível validar:

* Geração de access token;
* Validação de credenciais;
* Tratamento de erros;
* Retorno correto de códigos HTTP;
* Funcionamento da autenticação baseada em e-mail e senha.

---

# Conclusão
 Os teses foram realizados com sucesso no final dos testes, a principal dificuldade que encontrei ao realizar eles foi entender como utilizar o SUPABASE pois foi a minha primeiravez utilizado, porem achei uma boa plataforma.
 Quanto aplicação de caixa cinza, graças ao testes compreendi melhor como aplicar o conceito e quando aplicar.
