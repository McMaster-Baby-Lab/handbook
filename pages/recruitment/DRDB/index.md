---
layout: default
title: DRDB
parent: Recruitment
nav_order: 3
permalink: /DRDB
has_children: true
---

# Developmental Research Database (DRDB) System

{: .no_toc }

## Table of contents
{: .no_toc .text-delta }

* TOC
{:toc}

---

## What is the DRDB system?

The Developmental Research Database (DRDB) system is a web-based application focusing on managing developmental research. Developmental research relies on the successful management of relations between research projects, research personnel, and families from our communities. For example, researchers need to constantly maintain their participant pool by registering new families, updating existing family info, and tracking their participation history. We also need to manage our research projects and research staff assignments to ensure our projects can be implemented flawlessly.

The success of developmental research involves enormous efforts in managing complex relations among families, labs, research personnel, and projects. Extensive interactions among the stakeholders (e.g., participant recruitment and communicating experimenters) often impose significant challenges to the efficiency of research progress. Despite advancements in technology, a great proportion of developmental labs still rely on manual approaches to manage their research activities, which are both inefficient and prone to human errors. Furthermore, popular research management software is unable to streamline the entire process of developmental research, from scheduling to managing study activities.

To assist the complicated management work in developmental research, we developed the DRDB system. It stores information about research participants, research projects, research personnel, and study schedules with an industry-recognized database standard (MySQL). In addition to storing critical research data, the system is equipped with advanced algorithms, which can automate study schedule management and facilitate communication between families and researchers. The web-based design enables the system can be accessed by multiple researchers from different labs wherever they are whenever they want. This is especially useful during times when we must work remotely.


## What's in the DRDB system?

DRDB includes 3 major categories of data:
- family & children's demographic information
- lab relation information, including studies, lab members, and lab info
- study appointment information, such as appointment time and related experimenters


<figure>
    <img src="../../../assets/images/DRDBDataStructure.png" alt="DRDB Structure" align="center" width="1024"/>  
    <figcaption>A schematic display of data structure and relatons in DRDB.</figcaption>
</figure>

<!-- ## How does the DRDB system help recruitment and research management? -->

## Access to DRDB

