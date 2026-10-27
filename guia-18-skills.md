# 18 Skills de IA: como instalar, para que servem e exemplos práticos

*Descrição da página (Google e redes sociais):* Aprenda o que são skills de IA, como instalar no Claude Code, para que servem 18 skills populares e como usá-las em design, desenvolvimento, testes, conteúdo e automação.

---

## Por que skills

Você já pediu para uma IA criar um site, escrever um texto ou montar uma integração e recebeu uma resposta genérica? Isso acontece porque o agente não conhece o seu processo, as suas regras de qualidade nem as ferramentas do seu projeto.

As **skills** resolvem parte disso. Elas são pacotes reutilizáveis de instruções, referências, templates e, às vezes, scripts. Em vez de explicar o mesmo procedimento em todo prompt, você instala uma skill e o agente passa a seguir um fluxo mais organizado.

Uma skill não é um modelo de IA e não garante resultado perfeito. Ela funciona como uma camada de orientação: o agente ainda precisa interpretar as instruções, ter acesso às ferramentas certas e ter o trabalho revisado por você.

A diferença para um prompt comum é a reutilização. O prompt resolve um pedido pontual. A skill organiza um processo que você vai repetir.

Neste guia estão 18 skills que aparecem com frequência, para que cada uma serve e um exemplo de uso.

> **Antes de instalar qualquer uma:** nomes, repositórios e comandos mudam. Abra a página atual do repositório, leia o `SKILL.md` e confirme o comando oficial. Nunca execute um comando copiado de uma página, vídeo ou artigo sem conferir a origem.

## O que é uma skill

Uma skill é um conjunto organizado de conhecimento e procedimentos que o agente carrega quando uma tarefa pede aquela especialidade.

Uma skill de testes, por exemplo, pode orientar o agente a criar casos de teste, rodar a aplicação, verificar respostas e registrar falhas. Uma skill de copywriting pode ajudar a estruturar uma página de vendas com promessa, benefícios, objeções e chamada para ação.

No Claude Code, as skills são pastas com um arquivo `SKILL.md`. Podem ser usadas em um projeto, compartilhadas em um repositório ou distribuídas como plugin.

## Como instalar

**1. Prepare o ambiente.** Você precisa de Node.js com `npx`, um agente compatível (Claude Code, Cursor, Codex e outros), acesso ao terminal, o repositório correto da skill e, quando ela depender de um serviço externo, as credenciais ou chaves de API.

**2. Use o comando da página da skill.** O diretório skills.sh usa um formato parecido com este:

```bash
npx skills add <owner/repositorio> --skill <nome-da-skill>
```

Exemplo genérico:

```bash
npx skills add vercel-labs/skills --skill find-skills
```

O endereço e o nome podem mudar. Use sempre o comando copiado da página atual da skill.

**3. Leia o conteúdo antes de dar permissão.** Uma skill pode incluir scripts executáveis, chamadas de API e acesso a arquivos. Confira quem mantém o repositório, quando foi atualizado, quais arquivos serão executados, se há acesso a tokens ou variáveis de ambiente, quais serviços externos serão chamados e se o uso pode gerar cobrança.

**4. Faça um teste controlado.** Instale primeiro em um projeto de teste, com arquivos sem dados confidenciais, e peça uma tarefa pequena. Só depois use em um projeto de verdade.

## As 18 skills

### 1. `skill-creator`
**Serve para:** criar uma skill própria para um processo seu.
**Onde ajuda:** se você segue sempre o mesmo caminho para publicar artigos (pesquisa de palavras-chave, pauta, escrita, revisão de SEO, links, checklist final), ela ajuda a transformar isso em um pacote reutilizável.
**Exemplo:** uma skill `artigos-do-meu-site` com o tom de voz da marca, a estrutura dos textos, as regras de SEO e os critérios de revisão.
**Quando usar:** quando você repete uma rotina e quer o mesmo padrão em vários projetos.

