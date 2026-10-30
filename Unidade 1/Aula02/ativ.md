# Aula 02 — Engenharia de Prompt

## 1. Identificação

- **Curso:** Sistemas de Informação
- **Grupo:** Individual
- **Data:** 30/10/2026
- **Integrante:** Thomas Kristyann Santos Dias

## 2. Problema escolhido

O problema escolhido foi a criação de casos de teste para a tela de login de um sistema acadêmico.

A ideia é verificar se o acesso ao sistema funciona corretamente em diferentes situações, como quando o usuário informa os dados certos, digita uma senha incorreta ou deixa algum campo vazio.

## 3. Objetivo

Utilizar a inteligência artificial para ajudar na criação de casos de teste para uma tela de login, identificando situações que precisam ser verificadas para evitar possíveis erros no sistema.

## 4. Prompt inicial

```text
Crie alguns casos de teste para a tela de login de um sistema acadêmico.
```

## 5. Resultado inicial

A IA sugeriu alguns testes que poderiam ser realizados:

- Tentar entrar no sistema com e-mail e senha corretos.
- Tentar entrar utilizando uma senha incorreta.
- Informar um e-mail inválido.
- Tentar acessar o sistema deixando os campos vazios.
- Verificar se existe uma opção para recuperar a senha.

A resposta trouxe boas ideias para começar, mas não explicou muito bem como cada teste deveria ser feito.

## 6. Análise crítica

O primeiro resultado foi útil, pois mostrou algumas situações importantes que deveriam ser verificadas na tela de login. Porém, percebi que o pedido estava muito simples e, por isso, a resposta também ficou um pouco superficial.

Faltaram informações como o passo a passo de cada teste e o que deveria acontecer depois de cada tentativa de acesso.

Com isso, percebi que precisava explicar melhor o que eu esperava da IA, fornecendo mais detalhes sobre o sistema e sobre a maneira como gostaria de receber a resposta.

## 7. Prompt refinado

```text
Quero que você atue como alguém que trabalha com testes de software.

Estou desenvolvendo um sistema acadêmico que possui uma tela de login, onde os estudantes utilizam e-mail e senha para acessar suas contas.

Preciso que você crie pelo menos 8 casos de teste para verificar se essa tela está funcionando corretamente.

Considere situações como:
- Login com e-mail e senha corretos.
- Senha incorreta.
- E-mail inválido.
- Campos não preenchidos.
- Somente o e-mail preenchido.
- Somente a senha preenchida.
- E-mail e senha que não correspondem a uma conta.

Organize a resposta em uma tabela, mostrando o nome do teste, o que deve ser feito e qual resultado é esperado.

Utilize uma linguagem simples e explique cada teste de forma clara. Não invente funcionalidades que não foram informadas.
```

## 8. Resultado refinado

Depois de melhorar o prompt, a IA apresentou uma resposta mais organizada e detalhada. Os casos de teste ficaram da seguinte forma:

| Teste                                  | O que será feito                                                   | Resultado esperado                             |
| -------------------------------------- | ------------------------------------------------------------------ | ---------------------------------------------- |
| Login correto                          | Informar e-mail e senha válidos.                                   | O usuário consegue acessar o sistema.          |
| Senha incorreta                        | Informar o e-mail correto e uma senha errada.                      | O sistema não permite o acesso.                |
| E-mail inválido                        | Digitar um e-mail em formato incorreto.                            | O sistema informa que o e-mail é inválido.     |
| Campos vazios                          | Clicar em entrar sem preencher nada.                               | O sistema solicita o preenchimento dos campos. |
| E-mail não preenchido                  | Informar somente a senha.                                          | O sistema solicita o e-mail.                   |
| Senha não preenchida                   | Informar somente o e-mail.                                         | O sistema solicita a senha.                    |
| Dados que não correspondem a uma conta | Informar um e-mail e uma senha que não pertencem à mesma conta.    | O sistema impede o acesso.                     |
| Recuperação de senha                   | Verificar a opção de recuperação de senha, caso esteja disponível. | O sistema apresenta o processo de recuperação. |

## 9. Técnicas utilizadas

- Role Prompting — pedi para a IA assumir o papel de alguém que trabalha com testes de software.
- Contexto — expliquei que se tratava de um sistema acadêmico.
- Restrições — defini quais situações deveriam ser consideradas.
- Formato de saída — solicitei uma tabela para organizar os resultados.
- Refinamento iterativo — melhorei o prompt inicial para obter uma resposta mais completa.

## 10. Comparação entre os prompts

Comparando os dois resultados, percebi que o primeiro prompt trouxe apenas algumas ideias gerais de testes. Já o segundo apresentou informações mais completas, explicando melhor o que deveria ser feito e qual resultado era esperado.

A principal diferença foi a quantidade de informações fornecidas no pedido. Quando expliquei melhor o contexto e organizei as instruções, a resposta da IA também melhorou.

Por isso, considero que o segundo prompt foi mais eficiente para alcançar o objetivo da atividade.

## 11. Validação

Depois de analisar os resultados, percebi que os casos de teste apresentados fazem sentido para verificar uma tela de login.

Os cenários são simples de entender e podem ser utilizados como base para testes manuais. Mesmo assim, seria necessário executar cada um deles no sistema para confirmar se o comportamento esperado realmente acontece.

Também percebi que algumas situações dependem das funcionalidades que serão implementadas, como a recuperação de senha.

## 12. Ética e responsabilidade

Durante a atividade, percebi que não devemos confiar em tudo que a inteligência artificial apresenta. Ela pode ajudar bastante, mas também pode trazer informações incompletas ou sugerir algo que não existe no sistema.

Por isso, é importante analisar as respostas, conferir se fazem sentido e utilizar a IA como uma ferramenta de apoio, sem deixar de lado o nosso próprio conhecimento.

Também devemos evitar compartilhar informações pessoais ou senhas reais durante esse processo.

## 13. Take Away

Com essa atividade, entendi melhor a importância de saber como conversar com uma inteligência artificial.

Aprendi que não basta apenas fazer uma pergunta. É importante explicar o que queremos, apresentar o contexto e deixar claro como esperamos receber a resposta.

Também percebi que podemos melhorar bastante o resultado quando analisamos a primeira resposta e ajustamos o prompt. Dessa forma, a IA se torna uma ferramenta ainda mais útil nos estudos e no desenvolvimento de sistemas.

##
