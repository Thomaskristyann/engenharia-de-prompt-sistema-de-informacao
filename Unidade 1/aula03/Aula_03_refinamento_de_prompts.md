# Atividade - Refinamento de Prompts

## Identificação

- **Disciplina:** Tendências em Ciência da Computação
- **Curso:** Sistemas de Informação
- **Integrante:** Thomas Kristyann Santos Dias
- **Grupo:** Individual
- **Ferramenta de IA utilizada:** ChatGPT
- **Data:** 30/10/2026

---

## 1. Problema escolhido

### Contexto

Um sistema acadêmico permite que os alunos acessem suas informações utilizando e-mail e senha. Para que o acesso funcione corretamente, é importante verificar se a tela de login consegue lidar com diferentes situações.

### Problema

A dificuldade escolhida foi criar casos de teste para verificar o funcionamento de uma tela de login de um sistema acadêmico.

### Objetivo

Utilizar a inteligência artificial para criar casos de teste que ajudem a identificar possíveis erros no login, comparando como as respostas melhoram conforme os prompts são refinados.

---

## 2. Prompt 1 - Versão inicial

### Prompt

```text
Crie alguns casos de teste para a tela de login de um sistema acadêmico.
```

### Resultado

A IA apresentou alguns exemplos de testes que poderiam ser realizados:

1. **Login correto:** verificar se o usuário consegue entrar utilizando e-mail e senha válidos.
2. **Senha incorreta:** verificar se o sistema impede o acesso quando a senha está errada.
3. **E-mail inválido:** verificar se o sistema identifica um endereço de e-mail em formato incorreto.
4. **Campos vazios:** verificar se o sistema impede o login quando os campos não são preenchidos.
5. **Recuperação de senha:** verificar se o usuário consegue iniciar o processo de recuperação da senha.

### Primeira impressão

A resposta apresentou situações importantes e relacionadas ao problema. Porém, os exemplos ficaram muito simples e não explicaram como realizar cada teste.

Também faltaram informações como os passos necessários, os dados utilizados e o resultado esperado em cada situação. Dessa forma, seria necessário organizar melhor a solicitação para conseguir uma resposta mais útil.

---

## 3. Prompt 2 - Primeiro refinamento

### Alterações realizadas

- **Papel:** solicitei que a IA atuasse como alguém com experiência em testes de software.
- **Contexto:** expliquei que se tratava de um sistema acadêmico com acesso por e-mail e senha.
- **Objetivo:** deixei claro que precisava de casos de teste para verificar o funcionamento do login.
- **Público:** considerei estudantes iniciantes em Sistemas de Informação.
- **Formato:** solicitei uma tabela organizada.
- **Restrições:** pedi uma linguagem simples e situações relacionadas somente ao login.
- **Critérios:** solicitei que cada teste apresentasse os passos e o resultado esperado.

### Prompt

```text
Atue como um profissional com experiência em testes de software.

Estou desenvolvendo um sistema acadêmico em que os alunos
acessam suas contas utilizando e-mail e senha.

Crie 8 casos de teste para verificar o funcionamento da
tela de login.

Considere situações de sucesso, senha incorreta, e-mail
inválido, campos vazios e outros possíveis erros de entrada.

Organize os casos em uma tabela contendo:
- Nome do teste;
- Dados utilizados;
- Passos para realizar o teste;
- Resultado esperado.

Utilize uma linguagem simples, adequada para estudantes
iniciantes de Sistemas de Informação.
```

### Resultado

A IA apresentou os seguintes casos de teste:

| Teste | Dados utilizados | Passos | Resultado esperado |
|---|---|---|---|
| Login válido | E-mail e senha corretos | Preencher os campos e clicar em entrar | O acesso deve ser permitido |
| Senha incorreta | E-mail correto e senha errada | Preencher os campos e tentar entrar | O acesso deve ser negado |
| E-mail inválido | E-mail em formato incorreto | Informar o e-mail e tentar entrar | O sistema deve indicar o formato inválido |
| E-mail vazio | Campo de e-mail vazio | Preencher somente a senha | O sistema deve solicitar o e-mail |
| Senha vazia | Campo de senha vazio | Preencher somente o e-mail | O sistema deve solicitar a senha |
| Ambos vazios | Nenhum campo preenchido | Clicar em entrar | O sistema deve solicitar os dados |
| Dados incorretos | E-mail e senha incorretos | Preencher os campos e tentar entrar | O acesso deve ser negado |
| Espaços nos campos | Dados com espaços indevidos | Informar os dados e tentar entrar | O sistema deve tratar os espaços corretamente |

### Comparação entre Prompt 1 e Prompt 2

| Critério | Prompt 1 | Prompt 2 |
|---|---:|---:|
| Clareza | 3 | 5 |
| Precisão | 2 | 4 |
| Relevância | 4 | 5 |
| Organização | 2 | 5 |
| Adequação ao público | 3 | 5 |
| Atendimento ao objetivo | 3 | 5 |
| Utilidade prática | 2 | 4 |
| **Total** | **19** | **33** |

