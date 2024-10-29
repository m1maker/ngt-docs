## Class: combination

### Members

- `protected int items`: The total number of items from which combinations are to be generated.
- `protected int combinationSize`: The size of each combination.
- `protected array<int> currentCombination`: Holds the current state of the combination being generated.
- `bool repetitionMode`: Indicates whether repetitions are allowed in the combinations.

### Methods

#### Constructor
- Initializes member variables to default values (no items, no combination size, and no repetitions).

#### generate_all_combinations(int items, int combinationSize)
- Generates all possible combinations with repetitions.
- Returns `false` if the input parameters are invalid (not enough items or too small combination size).
- Initializes member variables and sets `repetitionMode` to `true`.

#### generate_unique_combinations(int items, int combinationSize)
- Generates all possible unique combinations.
- Returns `false` if the input parameters are invalid (not enough items or invalid combination size).
- Initializes member variables and sets `repetitionMode` to `false`.

#### next()
- Retrieves the next combination based on whether repetitions are allowed.
- Calls either `nextAllCombinations()` or `nextUniqueCombinations()` depending on `repetitionMode`.

#### reset()
- Resets the state of the combination generator, clearing all member variables and the current combination array.

## Usage

To use this code, you would typically instantiate an instance of the `combination` class and call the appropriate methods based on your needs:

1. **Generate combinations with repetitions:**
   ``` angelscript
   combination comb;
   if (comb.generate_all_combinations(items, combinationSize))
   {
       while (true)
       {
           array<int> nextComb = comb.next();
           if (nextComb.is_empty())
               break;

           // Process the combination
       }
   }
   ```

2. **Generate unique combinations:**
   ``` angelscript
   combination comb;
   if (comb.generate_unique_combinations(items, combinationSize))
   {
       while (true)
       {
           array<int> nextComb = comb.next();
           if (nextComb.is_empty())
               break;

           // Process the combination
       }
   }
   ```
