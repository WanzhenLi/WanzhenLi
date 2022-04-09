Name:Wanzhen Li
Collabrator: No
Source: https://gist.github.com/dssstr/aedbb5e9f2185f366c6d6b50fad3e4a4
Extension: Yes


Part 0
First, during initialization, we create a dictionary.
To rotate the letters, we want to map each letter to a number. Then to convert the rotated numbers into letters, create an inverse dictionary that maps the numbers back to letters.
In order to encrypt with a Caesar cipher, we need to first create an empty string. Let all the letters in the message loop through the rotation letter function to get the shifted letters.
The process of Caesar decoding is the inverse of encryption. So we just need to rotate the letter function in reverse order to decode.
Breaking the Caesar cipher requires the use of an alphabetical frequency table. First we read the csv file and create a heuristic. This allows us to score each letter, and the one with the max value in the decoded string is the brute force answer.
The vigenere cipher is similar. According to the key letter corresponding to the given key, each letter is shifted by different digits in order.
More detailed thoughs is as the pic below.

![image](https://github.com/WanzhenLi/WanzhenLi/blob/main/readme_pdf.pdf)

Extra:
1.OTP is created by randomly generating a string of characters or numbers that will be at least as long as the longest message that will be sent.
The reason why it's secure is that the key is truly random. As it is a ciphertext-only cryptanalysis, the attacker can't compute the plaintext from the ciphertext without knowlege of the key, even via a brute force search of the space of all keys.
The key is unpredictable。 Each part of the key exists independently. You cannot exploit any predictability in part of a message to derive a key that unlocks the rest of the message: even if you know 50% of the message, the other 50% is opaque. If a brute force search for the key even finds an 8-bit key, the ciphertext will be decrypted as "w" and the other will be decrypted as "z". But you still don't know which one is the actual plaintext.
2.Each part of the key exists independently. You cannot exploit any predictability in part of a message to derive a key that unlocks the rest of the message: even if you know 50% of the message, the other 50% is opaque. If a brute force search for the key even finds an 8-bit key, the ciphertext will be decrypted as "w" and the other will be decrypted as "z". But you still don't know which one is the actual plaintext.


If you use the same key over and over, an attacker can guess fragments of various encrypted messages, and each successful guess will reveal a key, so over times more and more keys are revealed.
That's why it's called ONE time Pad
