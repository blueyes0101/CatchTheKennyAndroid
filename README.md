# Catch The Kenny Game

This is a simple Android game called "Catch the Kenny," where the user must tap on a randomly appearing image of "Kenny" (or any character) to increase their score. The game runs on a timer, and the player has a limited time to catch as many "Kenny" images as possible before the timer runs out.

## Features
- A 15-second countdown timer.
- Randomly appearing images that the user must tap to score points.
- A running score display that updates every time the user catches "Kenny."
- **EdgeToEdge** and **WindowInsetsCompat** for immersive UI.

## Technologies Used
- **Android Studio**
- **Java**
- **Handler** and **Runnable** to manage the random image display.
- **CountDownTimer** for the game timer.
- **Random** for randomizing image positions.

## Code Overview

### Main Components
1. **MainActivity**:
   - Initializes a 15-second countdown timer that updates the **TextView** every second.
   - Manages an array of **ImageView** elements representing different positions where the "Kenny" image can appear.
   - The **hideImages()** method uses a **Handler** and **Runnable** to make the images randomly appear and disappear at a fixed interval (500ms).
   - The **increaseScore(View view)** method increments the score every time the user taps on the visible image.

2. **Image Handling**:
   - There are 12 image slots, and one randomly selected image becomes visible at any given time, encouraging the user to tap quickly.

### Methods
- **increaseScore(View view)**: Increases the score each time the user taps on the visible "Kenny" image.
- **hideImages()**: Uses a **Runnable** and **Handler** to randomly display and hide images every 500ms.
- **CountDownTimer**: Handles the 15-second game timer.

### Layout
- A **TextView** to display the remaining time.
- A **TextView** to display the user's score.
- 12 **ImageView** elements, one of which displays the "Kenny" image at a time.

## Getting Started

### Prerequisites
To run this project, you need:
- Android Studio installed on your computer.
- Basic knowledge of Kotlin/Java and Android development.

### Installation

1. Clone the repository:
    ```bash
    git clone https://github.com/blueyes0101/CatchTheKennyAndroid.git
    ```

2. Open the project in Android Studio.

3. Build and run the project on an emulator or physical device.

## Usage

1. When the game starts, a 15-second countdown begins.
2. Tap on the visible "Kenny" image as it appears to increase your score.
3. The game ends when the timer reaches zero, and your final score is displayed.

## Contributing
Feel free to contribute by opening issues or submitting pull requests.

## License
This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.
