---
external help file: Microsoft.Azure.Commands.Profile.dll-Help.xml
Module Name: AzureRM.Profile
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.profile/get-azurermenvironment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Get-AzureRmEnvironment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Get-AzureRmEnvironment.md
ms.openlocfilehash: ef42490d18702682413fd2c0a19e301614ce4d94
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93576833"
---
# <span data-ttu-id="25cab-101">Get-AzureRmEnvironment</span><span class="sxs-lookup"><span data-stu-id="25cab-101">Get-AzureRmEnvironment</span></span>

## <span data-ttu-id="25cab-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="25cab-102">SYNOPSIS</span></span>
<span data-ttu-id="25cab-103">Hämta slut punkter och metadata för en instans av Azure-tjänster.</span><span class="sxs-lookup"><span data-stu-id="25cab-103">Get endpoints and metadata for an instance of Azure services.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="25cab-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="25cab-104">SYNTAX</span></span>

```
Get-AzureRmEnvironment [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="25cab-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="25cab-105">DESCRIPTION</span></span>
<span data-ttu-id="25cab-106">Med Get-AzureRmEnvironment cmdlet får du slut punkter och metadata för en instans av Azure-tjänsterna.</span><span class="sxs-lookup"><span data-stu-id="25cab-106">The Get-AzureRmEnvironment cmdlet gets endpoints and metadata for an instance of Azure services.</span></span>

## <span data-ttu-id="25cab-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="25cab-107">EXAMPLES</span></span>

### <span data-ttu-id="25cab-108">Exempel 1: skaffa AzureCloud-miljön</span><span class="sxs-lookup"><span data-stu-id="25cab-108">Example 1: Getting the AzureCloud environment</span></span>
```
PS C:\> Get-AzureRmEnvironment AzureCloud

Name       Resource Manager Url          ActiveDirectory Authority
----       --------------------          -------------------------
AzureCloud https://management.azure.com/ https://login.microsoftonline.com/
```

<span data-ttu-id="25cab-109">Det här exemplet visar hur du kan hämta slut punkter och metadata för AzureCloud (standard).</span><span class="sxs-lookup"><span data-stu-id="25cab-109">This example shows how to get the endpoints and metadata for the AzureCloud (default) environment.</span></span>

### <span data-ttu-id="25cab-110">Exempel 2: skaffa AzureChinaCloud-miljön</span><span class="sxs-lookup"><span data-stu-id="25cab-110">Example 2: Getting the AzureChinaCloud environment</span></span>
```
PS C:\> Get-AzureRmEnvironment AzureChinaCloud | Format-List

Name                                              : AzureChinaCloud
EnableAdfsAuthentication                          : False
ActiveDirectoryServiceEndpointResourceId          : https://management.core.chinacloudapi.cn/
AdTenant                                          :
GalleryUrl                                        : https://gallery.chinacloudapi.cn/
ManagementPortalUrl                               : https://go.microsoft.com/fwlink/?LinkId=301902
ServiceManagementUrl                              : https://management.core.chinacloudapi.cn/
PublishSettingsFileUrl                            : https://go.microsoft.com/fwlink/?LinkID=301776
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

<span data-ttu-id="25cab-111">Det här exemplet visar hur du kan hämta slut punkter och metadata för AzureChinaCloud-miljön.</span><span class="sxs-lookup"><span data-stu-id="25cab-111">This example shows how to get the endpoints and metadata for the AzureChinaCloud environment.</span></span>

### <span data-ttu-id="25cab-112">Exempel 3: skaffa AzureUSGovernment-miljön</span><span class="sxs-lookup"><span data-stu-id="25cab-112">Example 3: Getting the AzureUSGovernment environment</span></span>
```
PS C:\> Get-AzureRmEnvironment AzureUSGovernment

Name              Resource Manager Url                  ActiveDirectory Authority
----              --------------------                  -------------------------
AzureUSGovernment https://management.usgovcloudapi.net/ https://login.microsoftonline.us/
```

<span data-ttu-id="25cab-113">Det här exemplet visar hur du kan hämta slut punkter och metadata för AzureUSGovernment-miljön.</span><span class="sxs-lookup"><span data-stu-id="25cab-113">This example shows how to get the endpoints and metadata for the AzureUSGovernment environment.</span></span>

## <span data-ttu-id="25cab-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="25cab-114">PARAMETERS</span></span>

### <span data-ttu-id="25cab-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="25cab-115">-DefaultProfile</span></span>
<span data-ttu-id="25cab-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="25cab-116">The credentials, account, tenant and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="25cab-117">-Namn</span><span class="sxs-lookup"><span data-stu-id="25cab-117">-Name</span></span>
<span data-ttu-id="25cab-118">Anger namnet på Azure-instansen som ska visas.</span><span class="sxs-lookup"><span data-stu-id="25cab-118">Specifies the name of the Azure instance to get.</span></span>

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

### <span data-ttu-id="25cab-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="25cab-119">CommonParameters</span></span>
<span data-ttu-id="25cab-120">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="25cab-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="25cab-121">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="25cab-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="25cab-122">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="25cab-122">INPUTS</span></span>

### <span data-ttu-id="25cab-123">System. String</span><span class="sxs-lookup"><span data-stu-id="25cab-123">System.String</span></span>

## <span data-ttu-id="25cab-124">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="25cab-124">OUTPUTS</span></span>

### <span data-ttu-id="25cab-125">Microsoft. Azure. commands. Profile. Models. PSAzureEnvironment</span><span class="sxs-lookup"><span data-stu-id="25cab-125">Microsoft.Azure.Commands.Profile.Models.PSAzureEnvironment</span></span>

## <span data-ttu-id="25cab-126">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="25cab-126">NOTES</span></span>

## <span data-ttu-id="25cab-127">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="25cab-127">RELATED LINKS</span></span>

[<span data-ttu-id="25cab-128">Add-AzureRMEnvironment</span><span class="sxs-lookup"><span data-stu-id="25cab-128">Add-AzureRMEnvironment</span></span>](./Add-AzureRMEnvironment.md)

[<span data-ttu-id="25cab-129">Remove-AzureRMEnvironment</span><span class="sxs-lookup"><span data-stu-id="25cab-129">Remove-AzureRMEnvironment</span></span>](./Remove-AzureRMEnvironment.md)

[<span data-ttu-id="25cab-130">Set-AzureRMEnvironment</span><span class="sxs-lookup"><span data-stu-id="25cab-130">Set-AzureRMEnvironment</span></span>](./Set-AzureRMEnvironment.md)

