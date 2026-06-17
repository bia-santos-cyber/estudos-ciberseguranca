# 📘 AULA 4: Redes - Portas e Serviços
📅 Data: 17/06/2026
📂 Assunto: Funcionamento, números, segurança e ataques

---

## 📌 1. O que é uma Porta de Rede?
É um **número** (de 0 a 65535) que funciona como um **identificador de aplicação**.

> 💡 **Analogia do Prédio:**
> - **IP** = Endereço do prédio (chega no lugar certo).
> - **PORTA** = Número da sala/andar (chega na pessoa/setor certo).

✅ **Função:** Direciona os dados recebidos para o programa ou serviço correto que está rodando dentro do equipamento.

---

## 🧩 2. Faixas e Classificação das Portas
Elas são divididas em grupos conforme o uso:

### 🔹 Portas Bem Conhecidas → **0 a 1023**
✅ **As mais importantes e usadas.**
São portas padrão, reservadas para os serviços principais da internet.
**É OBRIGATÓRIO conhecer essas:**

| Porta | Protocolo | Serviço / Função | Nível de Segurança |
|:---:|:---:|---|:---:|
| **20 / 21** | FTP | Transferência de arquivos | ❌ INSEGURO |
| **22** | SSH | Acesso remoto e comando | ✅ SEGURO |
| **23** | Telnet | Acesso remoto antigo | ❌ PERIGOSO |
| **25** | SMTP | Envio de e-mails | ⚠️ Atenção |
| **53** | DNS | Tradução de nomes | ⚠️ CRÍTICO |
| **80** | HTTP | Navegação Web | ❌ INSEGURO |
| **110** | POP3 | Recebimento de e-mails | ❌ INSEGURO |
| **143** | IMAP | Recebimento de e-mails | ⚠️ Atenção |
| **443** | HTTPS | Navegação Web Segura | ✅ SEGURO |

---

### 🔹 Portas Registradas → **1024 a 49151**
- Usadas por softwares, aplicativos e serviços não oficiais.
- Ex: Bancos de dados, sistemas específicos, jogos.

### 🔹 Portas Dinâmicas → **49152 a 65535**
- Usadas temporariamente pelo seu computador para iniciar conexões de saída.
- Funcionam como "porta de saída" ou retorno.

---

## ⚙️ 3. O que é um Serviço?
É o **programa ou software** instalado na máquina que fica **"escutando"** em uma porta específica, esperando receber pedidos para responder.

> 📌 **Exemplo:**
> Se o serviço de site estiver ligado → ele escuta na porta 80 ou 443.
> Se o serviço de acesso remoto estiver ligado → ele escuta na porta 22.

### 🛡️ REGRA DE SEGURANÇA FUNDAMENTAL:
> **"Serviço ligado = Porta Aberta = Risco Potencial"**
> Se você não utiliza determinado serviço, **DESATIVE-O** e **FECHE A PORTA**.
> Quanto menos portas abertas, mais difícil é para o invasor entrar.

---

## 🕵️ 4. Ataques e Segurança: O Escaneamento de Portas
É a primeira etapa de quase todos os ataques em redes.

### 🔍 Como funciona?
1. Invasor descobre o IP do alvo.
2. Envia uma mensagem para cada porta (uma por uma) perguntando: *"Tem alguém aí?"*.
3. Se receber resposta: **PORTA ABERTA** → ele sabe exatamente o que tem ali.
4. Se não receber resposta: **PORTA FECHADA / BLOQUEADA**.

### ⚠️ O perigo:
Ao descobrir uma porta aberta, o atacante já sabe qual tecnologia usar para tentar invadir:
- Porta 21 aberta → Tentar roubar arquivos via FTP.
- Porta 22 aberta → Tentar adivinhar senha de acesso.
- Porta 80 aberta → Buscar falhas no site/aplicação web.

> 📌 **Conclusão:** Portas abertas são o **mapa do tesouro** para quem ataca.

---

## 🔗 Relação com a Tríade da Segurança
*(Conceito da Aula 1)*

- 🔐 **Confidencialidade:** Serviços em portas inseguras (ex: 21, 23, 80) vazam dados.
- 📝 **Integridade:** Serviços sem proteção permitem alteração de arquivos.
- 🚀 **Disponibilidade:** Envio excessivo de dados para uma porta pode travar o serviço.

---

## ✅ Resumo Geral
1. Porta = Número para encontrar o serviço certo.
2. Faixa 0-1023 = As mais importantes.
3. Serviço = Programa que escuta na porta.
4. Regra de ouro: **Feche o que não usa.**
5. Escaneamento: Invasor procura portas abertas para saber por onde atacar.

---

## ❓ Dúvidas / Observações
*(Anotar aqui o que não ficou claro ou pontos importantes)*