# Hotel Effectiveness Night Audit Entry Reporter

Minimal script that automates the room count sorted by room type for Housekeeping Gameday in Hotel Effectiveness

## Background Info

WILL ONLY WORK WITH EXCEL FILES FROM INFOR HMS. Download the excel file directly from Housekeeping Assignment page. Will need to filter out unassigned rooms.\
Error handeling is not implemented yet. Selecting wrong file type or certain changes will cause script to end abruptly

Future Implementation:\
Error Handeling\
Initialization of room types/points instead of manually changing code to fit per property.\
Streamline building of script\
Create more visual pleasing GUI\
Automatically input into Hotel Effectiveness

## Dependecies

Packages:

[Pandas](https://pandas.pydata.org/)\
[numpy](https://numpy.org/)

Use package mangaer [pip](https://pip.pypa.io/en/stable/)

```bash
pip install Pandas
pip install numpy
```

## Usage

This version is set to a specific hotel.

To change room type change global variables on HKRECON.py

```python
kings = ['Room types here']
queens = ['Room types here']
suitesK = ['Room types here']
SuitesS = ['Room types here']
suitesQ = ['Room types here']
```

To change points/credits\
Lines 70-114

```python
if points == credit_values_here
```

## Create Executable File

After changing the room types and points, use [pyinstaller](https://pypi.org/project/pyinstaller/) or [auto_py_to_exe](https://pypi.org/project/auto-py-to-exe/) to create executable

```bash
pip install pyinstaller
pip install auto_py_to_exe
```
Using pyinstaller use the following command
```bash
pyinstaller --noconfirm --onefile --windowed  "'PATH TO FOLDER'\gui.py"
```

Using auto_py_to_exe run the following command to start
```bash
auto_py_to_exe
```
This will bring up a GUI for pyinstaller.\
Select the script gui.py and select One File, Window Based

![Alt text](/img/auto_py_to_exe.PNG) 

Convert the script to executable and the exe file should move to "C:\User\YOUR NAME\output"