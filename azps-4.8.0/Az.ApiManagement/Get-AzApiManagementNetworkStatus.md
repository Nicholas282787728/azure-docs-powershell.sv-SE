---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementnetworkstatus
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementNetworkStatus.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementNetworkStatus.md
ms.openlocfilehash: 5ba351ab1a5102acc1855e13821650b8ce1b4373
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94101256"
---
# <span data-ttu-id="54f1a-101">Get-AzApiManagementNetworkStatus</span><span class="sxs-lookup"><span data-stu-id="54f1a-101">Get-AzApiManagementNetworkStatus</span></span>

## <span data-ttu-id="54f1a-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="54f1a-102">SYNOPSIS</span></span>
<span data-ttu-id="54f1a-103">Hämtar anslutnings status till de externa resurser som API-hanteringskonsolen är beroende av i moln tjänsten.</span><span class="sxs-lookup"><span data-stu-id="54f1a-103">Gets the Connectivity Status to the external resources on which the Api Management service depends from inside the Cloud Service.</span></span> <span data-ttu-id="54f1a-104">Det returnerar också de DNS-servrar som visas för CloudService.</span><span class="sxs-lookup"><span data-stu-id="54f1a-104">This also returns the DNS Servers as visible to the CloudService.</span></span>

## <span data-ttu-id="54f1a-105">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="54f1a-105">SYNTAX</span></span>

