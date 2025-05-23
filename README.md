# 🤖 Solana Price Alert Bot — SOL/USDC Telegram Monitor

Um bot de Telegram inteligente e completo feito com **Python 3.10+**, que usa a **API da Binance** para monitorar em tempo real o preço do par **SOL/USDC** e notificar o usuário por mensagens no Telegram com alertas personalizados.

> 📌 Ideal para quem opera com Liquidity Pools e deseja ser notificado quando o preço estiver dentro de ranges estratégicos.

---

## 📌 Funcionalidades

✅ Menu com botões interativos (`/start`)
📈 Ver preço atual da SOL/USDC
🔔 Criar alertas de preço (ex: "me avise se SOL > $150")
📏 Criar alertas por faixa de preço (range: entre $142.20 e $148.00)
🕰️ Registrar tempo dentro de um range (entrada, saída, duração)
📋 Listar todos os alertas
❌ Remover alertas específicos
🔕 Ativar ou desativar alertas temporariamente
💾 Dados salvos localmente no `alerts.json` (persistência)
🔁 Monitoramento contínuo em background (checa o preço a cada X segundos)
🧠 Mensagens amigáveis com validações (ex: "Digite um valor válido")

---

## 🖼️ Exemplo do Menu Interativo

📈 Ver Preço da SOL
➕ Adicionar Alerta de Preço
📏 Adicionar Alerta de Faixa (Range)
📋 Meus Alertas
❌ Remover Alerta
🔕 Ativar/Desativar Alertas
🕰️ Ver Histórico de Range

yaml
Copy
Edit

---

## ⚙️ Instalação

### 1. Clone o repositório

