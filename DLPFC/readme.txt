Version fom Dec. 5th 2017
go it from Emily 
Dave wrote most of it?!?

///it uses 12345 as input parameters

(“LetterOrderTask_d5.py”) is for the DLPFC task

The files BasicPromptTools.py and LetterOrderPrompts_5button.txt need to be in a subfolder called “Prompts” (of the directory you run the .py script from).
 
There are two parameter files: one to do the 6 min functional localizer of 10 s ON, 10 s OFF (“LetterOrder_6mLOC.pickle”) and one to do the full experimental run (“LetterOrder_20trialRUN.pickle”).
 
The script will give you the option to load one of these existing parameter files at the start of each run. The only thing you should need to modify prior to running are lines 29 and 33:
 
Line 29:
True if doing localizer, False otherwise
 
Line 33:
alphaVsRemem = True # this means the script will do 10 REMEM trials and 10 ALPHA trials, with all being GO (output) trials
alphaVsRemem = False # this means the script will do 10 go (output) trials and 10 no-go (no output) trials, with all being ALPHA trials
 
For the 20 trial RUN, each trial is 32s long as we discussed, and there is an 8-sec warm up at the beginning and 8-sec cool down at the end, so the total run length is 656 s, or 10m56s.
 