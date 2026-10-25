From Broadcast to Bench: Real-Time Volleyball Coaching Tool Through Computer Vision and Machine Learning

Commercial volleyball analytics systems need multiple calibrated cameras and cost an estimated $8,500 to $15,600 CAD. This project shows that a laptop, a Roboflow account, and one existing camera can provide near real-time analytics instead.

What it does

Detects players, the ball, and the court, and classifies serves, attacks, blocks, passes, and sets.
Feeds the detections into a live dashboard with team KPIs, heatmaps on a 9-zone court grid, and action counts.

How it was built

Labelled 19,000+ frames from TRU Women’s Volleyball matches (7,502 for player tracking and 11,607 for action classification).
Trained and compared 8 models across YOLOv11, YOLO-NAS, RF-DETR, and Roboflow 3.0, using a 70:20:10 split grouped by rally clip to avoid data leakage.
Chose the final models based on compatibility with continuous video, not accuracy alone.

Results

Player tracking: 90.0% mAP@0.50, 95.1% precision, 90.9% recall.
Action classification: 86.4% mAP@0.50, 84.3% precision, 86.1% recall.

Limitations and next steps

Pass and Set are confused because of near-identical body positions from one camera angle, and ball detection misses some frames. Planned work includes pose estimation, a short temporal window, and outcome tracking.

Tools: Python, JavaScript, Roboflow, REST APIs

Demo uses sample data. Real match footage and player data are not included.
