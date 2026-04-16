# Especificacao de Telas e Fluxos

## 1. Objetivo

Este documento descreve a interface principal observada e os fluxos funcionais provaveis do sistema.

## 2. Tela: Inicio

### 2.1 Finalidade

Servir como area central de monitoramento operacional, reunindo os registros mais relevantes para consulta, filtro, triagem e acompanhamento.

### 2.2 Componentes visuais

#### Cabecalho

Elementos identificados:

- titulo "Inicio";
- seletor de idioma;
- avatar do usuario;
- nome do usuario;
- perfil do usuario.

#### Menu lateral

Entradas identificadas:

- Inicio
- Assistente IA
- Feedback
- Pesquisas
- Reclamacoes
- Sugestoes
- Relatorios
- Transmissao
- Cidadaos
- Estatisticas da Cidade
- Configuracoes
- Help

#### Area de filtros

Elementos identificados:

- campo "Pesquisar";
- botao "Filtrar";
- opcao "Mostrar inativos";
- campo "Insira uma data".

#### Grade de listagem

Colunas identificadas:

- Status
- Protocolo
- Criado
- Canal
- Nome/CPF
- Mensagem/CID
- Elegibilidade

#### Rodape da listagem

Elementos identificados:

- indicacao de faixa de itens exibidos;
- controles numericos de paginas;
- acao "Proximo".

## 3. Descricao detalhada dos campos da grade

### 3.1 Status

Representa a situacao atual do registro. O uso de icones e cores sugere uma camada visual de prioridade ou resultado.

Interpretacoes provaveis:

- sino: alerta, pendencia ou acompanhamento;
- circulo verde: aprovado ou concluido com sucesso;
- circulo vermelho: reprovado, erro ou indeferido.

### 3.2 Protocolo

Identificador unico do registro. Deve permitir rastreabilidade ponta a ponta.

### 3.3 Criado

Data e hora de criacao do registro. A presenca de setas no titulo sugere ordenacao crescente e decrescente.

### 3.4 Canal

Origem, categoria operacional ou classificacao de entrada do registro.

Exemplos visiveis:

- Cadastro
- Aprovados
- Reprovados
- Segunda Via
- Recadastro

Subtexto observado:

- "Remedio em Casa"

Isso sugere que o canal pode possuir categoria principal e subcategoria ou programa vinculado.

### 3.5 Nome/CPF

Identificacao do cidadao vinculado ao atendimento.

### 3.6 Mensagem/CID

Descricao principal do item tratado, acompanhada de codigo auxiliar. No exemplo exibido:

- "Abatacepte 125 mg injetavel (seringa preenchida)"
- "M05.3"

Isso pode representar medicamento solicitado, procedimento, item regulado ou classificacao clinica.

### 3.7 Elegibilidade

Indicador percentual com barra visual. Sugere um score de aderencia, prioridade, conformidade ou elegibilidade do caso.

Valores observados:

- 91%
- 84%
- 72%
- 5%

## 4. Fluxos operacionais provaveis

### 4.1 Fluxo de consulta rapida

1. O usuario acessa a tela Inicio.
2. Digita um termo no campo de pesquisa.
3. Ajusta filtros adicionais, se necessario.
4. Seleciona uma data ou periodo.
5. Visualiza os registros retornados na grade.
6. Abre o registro desejado para aprofundamento.

### 4.2 Fluxo de triagem operacional

1. O sistema apresenta novos registros.
2. O operador avalia protocolo, cidadao, mensagem e score de elegibilidade.
3. O operador decide a tratativa ou encaminhamento.
4. O registro recebe um status adequado.
5. O historico e mantido para auditoria.

### 4.3 Fluxo de aprovacao ou reprovacao

1. Um registro e analisado.
2. O sistema ou o operador calcula ou informa a elegibilidade.
3. Se os criterios forem atendidos, o caso pode ser aprovado.
4. Se os criterios nao forem atendidos, o caso pode ser reprovado.
5. Em situacoes especificas, o caso pode seguir para recadastro ou emissao de segunda via.

### 4.4 Fluxo de tratamento de inativos

1. O usuario ativa a opcao "Mostrar inativos".
2. O sistema inclui na listagem registros fora do conjunto ativo.
3. O usuario pode consultar historico, auditar ou reativar conforme permissao.

### 4.5 Fluxo de navegacao gerencial

1. O gestor acessa a listagem inicial.
2. Avalia o volume, status e sinais visuais.
3. Navega para Relatorios ou Estatisticas da Cidade.
4. Consolida dados para decisao, apresentacao ou acompanhamento de desempenho.

## 5. Fluxos por modulo

### 5.1 Assistente IA

1. Usuario acessa o modulo.
2. Informa duvida, comando ou contexto do protocolo.
3. A IA retorna sugestoes, resumo, classificacao ou orientacao operacional.
4. O usuario valida a resposta e executa a acao cabivel.

### 5.2 Feedback

1. Usuario escolhe o subtipo da manifestacao.
2. Registra ou consulta itens.
3. Classifica e acompanha.
4. Gera historico e relatorios.

### 5.3 Relatorios

1. Usuario seleciona filtros.
2. Sistema consolida os registros.
3. Usuario visualiza, exporta ou compartilha o relatorio.

### 5.4 Cidadaos

1. Usuario localiza o cidadao.
2. Acessa dados cadastrais.
3. Consulta historico de protocolos e interacoes.
4. Atualiza informacoes, quando permitido.

## 6. Regras visuais e de usabilidade observadas

- O sistema utiliza hierarquia visual clara em azul e branco.
- A barra lateral organiza os modulos por natureza funcional.
- A grade prioriza leitura rapida de casos.
- O percentual de elegibilidade foi destacado para tomada de decisao.
- A interface e desenhada para uso administrativo em desktop.

## 7. Melhorias recomendadas

- permitir filtro por intervalo de datas;
- incluir legenda para os icones de status;
- exibir tooltip com descricao do score de elegibilidade;
- adicionar exportacao direta da grade;
- permitir salvar filtros favoritos;
- disponibilizar visao detalhada por clique na linha inteira.
