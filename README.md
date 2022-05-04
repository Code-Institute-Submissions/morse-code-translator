# Morse Code Translator in Python

Morse code is a method of transmitting text information as a series of on-off tones, lights, or clicks that can be directly understood by a skilled listener or observer without special equipment. It is named for Samuel F. B. Morse, an inventor of the telegraph.

To run the program type the following command in the terminal: `python run.py`
## Algorithm

The algorithm is very simple. Every character in the English language is substituted by a series of ‘dots’ and ‘dashes’ or sometimes just singular ‘dot’ or ‘dash’ and vice versa. The Morse code used is just a small set of the International standard.

## Encryption

1. In the case of encryption, we extract each character (if not space) from a word one at a time and match it with its corresponding morse code stored in whichever data structure we have chosen(if you are coding in python, dictionaries can turn out to be very useful in this case).
2. Store the morse code in a variable that will contain our encoded string and then we add a space to our string that will contain the result.
3. While encoding in morse code we need to add 1 space between every character and 2 consecutive spaces between every word.
4. If the character is a space then add another space to the variable containing the result. We repeat this process till we traverse the whole string.

## Decryption

1. In the case of decryption, we start by adding a space at the end of the string to be decoded (this will be explained later).
2. Now we keep extracting characters from the string till we are not getting any space.
3. As soon as we get a space we look up the corresponding English language character to the extracted sequence of characters (or our morse code) and add it to a variable that will store the result.
4. Remember keeping track of the space is the most important part of this decryption process. As soon as we get 2 consecutive spaces we will add another space to our variable containing the decoded string.
5. The last space at the end of the string will help us identify the last sequence of morse code characters (since space acts as a check for extracting characters and start decoding them).

## Implementation

Python provides a data structure called a `dictionary` which stores information in the form of key-value pairs which is very convenient for implementing a cipher such as a morse code. We can save the morse code chart in a dictionary where (key-value pairs) => (English Characters-Morse Code). The plaintext (English characters) takes the place of keys and the ciphertext (Morse code) forms the values of the corresponding keys. The values of keys can be accessed from the dictionary in the same way we access the values of an array through their index and vice versa.

## Testing

Test text to Morse and vice versa:
![test text](/images/text.png)
Test numbers to Morse and vice versa:
![test numbers](/images/numbers.png)
Test punctuation to Morse and vice versa:
![test punctuation](/images/punctuation.png)
Test all to Morse and vice versa:
![test all](/images/all.png)

## Deployment

This project was deployed using Code Institute's mock terminal for Heroku.

Steps for deployment:
* Fork or clone this repository
* Create a new Heroku app
* Set the buildbacks to `Python` and `NodeJS` in that order
* Link the Heroku app to the repository
* Click on Deploy

## Credits

* Code Institute for the deployment terminal
* Wikipedia for the details of the Morse Code