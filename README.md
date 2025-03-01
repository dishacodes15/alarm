# Python Alarm with GUI using Tkinter

This is a simple alarm clock application built using Python and the Tkinter library. It allows users to set an alarm time, and when the alarm triggers, it plays a sound to notify the user.

## Features

* Set alarm time with hours, minutes, and seconds.
* Uses threading to run the alarm check in the background.
* Plays a sound when the alarm time is reached.
* Simple and easy-to-use graphical user interface (GUI).

## Requirements

* Python 3.11.9
* Tkinter (usually included with Python)
* playsound library (`pip install playsound`)

## How to Use

1. **Clone the repository:** `git clone https://github.com/your-username/alarm-clock-tkinter.git`
2. **Install playsound:** `pip install playsound`
3. **Replace the sound file:** Replace `C:\Users\VSCODE\python alarm\262436-Telemetry_Tech_Data_22.wav` with the path to your desired sound file.
4. **Run the script:** `python alarm_clock.py`
5. **Set the alarm time:** Use the dropdown menus to select the desired hour, minute, and second.
6. **Click "Set Alarm":** The alarm will be activated and will trigger at the specified time.

## Logic

The alarm clock works by continuously comparing the current time with the set alarm time in a separate thread. Here's a breakdown of the logic:

1. **Get Alarm Time:** The alarm time is obtained from the hour, minute, and second values selected by the user in the GUI.
2. **Threading:** A new thread is created to run the alarm check in the background. This prevents the GUI from freezing while the alarm is waiting to trigger.
3. **Infinite Loop:** The alarm thread enters an infinite loop where it continuously performs the following steps:
   * **Wait:** The thread sleeps for one second.
   * **Get Current Time:** The current time is retrieved using `datetime.datetime.now().strftime("%H:%M:%S")`.
   * **Compare Times:** The current time is compared with the set alarm time.
   * **Trigger Alarm:** If the current time matches the alarm time:
     * A message "Time to Wake up" is printed to the console.
     * The `playsound` function is used to play the specified sound file.

## Contributions

Contributions are welcome! Feel free to open issues or pull requests for bug fixes, feature enhancements, or any other improvements.

## Author

* Disha Madhusudana


