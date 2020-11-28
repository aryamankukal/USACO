f = open("crossroad.in", "r")
p = open("crossroad.out", "w")

N = int(f.readline()) # a positive integer at most 100

allIDandPos = []
for x in range(N):
    IDandPosition = f.readline().strip("\n")
    IDandPosition = IDandPosition.split(" ")
    ID = IDandPosition[0]
    position = IDandPosition[1]
    allIDandPos.append([ID, position])

allID = []
for pair in allIDandPos:
    allID.append(pair[0])

IDandPosChanges = {}

for ID in allID:
    currentIDPositionChanges = []
    for pair in allIDandPos:
        if pair[0] == ID:
            currentIDPositionChanges.append(pair[1])
    IDandPosChanges[ID] = currentIDPositionChanges

totalCrossings = 0
for value in IDandPosChanges.values():
    if len(value) > 1:
        consecutiveCombinationPairs = [value[i: j] for i in range(len(value)) for j in range(i + 1, len(value) + 1) if len(value[i:j]) == 2]
        for pair in consecutiveCombinationPairs:
            if "0" in pair and "1" in pair:
                totalCrossings += 1

p.write(str(totalCrossings))
p.close()
