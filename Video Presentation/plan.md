## Plan
1. Introduction (1 min)
	- Briefly explain the problem tackled by the project
	- Discuss how companies like Snap Vision are working towards improving visual search tools in the fashion industry (Show Snap Vision website)
	-   Mention the dataset supplied by Snap Vision consisting of 3 or more photographs of the same fashion item with 1500 different items within the dataset (Show examples of dataset)
	-   State the project's goal to explore how better feature representations can be realized using this dataset with additional data from retail sites (show presenter)
2. Initial Thinking (2 mins)
	-   Discuss the group's approach to the project (Show linitial papers and git repos visited for embeddings)
	-   Mention the use of GitHub repository for sharing code segments (show group's git repo)
	-   Explain the difficulty of extracting feature vectors without domain knowledge of model architecture (Show some examples of broken code)
	-   Mention the use of YOLOv5, a popular computer vision model, for approximating feature vectors (Show YOLOv5 Git repo)
	-   Discuss the effectiveness of the YOLOv5 model after 20 and 100 epochs (Show train/test loss graphs)
	-   Mention the importance of resizing images to 224x224 and using Google Colab for better collaboration and processing power (show colab notebook used for training)
3. Work So Far (2 mins)
	-   Discuss the use of YOLOv5 model on augmented data (flipped, rotated, etc. assuming this is done by video recording time)
	-   Mention the addition of Vinted data to the finetuned YOLOv5 model to test feature embeddings for new images (show examples of vinted data)
	-   Discuss the use of data visualization for evaluating results (Show the T-SNE, PCA tensorboard and demonstrate it's weakness)
4. Challenges (2 mins)
	-   Mention the slower speed of YOLOv8 and the decision to use YOLOv5
	-   Discuss the lack of metadata and multiple items of clothing within a single image
	-   Show an example of the problem with people's 'search images' needing to be specific enough (look at the incorrect predictions notebook)
	-   Mention the evaluation difficulties and the plan to evaluate using the current dataset and new data scraped from other websites (show the euclidian and cosine similarity plots)
	- Explain how the nearest vectors in the space can be used as an evaluation metric on new data.
1. Conclusion (1 min)
	-   Summarize the main points of the presentation
	-   Encourage feedback and questions from the audience