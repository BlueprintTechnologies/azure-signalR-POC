# Blueprint Azure SignalR Quickstart Accelerator

### Background
Azure SignalR Service is an Azure managed service that helps developers easily build web applications with real-time features. We put this accelerator together while evaluating SignalR for use in real-time dashboard updating (no refresh required). This accelerator is a revision and improvement upon the tutorial provided by Microsoft at https://docs.microsoft.com/en-us/azure/azure-signalr/signalr-quickstart-azure-functions-javascript.

NOTE: We highly recommend reviewing the tutorial. This quickstart is intended for local development only.


### Prerequisites

An Azure account with an active subscription. If you don't already have an Azure account, create an account for free.

[Azure Functions Core Tools, version 2 or above](https://github.com/Azure/azure-functions-core-tools#installing). Used to run Azure Function apps locally.

Node.js, version 10.x. Tested with the most current version but the Azure Core Tools did not work properly. For instructions on how to run multiple versions of Node, check out [this tutorial](https://chamikakasun.medium.com/how-to-manage-multiple-node-versions-in-macos-2021-guide-5065f32cb63b).

### Build Steps
1. Clone repo

2. Create a local.settings.json in the root, with the following content:
`{
  "IsEncrypted": false,
  "Values": {
    "FUNCTIONS_WORKER_RUNTIME": "node",
    "AzureWebJobsStorage": "<Connection string for an Azure Blob storage account>",
    "AzureSignalRConnectionString": "<Connection string for an Azure SignalR account>"
  },
  "ConnectionStrings": {}
}`

3. Run `func start`.

4. Win.
