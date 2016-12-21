# WARNING

Use this program at your own risk! This is an alpha soft release. I am not responsible for any damages to your computer.

As this is currently in testing, there are a few known issues.

*Bane Voice* Since I have a current "working" version I offer it to you, the people.

This currently only has AMD OpenCL support. NVIDIA CUDA support will come in a later version after all fixes are made in this version. So obviously, you should not run this program if you do not have an AMD card in your Macintosh. How do you check what graphics you have? Simply click on the little apple in the top left of your computer screen and then click on About This Mac. There will be a line that says Graphics in bold and next to it will have your hardware. If it says anything other than AMD or Radeon then you should not run this program. If it says something like Intel Graphics or GTX or NVIDIA, do not run this program (it won't harm your computer, it is just a pain to deal with as it is likely to slow down your computer tremendously, plus it just won't hash).

Keep in mind even, if you do have an AMD card it is likely to slow down your computer because most Macs have only one graphics card with the exception of some Mac Pros which have 2 AMD graphics modules installed. I plan on releasing a version in which you can modify the amount of GPU you would like to use for the miner. But for now, I just need to know if it works globally!

If you know how to kill a processes from the Terminal then you should be okay for testing.

## Common problems

### clEnqueueNDRangeKernel (-4) error:

This error can occur for two known reasons - 1) not enough memory, 2) no AMD card!

### segmentation fault:

This error has two known reasons - 1) not enough memory, 2) you are missing the necessary silentarmy kernels

### laggy computer:

It is likely you killed the program before the program can kill the miner. Kill the process from Terminal. You can find the process by using top, then kill $pid#.
