# Planilha de Contas — Finanças e Agenda

Painel pessoal de controle financeiro mensal + agenda, em um único `index.html` (sem build, sem dependências).

**Acesse:** https://ruandgarcia.github.io/planilhacontas/

## Funcionalidades

- **Financeiro:** lançamentos editáveis por mês (data, descrição, categoria, valor, pago, fixo), resumo de receitas/despesas/saldo, gastos por categoria, resumo anual com acumulado e cópia dos lançamentos fixos do mês anterior.
- **Agenda:** calendário mensal com compromissos (hora + anotação), contas a pagar no dia do vencimento e lista dos próximos 14 dias.
- **Importar / Exportar:** CSV (`;` ou `,`, datas `dd/mm/aaaa` ou `aaaa-mm-dd`) e backup completo em JSON.

## Onde ficam os dados

Este repositório guarda **só a página**: nenhum dado financeiro fica aqui.

Os dados são salvos em um arquivo `dados.json` num **repositório privado** (ex.: `painel-dados`), pela API do GitHub. Cada alteração vira um commit lá, então existe histórico de tudo. Sem GitHub configurado, a página salva no navegador (`localStorage`).

### Configurar a sincronização (uma vez por aparelho)

1. Crie um repositório **privado** `painel-dados` (com README).
2. Gere um token *fine-grained* em <https://github.com/settings/personal-access-tokens/new>:
   - **Repository access:** *Only select repositories* → `painel-dados`
   - **Permissions → Contents:** *Read and write*
3. Abra o painel, clique em **☁ GitHub**, cole o token e clique em **Testar e conectar**.

O token fica salvo apenas no navegador do aparelho. A página não conecta a repositórios públicos.