*Escala: 1 = muito insatisfatório e 5 = excelente.*

### Análise das melhorias

A segunda resposta ficou mais organizada e apresentou informações que não estavam presentes na primeira. A tabela facilitou a leitura e permitiu entender melhor como cada teste deveria ser realizado.

Mesmo assim, percebi que alguns casos ainda poderiam ser mais específicos. Por exemplo, o teste de espaços nos campos não explica exatamente como o sistema deveria tratar essa situação. Também seria interessante indicar a prioridade de cada teste e deixar claro quando uma funcionalidade não foi especificada.

---

## 4. Prompt 3 - Segundo refinamento

### O que ainda precisava melhorar?

1. A primeira resposta era muito genérica e não apresentava os passos dos testes.
2. O primeiro refinamento melhorou a organização e acrescentou dados e resultados esperados.
3. Ainda faltavam critérios mais específicos para avaliar cada situação.
4. Seria útil adicionar a prioridade dos testes e separar melhor as condições de entrada.
5. Não era necessário acrescentar funcionalidades que não foram informadas sobre o sistema.
6. Essas mudanças podem deixar os casos de teste mais claros e evitar suposições.

### Hipótese de melhoria

Acredito que a terceira resposta ficará melhor porque terá instruções mais específicas, apresentará os passos de cada teste e indicará a prioridade. Além disso, a IA deverá evitar inventar funcionalidades que não foram descritas.

### Prompt

```text
Atue como um profissional de testes de software.

CONTEXTO:
Estou analisando a tela de login de um sistema acadêmico.
O acesso é realizado por meio de e-mail e senha.

OBJETIVO:
Criar casos de teste que ajudem a verificar se o login
funciona corretamente e se o sistema trata entradas inválidas.

TAREFA:
Crie 8 casos de teste diferentes, incluindo:
- Login com dados válidos;
- Senha incorreta;
- E-mail em formato inválido;
- E-mail vazio;
- Senha vazia;
- Ambos os campos vazios;
- Dados incorretos;
- Espaços antes ou depois dos dados informados.

FORMATO:
Organize os resultados em uma tabela com:
1. Identificação do teste;
2. Objetivo;
3. Dados de entrada;
4. Passos para execução;
5. Resultado esperado;
6. Prioridade (alta, média ou baixa).

RESTRIÇÕES:
- Utilize linguagem simples e direta.
- Não invente funcionalidades que não foram informadas.
- Não considere que o sistema possui recursos específicos
  sem que isso tenha sido descrito.
- Diferencie os testes de sucesso dos testes de falha.

CRITÉRIO DE QUALIDADE:
Os casos devem ser claros o suficiente para que outra
pessoa consiga entender o que precisa ser testado e
qual resultado deve ser observado.
```

### Resultado

A IA apresentou uma tabela mais completa:

| Teste | Objetivo e dados | Passos | Resultado esperado | Prioridade |
|---|---|---|---|---|
| Login válido | Verificar acesso com e-mail e senha corretos | Preencher os dois campos e clicar em entrar | O sistema deve permitir o acesso | Alta |
| Senha incorreta | Utilizar e-mail válido e senha errada | Preencher os campos e tentar entrar | O acesso deve ser negado | Alta |
| E-mail inválido | Informar um endereço em formato incorreto | Digitar o e-mail inválido e tentar entrar | O sistema deve impedir o envio ou informar o formato inválido | Média |
| E-mail vazio | Deixar o e-mail sem preenchimento | Informar somente a senha e tentar entrar | O sistema deve indicar que o e-mail é obrigatório | Alta |
| Senha vazia | Deixar a senha sem preenchimento | Informar somente o e-mail e tentar entrar | O sistema deve indicar que a senha é obrigatória | Alta |
| Ambos vazios | Não preencher nenhum campo | Clicar em entrar | O sistema não deve permitir o acesso | Alta |
| Dados incorretos | Informar e-mail e senha que não correspondem a uma conta válida | Preencher os campos e tentar entrar | O acesso deve ser negado | Alta |
| Espaços nos dados | Informar dados com espaços no início ou no final | Preencher os campos com espaços adicionais e tentar entrar | O sistema deve tratar os espaços de forma adequada, sem permitir acesso indevido | Média |

**Observação:** os resultados esperados são critérios propostos para o teste. O comportamento exato depende das regras implementadas no sistema real.

---

## 5. Comparação final dos três prompts

| Critério | Prompt 1 | Prompt 2 | Prompt 3 |
|---|---:|---:|---:|
| Clareza | 3 | 5 | 5 |
| Precisão | 2 | 4 | 5 |
| Relevância | 4 | 5 | 5 |
| Organização | 2 | 5 | 5 |
| Adequação ao público | 3 | 5 | 5 |
| Atendimento ao objetivo | 3 | 5 | 5 |
| Utilidade prática | 2 | 4 | 5 |
| **Total** | **19** | **33** | **35** |

