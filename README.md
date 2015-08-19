# DotNET-MVC-Enumerator

##About

This script can be used to enumerate all the endpoints in an .NET MVC application and also list out the HTTP methods suported by them, if any. Additionally, if any security directives are supported by the application, we can search them by passing it as an argument. They will be listed out if they are set at either the class level or the method level itself. 
And yeah, the ouput can be saved in a CSV format if specified.


###Supported Platforms:

 .NET Framework 4.5 

###Installation

Fetch the .sln file and you should be good to go. Build it in Visual Studio supporting .NET version 4.5+.
All the dependencies are in the packages/ directory. 

###Usage

The basic usage of the script is as follows:

    > DotNotMVCEnumerator.exe -h

    Usage: DotNetMVCEnumerator.exe

    [-d Directory To Scan  *Required]

    [-a Attribute Name to Search]

    [-n Attribute Name To Perform Negative Search]

    [-o File Name to Output Results as CSV]

    [-h Display Usage Help Text]
    
It recursively searches for all .cs files from the current directory and attempts to list out the Entry points.If we specify an attribute, it lists out its presence or absence in each method as well.The output by default is presented on the console. However, the results can be obtained in csv format if we specify the name of the output file using the -o flag.

Sample Usage 1 - Scan code within a directory and write output to the ‘results.csv’ file.

    > DotNetMVCEnumerator.exe -d “C:\Code” -o results.csv

Sample Usage 2 - Scan code and only include results of methods containing the ‘CSRFTokenValidate’ attribute filter. The output is written to the console and to the ‘results.csv’ file.

    > DotNetMVCEnumerator.exe -d “C:\Code” -o results.csv -a CSRFTokenValidate


