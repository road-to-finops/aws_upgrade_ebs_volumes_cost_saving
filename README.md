# GP2 to GP3 EBS Volume converter

This python script can be used in one account to change ebs volumes from gp2 to gp3. This will look for volumes that fir the criteria from gp2/io1 that are less than 1TB and 3000 iops and change to gp3 which has a 20% cost reduction.

See manual proccess [here](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/requesting-ebs-volume-modifications.html?trk=el_a134p000006peKgAAI&trkCampaign=AWSInsights_Website_Docs_requesting-ebs-volume-modifications&sc_channel=el&sc_campaign=AWSInsights_Blog_finding-savings-from-2020-reinvent-announcements&sc_outcome=Product_Marketing)

See AWS Blog Post for more info [here](https://aws.amazon.com/blogs/aws-cost-management/finding-savings-from-2020-reinvent-announcements/)

## Run Script
Ensure you are loged into the right account in your terminal. You can do this by setting access keys and using your default profile. See instructions [here](https://docs.aws.amazon.com/cli/latest/userguide/cli-chap-configure.html)

By Default this is a dry run script. If you wish it to be a review then *no* export needed. To make changes you can run
```export DRYRUN=False```
Then to run the review/change
```python gp3.py```
