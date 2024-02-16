Approach and Explanation of Lasagna Cooking Functions

To tackle the task of helping Lucian cook an exquisite lasagna from his favorite cookbook and managing his time effectively, we employ a modular approach with three functions: `remainingMinutesInOven`, `preparationTimeInMinutes`, and `totalTimeInMinutes`.

1. Constants Initialization:
     EXPECTED_MINUTES_IN_OVEN: A constant representing the expected time the lasagna should spend in the oven, set to 40 minutes.
     PREPARATION_MINUTE_PER_LAYER: A constant representing the time taken to prepare each layer of the lasagna, set to 2 minutes.

2. remainingMinutesInOven Function:
    Calculates the remaining time the lasagna needs to stay in the oven based on the actual minutes it has been cooking.
    The function takes actualMinutesInOven as a parameter, subtracts it from the expected oven time, and returns the remaining minutes.

3. preparationTimeInMinutes Function:
    Computes the total time spent on preparing the lasagna based on the number of layers added.
    The function takes numberOfLayers as a parameter, multiplies it by the preparation time per layer constant, and returns the total preparation time.

4. totalTimeInMinutes Function:
    Calculates the total time spent on cooking the lasagna, including preparation and time in the oven.
    The function takes numberOfLayers and actualMinutesInOven as parameters.
    It calls preparationTimeInMinutes to get the preparation time and adds it to the actual minutes the lasagna has been in the oven.
    The total time is then returned.

 Code:

export const EXPECTED_MINUTES_IN_OVEN = 40;
const PREPARATION_MINUTE_PER_LAYER = 2;

export function remainingMinutesInOven(actualMinutesInOven) {
  return EXPECTED_MINUTES_IN_OVEN - actualMinutesInOven;
}

export function preparationTimeInMinutes(numberOfLayers) {
  return numberOfLayers * PREPARATION_MINUTE_PER_LAYER;
}

export function totalTimeInMinutes(numberOfLayers, actualMinutesInOven) {
  return preparationTimeInMinutes(numberOfLayers) + actualMinutesInOven;
}
