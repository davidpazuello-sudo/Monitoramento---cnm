# Perfis, Permissoes e Governanca

## 1. Objetivo

Definir uma proposta de estrutura de acesso, responsabilidades e controles para o sistema.

## 2. Perfil observado

A interface mostra o usuario "Joao Paulo" com o perfil "Admin - System". Isso indica que o sistema suporta, no minimo, diferenciacao de papeis.

## 3. Perfis recomendados

### 3.1 Administrador do sistema

Responsabilidades:

- gerenciar configuracoes gerais;
- administrar perfis e permissoes;
- parametrizar categorias, status e canais;
- acompanhar logs e integracoes;
- atuar em sustentacao e governanca.

### 3.2 Gestor

Responsabilidades:

- acompanhar operacao;
- monitorar indicadores;
- validar relatorios;
- supervisionar aprovacoes e excecoes.

### 3.3 Analista operacional

Responsabilidades:

- consultar registros;
- realizar triagem;
- atualizar status;
- registrar encaminhamentos e observacoes.

### 3.4 Atendente

Responsabilidades:

- localizar cidadaos e protocolos;
- registrar novas demandas;
- orientar o fluxo inicial.

### 3.5 Leitor ou auditor

Responsabilidades:

- acompanhar operacao;
- auditar historico e conformidade;
- gerar evidencias e relatorios.

## 4. Matriz resumida de acesso

| Modulo | Admin | Gestor | Analista | Atendente | Leitor |
|---|---|---|---|---|---|
| Inicio | Sim | Sim | Sim | Sim | Sim |
| Assistente IA | Sim | Sim | Sim | Opcional | Nao |
| Feedback | Sim | Sim | Sim | Sim | Leitura |
| Relatorios | Sim | Sim | Basico | Basico | Sim |
| Transmissao | Sim | Opcional | Opcional | Nao | Leitura |
| Cidadaos | Sim | Sim | Sim | Sim | Leitura |
| Estatisticas da Cidade | Sim | Sim | Leitura | Nao | Sim |
| Configuracoes | Sim | Nao | Nao | Nao | Nao |

## 5. Regras de governanca recomendadas

### 5.1 Segregacao de funcoes

Funcoes criticas devem ser separadas para reduzir risco operacional:

- quem cadastra nao deveria aprovar sozinho em processos sensiveis;
- alteracoes de parametros devem ficar restritas;
- exclusoes definitivas devem ser evitadas ou fortemente auditadas.

### 5.2 Trilha de auditoria

Toda acao relevante deve registrar:

- usuario;
- data e hora;
- acao executada;
- valor anterior e valor novo;
- origem da operacao.

### 5.3 Governanca de dados pessoais

Como ha nome e CPF, o sistema deve observar principios de protecao de dados:

- acesso minimo necessario;
- mascaramento em telas e relatorios, quando apropriado;
- registro de consentimento ou base legal, se aplicavel;
- retencao adequada dos dados;
- controle de exportacao.

### 5.4 Controle de IA

Se o Assistente IA manipula dados reais:

- deve haver politica de uso;
- respostas precisam ser auditaveis quando impactarem decisao;
- sugestoes da IA nao devem substituir validacao humana em decisoes criticas;
- logs de prompts e respostas devem obedecer regras internas e LGPD.

## 6. Eventos criticos que exigem controle reforcado

- aprovacao e reprovacao de casos;
- alteracao de score de elegibilidade;
- emissao de segunda via;
- alteracao cadastral de cidadao;
- mudanca de parametros do sistema;
- exportacao massiva de dados;
- acesso administrativo.

## 7. Recomendacoes de seguranca

- autenticar usuarios com politica forte de senha;
- adotar sessao com expiracao por inatividade;
- registrar tentativas invalidas de acesso;
- limitar exportacoes por perfil;
- proteger informacoes sensiveis em transito e em repouso;
- revisar periodicamente os acessos concedidos.
