# Algorithm
 an algorithm that read a sentence, which ends with a point, character by character...
 
 Here's an algorithm in pseudocode that reads a sentence, character by character, and determines the length of the sentence, the number of words in the sentence, and the number of vowels in the sentence:

sql
Copy code
BEGIN
    SET length = 0
    SET word_count = 1
    SET vowel_count = 0
    READ input_sentence
    FOR each character IN input_sentence DO
        IF character = " " THEN
            SET word_count = word_count + 1
        ELSEIF character IN ["a", "e", "i", "o", "u", "A", "E", "I", "O", "U"] THEN
            SET vowel_count = vowel_count + 1
        ENDIF
        SET length = length + 1
    END FOR
    SET length = length - 1 // to exclude the period
    WRITE "Length of sentence: ", length
    WRITE "Number of words in sentence: ", word_count
    WRITE "Number of vowels in sentence: ", vowel_count
END
In this algorithm, we first initialize three counters: length for the length of the sentence, word_count for the number of words in the sentence, and vowel_count for the number of vowels in the sentence. We then read in the input sentence and loop through each character in the sentence.

In the loop, we check if the character is a space. If it is, we increment word_count since we assume that words are separated by a single space. If the character is a vowel (either lowercase or uppercase), we increment vowel_count. We also increment length for each character in the sentence.

Finally, we subtract 1 from length to exclude the period at the end of the sentence, and output the values of length, word_count, and vowel_count.

This algorithm should work for most cases, but there are some potential edge cases that it does not handle. For example, if there are multiple spaces between words, or if there are non-alphabetic characters in the sentence that should be counted as part of a word, the word count may be incorrect. However, for most simple sentences, this algorithm should be sufficient.
