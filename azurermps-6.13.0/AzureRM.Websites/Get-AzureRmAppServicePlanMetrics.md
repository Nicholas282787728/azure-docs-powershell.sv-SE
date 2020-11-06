---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.Websites
ms.assetid: 0AC0C4F9-4138-49EA-88CB-DC220DE7E9F4
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/get-azurermappserviceplanmetrics
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Get-AzureRmAppServicePlanMetrics.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Get-AzureRmAppServicePlanMetrics.md
ms.openlocfilehash: a8bb330315cfdd43e30ab790afcdeba0b09cef08
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93577768"
---
# <span data-ttu-id="8df73-101">Get-AzureRmAppServicePlanMetrics</span><span class="sxs-lookup"><span data-stu-id="8df73-101">Get-AzureRmAppServicePlanMetrics</span></span>

## <span data-ttu-id="8df73-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="8df73-102">SYNOPSIS</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8df73-103">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="8df73-103">SYNTAX</span></span>

### <span data-ttu-id="8df73-104">S</span><span class="sxs-lookup"><span data-stu-id="8df73-104">S1</span></span>
```
Get-AzureRmAppServicePlanMetrics [-Metrics] <String[]> [-StartTime] <DateTime> [[-EndTime] <DateTime>]
 [-Granularity] <String> [-InstanceDetails] [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8df73-105">S2</span><span class="sxs-lookup"><span data-stu-id="8df73-105">S2</span></span>
```
Get-AzureRmAppServicePlanMetrics [-Metrics] <String[]> [-StartTime] <DateTime> [[-EndTime] <DateTime>]
 [-Granularity] <String> [-InstanceDetails] [-AppServicePlan] <PSAppServicePlan>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8df73-106">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="8df73-106">DESCRIPTION</span></span>
<span data-ttu-id="8df73-107">**AzureRmAppServicePlanMetrics** får App Service-planens mått.</span><span class="sxs-lookup"><span data-stu-id="8df73-107">The **Get-AzureRmAppServicePlanMetrics** gets App Service Plan metrics.</span></span>

## <span data-ttu-id="8df73-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="8df73-108">EXAMPLES</span></span>

### <span data-ttu-id="8df73-109">9.1</span><span class="sxs-lookup"><span data-stu-id="8df73-109">1:</span></span>
```
PS C:\>Get-AzureRmAppServicePlanMetrics -ResourceGroupName "Default-Web-WestUS" -Name "ContosoAppServPlan" -StartTime 2016-11-30T22:00:00Z -EndTime 2016-11-30T22:30:00Z -Granularity PT1M -Metrics "CPU Percentage"
```

<span data-ttu-id="8df73-110">Det här kommandot får CPU-procent för App Service-planen per minut (PT1M-avsöknings tid 1 minut) mellan StartTime och slut värde</span><span class="sxs-lookup"><span data-stu-id="8df73-110">This command gets CPU percentage of the App Service Plan per minute(PT1M - Poll Time 1 minute) between StartTime and EndTime</span></span>

## <span data-ttu-id="8df73-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="8df73-111">PARAMETERS</span></span>

### <span data-ttu-id="8df73-112">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="8df73-112">-AppServicePlan</span></span>
<span data-ttu-id="8df73-113">App Service plan-objekt</span><span class="sxs-lookup"><span data-stu-id="8df73-113">App Service Plan Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.WebApps.Models.WebApp.PSAppServicePlan
Parameter Sets: S2
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8df73-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8df73-114">-DefaultProfile</span></span>
<span data-ttu-id="8df73-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="8df73-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8df73-116">-Slut tid</span><span class="sxs-lookup"><span data-stu-id="8df73-116">-EndTime</span></span>
<span data-ttu-id="8df73-117">Slut tid i UTC</span><span class="sxs-lookup"><span data-stu-id="8df73-117">End Time in UTC</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8df73-118">-Granularitet</span><span class="sxs-lookup"><span data-stu-id="8df73-118">-Granularity</span></span>
<span data-ttu-id="8df73-119">Granularitet</span><span class="sxs-lookup"><span data-stu-id="8df73-119">Granularity</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: PT1M, PT1H, P1D

Required: True
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8df73-120">-InstanceDetails</span><span class="sxs-lookup"><span data-stu-id="8df73-120">-InstanceDetails</span></span>
<span data-ttu-id="8df73-121">Instans Detaljer</span><span class="sxs-lookup"><span data-stu-id="8df73-121">Instance Details</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8df73-122">-Mått</span><span class="sxs-lookup"><span data-stu-id="8df73-122">-Metrics</span></span>
<span data-ttu-id="8df73-123">Mått</span><span class="sxs-lookup"><span data-stu-id="8df73-123">Metrics</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8df73-124">-Namn</span><span class="sxs-lookup"><span data-stu-id="8df73-124">-Name</span></span>
<span data-ttu-id="8df73-125">Namn på App Service-abonnemang</span><span class="sxs-lookup"><span data-stu-id="8df73-125">App Service Plan Name</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8df73-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8df73-126">-ResourceGroupName</span></span>
<span data-ttu-id="8df73-127">Resurs grupps namn</span><span class="sxs-lookup"><span data-stu-id="8df73-127">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8df73-128">-StartTime</span><span class="sxs-lookup"><span data-stu-id="8df73-128">-StartTime</span></span>
<span data-ttu-id="8df73-129">Start tid i UTC</span><span class="sxs-lookup"><span data-stu-id="8df73-129">Start Time in UTC</span></span>

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8df73-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8df73-130">CommonParameters</span></span>
<span data-ttu-id="8df73-131">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8df73-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8df73-132">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8df73-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8df73-133">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="8df73-133">INPUTS</span></span>

### <span data-ttu-id="8df73-134">Microsoft. Azure. Management. webbplatser. Models. AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="8df73-134">Microsoft.Azure.Management.WebSites.Models.AppServicePlan</span></span>
<span data-ttu-id="8df73-135">Parametrar: AppServicePlan (ByValue)</span><span class="sxs-lookup"><span data-stu-id="8df73-135">Parameters: AppServicePlan (ByValue)</span></span>

## <span data-ttu-id="8df73-136">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="8df73-136">OUTPUTS</span></span>

### <span data-ttu-id="8df73-137">Microsoft. Azure. Management. webbplatser. Models. ResourceMetric</span><span class="sxs-lookup"><span data-stu-id="8df73-137">Microsoft.Azure.Management.WebSites.Models.ResourceMetric</span></span>

## <span data-ttu-id="8df73-138">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="8df73-138">NOTES</span></span>

## <span data-ttu-id="8df73-139">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="8df73-139">RELATED LINKS</span></span>