DRDB can be accessed here (must be connected to McMaster VPN if not on McMaster Wifi): [Developmental Research Database](https://drdb.mcmaster.ca/#/)



{: .highlight}
> Move the following contents into subpages.

Watch the second half of this video for a tutorial on DRDB: [DRDB Tutorial](https://mcmasteru365.sharepoint.com/sites/labtest/Shared%20Documents/Forms/AllItems.aspx?id=%2Fsites%2Flabtest%2FShared%20Documents%2FTraining%2FRecordings%2FRecruitment%20%26%20DRDB%20Training%2D20220525%5F180343%2DMeeting%20Recording%2Emp4&parent=%2Fsites%2Flabtest%2FShared%20Documents%2FTraining%2FRecordings)



#### **How to check a child’s participation history**

1. Navigate to the _Family Information_ page
2. Search for the family
3. Look at the list of participation records or the summary figure
4. Use the actions to…

- Schedule a participant using the calendar icon
- Indicate a no-show using the face icon
- Reschedule the appointment using the clock icon
- Cancel the appointment using the circle icon

![8](https://github.com/McMaster-Baby-Lab/handbook/assets/132396918/70652c12-6b9f-42de-a5d2-831c8ec903bc)


### Scheduling Studies

#### **How to see eligible families for a study**

1. Navigate to the _Schedule Studies_ page
2. Select the name of the study from the studies drop-down menu
3. View the phone script and switch to the study info tab to see the summary, study type, main contact and study criteria
4. Navigate through eligible families for that specific study using the arrows at the top of the screen

![11](https://github.com/McMaster-Baby-Lab/handbook/assets/132396918/38b2db3b-8721-4f08-be13-cb8f8d5af4ad)



#### **If a family is interested but doesn’t commit to a time…**

1. Navigate to the _Schedule Studies_ page
2. Select the _Schedule a Study for this Child_ drop down menu
3. Select _interested_
4. Click on the mail icon, and then click _confirm a tentative appointment_.

- This button will generate an email template to determine the family’s interest.

5. Proofread the generated email and select _send email_
6. Select next to proceed to the _next contact_ tab. You can now select when you wish to contact the family again (default 2 days).
7. Select _complete_ to finish this process.

- The participant’s participation status will now show as TBD meaning to be determined.

![14](https://github.com/McMaster-Baby-Lab/handbook/assets/132396918/ad86a9e8-539c-481e-b2db-67adb33fe34a)

#### **If a family does not answer the call…**

1. Navigate to the _Schedule Studies_ page
2. Select the _Schedule a Study for this Child_ drop down menu
3. Select _leave a message_
4. Click on the mail icon to _confirm a tentative appointment_
5. Review and send the follow-up email
6. Set the reminder for the next contact date.

![15](https://github.com/McMaster-Baby-Lab/handbook/assets/132396918/6a6f6223-7b84-42e4-932f-9910a0f0613d)

#### **If a family is not interested in participating…**

1. Navigate to the Schedule Studies page
2. Select the _Schedule a Study for this Child_ drop down menu
3. Select rejected and then select the shrugging person icon.
4. Set a reminder for the next contact to determine whether the participant is interested in participating in future studies.
5. Click _complete_ to finish the process

![16](https://github.com/McMaster-Baby-Lab/handbook/assets/132396918/897151d4-5177-4f44-8d4a-32c56f66390b)



#### **How to send a thank you email**!

1. Navigate to the _Study Appointments_ page
2. Search for family/study appointments
3. Click the heart beside the participant to send a thank you email

![22](https://github.com/McMaster-Baby-Lab/handbook/assets/132396918/b60c352e-50a1-47f7-941f-646ba162f1a5)

### Study Management

#### **View study information**

1. Navigate to the _Study Management_ page
2. Click on the abbreviation for the study on the left side to see a summary of the study and phone scripts for contacting participants.
3. Below, the main researchers for the study will be listed with contact information.

![23](https://github.com/McMaster-Baby-Lab/handbook/assets/132396918/ac51bf02-9095-4122-ae2b-68c69b2e3bac)

#### **How to view the email templates for a study**

1. Navigate to the _Study Management_ page
2. Click on the abbreviation for the study on the left side
3. Click preview email templates

![24](https://github.com/McMaster-Baby-Lab/handbook/assets/132396918/7c97b845-3ba1-4ad6-942e-1ad6b5b45ed2)

#### **Edit Study Information**

1. Navigate to the _Study Management_ page
2. Click on the abbreviation for the study on the left side
3. Click _edit study info_

- When you click on this button, there is a link to a document including instructions on how to set up the email templates.

4. Make the desired changes and select save

![25](https://github.com/McMaster-Baby-Lab/handbook/assets/132396918/7eff087c-4fb1-4731-8379-070839617836)

#### **Add a study**

1. Navigate to the _Study Management_ page
2. Click + under the names of the studies
3. Need to add name, type, experimenter, and criteria at minimum
4. Click the instructions button to see how to set up email templates
5. Hit save

![26](https://github.com/McMaster-Baby-Lab/handbook/assets/132396918/eba1ed60-fb43-4535-8c78-fc8e0948ec1a)

#### **Delete a study**

1. Navigate to the _Study Management_ page
2. Click on the abbreviation for the study on the left side
3. Select _delete_ on the right side
4. Hit _confirm_

![27](https://github.com/McMaster-Baby-Lab/handbook/assets/132396918/73fd685c-361e-40ed-9419-cc55fdf54bab)

### Research Personnel

#### **View Lab Members/See assigned studies**

1. Navigate to the _Personnel Management_ page
2. Search for the lab member using full or partial information
3. Select the lab member’s name
4. Assigned studies will appear under the member’s name

![28](https://github.com/McMaster-Baby-Lab/handbook/assets/132396918/31d460b9-d2e3-4a5e-b9ed-99b5d62c7ffe)







## Sharepoint

Sharepoint stores all of the data and documents for the lab. The sharepoint can be accessed using this link: [Sharepoint](https://mcmasteru365.sharepoint.com/sites/labtest)
