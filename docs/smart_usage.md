
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
- reference your spectrum to residual solvent peaks or other reference points such as TMS signal (optional as SMART recognizes the relative position of all correlations)
- click on Auto Peak Picking (Important: Check by manually adding missed peaks and removing duplicated, nonsense and solvent peak annotations).
Now each peak should be annotated with two numbers separated by comma (1H, 13C chemical shifts)

![HSQC_annotation](https://user-images.githubusercontent.com/57916837/70353559-7939b080-1822-11ea-84ea-87cc07946574.png)

4. Generate NMR table from annotated HSQC spectrum
- click on 'Analysis' tab
- click on 'NMR Peaks Table'
- move the f2 column to the left of the f1 column
- copy all (ctrl+A)
- click on 'copy peaks' and choose 'copy table'

![HSQC_annotation_to_table](https://user-images.githubusercontent.com/57916837/70353982-6a9fc900-1823-11ea-8704-7458b0a7f783.png)

- open Excel or similar program and paste the table (ctrl+V)

![image](https://user-images.githubusercontent.com/57916837/70354067-958a1d00-1823-11ea-93da-9eaf03f11d2f.png)

- align table in such a way that all values of f2 dimension = 1H are in one column and all values of the f1 dimension = 13C are in another column next to it

![image](https://user-images.githubusercontent.com/57916837/70354383-409ad680-1824-11ea-8847-7eaa167779be.png)

- open a new excel document (ctrl+N)
- type in column A1: '1H' and in column B1: '13C'
- copy and paste the table so that all values with 1H data are in column A2-AX and all values with 13C data are in column B2-BXX

![image](https://user-images.githubusercontent.com/57916837/70354216-e3068a00-1823-11ea-9ac9-cb51e5381091.png)

- reduce column B (13C values) from two decimals to one (for example 128.22 --> **128.2**)


- mark your table + header (1H,13C) and save as comma-separated file (.csv).

**You are ready to use SMART 2.0 Analysis! :)**


## User's Guide for SMART 2.0 Analysis

Welcome to use the SMART 2.0 to test your compound(s). 

The current version of SMART 2.0 as of 11/25/2019 consists of 2D NMR spectra from 53,076 natural products. 

Before you start, please unblock any pop-up blockers in your web browser for smart.ucsd.edu website.

Please checkout the server at [SMART 2.0](https://smart.ucsd.edu/classic).

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

After the .csv file is ready, simply upload it to the first window by drag&drop. You can submit multiple jobs at one time. The result will show up in the next webpage as images with chemical structures, compound names, similarity scores, and molecular weights. The Top 10 hits are ranked by similarity scores. You can download the result by clicking the “download results” icon.

## Visualizing your result(s) in the 3D cluster space (Moliverse)

Please click the "Embed in the Moliverse" bar in the upper right side of the result page. Wait a while for the Embedding Projector to launch. To find your query molecule, please type "query" in the search bar in the upper right side of the Embedding Projector Webpage. Naturally, your query compound as well as its 100 closest analogues will light up in unique colors (decreasing cosine similarity will be displayed by purple-red-orange-yellow).

- To better observe the clustering effect, please click UMAP or T-SNE tabs in the lower left window. The clusters will organize themselves in real-time, clustering more similar compounds in close proximity and more dissimilar compounds apart from each other.
- Further you can access and enjoy the whole 'Moliverse' under https://smart.ucsd.edu/classic (click on 'Explore Moliverse')

## Visualizing your 3D cluster space in a VR headset

Please click [here](https://youtu.be/Pgfw-90t1t0) to watch the VR movie. The VR software will be delivered soon!

## References, Q&A

To reference the system please citing the papers listed below. To ask questions, please post on the user [forum](https://twitter.com/SMARTNMR1). We will respond you as soon as we can.

1. Zhang C, Idelbayev Y, Roberts N, Tao Y, Nannapaneni Y, Duggan BM, Min J, Lin EC, Gerwick EC, Cottrell GW, Gerwick WH. Small Molecule Accurate Recognition Technology (SMART) to Enhance Natural Products Research. Scientific reports. 2017, 7(1), 14243.

2. Coming soon.

<img src="https://user-images.githubusercontent.com/20175888/70386594-ecd8dc00-194e-11ea-8378-ba1929e90ae4.png" align="right" width="250" height="100" >
