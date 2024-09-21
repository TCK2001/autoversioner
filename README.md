# versionrunner
## Motivation

After writing a program, it is essential to generate a `requirements.txt` file before distribution, so that other users can easily recreate the deployed program.

However, finding and specifying the versions manually can often be tedious. In such cases, you can use `versionrunner` to quickly convert the library versions into a requirements.txt file and save it automatically.

---

## How to Run ?
```python
from versionrunner import *

search_version(__file__)  # or search_version('your_file_name')
```

## Example
```python
# for database
import sqlite3
from database import init_db

# for dialog
import sys
from PyQt5.QtWidgets import QApplication, QMainWindow, QCalendarWidget, QDialog, QVBoxLayout, QLineEdit, QTimeEdit, QPushButton, QListWidget, QWidget, QMessageBox, QSlider, QLabel, QHBoxLayout
from PyQt5.QtCore import QDate, QTime, QTimer, QUrl, Qt
from PyQt5.QtGui import QIcon
from PyQt5.QtMultimedia import QMediaPlayer, QMediaContent
import yt_dlp

from styles import apply_slider_stylesheet, apply_stylesheet, apply_edit_delete_stylesheet
from event_dialog import EventDialog, URLInputDialog

# import the library
from versionrunner import *

....
....

if __name__ == '__main__':
  ....
  # 
  search_version(__file__)
  ....
```
### Result
requirements.txt
```
PyQt5==5.15.10
versionrunner==0.0.2
sys==3.11.5
yt_dlp==2024.8.6
sqlite3==2.6.0
```