### 2. `find-skills`
**Serve para:** encontrar skills que já existem para uma tarefa.
**Onde ajuda:** em vez de procurar à mão entre centenas de repositórios, você descreve o que quer fazer e descobre as opções.
**Exemplo:** "encontre uma skill para testar formulários de uma aplicação web e explique quais permissões ela exige".
**Quando usar:** no começo de um projeto, ou quando você percebe que está criando do zero algo que já existe.

### 3. `frontend-design`
**Serve para:** orientar a criação de interfaces mais consistentes e menos genéricas.
**Onde ajuda:** hierarquia visual, composição, tipografia, espaçamento, estados dos componentes e identidade visual.
**Exemplo:** uma tela de painel para um SaaS, com menu lateral, cartões de métricas, tabela responsiva e estados de carregamento, erro e vazio.
**Atenção:** ela não substitui um designer. Compare o resultado com o objetivo do produto e teste com pessoas de verdade.

### 4. `shadcn` (shadcn/ui)
**Serve para:** trabalhar com componentes de interface reutilizáveis e personalizáveis.
**Onde ajuda:** botões, modais, abas, tabelas, calendários, menus e formulários dentro de um mesmo sistema visual.
**Exemplo:** um formulário de cadastro com validação, mensagens de erro, botão de envio e estado de carregamento.
O shadcn/ui entrega o código dos componentes dentro do seu projeto, para você poder alterá-los direto. Isso é diferente de instalar uma biblioteca fechada e sobrescrever os estilos.

### 5. `web-design-guidelines`
**Serve para:** revisar uma interface ou um código em busca de problemas de design e usabilidade.
**Onde ajuda:** contraste, tamanho de texto, espaçamento, responsividade, estados de interação e problemas comuns de experiência.
**Exemplo:** depois que o agente criar uma landing page, pedir "verifique acessibilidade, comportamento em telas pequenas e clareza das chamadas para ação".
**Quando usar:** depois da primeira versão e antes de mostrar para usuários ou clientes.

### 6. `ai-image-generation`
**Serve para:** orientar a geração de imagens com modelos de IA e ferramentas compatíveis.
**Onde ajuda:** thumbnails, imagens para artigos, conceitos visuais, ilustrações, imagens de produto e variações de campanha.
**Exemplo:** cinco conceitos de thumbnail para um artigo sobre automação, na mesma paleta e com espaço livre para o título.
**Atenção:** ela pode depender de um CLI, de login e de provedores externos. Confira custo, licença comercial e política de uso das imagens.

### 7. `nano-banana-2`
**Serve para:** um fluxo específico de geração e edição de imagens, ligado ao modelo indicado na página da skill.
**Onde ajuda:** criar variações visuais em um processo automatizado, adaptar a mesma imagem para formatos diferentes ou produzir uma sequência de peças com instruções padronizadas.
**Exemplo:** transformar uma imagem de produto em versões para banner, post quadrado e story, preservando o produto e mudando só a composição e a proporção.
**Atenção:** confira o nome atual do modelo, o provedor e a forma de autenticação. Ferramentas de imagem mudam rápido.

### 8. `ai-video-generation`
**Serve para:** organizar fluxos de geração de vídeo com IA.
**Onde ajuda:** vídeos curtos para redes sociais, cenas de demonstração, storyboards e variações de anúncio.
**Exemplo:** três versões de 10 segundos para divulgar um aplicativo: uma mostrando o problema, outra a solução e outra o benefício principal.
**Atenção:** gerar vídeo costuma envolver processamento externo, fila, limites, cobrança e políticas de conteúdo. Instalar a skill não libera todos os modelos automaticamente.

### 9. `brainstorming`
**Serve para:** transformar uma ideia solta em um escopo claro, por meio de perguntas e etapas de descoberta.
**Onde ajuda:** definição de produto, planejamento de funcionalidades, riscos e documento de requisitos.
**Exemplo:** começar com "quero criar uma plataforma de agendamento" e chegar a público, problema, fluxo principal, funcionalidades do MVP e critérios de sucesso.
**Quando usar:** antes de pedir código. Uma ideia bem definida reduz retrabalho e respostas genéricas.

