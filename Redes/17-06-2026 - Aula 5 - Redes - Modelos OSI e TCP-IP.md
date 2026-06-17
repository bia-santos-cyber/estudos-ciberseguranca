# 📘 AULA 5: Redes - Modelos OSI e TCP/IP
📅 Data: 17/06/2026
📂 Assunto: Camadas, funcionamento e segurança

---

## 📌 O que são?
São modelos que dividem o processo de comunicação em rede em **camadas**, com funções definidas.  
Servem para:
✅ Padronizar a comunicação entre sistemas diferentes.
✅ Facilitar a resolução de problemas.
✅ Entender **exatamente onde** aplicar segurança ou onde está a falha.

> 💡 **Analogia:** Como uma linha de montagem. Cada etapa (camada) adiciona algo ou transforma o produto, até chegar ao final.

---

## 🧱 1. Modelo OSI — O modelo teórico (7 Camadas)
É o modelo completo e de referência internacional. Organiza-se de cima para baixo:

### 1️⃣ Camada de APLICAÇÃO
👤 **Mais próxima do usuário**
✅ **Função:** Ponto de acesso aos serviços de rede. É onde os dados são gerados ou consumidos.
📡 **Protocolos:** HTTP, HTTPS, FTP, SSH, DNS, SMTP.
🛡️ **Segurança:** Criptografia, autenticação, validação de dados.

### 2️⃣ Camada de APRESENTAÇÃO
🔄 **Tradutor e Codificador**
✅ **Função:** Formata, traduz, comprime ou **CRIPTOGRAFA** os dados para que qualquer máquina entenda.
🛡️ **Segurança:** É aqui que o conteúdo é embaralhado/desembaralhado.

### 3️⃣ Camada de SESSÃO
🔌 **Gerenciador de Conexão**
✅ **Função:** Abre, controla, mantém e fecha a conversa entre origem e destino.

### 4️⃣ Camada de TRANSPORTE
🚚 **Entrega e Controle**
✅ **Função:** Controla como os dados são entregues, divide em pacotes, garante ordem e integridade. **A MAIS IMPORTANTE PARA NÓS.**
📡 **Elementos:** **TCP / UDP** e **NÚMEROS DE PORTA**.
🛡️ **Segurança:** Controle de fluxo, bloqueio de portas, prevenção de sobrecarga.

### 5️⃣ Camada de REDE
🗺️ **Endereçamento e Roteamento**
✅ **Função:** Define o endereço lógico (**IP**) e decide qual caminho os pacotes vão seguir pela rede.
📡 **Elementos:** **IP**, Roteadores.
🛡️ **Segurança:** Filtro de IPs, bloqueio de rotas, prevenção de falsificação.

### 6️⃣ Camada de ENLACE DE DADOS
🔗 **Comunicação Local**
✅ **Função:** Prepara os dados para o meio físico, controla erros na transmissão local e usa endereços físicos (**MAC**).
📡 **Elementos:** Placas de rede, Switches.

### 7️⃣ Camada FÍSICA
⚡ **Meio de Transmissão**
✅ **Função:** Transforma dados digitais em sinais (elétrico, luz, onda) e envia pelo meio.
📡 **Elementos:** Cabos, fibra, ondas de rádio, hardware.

---

## 🔨 2. Modelo TCP/IP — O modelo prático da Internet (4 Camadas)
É o modelo que realmente funciona no mundo real, mais enxuto, que junta camadas do OSI.

| Modelo TCP/IP | Equivale no Modelo OSI | Principais Funções / Protocolos |
|:---:|:---:|---|
| **APLICAÇÃO** | Camadas 1, 2 e 3 | HTTP, HTTPS, DNS, SSH, FTP |
| **TRANSPORTE** | Camada 4 | TCP, UDP, Portas |
| **INTERNET** | Camada 5 | IP, Roteamento |
| **ACESSO À REDE** | Camadas 6 e 7 | Endereço MAC, Cabos, Sinais |

---

## 🔄 3. O CICLO COMPLETO: Como os dados viajam

### ⬇️ Descendo (Origem → Rede)
1. **Aplicação:** Você pede um site → Dados criados.
2. **Apresentação:** Dados criptografados (HTTPS).
3. **Sessão:** Conexão iniciada.
4. **Transporte:** Dados divididos em pacotes; escolhe **Porta 443** e **TCP**.
5. **Rede:** Coloca o **IP de destino** no pacote.
6. **Enlace:** Prepara para enviar.
7. **Física:** Transforma em sinal e envia.

> 🚀 **VIAGEM:** Roteadores leem apenas o **IP** (Camada Internet) para decidir o caminho.

### ⬆️ Subindo (Destino → Usuário)
1. **Física:** Sinal recebido.
2. **Enlace:** Verifica integridade do sinal.
3. **Rede:** Confirma que o IP é o meu.
4. **Transporte:** Confirma que a **Porta 443** está aberta e remonta os pacotes.
5. **Aplicação:** Descriptografa e interpreta o pedido → Responde.

---

## 🛡️ 4. Segurança em Camadas
**Princípio: Segurança em Profundidade.**  
Proteja em todas as etapas, pois cada camada tem riscos diferentes:

- 📌 **Aplicação:** Ataques a sites, phishing, falhas em protocolos. *Proteção: Criptografia, filtros.*
- 📌 **Transporte:** Inundação de conexões, escaneamento de portas. *Proteção: Firewall, fechar portas.*
- 📌 **Rede:** Falsificação de IP, desvio de rota. *Proteção: Listas de bloqueio.*
- 📌 **Física:** Interceptação de cabo, acesso não autorizado. *Proteção: Segurança física.*

---

## ✅ Resumo Geral
1. **OSI:** 7 camadas → Teoria completa.
2. **TCP/IP:** 4 camadas → Prática real da internet.
3. **Para baixo:** Dado vira sinal.
4. **Para cima:** Sinal vira dado.
5. **Cada protocolo mora numa camada:** IP = Rede; TCP = Transporte; HTTP = Aplicação.

---

## ❓ Dúvidas / Observações
*(Anotar aqui o que não ficou claro ou pontos importantes)*