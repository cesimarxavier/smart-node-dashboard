# SmartNode Dashboard

O SmartNode Dashboard é um *framework* que foi criado a partir da base de código do [Bootstrap](http://getbootstrap.com). Sua proposta é fornecer um código base para criação de Dashboads a partir dos elementos _cards_. Os *cards* são padrões de interfaces altamente versáteis e por isso sua utilização é muito interessante para ser utilizada neste projeto. 

Por ter sido derivado do Bootstrap, esse _framework_ estende também as mesmas convenções de código. Além disso ela utiliza a arquitetura de código CSS [BEM](http://getbem.com/). A intenção principal deste projeto é fornecer aos programadores que precisam lidar com a criação de interfaces para _dashboards_ ter uma ferramenta que ajude a produzir projetos mais eficazes e num curto espaço de tempo. Além do mais, é possível criar novos formatos a partir da estrutura proposta no _SmartNode Dashboard_.

## Iniciando
Há duas opções de iniciar utilizando o framework.
* [Baixando a versão estável atual](https://github.com/smart-node-dashboard/zipball/master).
* Fazendo um clone do repositório: `git clone git://github.com/smart-node-dashboard.git`.

### Arquitetura do Código

A figura abaixo mostra a arquitetura de um _card_ utilizado para exibir os dados no _dahsboard_.

![Arquitetura do Card](https://raw.githubusercontent.com/cesimar/smart-node-dashboard/master/arquitetura-card.jpg)

O container de _card_ é subdivido internamente em três partes de conteúdo. Cada classe representa um bloco e sua funcionalidade.

1. __*.card*:__ classe básica do _container_. É responsável pela formatação do bloco principal e formatação geral do bloco;
2. __*.card__header*:__ classe responsável por formatar o bloco de cabeçalho do _card_. Esse bloco é responsável por exibir detalhes de identificação do _card_;
3. __*.card__body*:__ classe que formata os elementos de conteúdo. O bloco de conteúdo que é formatado por esta classe, contém três sub-blocos, que dividem o espaço de conteúdo e que pode ser formatado livremente. Os blocos internos são:  * __.card__body__top__: um bloco para conteúdo acima; 
  * __.card__body__content__, que é organizado para ser o elemento do conteúdo principal e;
  * __.card__body__down__, bloco para conteúdo complementar;  
4. __*.card__footer*:__ classe responsável pela formatação do bloco de rodapé. Esse bloco é indicado para incluir funcionalidades de interação (como links e botões, por exemplo).

### Elementos
O projeto conta com alguns elementos básicos (_cards_ e gráficos). Nesta primeira versão ele conta apenas com _cards_. Cada _card_ tem uma funcionalidade específica. Atualmente o framework conta com os seguintes elementos:

* Card de Tempo
* Card de Bikes (estações de aluguéis de bicicletas)
* Card de Qualidade do Ar
* Card de Trânsito
* Card de Novidades e Tendências
* Card de Ônibuss
* Card de Câmeras de Trânsito
* Card de Mapas da Cidade

