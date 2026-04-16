# Requisitos Funcionais

## 1. Objetivo

Este documento detalha os requisitos funcionais identificados ou inferidos a partir da interface do sistema.

## 2. Requisitos gerais da plataforma

### RF-001. Autenticacao de usuario

O sistema deve permitir acesso autenticado por usuario individual.

### RF-002. Exibicao de usuario e perfil

O sistema deve exibir o nome do usuario logado e seu perfil no cabecalho.

### RF-003. Navegacao entre modulos

O sistema deve disponibilizar menu lateral para acesso aos modulos principais.

### RF-004. Internacionalizacao

O sistema deve permitir selecao ou visualizacao do idioma da interface.

## 3. Requisitos da tela inicial

### RF-005. Exibicao de painel inicial

O sistema deve apresentar uma tela inicial com listagem dos registros em formato tabular.

### RF-006. Pesquisa textual

O sistema deve permitir pesquisar registros por texto livre.

### RF-007. Filtros complementares

O sistema deve permitir filtrar os registros por criterios adicionais.

### RF-008. Filtro por data

O sistema deve permitir filtrar registros por data.

### RF-009. Exibicao de registros inativos

O sistema deve permitir visualizar ou ocultar registros inativos.

### RF-010. Ordenacao da grade

O sistema deve permitir ordenacao por colunas, ao menos na data de criacao.

### RF-011. Paginacao

O sistema deve paginar os resultados da grade.

## 4. Requisitos da grade de registros

### RF-012. Exibicao do status

O sistema deve exibir o status do registro com apoio visual por icone e cor.

### RF-013. Exibicao do protocolo

O sistema deve exibir numero unico de protocolo para cada registro.

### RF-014. Exibicao da data e hora de criacao

O sistema deve exibir a data e a hora de criacao do registro.

### RF-015. Exibicao do canal de origem

O sistema deve exibir o canal pelo qual o registro foi originado ou classificado.

### RF-016. Exibicao de identificacao do cidadao

O sistema deve exibir nome e CPF do cidadao vinculado ao registro.

### RF-017. Exibicao da mensagem e CID

O sistema deve exibir o conteudo principal da solicitacao e o CID ou codigo complementar quando aplicavel.

### RF-018. Exibicao de percentual de elegibilidade

O sistema deve exibir percentual numerico e indicador visual de elegibilidade.

### RF-019. Acesso ao detalhe do registro

Ao selecionar uma linha, o sistema deve permitir abrir a visao detalhada do registro.

### RF-020. Atualizacao de status

O sistema deve permitir alterar ou registrar a evolucao do status conforme permissao do usuario.

### RF-021. Historico do registro

O sistema deve manter historico de alteracoes e decisoes relacionadas ao protocolo.

## 5. Requisitos por modulo

### RF-022. Assistente IA

O sistema deve disponibilizar um modulo de assistente IA para apoio ao usuario administrativo.

### RF-023. Pesquisas

O sistema deve permitir registrar e consultar pesquisas de satisfacao ou opiniao.

### RF-024. Reclamacoes

O sistema deve permitir registrar, consultar e acompanhar reclamacoes.

### RF-025. Sugestoes

O sistema deve permitir registrar, consultar e acompanhar sugestoes.

### RF-026. Relatorios

O sistema deve gerar relatorios por periodo, status, canal, usuario ou elegibilidade.

### RF-027. Exportacao de dados

O sistema deve permitir exportacao dos relatorios em formatos padrao.

### RF-028. Transmissao

O sistema deve permitir acompanhar eventos de transmissao, envio ou sincronizacao de dados.

### RF-029. Cadastro de cidadaos

O sistema deve permitir cadastrar e manter dados basicos dos cidadaos.

### RF-030. Historico do cidadao

O sistema deve permitir visualizar todos os protocolos e interacoes vinculados a um cidadao.

### RF-031. Estatisticas

O sistema deve consolidar indicadores em dashboards e estatisticas agregadas.

### RF-032. Configuracoes

O sistema deve permitir gerenciar perfis, canais, status e categorias do sistema.

## 6. Requisitos de auditoria

### RF-033. Registro de logs

O sistema deve registrar logs de acesso, alteracoes e acoes criticas.

### RF-034. Rastreabilidade por usuario

O sistema deve vincular alteracoes relevantes ao usuario responsavel.

### RF-035. Trilhas de aprovacao

O sistema deve registrar decisoes de aprovacao, reprovacao, recadastro ou segunda via.

## 7. Pontos que precisam de confirmacao

- significado exato do campo "CID";
- formula da "Elegibilidade";
- relacao entre "Canal" e "Status";
- logica de "Segunda Via";
- papel real do modulo "Transmissao";
- escopo do Assistente IA.
