FUNCTION isPalindrome(word: STRING) : BOOLEAN
    // Stop condition: an empty word or a word containing a single character is a palindrome
    IF length(word) <= 1 THEN
        RETURN TRUE
    END IF

    // Compare characters at the ends of the word
    IF firstCharacter(word) equals lastCharacter(word) THEN
        // Recursively test the rest of the word
        RETURN isPalindrome(middleCharacters(word))
    ELSE
        // If there's a difference, it's not a palindrome
        RETURN FALSE
    END IF
END FUNCTION
