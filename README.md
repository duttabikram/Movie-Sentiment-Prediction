# Movie-Sentiment-Prediction
HOW THE THINGS WORKS INTERNALLY IN THE MODEL ------
Your text is encoded → padded → numeric tensor (1, 500)
Embedding layer converts numbers → 500×32 matrix
RNN processes all 500 time steps sequentially
Final RNN output → Dense layer → sigmoid output
You get a probability between 0 and 1
HOW THE THING WORK AFTER THE USER INPUT ---------
Lets the user type a movie review.
When the “Classify” button is clicked:
The input is preprocessed into padded numeric sequence.
The IMDB dataset comes with a word_index dictionary.so you first get all the word indices
You load your trained RNN model and pass it in it
Model makes a prediction → returns a probability (between 0 and 1).
Closer to 1 → Positive sentiment
Closer to 0 → Negative sentiment
If probability > 0.5 → classify as “Positive”
Otherwise → “Negative”
Display both sentiment and prediction score on the screen.
