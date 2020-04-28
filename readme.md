# A Simple Application To View Apache's error.log file

![Log Viewer - Main Window](https://nshiell.com/img/blue-log-viewer/product-ubuntu-v1-2-0.png)

*This program is not related to Apache or the Apache Software Foundation in any way*

## To Run on GNU/Linux:
`./blue-log-viewer.py /var/log/apache2/error.log`

#### If you see something resembling the following:
```
Traceback (most recent call last):
  File "./blue-log-viewer.py", line 3, in <module>
    from PyQt5.QtWidgets import QApplication
ModuleNotFoundError: No module named 'PyQt5'
```

##### then on Debian / Ubuntu / XUbuntu / Kubuntu / KDE Neon run:
`sudo apt-get install python3-pyqt5`

##### or on Fedora (Redhat RPM based) use pip3 instead:
```sudo pip3 install pyqt5```


...then try again.

_______________________________________________________

## To Run on Mac OSX:
![Log Viewer - Main Window](https://nshiell.com/img/blue-log-viewer/product-osx-v1-2-0.png)
I use https://brew.sh/ to get it to install - you can try pip3 etc

`python3.7 blue-log-viewer.py`

#### If you see something resembling the following:
```
Traceback (most recent call last):
  File "./blue-log-viewer.py", line 3, in <module>
    from PyQt5.QtWidgets import QApplication
ModuleNotFoundError: No module named 'PyQt5'
```
##### Then run
```brew install pyqt5```

...then try again.


_______________________________________________________

## To test
This application has some Selenium style functional tests.
You can see them by looking in `/features/runs.py` and looking at the [Cucumber](https://cucumber.io/docs/gherkin/reference/) in the comments.

They use Python's native [testing](https://docs.python.org/3/library/unittest.html) as a test harness for running these tests.

To run them do the following:

  1. Edit /blue-log-viewer.py, find the line `if False` and flip it to true to enable testing (make sure you turn it back to false for production).

  2. Make sure localhost port **8032** is available

  3. run `python3 features/runs.py`
