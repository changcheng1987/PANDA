#PANDA & PANDA-view

##What are they?
PANDA is a novel and comprehensive software package for quantitative proteomics data analysis which is developed based on our solid foundations in quantitative proteomics for years. Additionally, PANDA provides user-friendly interfaces for parameter setting, quantification analysis and data visualization (PANDA-view). The core of PANDA was written in standard C++ language on the platform of Microsoft Visual Studio ultimate 2013 in Windows System. And the interfaces of PANDA was implemented in C# on the same platform.

As an affiliated tool of PANDA, PANDA-view is developed for statistical analysis and data visualization. The core of PANDA-view was written in Qt C++ language on the platform of Microsoft Visual Studio ultimate 2013 in Windows System.
  
##The release version

###version v1.0.1 (8/31/2016)
* PANDA v1.0.1 is able to be used in Windows XP and Windows Server 2003&2008. The required minimum version of .NET Framework is changed from v4.5 to v4.0.
* PANDA-view v1.0.1 fixed a bug when ploting the multiple XICs for precursor-labeled data.

###version v1.0.0 (8/1/2016)
The first release version of PANDA and PANDA-view.

## Hardware requirements
- Intel Pentium III/800 MHz or higher (or compatible) although one should probably not go below a dual core processor.
- 2 GB RAM minimum.
##Software requirements
Windows is currently the only operating system supported. Supported versions are

- Windows Vista SP2 (x86 and x64)
- Windows 7 SP1 (x86 and x64)
- Windows 8
- Windows 10
- Windows Server 2008 R2 SP1 (x64)
- Windows Server 2008 SP2 (x86 and x64)
- Windows Server 2012
- .NET Framework 4.0 or higher from Microsoft
- R for Windows （only for PANDA-view）



###Note1: R software can be downloaded from [https://www.r-project.org/](https://www.r-project.org/). Users should also add the directory which includes RScript.exe into the system environment variable. The method for setting system environment variable can be found at [http://www.computerhope.com/issues/ch000549.htm](http://www.computerhope.com/issues/ch000549.htm).
###Note2: The required R packages and their installation commands are listed below:
- install.packages("rgl")
- install.packages("scatterplot3d")
- install.packages("RColorBrewer")
- install.packages("gplots")
- install.packages("survival")
- install.packages("coin")
- install.packages("Rcpp")
- install.packages("lattice")
- source("http://bioconductor.org/biocLite.R")
- biocLite("impute")
- biocLite("splines")
- biocLite("R.methodsS3")
- biocLite("matrixStats")
- biocLite("samr")
##  Installation

Download link: [https://sourceforge.net/projects/panda-tools/](https://sourceforge.net/projects/panda-tools/)  
Please see the file named "User Guide for PANDA and PANDA-view.pdf" (coming soon).

##  Licensing

  Please see the file called "LICENSE.md" and "LICENSE_Chinese.md".

##  Contacts

  For any questions involving PANDA and PANDA-view, please contact Dr. Cheng Chang (Email: 1987ccpacer@163.com or 1987ccpacer@gmail.com).

## Copyright

This software product is developed by the National Center for Protein Sciences (Beijing)-Bioinformatics group. All title and intellectual property rights, which is generated by the software product (including, but not limited to the software products, including any relative images, data, texts and additional programs (dll, exe, etc.)), incidental help materials, and any copies of the Software Products is protected by the copyright laws in People's Republic of China and international copyright treaties and other intellectual property laws and treaties. Users only get the right to use this software product.