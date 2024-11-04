# Cosmos DB VS Code Extension for NoSQL API Bug Bash Instructions

For the purposes of this bug bash, we will focus on testing the following key features of the VS Code Extension: 
- Query Editor
- CRUD Documents
- View documents table/treeview/json
- Download data from query
- Upload query

Please report any bugs found during testing [here.](https://msdata.visualstudio.com/ba574a88-a171-48e0-8fcb-5fef6d23739c/_workitems/create/Bug?templateId=b2e99ad5-c743-44fc-8d99-c10f6e19997c&ownerId=53949023-eaac-440a-ae64-84428a77f43e)


## Prerequisite
To begin, if you do not already have a sample Cosmos DB NoSQL API account, please follow these instructions for creating an account and inserting sample data.

1. Go to the Azure portal and create a Cosmos DB NoSQL account.
2. Then navigate to the Data Explorer to query the resource.
3. Select "Launch Quickstarts" to insert a new database, container, and sample data.
<img width="1190" alt="image" src="https://github.com/user-attachments/assets/342a8b91-6a4e-49e7-abe0-6fe430b9d74e">

## How to install the extension

To manually install the Visual Studio Code (VS Code) extension from a VSIX file, you can do the following:
Download the latest VS Code Extension Release: vscode-cosmosdb-0.23.1-alpha-PrPr-25.10.2024 
1. Click the Extensions icon at the bottom of the Activity Bar
2. Click the More button in the top right corner of the Extensions view
3. Select Install from VSIX
4. Select the VSIX file in the file browser or in your downloads folder.
5. Click Install
6. Click Reload to activate the extension

*Note*: Auto-updates for extensions installed via VSIX should be disabled by default.

## Authenticating via Entra ID
We recommend you use Microsoft Entra ID when accessing your Azure Cosmos DB resources (instead of account keys) for the most secure authentication method. Once you're signed into Azure, In the Azure tree view, drill down to the collection you'd like to access and right-click on the resource to open the Query editor experience.

![image](https://github.com/user-attachments/assets/d4d02dc3-8db3-4317-8574-5825af3e8442)


### Scenario 1: Inserting data 
Insert a sample dcoument into the previously created resource.
```javascript
{
    "id": "<Replace with ID>",
    "categoryId": "26C74104-40BC-4541-8EF5-9892F7F03D72",
    "categoryName": "Components, Saddles",
    "sku": "SE-R581",
    "name": "LL Road Seat/Saddle",
    "description": "The product called \"LL Road Seat/Saddle\"",
    "price": 27.12,
    "tags": [
        {
            "id": "0573D684-9140-4DEE-89AF-4E4A90E65666",
            "name": "Tag-113"
        },
        {
            "id": "6C2F05C8-1E61-4912-BE1A-C67A378429BB",
            "name": "Tag-5"
        },
        {
            "id": "B48D6572-67EB-4630-A1DB-AFD4AD7041C9",
            "name": "Tag-100"
        },
        {
            "id": "D70F215D-A8AC-483A-9ABD-4A008D2B72B2",
            "name": "Tag-85"
        },
        {
            "id": "DCF66D9A-E2BF-4C70-8AC1-AD55E5988E9D",
            "name": "Tag-37"
        }
    ],
    "_rid": "Kw4GAOs6tq8BAAAAAAAAAA==",
    "_self": "dbs/Kw4GAA==/colls/Kw4GAOs6tq8=/docs/Kw4GAOs6tq8BAAAAAAAAAA==/",
    "_etag": "\"41071826-0000-0800-0000-672894c90000\"",
    "_attachments": "attachments/",
    "_ts": 1730712777

```

### Scenario 2: Querying data 
- Query your data using these starter sample queries. Feel free to test the query editor by writing your own queries!

```javascript
SELECT * FROM c
```

### Scenario 3: Upload sample query

- Upload and run the following sample query.


### Scenario 4: View query perfomance

- Identify how many RUs it took to run the previous query.

### Scenario 5: Download results

- Download results of your previous query as a CSV or json.


### Scenario 6: Viewing results

- Display the results of your query in tree, table, and JSON view.

### Scenario 7: Edit data

- In table view, edit one of your documents and save the changes.
- Verify the changes propgated to your container by querying for the change made.

### Scenario 8: Delete Document
- In tableview, delete any selected document.
- Verify the changes propgated to your container by querying for the document.
- Zero results should be returned.










