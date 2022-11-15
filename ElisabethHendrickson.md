# PTQS8D1 Elisabeth Hendrickson

---
Para a produção do desafio, pesquisei três autoras que abordavam temas de Testes de Software e Métodos ágeis, este é um resumo sobre Elisabeth Hendrickson, fundadora da Quality Tree Software e membro de várias empresas e organizações voltadas à qualidade de software ela escreveu sua primeira linha de código em 1980 e encontrou seu primeiro bug. Defende fortemente os testes exploratórios e visão de testes baseados em heurística, seu livro mais conhecido é Explore it!

No seu post sobre o tema CRUD (*Create, Read, Update, Delete*), Elisabeth Hendrickson explica sobre a heurística e as várias possibilidades de explorar um sistema que tenha banco de dados, seja ele com cadastro de clientes, produtos e até envio de e-mails pois os sistemas são geralmente pensados para seguir sequências pré-determinadas como a sigla acima, mas isso não significa que o usuário pense desta forma ou, por algum motivo, o sistema caminhe por outro trajeto DRUC, por exemplo.

Uma falha no sistema que permita que seja apagado um registro no mecanismo de procura, quebre o sistema após remover todos os itens do estoque, mantenham dependentes cujos pais foram removidos podem gerar falhas graves de segurança, perda de desempenho, ocupação indevida de espaço no banco de dados entre outros problemas.

Em outro caso a autora descreve a criação de um software que simula o aparecimento aleatório de bugs. Neste software a quantidade de bugs era ajustada em uma escala entre 0 e 1, quanto maior a qualidade menor a quantidade de bugs, porém, o resultado não foi como esperado. A princípio a simulação resultou que para 100% qualidade o resultado foi 0 bug, mas baixando a qualidade um pouco o resultado explodia em bugs.

Com a ajuda de um desenvolvedor especialista, descobriu-se que realmente o resultado estava mais próximo da realidade do que se esperava, pois no início a cada entrega havia uma chance de criar um bug, mas não somente na funcionalidade entregue e, sim, também nas funcionalidades já entregues anteriormente o que fazia com que no final de centenas de entregas houvesse centenas de bugs.

De acordo com Elisabeth, o desenvolvimento de um software não segue uma linearidade, e, por linearidade, define-se que a causa e efeito não são proporcionais nem imediatos. Isso pode causar prazos de entregas não proporcionais à implementação do produto, causando atrasos e falhas na qualidade.

Em um exemplo, o dono do produto pediu para o desenvolvimento corrigir uma letra no código, uma alteração simples, em uma classe de base, mas complexa pois por conta de objetos com características herdadas, fez com que todo o sistema quebrasse. Esse tipo de problema pode acontecer em atualizações de dependências e patches de segurança, essenciais e necessários.

Fazer testes no sistema alterando a sequência esperada e verificar os logs do sistema são algumas das formas de verificar possíveis falhas nesses processos, principalmente quando eles são acionados indiretamente ou assíncrona e o resultado pode não ser visível para o usuário imediatamente. Por isso é necessário fazer pequenas mudanças, testar e automatizar os testes regressivos, manter o código versionado, tratar configurações como código e entregar de forma incremental e frequente.

---
Veja mais sobre Elisabeth Hendrickson em:

https://www.youtube.com/watch?v=9FKY1Is0lgs 

https://medium.com/search?q=elisabeth+hendrickson 

https://www.curiousduck.io