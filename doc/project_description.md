# Combine PSMs by rescoring PSMs

The project strives to combine PSMs from different search engines by predicting the spectra of each PSM's peptide, and compare the predicted peptide with an observed spectrum.

## Spectrum prediction

We will use results as predicted from the search engine [Prosit](https://pubmed.ncbi.nlm.nih.gov/31133760/.

## Rescoring PSMs

Others have rescored PSMs for other purposes previously.
Most notably [MS2Rescore](https://pubmed.ncbi.nlm.nih.gov/31077310/) and [Proteoformer](https://www.mcponline.org/article/S1535-9476(20)32766-3/fulltext) with a [follow-up](https://www.mcponline.org/article/S1535-9476(21)00049-9/fulltext).


## Search engines to combine

* [crux/tide](http://crux.ms/commands/tide-search.html)
* [msgf+](https://omics.pnl.gov/software/ms-gf)
* [MS-Amanda](https://ms.imp.ac.at/?goto=msamanda)
* [Andromeda](https://www.maxquant.org/)


### Dataset

A temptive set to start with is this [HELA-UPS mixture](http://proteomecentral.proteomexchange.org/cgi/GetDataset?ID=PXD002370-1&test=no).

#### First try
* Download the raw data
* Convert one of the raw files to msdata-format using Proteowizard's [msconvert](http://proteowizard.sourceforge.net/tools.shtml). This is available through [containers](https://hub.docker.com/r/biocontainers/proteowizard/).
* Search the data with crux/tide.