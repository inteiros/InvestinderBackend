![](https://i.imgur.com/9jz2SKD.png)

Back-end application for InvesTinder!

InvesTinder is an application developed by João Gabriel Eler Mendes and Victor Lomba in JavaScript using ReactJS to compete in a Hackaton.

This application lets investors connect easily with consultants or advisors, leting them match if they like each other's profile and then providing contact information.

InvesTinder is still on development, so many other features might be added later.

## Usage

After installing all dependencies with yarn or npm i, you can run the back-end with

```bash
node src/index.js
```

## Info

The Back-end application was developed using Node.js, and its responsible for the communication with the database and the services such
as liking, matching, listing users, creating accounts and logging in.

The currently used database is SQLite3, and this application will be deployed using PostgreSQL later on. 

## Routes 

***/login*** : this route requests a registered email and password as body and generates a Json Web Token to create a session in the app.

***/profile/investidor*** : Requests all the fields to create an account as an investor, but the only obligatory ones are email, password and name.

***/profile/consultor*** : Creates an account as an consultant or as an advisor.

***/profile/investidor/list*** : Requests the logged investor ID and returns a profile that he didnt like yet.

***/profile/consultor/list*** : Requests the logged consultant/advisor ID and returns a profile that he didnt like yet.

***/profile/investidor/:TargetId/like*** : The logged investor likes the consultant/advisor that has the ID on the params.

***/profile/consultor/:TargetId/like*** : Consultant/advisor likes the investor.

***/profile/investidor/:TargetId/dislike*** : Investor disliking Consultant/advisors.

***/profile/consultor/:TargetId/dislike*** : Consultant/advisor disliking investors.

***/profile/investidor/matches*** : List all the matches from an investor.

***/profile/consultor/matches*** : List all the matches from a consultant/advisor.
