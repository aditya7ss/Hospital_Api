
# Hospital API

An API created using NodeJS for the doctors of a hospital to cater to the need of the healthcare system during Covid-19.
Tech Stack: Node.js,Postman & Mongo DB


## Root Hosted Link - 
https://hospital-api-6xfd.onrender.com

## Theme
 Task
 - Theme:
 - We’re going to design an API for the doctors of a Hospital which has been allocated by the
 govt for testing and quarantine + well being of COVID-19 patients
 - There can be 2 types of Users
 - Doctors
 - Patients
 - Doctors can log in
 - Each time a patient visits, the doctor will follow 2 steps
 - Register the patient in the app (using phone number, if the patient already exists, just
   return the patient info in the API)
 - After the checkup, create a Report
 - Patient Report will have the following fields
 - Created by doctor
 - Status (You can use enums if you want to):
 - Can be either of: [Negative, Travelled-Quarantine, Symptoms-Quarantine,
   Positive-Admit]
 - Date



## Run Locally

Clone the project

```bash
  git clone https://github.com/aditya7ss/Hospital_Api
```

Go to the project directory

```bash
  cd Hospital-API-For-Covid-19
```

Install dependencies

```bash Buid Command
  npm install
```

Start the server

```bash Run Command
  npm start
```

  
## Documentation


Routes :

   use Post a. /doctors/register - Registers a new Doctor.
   use Post b. /doctors/login - Authenticates and returns the JWT token to be used.
   use Post c. /patients/register - Allows a doctor to register a new patient (JWT Auth enabled).
   use Post  d. /patients/:id/create_report - Allows a doctor to create a patients report (JWT    Auth enabled).
   use Get e. /patients/:id/all_reports - Sends all the reports of a patient oldest to latest. (JWT Auth enabled).
   use Get f. /reports/:status - List of all the reports of all patients with a specific status. (JWT Auth enabled).

Data that needs to be sent with a route :
    
    a. /doctors/register - name, email, password (Form type data)
    b. /doctors/login - email, password (Form type data).
    c. /patients/register - JWT Token (In Headers), name, phone, age, sex, comorbidity status (Form type data).
    d. /patients/:id/create_report - JWT Token (In Headers), Patient's ID (params), status (Form type data).
    e. /patients/:id/all_reports - JWT Token (In Headers), Patient's ID (params).
    f. /reports/:status - JWT Token (In Headers), status (params).


## 🖼️ Screenshots

![Screenshot_20230211_034209](https://user-images.githubusercontent.com/100330745/218295098-4a381a12-d4ac-4843-adce-5cb982dd292b.png)


![Screenshot_20230211_034233](https://user-images.githubusercontent.com/100330745/218295100-412fd3a2-457e-4119-bd1a-b233fdb0481a.png)


![Screenshot_20230211_100631](https://user-images.githubusercontent.com/100330745/218295101-a585bfce-da21-4e07-ab93-36727cdac1af.png)

  
 