# OperatingSystem_Networking_Project
Group Project Submission (Suvrat, Kavyah, Ayati, Kayana)  

## General Instructions for Installation & Execution: 
step1: download the repository as a zipped file and extract the contents of the zip file<br>
step2: open the desired code in jupyter notebook<br> 
step3: in iam dashboard in aws, under quick links, click my security credentials and create an access key and store it safely in computer<br>
step4: create an ec2 instance on aws with basic settings<br> 
step5: under ec2 instance security section, modify the inbound rules for the applied security group (source ssh on all addresses)<br>
step6: create a new iam role with the policy (AmazonSSMManagedInstanceCore) and assign the role to ec2<br>
step7: open the terminal in jupyter notebook in a new tab<br>
step8: pip install boto3<br>
step9: aws configure<br> 
step10: enter details like access key id, secret access key, region, jason(output format)<br>
step11: run the code script cell by cell 

## IPv4 Subnetting 
Given the ip address, first check its class using first octet. Accordingly mention the network to host ratio, default subnet mask and prefix.<br>
Identify the number of host bits available for subnetting. Based on the requirement of specific quantity of host or subnets, find the power of 2 that suffices it.<br.
Remaining bits will be used for other. Let the number of host bits be 'h' and number of subnet bits be 's'.<br>
Total number of subnets: 2^s<br>
Increment factor: 2^h<br>
Total number of usable host per subnet: 2^h - 2<br>
Determine the network id (NID), first usable host (FUH), last usable host (LUH) and broadcast id (BID) for all the subnets.<br>
FUH = NID + 1<br>
BID = next NID - 1<br>
LUH = BID - 1
## Process Schedulling Algorithms
### First Come First Serve (FCFS) [non priority + non pre-emptive]
List processes in the order they arrive. If 2 processes have the same arrival time, give preference to the process with lower process id.<br>
Select the first process in the queue and give it the CPU immediately. ⁠Run the process until completion. FCFS is non-preemptive, so it runs fully.<br>
Move to the next process in arrival order. Repeat until all processes are completed. 
### Shortest Job First (SJF) [priority + non pre-emptive]
List all the arrived processes and note their CPU burst times. Choose the process with the shortest burst time.<br>
If 2 processes have the same burst time, give preference to the process with lower process id. Smallest job gets the CPU first.<br>
Run that process completely as SJF is non-preemptive. Remove the finished process from the list.<br>
Again choose the shortest job from the remaining updated arrived processes. Repeat until all processes are completed. 
### Shortest Remaining Time First (SRTF) [priority + preemptive]
List all the arrived processes and note their CPU burst times. Choose the process with the shortest burst time.<br>
If 2 processes have the same burst time, give preference to the process with lower process id. Smallest job gets the CPU first.<br>
Run the process untill a new process enters ram. Check for the minimum remaining burst time process.<br>
If the process chosen is same, execution continues, else the process get prempted and the newly selected process gets CPU.<br>
Repeat until all processes are completed. 
### Common Metrics 
Turnaround Time (TAT) = CT – AT<br>
Waiting Time (WT) = TAT – BT<br> 
Scheduled Length (SL) = Max(CT) - Min(AT)<br>
Throughput = Total number of processes / Scheduled length 
### Visualisation via Gnatt Chart









