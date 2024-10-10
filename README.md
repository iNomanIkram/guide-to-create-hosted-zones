# Instructions for creating Hosted Zone

## Accounts

There are two accounts available at the moment.

1. **Master account** 
2. **Sub account**    

In `Master` account, hosted zones of type `Public` and `Private` are already present for the domain `sampledomain.com`.

## Steps to creating Hosted Zones in Sub Account

In order to create `Hosted Zones` in `Sub account`. Follow the following steps.

1. Go to Route53 Service.
2. Select `Create Hosted Zone` button.
3. For instance, we are creating hosted zones for specific environments. So the syntex of domain name will look like `<env>.sampledomain.com`. where env can be `dev`,`uat`,`prd` etc. For our case, we will consider it as `uat.sampledomain.com`.
4. Create both `Public Hosted Zone` and `Private Hosted Zone` for above specific / newly created domain.

**Note:** For newly created domain, two records are automatically created for each hosted zone. One record is of Type `NS` and another record is of type `SOA`.

## Add Record in Master account

In order to add record in `Master` account. Following these steps.

1. Go to `Route53`, Select your hosted zone. For our case, its `sampledomain.com`
2. Click on `Create Record`. **Note:** We'll create record for `Public Hosted Zone` only that we have created in `Sub account`
3. In `Quick create record` menu, type the name for record. Since we created hosted zone in `Master` account with domain name `uat.sampledomain.com`. So our record name will also be `uat.sampledomain.com`. 
4. Select type of record as `NS - Name Servers for the hosted Zone` from drop down list.
5. Add `Value` for `Record`. **Note:** Value of the record will be copied from the `Sub account`, for that purpose go to our newly created hosted zone i.e. `uat.sampledomain.com` and copy the value from record of type `NS`.
6. Paste copied value into `Value` field for the record.



