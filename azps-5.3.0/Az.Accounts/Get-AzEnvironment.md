---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/get-azenvironment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Get-AzEnvironment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Get-AzEnvironment.md
ms.openlocfilehash: 176874b9d3fbf192597cd98659e45df800dc819c
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98523365"
---
# <span data-ttu-id="b1077-101">Get-AzEnvironment</span><span class="sxs-lookup"><span data-stu-id="b1077-101">Get-AzEnvironment</span></span>

## <span data-ttu-id="b1077-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="b1077-102">SYNOPSIS</span></span>
<span data-ttu-id="b1077-103">Hämta slut punkter och metadata för en instans av Azure-tjänster.</span><span class="sxs-lookup"><span data-stu-id="b1077-103">Get endpoints and metadata for an instance of Azure services.</span></span>

## <span data-ttu-id="b1077-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="b1077-104">SYNTAX</span></span>

```
Get-AzEnvironment [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b1077-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="b1077-105">DESCRIPTION</span></span>
<span data-ttu-id="b1077-106">Med Get-AzEnvironment cmdlet får du slut punkter och metadata för en instans av Azure-tjänsterna.</span><span class="sxs-lookup"><span data-stu-id="b1077-106">The Get-AzEnvironment cmdlet gets endpoints and metadata for an instance of Azure services.</span></span>

## <span data-ttu-id="b1077-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="b1077-107">EXAMPLES</span></span>

### <span data-ttu-id="b1077-108">Exempel 1: skaffa AzureCloud-miljön</span><span class="sxs-lookup"><span data-stu-id="b1077-108">Example 1: Getting the AzureCloud environment</span></span>
```
PS C:\> Get-AzEnvironment AzureCloud

Name       Resource Manager Url          ActiveDirectory Authority
----       --------------------          -------------------------
AzureCloud https://management.azure.com/ https://login.microsoftonline.com/
```

<span data-ttu-id="b1077-109">Det här exemplet visar hur du kan hämta slut punkter och metadata för AzureCloud (standard).</span><span class="sxs-lookup"><span data-stu-id="b1077-109">This example shows how to get the endpoints and metadata for the AzureCloud (default) environment.</span></span>

### <span data-ttu-id="b1077-110">Exempel 2: skaffa AzureChinaCloud-miljön</span><span class="sxs-lookup"><span data-stu-id="b1077-110">Example 2: Getting the AzureChinaCloud environment</span></span>
```
PS C:\> Get-AzEnvironment AzureChinaCloud | Format-List

Name                                              : AzureChinaCloud
EnableAdfsAuthentication                          : False
ActiveDirectoryServiceEndpointResourceId          : https://management.core.chinacloudapi.cn/
AdTenant                                          :
GalleryUrl                                        : https://gallery.chinacloudapi.cn/
ManagementPortalUrl                               : http://go.microsoft.com/fwlink/?LinkId=301902
ServiceManagementUrl                              : https://management.core.chinacloudapi.cn/
PublishSettingsFileUrl                            : http://go.microsoft.com/fwlink/?LinkID=301776
ResourceManagerUrl                                : https://management.chinacloudapi.cn/
SqlDatabaseDnsSuffix                              : .database.chinacloudapi.cn
StorageEndpointSuffix                             : core.chinacloudapi.cn
ActiveDirectoryAuthority                          : https://login.chinacloudapi.cn/
GraphUrl                                          : https://graph.chinacloudapi.cn/
GraphEndpointResourceId                           : https://graph.chinacloudapi.cn/
TrafficManagerDnsSuffix                           : trafficmanager.cn
AzureKeyVaultDnsSuffix                            : vault.azure.cn
AzureDataLakeStoreFileSystemEndpointSuffix        :
AzureDataLakeAnalyticsCatalogAndJobEndpointSuffix :
AzureKeyVaultServiceEndpointResourceId            : https://vault.azure.cn
```

<span data-ttu-id="b1077-111">Det här exemplet visar hur du kan hämta slut punkter och metadata för AzureChinaCloud-miljön.</span><span class="sxs-lookup"><span data-stu-id="b1077-111">This example shows how to get the endpoints and metadata for the AzureChinaCloud environment.</span></span>

### <span data-ttu-id="b1077-112">Exempel 3: skaffa AzureUSGovernment-miljön</span><span class="sxs-lookup"><span data-stu-id="b1077-112">Example 3: Getting the AzureUSGovernment environment</span></span>
```
PS C:\> Get-AzEnvironment AzureUSGovernment

Name              Resource Manager Url                  ActiveDirectory Authority
----              --------------------                  -------------------------
AzureUSGovernment https://management.usgovcloudapi.net/ https://login.microsoftonline.us/
```

<span data-ttu-id="b1077-113">Det här exemplet visar hur du kan hämta slut punkter och metadata för AzureUSGovernment-miljön.</span><span class="sxs-lookup"><span data-stu-id="b1077-113">This example shows how to get the endpoints and metadata for the AzureUSGovernment environment.</span></span>

## <span data-ttu-id="b1077-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="b1077-114">PARAMETERS</span></span>

### <span data-ttu-id="b1077-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b1077-115">-DefaultProfile</span></span>
<span data-ttu-id="b1077-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="b1077-116">The credentials, account, tenant and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b1077-117">-Namn</span><span class="sxs-lookup"><span data-stu-id="b1077-117">-Name</span></span>
<span data-ttu-id="b1077-118">Anger namnet på Azure-instansen som ska visas.</span><span class="sxs-lookup"><span data-stu-id="b1077-118">Specifies the name of the Azure instance to get.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b1077-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b1077-119">CommonParameters</span></span>
<span data-ttu-id="b1077-120">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b1077-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b1077-121">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b1077-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b1077-122">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="b1077-122">INPUTS</span></span>

### <span data-ttu-id="b1077-123">System. String</span><span class="sxs-lookup"><span data-stu-id="b1077-123">System.String</span></span>

## <span data-ttu-id="b1077-124">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="b1077-124">OUTPUTS</span></span>

### <span data-ttu-id="b1077-125">Microsoft. Azure. commands. Profile. Models. PSAzureEnvironment</span><span class="sxs-lookup"><span data-stu-id="b1077-125">Microsoft.Azure.Commands.Profile.Models.PSAzureEnvironment</span></span>

## <span data-ttu-id="b1077-126">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="b1077-126">NOTES</span></span>

## <span data-ttu-id="b1077-127">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="b1077-127">RELATED LINKS</span></span>

[<span data-ttu-id="b1077-128">Add-AzEnvironment</span><span class="sxs-lookup"><span data-stu-id="b1077-128">Add-AzEnvironment</span></span>](./Add-AzEnvironment.md)

[<span data-ttu-id="b1077-129">Remove-AzEnvironment</span><span class="sxs-lookup"><span data-stu-id="b1077-129">Remove-AzEnvironment</span></span>](./Remove-AzEnvironment.md)

[<span data-ttu-id="b1077-130">Set-AzEnvironment</span><span class="sxs-lookup"><span data-stu-id="b1077-130">Set-AzEnvironment</span></span>](./Set-AzEnvironment.md)

