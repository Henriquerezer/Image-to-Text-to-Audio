# Image-to-Text-to-Audio

Uma ferramenta com IA que transforma imagem para texto e este texto para uma descrição do ambiente e por fim transforma para áudio..

A ferramenta utiliza Hugging Face Transformers open-source framework para deep em combinação com OpenAI prompting via Langchain framework.

![](https://github.com/Henriquerezer/Image-to-Text-to-Audio/assets/87787728/7d2e3b65-b2d3-4471-adc4-2df30f8fa69d)
![](https://github.com/Henriquerezer/Image-to-Text-to-Audio/assets/87787728/d0463153-2f5d-445d-b73a-f23370fda094)

# Abordagem

A exucução é abordada em 3 partes:
- **Image to text:**
  um modelo de transformador de imagem para texto ([Salesforce/blip-image-captioning-base](https://huggingface.co/Salesforce/blip-image-captioning-base)) é usado para gerar um cenário de texto baseado na compreensão da IA do contexto da imagem
- **Text to story:**
  O modelo OpenAI LLM é solicitado a criar uma descrição do cenário
- **Story to speech:**
  um modelo de transformador de texto para fala ([espnet/kan-bayashi_ljspeech_vits](https://huggingface.co/espnet/kan-bayashi_ljspeech_vits)) é usado para converter o conto gerado em um arquivo de áudio narrado por voz
- Uma interface de usuário é construída usando streamlit para permitir o upload da imagem e a reprodução do arquivo de áudio

# requirements

- os
- dotenv
- transformers
- langchain
- requests
- streamlit
- openai

# Objetivos Futuros 
- Este trabalho serve como um projeto para entendimento inicial do uso das ferramentas.
- O objeitvo principal é utilziar as ferramentas de Image-To-Text, para a descrição do ambiente para pessoas cegas, como ferramenta de suporte.
- Servindo como descrição do Ambiente, Posição espacial, entre demais opções
