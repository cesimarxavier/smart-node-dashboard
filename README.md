# SmartNode Dashboard

O SmartNode Dashboard é um *framework* que foi criado a partir da base de código do [Bootstrap](http://getbootstrap.com). Sua proposta é fornecer um código base para criação de Dashboads a partir dos elementos _cards_. Os *cards* são padrões de interfaces altamente versáteis e por isso sua utilização é muito interessante para ser utilizada neste projeto. 

Por ter sido derivado do Bootstrap, esse _framework_ estende também as mesmas convenções de código. Além disso ela utiliza a arquitetura de código CSS [BEM](http://getbem.com/). A intenção principal deste projeto é fornecer aos programadores que precisam lidar com a criação de interfaces para _dashboards_ ter uma ferramenta que ajude a produzir projetos mais eficazes e num curto espaço de tempo. Além do mais, é possível criar novos formatos a partir da estrutura proposta no _SmartNode Dashboard_.

## 1. Iniciando
Há duas opções de iniciar utilizando o framework.
* [Baixando a versão estável atual](https://github.com/smart-node-dashboard/zipball/master).
* Fazendo um clone do repositório: `git clone git://github.com/smart-node-dashboard.git`.

### 1.1 Arquitetura e funcionamento

A figura abaixo mostra a arquitetura de um _card_ utilizado para exibir os dados no _dahsboard_.

![Arquitetura do Card](https://raw.githubusercontent.com/cesimar/smart-node-dashboard/master/arquitetura-card.jpg)

O container de _card_ é subdivido internamente em três partes de conteúdo. Cada classe representa um bloco e sua funcionalidade.

1. __*.card*:__ classe básica do _container_. É responsável pela formatação do bloco principal e formatação geral do bloco;
2. __*.card__header*:__ classe responsável por formatar o bloco de cabeçalho do _card_. Esse bloco é responsável por exibir detalhes de identificação do _card_;
3. __*.card__body*:__ classe que formata os elementos de conteúdo. O bloco de conteúdo que é formatado por esta classe, contém três sub-blocos, que dividem o espaço de conteúdo e que pode ser formatado livremente. Os blocos internos são:  
    *__.card__body__top__: um bloco para conteúdo acima; 
    * __.card__body__content__: utilizado para incluir o contéudo principal;
    * __.card__body__down__: bloco para conteúdo complementar;
4. __*.card__footer*:__ classe responsável pela formatação do bloco de rodapé. Esse bloco é indicado para incluir funcionalidades de interação (como links e botões, por exemplo).

![Card de Tempo](https://raw.githubusercontent.com/cesimar/smart-node-dashboard/master/arquitetura-card-tempo.jpg)

A figura acima mostra uma exemplo de utilização de um _card_ customizado para apresentar informações sobre o tempo. Esse exemplo está disponível na coleção de _cards_ de exemplos já customizados e disponíveis nessa versão do _framework_.

### 1.2 Cards de exemplo disponíveis
O projeto conta com alguns elementos básicos já disponíveis (_cards_ e gráficos). Cada _card_ tem uma funcionalidade específica e sua customização é apenas uma estilização simples que pode ser facilmente modificada. Atualmente o framework conta com os seguintes elementos:

| _Card_                        | Classe Modificadora  |
| ----------------------------- |:--------------------:|
| Card de Tempo                 | .card--tempo         |
| Card de Bikes                 | .card--bike          |
| Card de Qualidade do Ar       | .card--ar            |
| Card de Trânsito              | .card--transito      |
| Card de Eventos Culturais     | .card--news          | 
| Card de Linhas de Ônibus      | .card--bus           |
| Card de Câmeras de Trânsito   | .card--cameras       |

### 1.3 Contribuir com o _SmartNode Dashboard_
Os programadores podem contribuir enviando novos _cards_ para este repositório.

## 2. Usando o SmartNode Dashboard

O código abaixo mostra o código básico de uso de um _card_. A customização será a padronizada no _framework_.

```html
    <section class="card">
      <section class="card__header">
        <!-- texto do título -->
      </section>

      <section class="card__body">
        <div class="card__body__top">
          <!-- texto do complementar -->
        </div>
        <div class="card__body__content">
          <!-- texto do conteúdo principal -->
        </div>
        <div class="card__body__down">
          <!-- texto do complementar -->
        </div>
      </section>

      <section class="card__footer">
        <!-- conteúdo de interação -->
      </section>
    </section>
```

O código abaixo mostra o _card_ sendo modificado para um tipo específico de visualização. O _card_ de tempo. Perceba que nesse código a única alteração foi na classe extra incluída no container principal do _card_. Dessa forma é possível reescrever ou apenas sobrepor a funcionalidade pré-existente do elemento tempo.

```html
    <section class="card card--tempo">
      <section class="card__header">
        <!-- texto do título -->
      </section>

      <section class="card__body">
        <div class="card__body__top">
          <!-- texto do complementar -->
        </div>
        <div class="card__body__content">
          <!-- texto do conteúdo principal -->
        </div>
        <div class="card__body__down">
          <!-- texto do complementar -->
        </div>
      </section>

      <section class="card__footer">
        <!-- conteúdo de interação -->
      </section>
    </section>
```