### 10. `mcp-builder`
**Serve para:** criar servidores e integrações baseados no Model Context Protocol (MCP).
**Onde ajuda:** conectar um agente a um banco de dados, sistema interno, calendário, ferramenta de atendimento, CRM ou serviço externo.
**Exemplo:** uma integração para o agente consultar pedidos em um sistema interno e responder o status correto, respeitando permissões.
O MCP é uma camada de conexão entre aplicações de IA e sistemas externos. Ele não é uma skill, um modelo nem um banco de dados. A skill ajuda a construir o MCP, mas autenticação, autorização e dados sensíveis continuam sendo sua responsabilidade.

### 11. `webapp-testing`
**Serve para:** orientar testes automatizados e verificações em aplicações web.
**Onde ajuda:** login, cadastro, checkout, navegação, filtros, formulários e fluxos críticos.
**Exemplo:** em uma loja virtual, testar se o cliente escolhe um produto, adiciona ao carrinho, preenche os dados e conclui sem erro.
**Quando usar:** durante o desenvolvimento, antes de apresentar o MVP e a cada mudança relevante.

### 12. `supabase` (ou `supabase-postgres`)
**Serve para:** apoiar decisões e implementações com PostgreSQL no Supabase.
**Onde ajuda:** modelagem de tabelas, relacionamentos, políticas de acesso, consultas, índices e organização do backend.
**Exemplo:** criar as tabelas de usuários, projetos e tarefas, definir quem pode ler ou editar cada registro e preparar as consultas do painel.
**Atenção:** nunca aceite automaticamente uma política de acesso gerada por IA. Revise RLS, permissões, exposição de dados e chaves de serviço.

### 13. `stripe` (ou `stripe-best-practices`)
**Serve para:** orientar integrações de pagamento, assinatura e cobrança com Stripe.
**Onde ajuda:** checkout, planos recorrentes, portal do cliente, webhooks e atualização do status da assinatura.
**Exemplo:** um plano gratuito e dois pagos, com funcionalidades liberadas de acordo com a assinatura e acesso bloqueado quando o pagamento falha.
**Atenção:** pagamento é área sensível. Teste em modo de teste, valide os webhooks e nunca exponha chaves secretas no frontend.

### 14. `pdf`
**Serve para:** ler, extrair, criar ou editar documentos PDF.
**Onde ajuda:** e-books, relatórios, propostas comerciais, extração de dados e materiais para clientes.
**Exemplo:** transformar um relatório de análise em um PDF com capa, sumário, seções e referências.
**Atenção:** confira se a skill só orienta o agente ou se também traz scripts para converter e manipular arquivos.

### 15. `pptx`
**Serve para:** criar e organizar apresentações em PowerPoint.
**Onde ajuda:** pitch de startup, apresentação comercial, treinamento interno e demonstração de produto.
**Exemplo:** converter a pesquisa de um produto em uma apresentação com problema, público, solução, protótipo, modelo de negócio e próximos passos.
**Atenção:** revise gráficos, números, fontes e layout. Uma apresentação gerada automaticamente ainda precisa de direção editorial.

### 16. `docx`
**Serve para:** criar e estruturar documentos editáveis do Word.
**Onde ajuda:** propostas, manuais, briefings, relatórios e documentos de requisitos.
**Exemplo:** um documento de escopo com objetivo, funcionalidades, regras de negócio, critérios de aceite e cronograma.
**Atenção:** para contratos e materiais jurídicos ou regulatórios, a IA ajuda na estrutura, mas não substitui revisão profissional.

### 17. `Copywriting`
**Serve para:** criar textos persuasivos e orientados à conversão.
**Onde ajuda:** landing pages, anúncios, e-mails, páginas de produto e chamadas para ação.
**Exemplo:** três versões da seção principal de um serviço de automação, cada uma para um público: empreendedor, agência e equipe de tecnologia.
**Quando usar:** depois de definir público, problema, benefício e prova. Sem isso, a skill tende a escrever textos genéricos.

