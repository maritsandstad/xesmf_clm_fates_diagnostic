# xesmf_clm_fates_diagnostic

An XESMF based diagnostic tool to produce various plots and tables for CLM-FATES

Currently very much a work in progress

## Prerequisites

In order to use the tool you need to load and ESMF module and build an xesmf-containing conda environment on top of it. 

## Usage

To run navigate to the folder called scripts (or extend paths for run-scripts to include the full path to that folder in the following commands) and run: 
```
. setup.sh
```
Then run 
```
python run_diagnostic_full_from_terminal.py path_1 weight=weight_path compare=opt_path_2 outpath=opt_out_path opt_file=opt_file_path
```
where `path_1` is the path to the lnd/hist folder containing your output.

The other arguments are optional:

`weight_path` is a path to a weight-file if the standard one is not to be used 

`opt_path_2` is a path to output from a run you wish to compare to 

`outpath` is the path of where you want the output diagnostic figures filetree to go. If not sent the figures will be expected to go in a folder called figs situated in whatever directory you ran the command from.
If you want this to be viewable by web, choose a web-facing directory. For instance if you have access to the NS9560K account, make a subdirectory with the same name as your username in /datalake/NS9560K/www/diagnostics/noresm/ and make that your outpath, i.e. `outpath=/datalake/NS9560K/www/diagnostics/noresm/username`
