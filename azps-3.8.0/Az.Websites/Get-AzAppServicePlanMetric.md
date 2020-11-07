---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: 0AC0C4F9-4138-49EA-88CB-DC220DE7E9F4
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/get-azappserviceplanmetric
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzAppServicePlanMetric.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzAppServicePlanMetric.md
ms.openlocfilehash: d3a2cd8d0907d26a137df547f1599c9ed09cb7b3
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93926514"
---
# <span data-ttu-id="26438-101">Get-AzAppServicePlanMetric</span><span class="sxs-lookup"><span data-stu-id="26438-101">Get-AzAppServicePlanMetric</span></span>

## <span data-ttu-id="26438-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="26438-102">SYNOPSIS</span></span>

## <span data-ttu-id="26438-103">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="26438-103">SYNTAX</span></span>

### <span data-ttu-id="26438-104">S</span><span class="sxs-lookup"><span data-stu-id="26438-104">S1</span></span>
```
Get-AzAppServicePlanMetric [-Metrics] <String[]> [-StartTime] <DateTime> [[-EndTime] <DateTime>]
 [-Granularity] <String> [-InstanceDetails] [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="26438-105">S2</span><span class="sxs-lookup"><span data-stu-id="26438-105">S2</span></span>
```
Get-AzAppServicePlanMetric [-Metrics] <String[]> [-StartTime] <DateTime> [[-EndTime] <DateTime>]
 [-Granularity] <String> [-InstanceDetails] [-AppServicePlan] <PSAppServicePlan>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="26438-106">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="26438-106">DESCRIPTION</span></span>
<span data-ttu-id="26438-107">**AzAppServicePlanMetric** får App Service-planens mått.</span><span class="sxs-lookup"><span data-stu-id="26438-107">The **Get-AzAppServicePlanMetric** gets App Service Plan metrics.</span></span>

## <span data-ttu-id="26438-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="26438-108">EXAMPLES</span></span>

### <span data-ttu-id="26438-109">9.1</span><span class="sxs-lookup"><span data-stu-id="26438-109">1:</span></span>
```
PS C:\>Get-AzAppServicePlanMetric -ResourceGroupName "Default-Web-WestUS" -Name "ContosoAppServPlan" -StartTime 2016-11-30T22:00:00Z -EndTime 2016-11-30T22:30:00Z -Granularity PT1M -Metrics "CPU Percentage"
```

<span data-ttu-id="26438-110">Det här kommandot får CPU-procent för App Service-planen per minut (PT1M-avsöknings tid 1 minut) mellan StartTime och slut värde</span><span class="sxs-lookup"><span data-stu-id="26438-110">This command gets CPU percentage of the App Service Plan per minute(PT1M - Poll Time 1 minute) between StartTime and EndTime</span></span>

## <span data-ttu-id="26438-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="26438-111">PARAMETERS</span></span>

### <span data-ttu-id="26438-112">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="26438-112">-AppServicePlan</span></span>
<span data-ttu-id="26438-113">App Service plan-objekt</span><span class="sxs-lookup"><span data-stu-id="26438-113">App Service Plan Object</span></span>

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

### <span data-ttu-id="26438-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="26438-114">-DefaultProfile</span></span>
<span data-ttu-id="26438-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="26438-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="26438-116">-Slut tid</span><span class="sxs-lookup"><span data-stu-id="26438-116">-EndTime</span></span>
<span data-ttu-id="26438-117">Slut tid i UTC</span><span class="sxs-lookup"><span data-stu-id="26438-117">End Time in UTC</span></span>

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

### <span data-ttu-id="26438-118">-Granularitet</span><span class="sxs-lookup"><span data-stu-id="26438-118">-Granularity</span></span>
<span data-ttu-id="26438-119">Granularitet</span><span class="sxs-lookup"><span data-stu-id="26438-119">Granularity</span></span>

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

### <span data-ttu-id="26438-120">-InstanceDetails</span><span class="sxs-lookup"><span data-stu-id="26438-120">-InstanceDetails</span></span>
<span data-ttu-id="26438-121">Instans Detaljer</span><span class="sxs-lookup"><span data-stu-id="26438-121">Instance Details</span></span>

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

### <span data-ttu-id="26438-122">-Mått</span><span class="sxs-lookup"><span data-stu-id="26438-122">-Metrics</span></span>
<span data-ttu-id="26438-123">Mått</span><span class="sxs-lookup"><span data-stu-id="26438-123">Metrics</span></span>

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

### <span data-ttu-id="26438-124">-Namn</span><span class="sxs-lookup"><span data-stu-id="26438-124">-Name</span></span>
<span data-ttu-id="26438-125">Namn på App Service-abonnemang</span><span class="sxs-lookup"><span data-stu-id="26438-125">App Service Plan Name</span></span>

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

### <span data-ttu-id="26438-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="26438-126">-ResourceGroupName</span></span>
<span data-ttu-id="26438-127">Resurs grupps namn</span><span class="sxs-lookup"><span data-stu-id="26438-127">Resource Group Name</span></span>

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

### <span data-ttu-id="26438-128">-StartTime</span><span class="sxs-lookup"><span data-stu-id="26438-128">-StartTime</span></span>
<span data-ttu-id="26438-129">Start tid i UTC</span><span class="sxs-lookup"><span data-stu-id="26438-129">Start Time in UTC</span></span>

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

### <span data-ttu-id="26438-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="26438-130">CommonParameters</span></span>
<span data-ttu-id="26438-131">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="26438-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="26438-132">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="26438-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="26438-133">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="26438-133">INPUTS</span></span>

### <span data-ttu-id="26438-134">Microsoft. Azure. commands. webapps. Models. WebApp. PSAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="26438-134">Microsoft.Azure.Commands.WebApps.Models.WebApp.PSAppServicePlan</span></span>

## <span data-ttu-id="26438-135">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="26438-135">OUTPUTS</span></span>

### <span data-ttu-id="26438-136">Microsoft. Azure. Management. webbplatser. Models. ResourceMetric</span><span class="sxs-lookup"><span data-stu-id="26438-136">Microsoft.Azure.Management.WebSites.Models.ResourceMetric</span></span>

## <span data-ttu-id="26438-137">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="26438-137">NOTES</span></span>

## <span data-ttu-id="26438-138">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="26438-138">RELATED LINKS</span></span>
