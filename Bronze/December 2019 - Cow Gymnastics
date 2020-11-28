from itertools import combinations

f = open("gymnastics.in", "r")
p = open("gymnastics.out", "w")

KandN = f.readline().strip("\n")
KandN = KandN.split(" ")
K = int(KandN[0])
N = int(KandN[1].strip("\n"))

listOfListsOfEachSession = []
for i in range(K):
    currentSession = f.readline().strip("\n")
    currentSession = currentSession.split(" ")
    listOfListsOfEachSession.append(currentSession)

combs = [] # apply to all the rows because the same numbers are in each row
pairsOfCombinations = list(combinations(listOfListsOfEachSession[0], 2))
for pair in pairsOfCombinations:
    listPair = list(pair)
    indexOfPair = pairsOfCombinations.index(pair)
    pairsOfCombinations.remove(pair)
    pairsOfCombinations.insert(indexOfPair, listPair)

listOfConsistentPairs = []

consistent = False
for pair in pairsOfCombinations:
    for session in listOfListsOfEachSession:
        if session.index(pair[0]) < session.index(pair[1]):
            consistent = True
        else:
            consistent = False
            break
    if consistent == True:
        listOfConsistentPairs.append(pair)
    consistent = False

p.write(str(len(listOfConsistentPairs)))
p.close()
