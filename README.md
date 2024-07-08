![Снимок экрана 2024-07-08 в 19 46 14](https://github.com/KristinaKolesnyk/SecurityAndroid_HW2/assets/126165994/ee75a73c-8472-46c6-a79f-068473688fc8)
# README

## Description

This project focuses on reverse engineering an APK to understand and tweak the game mechanics. The goal is to enable the game to run correctly based on the user’s ID, leading the user through a sequence of directional arrow presses to "survive" and reach a designated city.

### Game Mechanics

1. **Processing the ID:**
   - Each digit of the user's ID is converted using modulo 4 (`digit % 4`) and stored in an array.
   - The 8th digit of the ID is used to fetch the state from an array of states obtained from a server.

2. **Gameplay:**
   - The game screen features four directional buttons: up, right, down, and left.
   - Each button corresponds to an integer value:
     - Left = 0
     - Right = 1
     - Up = 2
     - Down = 3
   - The player must press the arrows in the correct order derived from their ID. Incorrect presses will result in a failure message.

### Example

- **ID:** 789654321
- **Sequence:** [3, 0, 1, 2, 1, 0, 3, 2, 1]
  - Down, Left, Right, Up, Right, Left, Down, Up, Right

## Development Process

1. **Initial Setup:**
   - Decompile the APK to extract the necessary resources and code.
   - Create a new Android project and import the extracted files.

2. **Configuration:**
   - Update the manifest file to match the project’s requirements.
   - Ensure the app has INTERNET permission.

3. **Code Modifications:**
   - Correct any bugs in the code (e.g., update URL).

4. **Testing:**
   - Enter your ID and follow the correct sequence of arrow presses.
   - Confirm the toast message displays the correct city name and survival message.

