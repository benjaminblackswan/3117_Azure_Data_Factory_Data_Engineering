# 14. Blueprint for the data lake

<img width="1293" height="631" alt="image" src="https://github.com/user-attachments/assets/2a1f135f-d64e-47cb-af02-e2f5dd4eb354" />

# 15. Storage account creation

First create a new **Resource Group** called *3117-rg-orders-dev-austeast-001*

## Create a new blob Storage account

Note that the name must be unique within entire Azure.

use Aus East region, standard performance and LRS redundancy

<img width="824" height="756" alt="image" src="https://github.com/user-attachments/assets/120bc152-0258-4a9c-a72d-4cf7839e27f5" />

Leave Hierarchical Namespace unchecked, otherwise it will turn into **ADLS gen2**

<img width="839" height="247" alt="image" src="https://github.com/user-attachments/assets/277f7d29-467e-479b-83ed-4815ee792da9" />


keep access tier Hot

<img width="843" height="131" alt="image" src="https://github.com/user-attachments/assets/da45685c-d395-4ed0-a12e-cf7b4b5fd855" />

In networking section, leave public network access Enable

<img width="828" height="235" alt="image" src="https://github.com/user-attachments/assets/f3bf319b-edc7-4f33-b4fd-f2e545492734" />

click **Create**

Now you should see the new storage account in the resource group

<img width="1143" height="447" alt="image" src="https://github.com/user-attachments/assets/3de7e155-8477-4a54-a6e8-f3cf6f4952f5" />

## Create a new datalake Storage account

The process is the same except that we must check **Enable hierarchical namespace**

<img width="851" height="298" alt="image" src="https://github.com/user-attachments/assets/cf259a6f-0e30-458d-90d8-aad23e7122fe" />

Now we should have two Storage Account

<img width="1497" height="503" alt="image" src="https://github.com/user-attachments/assets/7242ca6d-ccd9-480d-b039-a7fc5ab86a6d" />

# 16. Container Creation and File Upload

## create container in storder000111

<img width="622" height="351" alt="image" src="https://github.com/user-attachments/assets/38fd0a41-a48a-4ee2-b1c1-1201e724fab4" />

To add containers to a **storage account**

<img width="601" height="679" alt="image" src="https://github.com/user-attachments/assets/1db2a8ea-7058-4186-b040-39487743d10a" />

create a **container** called *landing*

then upload files


<img width="1682" height="442" alt="image" src="https://github.com/user-attachments/assets/bc1df53c-5c4f-4c02-ad87-798009bd8a18" />

because we had turned on **soft delete** when we created our storage account, if we delete a file, it will be retained for the retention period.

<img width="1457" height="388" alt="image" src="https://github.com/user-attachments/assets/f1ce006b-c3d0-4a84-8b76-24194d231cdb" />


## create container in dlorders000111

create four containers, raw, cleansed, structured and analytics

<img width="1690" height="414" alt="image" src="https://github.com/user-attachments/assets/39781ead-b35d-45ff-a6e3-2259fa199a7c" />

















































