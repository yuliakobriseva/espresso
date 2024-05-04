# espresso
class EspressoMachine:
    def __init__(self, water_level):
        self.water_level = water_level

    def make_espresso(self):
        if self.water_level > 0:
            print("Making espresso...")
            self.water_level -= 1
            print("Espresso is ready!")
        else:
            print("Cannot make espresso. Please refill water.")

    def refill_water(self, amount):
        print(f"Refilling water by {amount} units.")
        self.water_level += amount

# Example usage
if __name__ == "__main__":
    # Creating an instance of the EspressoMachine class
    espresso_machine = EspressoMachine(water_level=5)  # Assume initial water level is 5 units

    # Making espresso
    espresso_machine.make_espresso()

    # Refilling water and making espresso again
    espresso_machine.refill_water(3)
    espresso_machine.make_espresso()
