# Fundraising Proposal Assistant

Fundraising Proposal Assistant is a customized experience for the Microsoft Cloud for Nonprofit to allow fundraisers to generate a draft fundraising proposal email that can be edited and sent to prospective donors. The draft proposal is generated by Open AI based on the context of an opportunity, a donor’s profile, interests, and funding priorities in the Microsoft Cloud for Nonprofit.



## Prerequisites

- Dynamics 365 Sales Enterprise.
- Microsoft Cloud for Nonprofit – Fundraising and Engagement https://learn.microsoft.com/en-us/dynamics365/industry/nonprofit/fundraising-engagement-deploy-installer.
- Admin access to Microsoft Power Platform, Microsoft Dynamics 365 or tenant admin.


## API Key

- Log in to your OpenAI account
- Click on your name in the upper right corner and select View API keys from the drop-down menu.
- To get a new secret key, click the Create new secret key button near the center of the page.
- On the create new secret key dialog, enter a name for your API key and click Create secret key.


## Manual Solution Installation

1. Before installing the solution, make sure you have the solution file in your machine. (Select one of the files available on the "Releases" option on the right panel).
2. Go to the maker portal https://make.powerapps.com/.
3. On the top right, select the environment where you want to install the solution.
4. On the left navigation pane, click Solutions and Import solution.
5. Click Import solution.
6. Browse to the location of the solution file downloaded at step 1 and click Next.
7. On the confirmation window click Next.
8. The import process will ask you to reestablish a connection. A connection is needed for the Power Automate Flow that is part of the solution. This connection provides access to the org-based database on Microsoft Dataverse in current environment. If a connection already exists, you can select it from the dropdown and you can jump to step 12. In case there are no connections, Click the dropdown next to the connection reference and click New Connection.
9. A new window will open to create the connection. On the dialog, click Create.
10. Pick an account or log in with an account that has access to the current Dataverse Environment.
11. After creating the connection, go back to the previous window and click Refresh on the dialog shown. That will refresh the connections dropdown.
12. Select the newly created connection from the dropdown next to the connection reference and click Next.
13. Paste your API key from OpenAI on the Environment Variable OpenAI API Key and click Import. (to get an OpenAI API key see section Set up an OpenAI API Key).
14. Wait until the import process completes.

## Utilizing the AI Solution
Fundraisers can reach more prospective donors by quickly drafting personalized fundraising proposals with OpenAI in the Microsoft Cloud for Nonprofit.
With the click of a button, fundraisers can generate a draft fundraising proposal email that can be edited and sent to prospective donors. The draft proposal is generated by Open AI based on the context of an opportunity, a donor’s profile, interests, and funding priorities in the Microsoft Cloud for Nonprofit.

The following guidelines will show how to use the predeveloped solution:
1. Go to your organization’s Dynamics 365 CRM portal (e.g. https://organizationid.crm.dynamics.com).
2. From the list of apps, select the Fundraising and Engagement model-driven app.
3. From the navigation pane, select Opportunities, and open an existing opportunity record.
4. To draft a Fundraising Proposal Letter, click on the **Write Proposal** button inside the opportunity form.
5. A side panel dialog shows, which allows to add more guidance or context before sending the data to OpenAI. Some examples of Additional Guidance for OpenAI include:
    - “The letter should be written as if It was written by John Smith (Fundraising Director of ABC Organization)”.
    -  “The proposal must be written in Spanish”.
6. Once the additional context is added (is optional), click Generate Proposal. After the generation of the proposal completes, the dialog will show a confirmation.
7. The Open Email button allows opening the newly created.

## Developer Notes

- Find instructions on how to deploy Azure OpenAI [here](https://learn.microsoft.com/en-us/azure/cognitive-services/openai/how-to/create-resource?pivots=web-portal).


## FAQ
### Should the assistant use GPT-3.5 or GPT-4?
The app was tested with GPT-3.5 

### Can the assistant use Azure Open AI?
The app functions with both OpenAI or Azure Open AI. The repo currently uses Azure OpenAI. 
[Request access to Azure OpenAI.](https://customervoice.microsoft.com/Pages/ResponsePage.aspx?id=v4j5cvGGr0GRqy180BHbR7en2Ais5pxKtso_Pz4b1_xUOFA5Qk1UWDRBMjg0WFhPMkIzTzhKQ1dWNyQlQCN0PWcu)


