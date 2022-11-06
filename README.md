# CMPE283 : Virtualization 
# Assignment 1: Discovering VMX Features

#1 For each member in your team, provide 1 paragraph detailing what parts of the lab that member  implemented / researched. (You may skip this question if you are doing the lab by yourself).
    - *Sirisha Polisetty*
    - *Jayanth Vishal Reddy Godi*
2. Describe in detail the steps you used to complete the assignment. Consider your reader to be someone  skilled in software development but otherwise unfamiliar with the assignment. Good answers to this  question will be recipes that someone can follow to reproduce your development steps. Note: I may decide to follow these instructions for random assignments, so you should make sure  they are accurate. 
   1. Created a VM on gcloud using the insturctions that are required for creating a virtualization machine with virtualization capabilities enabled.
       - use cloud shell commmand to get the details about the account from google compute engine
       - add additional details to the cloud shell command to launch instance using instructions provided.
       - Final cloud shell command with ssh enabled.
         ```
         gcloud compute instances create cmpe283-assignment1 --project=valued-network-366918 --zone=us-central1-a --machine-type=n2-standard-8 --network-interface=network-tier=PREMIUM,subnet=default --metadata=ssh-keys=sirishacyd:ssh-ed25519\ AAAAC3NzaC1lZDI1NTE5AAAAICMdhjaZM4SHxu6BC7LYeX6r6yL48fbF5D\+MFwMU4w5j\ sirishacyd@gmail.com --maintenance-policy=MIGRATE --provisioning-model=STANDARD --service-account=1044074668714-compute@developer.gserviceaccount.com --scopes=https://www.googleapis.com/auth/devstorage.read_only,https://www.googleapis.com/auth/logging.write,https://www.googleapis.com/auth/monitoring.write,https://www.googleapis.com/auth/servicecontrol,https://www.googleapis.com/auth/service.management.readonly,https://www.googleapis.com/auth/trace.append --create-disk=auto-delete=yes,boot=yes,device-name=cmpe283-assignment1,image=projects/debian-cloud/global/images/debian-11-bullseye-v20221102,mode=rw,size=100,type=projects/valued-network-366918/zones/us-central1-a/diskTypes/pd-balanced --no-shielded-secure-boot --shielded-vtpm --shielded-integrity-monitoring --reservation-affinity=any --min-cpu-platform "Intel Cascade Lake" --enable-nested-virtualization
         ```
         ![](screenshots/1.instance_launch.png)
   2. Login to the launched instance using ssh connect from the googlec compute engine instances page.
    ![](screenshots/2.instance_connect.png)

# References
- [https://cloud.google.com/compute/docs/instances/nested-virtualization/enabling#gcloud](https://cloud.google.com/compute/docs/instances/nested-virtualization/enabling#gcloud)
- 
