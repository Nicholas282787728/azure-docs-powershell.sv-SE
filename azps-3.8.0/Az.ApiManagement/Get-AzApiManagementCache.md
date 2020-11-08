---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementcache
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementCache.md
ms.openlocfilehash: 757332267d2db2f797bb2f7ca2a39dbb32ee06c7
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94089668"
---
# <span data-ttu-id="47af6-101">Get-AzApiManagementCache</span><span class="sxs-lookup"><span data-stu-id="47af6-101">Get-AzApiManagementCache</span></span>

## <span data-ttu-id="47af6-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="47af6-102">SYNOPSIS</span></span>
<span data-ttu-id="47af6-103">Få information om cacheminnet.</span><span class="sxs-lookup"><span data-stu-id="47af6-103">Get the details of the Cache.</span></span>

## <span data-ttu-id="47af6-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="47af6-104">SYNTAX</span></span>

### <span data-ttu-id="47af6-105">ContextParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="47af6-105">ContextParameterSet (Default)</span></span>
```
Get-AzApiManagementCache -Context <PsApiManagementContext> [-CacheId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="47af6-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="47af6-106">ResourceIdParameterSet</span></span>
```
Get-AzApiManagementCache -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="47af6-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="47af6-107">DESCRIPTION</span></span>
<span data-ttu-id="47af6-108">Få information om cacheminnet som har kon figurer ATS i API Management Service.</span><span class="sxs-lookup"><span data-stu-id="47af6-108">Get the details of the Cache configured in Api Management service.</span></span>

## <span data-ttu-id="47af6-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="47af6-109">EXAMPLES</span></span>

### <span data-ttu-id="47af6-110">Exempel 1: Hämta alla cacheminnen</span><span class="sxs-lookup"><span data-stu-id="47af6-110">Example 1: Get all Caches</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementCache -Context $apimContext
```

```
CacheId           : westus
Description       : apim.redis.cache.windows.net
ConnectionString  : {{5cc1848125a3f724dcf9a928}}
ResourceId        : https://management.azure.com/subscriptions/a200340d-6b82-494d-9dbf-687ba6e33f9e/resourceGroups/Api-Default-West-US/providers/Microsoft.Cache/Redis/apim
Id                : /subscriptions/a200340d-6b82-494d-9dbf-687ba6e33f9e/resourceGroups/Api-Default-West-US/providers/Microsoft.ApiManagement/service/contoso/caches/westus
ResourceGroupName : Api-Default-West-US
ServiceName       : contoso
```

<span data-ttu-id="47af6-111">Hämtar en lista över alla Caches som har kon figurer ATS i API-hanterings tjänsten.</span><span class="sxs-lookup"><span data-stu-id="47af6-111">Gets a list of all the Caches configured in the Api Management service.</span></span>

### <span data-ttu-id="47af6-112">Exempel 2: hämta cacheminnet som anges av $ västkusten</span><span class="sxs-lookup"><span data-stu-id="47af6-112">Example 2: Get the Cache specified by the Identifier westus</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementCache -Context $apimContext -cacheId westus
```

```
CacheId           : westus
Description       : apim.redis.cache.windows.net
ConnectionString  : {{5cc1848125a3f724dcf9a928}}
ResourceId        : https://management.azure.com/subscriptions/a200340d-6b82-494d-9dbf-687ba6e33f9e/resourceGroups/Api-Default-West-US/providers/Microsoft.Cache/Redis/apim
Id                : /subscriptions/a200340d-6b82-494d-9dbf-687ba6e33f9e/resourceGroups/Api-Default-WestUS/providers/Microsoft.ApiManagement/service/contoso/caches/westus
ResourceGroupName : Api-Default-WestUS
ServiceName       : contoso
```

<span data-ttu-id="47af6-113">Få information om angiven cache konfigurerad för västkusten</span><span class="sxs-lookup"><span data-stu-id="47af6-113">Get the details of the specified Cache configured for westus</span></span>

## <span data-ttu-id="47af6-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="47af6-114">PARAMETERS</span></span>

### <span data-ttu-id="47af6-115">-CacheId</span><span class="sxs-lookup"><span data-stu-id="47af6-115">-CacheId</span></span>
<span data-ttu-id="47af6-116">Identifierare för ett cacheminne.</span><span class="sxs-lookup"><span data-stu-id="47af6-116">Identifier of a cache.</span></span>
<span data-ttu-id="47af6-117">Om du anger det här alternativet kommer cacheminnet att hittas efter ID.</span><span class="sxs-lookup"><span data-stu-id="47af6-117">If specified will try to find cache by the identifier.</span></span>
<span data-ttu-id="47af6-118">Denna parameter är valfri.</span><span class="sxs-lookup"><span data-stu-id="47af6-118">This parameter is optional.</span></span>

```yaml
Type: System.String
Parameter Sets: ContextParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="47af6-119">-Kontext</span><span class="sxs-lookup"><span data-stu-id="47af6-119">-Context</span></span>
<span data-ttu-id="47af6-120">Instans av PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="47af6-120">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="47af6-121">Denna parameter är obligatorisk.</span><span class="sxs-lookup"><span data-stu-id="47af6-121">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: ContextParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="47af6-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="47af6-122">-DefaultProfile</span></span>
<span data-ttu-id="47af6-123">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="47af6-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="47af6-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="47af6-124">-ResourceId</span></span>
<span data-ttu-id="47af6-125">Arm-resurs-ID för ett cacheminne.</span><span class="sxs-lookup"><span data-stu-id="47af6-125">Arm Resource Identifier of a cache.</span></span> <span data-ttu-id="47af6-126">Om du anger det här alternativet kommer cacheminnet att hittas efter ID.</span><span class="sxs-lookup"><span data-stu-id="47af6-126">If specified will try to find cache by the identifier.</span></span> <span data-ttu-id="47af6-127">Denna parameter är obligatorisk.</span><span class="sxs-lookup"><span data-stu-id="47af6-127">This parameter is required.</span></span>

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

### <span data-ttu-id="47af6-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="47af6-128">CommonParameters</span></span>
<span data-ttu-id="47af6-129">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="47af6-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="47af6-130">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="47af6-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="47af6-131">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="47af6-131">INPUTS</span></span>

### <span data-ttu-id="47af6-132">Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="47af6-132">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="47af6-133">System. String</span><span class="sxs-lookup"><span data-stu-id="47af6-133">System.String</span></span>

## <span data-ttu-id="47af6-134">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="47af6-134">OUTPUTS</span></span>

### <span data-ttu-id="47af6-135">Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementCache</span><span class="sxs-lookup"><span data-stu-id="47af6-135">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementCache</span></span>

## <span data-ttu-id="47af6-136">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="47af6-136">NOTES</span></span>

## <span data-ttu-id="47af6-137">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="47af6-137">RELATED LINKS</span></span>

[<span data-ttu-id="47af6-138">Get-AzApiManagementCache</span><span class="sxs-lookup"><span data-stu-id="47af6-138">Get-AzApiManagementCache</span></span>](./Get-AzApiManagementCache)

[<span data-ttu-id="47af6-139">Set-AzApiManagementCache</span><span class="sxs-lookup"><span data-stu-id="47af6-139">Set-AzApiManagementCache</span></span>](./Set-AzApiManagementCache.md)

[<span data-ttu-id="47af6-140">Remove-AzApiManagementCache</span><span class="sxs-lookup"><span data-stu-id="47af6-140">Remove-AzApiManagementCache</span></span>](./Remove-AzApiManagementCache.md)