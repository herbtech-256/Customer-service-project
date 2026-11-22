# Customer Service Project

AI camera table tracking for Bucke Café. A camera (or a recorded video) watches the tables, and the app shows:

- which tables are **free**, **seated**, **waiting for a waiter** or **need cleaning**
- a timer for each table, and an alert when guests wait too long for a waiter
- which table will probably free up next
- a daily report: guests per hour, busiest hour, average time at a table
- a **Manager** view with saved visits over days and weeks

The AI runs in the browser on the phone or computer itself. No video is uploaded anywhere.

## How to use

1. Open the page and choose **My video**.
2. Tap **Load video** and pick a recording of your tables, filmed from a high spot with the phone held still.
3. Tap **Add table** and tap the 4 corners around each table and its chairs.
4. Watch the tables change colour as people sit down and leave.

**Demo café** shows a simulated café, so you can see every feature without a video.

## Files

| File | What it is |
|---|---|
| `index.html` | The whole app: layout, styles and code |
| `model/centernet.json` | The AI model's structure |
| `model/centernet.wasm` | The AI model's weights (a binary file, renamed so it uploads easily) |

## Features that only work on claude.ai

Two features use services that exist only when the page is opened on claude.ai. On GitHub Pages they switch themselves off:

- **Double-check with Claude** (the button is hidden)
- **Saving visits for the Manager view.** The Manager tab still works with **Show example data**.

## Credits

- Person detection model: CenterNet with a MobileNetV3 backbone, in TensorFlow.js format, from the [`vladmandic/human`](https://github.com/vladmandic/human) project (MIT License).
- [TensorFlow.js](https://www.tensorflow.org/js) (Apache License 2.0), loaded from cdnjs.
