# VaccineNotifier
VaccineNotifier checks the cowin portal periodically to find vaccination slots available in your district and for your age. If found, it will send you emails every minute until the slots are available.


<font size="6"> Steps to run the script: </font> 

Step 1) Enable application access on your gmail with steps given here:
https://support.google.com/accounts/answer/185833?p=InvalidSecondFactor&visit_id=637554658548216477-2576856839&rd=1  
\
\
Step 2) Enter the details in the file .env, present in the same folder
\
\
Step 3) Find your districtId and put it at same .env file. To know district Id visit cowin website, right click to open network inspector go to network tab then select your state and district and hit search at webiste. You will notice a network call like 
https://cdn-api.co-vin.in/api/v2/appointment/sessions/public/calendarByDistrict?district_id=395&date=13-05-2021, here 395 is your districtId.
\
\
Step 4) Install node.js.
\
\
Step 5) Install pm2 server if not already. Run "npm install pm2 -g" to install.
\
\
Step 6) On your terminal run: npm i && pm2 start vaccineNotifier.js
\
\
To close the app run: pm2 stop vaccineNotifier.js && pm2 delete vaccineNotifier.js

Here's a sample of the resultant emails:
![image info](./sampleEmail.png)
