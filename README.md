This is a powershell wrapper for  Apr4h's CobaltStrikeScan (https://github.com/Apr4h/CobaltStrikeScan). 

The purpose is to identify the injected process(es) and parse beacon's config in memory. 

The program output will be saved in C:\CS\computername_CobaltStrikeMemoryScan.txt

Compatible with .NET 4.6

This tool does not operate 100% in memory. If you look at the execution via ProcMon, you'll see that the following files will be written to C:\Users\username\AppData\Local\Temp\Costura\random\64\ upon execution:

getinjectedthreads.dll

commandline.dll

cobaltstrikeconfigparser.dll

libyara.net.dll


These dependencies have been made "portable" using Costura and I plan to add code to ensure the files are cleaned up upon exit. 
Also this may generate a false positive for Defender's Real Time Protection - I'm assuming this is due to Costura's unpacking.