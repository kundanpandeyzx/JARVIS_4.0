# JARVIS_4.0
Hand Gesture Recognition for Controlling Computer's Mouse Cursor
---

This is a Python project for controlling a computer's mouse cursor using hand gestures. The program utilizes a webcam to recognize hand gestures via the **Mediapipe** library and controls the mouse cursor through the **PyAutoGUI** library.

## Project Structure

- **`app.py`**: Contains the main program logic.  
- **`controller.py`**: Handles mouse cursor movement and click events.  
- **`requirements.txt`**: Lists the required libraries for the project.

---

## Requirements

To run the program, the following libraries are needed:

- **OpenCV**
- **Mediapipe**
- **PyAutoGUI**

You can install these libraries using pip:

```bash
pip install opencv-python mediapipe pyautogui
```

Alternatively, use the `requirements.txt` file to install all dependencies at once:

```bash
pip install -r requirements.txt
```

---

## How to Run

1. Ensure you have Python installed and a webcam connected.
2. Install the required libraries (see the **Requirements** section).
3. Run the `app.py` file:

   ```bash
   python app.py
   ```

Once the program starts, it will capture video from the webcam, allowing you to control the mouse cursor using the following hand gestures:

### Hand Gestures and Actions

| **Gesture**               | **Action**                                                                 |
|---------------------------|-----------------------------------------------------------------------------|
| **All fingers raised**     | Move the cursor by moving your hand.                                       |
| **Thumb closed, others raised** | Freeze the cursor to prevent movement.                                   |
| **Fist**                   | Drag and drop objects.                                                    |
| **Index finger raised**    | Right-click.                                                              |
| **Middle finger raised**   | Left-click.                                                               |
| **Index and middle raised**| Double-click.                                                             |
| **Index and middle (move closer)** | Scroll up.                                                         |
| **Index and middle (move apart)** | Scroll down.                                                       |
| **Pinch (thumb & index)**  | Zoom in.                                                                  |
| **Spread (thumb & index)** | Zoom out.                                                                 |

---

## Demo

The repository includes demo GIFs demonstrating how to use hand gestures to control the mouse. To view them, navigate to the `demo/` folder and open the files using any image viewer.

---

## How It Works

The program uses the **Mediapipe** library to detect hand landmarks from the video stream captured by the webcam. The logic for mapping these landmarks to mouse actions, such as movement and clicking, is implemented in `controller.py`.

---

## Limitations

- Currently, the program supports controlling only a single mouse cursor.  
- Performance may degrade in low-light conditions.  
- Multi-hand gesture support is not implemented yet but could be added in future updates.
