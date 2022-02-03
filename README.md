# PANDA

## What is it?
PANDA is a novel and comprehensive software package for quantitative proteomics data analysis which is developed based on our solid foundations in quantitative proteomics for years. The advantage algorithms of our previous works, i.e. LFQuant ([Proteomics 2012, 12, (23-24), 3475-84](https://www.ncbi.nlm.nih.gov/pubmed/23081734)) and SILVER ([Bioinformatics 2014, 30, (4), 586-7](https://www.ncbi.nlm.nih.gov/pubmed/24344194)) have been implemented into PANDA. The core of PANDA was written in standard C++ language on the platform of Microsoft Visual Studio ultimate 2017 in Windows System. And the interface of PANDA was implemented in C# on the same platform.
## Cite PANDA and PANDA-view
- PANDA is published in *[Bioinformatics](https://academic.oup.com/bioinformatics/advance-article/doi/10.1093/bioinformatics/bty727/5078468)* on 8/21/2018. 
- [PANDA-view](https://sourceforge.net/projects/panda-view/) is published in *[Bioinformatics](https://academic.oup.com/bioinformatics/advance-article/doi/10.1093/bioinformatics/bty408/5001389)* on 5/22/2018, which is developed for statistical analysis and data visualization as an affiliated tool of PANDA.

>     Chang C, et al. PANDA: A comprehensive and flexible tool for proteomics data quantitative analysis. Bioinformatics 2019, 35, (5), 898-900.
>     Chang C, et al. PANDA-view: An easy-to-use tool for statistical analysis and visualization of quantitative proteomics data. Bioinformatics, 2018, 34, (20), 3594-3596.

## The release version

### PANDA v1.2.3 (2/3/2022)
> **Important improvement**

* Able to read [Byonic](https://proteinmetrics.com/byos/) identificaiton result file ("output.spectra.txt" in "objs\" file folder) for glycopeptide quantification.
* A new kind of output file "Peptides_FX.txt" is generated for each fraction (X is the fraction index). In this file, peptides are distinguished by sequence and modification. While in "PeptideIons_FX.txt", peptides are distinguished by sequence, modification and charge.
* Fix a bug when handling Orbitrap Exploris 480 FAIMS raw data.
 
### PANDA v1.2.2 (1/1/2022)
> **Important improvement**

* Able to handle Orbitrap Exploris 480 FAIMS raw data.
* NOTE: FAIMS raw data should be split into separate raw files according to their compensation voltages (CV) before quantification.
### PANDA v1.2.1 (6/10/2021)
* Fix a bug when reading pFind or pGlyco results for label-free quantification.
* pFindSplit has also been updated to pFindSplit\_release20210610 for reading large pFind search result files.

### PANDA v1.2.0 (7/30/2020)
* Fix a bug when merging multiple fractions for label-free quantification.

### PANDA v1.1.9 (7/22/2020)
* Fix a bug when reading the pFind and pGlyco searching results.

### PANDA v1.1.8 (6/2/2020)
* Modify the default peptide length cutoff from 7 to 6 for labeled quantification. When reading input peptide lists, the default peptide length should be >=6 for both labeled and label-free quantifications.
* Fix a bug when reading peptides with many proteins (e.g. when searching a UniProt TrEMBL database, a peptide can be mapped to >300 proteins).

### PANDA v1.1.7 (5/13/2020)
* Since v1.1.5, PANDA supports to read the search result files of [pFind3](http://pfind.ict.ac.cn/software/pFind3/index.html) and [pGlyco2](http://pfind.ict.ac.cn/software/pGlyco/index.html). The tool [pFindSplit](https://sourceforge.net/projects/panda-tools/files/) has been released to split the merged result files of pFind3 and pGlyco2 before running PANDA.
* Two versions of pFildSplit are provided:
* (1) pFindSplit\_release20200611 only splits the input file without filtering. Both versions of x64 and x86 are provided. **To process a large input file (>2GB), please use the x64 version of pFindSplit.**
* (2) pFindSplit\_release20200519 splits the input file and output the valid PSMs using some QC parameters: q-value<=0.01, peptide length>=6, target. Moreover, for pGlyco, there is one additional QC parameter: only PSMs with rank 1 are printed.
* The usage of pFindSplit is listed below.
>     pFindSplit.exe InputFile OutputFolder
>     InputFile: *.spectra, *.protein for pFind3 or *.txt for pGlyco2
>     OutputFolder: if the folder does not exist, it will be created automatically. 
>     Example: pFindSplit.exe c:\tmp\test.protein d:\output

* The [PSI-MS-CV](https://github.com/HUPO-PSI/psi-ms-CV) has been updated to v4.1.30 (8/30/2019). Thus, PANDA supports the latest format of mzIdentML extracted from Mascot (v2.7) and the other search engines.

### PANDA v1.1.6 (9/19/2019) (beta version)
* PANDA supports to read the search result files of [pFind3](http://pfind.ict.ac.cn/software/pFind3/index.html). This is a beta version for further test. PANDA can read two types of search results of pFind3:

    &ensp;**(1) pFind.protein**. PANDA will read the results from "pFind.protein" with protein FDR<1% by default. Users can change this threshold by setting the parameter "Peptide FDR" in the GUI of PANDA.

    &ensp;**(2) pFind-Filtered.spectra**. PANDA will read the results from "pFind-Filtered.spectra" with peptide FDR<1% by default. Users can change this threshold by setting the parameter "Peptide FDR" in the GUI of PANDA.

* PANDA supports to do glycopeptide quantification by reading the result file of [pGlyco2](http://pfind.ict.ac.cn/software/pGlyco/index.html). This function has been systematically tested since PANDA v1.1.5\_x64_GlycoPep.
* Please note that if you combine the search results of multiple raw files into a single file (such as a protein/spectra file for pFind3 or a txt file for pGlyco2) when using pGlyco2 or pFind3, you should split the search result file into multiple files before quantification. This is because, in PANDA, each raw file is required to be related with its corresponding search result file. **I have provided another tool ([pFindSplit](https://sourceforge.net/projects/panda-tools/files/)) for users to split the merged result files of pFind3 and pGlyco2.**

### PANDA v1.1.5 for glycopeptide quantification (8/1/2019) (beta version)
* PANDA now supports to read the result file of [pGlyco2](http://pfind.ict.ac.cn/software/pGlyco/index.html) for glycopeptide quantification.
* PANDA supports to read the result file of different versions of pGlyco: 
   
	&ensp;XX-GP-FDR.txt

    &ensp;XX-GP-SVM-FDR.txt

    &ensp;XX-GP-FDR-Pro.txt 


* Please download the **"[PANDA v1.1.5 x64_GlycoPep.7z](https://sourceforge.net/projects/panda-tools/files/PANDA_v1.1.5_x64_GlycoPep.7z/download)"** to do glycopeptide quantification.
* Please note that this is a beta version and for now, only label-free glycopeptide quantification can be done. 
### PANDA v1.1.5 (7/15/2019)
* Fix a bug when reading mzML files converting from SCIEX wiff files. Please note that when dealing with SCIEX wiff files, we should firstly convert wiff to mzXML using msconvert, then convert mzXML to mzML without choosing the option "use zlib compression". 
### PANDA v1.1.4 (12/12/2018)
* The cross quant function ("match between runs") will be skipped and PANDA will not be halted when there were few peptides for RT alignment.
* Fix a bug when reading Thermo raw files.
### PANDA v1.1.3 (6/27/2018)
* Fix a bug when quantifying iTRAQ/TMT labeling data.
### PANDA v1.1.2 (8/22/2017)
* Fix bugs about merging multiple samples in label-free quantification.
* The development environment is changed from VS2013 to VS2017. So users need to install [Microsoft Visual C++ Redistributable for Visual Studio 2017](https://www.visualstudio.com/zh-hans/downloads/) first before using PANDA.
* **PANDA no longer supports the 32 bit OS. The x64 version of PANDA is the official release now.**

### PANDA v1.1.1 (1/13/2017)
* Bugs about the parallel mode and the XML output function are corrected.
* Print the ModifiedSeq (ReadableMod) of peptide in PepList files.

### PANDA v1.1.0 (10/15/2016) 

> **Important improvement**

* Update the GUI of PANDA.
* Release the x64 version which is able to handle large-scale MS data. The x64 version of PANDA is recommended.


### PANDA v1.0.2 (9/13/2016)
PANDA v1.0.2 contains some updates in the GUI:

* Max thread number can be automatically set according to the core number of user's computer.
* Max cached file number is set as "sample num*replicate num".

### PANDA v1.0.1 (8/31/2016)
* PANDA v1.0.1 is able to be used in Windows XP and Windows Server 2003&2008. The required minimum version of .NET Framework is changed from v4.5 to v4.0.

### PANDA v1.0.0 (8/1/2016)
* The first release version of PANDA.

## Hardware requirements
- Intel Pentium III/800 MHz or higher (or compatible) although one should probably not go below a dual core processor.
- 2 GB RAM minimum.
## Software requirements

### (1) Microsoft Visual C++ Redistributable for Visual Studio 2017 is required since v1.1.2

* [Download link](https://go.microsoft.com/fwlink/?LinkId=746572) for x64
* [Download link](https://go.microsoft.com/fwlink/?LinkId=746571) for x86
### (2) [.NET Framework 4.5](https://www.microsoft.com/en-us/download/details.aspx?id=30653) or higher from Microsoft

### (3) MSFileReader

Both 32bit and 64bit versions are required to be installed to access Thermo raw files. The latest version MSFileReader 3.0 SP3 can be downloaded from [here](https://thermo.flexnetoperations.com/control/thmo/download?element=6306677).

### Windows is currently the only operating system supported. Supported versions are

- Windows 7 SP1 (x64)
- Windows 8
- Windows 10
- Windows Server 2008 R2 SP1 (x64)
- Windows Server 2008 SP2 (x64)


## Installation

Download link: [https://sourceforge.net/projects/panda-tools/](https://sourceforge.net/projects/panda-tools/)

Please see "[User Manual for PANDA.pdf](https://sourceforge.net/projects/panda-tools/files/User%20Manual%20for%20PANDA.pdf/download)" for details.

## Test data

* The label-free dataset consists of two mzXML files and two pepXML files (PeptideProphet results).

* The labeled dataset consists of two Thermo raw files and two PepList files ([PepDistiller](https://sourceforge.net/projects/pepdistiller/) results).

##  License

  Please see the file called "LICENSE_English.pdf" or "LICENSE_Chinese.pdf".

##  Contact

  For any questions involving PANDA, please contact [Dr. Cheng Chang](https://orcid.org/0000-0002-0361-2438)![](https://orcid.org/sites/default/files/images/orcid_16x16.png)
(Email: [changchengbio@gmail.com](mailto:changchengbio@gmail.com)).


## Copyright

This software product is developed by Dr. Cheng Chang from the National Center for Protein Sciences (Beijing). All title and intellectual property rights, which is generated by the software product (including, but not limited to, relative images, data, texts, additional program and other software products (dll, exe, etc.), incidental help materials, and any copies of the Software Products are protected by Copyright Law of People’s Republic of China and international copyright treaties and other intellectual property laws and treaties. Users only get the right to use this software product.
