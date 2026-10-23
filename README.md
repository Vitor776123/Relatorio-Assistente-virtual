# Projeto Puma Assistente Virtual

Painel estático (HTML + JS puro, sem build) com a retenção, temas e mensagens do bot PUMA no HiBot.

## Publicar
1. Suba esta pasta em um repositório no GitHub.
2. Na Vercel: **Add New > Project**, escolha o repositório, **Framework Preset: Other**, deixe build e output em branco e clique em Deploy.

## Atualizar os dados (para o time inteiro ver)
1. Abra o painel > **Atualizar base** e suba a nova planilha (CSV do HiBot). Confira o resultado.
2. Clique em **Baixar base.json**.
3. Substitua o `base.json` do repositório por esse arquivo e faça commit. A Vercel republica sozinha.

Subir a planilha no painel sem trocar o `base.json` vale só para aquele navegador.

## Regras de cálculo
- Ticket = coluna `tag_outras_duvidas` (BP) preenchida; ticket = não retido.
- Sem ticket = retido no chat. A aba "Retenção" da planilha não é usada.
- "Não, preciso de ajuda" sem ticket conta como retido, mas recebe a marca *Possível não retenção* (fora do cálculo).
- TU = time interno; TUC = e-mail ou nome com "puma" (configurável em Atualizar base > Regras). Rodada = um dia (configurável).
