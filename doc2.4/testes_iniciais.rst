===============
Testes iniciais
===============

Os testes realizados estão disponibilizados no `github <https://github.com/Projeto-Game-Antartica/Testes>`_ da organização do projeto no repositório de Testes.

REMAR
=====

Disponível em : https://github.com/Projeto-Game-Antartica/Testes/tree/master/Antartica_Remar 

Learning Analytics
==================


GBLxAPI
^^^^^^^^

Está de acordo com o K-12,  é uma designação para a educação primária até a educação secundária, padrão usado nos EUA e Canadá.
Está em beta. Utiliza interface para realizar a comunicação entre LRS e os Jogos feitos em Unity.

Exemplo de dashboard: 
https://gblxapi.org/images/analytics/GBLxAPI_Demo2-8-17-2018.png



Plataforma RAGE: https://github.com/e-ucm/rage-analytics
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

**R** ealising an **A** pplied **G** aming **E** cosystem é ecossistema dividido em três camadas, conforme :numref:`figRAGEarch`.

.. _figRAGEarch:
.. figure:: https://user-images.githubusercontent.com/5657407/28160045-4a483136-67bf-11e7-941e-2db0cd786869.png
   :align: center
   
   : Visão da arquitetura RAGE em três camadas (Cliente, Autenticação/Autorização e Aplicações).


**Cliente**

Acesso ao jogador e rastreia os jogos. Front-end do analytics permite acesso aos desenvolvedores, 
professores e estudantes. A2 front-end permite o administrador gerencia as contas dos usuários.

**A2**

Módulo A2 controla autenticações e autorizações de usuários e tráfego das informações. Pelo A2 é possível gerenciar 
usuários, papéis, recursos, permissões e aplicações.

**Aplicações**

Experience API (xAPI) é usado como padrão para o rastreio de dados do usuário. O analytics back-end armazena 
as informações obtidas através da A2. Kafka mantém filas de rastreios a serem processadas. Topologia Storm 
gerencia a análise de processos. Os resultados são armazenados no ElasticSearch. Kibana gerencia as visualizações 
dos resultados via ElasticSearch.


Acessibilidade
==============

Para o teste relacionado à acessibilidade, foram criado dois projetos distintos, um para `teste de sons e vídeo <https://github.com/Projeto-Game-Antartica/Testes/tree/master/snow_tile>`_ e outro para a `leitura de tela, navegação, mini-jogos e também o glossário. <https://github.com/Projeto-Game-Antartica/Testes/tree/master/translation-project>`_

Sons e Vídeo
=============

Os testes relacionados à sons e vídeos foram utilizados para testar as ferramentas do Unity com objetivo de verificar se seriam suficientes para contemplar os requisitos de acessibilidade. A parte de vídeo não foi testada com nenhum usuário, porém as funcionalidades da engine permitem que sejam feitas a execução de vídeo normalmente. Ainda existe a dúvida de como a execução será feita, se através de streaming ou não, visto que isso pode impactar no tamanho do jogo final (os vídeos podem ou não estar dentro da pasta do jogo, aumentando o seu tamanho).

O teste de som foi realizado com dois deficientes visuais participantes do projeto, onde foram apresentados um cenário 2D isométrico (:numref:`IsometricScene`) com diferentes tipos de chão (gelo, neve, etc) e diferentes animais espalhados pelo mapa. O objetivo era de saber se era possível localizar os animais e supor a distância que os mesmos estavam do personagem. Cada tipo de chão possuía um som característico, bem como os animais. Além disso, havia som de colisão com as paredes (cenário fechado).

O feedback dos testes foi positivo, porém com sugestões de melhorias e, dentre elas, pode-se destacar: transição mais suave dos sons (para ajudar na localização/distância dos animais, no caso), sons estáveis para objetos (por exemplo, caso haja uma parede ao norte do usuário, emitir um som estático característico representando essa situação).

.. _figIsometricScene:
.. figure:: cenario_isometrico_2d.png
   :align: center
   
   : Cenário 2D isométrico utilizado para teste.

Leitura de tela
===============

A leitura de tela foi apresentado através de um teste em formato de um quiz (minijogo). Assim, foi desenvolvido uma mecânica simples de transição de telas (menu, jogo, créditos) para também testar a usabilidade e navegação do jogo. 

Todo o conteúdo foi adaptado para que pudesse ser lido e relido pelo leitor de tela nativo do computador (sAPI, NVDA, por exemplo). Além do conteúdo exposto na tela, foram adicionados textos de instruções "invisíveis" ao usuário, i.e., textos que eram lidos a cada transição de tela para explicar detalhes de navegação (teclas de atalho) mas que não eram exibidos.

O teste foi realizado com um deficiente visual participante do projeto que nos deu um feedback positivo, além de mais sugestões para melhoria da navegabilidade, como por exemplo adicionar sons para representar o início/final das alternativas (quiz) e teclas de atalho para repetirem o último texto lido.

Além disso, foi testado também a tradução do jogo, ou seja, o jogo foi apresentado em dois idiomas com opção de escolha na primeira tela.

As telas podem ser vistas na :numref:`_figTraducao` e :numref:`_figQuiz`.

.. _figTraducao:
.. figure:: traducao.png
   :align: center
   
   : Tela inicial com seleção de idioma.

.. _figQuiz:
.. figure:: quiz.png
   :align: center
   
   : Quiz.
Glossário
==========

O conteúdo do glossário para realização do teste pode ser encontrado `aqui <https://docs.google.com/spreadsheets/d/1mvGuemPk3e-Gm60rgdjMvQxMZGOjmYUOElkMYs2TA3c/>`_ .
