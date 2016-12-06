
""" Hello! These are just some simple lines of codes from python."""
print "Here is a simple game that I created just for fun...And this is in relation to the game Modern Warfare 2 and 3"
from sys import exit # ill just write this anyway

def centre_room():
    print "You go through a door, only to find a lone AK-47 Hologram in front of you. You put on your night vision goggles, only to find that the room is all clear."
    print "Do you go forward to take the gun?"

    choice = raw_input("> ")

    if choice == "Yes":
        print "You rush forward to grab it, and no threats await you."
        print "You proceed to yet another room with the gun in hand. "
        right2_room()
    elif choice == "No":
        dead ("You get clubbed for standing on the spot for too long. You die!!! Get rekt!")
    else:
        dead ("You are shot by an unknown gunman and you die a grisly death. Good game!")
def right2_room():
    print "You are back at the room where Makarov is. You creep in without him noticing through the back door."
    print "Do you want to kill him?"

    choice = raw_input("> ")

    if choice == "Yes":
        print "You aim the AK47 at his head and fire a single shot using the scope. Blood splatters on the wall."
        print "You win!!!"
        exit(0)
    elif choice == "No":
        dead ( "Why do you choose this option? He notices you and riddles your body with bullets. GET REKT!!!")

def right_room():
    print "You pick up a knife and creak open the door."
    print "To your horror, you see your foe and understand who you came here to kill..."
    print "It is MAKAROV!!!!" # this is just a character in the game...
    print "Your brain processes the scene at hand."
    print "You have two options, to 'creep past him' or 'kill him'. However, you realise that any sudden actions will alert Makarov and you will die."
    print "What do you choose?"

    choice = raw_input("> ")

    if "creep" in choice:
        print "You enter yet another room without him noticing... You see a good chance..."
        centre_room()
    elif "kill" in choice:
        dead("Suddenly, he swings around and catches you by the hand. He has a RMD in hand and rounds riddle your body...")
    else:
        dead("He notices a figure [you] and he swings around with an RMD in hand and rounds riddle your body....")

def left_room():
    print "You pick up an M4A1 Grenadier and 4 Flashbangs."
    print "Suddenly, your security perimeter has been breached!"
    print "A horde of Russian Infidels surge in. You have two choices- to swap your gun for a machine gun which will never run out of bullets or to lob a flashbang and shoot them."
    print "Choose one of the two options - 'swap your gun for a machine gun' or 'lob a flashbang and shoot'"
    choice = raw_input("> ")

    if "swap" in choice:
        print "You get pass the horde of them. Yay!!"
        right_room()
    if "flashbang" or "lob" in choice:
        dead ("there's just too many of them you know.. a flashbang wont really work that well. ")
    elif "shoot" in choice:
        dead("Don't try shooting them... they swarm you with AK-47s and a whole lot of grenades.")

    else:
        print "I have no idea what does that mean..."


def dead(why):
    print why, "Good job! You die!"
    exit(0)

def start():
    print "Disclaimer: Print exactly what the options tell you , if not this game will not work well."
    print "You are currently in a dark room. You can hear shouts outside, coupled with intense gunfire. Your comrades are providing cover fire while you are on a mission..."
    print "You put on your night vision goggles and discover that there are two doors - one on your 'left' and 'right'."
    print "Which door do you choose?"
    choice = raw_input(" >")

    if choice == "centre":
        centre_room()
    elif choice == "left":
        left_room()
    elif choice == "right":
        right_room()
    else:
        dead ("A stray grenade lands in front of you. You try to grab it and throw it back, but whoever threw it cooked first. You die. Good job!")
start()
