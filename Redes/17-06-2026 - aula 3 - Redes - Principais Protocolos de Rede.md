# 📘 AULA 3: Redes - Principais Protocolos de Rede
📅 Data: 17/06/2026
📂 Assunto: TCP/IP, HTTP, HTTPS, DNS, SSH e outros

---

## 📌 O que é um Protocolo?
São as **regras e padrões** que definem como os dispositivos devem se comunicar, enviar e receber dados.  
> 💡 Sem protocolo, cada máquina falaria uma língua diferente e ninguém se entenderia.

---

## 🧱 1. TCP/IP — A Base de Toda a Internet
É o conjunto de protocolos principal que faz a rede funcionar. É formado basicamente por dois elementos:

### 🔹 IP (Internet Protocol)
✅ **Função:** Endereçamento. Define para onde o dado vai e de onde ele vem.  
*(Já vimos detalhes na aula anterior)*

### 🔹 TCP (Transmission Control Protocol)
✅ **Função:** Controle e confiabilidade da entrega.

📋 **Como funciona:**
1. Estabelece conexão antes de enviar (**Three-Way Handshake**):
   - Máquina A → *"Você me ouve?"*
   - Máquina B → *"Ouço sim."*
   - Máquina A → *"Pronto, vou enviar."*
2. Divide dados em pacotes e numera cada um.
3. Confirma recebimento de cada pacote.
4. Se algo se perde, pede reenvio.

> 🛡️ **Segurança:** Garante que a informação chegue completa e correta. Alvo de ataques que visam sobrecarregar a conexão.

### 🔹 UDP (User Datagram Protocol)
✅ **Função:** Entrega rápida, **SEM garantia** de chegada ou ordem.
- Não faz verificação, não confirma recebimento.
- 📌 **Usado em:** Vídeos, jogos, transmissões ao vivo.
- ⚠️ **Risco:** Fácil de enviar dados falsos ou inundar a rede.

---

## 🔗 2. HTTP / HTTPS — Navegação Web
### 🔸 HTTP (HyperText Transfer Protocol)
- Protocolo que rege a navegação de sites.
- ❌ **Segurança:** Dados trafegam em **texto puro**. Qualquer um que intercepte o pacote lê tudo (senhas, dados, mensagens).
- Hoje considerado inseguro e obsoleto para uso geral.

### 🔸 HTTPS (HyperText Transfer Protocol Secure)
- ✅ **Versão SEGURA do HTTP.**
- **Criptografa** todo o conteúdo antes de enviar.
- Se interceptado, os dados aparecem embaralhados e ilegíveis.
- Identificado pelo **cadeado** no navegador e endereço `https://`.
- 🛡️ **OBRIGATÓRIO** em sites de banco, compras, governo ou qualquer serviço que envolva dados pessoais.

---

## 🌍 3. DNS — Sistema de Nomes de Domínio
> 📌 **A "Agenda Telefônica" da Internet**

### ✅ O que faz?
Os computadores usam **números (IP)**, mas nós usamos **nomes (ex: google.com)**.
O DNS serve para **TRADUZIR** o nome que você escreve para o número IP que a máquina entende.

🔄 **Fluxo:**
1. Você digita: `www.banco.com.br`
2. Consulta ao servidor DNS: *"Qual o IP desse nome?"*
3. Resposta: *"É 200.204.150.30"*
4. Conexão feita com o IP correto.

### ⚠️ PRINCIPAL RISCO: DNS Spoofing
- Invasor altera a resposta do servidor DNS.
- Você acha que está acessando o site oficial, mas é levado para um site falso criado pelo atacante.
- Resultado: Roubo de senhas e dados.

---

## 🔑 4. SSH — Acesso Remoto Seguro
✅ **Função:** Permite controlar um computador ou servidor de forma remota, como se estivesse na frente dele.

📌 **Características:**
- Toda comunicação é **criptografada** (senhas, comandos, telas).
- É a ferramenta principal de administração de servidores e estudos de Linux.
- Substituiu protocolos antigos e inseguros (como Telnet).

---

## 📁 5. Outros Protocolos Importantes

### 🔸 FTP / SFTP — Transferência de Arquivos
- **FTP:** Transfere arquivos. ❌ Inseguro (dados abertos).
- **SFTP:** Versão segura. ✅ Usa criptografia. **Padrão atual.**

### 🔸 SMTP / POP3 / IMAP — E-mail
- **SMTP:** Responsável por **ENVIAR** e-mails.
- **POP3 / IMAP:** Responsáveis por **RECEBER** e ler e-mails.
- ⚠️ Versões antigas não são criptografadas e vazam dados.

---

## 🔗 Relação com a Tríade da Segurança
*(Conceito da Aula 1)*

- 🔐 **Confidencialidade:** Garantida por protocolos seguros como **HTTPS, SSH, SFTP**. Protocolos como HTTP ou FTP NÃO garantem.
- 📝 **Integridade:** Protocolos confiáveis (TCP) asseguram que o dado não foi corrompido.
- 🚀 **Disponibilidade:** Ataques a DNS ou TCP podem derrubar o serviço e impedir o acesso.

---

## ✅ Resumo Geral
1. **TCP/IP:** Base da internet. TCP = confiável; UDP = rápido.
2. **HTTP:** Navegação aberta → **HTTPS = Navegação segura.**
3. **DNS:** Traduz nome para IP → **Ponto crítico de ataques.**
4. **SSH:** Controle remoto seguro.
5. **Regra de ouro:** Sempre prefira a versão **SEGURA** de qualquer protocolo.

---

## ❓ Dúvidas / Observações
*(Anotar aqui o que não ficou claro ou pontos importantes)*