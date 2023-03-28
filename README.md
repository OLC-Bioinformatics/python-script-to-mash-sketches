# python-script-to-mash-sketches
This program calculates the mash sketches from the  BestAssemblies direcory using all .fasta files
people can keep adding the paths that is from processed data and it will look for files and does the mash sketches. usually there are too many files so it splits part by part and run and concatenate the sketches and remove the temporary part files.
Final step , it makes the final_sketches.msh file with all sketch

The purpose of this program is to calculate the sketches for every new incoming assemblies and can be used in close relatives by modifying sketch files, because those 
were created in 2019.

This runs on Julie's system where i work everyday at 12 am. if someone wants to modify the cron job it should be done like this

crontab -e ( my fav editor is vi)


0 0 * * *  /home/jshay/miniconda3/bin/python /mnt/nas/users/madhu/mash_sketch_all.py >> /mnt/nas/users/madhu/mash.log 2>&1   [ here the env of python is added and the script is included in the crontab shell and save it wq!]
