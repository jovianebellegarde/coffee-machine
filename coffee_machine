class CoffeeMachine:

    def __init__(self, money, water, milk, beans, cups):
        self.money = money
        self.water = water
        self.milk = milk
        self.beans = beans
        self.cups = cups

    def remaining(self):
        print(f'\nThe coffee machine has:\n'
              f'{self.water} ml of water\n'
              f'{self.milk} ml of milk\n'
              f'{self.beans} g of coffee beans\n'
              f'{self.cups} disposable cups\n'
              f'${self.money} of money')

    def espresso(self):
        if self.water >= 250 and self.beans >= 16 and self.cups >= 1:
            print('\nI have enough resources, making you a coffee!\n')
            self.water -= 250
            self.beans -= 16
            self.cups -= 1
            self.money += 4
        else:
            if self.water < 250:
                not_enough = 'water'
            elif self.beans < 16:
                not_enough = 'beans'
            else:
                not_enough = 'cups'
            print(f'Sorry, not enough {not_enough}!\n')

    def latte(self):
        if self.water >= 350 and self.milk >= 75 and self.beans >= 20 and self.cups >= 1:
            print('I have enough resources, making you a coffee!\n')
            self.water -= 350
            self.milk -= 75
            self.beans -= 20
            self.cups -= 1
            self.money += 7
        else:
            if self.water < 350:
                not_enough = 'water'
            elif self.milk < 75:
                not_enough = 'milk'
            elif self.beans < 20:
                not_enough = 'beans'
            else:
                not_enough = 'cups'
            print(f'Sorry, not enough {not_enough}!')

    def cappuccino(self):
        if self.water >= 200 and self.milk >= 100 and self.beans >= 12 and self.cups >= 1:
            print('I have enough resources, making you a coffee!')
            self.water -= 200
            self.milk -= 100
            self.beans -= 12
            self.cups -= 1
            self.money += 6
        else:
            if self.water < 200:
                not_enough = 'water'
            elif self.milk < 100:
                not_enough = 'milk'
            elif self.beans < 12:
                not_enough = 'beans'
            else:
                not_enough = 'cups'
            print(f'Sorry, not enough {not_enough}!\n')

    def buy(self):
        coffee_choice = input('\nWhat do you want to buy? 1 - espresso, '
                              '2 - latte, 3 - cappuccino, back - to main '
                              'menu:\n')

        if coffee_choice == '1':
            self.espresso()
        elif coffee_choice == '2':
            self.latte()
        elif coffee_choice == '3':
            self.cappuccino()
        else:
            return

    def fill(self):
        add_water = int(
            input('\nWrite how many ml of water you want to add:\n'))
        add_milk = int(input('Write how many ml of milk you want to add:\n'))
        add_beans = int(
            input('Write how many grams of coffee beans you want to '
                  'add:\n'))
        add_cups = int(
            input('Write how many disposable coffee cups you want to '
                  'add:\n'))

        self.water += add_water
        self.milk += add_milk
        self.beans += add_beans
        self.cups += add_cups

    def take(self):
        self.money -= self.money
        print(f'I gave you ${self.money}\n')

    def main(self):
        while True:
            choice = input(
                '\nWrite action (buy, fill, take, remaining, exit):\n')

            if choice == 'buy':
                self.buy()
            elif choice == 'fill':
                self.fill()
            elif choice == 'take':
                self.take()
            elif choice == 'remaining':
                self.remaining()
            else:
                break


if __name__ == "__main__":
    coffee_machine = CoffeeMachine(550, 400, 540, 120, 9)
    coffee_machine.main()
