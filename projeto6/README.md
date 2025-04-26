# Análise de Sentimentos com Language Studio no Azure AI

Este projeto demonstra como utilizar o **Language Studio**, da plataforma **Azure AI**, para realizar **análise de sentimentos** em textos. A Análise de Sentimentos é uma técnica de *Processamento de Linguagem Natural (NLP)* que classifica a opinião expressa em um texto como positiva, negativa, neutra ou mista.

## Objetivo

- Criar um recurso de linguagem no Azure.
- Analisar sentimentos de frases ou textos.
- Interpretar os resultados retornados (pontuações por sentimento).
- Aplicar esse recurso em cenários como atendimento ao cliente, feedbacks e redes sociais.

## Etapas do Projeto

### 1. Criação do Recurso de Linguagem:
   - Acesse o [Portal Azure](https://portal.azure.com/).
   - Crie um novo recurso do tipo "Serviço de Linguagem".
   - Anote a chave e o endpoint do recurso.

### 2. Acesso ao Language Studio:
   - Acesse [https://language.cognitive.azure.com](https://language.cognitive.azure.com).
   - Faça login com sua conta Microsoft.

### 3. Seleção da Análise de Sentimentos:
   - Escolha a opção "Análise de Sentimentos".
   - Insira o texto que deseja analisar.

### 4. Execução da Análise e Interpretação dos Resultados:
   - O Language Studio retornará as pontuações para cada sentimento.
   - Veja os sentimentos detectados por frase e a classificação geral do texto.

## Exemplo de Resultado

```json
{
  "sentiment": "positive",
  "confidenceScores": {
    "positive": 0.95,
    "neutral": 0.04,
    "negative": 0.01
  }
}
```

## Possíveis Aplicações

- Monitoramento de redes sociais.
- Classificação automática de feedbacks.
- Análise de e-mails ou atendimentos.

## Recursos Adicionais

- [Documentação oficial - Análise de Sentimentos](https://learn.microsoft.com/azure/cognitive-services/language-service/sentiment-opinion-mining/overview)
- [Azure AI Language Studio](https://language.cognitive.azure.com/)

## Contribuição

Sinta-se à vontade para enviar pull requests com melhorias ou abrir issues com dúvidas ou sugestões!

Autor: Rodrigo Barros  
Última Atualização: 26 de Abril de 2025
