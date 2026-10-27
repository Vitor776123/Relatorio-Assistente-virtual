# Projeto Puma Assistente Virtual

Painel estático (HTML + JS puro, sem build) com a retenção, temas e mensagens do bot PUMA no HiBot.

## Publicar
1. Suba esta pasta em um repositório no GitHub.
2. Na Vercel: **Add New > Project**, escolha o repositório, **Framework Preset: Other**, deixe build e output em branco e clique em Deploy.

## Atualizar os dados (para o time inteiro ver)
1. Abra o painel > **Atualizar base**, suba a planilha (CSV do HiBot) e escolha **de qual teste é a base** (TU1, TU2, TUC1...). Se algumas datas forem de outro teste, ajuste em "Algumas datas são de outro teste?".
2. Confira o resultado e confirme em **Substituir base atual**.
3. Clique em **Baixar base.json**.
4. Substitua o `base.json` do repositório por esse arquivo e faça commit. A Vercel republica sozinha.

Subir a planilha no painel sem trocar o `base.json` vale só para aquele navegador.

## Regras de cálculo
- **Teste** (TU1, TU2, TUC1...) é escolhido por você ao subir a base. Cada **data** é um dia dentro do teste.
- **Ticket** = coluna `tag_outras_duvidas` (BP) preenchida. Ticket = foi para a inbox = não retido.
- **Retenção original** = atendimentos sem ticket (ficaram no bot). Número bruto: não confirma que ajudou.
- **Retenção confirmada (oficial)** = atendimentos em que o cliente respondeu "Sim" à pergunta de ajuda, sobre o total.
- **Possível não retenção** = ficou no bot, mas disse que não ajudou ou saiu sem avaliação final. Fora do cálculo, é um alerta.
- A aba "Retenção" da planilha não é usada.
