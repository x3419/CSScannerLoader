This is a powershell wrapper for  Apr4h's CobaltStrikeScan (https://github.com/Apr4h/CobaltStrikeScan). 

The purpose is to identify the injected process(es) and parse beacon's config in memory. 

Compatible with .NET 4.6


Currently the following files will be written to C:\Users\<username>\AppData\Local\Temp\Costura\\<random>\\<random>\ upon execution:

getinjectedthreads.dll

commandline.dll

cobaltstrikeconfigparser.dll


These dependencies have been made "portable" using Costura and I plan to add code to ensure the files are cleaned up upon exit. 