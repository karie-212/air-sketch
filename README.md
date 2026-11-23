<div align="center">

# air-sketch

**Draw in the air with hand gestures - track 21 landmarks via webcam**

![Python](https://img.shields.io/badge/Python-3.8+-3776AB?style=flat&logo=python&logoColor=white)
![OpenCV](https://img.shields.io/badge/OpenCV-4.x-5C3EE8?style=flat&logo=opencv&logoColor=white)
![MediaPipe](https://img.shields.io/badge/MediaPipe-Latest-FF6F00?style=flat&logo=google&logoColor=white)
![License](https://img.shields.io/badge/License-MIT-yellow?style=flat)
![Status](https://img.shields.io/badge/Status-Active-brightgreen?style=flat)

</div>

---

## Introduction

**air-sketch** is a real-time drawing app that lets you paint in the air with your fingers through a webcam.
MediaPipe detects **21 hand landmarks**, OpenCV renders the live frame and the brush strokes. Point your index finger to draw, add the middle finger to erase, close your hand to pause.

## Demo

<div align="center">
<img width="480" height="272" alt="demo_handraw" src="https://github.com/user-attachments/assets/e05a4ea2-47a0-4ff3-98c5-06e40ab77bcf" />
</div>

## Project Structure

```
HANDRAW/
├── camera/
│   ├── captures/              # Screenshots saved here when pressing S
│   ├── drawing.py             # Drawing, erasing, color switching, HUD
│   └── hand_landmarker.task   # Pre-trained MediaPipe model
├── cam_draw.py                # Entry point
└── README.md
```

## Install

```bash
pip install opencv-python opencv-contrib-python mediapipe numpy
```

## How to run

```bash
python cam_draw.py
```

## Controls

### Hand gestures

| Gesture | Action |
|---|---|
| Index finger up | Draw |
| Index + middle finger up | Erase |
| Closed hand | Idle |

### Keyboard

| Key | Action |
|---|---|
| `1` - `9` | Switch color (green, blue, pink, orange, white, ...) |
| `+` / `-` | Increase / decrease brush size |
| `C` | Clear board |
| `S` | Save screenshot to `captures/` |
| `Tab` | Toggle HUD |
| `Q` / `Esc` | Quit |

## Hand Landmarks

MediaPipe detects **21 landmarks** on each hand, numbered 0 to 20:

<div align="center">
<img src="https://editor.analyticsvidhya.com/uploads/25204hand_landmarks.png" width="420" />
</div>

| Group | Landmarks | Description |
|---|---|---|
| Wrist | 0 | WRIST |
| Thumb | 1-4 | CMC - MCP - IP - TIP |
| Index finger | 5-8 | MCP - PIP - DIP - TIP |
| Middle finger | 9-12 | MCP - PIP - DIP - TIP |
| Ring finger | 13-16 | MCP - PIP - DIP - TIP |
| Pinky | 17-20 | MCP - PIP - DIP - TIP |

> Each finger has 4 points: base knuckle (MCP), middle knuckle (PIP), upper knuckle (DIP), and fingertip (TIP).

## Credits

- [MediaPipe](https://mediapipe.dev) - Google
- [OpenCV](https://opencv.org) - OpenCV.org (open-source community)

---

## About me

I'm **Tran Thai Kiet** (Karie), a 3rd-year Computer Science student at Dong Thap University, Vietnam.

Contact: [GitHub](https://github.com/karie-212) · [LinkedIn](https://www.linkedin.com/in/tranthaikiet) · [Facebook](https://www.facebook.com/tr.th.kiet) · [TikTok](https://www.tiktok.com/@kariebel)
