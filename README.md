
Suspects = ['A', 'B', 'C', 'D']
check_claims = [[1,True],[3,True],[1,True],[1,False],
                [2,True],[2,False],[2,True],[2,False],
                [0,False],[4,False],[4,True],
                [3,True],[3,False],[4,True],[4,True],
                
                [1,False],[4,False],[3,False],[3,True],[3,False]]
"""[1,True]A i met C,[3,True]C i didnt meet A ,[1,True] D says A did this,[1,False] B says D lied A didnt,
[2,True] A says B is guilty,[2,False] B says i didnt do this,
[2,True] D says B lies,[2,False] C says B is innocent,[0,False] teaf didnt know..,
[4,False] B says D didnt do this,[4,True]B says D lies,[3,True] C lies,[3,False] C doesnt lie
[4,True] C says D know driving, [1,False] A beleives i didnt do this,
[4,False] A beleives D didnt do this,
[3,False] A believes D didnt do this,[3,True] B believs C did this"""



i=j=k=z=0
for T in check_claims:
        if T[0] == 1:
            if T[1] == True:
                i +=1
            elif T[1] == False: 
                i-=1
        elif T[0] == 2:
            if T[1] == True:
                j+=1
            elif T[1] == False:
                j-=1
        elif T[0] == 3:
            if T[1] == True:
                k+=1
            elif T[1] == False:
                k-=1
        elif T[0]==4:
            if T[1] == True:
                z+=1
            elif T[1] == False:
                z-=1
Sus = {'A':i,'B':j,'C':k,'D':z}
for teaf , sus in Sus.items() :
    if  sus == 1:
        print(f"{teaf} is the teaf!")


