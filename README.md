# IndexDisableDrop
These are the PowerPoint, backup file and scripts to create the Agent jobs for STLSSUG Index Disable/Drop Presentation. They are presented "as is", but should work for any 2016+ SQL Server version.  

NOTES

It is important to note that the Agent jobs have been configured so that the email notification steps will not run.  This is by design; not everyone may want to use that functionality, and everyone who does will have a different setup for it.  In order to enable them, please do the following:
  1) Ensure database mail is enabled
  2) Supply the profile information for the idxdd.EmailIndexesToDrop and idxdd.EmailUnsedIndexes stored procedures
  3) In the Agent jobs, find the step prior to the email notification step and modify it so that the job does not stop before going on to the email step
