# SGSAC v2.0 - Sistema de Gerenciamento de Atendimento ao Consumidor

O **SGSAC** é um sistema comercial de automação e gerenciamento operacional que idealizei e desenvolvi para otimizar o fluxo de trabalho de uma grande rede de varejo farmacêutico nacional. 

O foco principal do projeto foi eliminar o desperdício de tempo dos operadores, centralizar consultas e automatizar processos repetitivos.

⚠️ **Nota de Portfólio**: Por se tratar de um projeto corporativo legado, os arquivos de código-fonte (.pas) e executáveis (.exe) não estão disponíveis neste repositório. O projeto está registrado aqui através do seu **Manual Geral do Usuário** (gerado a partir de capturas de tela puras para preservação de marcas e dados sensíveis) para fins de demonstração de arquitetura de software, engenharia de requisitos e regras de negócio.

---

## 🛠️ Tecnologias Utilizadas
* **IDE / Linguagem:** Lazarus (Free Pascal)
* **Banco de Dados:** MS Access (.accdb / .mdb)
* **Automação de Interface:** VBScript (Visual Basic Script)
* **Arquitetura:** Aplicação local desktop (focada em portabilidade, rodando direto de arquivos locais).

---

## 🖥️ Módulos e Explicação das Telas

### 1. Tela de Login e Segurança
* **O que faz:** Controla o acesso ao sistema através de credenciais (matrícula e senha). Possui níveis de permissão diferentes: o **Operador** tem acesso apenas às ferramentas de atendimento, enquanto o **Administrador (ADM)** tem acesso irrestrito, como a tela de cadastro de novos usuários.

### 2. Tela Principal e Painel de Links Úteis
* **O que faz:** Centraliza toda a navegação do sistema através de um menu lateral. No canto inferior direito, possui um painel retrátil acionado por um clique que lista os sistemas externos mais utilizados no dia a dia da operação (como *Vtex, Tactium, G4 flex, Portal RH e HUB Saúde*). Isso evita o excesso de janelas abertas e economiza o tempo do operador.

### 3. Tela de Consulta Inteligente de Filiais
* **O que faz:** Um motor de busca avançado onde o operador digita o número da loja ou filtra por múltiplos critérios (Estado, Cidade, Bairro ou Endereço parcial). Ao encontrar a filial, o sistema exibe de forma organizada em abas:
  * Dados cadastrais (CNPJ, Horários de funcionamento).
  * Fluxos internos específicos e televendas.
  * Contatos telefônicos e e-mails.
  * Grade de serviços disponíveis e testes de saúde realizados na loja.

### 4. Ferramenta SuperClipBoard 1.0 (Automação com VBScript)
* **O que faz:** A funcionalidade de maior impacto de produtividade do sistema. Ela resolve o problema do operador ter que ficar alternando janelas para cadastrar clientes. 
* **A Automação:** A ferramenta fica travada na frente da tela. O operador, precisava alternar entre as janelas, copiando e colando. Com essa ferramenta o operador copia o dado do cliente em um sistema externo (Ctrl+C) e o armazena no SGSAC atravez de clique. Ao acionar a injeção, o sistema gera e executa uma rotina em **VBScript** em segundo plano. O script simula comandos de teclado e digita todas as informações automaticamente dentro do software de CRM (Tactium) em apenas 2 segundos, eliminando o trabalho manual e erros de digitação. Também conta com gerador automatizado de respostas padrão para tratativas (como estornos e atrasos).

### 5. Tela de Solicitação de Troca de Dados
* **O que faz:** Permite que o operador selecione uma filial e envie uma solicitação formal para alterar informações defasadas (como telefones) no banco de dados. O pedido fica registrado com o status "Pendente" até que o administrador aprove a alteração.

### 6. Tela de Consulta à Farmácia Popular
* **O que faz:** Módulo de busca rápida contendo a listagem de medicamentos do programa do governo. Exibe códigos de referência, preços e indicativos de gratuidade em tempo real para agilizar o suporte ao cliente.

---

## 📁 Documentação
O manual completo, ilustrado com o passo a passo de todas as telas originais e fluxos criados no Lazarus, está disponível na pasta '/documentacao' deste repositório.
