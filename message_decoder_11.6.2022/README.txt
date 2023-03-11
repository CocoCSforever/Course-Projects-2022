Summary:
    The decoding algorithm uses a stack. Reading from left to right, each character is placed on the stack, except for the characters * (asterisk) and ^ (caret). Those two characters have special meaning. When the * is encountered, one character is popped from the stack and appended to the solution string. When the ^ is encountered, two characters are popped and appended to the solution string, one after the other (pop one and append it to the string, pop the next and append it to the string).
    (NOT cryptographically secure)


Run decoder.py
// ---- OUTPUT ---- //
b-5es^m9c*u?er^xl0t*a
secret

na0s*9-o*veXul^z-2it^,no^pr8
solution

zeM^un-e*0 t^a*l t^75*4a1:^s35*A,P ^2NM* ,^Mc.+GcO^ t^3*,0^2 ^5m0*x22^
Meet at 5:15 PM, Oct 30, 2022