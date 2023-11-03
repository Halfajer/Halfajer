- 👋 Hi, I’m @Halfajer
- 👀 I’m interested in ...
- 🌱 I’m currently learning ...
- 💞️ I’m looking to collaborate on ...
- 📫 How to reach me ...

<!---
Halfajer/Halfajer is a ✨ special ✨ repository because its `README.md` (this file) appears on your GitHub profile.
You can click the Preview link to take a look at your changes.
--->
import random
# Postavljanje inicijalnih vrijednosti
score = 0
level = 1
target_position = random.randint(1, 10)
# Glavna petlja igre
while True:
print(f"Level {level}, Score: {score}")
print("Aim your arrow and shoot (1-10):")
try:
player_input = int(input())
# Provjera da li je igrač pogodio metu
if player_input == target_position:
print("Hit!")
score += 1
else:
print("Miss!")
# Povećaj level nakon svakih 5 pogodaka
if score % 5 == 0:
level += 1
# Postavi novu poziciju mete
target_position = random.randint(1, 10)
except ValueError:
print("Unesite broj od 1 do 10.")
