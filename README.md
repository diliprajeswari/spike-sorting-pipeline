# Intro to Spike Sorting using SpikeInterface Demo - Hussaini Lab
<div style="text-align: right"> <font color='black'>- by Dilip Rajeswari</font>  </div>

For this demo session, we'll walk through the basics of using `SpikeInterface` <font color='blue'>(AP Buccino et al., 2020)</font>, a python module designed to improve the accessibility, reliability, and reproducibility of spike sorting and all its associated computations, for extracellular analysis and spike sorting comparison. 

SpikeInterface wraps 5 subpackages:

`spikeextractors` - Python-based module for extracting recorded and spike sorted extracellular data from any file format <br>
`spikesorters` - Python-wrappers to spike sorting algorithms <br>
`spiketoolkit` - Python-based tools for pre-, post-processing, validation, and curation <br>
`spikecomparison` - Python package for comparing spike sorting output <br>
`spikewidgets` - Python plots and widgets relevant to spike sorting and electrophysiology <br>


### Dataset for this demo anlaysis

For this demo analysis, we will be using a recording from hippocampus CA1 (recording from [CINPLA](https://www.mn.uio.no/ibv/english/research/sections/fyscell/cinpla/)) using two microdrives (one per hemisphere) with four tetrodes each (32 channels in total). The duration is about 10 min. The dataset can be downloaded from Zenodo - [open-ephys-dataset](https://doi.org/10.5281/zenodo.4657314).


### Overview of the Demo Notebook
In this Demo Notebook, we'll walk through the spike sorting steps and compare between two spike sorting packages:

1. Load the data (cambridge_data) using the spikeextractors package <br>
2. Load the probe information using SpikeInterface's ProbeInterface <br>
3. Preprocess the recorded signals <br>
      a. Filtering
4. Run three popular spike sorting algorithm - Kluster, MountainSort, and IronClust - with different parameters <br>
      a. Spike Detection  <br>
      b. Feature extraction <br>
      c. Clustering  
5. Postprocessing and data curating the spike sorting output <br>
      a. quality metrics (automatic) <br>
      b. consensus-based 
6. Challanges/Limitations of Spike sorting <br>

<b>Note</b>: We could additionally use manual spike sorters : [Phy](https://github.com/cortex-lab/phy)