### Qual foi a melhoria?

A principal melhoria foi a evolução de uma resposta simples para uma lista de testes mais organizada e detalhada. No primeiro prompt, a IA apenas sugeriu algumas situações. No segundo, apresentou dados, passos e resultados esperados. No terceiro, acrescentou objetivos, prioridades e restrições para evitar informações inventadas.

A modificação que teve maior impacto foi explicar melhor o contexto e definir exatamente como a resposta deveria ser organizada.

---

## 6. Validação crítica

Depois de analisar as respostas, percebi que nem tudo que a IA apresenta deve ser considerado correto automaticamente.

Os casos de teste fazem sentido para uma tela de login, mas alguns comportamentos dependem das regras do sistema. Por exemplo, não foi informado se o sistema deve remover espaços automaticamente ou apenas rejeitar os dados.

Também não foi possível confirmar o funcionamento dos testes em um sistema real, pois a atividade foi realizada com base em um cenário proposto.

Para validar os resultados, seria necessário executar cada caso em uma aplicação, comparar o comportamento com o resultado esperado e verificar se existem erros.

---

## 7. Reflexão individual

**1. Qual foi a principal diferença entre o prompt inicial e o prompt refinado?**

O prompt inicial era muito simples e deixava várias informações em aberto. Os refinados explicaram melhor o contexto, o objetivo e o formato esperado da resposta.

**2. Quais elementos tiveram maior impacto no resultado?**

O contexto, as instruções mais específicas e a organização em tabela foram os elementos que mais ajudaram.

**3. Um prompt mais longo necessariamente produz uma resposta melhor? Justifique.**

Não. Um prompt pode ser longo e continuar confuso. O mais importante é apresentar informações que realmente ajudem a IA a entender o que precisa fazer.

**4. O que acontece quando o objetivo solicitado à IA não está claramente definido?**

A IA pode interpretar a solicitação de várias maneiras e apresentar uma resposta muito genérica ou diferente do que realmente precisamos.

**5. Quais informações você considera indispensáveis para elaborar um bom prompt?**

Considero importante informar o contexto, o objetivo, a tarefa, o público e o formato desejado para a resposta.

**6. Como o refinamento de prompts pode ser útil para um profissional de Ciência da Computação?**

Pode ajudar na criação e revisão de códigos, elaboração de testes, identificação de erros e busca por soluções para problemas de tecnologia.

**7. Que riscos podem surgir quando confiamos em uma resposta da IA sem avaliar sua qualidade?**

Podemos utilizar informações incorretas, criar soluções com falhas ou tomar decisões baseadas em algo que não foi devidamente verificado.

**8. Houve alguma situação em que o Prompt 3 ficou pior que o Prompt 2? Se sim, explique.**

Neste exemplo, o terceiro prompt apresentou uma resposta mais completa. Porém, isso não significa que sempre será melhor, pois muitas instruções podem deixar a solicitação confusa.

**9. Existe um ponto em que adicionar mais instruções começa a prejudicar a resposta?**

Sim. Quando existem instruções desnecessárias ou contraditórias, a IA pode ter dificuldade para entender o que deve priorizar.

**10. O que você faria para verificar se a resposta tecnicamente está correta?**

Compararia as informações com materiais confiáveis e, quando possível, executaria os testes em um sistema real para verificar se os resultados correspondem ao esperado.

---

## 8. Cinco recomendações práticas

1. Explique claramente o que você deseja obter da IA.
2. Apresente o contexto do problema para evitar interpretações erradas.
3. Informe o formato em que deseja receber a resposta.
4. Acrescente restrições para evitar informações desnecessárias ou inventadas.
5. Sempre revise e valide as informações antes de utilizá-las.

---

## 9. Take Away

> Um bom prompt não é simplesmente um prompt longo. Ele precisa ser claro, apresentar o contexto correto e explicar exatamente o que esperamos da inteligência artificial.

Com essa atividade, percebi que pequenas mudanças na forma de escrever uma solicitação podem melhorar bastante o resultado. Também entendi que a IA pode ajudar em atividades da área de tecnologia, mas suas respostas precisam ser analisadas e verificadas antes de serem utilizadas.

---

## 10. Conclusão

O refinamento dos prompts mostrou como a qualidade das instruções influencia diretamente as respostas geradas pela inteligência artificial. Ao comparar as três versões, foi possível perceber que definir melhor o contexto, o objetivo e o formato torna a resposta mais útil.

A atividade também reforçou que a IA deve ser utilizada como uma ferramenta de apoio, e não como substituta da análise e do conhecimento de quem está desenvolvendo uma solução.
