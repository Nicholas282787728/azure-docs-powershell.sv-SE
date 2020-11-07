---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HealthcareApis.dll-Help.xml
Module Name: Az.HealthcareApis
online version: https://docs.microsoft.com/en-us/powershell/module/az.healthcareapis/get-azhealthcareapisservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HealthcareApis/HealthcareApis/help/Get-AzHealthcareApisService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HealthcareApis/HealthcareApis/help/Get-AzHealthcareApisService.md
ms.openlocfilehash: d1a6edc3365631f93d2bc3b7a0e153ec360c2611
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93925862"
---
# <span data-ttu-id="7335d-101">Get-AzHealthcareApisService</span><span class="sxs-lookup"><span data-stu-id="7335d-101">Get-AzHealthcareApisService</span></span>

## <span data-ttu-id="7335d-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="7335d-102">SYNOPSIS</span></span>
<span data-ttu-id="7335d-103">Hämta metadata för en tjänst instans.</span><span class="sxs-lookup"><span data-stu-id="7335d-103">Get the metadata of a service instance.</span></span>

## <span data-ttu-id="7335d-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="7335d-104">SYNTAX</span></span>

### <span data-ttu-id="7335d-105">ListParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="7335d-105">ListParameterSet (Default)</span></span>
```
Get-AzHealthcareApisService [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="7335d-106">ServiceNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="7335d-106">ServiceNameParameterSet</span></span>
```
Get-AzHealthcareApisService -ResourceGroupName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7335d-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="7335d-107">ResourceIdParameterSet</span></span>
```
Get-AzHealthcareApisService -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="7335d-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="7335d-108">DESCRIPTION</span></span>
<span data-ttu-id="7335d-109">Hämtar befintliga healthcareApis FHIR-tjänst konton som har skapats i det angivna abonnemanget eller en resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="7335d-109">Gets existing healthcareApis fhir service accounts created within the specified subscription or a resource group.</span></span>

## <span data-ttu-id="7335d-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="7335d-110">EXAMPLES</span></span>

### <span data-ttu-id="7335d-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="7335d-111">Example 1</span></span>
```powershell
PS C:\> Get-AzHealthcareApisService -Name "MyService" -ResourceGroupName "MyResourceGroup"

AccessPolicies          : {77777777-6666-5555-4444-1111111111111}
Audience                : https://azurehealthcareapis.com
Authority               : https://login.microsoftonline.com/72f988bf-86f1-41af-91ab-2d7cd011db47
CorsAllowCredentials    : False
CorsHeaders             : {}
CorsMaxAge              : 0
CorsMethods             : {}
CorsOrigins             : {}
CosmosDbOfferThroughput : 400
Etag                    : "00000000-0000-0000-0000-000000000000"
Id                      : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroup/providers/Microsoft
                          .HealthcareApis/services/MyService
Kind                    : fhir-R4
Location                : westus2
Name                    : MyService
ResourceGroupName       : MyResourceGroup
Tags                    : {}
ResourceType            : Microsoft.HealthcareApis/services
SmartProxyEnabled       : False
```

### <span data-ttu-id="7335d-112">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="7335d-112">Example 2</span></span>

<span data-ttu-id="7335d-113">Hämtar metadata för alla HealthcareApis tjänster i den tillhandahållna resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="7335d-113">Gets the metadata for all HealthcareApis services in the provided Resource Group.</span></span>

```powershell
PS C:\> Get-AzHealthcareApisService -ResourceGroupName "MyResourceGroup"

AccessPolicies          : {77777777-6666-5555-4444-1111111111111}
Audience                : https://azurehealthcareapis.com
Authority               : https://login.microsoftonline.com/72f988bf-86f1-41af-91ab-2d7cd011db48
CorsAllowCredentials    : False
CorsHeaders             : {}
CorsMaxAge              : 0
CorsMethods             : {}
CorsOrigins             : {}
CosmosDbOfferThroughput : 400
Etag                    : "00000000-0000-0000-0000-000000000000"
Id                      : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroup/providers/Microsoft
                          .HealthcareApis/services/MyService
Kind                    : fhir-R4
Location                : westus2
Name                    : MyService
ResourceGroupName       : MyResourceGroup
Tags                    : {}
ResourceType            : Microsoft.HealthcareApis/services
SmartProxyEnabled       : False

AccessPolicies          : {77777777-6666-5555-4444-1111111111111}
Audience                : https://azurehealthcareapis.com
Authority               : https://login.microsoftonline.com/72f988bf-86f1-41af-91ab-2d7cd011db478
CorsAllowCredentials    : False
CorsHeaders             : {}
CorsMaxAge              : 0
CorsMethods             : {}
CorsOrigins             : {}
CosmosDbOfferThroughput : 400
Etag                    : "00000000-0000-0000-0000-000000000000"
Id                      : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroup/providers/Microsoft
                          .HealthcareApis/services/MyService1
