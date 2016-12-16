# MacZcashMiner
CPU ZEC miner for OS X


This repository contains a ZEC (Zcash) miner for OS X. It employs the Xenoncat CPU algorithm.

## Run Instructions

### Startup Procedure

Open Terminal (Launchpad then typing "terminal" into the search bar is the simplest)

cd to the MacZcashMiner directory

Type ./CocomosMacZcashMiner

### UI vs Automatic Startup

#### UI

This program has a first of its kind user input. Currently, the user input is within the terminal and only appears if the configure.txt file is inactive (more on that in a second). It is simple to use and looks similar to the following:

       ------------------------------- Main Menu -------------------------------
   
            r:  Run program with current settings
            p:  Enter pool address (e.g. us1-zcash.flypool.org:3333)
            w:  Enter wallet address (e.g. t1cPPbXL3vABfTQ7GAUQSSUzUPLHQrZn59w)
            n:  Enter your worker name
		    t:  Enter the number of CPU threads to operate
	    print:  Print current settings
            d:  Reset all values to default
       * or q:  Quit program
   
And no, the print option does not physically print a copy, it just displays the current settings in your terminal.

You simply type the command given on the left corresponding to what it does on the right. It will then ask you for your input. Type r to run the program.

#### Automatic Startup

Within the repository is a provided configure.txt. You may add to this textfile the corresponding inputs. The program will read if the file is present and active and bypass the interactive input. A sample configure.txt file may be:

	$active 1 # 1 = active, 0 = inactive
	$pool us1-zcash.flypool.org:3333
	$wallet YourTransparentAddressHere
	$worker YourWorkerNameHere
	

