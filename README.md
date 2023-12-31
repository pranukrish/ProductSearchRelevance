# Product Search Relevance

The objective of this project is to demonstrate the application of large language models (LLMs) to enhance and expedite product search processes. Unlike traditional product search methods that rely on keyword matches, LLMs facilitate semantic search, leveraging conceptual similarities between words.

The conceptual understanding of word relationships in LLMs is acquired through exposure to diverse documents, allowing the model to recognize associations between terms. For instance, a document discussing the significance of play for "children" might use the term "child," establishing a relationship between the two. Through exposure to various documents, the model learns to identify close associations between related terms, even if they are not explicitly mentioned together.

Many LLMs are available as pre-trained models, having already learned these word associations from a broad range of publicly available information. Leveraging this knowledge, these models can be employed to search the descriptive text of product catalogs for items aligned with a user-supplied search term or phrase. To further enhance performance, the models can undergo a fine-tuning process with additional data specific to a particular site, adapting to the unique language and style used by the retailer or product suppliers.

This solution accelerator will showcase two approaches: one utilizing an off-the-shelf model and another fine-tuned to a specific product catalog. Additionally, the project will address deployment challenges, demonstrating how users can seamlessly deploy a semantic search capability through their Databricks environment.

## About Dataset - WANDS: 
WANDS is a Wayfair product search relevance dataset.
The dataset allows objective benchmarking and evaluation of search engines on an E-Commerce dataset. Key features of this dataset includes:

1. 42,994 candidate products
2. 480 queries
3. 233,448 (query,product) relevance judgements

The data is stored in the dataset folder in three files:

1. product.csv - Stores all candidate products, columns include:
a. product_id - ID of a product
b. product_name - String of product name
c. product_class - Category which product falls under
d. category_hierarchy - Parent categories of product, delimited by /
e. product_description - String description of product
f. product_features - | delimited string of attribute:value pairs which describe the product
g. rating_count - Number of user ratings for product
h. average_rating - Average rating the product received
i. review_count - Number of user reviews for product

3. query.csv - Stores search queries, columns include:
a. query_id - unique ID for each query
b. query - query string
c. query_class - category to which the query falls under

4. label.csv - Stores annotated (product,relevance judgement) pairs, columns include
a. id - Unique ID for each annotation
b. query_id - ID of the query this annotation is for
c. product_id - ID of the product this annotation applies to
d. label - Relevance label, one of 'Exact', 'Partial', or 'Irrelevant'




Source of Dataset: https://github.com/wayfair/WANDS

## Architectural Diagram

![image](https://github.com/pranukrish/ProductSearchRelevance/assets/112594201/2bb9b004-ba47-4210-9459-7eba4dce279e)

## Tech Stack

Tech Stack | Description  
--- | --- 
WANDS | Wayfair product search relevance data  
Langchain | Building applications with LLMs through composability
Chromadb | An open source embedding database
Sentence-transformers | Compute dense vector representations for sentences, paragraphs, and images



## Output Snapshot:



<img width="1439" alt="Screenshot 2023-12-15 at 7 34 52 PM" src="https://github.com/pranukrish/ProductSearchRelevance/assets/112594201/a6abe56b-f340-4a8c-93c4-9191862c68c6">



When users searched for "children table," the results not only included various children's tables but also displayed "kids desks." This result is a testament to the effectiveness of our semantic search optimization, ensuring a more intuitive and user-friendly search experience. It allows for a broader range of relevant product displays, increasing the likelihood of customer satisfaction and potential sales.


Presentation Link: https://docs.google.com/presentation/d/1rxpbfkc7ot-U2ojQpzmwWKIdxv728H5fSD8zsphRhZU/edit#slide=id.SLIDES_API1437014956_2857

Demo Link: https://drive.google.com/drive/folders/1SoElWZeKC22E-bab393sAs82VlnHvDlP?usp=sharing
