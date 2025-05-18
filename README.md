# ListaAnimes
Projeto para a imersão Alura 

# Projeto de Criação de Posts de Animes para TikTok

Este projeto utiliza múltiplos agentes com o Google AI SDK para pesquisar, planejar, redigir e revisar posts para o TikTok sobre temas de anime.

## Funcionalidades

- Pesquisa de animes baseada em um tema fornecido pelo usuário.
- Geração de uma lista ranqueada dos animes encontrados.
- Criação de um rascunho de post para o TikTok com legenda e conteúdo.
- Revisão e correção do rascunho do post para garantir precisão e adequação ao público-alvo.

## Como usar

1. Certifique-se de ter o Google AI SDK instalado. Se não tiver, execute: bash %pip -q install google-genai !pip install -q google-adk
2. 2. Configure sua chave de API do Google AI. No Colab, você pode fazer isso utilizando `userdata.get('GOOGLE_API_KEY')`.
3. Execute o código na célula do Colab.
4. O programa solicitará que você digite um tema de anime.
5. O projeto executará os agentes sequencialmente e exibirá os resultados de cada etapa, culminando no post final revisado.

## Estrutura do Código

- `call_agent(agent: Agent, message_text: str) -> str`: Função auxiliar para executar um agente e retornar sua resposta.
- `to_markdown(text)`: Função para formatar texto em Markdown para exibição no Colab.
- `agente_buscador(tema_anime, data_atual)`: Agente responsável por pesquisar animes na internet.
- `agente_planejador(tema_anime, animes_encontrados)`: Agente responsável por listar e ranquear os animes encontrados.
- `agente_redator(tema_anime, lista_animes_planejada)`: Agente responsável por redigir o post para o TikTok.
- `agente_revisor(tema_anime, rascunho_post)`: Agente responsável por revisar e corrigir o rascunho do post.

## Requisitos

- google-genai
- google-adk
- IPython
