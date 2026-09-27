# Prompt final — análise de feedbacks de cartão de crédito

Prompt de análise para times de produto, atendimento e experiência do cliente em instituição financeira.  
Desafio DIO: engenharia de prompt + versionamento no GitHub.

**Como usar:** cole este prompt no ChatGPT, Gemini ou similar e, em seguida, anexe ou cole os feedbacks reais. Sem a base de comentários, o modelo não deve inventar números nem conclusões.

---
## Dados
[Cole aqui os feedbacks: data, canal, texto, categoria/assunto e nota 1–5, quando existirem.]
Canal: Reclame Aqui. Sem data, sem nota 1–5 e sem dados pessoais nos resumos abaixo.
| # | Instituição | Categoria/assunto | Resumo do relato | Fonte |
|---|-------------|-------------------|------------------|--------|
| 1 | Itaú | Fatura/Cobrança | Cliente relata cobrança relacionada a uma fatura que afirma já ter sido paga. | [Reclame Aqui — Extra Itaucard](https://www.reclameaqui.com.br/cartoesitau/fui-cobrado-indevidamente-por-fatura-paga-no-meu-extra-itaucard_PsmBj_WRJAA7HCjp/) |
| 2 | Nubank | Estorno | Cliente relata que uma passagem aérea foi cancelada, mas o estorno não ocorreu corretamente. | [Reclame Aqui — Nubank](https://www.reclameaqui.com.br/nubank/minha-passagem-aerea-foi-cancelada-e-o-estorno-nao-ocorreu-corretamente_PH91dnkG_ElALETR/) |
| 3 | Bradescard | Aplicativo/Acesso | Cliente relata dificuldade para acessar o aplicativo e informa que o atendimento não reconhece seu CPF. | [Reclame Aqui — Bradescard](https://www.reclameaqui.com.br/bradescard/nao-consigo-acessar-meu-app-e-o-teleatendimento-diz-que-meu-cpf-nao-existe_RB3_v0tlkQMZvtyJ/) |
| 4 | C6 Bank | Atendimento/Cobrança | Cliente relata receber mais de 10 ligações por dia durante mais de um mês. | [Reclame Aqui — C6 Bank](https://www.reclameaqui.com.br/c6-bank/recebo-mais-de-10-ligacoes-diarias-de-voces-ha-mais-de-um-mes_Sayg4F6eyV8tfJlp/) |
| 5 | Credsystem | Anuidade/Negativação | Cliente relata ter sido negativado após realizar o pagamento da anuidade do cartão. | [Reclame Aqui — Credsystem](https://www.reclameaqui.com.br/credsystem-adm-cartoes-de-credito/fui-negativado-indevidamente-apos-pagar-anuidade-do-cartao_RRJpCkAjsYJSOzCX/) |
---
## Avaliação das fontes
**Adequadas ao exercício:** as cinco fontes são páginas **públicas** do Reclame Aqui, tratam de **cartão de crédito**, cobrem **temas distintos** (fatura/cobrança, estorno, aplicativo/acesso, atendimento/cobrança, anuidade/negativação) e **instituições distintas** (Itaú, Nubank, Bradescard, C6 Bank, Credsystem).
**Limitações:** Reclame Aqui concentra relatos de insatisfação (**viés negativo**); a amostra tem **n = 5**; a **frequência** (1/5 por tema) vale **somente neste conjunto**; **não generalizar** para o mercado, para cada banco ou para o canal como um todo. Não há notas 1–5 nem datas nestes resumos, então impacto/urgência no exemplo abaixo é inferência qualitativa a partir do que o cliente relatou, não estatística de mercado.
---
## Exemplo de saída do prompt
Análise restrita aos **5** feedbacks da seção Dados. Frequência = ocorrências neste conjunto (cada tema aparece **1 vez em 5**). Causas raiz **não** foram atribuídas quando o relato não as descreve.

### Resumo executivo
Nesta amostra de 5 reclamações públicas, todos os relatos são negativos e cada tema aparece uma única vez (1/5). Os clientes descrevem: cobrança ligada a fatura que afirmam já ter pago; estorno de passagem aérea cancelada que não ocorreu corretamente; falha de acesso ao app e atendimento que não reconhece o CPF; volume alto de ligações (mais de 10 por dia, por mais de um mês); e negativação após pagamento da anuidade. Não há elogios neste conjunto. As frequências não permitem ranquear “o problema mais comum do mercado”; as prioridades abaixo seguem o que os próprios relatos descrevem como prejuízo ou bloqueio de uso, sem presumir causa.

### Tabela
| Tema | Problema ou oportunidade | Sentimento predominante | Frequência | Evidência | Impacto/urgência (neste conjunto) | Ação sugerida |
|------|--------------------------|-------------------------|------------|-----------|-----------------------------------|---------------|
| Fatura/Cobrança | Cobrança associada a fatura que o cliente afirma já ter pago | Negativo | 1/5 | Relato Itaú (resumo) | Alto para o cliente afetado (cobrança contestada); frequência insuficiente para o mercado | Conciliar pagamento vs. cobrança e comunicar o resultado; não assumir causa (erro de sistema, atraso de compensação etc.) sem evidência |
| Estorno | Estorno de passagem aérea cancelada não ocorreu corretamente | Negativo | 1/5 | Relato Nubank (resumo) | Alto para o cliente afetado (valor não revertido conforme o relato); 1 caso | Investigar o fluxo de estorno desse caso; causa (emissor, bandeira, companhia aérea) **não** está no resumo |
| Aplicativo/Acesso | Dificuldade de acesso ao app; atendimento não reconhece o CPF | Negativo | 1/5 | Relato Bradescard (resumo) | Alto para o cliente afetado (uso do canal digital/atendimento bloqueado no relato); 1 caso | Validar identificação no app e no teleatendimento **neste** caso; não generalizar falha cadastral |
| Atendimento/Cobrança | Mais de 10 ligações por dia, por mais de um mês | Negativo | 1/5 | Relato C6 Bank (resumo) | Alto para o cliente afetado (contato repetido no tempo descrito); 1 caso | Revisar cadência de discagem **deste** fluxo; volume “de todos os clientes” não está nos dados |
| Anuidade/Negativação | Negativação relatada após pagamento da anuidade | Negativo | 1/5 | Relato Credsystem (resumo) | Alto para o cliente afetado (restrição cadastral no relato); 1 caso | Conferir baixa do pagamento vs. restrição neste caso; não inventar motivo da negativação |

### Principais elogios
Nenhum elogio nesta amostra de 5 relatos do Reclame Aqui.

### Principais oportunidades de melhoria
- Conferência explícita entre **pagamento informado pelo cliente** e **cobrança/negativação** (itens 1 e 5), sem presumir onde ocorreu o descompasso.
- Rastreabilidade de **estorno** quando o cliente informa cancelamento de passagem (item 2).
- Consistência de **identificação** entre app e teleatendimento (item 3).
- Política de **contato repetido** alinhada ao que o cliente descreveu (item 4).
- Estas são oportunidades **inferidas dos relatos**, não provas de falha sistêmica da instituição.

### Prioridades de ação (com evidência)
1. **Casos com restrição ou cobrança contestada (itens 1 e 5)** — o cliente afirma fatura já paga com nova cobrança, e outro afirma negativação após pagar anuidade. Evidência: dois relatos distintos neste conjunto. Fato: o que foi relatado. Interpretação: tratar como prioridade operacional **nestes casos**, não como ranking de mercado.
2. **Estorno não concluído conforme o relato (item 2)** — evidência: um relato de passagem cancelada sem estorno correto. Interpretação: priorizar a apuração do **caso**, sem atribuir culpa a um elo da cadeia que o resumo não cita.
3. **Acesso e identificação (item 3)** — evidência: um relato de app inacessível e CPF não reconhecido no teleatendimento. Interpretação: bloqueio de canal para **esse** cliente.
4. **Volume de ligações (item 4)** — evidência: o próprio texto cita mais de 10 ligações/dia por mais de um mês. Interpretação: impacto de contato excessivo **neste** cliente; não extrapolar frequência para a base.

### Fato vs. interpretação
- **Fato:** existem 5 reclamações públicas resumidas; instituições e temas são os da tabela de Dados; sentimento observado nesta amostra é negativo; elogios = 0; cada tema = 1/5.
- **Interpretação / sugestão:** impacto “alto para o cliente afetado”, ações de conciliação/investigação e a ordem das prioridades. Não é fato que a causa seja erro do banco, da loja, da aérea ou do cadastro, porque isso **não** está demonstrado nos resumos.
- **Limitação:** n = 5, canal com viés negativo, sem notas 1–5 e sem datas; frequência e urgência **não** representam o mercado.
