Open your web browwser and go to python.org and download the latest version of python.
(Currently 3.7.4)

When the installer downloads run it by double clicking on it. 
Be sure to tick the box at the bottom of the setup wizard:
Add Python 3.7 to PATH 
(this allows python to be called easily in a command prompt)

Open a command prompt 
Press Windows key and x and select 'Windows PowerShell'
Type:
python
and then press enter

PS C:\Users\Kevin> python
Python 3.7.4 (tags/v3.7.4:e09359112e, Jul  8 2019, 19:29:22) [MSC v.1916 32 bit (Intel)] on win32
Type "help", "copyright", "credits" or "license" for more information.
>>>


Congratualtions, you've installed and run python.

Lets test python a bit:

a = 3
b = 4
a + b

7

When you're ready we can exit python by typing

exit()

This will return us to the PowerShell prompt

Python comes with a package manager called pip.
You can think of pip as a sort of app store and packages as being much like Matlab toolboxes.
Unlike Matlab these packages are all free.

First lets see if pip is up to date:

python -m pip install --upgrade pip

You'll see some text come up in the PowerShell window and a loading bar as any new version is downloaded.

For example:

Collecting pip
  Downloading https://files.pythonhosted.org/packages/62/ca/94d32a6516ed197a491d17d46595ce58a83cbb2fca280414e57cd86b84dc/pip-19.2.1-py2.py3-none-any.whl (1.4MB)
    100% |████████████████████████████████| 1.4MB 7.9MB/s
Installing collected packages: pip
  Found existing installation: pip 19.0.3
    Uninstalling pip-19.0.3:
      Successfully uninstalled pip-19.0.3
Successfully installed pip-19.2.1

As you can see we've upgraded from pip 19.0.3 to 19.2.1

Next we will install jupyter 

pip install jupyter

You'll see a lot of different packaged being installed as part of the jupyter project.

Next we will install scipy. Scientific Python (scipy for short) is a bundle of packaged that gives python a lot of numerical computing tools much like Matlab.

pip install scipy

Again you'll see a wall of text and loading bars as packages like numpy and are installed.
The package numpy allows us to perfrom numerical calculation in a manner very much like Matlab.
The scipy package allows us to do additional Matlab like things like curvefitting and interpolation.

Next we will install Matplotlib, which, as the name suggests allows us to plot data much like Matlab.

Next lets install a package that lets us view 3D models in our notebooks:

pip install pyGEL3D

We can install any additional python packages directly from our Jupyter notebooks.


Finally for now we need to install FFmpeg, a free open source tool that is used to encode videos in these notebooks.
This is a little more advanced so pay close attention to these steps.

Open your web browser and go to ffmpeg.org and click download and then the link to Windows builds.

I downloaded the statically linked 64bit version 4.1.4 as a zip file to my Downloads folder.
Unzip the ffmpeg-xxxxxxxx-xxxxxxx-win64-static.zip file and copy it somewhere like the root directory of your C:\ drive.
I also renamed the folder to ffmpeg so it won't look cluttered

Press the Windows key + r to open the Run dialog.
Enter SystemPropertiesAdvanced and press enter.
Click on 'Environment Variables...' at the bottom.
Look under system variables in the bottom panel and highlight it by clicking on it.
Then click Edit...
Add 
C:\ffmpeg\bin

to the list. 

You should close and reopen your PowerShell window for this change to take effect.

In order to run our notebooks our command prompt has to be in the right directory.
We use the command cd for this purpose. My notebooks are stored in a folder:

C:\Users\Kevin\UCD\MEEN20010_Jupyter

So to switch the current directory to this one we do the follwing

cd 'C:\Users\Kevin\UCD\MEEN20010_Jupyter'

taking note of the quotations at the start and end of the path. These are impprtant because you might have a space in on of your folder names and the quotation marks tell PowerShell that they are part of the input.

now lets run Jupyter by typing 

jupyter notebook

This will fire up your default web browser and you'll see a bunch of .ipynb files.
These are our Jupyter notebooks! Jupyter is based on the iPython notebook format which explains the name.

If you didn't bother to change directory or you made a mistake you can simply browse to the correct directory using this interface.

Extensions

pip install jupyter_contrib_nbextensions 
jupyter contrib nbextension install 
