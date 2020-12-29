# congenial-potato
# This is my first program I created on my own. The program runs user generated input of possible places to travel
# to and having them run through random
# number generators. This is more for coding practice than anything serious but I have some things I want to add to it. 
# Enjoy!
import random
pPlaces = {'Idaho': 0, 'San Francisco': 0, 'South Florida': 0, 'Colorado': 0
}
def randomChoiceLoop():
  while max(pPlaces, key=pPlaces.get) != 'Colorado':
    for i in pPlaces:
      x = random.choice(tuple(pPlaces))
      pPlaces[x] += 1
      print(pPlaces)

for i in range(10_000_000):
  x = random.choice(tuple(pPlaces))
  pPlaces[x] += 1

print(pPlaces)
print(max(pPlaces, key=pPlaces.get))
