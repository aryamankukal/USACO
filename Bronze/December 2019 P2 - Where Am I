f = open("whereami.in", "r")
p = open("whereami.out", "w")

N = int(f.readline())
NCharacters = f.readline()

for K in range(1, N-1):

    subStringsOfLengthK = [NCharacters[i: j] 
                          for i in range(len(NCharacters)) 
                          for j in range(i + 1, len(NCharacters) + 1)
                          if len(NCharacters[i:j]) == K]

    for subString in subStringsOfLengthK:
        if subStringsOfLengthK.count(subString) > 1:
            break
        elif subStringsOfLengthK.count(subString) == 1 and subStringsOfLengthK[-1] == subString:
            p.write(str(K))
            quit()

p.close()
