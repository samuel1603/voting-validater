# voting-validater
This is program to how the vote is validate
eligiable=int(input("enter your age :"))

if eligiable<=18:
    print("you are not eligiable to vote")
    raise Exception("TRY AGAIN")
                
else:
    print("you are eligiable to vote")
    

dmk=0
admk=0

vote_id=[1,2,3,4,5,6,7,8,9,10]

nom_of_voter=len(vote_id)

while True:
    if vote_id==[ ]:
        print("voting seesion is over")
        if dmk>admk:
            print("dmk is won")
            break
        elif dmk==admk:
            print("vote tie")
            break
        else:
            print("admk is won")
            break
    else:
        voter=int(input("enter your voter id:"))
        if voter in vote_id:
            print("you are voter")
            vote_id.remove(voter)
            points=int(input("you are vote for dmk=1 or admk=2:"))
            if points==1:
                dmk+=1
                print("thank you for voting,your vote is vaild")
            elif points==2:
                admk+=1
                print("thank you for voting your vote is vaild")
        else:
            print("your not a voter or already voted")
