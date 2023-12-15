
## Product Search Relevance

The objective of this project is to demonstrate the application of large language models (LLMs) to enhance and expedite product search processes. Unlike traditional product search methods that rely on keyword matches, LLMs facilitate semantic search, leveraging conceptual similarities between words.

The conceptual understanding of word relationships in LLMs is acquired through exposure to diverse documents, allowing the model to recognize associations between terms. For instance, a document discussing the significance of play for "children" might use the term "child," establishing a relationship between the two. Through exposure to various documents, the model learns to identify close associations between related terms, even if they are not explicitly mentioned together.

Many LLMs are available as pre-trained models, having already learned these word associations from a broad range of publicly available information. Leveraging this knowledge, these models can be employed to search the descriptive text of product catalogs for items aligned with a user-supplied search term or phrase. To further enhance performance, the models can undergo a fine-tuning process with additional data specific to a particular site, adapting to the unique language and style used by the retailer or product suppliers.

This solution accelerator will showcase two approaches: one utilizing an off-the-shelf model and another fine-tuned to a specific product catalog. Additionally, the project will address deployment challenges, demonstrating how users can seamlessly deploy a semantic search capability through their Databricks environment.


## Steps to run

To start using a solution accelerator in Databricks follow the below steps: 

1. Attach the `RUNME` notebook to any cluster and execute the notebook via Run-All. A multi-step-job describing the accelerator pipeline will be created, and the link will be provided. The job configuration is written in the RUNME notebook in json format. 
2. Execute the multi-step-job to see how the pipeline runs. 


