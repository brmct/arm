# arm-dev
square braces are something that you need to interpolate.
---
*parameters: 7 types
integers
booleans
arrays
strings
securestrings
objects
secureobject

---
*variables are for when you are going to reuse something throughout your template.

an example would be an apiVersion.

--
can deploy any template you create by creating a hash table for the parameters and then passing it as a parameters object:
#define params in hash table
$ParametersObj = @{
storageAccountName = "mystoragename123"
storageAccountType = "Standard_LRS"
}

New-AzResourceGroupDeployment -Name "myStorage_01" -ResourceGroupName "myRG_01" -TemplateFile .\mytemplate.json -TemplateParameterObject $ParametersObj

*Function-Notes:
Common approach is to use a prefix and then append it to a resource type.

concatinate funciton can concatinate anything you need.

a function definition looks like:
"[functionName(parameter1, parameter2]"

square braces used for something that you need to interpolate.

https://docs.microsoft.com/en-us/azure/azure-resource-manager/templates/template-functions

