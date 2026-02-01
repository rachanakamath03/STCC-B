# STCC-B

## Short-Term Course on Unix for Bioinformatics

1. Introduction
Modern bioinformatics relies heavily on Unix/Linux environments for processing, analyzing, and managing large-scale biological datasets. This course focuses on practical command-line proficiency, enabling reproducible, scalable, and debuggable workflows commonly used in genomics, transcriptomics, and computational biology.
All commands were practiced using macOS Terminal, which is Unix-based and functionally equivalent to Linux systems used in HPC clusters and servers.

Why Linux / Unix Is Essential in Bioinformatics

Nature of Bioinformatics Data
Biological data is:
Large (GB–TB scale)
Text-based (FASTA, FASTQ, GTF, BED, VCF)
Often processed remotely (HPC, cloud)

Characteristics of Bioinformatics Tools
Most tools:
Lack graphical user interfaces
Expect text input via standard streams
Produce text-based outputs
Are designed to be chained in pipelines


## File System Basics
Everything in Unix is treated as a file
Directories are files that contain other files
Paths can be:
Absolute: /home/user/data/file.txt
Relative: data/file.txt

## Core Navigation Commands
- pwd	Print working directory	Pipelines fail if paths are wrong
- ls	List files	Identify available inputs
- ls -l	Detailed listing	Check sizes & permissions
- ls -a	Show hidden files	Reveal .git, config files
- cd dir	Change directory	Navigate projects
- cd ..	Move up	Avoid directory confusion
- cd ~	Home directory	Reset navigation
- cd -	Previous directory	Fast switching
- Tip: Folder names with spaces require quotes - cd "project files"

## File & Directory Creation
- mkdir project
- mkdir -p genomics/{data,scripts,results}
- touch metadata.csv
- mkdir -p creates nested directories
- touch creates empty files (does not add content)

## Writing & Viewing Files
- echo -- "SampleID,Condition" > samples.csv
- echo "S1,Control" >> samples.csv
- cat samples.csv

## Operator	Meaning
- Overwrite - >
- Append safely - >>	

## Copying, Moving & Deleting
- cp file1.txt backup.txt
- mv old.txt new.txt
- rm file.txt
- rmdir empty_dir
