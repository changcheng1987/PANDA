#PANDA & PANDA-view
[![DOI](https://zenodo.org/badge/66350175.svg)](https://zenodo.org/badge/latestdoi/66350175)
##What are they?
PANDA is a novel and comprehensive software package for quantitative proteomics data analysis which is developed based on our solid foundations in quantitative proteomics for years. Additionally, PANDA provides user-friendly interfaces for parameter setting, quantification analysis and data visualization (PANDA-view). The core of PANDA was written in standard C++ language on the platform of Microsoft Visual Studio ultimate 2013 in Windows System. And the interfaces of PANDA was implemented in C# on the same platform.

As an affiliated tool of PANDA, PANDA-view is developed for statistical analysis and data visualization. The core of PANDA-view was written in Qt C++ language on the platform of Microsoft Visual Studio ultimate 2013 in Windows System.
  
##The release version
### PANDA version v1.1.2 (8/22/2017)
* Bugs about merging multiple samples in label-free are corrected.
* The development environment is changed from VS2013 to VS2017. So users need to install [Microsoft Visual C++ Redistributable for Visual Studio 2017](https://www.visualstudio.com/zh-hans/downloads/) first before using PANDA. 

### PANDA version v1.1.1 (1/13/2017)
* Bugs about the parallel mode and the XML output function are corrected.
* Print the ModifiedSeq (ReadableMod) of peptide in PepList files.

###PANDA version v1.1.0 (10/15/2016) 

> **Important improvement**

* Updates of the GUI, including the 
* Release the x64 version which is able to handle large-scale MS data. The x64 version of PANDA is recommended.


### PANDA version v1.0.2 (9/13/2016)
PANDA v1.0.2 contains some updates in the GUI:

* max thread number is auto set according to the core number of user's computer.
* max cached file number is set as "sample num*replicate num".

###PANDA & PANDA-view version v1.0.1 (8/31/2016)
* PANDA v1.0.1 is able to be used in Windows XP and Windows Server 2003&2008. The required minimum version of .NET Framework is changed from v4.5 to v4.0.
* PANDA-view v1.0.1 fixed a bug when ploting the multiple XICs for precursor-labeled data.

###PANDA & PANDA-view version v1.0.0 (8/1/2016)
The first release version of PANDA and PANDA-view.

## Hardware requirements
- Intel Pentium III/800 MHz or higher (or compatible) although one should probably not go below a dual core processor.
- 2 GB RAM minimum.
##Software requirements

### Microsoft Visual C++ Redistributable for Visual Studio 2017 is required since v1.1.2
* [Download link](https://go.microsoft.com/fwlink/?LinkId=746572) for x64
* [Download link](https://go.microsoft.com/fwlink/?LinkId=746571) for x86
###Windows is currently the only operating system supported. Supported versions are

- Windows Vista SP2 (x86 and x64)
- Windows 7 SP1 (x86 and x64)
- Windows 8
- Windows 10
- Windows Server 2008 R2 SP1 (x64)
- Windows Server 2008 SP2 (x86 and x64)
- Windows Server 2012
- .NET Framework 4.0 or higher from Microsoft
- R for Windows **（only for PANDA-view）**



###Note1
R software can be downloaded from [https://www.r-project.org/](https://www.r-project.org/). Users should also add the directory which includes RScript.exe into the system environment variable. The method for setting system environment variable can be found at [http://www.computerhope.com/issues/ch000549.htm](http://www.computerhope.com/issues/ch000549.htm).
###Note2
The required R packages and their installation commands are listed below:

    install.packages("rgl")
    install.packages("scatterplot3d")
    install.packages("RColorBrewer")
    install.packages("gplots")
    install.packages("survival")
    install.packages("coin")
    install.packages("Rcpp")
    install.packages("lattice")
    source("http://bioconductor.org/biocLite.R")
    biocLite("impute")
    biocLite("splines")
    biocLite("R.methodsS3")
    biocLite("matrixStats")
    biocLite("samr")

##Installation

Download link: [https://sourceforge.net/projects/panda-tools/](https://sourceforge.net/projects/panda-tools/)
 
Please see the file named "User Guide for PANDA and PANDA-view.pdf" (coming soon).

##  Licensing

  Please see the file called "LICENSE_English.pdf" or "LICENSE_Chinese.pdf".

##  Contacts

  For any questions involving PANDA and PANDA-view, please contact [Dr. Cheng Chang](https://www.linkedin.com/in/cheng-chang-5263b439 "LinkedIn") (Email: [1987ccpacer@163.com](mailto:1987ccpacer@163.com) or [1987ccpacer@gmail.com](mailto:1987ccpacer@gmail.com)).

## Copyright

This software product is developed by the National Center for Protein Sciences (Beijing)-Bioinformatics group. All title and intellectual property rights, which is generated by the software product (including, but not limited to the software products, including any relative images, data, texts and additional programs (dll, exe, etc.)), incidental help materials, and any copies of the Software Products is protected by the copyright laws in People's Republic of China and international copyright treaties and other intellectual property laws and treaties. Users only get the right to use this software product.