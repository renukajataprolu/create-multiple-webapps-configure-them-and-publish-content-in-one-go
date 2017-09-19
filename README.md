# create-multiple-webapps-configure-them-and-publish-content-in-one-go
This template creates multiple webapps, configures apps and publishes content in one go.
How to use the template

1.Generate input params.json file with requried parameters. Parameters description as follows
      hostingPlanName : App plan which webapps are hosted.
      siteName        : webapp/site name
      packageuri      : Blob Url in which app content is present in blobstorage. Before using this template package should be available in blob storage
    clientCertEnabled : If your webapp requires certificate based authentication set it to true, else false.
clientAffinityEnabled : Affinity to true or false based on your requirement.

How to execute :

e.g.
New-AzureRmResourceGroupDeployment -Name "deployment name,you can give any name" -ResourceGroupName "resource group name" -TemplateParameterFile "path to inputparameters json file"  -TemplateFile "path to template file" -Force
