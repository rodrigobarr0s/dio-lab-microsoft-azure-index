# Azure Cognitive Search: Utilizando AI Search para indexação e consulta de Dados

Este projeto demonstra como utilizar o **Azure Cognitive Search** para indexar e consultar dados, com a adição de recursos de **AI Search** para melhorar a busca e a extração de informações de fontes de dados estruturados e não estruturados.

## Objetivo

- Configurar o **Azure Cognitive Search** para indexação de dados.
- Utilizar **AI Search** para aplicar inteligência à busca de dados.
- Implementar consultas inteligentes para extrair informações relevantes a partir de dados não estruturados.
- Demonstrar o uso de **cognitive skills** para enriquecer os resultados da pesquisa.

## Etapas do Projeto

### 1. Criação do Recurso de Pesquisa Cognitiva
   - Acesse o [Portal Azure](https://portal.azure.com/).
   - Crie um novo recurso do tipo **Azure Cognitive Search**.
   - Defina a região e configure os planos de preço conforme necessário.

### 2. Configuração da Fonte de Dados
   - Selecione a fonte de dados a ser indexada (por exemplo, documentos armazenados no **Azure Blob Storage**, banco de dados **SQL**, ou outros tipos de dados).
   - Configure o **Data Source** no Azure Cognitive Search para acessar essa fonte de dados.

### 3. Criação e Configuração do Índice
   - Crie um índice para organizar os dados que serão indexados.
   - Defina os campos a serem indexados (texto, números, datas, etc.).
   - Utilize **AI Enrichment** (habilitando Cognitive Skills) para aplicar técnicas de inteligência artificial, como **OCR** (reconhecimento de texto em imagens) e **análise de sentimentos**.

### 4. Realização de Consultas
   - Após a indexação, utilize a **API de Pesquisa** do Azure para realizar consultas inteligentes.
   - Explore como as consultas podem retornar dados relevantes com base em contextos ou palavras-chave, e até mesmo fornecer resumos de textos.

### 5. Aplicação de AI Search
   - Ative o recurso **AI Search** para melhorar os resultados das buscas, com funcionalidades como sugestão de autocompletar, facetas de pesquisa, e análises de sentimentos.

## Exemplo de Código

```csharp
// Exemplo de consulta de pesquisa usando a API de Azure Cognitive Search
SearchClient searchClient = new SearchClient(new Uri("https://<nome-do-serviço>.search.windows.net"), "<índice>", new AzureKeyCredential("<chave-do-serviço>"));
SearchResults<SearchDocument> results = searchClient.Search<SearchDocument>("exemplo de consulta");
await foreach (SearchResult<SearchDocument> result in results.GetResultsAsync())
{
    Console.WriteLine($"Resultado encontrado: {result.Document}");
}
```

## Possíveis Aplicações

- Pesquisa em grandes volumes de documentos não estruturados (textos, PDFs, imagens).
- Análise de dados de feedback de clientes ou redes sociais.
- Busca inteligente em grandes bases de dados de produtos, artigos ou documentos.

## Recursos Adicionais

- [Documentação oficial - Azure Cognitive Search](https://learn.microsoft.com/azure/search/)
- [Azure AI Search Overview](https://learn.microsoft.com/azure/search/cognitive-search-introduction)
- [Azure Cognitive Search API](https://learn.microsoft.com/azure/search/search-what-is-api)

## Contribuição

Sinta-se à vontade para enviar pull requests com melhorias ou abrir issues com dúvidas ou sugestões!

Autor: Rodrigo Barros  
Última Atualização: 26 de Abril de 2025
