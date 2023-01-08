PARODY PET 08/22/2022

**Inspiration**

I needed a way to accurately measure my dogs’ food to control their weight. They are small dogs, and the food instructions provide a wide range. Also, the available food calculators recommend way more food than my dogs should eat. Not sure why this, but hope to avoid that pitfall and dial the amounts in more accurately.

**Initial Approach**

Although Parody Pet is a fictitious brand, I plan to use suggested measurements from popular high-end foods as an initial measurement to adjust. I will also use the amounts I that work for maintaining my dogs’ weights compare calculations. I anticipate the cat and bird foods will have more variance unless I can work with numbers from friends’ pets to compare.

**Goal**

Program should calculate the correct amount of food for the desired weight, whether to maintain current weight or lose weight.

**Thoughts**

Three pet types: bird, cat, dog

Inputs: pet name, age (years/months), weight (pounds/ounces), and goal weight

Selection: type of pet

*Example:*

	Mr. Pickles
	age: 8 years 11 months
	weight: 17 pounds 8 ounces
	goal weight: 17 pounds 8 ounces

Outputs: Food Name (different for baby, adult, and senior), how much food to maintain current weight, and how much to lose weight – maybe include suggestion for incremental decrease and consulting veterinarian.

**Organization**

*Interfaces*

PetInfo interface to create contract for pet type, name, age, weight, and goal weight.
BirdCalculator Interface
CatCalculator Interface
DogCalculator Interface

*Classes*

Abstract Pet class implements PetInfo
Bird extends Pet, implements BirdCalculator
Cat extends Pet, implements CatCalculator
Dog extends Pet, implements DogCalculator

*PetInfo*

I am wondering if PetInfo interface is necessary. Going to think on this for a bit.

If this is used, should it be one public void method or a method for each of species, name, age, weight, and goal weight?

* These should each be different methods:
	* species will determine which pet and calculator is used
	name will print something about the name “What a great name!”
	* age will determine which pet food is used (young, adult, senior)
	weight will be used to determine how much food is needed to maintain
	goal weight will provide the necessary information to adjust the food

Do we want to know if pet is male or female?

BirdCalculator interface

birdFoodCalculator(…
