# Projeto Deputados e Partidos - Integração com API da Câmara dos Deputados

Este projeto é uma aplicação web que faz uso das APIs públicas da Câmara dos Deputados do Brasil. O objetivo é exibir uma lista de partidos políticos e, ao selecionar um partido, mostrar os deputados associados a ele.

## Funcionalidades

- Exibir uma lista de partidos políticos, ordenada pela sigla.
- Exibir detalhes do partido selecionado.
- Ao clicar em "Listar Deputados", exibir todos os deputados vinculados ao partido escolhido.

## Tecnologias Utilizadas

- **HTML5**: Estruturação da página.
- **CSS3**: Estilização e layout visual.
- **JavaScript (ES6)**: Manipulação de dados e interação com a API.
- **API da Câmara dos Deputados**: Fornece informações sobre partidos e deputados.

## Estrutura do Projeto

- `index.html`: Arquivo principal que contém a estrutura HTML, os estilos CSS e os scripts JavaScript.

## Fluxo da Aplicação

1. **Carregamento Inicial**:
   - Ao abrir a aplicação, a função `carregarPartidos()` é executada, realizando uma requisição à API para obter a lista de partidos, que são exibidos em uma lista interativa.

2. **Seleção de Partido**:
   - Ao clicar em um partido da lista, os detalhes (nome e ID) são exibidos na área de informações.
   - Um botão "Listar Deputados" é habilitado para que o usuário possa visualizar os deputados relacionados ao partido.

3. **Exibição dos Deputados**:
   - Ao clicar em "Listar Deputados", a função `carregarDeputados()` é chamada, enviando uma solicitação à API de deputados, com base na sigla do partido selecionado.
   - A lista de deputados é exibida abaixo dos detalhes do partido e atualizada sempre que um novo partido é escolhido.

## APIs Utilizadas

1. **API de Partidos**:
   - URL: `https://dadosabertos.camara.leg.br/api/v2/partidos`
   - Parâmetros: `ordem=ASC&ordenarPor=sigla`

2. **API de Deputados**:
   - URL: `https://dadosabertos.camara.leg.br/api/v2/deputados`
   - Parâmetros: `ordem=ASC&ordenarPor=nome&siglaPartido={SIGLA}`

## Como Executar o Projeto

1. Clone este repositório:
    ```bash
    git clone https://github.com/seu-usuario/deputados-partidos.git
    ```

2. Abra o arquivo `index.html` em seu navegador preferido.

3. A aplicação carregará automaticamente a lista de partidos. Clique em um partido para ver seus detalhes, e depois em "Listar Deputados" para visualizar os deputados associados ao partido selecionado.
