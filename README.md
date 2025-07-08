# 🤖 Resumo Inteligente de Observações via Excel + Groq (IA)

Este script Python permite que você leia um arquivo Excel com observações de clientes, envie esse conteúdo para uma IA via API Groq e receba um **resumo final objetivo e útil**. Ideal para análises de feedback, SAC, atendimento ou pós-venda.

---

## 🔍 O que ele faz

1. Carrega um Excel com observações em uma aba chamada `Planilha1`.
2. Verifica se a coluna com as observações existe.
3. Limpa células vazias ou em branco.
4. Divide o conteúdo em partes de até 15.000 caracteres (~3750 tokens).
5. Envia cada parte para a IA (modelo `llama3-70b-8192`) para gerar resumos parciais.
6. Compila os resumos parciais em um **resumo final geral**.
7. Exibe o resultado final no terminal.

---

## ⚙️ Pré-requisitos

- Python 3.8+
- Bibliotecas:
  - `pandas`
  - `openai` (via Groq)
  - `textwrap`

Instale com:
```bash
pip install pandas openai
🛠️ Como usar
Altere no script:

CAMINHO DO ARQUIVO: caminho completo do seu Excel.

"NOME DA COLUNA": nome da coluna com as observações (ex: "Observação").

Sua chave da API da Groq.

Execute o script:

bash
Copiar
Editar
python Leitura_Excel_IA.py
Veja o resumo final no terminal.

🔐 Atenção
Sua chave da Groq deve ser configurada no os.environ["OPENAI_API_KEY"].

Cuidado para não ultrapassar limites de uso da API.

📈 Exemplo de aplicação
Analisar feedbacks de clientes.

Resumir observações de chamados de suporte.

Gerar sumários para reuniões de atendimento.

📄 Licença
Uso livre e open-source. Melhorias são bem-vindas!
