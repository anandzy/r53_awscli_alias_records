### r53_awscli_alias_records
### This repo have the policy &amp; awscli input file format to update(UPSERT) the changed ip address for the machine.
### The above policy is used to upsert(update) the changed ip or value to the 'Alias' records in R53.
### AWS simply confused me by keeping the Hosted Zone ID:ZXXXXXXXXX beside the alias records inside the Hosted Zone.
` aws route53 list-hosted-zones-by-name | jq`
` aws route53 change-resource-record-sets --hosted-zone-id Z1E5QYKGMFGDPA --change-batch file://r53.json`
### To execute above commands and get the host-none id you need to get "AmazonRoute53AutoNamingFullAccess" policy for the U/G   
### To invalidate(update) the objects to cdn from the s3 bucket the below command with invalidate.json
### get the list of distribution list with below command
`aws cloudfront list-invalidations --distribution-id ECGOJT7XCZQJV`
### create invalidation request 
### Before creating the new validation id from the below command with the given file.json, Its important to change the callerreference and some new comment.
`aws cloudfront create-invalidation --distribution-id ECGOJT7XCZQJV --invalidation-batch file://invalidate_cdn.json`

**Dont confuse with hosted zone id in Alias attributes.**
