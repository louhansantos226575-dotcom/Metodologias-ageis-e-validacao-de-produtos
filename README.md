# Da Hipótese à Evidência: Relatório de Performance com Narrativa por IA

Case de Product Discovery e validação de produto. Disciplina **Metodologias Ágeis e Validação de Produtos** (Graduação em IA e Automação Digital, UniFECAF \+ Rocketseat).

**Autor:** Louhan **Período das entrevistas:** 31/10/2026

---

## 1\. Resumo do case

Gestores de tráfego gastam muito tempo montando relatórios que o cliente final muitas vezes não entende. A hipótese testada foi que um relatório com explicação em linguagem de cliente, gerado por IA, resolve essa dor e é algo que o gestor aceitaria testar com um cliente real.

Em vez de construir o produto, executei um experimento barato: entrevistas com 5 potenciais usuários, usando um relatório de exemplo (com dados fictícios) como estímulo. Os critérios de sucesso e a regra de decisão foram definidos antes das entrevistas.

Resultado: H1 (problema) atingida em 4 de 5; H2 (solução) e H3 (valor) atingidas em 3 de 5, exatamente no limite mínimo. Decisão: perseverar, com ajustes no MVP (seção 11).

---

## 2\. Problema, público e oportunidade

- **Problema:** montar relatórios de tráfego consome horas todo ciclo, e o cliente frequentemente não entende os números e pede explicação.  
- **Público:** gestores de tráfego pago (freelancers e agências pequenas e médias) que enviam relatórios recorrentes a clientes.  
- **Oportunidade:** as ferramentas atuais (planilhas, Looker Studio, Reportei e similares) organizam e mostram dados, mas a interpretação (o que aconteceu e por quê) continua manual. A hipótese é que essa camada pode ser gerada com apoio de IA.

---

## 3\. Hipóteses e critérios (definidos antes do teste)

| Hipótese | Enunciado | Critério de sucesso (de 5 pessoas válidas) |
| :---- | :---- | :---- |
| **H1: Problema** | Gestores gastam tempo relevante em relatórios, e o cliente pede explicação ou não entende | 3 ou mais gastam 2h ou mais por semana **e** relatam dúvida do cliente |
| **H2: Solução** | Um relatório com narrativa em linguagem de cliente, gerado por IA, é bom o bastante para ser usado quase sem edição | 3 ou mais dão nota 4 ou 5 (de 5\) ao exemplo **e** editariam menos de 30% |
| **H3: Valor** | O gestor quer isso no dia a dia | 3 ou mais aceitam testar com 1 cliente real na semana seguinte, com compromisso concreto (qual cliente) |

**Regra de decisão (fixada antes):**

- **Perseverar:** H1, H2 e H3 atingidas.  
- **Ajustar:** H1 atingida, mas H2 ou H3 não (o problema existe, a solução precisa mudar).  
- **Pivotar:** H1 não atingida, mas 3 ou mais pessoas citam outra dor em comum.  
- **Abandonar:** H1 não atingida e nenhum padrão alternativo.

Na H3, respostas como "talvez" ou "depende" foram contadas como **não**.

---

## 4\. Solução inicial e MVP

