# 📘 AULA 2: Redes de Computadores - Conceitos Básicos
📅 Data: 17/06/2026
📂 Assunto: Fundamentos, conexão e funcionamento

---

## 📌 1. O que é Rede de Computadores?
É um conjunto de **dois ou mais dispositivos conectados** entre si, capazes de trocar informações, arquivos, mensagens e compartilhar recursos.

> 💡 **Explicação simples:**
> Funciona como uma conversa entre pessoas, mas feita por máquinas. A conexão pode ser por **fio** (cabo, fibra) ou **sem fio** (Wi-Fi, 4G/5G, Bluetooth).

✅ **Objetivo principal:** Compartilhar dados e serviços.

---

## 🧩 2. Componentes essenciais de uma rede
Para uma rede funcionar, existem 4 elementos obrigatórios:

1. 📱 **Dispositivos (Nós):** Aparelhos que se conectam.  
   *Exemplo:* Computador, celular, roteador, servidor, impressora.

2. 🛤️ **Meio de transmissão:** O caminho por onde os dados passam.  
   *Exemplo:* Cabo de rede, fibra óptica, ondas de rádio (ar).

3. 📜 **Protocolos:** São as **regras de comunicação**.  
   Definem como os dados são enviados, como são entendidos e como chegam ao destino. *Sem protocolo, não há comunicação.*

4. 📄 **Dados:** A informação que está sendo trafegada (texto, imagem, vídeo, comando).

---

## 📍 3. Endereçamento: Como encontrar as máquinas?
Assim como uma carta precisa de endereço, uma máquina precisa de um número único para ser localizada. Esse número é o **ENDEREÇO IP**.

### 🔹 O que é IP?
- **IP = Internet Protocol**
- É a identificação única de cada dispositivo na rede.
- Formato: `xxx.xxx.xxx.xxx` (Ex: `192.168.0.25`)

### 🔹 Tipos de IP
- **🔒 IP Privado:** Usado dentro da sua casa ou empresa. Apenas dispositivos da mesma rede enxergam esses números.
  *Ex:* `192.168.0.10`
- **🌐 IP Público:** É o endereço da sua conexão na internet. É o número que todo mundo fora da sua rede vê. Todos os aparelhos da sua casa compartilham o mesmo IP público.

---

## 🗺️ 4. Classificação por alcance
Dividimos as redes conforme o tamanho da área que ela cobre:

### 🏠 LAN (Rede de Área Local)
- Pequena distância: Casa, escritório, escola.
- Conecta máquinas próximas.
- *Ex:* Sua rede Wi-Fi doméstica.

### 🏢 MAN (Rede de Área Metropolitana)
- Cobre uma cidade ou região.
- *Ex:* Conexão entre filiais de uma empresa na mesma cidade.

### 🌍 WAN (Rede de Área Ampla)
- Cobre países, continentes ou o mundo inteiro.
- **A INTERNET é a maior WAN existente.**

---

## 📦 5. Como os dados viajam? (Conceito de Pacote)
Nenhuma informação grande é enviada de uma vez só. A rede **quebra tudo em pequenos pedaços**, chamados de **PACOTES**.

Cada pacote tem:
1. 📋 **Cabeçalho:** Informações de controle → Endereço de ORIGEM e endereço de DESTINO.
2. 📄 **Dados:** Parte da informação real (um pedaço da foto, um trecho do texto).

Na chegada, todos os pacotes são reunidos novamente para formar o conteúdo completo.

> ⚠️ **PONTO CHAVE PARA SEGURANÇA:**
> Como os dados viajam em pacotes por caminhos diferentes, **a segurança entra para garantir que ninguém leia, altere ou roube esses pacotes no caminho**.

---

## 🚦 6. O que é um Roteador?
É o dispositivo principal que:
- Liga a sua rede interna (LAN) com a rede externa (INTERNET);
- Funciona como um **guia de tráfego**: decide por qual caminho enviar os dados para chegar ao destino;
- Faz a "tradução" entre o seu IP privado e o IP público.

---

## 🔗 Relação com a Tríade da Segurança
*(Conceito da Aula 1)*
- 🔐 **Confidencialidade:** Pacotes criptografados → só o destinatário lê.
- 📝 **Integridade:** Pacotes não podem ser alterados no caminho.
- 🚀 **Disponibilidade:** A rede e os equipamentos devem estar funcionando para os dados passarem.

---

## ✅ Resumo Geral
1. Rede = Conexão para troca de dados;
2. IP = Endereço único de cada máquina;
3. Dados são divididos em **pacotes** para viajar;
4. Roteador = O caminho que liga você à internet;
5. Segurança = Proteger essa comunicação.

---

## ❓ Dúvidas / Observações
*(Anotar aqui o que não ficou claro ou pontos importantes)*