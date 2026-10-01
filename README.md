# Diep.io bot

One of my earliest projects, from 2021. It plays [diep.io](https://diep.io) by watching the screen.

The script takes a screenshot and looks for the shapes you farm for points (squares, triangles, pentagons) by matching them against reference images with `pyautogui.locateCenterOnScreen`. When it finds one, it moves the mouse onto it so your tank aims there, and it keeps tracking the same shape for a few frames before looking again. Pentagons get priority over triangles, and triangles over squares, since they're worth more. Pink triangles (the ones that chase you) get flagged first. Hold `p` to stop it.

The code is in `old shape finder (center).txt`. I'd also started on spotting enemy players and bullets, and that part is still in there, commented out.

## Running it

It's Windows-only, because it moves the mouse with `win32api`.

```bash
pip install pyautogui opencv-python keyboard pywin32
```

Rename the file to `.py`. It also needs screenshots of each shape, cropped with the background removed, saved next to the script under the names the code looks for (`Diep.io Pentagon no background.png` and so on). Those images aren't in the repo, so you'll have to take your own at your screen's resolution.
