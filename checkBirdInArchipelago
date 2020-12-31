def binary_search(findbird, birdlist):
    first = 0
    last = len(birdlist) - 1
    found = False

    while first <= last and not found:
        midpoint = (first + last) // 2
        if birdlist[midpoint] == findbird:
            found = True
        else:
            if findbird < birdlist[midpoint]:
                last = midpoint - 1
            else:
                first = midpoint + 1
    return found

commonBirdsOfAzores = open("BirdsAzores", "r")
azores = commonBirdsOfAzores.read().split(",")
azores.sort()
azores = [eachBird.casefold() for eachBird in azores]

commonBirdsOfCanaryIslands = open("BirdsCanaryIslands", "r")
canaryIslands = commonBirdsOfCanaryIslands.read().split(",")
canaryIslands.sort()
canaryIslands = [eachBird.casefold() for eachBird in canaryIslands]

commonBirdsOfCapeVerde = open("BirdsCapeVerde", "r")
capeVerde = commonBirdsOfCapeVerde.read().split(",")
capeVerde.sort()
capeVerde = [eachBird.casefold() for eachBird in capeVerde]

commonBirdsOfMadeira = open("BirdsMadeira", "r")
madeira = commonBirdsOfMadeira.read().split(",")
madeira.sort()
madeira = [eachBird.casefold() for eachBird in madeira]

print("From which Macaronesian archipelago would you like to search for a bird?")
pickArchipelago = input()
archipelago = False
while (archipelago != True):
    archyPelly = ""
    if(pickArchipelago == "Azores"):
        archyPelly = azores
        archipelago = True
        break
    elif (pickArchipelago == "Canary Islands"):
        archyPelly = canaryIslands
        archipelago = True
        break
    elif (pickArchipelago == "Cape Verde"):
        archyPelly = capeVerde
        archipelago = True
        break
    elif (pickArchipelago == "Madeira"):
        archyPelly = madeira
        archipelago = True
        break
    else:
        print("Invalid archipelago, you silly goose!")
    pickArchipelago = input()

print("Enter the name of the bird: ")
birdToBeChecked = input()

while birdToBeChecked != "PIP PIP":
    if binary_search(birdToBeChecked.casefold(), archyPelly):
        print("Yes, we have that bird.")
    else:
        print("No, we do not have that bird.")

    birdToBeChecked = input()
