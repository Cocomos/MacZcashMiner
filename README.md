# MacZcashMiner
ZEC miner for OS X for pools


This repository contains a ZEC (Zcash) miner for OS X. The CPU miner employs the Xenoncat algorithm, the GPU miner is currently in testing (use at your own risk) and is only for AMD cards. The GPU miner uses fast silentarmy kernels. This is for pools.

If you are testing the soft release of the AMD miner, please read the GPUMinerReleases/WARNING.md file before doing so. I am not responsible for any damages. It's not so much the program may harm the computer, but false measures you take to fix possible errors are what's more likely to cause harm! Just covering my booty if your computer breaks. Rule of thumb, don't be a dummy and start changing important header files and such.

### Current Works in Progress
- Pure OpenCL miner

NOTE: CUDA support scrapped! Since all Macs have their CPUs and GPUs support some version of OpenCL, the project has now been changed to an all OpenCL project. This way, any Mac owner will be able to mine on their CPU and GPU. That means all GPUs will be supported, including AMD, NVIDIA, and Intel HD Graphics! Both the CPU and GPU miners here will no longer be updated (maybe once more as I have made some improvements).

## Run Instructions

### Neccessary Packages

There are a few packages that are required before you are able to run it. Really BOOST is all that is required so if you already have that then you can skip down to the Startup Procedure to start mining. If you don't have the boost library, the following procedure will install it (with a few other things as well). The order is install brew, install python, install boost, mine Zcash!

	ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)" #installs brew
	brew update #optional
	brew install python #not needed if python already
	brew install boost --with-python

### Startup Procedure

Open Terminal (Launchpad then typing "terminal" into the search bar is the simplest)

cd to the MacZcashMiner directory

Type

	./CocomosMacZcashMiner

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
	$threads NumberOfCpuThreadsYouWouldLikeToMineOnGetEnteredHere
	
## Supported Versions

As I do not have any great resources, I can only test on what I have. So at this time I only know that it runs on OS X Sierra 10.12.2. That does not mean that it cannot run on other versions, nor does that mean it will never run on any other version. I ask the public to check their OS version, attempt to run the program, and report errors/successes. This repository will be updated as time goes. Below is the list of known working versions.

### OS X Sierra
	10.12.2
	
### OS X El Capitan
	10.11.6

## Donations

Donations option lifted in version 1.2 of CPU and GPU miners.

## Acknowledgements

Much of this code at this time was adapted from existing freesource software, so I must give my thanks to the following:

	Zcash official and unofficial devolopers
	Xenoncat and the freesource CPU algorithm used here
	NiceHash and their freesource nheqminer to which I based my output and organization off of substantially
	Silentarmy and their freesource software as I have applied their fast kernels
	Those individuals on mining forums asking for viable OS X Zcash miner
	
