# Desafio 3

# Técnicas de Testes com base na Experiência

### Participantes

Amanda Rossi

Camila Teixeira

Johnny Kamigashima

Raquel Sales

---

---

# Sumário

[Relatório de incidente – ISO-29119-3](https://docs.craft.do/editor/d/3a8c1925-8eba-6155-1bcd-1eb0dbcf2709/4FBC7C73-BEFE-4372-BFCD-263D013DE265/b/9500FBD9-50FD-4DB6-970A-D07DE2A3B6A0#D2C3632E-E8CF-45FE-90CE-4213D947DDB3)

[Retrospectiva](https://docs.craft.do/editor/d/3a8c1925-8eba-6155-1bcd-1eb0dbcf2709/4FBC7C73-BEFE-4372-BFCD-263D013DE265/b/9500FBD9-50FD-4DB6-970A-D07DE2A3B6A0#D1309D53-FB58-4662-B21C-8F122EC8A3CD)

[Referências](https://docs.craft.do/editor/d/3a8c1925-8eba-6155-1bcd-1eb0dbcf2709/4FBC7C73-BEFE-4372-BFCD-263D013DE265/b/9500FBD9-50FD-4DB6-970A-D07DE2A3B6A0#8E6B1456-13A3-40F7-A8A2-EB0EC4FE2EC4)

---

---

### Relatório de incidentes

# Dados de Teste:

Sistema: Lojinha WEB: [http://165.227.93.41/lojinha-web/v2/](http://165.227.93.41/lojinha-web/v2/)

Usuário: admin

Senha: admin

# Identificador único: #1

# Título

A tela de cadastro de produto fecha ao apresentar mensagem de validação de campos

# Informação de tempo

18/03/2023 20:00:00

# Originador

Raquel Sales

# Contexto

- Chrome versão 111.0.5563.65

# Técnica de Teste

Heurística FEW HICCUPPS - Produtos Comparáveis

“Produtos comparáveis. Esperamos que o sistema seja consistente com sistemas que sejam de alguma forma comparáveis. Isso inclui outros produtos da mesma linha de produtos; produtos, serviços ou sistemas concorrentes; ou produtos que não estão na mesma categoria, mas que processam os mesmos dados; ou processos ou algoritmos alternativos.”

# Pré-condição

   1. Estar logado na Lojinha.
   2. Utilizar navegador Google Chrome

# Descrição do incidente

Após seguir o passo a passo a seguir, a aplicação se comportou de maneira incorreta, relevando assim o incidente:

   1. Após realizar login no sistema
   2. Na tela principal, clicar no botão “Adicionar Produto”
   3. Não preencher nenhum dos campos
   4. Clicar em Salvar
   5. O sistema fecha a tela de cadastro de produto e volta para a tela principal
   6. E na tela principal, apresenta a mensagem “O valor do produto deve ser entre R$ 0,01 e R$ 7000,00”

# Resultado Esperado

Espera-se que as mensagens de validação sejam apresentadas na mesma tela de cadastro de produto e não voltem para a tela principal.

# Evidências:

![4322D480-17B4-492E-9520-DF6ABC258C3F.gif](https://res.craft.do/user/full/3a8c1925-8eba-6155-1bcd-1eb0dbcf2709/doc/4FBC7C73-BEFE-4372-BFCD-263D013DE265/D3F29CCA-E571-41DD-8F20-D1F8BC63A6DE_2/qGjl0yMO4TWXbj3HOoPXF2PhazDgsv5bAToGxw5lIoMz/4322D480-17B4-492E-9520-DF6ABC258C3F.gif)

# Avaliação da severidade

Média

# Avaliação de prioridade

Alta

# Risco

- Impacta na Usabilidade do Sistema, fazendo com que o usuário tenha que acessar novamente a tela de cadastro para concluir a ação.

# Status do incidente

Pendente

---

---

# Identificador único

\#20230318 2230

# Título

Item sem nome não é Alcançável

Informação de tempo

18/03/2023 22:30

# Originador

Johnny Kamigashima

# Contexto

- Estava usando o Chrome versão 111.0.5563.64
- Estava usando um computador desktop Mac com sistema Ventura 13.2.1
- O mesmo erro ocorre com o navegador Edge 111.0.1661.44

# Técnica de teste

ALTER FACE - Esta heurística de testes Web verifica se os elementos visíveis estão se comportando da forma esperada.

Ativação - Quando interagir com um elemento, este deve ter seu estado alterado de acordo com sua função.

Layers - As camadas de elementos visuais devem respeitar sua hierarquia e/ou sua ordem na tela e não podem cobrir outros elementos.

Timing - Elementos que aparecem e desaparecem em tempo definido devem fazê-lo conforme o esperado.

Exclusion - Elementos que não serão mais usados devem ser excluídos para que um novo elemento não caia sobre ele. E novos elementos não devem ocupar o mesmo espaço de outro anterior.

Removable - Elementos cuja função é remover e esconder e ser removidos devem fazê-lo.

Float - Elementos cuja função é flutuar sobre a tela precisam manter seu status flutuante mesmo ao navegar em outras partes da tela e fazer scroll, sem sumir nem esconder outro elemento.

Achievable - Elementos precisam ser acessíveis, mesmo em listas longas que não caibam em uma tela por meio de scroll e outra forma.

Collision - Um elemento não pode colidir com outro nem deformar a tela quando este altera sua posição.

Expansion - Quando um elemento altera seu formato, ele não deve deformar o seu ambiente nem distorcer outros elementos da tela.

# Descrição do incidente

Após efetuar os passos descritos abaixo, percebi que para o item ser editável, e Acessível, é necessário ter um nome, pois é a partir dele que tenho acesso.

Este elemento viola o princípio do Achievable desta Heurística, pois mesmo estando visível ele não permite acessibilidade.

Expectativa: O produto não deveria aceitar ser cadastrado sem nome e o produto, mesmo sem nome ou deveria possuir outra forma de acesso.

   1. Visite o endereço do site
   2. Clique em "Usuário"
   3. Digite "admin" no campo "Usuário"
   4. Digite "admin” no campo "Senha"
   5. Pressione Enter
   6. Clique em "Adicionar produto "
   7. Digite "3.99" no campo "Valor do Produto"
   8. Clique em "Salvar"
   9. Faça scroll para baixo
   10. Verifique se o produto cadastrado é acessível

# Evidências:

- Screenshot

![959368D9-8CE7-4AF2-9E3A-4668AA563A43.png](https://res.craft.do/user/full/3a8c1925-8eba-6155-1bcd-1eb0dbcf2709/doc/4FBC7C73-BEFE-4372-BFCD-263D013DE265/BE1A4DEA-8AFF-4314-9593-998682E05563_2/eUJbR3awNohHZiqis49wEj4pH57F02VMktOp76oyPR4z/959368D9-8CE7-4AF2-9E3A-4668AA563A43.png)

- Gif passo-a–passo

![5CD6457E-8F4A-48E4-96A3-021739373D43.gif](https://res.craft.do/user/full/3a8c1925-8eba-6155-1bcd-1eb0dbcf2709/doc/4FBC7C73-BEFE-4372-BFCD-263D013DE265/B0676E74-1ED5-442B-905A-1BEA1DC6D87B_2/3lTcvFsQ3sKxgvuJDfNOuevy3e53fyy9nTHLzFBlL5Qz/5CD6457E-8F4A-48E4-96A3-021739373D43.gif)

# Avaliação da severidade

Baixa

# Avaliação de prioridade

Alta

# Risco

- Produz itens sem utilidade no banco de dados

## Status do incidente

Pendente

## Observações:

Outras falhas poderiam ter sido encontradas usando técnicas mais rápidas de teste que não são cobertas por esta heurística. Michael Bolton diz que testes rápidos podem revelar outros defeitos superficiais antes de descobrir outros mais profundos.

Uma alternativa que poderia ter sido usada, se fosse possível voltar no tempo, seria a técnica de Testes por Sessões, que não segue um critério definido além do foco e do tempo e revela falhas, como a falha na regra de negócio onde o campo não deveria aceitar valor acima de 7000 reais, a falha de que o valor está sendo apresentado em formato numérico norte americano com ponto ao invés de vírgula e o fato do botão adicionar componente não estar disponível na tela de inclusão do produto.

---

---

## Identificador único

\#190323

## Título

Cor da borda inferior do campo não desaparece após perder o foco

## Informação de tempo

19/03/2023 17:49

## Originador

Amanda Rossi

## Técnica de teste

ALTER FACE

## Contexto

   - Estava usando o Chrome versão 109.0.5414.75
   - Estava usando um notebook com SO Windows 10
   - Estava usando os dados de login de usuário admin

## Descrição do incidente

Após realizar o passo a passo, a aplicação Lojinha Bugada se comportou de maneira incorreta conforme o princípio Removable da heurística ALTER FACE, apresentando assim o incidente:

   1. Realizei o login na lojinha;
   2. Cliquei em um produto para editá-lo;
   3. Cliquei no campo Nome do Produto;
   4. A label e a borda inferior do campo apresentam a cor da fonte #4CAF50 quando o campo está com foco;
   5. Cliquei no campo Valor do Produto;
   6. A borda inferior do campo Nome do Produto permaneceu com a cor de foco;
   7. O mesmo comportamento foi apresentado nos demais campos.

## Evidências:

Imagem com campo Cores do Produto em foco

![8EFB9BE9-ADC1-462C-978B-FCAB9A502CC4.png](https://res.craft.do/user/full/3a8c1925-8eba-6155-1bcd-1eb0dbcf2709/doc/4FBC7C73-BEFE-4372-BFCD-263D013DE265/DDC4FF32-8EE3-492F-BA3D-4D9A3156FBC7_2/z7RYzy8rQ8qj8ZUi0yofYzIrrNridn864WUmaW27mx0z/8EFB9BE9-ADC1-462C-978B-FCAB9A502CC4.png)

Vídeo com o passo a passo

![593E6CD1-92DB-4C01-ADF9-2D26D4B46147.gif](https://res.craft.do/user/full/3a8c1925-8eba-6155-1bcd-1eb0dbcf2709/doc/4FBC7C73-BEFE-4372-BFCD-263D013DE265/704DBA9D-84D7-46EA-91A0-FD1DB26946CD_2/sTseh21gJWJNP2j5PGbPv5istuialb39AvEefHKZazwz/593E6CD1-92DB-4C01-ADF9-2D26D4B46147.gif)

## Avaliação da severidade

Baixa

## Avaliação de prioridade

Baixa

## Risco

- Impacta na usabilidade da tela, não apresentando de forma clara qual campo está com o foco.

## Status do incidente

Pendente

---

---

## Identificador único

202303212031

## Título

Ativação/desativação dos campos dos formulários não seguem padrão no sistema.

## Informação de tempo

21/03/2023 20:31:12

## Originador

Camila Teixeira

## Contexto

   - Estava usando o Chrome versão 111.0.5563.111 - 64 bits
   - Estava utilizando sistema operacional Windows 11
   - Estava usando os dados de login disponibilizados para a tarefa

## Técnica de teste

   - Heurística ALTER FACE
   - Ativação - com esta heurística avaliamos se um elemento ativado por um evento, tem de fato seu estado alterado ao receber o evento esperado. No nosso incidente, o motion apresentado ao receber um clique no formulário de login, não foi apresentado nos demais formulários de cadastro e edição de produto.
   - Heurística CHIQUE
   - Habilitar/Desabilitar formulários: ao habilitar/ desabilitar um campo do formulário na tela de login observamos um comportamento e nos demais formulários da aplicação web observamos outro comportamento.
   - Heurística FEW HICCUPPS
   - Produto: esta heurística relata que esperamos que cada elemento do sistema (ou produto) seja consistente com objetos comparáveis dentro do mesmo sistema, o que não ocorreu ao não reproduzir o mesmo comportamento para todos os campos de formulários onde era possível realizar o preenchimento.

## Descrição do incidente

Após seguir o passo a passo a seguir, a aplicação não apresentou mesmo padrão nos campos semelhantes do formulário, revelando assim o incidente:

   1. Abri o Chrome
   2. Naveguei até a página [http://165.227.93.41/lojinha-web/v2/](http://165.227.93.41/lojinha-web/v2/)
   3. Digitei o usuário "admin"
   4. Digitei a senha "admin"
   5. Cliquei em "Fazer login"
   6. Ao entrar na lojinha, cliquei em “Adicionar produto”
   7. Preenchi os campos do formulário
   8. Cliquei em “Salvar”
   9. Cliquei em “Lista de produtos”
   10. Cliquei no último produto
   11. Preenchi os campos do formulário da tela de edição.
   12. Salvei.

## Evidências:

![CBEE1C7A-4C8B-4EC6-BB72-DAE0199C6F03.gif](https://res.craft.do/user/full/3a8c1925-8eba-6155-1bcd-1eb0dbcf2709/doc/4FBC7C73-BEFE-4372-BFCD-263D013DE265/555A545E-A46A-448D-ADAA-DDC15B6FB6D5_2/tqQReTG1yZl4nzS4woJGsyEiV9BHsuIqqgvwFOaQqsoz/CBEE1C7A-4C8B-4EC6-BB72-DAE0199C6F03.gif)

## Avaliação da severidade

Baixa

## Avaliação de prioridade

Baixa

## Risco

- Não impacta no uso do sistema, porém pode prejudicar a imagem do produto por não haver um padrão em seus elementos/componentes.

## Status do incidente

Pendente

---

---

# Retrospectiva

![FAB987C1-3410-4FB6-854C-0B0E2AC8C74F.png](https://res.craft.do/user/full/3a8c1925-8eba-6155-1bcd-1eb0dbcf2709/doc/4FBC7C73-BEFE-4372-BFCD-263D013DE265/4ED3C7B8-9799-40B1-87C4-3A4B225199F0_2/xhbM9QZ7QA8599HmZ0y4yyAaxdVGUL91IaUhFYbxLOQz/FAB987C1-3410-4FB6-854C-0B0E2AC8C74F.png)

---

---

> # Referências

Heurística ALTER FACE do Julio de Lima: [https://www.slideshare.net/juliodelimas/alter-face-test-heuristic-238982989](https://www.slideshare.net/juliodelimas/alter-face-test-heuristic-238982989)

Heurística FEW HICCUPPS de Michael Bolton:

[https://medium.com/artigos-traduzidos-do-rapid-software-testing/few-hiccupps-7b54fc1b36bc](https://medium.com/artigos-traduzidos-do-rapid-software-testing/few-hiccupps-7b54fc1b36bc)

Heurística CHIQUE do Julio de Lima:

[https://medium.com/revista-tspi/heur%C3%ADsticas-de-teste-de-software-o-que-s%C3%A3o-e-seus-benef%C3%ADcios-4a59996ca1ec](https://medium.com/revista-tspi/heur%C3%ADsticas-de-teste-de-software-o-que-s%C3%A3o-e-seus-benef%C3%ADcios-4a59996ca1ec)

