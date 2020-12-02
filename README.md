# Trabalho de Graduação

FATEC - Professor Jessen Vidal

Faculdade de Tecnologia de São José dos Campos

**Ciência de dados com aplicação em sistemas de navegação (GPS)**

### 1. INTRODUÇÃO

Desde o período da popularização dos aplicativos de navegação, é muito comum que eles sejam utilizados para identificação do caminho mais rápido a um destino em casos de congestionamentos, desviar de bloqueios na estrada, ou até mesmo com o intuito de informação para pessoas que não conhecem o lugar onde se encontram. Apesar de muito eficientes em seu propósito, tais aplicativos muitas vezes colocam em risco seus usuários, enviando eles através de caminhos desconhecidos, pouco estruturados e até mesmo arriscados, como exposto em 2017 pela revista Veja: "Ao confiarem nos percursos sugeridos por aparelhos e aplicativos de GPS para desviar-se de avenidas congestionadas ou blitz policiais, vários paulistanos têm colocado a vida em perigo. Isso porque as empresas do setor nem sempre conseguem bloquear as vias que representam risco à segurança." [1].

Uma reportagem feita pelo portal de notícias G1, em 2015, expõe também um dos casos em que um usuário de um aplicativo de navegação, foi atacado por traficantes enquanto procurava uma pizzaria com a ajuda do aplicativo [2]. Pensando em casos como estes, o sistema desenvolvido tem como objetivo aplicar mais uma camada no calculo das rotas, levando em consideração dados de segurança. A utilização da ciência de dados é vital para o funcionamento do projeto, que coleta dados fornecidos por órgãos governamentais e mapeia os locais com maior incidência de crimes na região da rota calculada e os pontuando, apenas após o cálculo da segurança da rota, a velocidade do trajeto seria considerada, dando como resultado final para o usuário a rota mais rápida dentro de um padrão de segurança. Atualmente os aplicativos tradicionais não levam dados de segurança em consideração, portanto, o sistema se categoriza como uma inovação no ramo.

#### 1.1. Objetivos

O projeto tem como objetivo o desenvolvimento de um sistema de navegação que, com a utilização de dados fornecidos pela Secretaria de Segurança Pública do estado de São Paulo, determine a rota mais segura até um destino limitado dentro da cidade de São José dos Campos.

Para atingir seus objetivos, o sistema coleta, limpa e interpreta os dados fornecidos sobre boletins de ocorrência, utiliza tais dados para o cálculo de uma pontuação para cada local em meio ao trajeto até o destino do usuário, e com a utilização desta pontuação, determinar qual o percurso que menos oferece risco ao usuário.

### 2. FUNDAMENTAÇÃO TÉCNICA 
