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

Sons
=====

Video
=====

Leitura de tela
===============

Glossário
==========

O conteúdo do glossário para realização do teste pode ser encontrado `aqui. <https://docs.google.com/spreadsheets/d/1mvGuemPk3e-Gm60rgdjMvQxMZGOjmYUOElkMYs2TA3c/>`_
