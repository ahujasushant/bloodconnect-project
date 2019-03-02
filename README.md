# bloodconnect-project
This repository is for making an application of BloodConnect Foundation

*About BloodConnect*
BloodConnect is one of India's largest a youth run initiative in the field of voluntary blood
donation, which works to tackle the problem of blood shortage in the country. Established in
2010, we have organized more than 300 blood donation camps, handled more than 7000
helpline, and organised more than 150 awareness sessions thereby helping save over 1,50,000
lives. We at BloodConnect believe that the youth combined together can solve this problem.
We have worked with over 75 colleges across 20 different cities to ensure that the youth puts
up a united front and can become a stakeholder in the process. BloodConnect has three (3)
main spheres, namely:
1. Blood Donation Camps: BloodConnect organises blood donation camps with colleges,
residential societies and corporate houses. It is pertinent to note that BloodConnect
only collaborates with government hospitals for carrying out the process of blood
donation as we believe that government blood banks have 70% patients below poverty
line or those who cannot afford private blood banks. In Delhi, we regularly organise
blood donation camps with AIIMS, RML, DDU, Hindu Rao, Safdarjung Hospital amongst
other blood banks.
2. Helpline: BloodConnect operates an emergency helpline system wherein a person in
dire need can contact us and we try to provide them with blood donors. The database of
donors is collected from the blood donation camps organised by BloodConnect and used
in emergency requests.
3. Awareness: BloodConnect regularly organises awareness sessions to remove the myths
of potential donors thereby trying to increase the number of voluntary blood donations
through innovative means. BloodConnect has come up with innovative ideas like street
plays, PPT sessions, scribbling donor experiences, etc. to engage potential donors and
thereafter to enrich the donor experience so that the person associates with the cause
in the long run.


# What are we looking for?
A central remote database of:
1. Donors (sorted on the basis of city > bloodgroup > locality > donor rating)
2. All the helpline, camps, and awareness requests
3. Documentation of help camps, awareness sessions, and handles requests.
These databases should be updated in real time through app and our website

# Application requirements
We are planning to get 2 apps developed.

# 1. For public: 
This app will be used by common public, where they can sign up and login. This app
will have features for:
	a. About BloodConnect: Our general info
	b. Donate Blood: If donor wants to donate a blood on a certain day, we will get the notification
	(mail on a particular ID or user on the volunteer app) for that so that we can send him for
	emergency requests
	c. Raising helpline request: This feature fill collect information on a form and send mail to the
	specific google groups according to the city user has selected in a specified format. (We will
	provide content of form, mail ID list and format of the mail)
	d. Raising camp request: Specifics same as helpline request but content will be different.
	e. Raising awareness request: Specifics same as helpline request but content will be different.
	f. Donation/Collaborating with us: User will provide his contact details which will be mailed to
	specific IDs
	g. Social Media links of BloodConnect
	h. Contact us: Send the user contact details and his query to the specific mail IDs.
	i. App will give notification for awareness purposes, like facts and quotes
	This App will ask user if he wants to register as an emergency donor when he/she will sign
	up and if he/she select yes, it will prompt user to fill up a from and his data will be saved in
	database
	
Page Structure for this App:
1. Logo
2. Login/Signup
3. Home page with About BloodConnect as default page and with following tabs
Tabs
1. Donate Blood - if user has already registered, prompt the user to select the city he is in and
contact details and send a mail to specific IDs. If not registered as donor, prompt the user to
fill up the form and send the mail.
2. Raise a Request - Helpline form; send mail to the city; send a confirmation mail to requester
3. Organize a camp - Camp form; send mail to the city group; send a confirmation mail to
requester
4. Organize an Awareness Session - Camp form; send mail to the city; send a confirmation mail
to requester
5. Donate to BloodConnect – Ways of donation
6. Social Media links
7. Contact us – Prompt user to enter his general info and his query and send the mail.
 

# 2. For Volunteers: #
This app will be used by volunteers to handle the work of BloodConnect. This
app will have following features:
	a. Helpline, Camp and awareness interface for each city
	b. Hierarchical Role Structure
	- VP Tech (Full Admin access, making accounts for volunteers, and changing roles of
	users)
	- Board Members (Access to all department)
	- City Presidents (Access to camp, awareness and helpline of respective city)
	- Camp, helpline, awareness VPs and managers (Access to their departments of their city)
	- Volunteers of every city

Page Structure for Volunteer App:
1. Logo Page
2. Login page – Login credential will be created and role will be assigned by VP Tech (admin); a user
with higher roles can revoke the roles of lower one and can remove them too.
3. Select city
4. After this the display for each of the city will have separate but same function which are
mentioned below

The functionalities of this app separate for each city would be:
1. Camps Department:
- Camp VP or manager can add a camp after confirming with organizer and hospital
- All active camps can be seen in the camp section and a volunteer can click on any camp
and there will be button for where he can select ‘In for the day’, ‘in for the first slot’, ‘in
for the second slot’ or a custom message.
- No of people who have already volunteered should be displayed with the camp
- After the camp is done, we ask donors if they want to be a part of our emergency
donors and collect their data on separate google sheets. This app will have an option to
add the donor directly to the central database.
- After completing all the after-camp work, manager or VP can end this camp so and its
data will be saved in database and it will no longer be displayed in the camp section
2. Awareness Department: Its functionalities will be same as camps
3. Helpline Department:
- VPs can add a helpline request which has been mailed to the google group with options
- All the current helplines will be displayed shown in this section and a volunteer can click
on this, so its complete information is opened, and he/she will have options for
‘Handling’. As soon as someone click on handling a single tick will be displayed so that
remaining volunteers can go for other requests
- After handling, volunteers will have option for saying ‘Request Verified’ and custom
messages for updating info. After saying verified app will display two ticks
- After donation, volunteers will have option for closing requests and filling the Master
Spreadsheet form which stores all the info for the request that are being handled.
- After this, volunteer will have the option to update data for donor who has donated
blood.
- Helpline manager and VP will have option to End a request after it has been closed by
the volunteer, after that helpline request will not be visible to the volunteer and its data
will be saved.
4. Donor Search
- A volunteer can enter locality, bloodgroup, urgency and app will retrieve the data for donor one by one (who have not donated in last three months) and volunteer will call the donor. If donor agrees to donate, he can mark that donor with helpline number so that other volunteers do not call the same donor for other requests. If donor cannot donate blood due to circumstances, volunteer will have an option to update data and donor rating
- Donor will be retrieved according to their rating (5stars for very urgent cases) and also randomly if volunteer do not mention urgent.
