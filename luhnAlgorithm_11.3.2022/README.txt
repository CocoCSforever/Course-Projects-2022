Summary:
    Luhn’s algorithm, also known as the modulus 10 or mod 10 algorithm, is a checksum formula used to validate a variety of identification numbers, 
    such as credit card numbers and ID numbers. luhn.py will ask for an account number and determines whether or not the number is valid using Luhn’s algorithm.


Implementation:
    1. Beginning with the second to right-most digit, modify every other digit moving from right to left as follows:
        Double the digit's value.
        If the resulting number is a two digit number, add the first digit of that value to the second digit, yielding a single digit number.
    2. Add the sum of the modified digits to the sum of the digits from the original sequence which were skipped over in step 1.
    3. If the resulting sum is evenly divisible by 10, the sequence is valid. If the resulting sum is not divisible by 10, the sequence is not valued.
