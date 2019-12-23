# r53_awscli_alias_records
This repo have the policy &amp; awscli input file format to update(UPSERT) the changed ip address for the machine.

#The above policy is used to upsert(update) the changed ip or value to the 'Alias' records in R53.
#AWS simply confused me by keeping the Hosted Zone ID:ZXXXXXXXXX beside the alias records inside the Hosted Zone.
#aws route53 list-hosted-zones-by-name | jq #get the hosted name ID 
#To execute above commands and get the host-none id you need to get "AmazonRoute53AutoNamingFullAccess" policy for the      u user/group.
****Dont confuse with hosted zone id in Alias attributes.*****
