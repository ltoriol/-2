# -2
class Pet:
    def __init__(self, name, species):
        self.name = name
        self.species = species
        self.energy = 100

    def sleep(self, hours):
        self.energy += hours * 10
        print(f"{self.name} виспався і має тепер {self.energy} одиниць енергії.")

    def play(self, hours):
        if self.energy >= hours * 5:
            self.energy -= hours * 5
            print(f"{self.name} грається і втрачає {hours * 5} одиниць енергії.")
        else:
            print(f"{self.name} занадто втомився для гри!")

my_pet = Pet(name="Мурзик", species="Кіт")

my_pet.sleep(3)
my_pet.play(2)
