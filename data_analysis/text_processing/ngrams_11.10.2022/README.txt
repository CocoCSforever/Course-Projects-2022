Summary:
    This project serves as a way to practice machine learning models for natural language processing where frequencies of words in sequence can be important features.
    Short sequences of word tokens are referred to as n-grams, where n is the number of tokens in each item. So, a count of unigrams is simply a count of occurrences for each word token. Bigrams refer to pairs of words in sequence (for example, "pairs_of", "of_words", "words_in", and "in_sequence") and trigrams are triples of words in sequence ("triples_of_words", "of_words_in", "words_in_sequence").
    The longer the n-gram, the less frequently it will be found in a given text, so n-grams much longer than trigrams are often too sparsely distributed to be worth collecting.


Implementation details
· All alphabetical characters should be rendered in lowercase. Our n-grams will be case insensitive.
· N-grams will be collected only within sentences. Words on the end of one sentence will not form n-grams with words on the beginning of the next sentence. For this reason, we will need to split each paragraph of text into the sentences that compose it.
· In order to use periods to split sentences, we'll need to get rid of other periods first, such as those at the end of abbreviated like "Mr." and "Dr.". These words will have to be dealt with explicitly. Your pre-processor does not have to be exhaustive, but it should deal with the most common words of this nature.
· We will keep apostrophes in. We want to be able to distinguish won't from wont, and without a more powerful tokenizer (with slightly deeper linguistic analysis) this means keeping the apostrophes. This means that burton and burton's will be treated as two distinct tokens.
· We will treat commas as tokens themselves. The way I approached this was to render each comma as the all caps token COMMA. As you can see above, this token winds up being one of the most frequent unigrams and part of several frequent bigrams.
· All other punctuation: quotes, parentheses, dashes, etc. will be stripped out.


Run frequencies.py
// ----OUTPUT---- //
Top 10 unigrams:
         ('the', 0.089)
         ('COMMA', 0.07)
         ('and', 0.039)
         ('a', 0.035)
         ('of', 0.031)
         ('to', 0.014)
         ('for', 0.012)
         ('in', 0.012)
         ('with', 0.012)
         ('by', 0.01)
Top 10 bigrams:
         ('COMMA_the', 0.016)
         ('in_the', 0.01)
         ('and_the', 0.008)
         ('COMMA_and', 0.008)
         ('of_the', 0.008)
         ('into_the', 0.006)
         ('the_world', 0.006)
         ('for_the', 0.004)
         ("tim_burton's", 0.004)
         ('corpse_bride', 0.004)
Top 10 trigrams:
         ('the_world_of', 0.004)
         ('mr_burton_and', 0.004)
         ('the_land_of', 0.004)
         ("it's_a_dead", 0.002)
         ('a_dead_scene', 0.002)
         ('dead_scene_COMMA', 0.002)
         ('scene_COMMA_but', 0.002)
         ("COMMA_but_that's", 0.002)
         ("but_that's_a", 0.002)
         ("that's_a_good", 0.002)