### 18. `Content Strategy`
**Serve para:** organizar temas, formatos, canais e etapas de uma estratégia de conteúdo.
**Onde ajuda:** calendário editorial, funil de conteúdo, agrupamentos de SEO, distribuição e reaproveitamento.
**Exemplo:** transformar um artigo principal sobre skills em uma sequência de vídeos curtos, posts, newsletter, checklist e estudo de caso.
**Quando usar:** antes de produzir em volume, para ligar cada conteúdo a uma etapa da jornada do público.

## Do protótipo ao produto funcionando

As skills rendem mais quando fazem parte de um processo completo, e não quando são instaladas ao acaso.

**1. Da ideia ao escopo.** Use `brainstorming` para esclarecer o problema, o público, as funcionalidades essenciais e os critérios de sucesso. O resultado deve ser um escopo pequeno o bastante para virar um MVP.

**2. Protótipo no Figma.** Antes de programar, faça um protótipo navegável. Ele valida aparência e experiência sem gastar tempo com funcionalidades que podem ser descartadas. Use `frontend-design`, `shadcn` e `web-design-guidelines` como apoio. O protótipo precisa responder: o usuário entende o que fazer na primeira tela? O caminho principal está claro? Os estados de erro e carregamento foram pensados? A interface funciona em telas de tamanhos diferentes?

**3. Construa o MVP.** Com o protótipo validado, use `supabase` para estruturar os dados, `stripe` se houver pagamento e `mcp-builder` se o produto precisar conversar com outros sistemas. O MVP não deve ter tudo: só o suficiente para testar a hipótese principal com usuários reais.

**4. Teste em staging.** Use `webapp-testing` nos fluxos principais, em um ambiente separado da produção, e registre os problemas. Uma sequência segura: testes internos, alpha com um grupo controlado, beta com um grupo maior, coleta organizada de feedback, correção e nova rodada.

**5. Materiais e divulgação.** Use `pdf`, `pptx`, `docx`, `Copywriting` e `Content Strategy` para transformar o projeto em apresentação comercial, manual de uso, estudo de caso, landing page, posts e roteiro de demonstração.

## Cinco regras para usar skills com segurança

1. **Não instale por popularidade.** Instalações e estrelas indicam atividade, não segurança nem qualidade. Leia o código e veja se há manutenção.
2. **Não exponha dados sensíveis.** Teste com dados fictícios. Nunca cole chaves secretas, documentos privados ou dados de clientes sem entender como a ferramenta trata essas informações.
3. **Não confunda orientação com execução.** A skill diz ao agente como fazer, mas a ferramenta ainda pode não estar instalada nem configurada.
4. **Não publique sem revisão.** Revise código, textos, imagens, pagamentos, permissões, acessibilidade e afirmações factuais antes de colocar qualquer coisa no ar.
5. **Meça o resultado.** Compare o processo com e sem a skill: tempo economizado, quantidade de erros, qualidade da entrega e retrabalho. A melhor skill é a que melhora o seu processo, não a que aparece em um ranking.

## Por onde começar

O benefício não está em instalar 18 skills de uma vez. Está em escolher as que resolvem um problema real do seu fluxo.

Comece por uma tarefa que você repete. Escolha uma skill, faça um teste pequeno, compare o resultado e, se funcionou, transforme em um processo documentado. A IA acelera o trabalho, mas a qualidade continua dependendo de boas decisões, critérios claros e revisão humana.

**Qual tarefa você mais repete hoje? Comece por ela.**

## Fontes para conferir

- Claude Code, "Extend Claude with skills": https://code.claude.com/docs/en/skills
- Repositório de Agent Skills da Anthropic: https://github.com/anthropics/skills
- Diretório skills.sh: https://skills.sh/
- Model Context Protocol: https://modelcontextprotocol.io
- shadcn/ui: https://ui.shadcn.com/docs
