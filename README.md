# msal-flask-graph

This repo features mainly the code from https://github.com/datamel/msal-flask-graph with some tiny modifications.

Remarks:
- [Article mentioned below can be found here.](https://www.codeproject.com/Articles/5318952/Microsoft-Graph-Authentication-in-Python)
- Register the app in Azure AD as Web app. Redirect URL can be found in the `app_config.py` file.
- OneNote Demo page does not work with personal accounts, due to the scope specified in `app_config.py`. [Notes.Read.All and Notes.ReadWrite.All are only valid for work or school accounts.](https://docs.microsoft.com/en-us/graph/permissions-reference#remarks-14)
- TEAM_ID can be extracted from the Team Link. Open Teams client, click on Teams (left bar), choose … and Get link to team. Use the `groupId` in the URL.

*---ORIGINAL README FORM HERE---*

Python Flask App utilizing Microsoft Authentication Library (MSAL), Microsoft Azure Active Directory and Microsoft Graph

This code accompanies articles written by Mel Hall in which we create a Flask Web App.

Authentication code is based on https://github.com/Azure-Samples/ms-identity-python-webapp

The app asks a user to log in using MSAL for authentication to request a token for accessing the Microsoft Graph API (a unified API for accessing all things Microsoft 365).
We shall make several API calls, retrieving our profile information, OneNote pages and create a Incident Management Bot which can create and manage Teams Channels. 

In addition our app will provide functionality to download our OneNote pages as Markdown.


## Instructions for Use

- Clone the repo.
- Complete the `app_config.py` section. Setup will involve app configuration on Azure Active Directory. Detailed instructions will appear on the article.
- `$ flask run --host=localhost --port=5000`
