README author: Bijaya Adhikari
Dated: December 13, 2018. 


The data accompanying this README was leveraged for the following paper.

Fast and Near-Optimal Monitoring for Healthcare Acquired Infection Outbreaks
Bijaya Adhikari, Bryan Lewis, Anil Vullikanti, Jose Mauricio Jimenez and B. Aditya Prakash
PLOS Computational Biology.

==========================================================================================================================================================================================

Data Overview:

The data consists of the following directories:

1) MobilityLogs
2) CalibratedSimulations
3) VariousInitialStates


Detailed description of each directory is as follows:


==========================================================================================================================================================================================

1) MobilityLogs

Consists of the mobility logs of anonymized patients and healthworkers. Schema of each file is described in the first row of the file. The files in the directories are as follows:
	a) all_locations_20130710.txt: Summary of all static agents. 
	
	
	b) all_populations_20130710.txt: Summary of all human agents.
	
	
	c) HAISE_Carilion_all_visits_day_[0-200].txt: The mobility logs for each day in the simulation. The files represent who-goes-where relations. An example entry in the file is as follows:
	
	                #Person location Sublocation StartTime EndTime Type
					  201      52        1         0         20      1
				
	The entry represents that the person with anyonimized ID of 201 was at location 52, sublocation 1 from time 0 to 20 (in seconds) performing activity of type 1.
	
	The time for each day starts at 0 seconds.
	
	d) loc_model: description of location types based on the IDs
	
==========================================================================================================================================================================================

2) CalibratedSimulations

Consists of calibrated simulations representing the Hospital Acquired Simulations spread given the Community Acquired Cases.

The subdirectories are as following:

i) results1: Represents the simulation results. 
ii) socialnet1: Represents the resulting graph from the interactions in the mobility log for each of the simulation.


The details regarding each of the files are as follwos:

	a) diseaseq[x].txt.A: represents the HAI spread in simulation x. The description for each state is given in the top of the file. An example entry in the file is as follows:
	
					#person time state 
					 10301    0    25
	
	The entry implies that the agent 10301 was at state 25 starting from time 0.
	
	The time in each file starts at 0 seconds and ends at [200*24*60*60] seconds.
	
	
	b) dz_dendogram[x].txt.A: represents the dendogram (who infects whom relation) for simulation x.
	
	c) socnet.txt.[x].A: represents the social network representation of the data.
	
	
==========================================================================================================================================================================================

3) VariousInitialStates

Consists of simulations on the calibrated models for various types of initial stage. The initial stage is defined as the infections in day 1. The schema of the simulatuon spread file is the same as above.


==========================================================================================================================================================================================


Please consider citing our paper mentioned above if you use the data.

Please contact the authors for more information.

 

 


