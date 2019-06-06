# Homework 10

You will fill out the following
questionnaire for each program and submit the answers as your final homework. You will
also share your questionnaire with the group that created the program __by the end of discussion__.

---

## Peer Review for MiSebastes Annotator

#### 1. Is the Readme file the first document displayed upon lading the Github?  Does this Readme page include a title, and the name and contact information for all project members?
Yes! Looks good

#### 2. Is the purpose of this program clear from the Introduction?  What -in your own words- is the motivation behind the program.
The purpose is to identify which Rockfish species share the same genetic barcode, which then tells you how many different species are present in your eDNA sample.
The intro is a little hard to understand because its so technical. Maybe splitting bits into different paragraphs could make it a little more digestible?

#### 3. Is there a program workflow and is it easy to understand?  What -in your own words- is the program workflow?
Its a little complicated. 
The program takes the input file, removes any repeated sequences, but I get lost at "with all species that share the barcode assigned to the sequence barcodes with different species that share a barcode. "

#### 4. Are the dependencies indicated in the workflow?  If there are Hoffman2 specific requirements are they indicated?
Yes dependencies are listed in the workflow, and their download links are in 'prerequisites'.
There are no Hoffman2-specific requirements

#### 5. Are there instructions for running the program?  Do the instructions make sense?  What would you do to improve the instructions?
There are multiple example usages and im a little confused which is the main one. 
Maybe you could have some bolded headers like "if you want to run the full program" and "if you just want to trim the fasta file" etc so its a bit clearer

#### 6. Is there a section that indicates the files and directories produced by the program?
Yes! well its not a section of its own, but they are listed at the end of example usage. 

#### 7. Are the research programs / motivations for the program cited?  Are the dependencies cited?
No, citations are needed.

---

### The Scripts

#### 8. Is there a directory that contains all of the program scripts?
No, the scripts are in the main directory

#### 9. Do these programs generate a run log?
N/a ? I think Emily said we didnt need this??

---

### The Vignette

#### 10. Is there a directory called Vignette and does it include a test set, the commands used to run the program and the expected output databases?
No, but theres a Vignette readme. 

#### 11. Where you able to run the Vignette using the small test dataset? If not what errors did you get?  If so was it easy to run the dataset?  Where the instructions clear.
N/a

#### 12. Where you able to reproduce the expected output?  If not what was different.   
N/a

---

### General

#### 13. Give __at least two__ suggestions for ways to improve the GitHub page or the operation of the program.
I think having more defined sections with bolded headers could improve the organization/readability of the readme
I think making the intro a little less jargon-y could also help. But I know its a specific code for experts, so this probably isnt important. Maybe just include some paragraphs in the intro to break it up
:)

---

## Peer Review for Info-Fish: Matching eDNA Recovered Species to Ecological Information from Fishbase

### The Readme

#### 1. Is the Readme file the first document displayed upon lading the Github?  Does this Readme page include a title, and the name and contact information for all project members?
Yes! Looks great

#### 2. Is the purpose of this program clear from the Introduction?  What -in your own words- is the motivation behind the program.
Yes! I love how you get into the purpose of the program by the 3rd sentence. 
The motivation is to make it easier to assign trait information to an eDNA file that has been processed by Anacapa. 

#### 3. Is there a program workflow and is it easy to understand?  What -in your own words- is the program workflow?
Yes, theres a workflow but maybe it could be a bit more detailed (like explain how it does things? and what an ASV is)
It takes the input file, extracts the unique species, searches them through fishbase (by matching the ASVs to the ASVs in fishbase?), and then makes an output table.
- the Project Outline section includes all these things in more detail. maybe move this bit to your workflow section?

#### 4. Are the dependencies indicated in the workflow?  If there are Hoffman2 specific requirements are they indicated?
Yes! Hoffman2 requirements are listed further on. 

#### 5. Are there instructions for running the program?  Do the instructions make sense?  What would you do to improve the instructions?
Yes they do! maybe you could add that they need to install everyting before running? 

#### 6. Is there a section that indicates the files and directories produced by the program?
Yup

#### 7. Are the research programs / motivations for the program cited?  Are the dependencies cited?
Yes

---

### The Scripts

#### 8. Is there a directory that contains all of the program scripts?
No, theyre all in the main directory

#### 9. Do these programs generate a run log?
N/a ? I think

---

### The Vignette

#### 10. Is there a directory called Vignette and does it include a test set, the commands used to run the program and the expected output databases?

Yes

#### 11. Where you able to run the Vignette using the small test dataset? If not what errors did you get?  If so was it easy to run the dataset?  Where the instructions clear.
When i type "bash final_project_bash_script.sh -w /output_directory -a /directory_with_file/Fish_taxonomy_file.txt" into the command line I get the error message "bash: final_project_bash_script.sh: No such file or directory"

I changed the script name to the one in the directory, (fishbase_bash_script.sh). I then tried the command "bash fishbase_bash_script.sh -w /output_directory -a /directory_with_file/Fish_taxonomy_file.txt"
I got the message:
```
The variable stored in -w is /output_directory
The variable stored in -a is /directory_with_file/Fish_taxonomy_file.txt
\n
The first variable $DB is /Users//Documents/C177/Project/
The second variable $EST is Species,MaxLengthTL,Troph,seTroph,TrophObserved
The third variable $PRE is Species,PredatorGroup,PredatorName
The fourth variable $STO is Species,StockDefsGeneral,IUCN_Code,EnvTemp,Resilience,GenBankID,IUCN_ID
fishbase_bash_script.sh: line 42: Rscript: command not found
```
#### 12. Where you able to reproduce the expected output?  If not what was different.
No I couldnt :(

---

### General

#### 13. Give __at least two__ suggestions for ways to improve the GitHub page or the operation of the program.
Check the bit of the code (line 42?) that makes an error message. 
Reorganize the readme to include some of the later details in the workflow + instructions sections. 
