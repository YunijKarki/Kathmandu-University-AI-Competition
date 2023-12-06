
# LLM Competition Organized By Kathmandu University




## Problem Statement

 Use LLMs for identifying the table and Key Value(KV) from provided invoices samples. We will be providing api keys for OpenAI to individual teams, with strong monitoring in the usage. If highly overused by any participants, we hold the right to disqualify them from the competition. So we request you to make the openai call carefully. 

KV: For KV, you are required to extract bbox and text for the following keys:

Invoice Number

Issue Date

Total

Table: For Table, you are required to identify the table bbox and table text.
## Evaluation Criteria

The evaluation will be done via the mean of the kv and table extraction.
For KV, the extracted text is compared with ground truth text and fuzzy match should be > 80%. The bbox IOU should also be > 80%. This criteria should be crossed for each 3 KV field. Then, it is considered as a correct KV extraction i.e KV = 1.

For the table, the extracted table text will be compared with the ground truth text. The fuzzy match between these should be > 80%. And IOU of the table bbox > 80% with the ground truth to be considered as a valid extraction i.e, Table = 1.

For eg, for a single document:

If KV = 1 , Table = 1: the extraction score is 1 

If KV = 0, Table = 1, the extraction score is 0.5

In the similar fashion, the score is calculated for all the documents and then the final score is calculated by taking the mean of it.