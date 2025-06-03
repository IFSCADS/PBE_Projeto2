# Projeto 2: um sistema de leilão online

Neste projeto, sua equipe deverá desenvolver o backend para uma aplicação para leilão online. A aplicação deve possibilitar fazer tanto leilões para compra ou venda de bens e serviços.

## Introdução

A atividade de leilão envolve possibilitar que interessados disputem pela aquisição de um produto de forma sistemática. Em um leilão, participantes podem fazer lances, em que cada lance deve oferecer um preço malhor do que o lance anterior. Ao final do leilão, o autor do maior lance vence a disputa, dando-lhe direito ao bem ou serviço leiloado. Veja alguns exemplos de serviço de leilão:
* [Leilão online](https://www.leilaoonline.net/)
* [Leilão eletrônico da Receita Federal](https://www.leilaoonline.net/)
* [Leilão de imóveis da Caixa Econômica Federal](https://www.caixa.gov.br/voce/poupanca-e-investimentos/acoes-online/leiloes/Paginas/default.aspx)

Um pregão é parecido com um leilão, porém ao invés de comprar um bem, os participantes disputam para vender um bem ou serviço. A dinâmica é parecida com a do leilão, porém ao final vence o autor do menor lance ofertado. Isso lhe dará o direito de vender o bem ou serviço para o contratante do pregão. Alguns exemplos de sistemas de pregão são:
* [ComprasBR](https://comprasbr.com.br/pregao-eletronico/?status=AGUARDANDO_ABERTURA&utm_source=Google&utm_medium=Pesquisa&utm_campaign=AN009_pregao_de_moveis)
* [Portal de Compras do Governo Federal](https://www.gov.br/compras/pt-br)

## Descrição da aplicação

Sua aplicação deve ser desenvolvida usando um destes frameworks:
* Spring Boot
* Express.JS

Seguem os requisitos para a aplicação:
* Cada leilão é composto de: data e hora do início, duração, item leiloado (nome, descrição, valor inicial) e tipo de leilão (compra ou venda).
  * Em leilões do tipo compra, a oferta vencedora é a com menor preço. Se tipo venda, é a com maior preço.
* Um leilão deve ser iniciado automaticamente de acordo com sua data e horário de início, e terminado também automaticamente, em função da duração programada.
* A aplicação deve ser capaz de realizar múltiplos leilões simultaneamente
* Administradores podem cadastrar, modificar e excluir leilões. Leliões em andamento não podem ser modificados ou excluídos.
* Participantes devem estar cadastrados para poderem participar do leilão. O cadastro é formado por: nome e CPF
* Um participante pode consultar leilões futuros e em andamento. Quando em andamento, a resposta deve incluir os lances feitos até o momento
* Um participante pode participar de um leilão, e então fazer ofertas e receber notificações de ofertas feitas por outros usuários.
  * Faltando um minuto para encerrar, o participante receberá notificações de alerta a cada 10 segundos.
  * Se leilão encerrar, uma notificação informa a todos os participantes o lance vencedor, e ao participantes vencedor a notificação inclui um aviso de que seu lance venceu o leilão.
* Um usuário pode participar de múltiplos leilões simultaneamente
* As informações sobre leilões e usuários devem ser persistentes

Crie seu backend explorando o que foi estudado até o momento. Isso envolve:
* Especificar a API do seu backend: ela pode ser uma composição de um ou mais tipos de API estudados. Não esqueça de documentá-la !
* Definir a arquitetura do backend: pense em como os elementos de software estarão organizados e relacionados
* Conceber e descrever o modelo de software: use os conhecimentos vistos em Engenharia de Software para modelar seu backend. Esse modelo deve ser descrito usando as ferramentas de modelagem estudadas, dentre elas diagramas  estruturais e comportamentais.
* Modelar o armazenamento dos dados: como as informações devem persistir, será necessário usar um banco de dados. Define o modelo relacional dos dados, e use um ORM para acessá-los.

Por fim, para fins de demonstração, crie também um frontend para acesso à aplicação. Pode ser um frontend simplificado, porém que possibilite o pleno uso da aplicação.
