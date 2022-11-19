PTQS – Programa de Teste e Qualidade de Software
===================================================
Mentor: Júlio de Lima
=====================

Turma 8 | Desafio 2  

======================

Alunos: Johnny Kamigashima [https://www.linkedin.com/in/kamigashima](https://www.google.com/url?q=https://www.linkedin.com/in/kamigashima&sa=D&source=editors&ust=1668902282084060&usg=AOvVaw0Dvu69FeFkgY79aKhKU0g4),  
Miller Barros [https://www.linkedin.com/in/miller-c-barros-a6a514227/](https://www.google.com/url?q=https://www.linkedin.com/in/miller-c-barros-a6a514227/&sa=D&source=editors&ust=1668902282084379&usg=AOvVaw2rL1sBm74mrXE8fxfsUQjh), 
Rafael Angelo da Costa [https://www.linkedin.com/in/rafaelangelodacosta/](https://www.google.com/url?q=https://www.linkedin.com/in/rafaelangelodacosta/&sa=D&source=editors&ust=1668902282084630&usg=AOvVaw2tfwavQlOTjljq25qc9NBm),
Vitor Silva [https://www.linkedin.com/in/vitor-victoria-da-silva-703006199/](https://www.google.com/url?q=https://www.linkedin.com/in/vitor-victoria-da-silva-703006199/&sa=D&source=editors&ust=1668902282084871&usg=AOvVaw3ffR4b9GUF7CUUoaUOP7Ev)

![](images/image37.png)

Ferramenta Testlink para gestão de testes

* * *

Testlink é uma ferramenta utilizada para gerenciar testes de forma colaborativa e acessível para toda a equipe. É uma ferramenta open source, organizada e de fácil utilização, que possibilita: criar projeto, plano de teste, criar/gerir casos de teste, podendo anexar evidências de cada teste, gerar relatórios com resultados dos testes, atribuir os testes para quem irá testar, independente da quantidade de testadores, filtrar testes por testador, integrar com ferramenta de gestão de bug, fazer integração com automação de testes, etc.

* * *

Terminologias da Ferramenta
---------------------------

Neste tutorial mostraremos as principais funções da ferramenta TestLink. A seguir:

### Projeto de teste

O projeto de teste é o primeiro elemento a ser criado no aplicativo, nele serão adicionados recursos, funcionalidades, documentação de requisitos, especificações de teste, planos de testes e direitos de usuários.

Os projetos de testes são independentes e não compartilham dados com outros projetos de teste, em geral são utilizados somente um projeto de teste por equipe ou produto.

### Plano de teste

É o primeiro elemento base para execução dos testes, um plano de teste possui nome, descrição, coleção de dados de teste, versão, resultados de teste, marcos, atribuição de teste e definição das prioridades. Cada plano de teste está subordinado a um Projeto de testes.

### Build, Release, Baseline

O software que faz parte do projeto sofre modificações ao decorrer do tempo, e a cada nova modificação é atribuída uma versão, o Testlink considera essas versões nos seus casos de testes.

### Suíte de teste

No Testlink uma suíte de teste é organizada em formato de árvore de casos de testes com nome e descrição de cada caso.

### Casos de teste

Casos de teste são conjunto de verificações de uma determinada funcionalidade contendo entradas, condições e resultados esperados.

### Plataforma

As plataformas podem ser divididas em navegadores, sistemas operacionais ou dispositivos.

* * *

Fazendo Login no Testlink
-------------------------

![Imagem de login do testlink](images/image27.png "Imagem de login do testlink")

#### Tela de login do Testlink

1.  ##### Navegue até o endereço instalado do testlink, fornecido pelo responsável pelo sistema e preencha seus dados de login e senha.
    
2.  ##### Caso você ainda não tenha usuário cadastrado, clique em Novo Utilizador, faça o cadastro e peça para o responsável pelo sistema aprovar o cadastro e atribuir um nível de usuário.
    

* * *

Iniciando um Projeto de Teste no TestLink
-----------------------------------------

![](images/image26.png)

#### Menu principal do TestLink

![](images/image7.png)

#### Sempre que desejar voltar ao menu inicial clique na casinha ou no logo

* * *

I – Criando um projeto de teste
-------------------------------

No Testlink é necessário inicialmente ter um projeto, esta etapa seria a primeira etapa para configurar seu projeto.

##### 1.1 – No menu principal, clique na opção “Gerenciar Projeto de Teste”.

##### ![](images/image45.png)

##### 1.2 – Clique no botão “CRIAR”.

![](images/image42.png)

##### 1.3 – Preencha os dados do “Projeto”.

###### Aqui é importante detalhar informações que sejam de interesse a todos os participantes. Você pode criar um novo projeto a partir de um projeto existente ou criar um projeto individual, adicionar um prefixo, que será usado para nomear testes e selecionar adições como funcionalidade de requisitos, prioridades, etc.

###### A opção ‘Ativo’ significa que este projeto já está pronto para uso e acessível para todos os participantes, porém é possível iniciar um projeto no estado ‘inativo’ e habilitar essa opção depois de ter tudo configurado.

###### A opção ‘público’ habilita outros usuários do aplicativo que não estejam no projeto a visualizá-lo.

###### Ao finalizar, clique em criar.

![](images/image46.png)

##### 1.4 – Selecione o projeto

###### Uma vez criada, selecione o projeto no canto superior direito do aplicativo.

![](images/image13.png)

* * *

II – Criando um Plano de Teste
------------------------------

##### 2.1 – No menu principal clique na opção “Gerenciar Plano de Teste”.

![](images/image31.png)

#####  2.2 – Clique na opção “CRIAR”, para criar um novo Plano de Teste.

![](images/image41.png)

##### 2.3 – Preencha os dados do “Plano de teste”

###### Assim como em projeto, é importante preencher informações relevantes ao plano de teste tais como o seu objetivo e delimitações. Nesta etapa também é possível criar a partir de outro plano já existente, deixar ativo e público.

###### Ao finalizar clique em criar.

![](images/image3.png)

##### 2.4 – Selecione o Plano de teste

###### No canto superior direito, logo abaixo do projeto, selecione o plano de teste atual.

![](images/image35.png)

* * *

* * *

III – Criando Baseline/Release
------------------------------

##### 3.1 – No menu principal, clique na opção “Baselines / Releases”.

![](images/image9.png)

##### 3.2 – Clique na opção “Criar”.

![](images/image20.png)

##### 3.3 – Na tela de “Baseline / Releases” configure as informações.

###### Ao criar uma Baseline você estará definindo qual versão do software que será testado, também pode ser classificada por data. Acrescente informações sobre este release e observações que devem ser levadas em conta.

###### Nesta tela você também tem a opção de deixar ‘Ativo e Aberto’ para testes, além de outros metadados caso você tenha necessidade para indexar em outro sistema. A opção ‘Dado do Release’ permite escolher uma data, utilizando um seletor mini calendário.

###### Ao finalizar, clique em “Criar”.

​​![](images/image19.png)

* * *

IV – Criando Plataformas
------------------------

##### 4.1 – No menu principal, clique em “Gerenciamento de Plataformas”

![](images/image12.png)

##### 4.2 – Clique em “Criar”

![](images/image32.png)

##### 4.3 – Preencha as informações da plataforma

‘Plataforma’ é o ambiente onde os testes serão executados. Exemplo: Navegador Chrome, Firefox, Android, iOS, etc.  
Dê um nome fácil de entender e uma descrição detalhada do sistema, modelo do equipamento e sistema operacional.

Deixe somente a opção “On execution” ativada para que possa ser utilizada nos testes, caso contrário ela não será selecionável.

Ao final clique em Gravar.

Adicione quantas plataformas sejam necessárias para o projeto, uma vez adicionadas elas poderão ser utilizadas inúmeras vezes dentro do mesmo projeto e não é necessário adicionar novamente.

![](images/image24.png)

##### 4.4 – No menu principal, atribua plataformas ao Plano de teste

Clique em Adicionar / Remover Plataformas

![](images/image6.png)

##### 4.5 – Selecione as plataformas e atribua utilizando as setas > ou >> e clique em “Gravar”

![](images/image43.png)

* * *

V – Criar Suíte de testes e Casos de testes
-------------------------------------------

##### 5.1 – No menu principal, clique em “Especificar Casos  de Teste”

![](images/image2.png)

##### 5.2 – Clique na engrenagem para abrir mais opções

![](images/image8.png)

##### 5.3 – Clique no ícone de +

![](images/image22.png)

* * *

##### 5.4 – Preencha os dados da suíte de testes

A suíte de testes é o diretório onde se encontrarão os casos específicos de testes para o determinado projeto de teste. Poderão existir inúmeras suítes de teste dependendo dos cenários projetados.

Preencha o nome da suíte e sua descrição, caso queira organizar por palavras chaves, atribua no campo abaixo. (as palavras chaves precisam ser adicionadas anteriormente através do menu principal)

Ao final clique em “Gravar”

![](images/image1.png)

##### 5.5 – Editar suíte de testes e criar Casos de teste

###### Após criar a suíte de testes você poderá selecionar no navegador à esquerda, selecionando o ícone da engrenagem, será disponibilizado opções para editar, mover, deletar, exportar Suítes de teste e Casos de teste.

![](images/image40.png)

* * *

##### 5.6 – Crie Casos de Teste

Ao selecionar no menu anterior o ícone +, atribua nomes e descrições para os casos de testes, nesta janela é possível definir objetivo, pré-condição, status, prioridade, tempo estimado de execução e tipo de execução (manual/automatizado).

Ao final clique em “Criar”

![](images/image21.png)

##### 5.7 – Após criar um teste, selecione-o no navegador à esquerda

![](images/image39.jpg)

##### 5.8 – Clique em ‘Criar um passo’ para especificar os passos do teste

![](images/image10.png)

##### 5.9 – Preencha o passo e clique em “Gravar” para inserir o próximo passo ou “Gravar e sair” para concluir

![](images/image36.jpg)

##### 5.10 – De volta na página de Caso de teste, clique na engrenagem novamente e depois em “Adicionar aos Planos de Teste”

![](images/image15.png)

##### 5.11 – Selecione os checkboxes dos testes a serem adicionados e clique em “Adicionar”

![](images/image30.png)

* * *

* * *

VI – Como atribuir testes para execução
---------------------------------------

##### 6.1 – A partir do menu principal clique em “Atribuir Casos de Teste para execução”

![](images/image11.png)

##### 6.2 – Selecione o Plano, Plataforma e Baseline/Build para atribuir o teste

![](images/image33.png)

##### 6.3 - Selecione o “Caso de Teste”

![](images/image16.png)

##### 6.4 – Selecione o ‘usuário’ a fazer os testes e selecione na lista quais testes serão atribuídos a este usuário. É possível selecionar mais de um usuário.  
Em seguida clique no botão “Aplicar Atribuição” e “Gravar Atribuições”

![](images/image5.png)

![](images/image23.png)

* * *

VII – Executar testes
---------------------

##### 7.1 – A partir do menu principal selecione “Executar Testes”

![](images/image17.png)

##### 7.2 – Selecione o teste a ser executado

![](images/image25.png)

##### 7.3 – Nesta tela o usuário terá todas as informações pertinentes ao teste e os passos que precisam ser seguidos

![](images/image44.png)

* * *

##### 7.4 – Execute o teste

        Passo 1: Acessar página de login disponível no link …. (esses passos estão na imagem acima).

        Passo 2: Informar ‘usuário e senha’ e clicar no botão entrar …

\>> Mensagem ‘Boas vindas, admin!’ é exibida.

![](images/image29.jpg)

![](images/image4.jpg)

##### 7.5 – Ao completar o teste, marque na página se a etapa passou e adicione comentários da etapa.

![](images/image18.png)

##### 7.6 – Ao final do teste anote o tempo usado e selecione nos ícones (![](images/image14.png)) se o teste passou, falhou ou foi bloqueado.

![](images/image38.png)

##### 7.7 – Clique no ícone de pasta ao lado esquerdo do nome do caso de teste para ‘anexar evidências’ do resultado do teste.

![](images/image34.png)

##### 7.8 – No final da página selecione “Escolher arquivo” para anexar a prova de execução e clique em “Enviar arquivo”

![](images/image28.png)

* * *

* * *

Sumário
-------

[PTQS – Programa de Teste e Qualidade de Software](#h.oai13f14n8la)

[Terminologias da Ferramenta](#h.b3d9vrtc1eha)

[Projeto de teste](#h.ph1khpi1qtcg)

[Plano de teste](#h.tkpyt1dhnuou)

[Build, Release, Baseline](#h.rc3oi7v76u44)

[Suíte de teste](#h.tycjjrt77vp4)

[Casos de teste](#h.o7etjhnl77ns) 

[Plataforma](#h.w6nbzvdpcdy0)

[Fazendo Login no Testlink](#h.7ulit9kbsn08)

[Tela de login do Testlink](#h.xnalhjrwv8zd)

[Iniciando um Projeto de Teste no TestLink](#h.uq0y98osgb25)

[Menu principal do TestLink](#h.ilyzkdsgap3n)

[I – Criando um projeto de teste](#h.bmi2jrm28pad)

[II – Criando um Plano de Teste](#h.uuhw04ehe1ne)

[III – Criando Baseline/Release](#h.nw4zm2m15s4l)

[IV – Criando Plataformas](#h.9wc3hd8hhf05)

[V – Criar Suíte de testes e Casos de testes](#h.2magmrimi16q)

[VI – Como atribuir testes para execução](#h.3jc482yjvlck)

[VII – Executar testes](#h.y9d0u8qapsmu)

* * *

Referências: Testlink distribuído pela Bitnami - [https://hub.docker.com/r/bitnami/testlink](https://www.google.com/url?q=https://hub.docker.com/r/bitnami/testlink&sa=D&source=editors&ust=1668902282116390&usg=AOvVaw0OHxTzQ9LxZyJctT48pki7), Manual da versao anterior no medium: [https://medium.com/@luanasreis/testlink-uma-ferramenta-de-gerenciamento-de-testes-de-software-44001b816f64](https://www.google.com/url?q=https://medium.com/@luanasreis/testlink-uma-ferramenta-de-gerenciamento-de-testes-de-software-44001b816f64&sa=D&source=editors&ust=1668902282116761&usg=AOvVaw2Cz3qPSR_hROMv4pzCvqrL) 

A versão utilizada para este tutorial foi 1.9.20 \[DEV, a última disponibilizada pela Bitnami antes dela abandonar o projeto.\]