### <span data-ttu-id="54f1a-106">ByInputObject (standard)</span><span class="sxs-lookup"><span data-stu-id="54f1a-106">ByInputObject (Default)</span></span>
```
Get-AzApiManagementNetworkStatus -ApiManagementObject <PsApiManagement> [-Location <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="54f1a-107">ExpandedParameter</span><span class="sxs-lookup"><span data-stu-id="54f1a-107">ExpandedParameter</span></span>
```
Get-AzApiManagementNetworkStatus -ResourceGroupName <String> -Name <String> [-Location <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="54f1a-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="54f1a-108">DESCRIPTION</span></span>
<span data-ttu-id="54f1a-109">Hämtar nätverks statusen för API-hanterings tjänsten</span><span class="sxs-lookup"><span data-stu-id="54f1a-109">Gets the Network status of their Api Management service</span></span>

## <span data-ttu-id="54f1a-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="54f1a-110">EXAMPLES</span></span>

### <span data-ttu-id="54f1a-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="54f1a-111">Example 1</span></span>
```powershell
PS D:\github\azure-powershell> Get-AzApiManagementNetworkStatus -ResourceGroupName powershelltest -Name powershellsdkservice

Location DnsServers      ConnectivityStatus
-------- ----------      ------------------
West US  {168.63.129.16} {apimgmtstaoonqs7wwzjosky.blob.core.windows.net, apimgmtstaoonqs7wwzjosky.file.core.windows.net, apimgmtstaoonqs7wwzjosky.queue.core.windows.net, apimgmtstaoonqs7wwzjosk...


PS D:\github\azure-powershell> $networkStatus = Get-AzApiManagementNetworkStatus -ResourceGroupName powershelltest -Name powershellsdkservice
PS D:\github\azure-powershell> $networkStatus.ConnectivityStatus


Name             : apimgmtstaoonqs7wwzjosky.blob.core.windows.net
Status           : success
Error            :
LastUpdated      : 5/2/2019 5:06:38 PM
LastStatusChange : 1/30/2019 5:31:38 PM

Name             : apimgmtstaoonqs7wwzjosky.file.core.windows.net
Status           : success
Error            :
LastUpdated      : 5/2/2019 5:06:38 PM
LastStatusChange : 1/30/2019 5:31:39 PM

Name             : apimgmtstaoonqs7wwzjosky.queue.core.windows.net
Status           : success
Error            :
LastUpdated      : 5/2/2019 5:06:38 PM
LastStatusChange : 1/30/2019 5:31:39 PM

Name             : apimgmtstaoonqs7wwzjosky.table.core.windows.net
Status           : success
Error            :
LastUpdated      : 5/2/2019 5:06:38 PM
LastStatusChange : 1/30/2019 5:31:38 PM

Name             : bx9gltecfv.database.windows.net
Status           : success
Error            :
LastUpdated      : 5/2/2019 5:06:41 PM
LastStatusChange : 1/30/2019 5:31:39 PM

Name             : https://prod3.metrics.nsatc.net:1886/RecoveryService
Status           : success
Error            :
LastUpdated      : 5/2/2019 5:07:11 PM
LastStatusChange : 4/29/2019 1:31:30 PM

Name             : prod.warmpath.msftcloudes.com
Status           : success
Error            :
LastUpdated      : 5/2/2019 5:06:38 PM
LastStatusChange : 1/30/2019 5:31:38 PM

Name             : Scm
Status           : success
Error            :
LastUpdated      : 5/2/2019 5:04:27 PM
LastStatusChange : 4/30/2019 11:16:20 PM
```

<span data-ttu-id="54f1a-112">Hämtar anslutnings statusen för de olika resurser som ApiManagement-tjänsten är beroende av.</span><span class="sxs-lookup"><span data-stu-id="54f1a-112">Gets the connectivity status of the different resources on which ApiManagement service depends upon.</span></span>

## <span data-ttu-id="54f1a-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="54f1a-113">PARAMETERS</span></span>

### <span data-ttu-id="54f1a-114">-ApiManagementObject</span><span class="sxs-lookup"><span data-stu-id="54f1a-114">-ApiManagementObject</span></span>
<span data-ttu-id="54f1a-115">Instans av PsApiManagement.</span><span class="sxs-lookup"><span data-stu-id="54f1a-115">Instance of PsApiManagement.</span></span> <span data-ttu-id="54f1a-116">Denna parameter är obligatorisk.</span><span class="sxs-lookup"><span data-stu-id="54f1a-116">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="54f1a-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="54f1a-117">-DefaultProfile</span></span>
<span data-ttu-id="54f1a-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="54f1a-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="54f1a-119">-Plats</span><span class="sxs-lookup"><span data-stu-id="54f1a-119">-Location</span></span>
<span data-ttu-id="54f1a-120">Platsen för API-hanterings tjänsten.</span><span class="sxs-lookup"><span data-stu-id="54f1a-120">Location of the API Management Service.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="54f1a-121">-Namn</span><span class="sxs-lookup"><span data-stu-id="54f1a-121">-Name</span></span>
<span data-ttu-id="54f1a-122">Namn på API-hantering.</span><span class="sxs-lookup"><span data-stu-id="54f1a-122">Name of API Management.</span></span>

```yaml
Type: System.String
Parameter Sets: ExpandedParameter
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="54f1a-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="54f1a-123">-ResourceGroupName</span></span>
<span data-ttu-id="54f1a-124">Namn på resurs gruppen som API-hantering finns under.</span><span class="sxs-lookup"><span data-stu-id="54f1a-124">Name of resource group under which API Management exists.</span></span>

```yaml
Type: System.String
Parameter Sets: ExpandedParameter
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="54f1a-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="54f1a-125">CommonParameters</span></span>
<span data-ttu-id="54f1a-126">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="54f1a-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="54f1a-127">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="54f1a-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="54f1a-128">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="54f1a-128">INPUTS</span></span>

### <span data-ttu-id="54f1a-129">Microsoft. Azure. commands. ApiManagement. Models. PsApiManagement</span><span class="sxs-lookup"><span data-stu-id="54f1a-129">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement</span></span>

### <span data-ttu-id="54f1a-130">System. String</span><span class="sxs-lookup"><span data-stu-id="54f1a-130">System.String</span></span>

## <span data-ttu-id="54f1a-131">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="54f1a-131">OUTPUTS</span></span>

### <span data-ttu-id="54f1a-132">Microsoft. Azure. commands. ApiManagement. Models. PsApiManagementNetworkStatus</span><span class="sxs-lookup"><span data-stu-id="54f1a-132">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementNetworkStatus</span></span>

## <span data-ttu-id="54f1a-133">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="54f1a-133">NOTES</span></span>

## <span data-ttu-id="54f1a-134">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="54f1a-134">RELATED LINKS</span></span>
