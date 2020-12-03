# Trabalho de Graduação

FATEC - Professor Jessen Vidal

Faculdade de Tecnologia de São José dos Campos

**Ciência de dados com aplicação em sistemas de navegação (GPS)**

## 1. INTRODUÇÃO

Desde o período da popularização dos aplicativos de navegação, é muito comum que eles sejam utilizados para identificação do caminho mais rápido a um destino em casos de congestionamentos, desviar de bloqueios na estrada, ou até mesmo com o intuito de informação para pessoas que não conhecem o lugar onde se encontram. Apesar de muito eficientes em seu propósito, tais aplicativos muitas vezes colocam em risco seus usuários, enviando eles através de caminhos desconhecidos, pouco estruturados e até mesmo arriscados, como exposto em 2017 pela revista Veja: "Ao confiarem nos percursos sugeridos por aparelhos e aplicativos de GPS para desviar-se de avenidas congestionadas ou blitz policiais, vários paulistanos têm colocado a vida em perigo. Isso porque as empresas do setor nem sempre conseguem bloquear as vias que representam risco à segurança." [1].

Uma reportagem feita pelo portal de notícias G1, em 2015, expõe também um dos casos em que um usuário de um aplicativo de navegação, foi atacado por traficantes enquanto procurava uma pizzaria com a ajuda do aplicativo [2]. Pensando em casos como estes, o sistema desenvolvido tem como objetivo aplicar mais uma camada no calculo das rotas, levando em consideração dados de segurança. A utilização da ciência de dados é vital para o funcionamento do projeto, que coleta dados fornecidos por órgãos governamentais e mapeia os locais com maior incidência de crimes na região da rota calculada e os pontuando, apenas após o cálculo da segurança da rota, a velocidade do trajeto seria considerada, dando como resultado final para o usuário a rota mais rápida dentro de um padrão de segurança. Atualmente os aplicativos tradicionais não levam dados de segurança em consideração, portanto, o sistema se categoriza como uma inovação no ramo.

### 1.1. Objetivos

O projeto tem como objetivo o desenvolvimento de um sistema de navegação que, com a utilização de dados fornecidos pela Secretaria de Segurança Pública do estado de São Paulo, determine a rota mais segura até um destino limitado dentro da cidade de São José dos Campos.

Para atingir seus objetivos, o sistema coleta, limpa e interpreta os dados fornecidos sobre boletins de ocorrência, utiliza tais dados para o cálculo de uma pontuação para cada local em meio ao trajeto até o destino do usuário, e com a utilização desta pontuação, determinar qual o percurso que menos oferece risco ao usuário.

## 2. FUNDAMENTAÇÃO TÉCNICA 

Para o desenvolvimento técnico deste projeto, serão abordados principalmente os conceitos de geolocalização e ciência de dados. Para o desenvolvimento do aplicativo, serão utilizadas APIs em arquitetura REST e linguagens para desenolvimento de aplicativos nativos para celular.

### 2.1 Geolocalização

O conceito de geolocalização, consite na localização geográfica de um dispositivo no planeta terra através de um satélite, dispositivo este, que necessita de conexão com a internet para que esteja visível para o satélite que informará suas coordenadas geográficas. As aplicações da geolocalização atualmente são variadas, vão desde a utilização em sites e aplicativos para fins de marketing regional, monitoramento de cargas e veículos, até navegação.

Neste projeto, a geolocalização será utilizada com o intuito de verificar onde o usuário está para que ele tenha seu ponto de partida, além de identificar as coordenadas de seu destino e as rotas possíveis. A empresa Google, disponibiliza hoje uma API de geoloccalização de uso gratuito porém limitado, que será utilizada na construção do protótipo do sistema.

### 2.2 Ciência de dados

A ciência de dados consiste na análise e unificação para a obtenção de resultados. Inclui três fases, o design, que consiste em determinar o propósito para o qual os dados serão utilizados, a coleta, onde são adquiridos os dados necessários para a próxima fase, a análise, onde são utilizadas diversas metodologias para a obtenção do resultado. 

Para este projeto, a ciência de dados será utilizada na obtenção e análise dos dados referentes a segurança das regiões presentes na rota do usuário do aplicativo.

## 3. DESENVOLVIMENTO

O sistema será feito na forma de um aplicativo Android, que alimentado com os dados fornecidos pelo Portal de Transparência da SSP São Paulo pontuará no mapa a melhor rota para que um usuário posso chegar ao seu destino em segurança. Para o protótipo, apenas alguns destinos pré-definidos estarão disponíveis. 

### 3.1 Aplicativo

Essa aplicação é a parte principal do sistema, é nela que o usuário fará todas as suas interações. A partir da interface, o usuário poderá selecionar qual o destino que deseja, em seguida, uma conexão com o servidor backend da aplicação será estabelecida e os dados da origem e destino do usuário entrarão para o processamento dos dados.

A aplicação será nativa para Android, isso significa que ele ficará armazenado no dispositivo do usuário. A escolha da utilização de um aplicativo nativo parte diretamente da necessidade da interação com o sitema do celular para a obtenção dos dados de localização do GPS. Ele será desenvolvido com a utilização das linguagens React Native, baseada em JavaScript e utilizada para a construção da interface, e Django, um framework Python para a construção da lógica da aplicação, a escolha de um framework baseado em Python surge da facilidade encontrada para desenvolvimento de aplicações de ciência de dados com ela, com grande disponibilidade de bibliotecas para esse propósito.

## Bibliografia

[1] Veja São Paulo, 2017. **As roubadas enfrentadas por motoristas ao seguir atalhos de aparelhos de GPS por Adriana Farias**. Disponível em: <https://vejasp.abril.com.br/cidades/roubadas-motoristas-dicas-rota-gps-waze/>. Acesso em dezembro de 2020.

[2] G1, 2015. **Saiba como evitar riscos ao seguir aplicativos e equipamentos de GPS**. Disponível em: <http://g1.globo.com/jornal-nacional/noticia/2015/10/saiba-como-evitar-riscos-ao-seguir-aplicativos-e-equipamentos-de-gps.html>. Acesso em dezembro de 2020.

Chikio Hayashi, **What is Data Science? Fundamental Concepts and a Heuristic Example**. Disponível em: <https://link.springer.com/chapter/10.1007/978-4-431-65950-1_3>. Acesso em dezembro de 2020.
