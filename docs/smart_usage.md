
## How to process a raw HSQC spectrum to a NMR table with MestreNova

1. Open your raw HSQC spectrum in MestreNova
    - Drag&Drop your HSQC file (for Bruker data you find your spectrum under: pdata/1/2rr)
    - Depending on purity and concentration of your sample and aquisition time your
      spectrum looks more or less clean and may need additional processing (see 2.)
    ![image](https://user-images.githubusercontent.com/57916837/70353294-f153a680-1821-11ea-96fb-85f3fea4f2b4.png)
2. For processing your HSQC spectrum click on 'Processing' tab
    - click on 'Auto Phase Correction' (optional: correct manually)
    - click on 'Auto Baseline Correction'
    - click on 'More Processing' --> click on 'Reduce t1 noise'
    You should see a clean spectrum now.
    ![image](https://user-images.githubusercontent.com/57916837/70353422-2b24ad00-1822-11ea-90a9-424dd2619d1a.png)
3.  Annotate HSQC spectrum with chemical shifts (1H,13C)
    - click on 'Analysis' tab
    - click on Auto Peak Picking (Important: Check by manually adding missed peaks and removing duplicated, nonsense and solvent peak         annotations).
    Now each peak should be annotated with two numbers separated by comma (1H, 13C chemical shifts)
    ![HSQC_annotation](https://user-images.githubusercontent.com/57916837/70353559-7939b080-1822-11ea-84ea-87cc07946574.png)
4. Generate NMR table from annotated HSQC spectrum
    - click on 'Analysis' tab
    - click on 'NMR Peaks Table'
    - move the f2 column to the left of the f1 column
    - copy all (ctrl+A)
    - click on 'copy peaks' and choose 'copy table'
    ![HSQC_annotation_to_table](https://user-images.githubusercontent.com/57916837/70353982-6a9fc900-1823-11ea-8704-7458b0a7f783.png)
5. Generate .csv file for SMART Analysis
    - open Excel or similar program and paste the table (ctrl+V)
    ![image](https://user-images.githubusercontent.com/57916837/70354067-958a1d00-1823-11ea-93da-9eaf03f11d2f.png)
    - align table in such a way that all values of f2 dimension = 1H are in one column and all values of the f1 dimension = 13C are in         another column next to it
    ![image](https://user-images.githubusercontent.com/57916837/70354383-409ad680-1824-11ea-8847-7eaa167779be.png)
    - open a new excel document (ctrl+N)
    - type in column A1: '1H' and in column B1: '13C'
    - copy and paste the table so that all values with 1H data are in column A2-AX and all values with 13C data are in column B2-BXX         ![image](https://user-images.githubusercontent.com/57916837/70354216-e3068a00-1823-11ea-9ac9-cb51e5381091.png)
    - reduce column B (13C values) from two decimals to one (for example 128.22 --> **128.2**)
    - mark your table + header (1H,13C) and save as comma-separated file (.csv).

**You are ready to use SMART 2.0 Analysis! :)**

**Please feel free to play around with the processing parameters such as including/excluding noise signals or signals from other minor compounds in case of mixtures or explore the differences of SMART results when referencing your spectra compared to tables without referencing. Overall SMART is designed to be very robust towards any of these changes as its training is not only based on the absolute position of the peaks, but the relative position of each peak towards every other peak (see also References 1 + 2).**

## User's Guide for SMART 2.0 Analysis

Welcome to use the SMART 2.0 to test your compound(s) @ [SMART 2.0](https://smart.ucsd.edu/classic).

- The current version of SMART 2.0 as of 11/25/2019 consists of 2D NMR spectra from 53,076 natural products. 
- Before you start, please unblock any pop-up blockers in your web browser for smart.ucsd.edu website.
- One SMART 2.0 analysis should take < 20 seconds (if still 'analyzing' double check your input).
- You can run multiple (up to 10) analyses at once.
- If your results are dissatisfying please try to process your data again manually (go back to **How to process a raw HSQC spectrum to a NMR table** and then delete noise and duplicate annotations, add peaks missed by auto-peak picking etc.) 

## Input Data Formatting

Please prepare your NMR peak lists of each compound using Excel or preferably notepad/wordpad and save the NMR table of each compound as a comma-separated value (.csv) file. If you are using Microsoft Excel, this can be done by click "save as" and then choose the two file types. Please always place 1H data in the first column and their corresponding 13C data in the second column. The first row will be left for strings “1H” and “13C” as table head. Please strictly keep 1H shifts in 2 decimals and 13C shifts in a single decimal only. You can name the .csv file with any name that your operating system accepts.

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

### Supported Formats at SMART
SMART supports CSV formats for analysis. You can check your csv file by opening it with text editors such as wordpad or notepad. Your table should appear like this:

    1H,13C
    1.09,14.3
    2.21,22.2
    3.41,56.9
    7.21,128.6
    7.29,123.4

### Submit CSV file for SMART Analysis

After the .csv file is ready, simply upload it to the first window by drag&drop (analysis automatically starts) or copy and paste the table and click analyze. You can submit multiple jobs at one time. **Important: You have to allow pop-ups for https://smart.ucsd.edu/classic. If your analysis is still running after 20 seconds, pop-up blockers are the most likely reason why your analysis failed.** The result will show up in the next webpage as images with chemical structures, compound names, similarity scores, and molecular weights. The Top 100 hits are ranked by similarity scores. You can download the result by clicking the “download results” icon and open it with Excel.

## Troubleshooting

### Overview
This section addresses some common issues with the analysis workflows at SMART. If you run into any of these common issues, hopefully this page will give you actionable steps to address them. If this page cannot help you, please refer to the [forum](https://groups.google.com/forum/#!forum/smartnmr) to help answer your questions.

### SMART Analysis

**Failed Job**

1. If your analysis is still running after 20 seconds, pop-up blockers are the most likely reason why your analysis failed. You have to allow pop-ups for https://smart.ucsd.edu/classic.
2. The file format input is incorrect. Please make sure it is a supported file format for SMART (see Input Data Formatting)

**Downloaded Results file cannot be opened**

Yes you can :) You can open the downloaded results with any text editor (Excel, Notepad, Wordpad). Just make a right-click on the file, click on 'open with' and then choose one of the former mentioned programs.

**Results Incorrect**

The SMART is still at its early stage of development. It will become more and more accurate the more spectra you contribute to the Moliverse (see Contribute to SMART).
- If your results show strange suggestions and all of the have a cosine score of 1.0 you probably have switched the columns. Please be sure that your first column has proton shifts (1H) and your second column has carbon shifts (13C), where each 1H-13C pair is separated by a comma.
- If your CSV file won't show exactly two decimals for 1H, or exactly a single digit for 13C, you can mannually change the last digit of the chemical shift from 0 to 1. E.g., change 7.30 to 7.31. Slight variation of the last digit won't affect your test result.

## Visualize your result(s) in the 3D cluster space (Moliverse)

Please click the "Embed in the Moliverse" bar in the upper right side of the result page. Wait a while for the Embedding Projector to launch. To find your query molecule, please type "query" in the search bar in the upper right side of the Embedding Projector Webpage. Naturally, your query compound as well as its 100 closest analogues will light up in unique colors (decreasing cosine similarity will be displayed by purple-red-orange-yellow).

- To better observe the clustering effect, please click UMAP or T-SNE tabs in the lower left window. The clusters will organize themselves in real-time, clustering more similar compounds in close proximity and more dissimilar compounds apart from each other.
- Further you can access and enjoy the whole 'Moliverse' under https://smart.ucsd.edu/classic (click on 'Explore Moliverse')

## Visualize the 3D cluster space (Moliverse) with VR devices

Please click [Video_1](https://youtu.be/Pgfw-90t1t0), [Video_2](https://youtu.be/2qM_kFf-SRo) and [Video_3](https://www.youtube.com/watch?v=v_c-Z1a5-KU) to watch the VR movie. The VR software will be delivered soon!

[![VIDEO_1](http://img.youtube.com/vi/Pgfw-90t1t0/0.jpg)](http://www.youtube.com/watch?v=Pgfw-90t1t0 "Small-molecule Interactive Mapping Applications")

[![VIDEO_2](http://img.youtube.com/vi/2qM_kFf-SRo/0.jpg)](http://www.youtube.com/watch?v=2qM_kFf-SRo "Into the Moliverse")

[![VIDEO_3](http://img.youtube.com/vi/v_c-Z1a5-KU/0.jpg)](http://www.youtube.com/watch?v=v_c-Z1a5-KU "The Moliverse, A Digital Frontier to Reshape Natural Products Research")

## Contact

If you have any questions about how to use SMART please first ask the community at the SMART forum located here: [forum](https://groups.google.com/forum/#!forum/smartnmr). We will respond you as soon as we can. If you woud like to access our to be online SMART 3.0 version, please email Hyunwoo Kim (hwkim at-sign ucsd dot edu) for off-line trials.

## References

To reference the system please cite the papers listed below.

1. Zhang C, Idelbayev Y, Roberts N, Tao Y, Nannapaneni Y, Duggan BM, Min J, Lin EC, Gerwick EC, Cottrell GW, Gerwick WH. Small Molecule Accurate Recognition Technology (SMART) to Enhance Natural Products Research. Scientific reports. 2017, 7(1), 14243.  [DOI: 10.1038/s41598-017-13923-x](https://doi.org/10.1038/s41598-017-13923-x)

2. Coming soon.

<a href="https://smart.ucsd.edu/classic" target="_blank"><img src="https://user-images.githubusercontent.com/20175888/70386594-ecd8dc00-194e-11ea-8378-ba1929e90ae4.png" alt="SMART_LOGO" title="USE SMART" align="right" width="250" height="100" border="10" /></a>
