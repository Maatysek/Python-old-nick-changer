# Python-old-nick-changer
#Basic python code to change your nick, to the one like in the old times. Example: Matej --> M4t3j

def transform_nick(stary_nick):
    novy_nick = ""

    for char in stary_nick:
        if char.lower() == 'a':
            novy_nick += '4'
        elif char.lower() == 'e':
            novy_nick += '3'
        elif char.lower() == 'i':
            novy_nick += '!'
        elif char.lower() == 's':
            novy_nick += '$'

        # pravidla

        else:
            novy_nick += char

    return novy_nick

# nick input
stary_nick = input("Please enter your old nick: ")

#kontrola
if isinstance(stary_nick, str):
    # funkce na nick
    novy_nick = transform_nick(stary_nick)
    print(f"Your new nick: {novy_nick}")
else:
    print("Not a valid nick. Please enter a valid nick.")
