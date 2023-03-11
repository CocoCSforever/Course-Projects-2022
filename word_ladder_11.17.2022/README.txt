Summary:
    This project is to implement a word ladder that connects from one word to another, which is formed 
by changing one letter at a time with the constraint that at each step the sequence of letters still forms a valid word.
    The file words_alpha.txt provides the list of valid words and is loaded into the program as a dictionary of sets.
    Word ladders can be made between words of varying lengths by insertion, deletion, alteration 
of a single letter to or from anywhere in a word at each step.


Implementation:
    1. Initialize a queue containing a single stack, which in turn contains the first word in the word ladder.
    2. For each element in the queue (initially just one):
        Dequeue the element, which is a stack. Peek at its top item (a word). For each character in the word:
            For each letter in the alpahbet:
                Replace the character with that letter to generate a candidate new word.
                Check the candidate to see if it is an English word.
                    If it is an English word:
                        Make a duplicate of the stack and push the new word onto the new stack.
                            If the word is the last word of the word ladder, return the new stack.
                            If the word is not the last word of the ladder, enqueue the new stack onto the end of the queue
    3. If the queue is empty, return None, otherwise, continue with step 2.

Run word_ladder_app.py