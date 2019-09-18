# DM_TowerHanio
This is a handin for Tower of Hanio for PBA discrete math 2019 SOFT fall

# Recursion
The 3 criteria for recursion:
1) A base case: When discNumber is 1, we no longer call the method (discnumber 1 is the smallest disc)
2) A direction: We traverse the dicsnumber from X >= 1 down to 1
3) Repetition: If discnumber > 1, we repeat the methodcall 

# Algorithm written in javascript<br>
Note - that the async/await is solely for gfx.
```
async function DoIt( discnumber,  fromTower,  interTower,  toTower){
                if(discnumber == 1){
                  await  move(fromTower, toTower);
                }else
                {
                   await DoIt(discnumber-1, fromTower, toTower, interTower);
                   await  move( fromTower, toTower);
                   await DoIt(discnumber-1, interTower,fromTower,toTower);
                }
            }
```

# See it in action
Clone the repo and navigate to the index.html file using a browser (due to gfx - Safari not so much)
