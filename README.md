# ProductSearchRelevance

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

2. query.csv - Stores search queries, columns include:
a. query_id - unique ID for each query
b. query - query string
c. query_class - category to which the query falls under

3. label.csv - Stores annotated (product,relevance judgement) pairs, columns include
a. id - Unique ID for each annotation
b. query_id - ID of the query this annotation is for
c. product_id - ID of the product this annotation applies to
d. label - Relevance label, one of 'Exact', 'Partial', or 'Irrelevant'

