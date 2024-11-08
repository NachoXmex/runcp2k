# runcp2k
Script to submit CP2K jobs using the slurm queue system. Intended for Alps.
Before using it:
  - Modify account and cp2k_path accordingly

This script will:
 1 Create a work directory with the name of the input and the PID of the script in the scratch directory. 
 2 Copy the input and restart files if necessary to that work directory.
 3 Build the jobfile for the slurm system based on the selected options in the work directory.
 4 Submit the jobfile
 
All calculation outputs will be left in the work directory

Usage:
./runcp2k [options] input.inp

  Options:
    --manual, -m 
                 The script will display all the available queues and
                 it will ask for all required options.
    --queue, -q  
                 Name of que queue
    --nodes, -n  
                 Number of nodes
    --time, -t   
                 Maximum time for the job

input.inp can be any name, the .inp extension is optional.
