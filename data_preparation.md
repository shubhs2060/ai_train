For Model Training we need to prepare some data

To prepare data it involves these 3 steps

1. Crawl the data from the internet

Data can be crawled using a script
We can also use some crwaler that are available online to get cleaned crawl data

2. Data cleaning
   We need to filter data that is crawled to remove duplicates and to get only required data

3. Tokenization
   Raw cleaned data has to converted to tokens so that model can search on that

There are commonly 3 types of tokenziation techiniques

1. Word level
   Not being used now as it was unoptimised. Here we use to genarate a list of words from raw text and assgin tokens to each of them

2. Character level
   Not being used now as it was unoptimised. Here we use to genarate a list of characters from raw text and assgin tokens to each of them

3. Sub word level
   Being used at most places were we break the words and assign tokens to each of them
   example - input - "Perfectly fine"
   output - ["Perfect","ly","fine"]
   Common Algorithms:

Byte Pair Encoding (BPE) — used in GPT and OpenAI models.

WordPiece — used in BERT.

SentencePiece (Unigram) — used in models like T5 and ALBERT.

One example is tiktokenizer provided by Open AI
so you can do a pip install tiktokenizer

tokenzier = Tokenizer
tokenizer.encode("I am sleeping")
output - [23,1,32323]

tokenizer.decode([23,1,32323])
output - I am sleeping