- **Solução inicial:** relatório semanal gerado por IA a partir dos dados da conta, com resumo, causas das variações e próximos passos, em linguagem de cliente.  
- **MVP (concierge, sem código):** um relatório de uma página, montado com apoio de IA a partir de **dados fictícios**, mostrado aos entrevistados. Arquivo: [`docs/relatorio_exemplo_dados_ficticios.pdf`](http://docs/relatorio_exemplo_dados_ficticios.pdf).

O relatório é um estímulo para medir reação, não um produto funcional. Nenhum número dele é real, e isso foi dito aos entrevistados.

---

## 5\. Lean Canvas

Os blocos em **verde** (Problema, Solução, Proposta de Valor, Métricas-Chave, Segmentos) foram testados neste experimento. Os blocos em **cinza** (Fontes de Receita, Estrutura de Custos, Canais, Vantagem Competitiva) **não foram validados** nesta rodada e continuam como suposição.

---

## 6\. Como a IA foi usada

- **Claude (Anthropic)** apoiou: a geração de ideias e hipóteses candidatas, a estruturação dos critérios e da regra de decisão, o roteiro de entrevista e a mensagem de convite, o prompt do Lean Canvas, o relatório de exemplo com dados fictícios e a organização das respostas em tabelas.  
- **Eu decidi:** a ideia escolhida, a aprovação das hipóteses e dos critérios antes do teste, a escolha e o contato com os entrevistados, as entrevistas, a interpretação e a decisão final.  
- **O que a IA não fez:** validar mercado nem gerar respostas de usuários. Todas as respostas registradas vêm das pessoas citadas.  
- &nbsp;

---

## 7\. Experimento

**Método:** entrevistas de 10 a 15 minutos, com triagem de perfil, perguntas sobre o problema **antes** de mostrar o relatório de exemplo e perguntas de avaliação depois.

**Triagem (T1 a T4):** atua com tráfego pago? Quantos clientes? Envia relatório e com que frequência? Quem monta o relatório?

**Classificação:**

- **Central:** atende 3 ou mais clientes, envia semanal ou quinzenal e monta o relatório sozinho.  
- **Parcial:** atua e envia relatório, mas não cumpre todos os critérios acima (envio mensal ou só revisa).  
- **Fora do perfil:** não atua ou não envia relatório. Não entra na contagem.

**Amostra:** 5 pessoas válidas, **1 central (Julia) e 4 parciais (Gustavo, Zaia, Izabela e Geovanne)**. Uma pessoa inicialmente convidada foi classificada como fora do perfil e **excluída da contagem**, sendo substituída por Izabela.

**Formato e registro:** a entrevista é conduzida ao vivo pelo pesquisador. O Google Forms funciona como ficha interna de registro: o entrevistador preenche as respostas durante ou logo após a conversa; o formulário não deve ser enviado ao participante para autopreenchimento.

**Identificação e privacidade:** usar nome ou código de participante conforme o consentimento obtido. Não afirmar que houve autorização para registro, gravação ou citação sem confirmar isso diretamente com cada pessoa.

### 7.1. Fluxo de coleta: Google Forms → Google Sheets

O registro foi estruturado em um Google Forms criado com Google Apps Script. O formulário reúne identificação, data da entrevista, autorização de registro e gravação, triagem (T1 a T4), perguntas do roteiro (P1 a P7), encerramento e observações do entrevistador.

**Como conectar o formulário à planilha:**

1. Abrir o formulário criado pelo Apps Script usando o link de edição.  
2. Acessar a aba **Respostas** no Google Forms.  
3. Clicar no ícone do Google Sheets (**Vincular ao Planilhas**) e escolher **Criar uma nova planilha**.  
4. A partir dessa vinculação, cada envio do formulário gera uma nova linha na planilha, com carimbo de data/hora e uma coluna para cada pergunta.  
5. Usar essa planilha como base de organização e análise. Não alterar manualmente as respostas originais; se necessário, criar outra aba para limpeza, classificação e cálculos.

**Importante:** o script cria o formulário, mas a vinculação à planilha de respostas deve ser feita na interface do Google Forms, conforme os passos acima. O carimbo de data/hora é gerado pelo Google Forms no envio. A data da entrevista é registrada em uma pergunta separada.

**Estrutura de armazenamento:**

- **Google Forms:** instrumento de coleta e registro de cada entrevista.  
- **Google Sheets:** base consolidada, com uma linha por entrevista e colunas correspondentes às perguntas.  
- **Registros originais:** Conversas \+ Form  
- **Análise:** usar uma aba separada para classificar perfil, calcular tempo semanal, notas, percentual de edição e resultado de cada hipótese.

<details>
<summary>Roteiro de entrevista usado</summary>

&nbsp;

**Bloco 1: Problema (sem mostrar o relatório)**

- P1. Me conta como foi o último relatório que você enviou (ou revisou) a um cliente, do começo ao fim.  
- P2. Somando todos os clientes, quanto tempo por semana vai em relatórios? (Se só revisa: quanto o time leva e quanto você leva revisando.)  
- P3. Os clientes costumam ter dúvida ou pedir explicação? Se sim, qual foi a última vez?  
- P4. O que você usa hoje para montar o relatório e o que não te atende?

**Bloco 2: Solução (depois de mostrar o relatório de exemplo, com dados fictícios)**

- P5. De 1 a 5, quanto você enviaria esse relatório a um cliente? Por quê?  
- P6. O que você mudaria? Quanto editaria, em porcentagem?

**Bloco 3: Valor**

- P7. Você testaria isso com um cliente real na próxima semana? Qual cliente?

</details>

&nbsp;

---

## 8\. Base de respostas e evidências

### 8.1 Perfil e H1 (problema) — dados simulados

| Entrevistado | Perfil | Quem monta | Tempo por semana | Cliente tem dúvida? | H1 |
| :---- | :---- | :---- | :---- | :---- | :---- |
| Gustavo | Parcial (envio mensal) | Próprio(a) gestor(a) | 5h | Sim (custo por lead subiu, leads caíram) | Sim |
| Zaia | Parcial (revisa o time) | Time | Time 10h, revisão 2 a 3h | Sim (muito alcance, poucas conversões) | Sim |
| Julia | **Central** | Próprio(a) gestor(a) | 3 a 4h | "Não muito" (1 caso citado) | Não\* |
| Izabela | Parcial (envio mensal; nº de clientes não registrado) | Próprio(a) gestor(a) | 6h | Sim (qualidade dos leads) | Sim |
| Geovanne | Parcial (revisa o time) | Time | Time 12h, revisão 3h | Sim (queda sem motivo claro) | Sim |

\*Julia atingiu o tempo, mas disse que o cliente "não muito" tem dúvida. Pontuei de forma conservadora. Se contada como sim, a H1 vai a 5/5 e a decisão não muda.

### 8.2 H2 (solução) e H3 (valor)

| Entrevistado | Nota (1 a 5\) | Edição | H2 | Aceita testar? | Compromisso | H3 |
| :---- | :---- | :---- | :---- | :---- | :---- | :---- |
| Gustavo | 4 | 20% | Sim | Sim | Cliente definido, oferece relatório real | Sim |
| Zaia | 5 | 15% | Sim | Sim | Cliente de e-commerce | Sim |
| Julia | 3 | 40% | Não | "Talvez" | Nenhum cliente definido | Não |
| Izabela | 4 | 25% | Sim | Sim | Cliente de serviços, oferece relatório real | Sim |
| Geovanne | 2 | 50% | Não | Não | Quer entender como o sistema chega nas explicações | Não |

Nota média: 3,6 (mediana 4). Edição média estimada: 30%.

### 8.3 Citações

- Gustavo: "O Looker ajuda bastante na visualização, mas não explica os resultados."  
- Zaia: "O problema é que falta uma camada de interpretação."  
- Julia: "A ideia de explicar os resultados é boa, mas eu deixaria mais direto."  
- Izabela: "Só teria que tomar cuidado para as explicações realmente corresponderem aos dados."  
- Geovanne: "Algumas explicações parecem genéricas e poderiam ser aplicadas a qualquer cliente."

---

## 9\. Síntese dos feedbacks e padrões

| Padrão | Frequência | Observação |
| :---- | :---- | :---- |
| Falta de uma camada de interpretação nas ferramentas atuais | Gustavo, Zaia e Izabela (explícito); Zaia e Geovanne pedem padronização das análises | Reforça o problema (H1) |
| Necessidade de personalizar por cliente ou segmento | 5 de 5 | Como pedido, risco ("genérico") ou condição para testar |
| Mais ações e próximos passos no relatório | 4 de 5 (Gustavo, Zaia, Izabela, Geovanne) | Zaia, Izabela e Geovanne também pedem comparação com o período anterior |
| Preocupação com confiabilidade | Izabela e Geovanne | Medo de a IA explicar algo que os dados não sustentam |
| Texto mais curto e mais visual | Julia | Única entrevistada de perfil central |

Quem deu nota 4 ou 5 aceitou testar. Quem deu 2 ou 3, não. Os mesmos dois (Julia e Geovanne) falharam na H2 e na H3.

---

## 10\. Modelo de comparação: hipótese inicial vs resultadosREA

| Hipótese | Critério | Resultado | Veredito | O que os dados dizem |
| :---- | :---- | :---- | :---- | :---- |
| **H1: Problema** | 3 de 5 | **4 de 5** | Atingida | O tempo gasto e a dúvida do cliente aparecem de forma consistente. Entre quem revisa, o tempo do time é de 10 a 12h por semana. |
| **H2: Solução** | 3 de 5 | **3 de 5** | Atingida no limite | A linguagem de cliente foi bem recebida. As críticas foram: texto longo, análise genérica e pouca personalização. |
| **H3: Valor** | 3 de 5 | **3 de 5** | Atingida no limite | Três se comprometeram com um cliente concreto. Os dois que não se comprometeram citaram ajuste ao segmento (Julia) e confiabilidade (Geovanne). |

---

## 11\. Decisão final: perseverar, com ajustes&nbsp;

**Decisão:** perseverar, de acordo com a regra fixada antes do teste (H1, H2 e H3 atingidas).

**Justificativa:**

1. O problema foi confirmado em 4 de 5 entrevistas, com relatos concretos de dúvida do cliente.  
2. A solução foi bem avaliada por 3 de 5, e as mesmas 3 se comprometeram com um teste real. O interesse não ficou só no elogio.  
3. As críticas dos que não aprovaram apontam para ajustes de produto (personalização, brevidade, confiabilidade), não para a ideia errada.

**O que esta decisão não afirma:**

* H2 e H3 passaram **no limite mínimo**, então o sinal é moderado, não conclusivo.  
* Fontes de Receita, Estrutura de Custos, Canais e Vantagem Competitiva **não foram validados**.  
* "Aceitar testar" não é testar. O teste real ainda não foi executado.

**Ajustes para a próxima versão do MVP:**

1. **Personalização por cliente e segmento:** tom técnico ou simples, linguagem adaptada ao negócio.  
2. **Mais ações e próximos passos,** com comparação com o período anterior.  
3. **Versão curta e visual:** resumo objetivo e gráficos, para clientes sem paciência para ler.  
4. **Confiabilidade:** cada afirmação rastreável aos números, com revisão humana antes do envio.

**Próximo experimento recomendado:** concierge com **relatórios reais** (dados anonimizados) para os 3 entrevistados que se comprometeram (Gustavo, Zaia e Izabela). Critérios propostos, a ajustar **antes** de executar:

* O tempo de produção cai pelo menos 50% em relação ao processo manual.  
* O gestor edita menos de 30% do texto.  
* O cliente final dá nota 4 ou 5 para a clareza do relatório.  
* Pelo menos 2 dos 3 gestores querem usar no ciclo seguinte.

---

## 12\. Limitações e transparência

- Amostra pequena e não aleatória: 5 pessoas de uma rede próxima (amigos, parceiros e familiares) . Há risco de viés de cortesia.&nbsp;  
- Só 1 entrevistada de perfil central, e foi ela quem deu o sinal mais fraco. Não dá para generalizar a partir de 1 pessoa.  
- O estímulo foi um relatório fictício, não um produto funcional. A reação a ele não mede o desempenho real da IA com dados de uma conta.  
- Interpretação da H1 para quem só revisa: o critério de tempo foi aplicado ao tempo que a própria pessoa gasta revisando, e o tempo do time foi registrado à parte.

---

## 13\. Aprendizados e pontos a verificar

- Os critérios definidos **antes** do teste evitaram interpretar os resultados a posteriori.  
- Perguntar sobre o passado ("me conta a última vez") rendeu relatos mais úteis do que perguntar sobre intenção.  
- A avaliação da solução e o interesse em testar andaram juntos (H2 e H3). Isso sugere que a qualidade percebida do relatório é o principal fator de adoção.  
- A confiabilidade da análise gerada por IA é uma condição de uso, não um detalhe: dois entrevistados a citaram sem serem perguntados.

---

## 14\. Estrutura do repositório

```
.
├── README.md
├── docs/
│   ├── lean-canvas.png
│   └── relatorio_exemplo_dados_ficticios.pdf
└── evidencias/
    ├── evidencias_entrevistas.xlsx
    └── [PREENCHER: registros originais (áudios, prints ou anotações)]
```

&nbsp;
