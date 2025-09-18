# Desafio: Sistema Bancário em Python V2

![Python](https://img.shields.io/badge/Python-3.x-blue?logo=python)
![Status](https://img.shields.io/badge/Status-Concluído-brightgreen)

Este projeto faz parte do desafio do curso de Python da DIO.  
Na **versão 2**, o sistema bancário foi **refatorado** para usar funções e passou a incluir **cadastro de usuários e contas correntes**, deixando a aplicação mais organizada, modular e próxima de um sistema real.

## 💡 Funcionalidades
- **[d] Depositar**: Adicionar valores à conta (somente valores positivos).  
- **[s] Sacar**: Retirar valores da conta, respeitando saldo, limite de saque e número máximo diário.  
- **[e] Extrato**: Visualizar todas as movimentações e o saldo atual.  
- **[nu] Novo Usuário**: Cadastrar um novo cliente, validando CPF para evitar duplicidade.  
- **[nc] Nova Conta**: Criar uma conta corrente vinculada a um usuário já cadastrado.  
- **[lc] Listar Contas**: Exibir todas as contas cadastradas no sistema.  
- **[q] Sair**: Encerra a aplicação.  

## ⚙️ Regras Implementadas
- Limite máximo por saque: **R$ 500,00**  
- Número máximo de saques diários: **3**  
- Histórico de movimentações armazenado em memória (extrato).  
- Um mesmo CPF **não pode ser cadastrado mais de uma vez**.  
- Cada conta é composta por: **agência (fixa: 0001), número sequencial da conta e usuário vinculado**.  
- Um usuário pode ter mais de uma conta, mas cada conta pertence a apenas um usuário.  

## 🛠 Tecnologias Utilizadas
- Python 3.x  

## 🚀 Como Executar
Clone o repositório, entre no diretório do projeto e execute o script principal:

git clone https://github.com/skynetsites/sistema-bancario-com-python-v2.git  
cd sistema-bancario-com-python-v2  
python sistema_bancario_v2.py  

## 📌 Exemplo de uso no terminal
```text
[d] Depositar
[s] Sacar
[e] Extrato
[nu] Novo Usuário
[nc] Nova Conta
[lc] Listar Contas
[q] Sair

=> nu
Informe o CPF (somente números): 12345678900
Informe o nome completo: Isaias Oliveira
Informe a data de nascimento (dd/mm/aaaa): 11/12/1980
Informe o endereço (Logradouro, Número - Bairro - cidade/UF): Rua João e Maria, 123 - Floresta - Fortaleza/CE
Usuário criado com sucesso!

=> nu
Informe o CPF (somente números): 12345678900
Já existe um usuário com esse CPF!

=> nc
Informe o CPF do usuário: 12345678900
Conta criada com sucesso!

=> lc
==============================
Agência: 0001
C/C: 1
Titular: Isaias Oliveira

=> d
Informe o valor do depósito: 1000
Depósito de R$ 1000.00 realizado com sucesso!

=> s
Informe o valor do saque: 300
Saque de R$ 300.00 realizado com sucesso!

=> s
Informe o valor do saque: 600
Operação falhou! O valor do saque excede o limite permitido.

=> e
================ EXTRATO =================
Depósito: R$ 1000.00
Saque: R$ 300.00

Saldo: R$ 700.00
==========================================

Desafio concluído!
Um projeto prático do curso DIO de Python para você explorar, testar e aprimorar suas habilidades.