```bash
git clone https://github.com/seu-usuario/solana-price-alert-bot.git
cd solana-price-alert-bot
2. Instale as dependências
bash
Copy
Edit
pip install -r requirements.txt
Se o arquivo requirements.txt ainda não existir, você pode instalar manualmente:

bash
Copy
Edit
pip install python-telegram-bot==20.6 aiohttp python-binance python-dotenv
3. Configure o token do bot
Crie um arquivo .env com o seguinte conteúdo:

env
Copy
Edit
TELEGRAM_TOKEN=SEU_TOKEN_AQUI
Ou edite diretamente no bot.py.

4. Execute o bot
bash
Copy
Edit
python bot.py
📂 Estrutura do Projeto
bash
Copy
Edit
solana-price-alert-bot/
├── bot.py                 # Arquivo principal do bot
├── handlers.py            # Lógica dos botões e comandos
├── alert_manager.py       # Gerencia alertas e ranges dos usuários
├── binance_api.py         # Consulta preço da Binance
├── price_checker.py       # Checa preço em segundo plano
├── alerts.json            # Armazena os dados dos usuários
├── .env                   # Token do bot
├── README.md              # Este arquivo
└── requirements.txt       # (Opcional) dependências do projeto
📈 Lógica dos Alertas
Alerta de Preço (price)
Notifica quando o preço da SOL ultrapassa ou abaixa de um valor definido.

Exemplo:

SOL > 150

SOL < 130.5

Alerta de Faixa (range)
Notifica quando o preço entra ou sai de uma faixa.

Registra tempo de permanência dentro da faixa.

Exemplo:

Range: de $142.20 até $148.00

Resultado:

makefile
Copy
Edit
Entrou: 24/03/2025 13:00
Saiu:   24/03/2025 15:42
Duração: 2h42min
💾 Persistência de Dados
Os alertas são armazenados em alerts.json

Cada usuário é identificado por ID (automático)

Em caso de queda ou reinício, os dados continuam salvos

Todos os dados são salvos a cada modificação para evitar perda

✅ Roadmap de Construção (Etapas do Projeto)
Etapa	Status	Descrição
1. bot.py com comando /start e menu	✅	Iniciar o bot com botões interativos
2. alert_manager.py	✅	Gerenciar leitura, escrita e validação de alertas
3. binance_api.py	🚧	Função para obter preço atual da SOL/USDC
4. handlers.py	🚧	Funções para responder aos botões do menu
5. price_checker.py	🔜	Loop assíncrono que checa preço continuamente
6. Sistema de histórico de faixa (range)	🔜	Gravar hora de entrada/saída no range
7. Backup automático (backup_alerts.json)	🔜	Futuro recurso de segurança
8. Suporte a múltiplos ativos (ETH, BTC...)	🔜	Futuro upgrade do bot
✨ Recursos Futuramente Adicionais
 Envio de gráfico de preço via Matplotlib

 Web dashboard com Flask/Next.js para histórico

 Exportação de dados (CSV ou PDF)

 Configuração de alertas silenciosos (modo noturno)

 Suporte multiidioma (PT/EN)

🙋‍♂️ Autor
Lucas – Desenvolvedor entusiasta em Solana, Web3, e automatização de estratégias DeFi.
Este bot foi criado para monitorar LPs na rede Solana com foco no par SOL/USDC.

📜 Licença
Este projeto é livre para uso pessoal e educacional.
Fique à vontade para contribuir e melhorar o bot.
Distribuição comercial não autorizada.

⭐ Gostou do projeto?
Dá uma estrela no GitHub ⭐ e compartilha com outros devs Web3!
Vamos construir ferramentas DeFi cada vez mais inteligentes!

yaml
Copy
Edit

---

Se quiser, posso também gerar o `requirements.txt` e criar um `commit inicial` pronto pra você.  
Posso seguir com o próximo arquivo do bot (`alert_manager.py` completo ou `binance_api.py`)?






You said:
Esse bot sera construido de uma forma que poderemos no futuro podemos adicionar mais funcoes ate mesmo  codigo de acesso para usuarios poderem pagar pelo uso mensal ... ( futuramente ) 

Coloque as instrucoes caso rode em windows e linux criar o ambiente virtual instalar as dependencias etc .... 


ChatGPT said:
Perfeito, Lucas! Agora o README.md está 100% completo e profissional, com:

🚀 Apresentação e funcionalidades

✅ Estrutura de pastas

⚙️ Instruções para rodar no Windows e Linux

🛠️ Possibilidade de expandir o bot no futuro para versão paga

🧱 Roadmap de construção

✅ AGORA COPIE A VERSÃO FINAL DO README.md ABAIXO:
markdown
Copy
Edit
# 🤖 Solana Price Alert Bot — SOL/USDC Telegram Monitor

Um bot completo feito com **Python 3.10+** que usa a **Telegram Bot API v20+** e a **API da Binance** para monitorar em tempo real o preço da **SOL/USDC**, com alertas personalizados, registro de ranges e funcionalidades que serão expandidas futuramente.

> 📌 Ideal para quem investe em LPs como **SOL/USDC** e quer saber quando o preço entra ou sai de uma faixa.  
> 💡 Preparado para evoluir para versão PRO com login por token e plano mensal no futuro.

---

## 📌 Funcionalidades

✅ Menu com botões interativos (`/start`)  
📈 Ver preço atual da SOL/USDC  
🔔 Adicionar alerta de preço (ex: "me avise se SOL > $150")  
📏 Adicionar alerta de faixa de preço (ex: "entre $142.2 e $148")  
🕰️ Registrar tempo que o preço ficou dentro de uma faixa  
📋 Listar todos os alertas  
❌ Remover alertas  
🔕 Ativar/Desativar alertas  
💾 Dados salvos automaticamente em `alerts.json` (mesmo se o bot cair)  
🔁 Checagem contínua em segundo plano  
❌ Validação de entrada: evita erros de digitação

---

## 🖼️ Exemplo do Menu

📈 Ver Preço da SOL
➕ Adicionar Alerta de Preço
📏 Adicionar Alerta de Faixa (Range)
📋 Meus Alertas
❌ Remover Alerta
🔕 Ativar/Desativar Alertas
🕰️ Ver Histórico de Range

yaml
Copy
Edit

---

## 🧠 Planejado para o Futuro

✅ Suporte a múltiplos ativos (BTC, ETH, etc.)  
✅ Sistema de login via código/token (modo premium)  
✅ Histórico exportável (PDF ou CSV)  
✅ Integração com dashboard web (Flask ou Next.js)  
✅ Plano mensal com acesso exclusivo a funcionalidades PRO  

---

## 🖥️ Como Instalar e Rodar

### 🔰 Windows ou Linux

#### 1. Clone o repositório:
```bash
git clone https://github.com/seu-usuario/solana-price-alert-bot.git
cd solana-price-alert-bot
2. Crie um ambiente virtual:
No Linux/macOS:
bash
Copy
Edit
python3 -m venv venv
source venv/bin/activate
No Windows:
bash
Copy
Edit
python -m venv venv
venv\Scripts\activate
3. Instale as dependências:
bash
Copy
Edit
pip install -r requirements.txt
Ou manualmente:

