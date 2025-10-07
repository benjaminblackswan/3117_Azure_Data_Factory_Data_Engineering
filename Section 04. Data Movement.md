# 22. Copy Activity Overview

<img width="1191" height="980" alt="image" src="https://github.com/user-attachments/assets/5fd938bb-cc32-4403-86b6-beea7882c9fc" />

# 24. Copy Activity - Order Items Part 1 (Linked Services and Source/Sink Datasets)

the goal is to move files from the *landing* container in blob storage to the *raw* container in DL.

Create a Linked service to blob storage

<img width="1651" height="566" alt="image" src="https://github.com/user-attachments/assets/0de05313-2cd4-4d5b-9d23-2294d20ea62e" />

<img width="691" height="917" alt="image" src="https://github.com/user-attachments/assets/419d6cd6-0361-4450-975e-0e4d9fda8524" />

create a second linked service to the adls gen 2

## create datasets

<img width="355" height="414" alt="image" src="https://github.com/user-attachments/assets/6c09c090-3a85-4d3a-9c5d-b922e023fa13" />


# 25. Copy Activity - Order Items Part 2 (Copy Activity and Pipeline)

first create a new **pipeline**

<img width="497" height="240" alt="image" src="https://github.com/user-attachments/assets/67e623da-2eca-40db-a071-46e241f35cea" />

give the pipeline a name

search for Copy data under Move and transform

<img width="1212" height="734" alt="image" src="https://github.com/user-attachments/assets/2aa4c8ed-3a24-4ce3-a387-3a7aa8322510" />

enter the following General information about the copy data

<img width="652" height="930" alt="image" src="https://github.com/user-attachments/assets/ab0adcbd-cb35-45fb-a105-1bddd94fed3c" />

<img width="990" height="442" alt="image" src="https://github.com/user-attachments/assets/5d4dafe2-1de2-4a73-a4b3-1cc9d8cbb251" />

Sink = destination 

<img width="864" height="422" alt="image" src="https://github.com/user-attachments/assets/80357c38-ac20-4b02-9e10-f035e83ac1c6" />

Validate > Publish (to save) > Debug (to run)

<img width="1524" height="895" alt="image" src="https://github.com/user-attachments/assets/795486e3-ea7c-4872-b6f8-ca171251e2c0" />


Pipeline ran

<img width="1269" height="699" alt="image" src="https://github.com/user-attachments/assets/36c922a7-860f-4f4e-a917-0113fb8215d0" />

hover over the binoculas to see details

<img width="491" height="282" alt="image" src="https://github.com/user-attachments/assets/1238d142-5728-4960-8882-e940d10030aa" />


<img width="1117" height="680" alt="image" src="https://github.com/user-attachments/assets/966dec9c-6f86-46c3-a553-77f5d265aafa" />

## see cost

Go to Monitor > pipeline > hover over pipeline name > Consumption

<img width="1058" height="412" alt="image" src="https://github.com/user-attachments/assets/76a52a17-d3a2-4bc7-840f-086d19ddc088" />

<img width="628" height="498" alt="image" src="https://github.com/user-attachments/assets/08614c2f-d169-4c4f-aff2-ee5611a81bc4" />

pipeline pricing https://azure.microsoft.com/en-us/pricing/details/data-factory/data-pipeline/

this run costed $0.02 AU

check the raw container in datalake, the copy is successful.

<img width="1376" height="427" alt="image" src="https://github.com/user-attachments/assets/7c943eea-60f5-447c-91f1-eb984cc596bf" />



# 26. Copy Activity - Customers JSON
<img width="1004" height="288" alt="image" src="https://github.com/user-attachments/assets/5fb24070-0907-4cd9-8fc6-c46a30ca9882" />




# 29. Organising Data Factory Objects in Folders


We now have 10 datesets

<img width="320" height="598" alt="image" src="https://github.com/user-attachments/assets/7e6ab64c-c732-4382-b8bf-e58281dda5c8" />

time to organise them, create folders


<img width="456" height="107" alt="image" src="https://github.com/user-attachments/assets/b967c467-c426-4616-8306-7986f54f3726" />


<img width="309" height="107" alt="image" src="https://github.com/user-attachments/assets/1cf65f4d-e42b-431d-a4d4-a35579559a0d" />


Move all Copy activities from all other pipelines into *pl_orders_landing_to_raw* pipeline, then delete all other pipelines and keep only  *pl_orders_landing_to_raw* pipeline.

<img width="1258" height="528" alt="image" src="https://github.com/user-attachments/assets/0b11535c-4c7a-4d79-8694-148515a35788" />

validate, publish and debug (VPD)


# 30. Chaining Activities

chain all the activities in the *pl_orders_landing_to_raw* pipeline together on success completion of the previous activitity.

<img width="1250" height="255" alt="image" src="https://github.com/user-attachments/assets/61cffa38-ea54-4e3a-913e-00d0d78494ed" />

## Create an error on purpose

<img width="1008" height="711" alt="image" src="https://github.com/user-attachments/assets/4ce9fa12-6662-43e6-bc6e-e727384c1004" />

click on Copy Orders activity,

<img width="1008" height="711" alt="image" src="https://github.com/user-attachments/assets/59da274f-411b-4e2e-a63e-f04f081ac6e6" />

validate the debug

<img width="1354" height="591" alt="image" src="https://github.com/user-attachments/assets/27a31d9e-b7a8-4e36-b8fe-58e599f35452" />


the pipeline is stopped.


# 31. Working with Multiple Files as a Source and Copy Behaviour
