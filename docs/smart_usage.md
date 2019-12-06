
## Webserver User's Guide for SMART 2.0 Analysis

Welcome to use the SMART 2.0 to test your compound(s). 

The current version of SMART 2.0 as of 11/25/2019 is trained on 2D NMR spectra of 53,076 natural products. 

Before you start, pleaes unblock any pop-up blockers in your web browser.

Please checkout the server at [smart.ucsd.edu](https://smart.ucsd.edu/classic/).

## Input Data Formatting

Please prepare your NMR peak lists of each compound using Excel or preferably notepad/wordpad and save the NMR table of each compound as a comma-separated value (.csv) or tab-separated (.tsv) file. If you are using Microsoft Excel, this can be done by click "save as" and then choose the two file types. Please always place 1H data in the first column and their corresponding 13C data in the second column. The first row will be left for strings “1H” and “13C” as table head. Please strictly keep 1H shifts in 2 decimals and 13C shifts in a single decimal only. You can name the .csv file with any name that your operating system accepts.

|     1H     |     13C     |
|:----------:|:-----------:|
|    3.00    |     29.0    |
|    3.40    |     29.0    |
|    5.00    |     57.6    |
|    5.60    |     59.4    |
|    1.80    |     19.2    |
|    5.17    |     57.4    |
|    7.49    |    129.0    |
|    7.51    |    130.5    |
|    7.47    |    131.4    |

In the NMR table files, wherever there are diastereotopic protons on a methylene carbon (i.e., CH2 with two distinct proton shifts), please add a separate entry for both the carbon and proton:

|     1H     |     13C     |
|:----------:|:-----------:| 
| 3.12       | 43.2        |
| 3.40       | 43.2        | 

After the .csv (or .tsv) file is ready, simply upload it to the first window by drag&drop. You can submit multiple jobs at one time. The result will show up in the next webpage as images with chemical structures, compound names, similarity scores, and molecular weights. The Top 10 hits are ranked by similarity scores. You can download the result by clicking the “download results” icon.

## References

To reference the system please citing the papers listed below. To ask questions, please post on the user forum. We will respond you as soon as we can.

1. Zhang C, Idelbayev Y, Roberts N, Tao Y, Nannapaneni Y, Duggan BM, Min J, Lin EC, Gerwick EC, Cottrell GW, Gerwick WH. Small Molecule Accurate Recognition Technology (SMART) to Enhance Natural Products Research. Scientific reports. 2017, 7(1), 14243.

2. Coming soon.
