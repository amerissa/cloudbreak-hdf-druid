# HDP With Druid and HDF Using Cloudbreak
This repo has the code and insturctions needed to spin up many (we did 50 at a time) single node clusters with HDP, Druid, and HDF with a single command line.

Due to compatibility issues with HDP and HDF on a single Ambari, we are limited to HDP 2.6, Ambari 2.6, and HDF 3.0

The repo has the following:
  - Blueprint: upload as to Cloudbreak.
  - CLI: json to create clusters with json. Edit to contain your key and credentials
  - Recipes: Two recipes, hdfprep is pre ambari start and streamline is post cluster install.
  - WWW: Due to a bug with repo version, use the tar housed in the repo for the mpack. 

### Insturctions:

  - Install cloudbreak using the default install (see cloudbreak docs)
  - Upload blueprint as datavore
  - Upload the two recipes: hdfprep as pre-ambari-start, streamline as a post-cluster-install
  - Install and configure Cloudbreak CLI (see cloudbreak docs)
  - Change the lab.json to your liking (VPC, subnet, credentials, sshkey)
  - The commands file has sample oneliners to spinup or destory multiple clusters
