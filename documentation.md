##Dataset Used
Dolly-HH-RLHF Yoruba Response Dataset from Hugging Face. The dataset was selected it because it contains diverse, natural Yoruba sentences across different topics, which makes it valuable for language modeling or chatbot training. The dataset also contained English language translations and Hugging Face SQL Console was used to write a query to select the Yoruba response column that is needed for the task.

##SQL CODE: 
SELECT Response_Yoruba 
FROM train;
Run the query and download the result in .csv file format.

##Preprocessing Steps
1.	Uploaded the CSV file into Google Colab. 
2.	Imported the necessary/required library (pandas, string, and re)
3.	Load the file path (pd.read_csv(‘/content/ccibeekeoc42-dollyhhrlhf-yoruba.csv’))
4.	Showed the first few rows of the dataset
5.	Cleaned the text by checking for null values, removing punctuation and extra whitespace while preserving Yoruba characters.
6.	Generated basic statistics such as total word, sentence counts, and most common words to understand the dataset better.

##Challenges and Lessons Learned

##Challenges:
1. Avoiding removal of special Yoruba characters (ẹ, ṣ, ọ, etc.) during punctuation cleaning.
2. Avoiding removel of fullstops (.) at the end of every sentences.
3. Ensuring whitespace normalization did not disrupt sentence structure.

##Resolutions:

1. Used a customized regex pattern (r'[^\w\sÀ-ÿ]') to preserve Unicode characters.
2. Visual inspection after cleaning helped validate the results.

##Lessons Learned:
1. Always inspect unique linguistic patterns before applying generic text cleaning rules.
2. Frequency analysis helps uncover common patterns even in unfamiliar languages.

##Google Colab link: 
https://colab.research.google.com/drive/1iwogoIgJr6Gu4WvgkGEhsWYlAmLp8l6o?usp=sharing

##Dataset link: 
https://drive.google.com/file/d/1ySxhqtZM0QkFvqNg7x9kDO321EP4PMIX/view?usp=sharing

