# Welcome to SMART Documentation

SMART (Small Molecule Accurate Recognition Technology) is the next generation of NMR analysis.

## Webserver User's Guide for SMART 2.0 Analysis

Welcome to use the SMART 2.0 to test your compound(s). 
The current version of SMART 2.0 is trained on 2D NMR spectra of 53,076 natural products. 
Please prepare your NMR peak lists of each compound using Excel or preferably notepad/wordpad and save the NMR table of each compound as a comma-separated value (.csv) or tab-separated (.tsv) file. Please always place 1H data in the first column and their corresponding 13C data in the second column. The first row will be left for strings “1H” and “13C” as table head. Please strictly keep 1H shifts in 2 decimals and 13C shifts in a single decimal only. You can name the .csv file with any name that your operating system accepts.

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

To reference the system please citing the papers listed below. To ask questions, please post on the user forum. We will respond you as soon as we can.

## Instructions for submitting NMR data to the Moliverse (the training set for SMART)
Please read all of the instructions below before you fill in the data collection files.
### Definitions
Folder = a folder on your computer for organizing files; File = an excel file in .xlsx or .csv format; Sheet = a sheet within an excel file; Training database = the database used to train the AI; Test dataset = the inquiry dataset awaiting the AI to generate structural hypothesis
### Submitting structures to the Moliverse library
Thank you for contributing to the SMART training database (AKA the Moliverse Library). For this submission, we ask you to fill out some information in the metadata file (only one metadata file for all compounds being submitted), and a second file with the tabulated NMR data as described below (the NMR data for each compound in its own file). 
Connection between the two files will be by a 6 digit code number.  The starting letter/number combination for your submitted compounds will be assigned by the SMART operators, and then you should increment up for each ensuing compound by a value of 1 (e.g. AAA001 is the assigned code, the next compound in your series is AAA002, and so forth). Although compound replicates need to be avoided, please don’t worry as the SMART can cope with some replicates.
In the Metadata file and the NMR Tables, only the items with an orange colored background are required; the green fields are desirable and will help us with developing more accurate and informative future versions of SMART. If for any compound, a specific data entry is not available, please leave it as blank.
As noted above, in the Metadata file, only the SMILES entry is mandatory. Only when the isomeric SMILES is not available for a compound, canonical SMILES can be entered instead. The SMILES can be found on the PubChem website for majority of published compounds. If you cannot fine the SMILES on PubChem, the 3D structure in ChemDraw can be converted to SMILES by the program.
### Convert Structure to SMILES
To convert a ChemDraw structure to SMILES, you must:
1) Select the structure using the selection tool 
2) From the Edit menu, point to Copy As, and then choose SMILES
3) Paste the string in the target cell of the excel metadata file sheet.
### Minimum information for NMR tables
For compiling the NMR tables, please follow the examples in "NMR Tables" file in this same folder as the format for your data. NOTE: proton shifts should be rounded to exactly 2 decimal digits, and 13C shifts should be rounded to exactly a single decimal digit.
For the NMR tables, the atom numbering is not needed, but just be certain that the proton shift matches the carbon shift in every row of the table.
In the NMR table files, wherever there are diastereotopic protons on a methylene carbon (i.e., CH2 with two distinct proton shifts), please add a separate entry for both the carbon and proton:

| Column A | Column B | Column C               |   
|----------|----------|------------------------|
| 13C      | 1H       | Carbon type (optional) |
| 43.2     | 3.12     | CH2                    |
| 43.2     | 3.40     | CH2                    |

In the NMR table files, please put 13C shifts in Column A of the sheet and proton shifts in Column B of the sheet, as shown above.
If you have any questions, please contact Chen Zhang chz023@ucsd.edu or Raphael Reher (rreher@ucsd.edu)

End of Instructions.

## Acknowledgements

We sincerely thank the following people who have done great work to make the idea of web-based SMART become true. You guys are awesome. 
Names appear in alphabetic order.

| First     |  Middle  | Last         |
|-----------|:--------:|--------------|
| Kelsey    |    L.    | Alexander    |
| Nuno      |          | Bandeira     |
| Mitchell  |          | Christy      |
| Garrison  |    W.    | Cottrell     |
| Pieter    |    C.    | Dorrestein   |
| Erik      |    C.    | Gerwick      |
| William   |    H.    | Gerwick      |
| Michael   |          | Gilson       |
| Jenny     |          | Hamer        |
| Yerlan    |          | Idelbayev    |
| Hyunwoo   |          | Kim          |
| Preston   |    B.    | Landon       |
| Aaron     |          | Landon       |
| Tiago     |    F.    | Leao         |
| Eugene    |    C.    | Lin          |
| Zheng     |          | Long         |
| Henry     |  Huanru  | Mao          |
| Andrés    | Mauricio | Caraballo    |
| Jie       |          | Min          |
| Anthony   |          | Mrse         |
| Ben       |    C.    | Naman        |
| Yashwanth |          | Nannapaneni  |
| Louis     |   Felix  | Nothias      |
| Poornav   |    S.    | Purushothama |
| Siddarth  |          | Ravichandran |
| Raphael   |          | Reher        |
| Nicholas  |          | Roberts      |
| Yiwen     |          | Tao          |
| Yoshinori |          | Uekusa       |
| Ezra      |          | VanEverbroeck|
| Vishal    |    T.    | Vasudevan    |
| Mingxun   |          | Wang         |
| Chen      |          | Zhang        |
| Jianping  |          | Zhao         |