Kind                    : fhir-R4
Location                : westus2
Name                    : MyService1
ResourceGroupName       : MyResourceGroup
Tags                    : {}
ResourceType            : Microsoft.HealthcareApis/services
SmartProxyEnabled       : False
```

### <span data-ttu-id="7335d-114">Exempel 3</span><span class="sxs-lookup"><span data-stu-id="7335d-114">Example 3</span></span>

<span data-ttu-id="7335d-115">Hämtar metadata för alla HealthcareApis tjänster i den angivna prenumerationen</span><span class="sxs-lookup"><span data-stu-id="7335d-115">Gets the metadata for all HealthcareApis services in the given subscription</span></span>

```powershell
PS C:\> Get-AzHealthcareApisService

AccessPolicies          : {77777777-6666-5555-4444-1111111111111}
Audience                : https://azurehealthcareapis.com
Authority               : https://login.microsoftonline.com/72f988bf-86f1-41af-91ab-2d7cd011db48
CorsAllowCredentials    : False
CorsHeaders             : {}
CorsMaxAge              : 0
CorsMethods             : {}
CorsOrigins             : {}
CosmosDbOfferThroughput : 400
Etag                    : "00000000-0000-0000-0000-000000000000"
Id                      : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroup/providers/Microsoft
                          .HealthcareApis/services/MyService
Kind                    : fhir-R4
Location                : westus2
Name                    : MyService
ResourceGroupName       : MyResourceGroup
Tags                    : {}
ResourceType            : Microsoft.HealthcareApis/services
SmartProxyEnabled       : False

AccessPolicies          : {77777777-6666-5555-4444-1111111111111}
Audience                : https://azurehealthcareapis.com
Authority               : https://login.microsoftonline.com/72f988bf-86f1-41af-91ab-2d7cd011db478
CorsAllowCredentials    : False
CorsHeaders             : {}
CorsMaxAge              : 0
CorsMethods             : {}
CorsOrigins             : {}
CosmosDbOfferThroughput : 400
Etag                    : "00000000-0000-0000-0000-000000000000"
Id                      : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroup/providers/Microsoft
                          .HealthcareApis/services/MyService1
Kind                    : fhir-R4
Location                : westus2
Name                    : MyService1
ResourceGroupName       : MyResourceGroup
Tags                    : {}
ResourceType            : Microsoft.HealthcareApis/services
SmartProxyEnabled       : False
```

## <span data-ttu-id="7335d-116">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="7335d-116">PARAMETERS</span></span>

### <span data-ttu-id="7335d-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7335d-117">-DefaultProfile</span></span>
<span data-ttu-id="7335d-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="7335d-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7335d-119">-Namn</span><span class="sxs-lookup"><span data-stu-id="7335d-119">-Name</span></span>
<span data-ttu-id="7335d-120">HealthcareApis-tjänstens namn.</span><span class="sxs-lookup"><span data-stu-id="7335d-120">HealthcareApis Service Name.</span></span>

```yaml
Type: System.String
Parameter Sets: ServiceNameParameterSet
Aliases: HealthcareApisName, FhirServiceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7335d-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7335d-121">-ResourceGroupName</span></span>
<span data-ttu-id="7335d-122">Resurs grupps namn.</span><span class="sxs-lookup"><span data-stu-id="7335d-122">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: ListParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ServiceNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7335d-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7335d-123">-ResourceId</span></span>
<span data-ttu-id="7335d-124">Namn på resurs-ID.</span><span class="sxs-lookup"><span data-stu-id="7335d-124">Resource Id Name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7335d-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7335d-125">CommonParameters</span></span>
<span data-ttu-id="7335d-126">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7335d-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7335d-127">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="7335d-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7335d-128">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="7335d-128">INPUTS</span></span>

### <span data-ttu-id="7335d-129">System. String</span><span class="sxs-lookup"><span data-stu-id="7335d-129">System.String</span></span>

## <span data-ttu-id="7335d-130">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="7335d-130">OUTPUTS</span></span>

### <span data-ttu-id="7335d-131">Microsoft. Azure. commands. HealthcareApisService. Models. PSHealthcareApisService</span><span class="sxs-lookup"><span data-stu-id="7335d-131">Microsoft.Azure.Commands.HealthcareApisService.Models.PSHealthcareApisService</span></span>

## <span data-ttu-id="7335d-132">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="7335d-132">NOTES</span></span>

## <span data-ttu-id="7335d-133">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="7335d-133">RELATED LINKS</span></span>
