## Conda

### New Env:
conda create -n [supertramp] --clone="/opt/anaconda"

conda create -n [supertramp] python=3.5 anaconda

#### Back to op/anaconda/bin
source activate [supertramp]

conda deactivate

### Remove Env:

conda env remove --name myenv

--------------------------------------------------------------
## Terminal 
### print in terminal and save
python scripts.py [other comm] 2>%1 | tee record.log

### screen
screen -r [session id] 
screen -d
screen -a 
screen -S [session id] -X quit

### Ubuntu Version
 lsb_release -a
 
### zip 
#### zip a file
zip myfile.zip filename.txt

#### zip a folder
zip -r filename.zip folder

### remove 
#### remove a file
rm file.name

#### remove an empty folder
rm -d dirname

#### remove a non-empty folder
rm -r dirname

-------------------------------------------------------------

### available space
du -d1 -h /home/hatchin| sort -h

## memory usage
du -sh /path/to/folder

df -h