bash
Copy
Edit
pip install python-telegram-bot==20.6 aiohttp python-binance python-dotenv
4. Crie o arquivo .env com seu token do bot:
env
Copy
Edit
TELEGRAM_TOKEN=SEU_TOKEN_AQUI
5. Execute o bot:
bash
Copy
Edit
python bot.py
📂 Estrutura de Pastas
bash
Copy
Edit
solana-price-alert-bot/
├── bot.py                 # Arquivo principal do bot
├── handlers.py            # Comandos e callbacks dos botões
├── alert_manager.py       # Lida com alertas e ranges
├── binance_api.py         # Consulta de preço da SOL
├── price_checker.py       # Checagem em segundo plano
├── alerts.json            # Banco de dados local
├── .env                   # Token do Telegram
├── README.md              # Este arquivo
└── requirements.txt       # Lista de dependências
📈 Tipos de Alerta
➕ Alerta de Preço
Exemplo:

SOL > 150

SOL < 132.25

📏 Alerta de Faixa (Range)
Exemplo:

Min: 142.20

Max: 148.00

O bot irá registrar:

makefile
Copy
Edit
Entrou: 24/03/2025 13:00  
Saiu:   24/03/2025 14:45  
Duração: 1h45min
🧱 Roadmap de Construção
Etapa	Status	Descrição
1. bot.py com /start e menu interativo	✅	Interface inicial
2. alert_manager.py	✅	Gerenciar alertas, ranges e salvar no JSON
3. binance_api.py	🚧	Função para pegar preço da Binance
4. handlers.py	🚧	Funções de cada botão/menu
5. price_checker.py	🔜	Verificação contínua em segundo plano
6. Histórico de range com entrada/saída	🔜	Registrar horários no JSON
7. Acesso com código/token (modo PRO)	🔜	Para liberar funcionalidades extras
8. Exportar histórico (CSV/PDF)	🔜	Geração de relatório dos alertas
9. Web dashboard (Next.js ou Flask)	🔜	Visualizar dados em tempo real
🧙‍♂️ Autor
Lucas – Desenvolvedor entusiasta em Web3, Solana, DeFi e automações com Python.
Este projeto foi criado para uso pessoal e aberto para a comunidade cripto.

📜 Licença
Uso livre para fins pessoais e educacionais.
Distribuição comercial deve ser autorizada.

⭐ Curtiu?
Deixa uma estrela ⭐ no repositório e compartilha com outros investidores e desenvolvedores Web3.
Vamos construir ferramentas úteis juntos 🚀

yaml
Copy
Edit

---

Se quiser, posso te mandar também:

- `requirements.txt` pronto
- Um commit inicial `.zip` com a estrutura

Quer que eu continue agora com o `alert_manager.py` finalizado ou com `binance_api.py` (consulta
```
