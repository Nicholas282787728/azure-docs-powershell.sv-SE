---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: 0AC0C4F9-4138-49EA-88CB-DC220DE7E9F4
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/get-azappserviceplanmetric
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzAppServicePlanMetric.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzAppServicePlanMetric.md
ms.openlocfilehash: 04f07e435f8656ef18e452538d97b3728179c969
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93921114"
---
# <span data-ttu-id="75124-101">Get-AzAppServicePlanMetric</span><span class="sxs-lookup"><span data-stu-id="75124-101">Get-AzAppServicePlanMetric</span></span>

## <span data-ttu-id="75124-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="75124-102">SYNOPSIS</span></span>

## <span data-ttu-id="75124-103">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="75124-103">SYNTAX</span></span>

### <span data-ttu-id="75124-104">S</span><span class="sxs-lookup"><span data-stu-id="75124-104">S1</span></span>
```
Get-AzAppServicePlanMetric [-Metrics] <String[]> [-StartTime] <DateTime> [[-EndTime] <DateTime>]
 [-Granularity] <String> [-InstanceDetails] [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="75124-105">S2</span><span class="sxs-lookup"><span data-stu-id="75124-105">S2</span></span>
```
Get-AzAppServicePlanMetric [-Metrics] <String[]> [-StartTime] <DateTime> [[-EndTime] <DateTime>]
 [-Granularity] <String> [-InstanceDetails] [-AppServicePlan] <PSAppServicePlan>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="75124-106">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="75124-106">DESCRIPTION</span></span>
<span data-ttu-id="75124-107">**AzAppServicePlanMetric** får App Service-planens mått.</span><span class="sxs-lookup"><span data-stu-id="75124-107">The **Get-AzAppServicePlanMetric** gets App Service Plan metrics.</span></span>

## <span data-ttu-id="75124-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="75124-108">EXAMPLES</span></span>

### <span data-ttu-id="75124-109">9.1</span><span class="sxs-lookup"><span data-stu-id="75124-109">1:</span></span>
```
PS C:\>Get-AzAppServicePlanMetric -ResourceGroupName "Default-Web-WestUS" -Name "ContosoAppServPlan" -StartTime 2016-11-30T22:00:00Z -EndTime 2016-11-30T22:30:00Z -Granularity PT1M -Metrics "CPU Percentage"
```

<span data-ttu-id="75124-110">Det här kommandot får CPU-procent för App Service-planen per minut (PT1M-avsöknings tid 1 minut) mellan StartTime och slut värde</span><span class="sxs-lookup"><span data-stu-id="75124-110">This command gets CPU percentage of the App Service Plan per minute(PT1M - Poll Time 1 minute) between StartTime and EndTime</span></span>

## <span data-ttu-id="75124-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="75124-111">PARAMETERS</span></span>

### <span data-ttu-id="75124-112">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="75124-112">-AppServicePlan</span></span>
<span data-ttu-id="75124-113">App Service plan-objekt</span><span class="sxs-lookup"><span data-stu-id="75124-113">App Service Plan Object</span></span>

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

### <span data-ttu-id="75124-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="75124-114">-DefaultProfile</span></span>
<span data-ttu-id="75124-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="75124-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="75124-116">-Slut tid</span><span class="sxs-lookup"><span data-stu-id="75124-116">-EndTime</span></span>
<span data-ttu-id="75124-117">Slut tid i UTC</span><span class="sxs-lookup"><span data-stu-id="75124-117">End Time in UTC</span></span>

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

### <span data-ttu-id="75124-118">-Granularitet</span><span class="sxs-lookup"><span data-stu-id="75124-118">-Granularity</span></span>
<span data-ttu-id="75124-119">Granularitet</span><span class="sxs-lookup"><span data-stu-id="75124-119">Granularity</span></span>

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

### <span data-ttu-id="75124-120">-InstanceDetails</span><span class="sxs-lookup"><span data-stu-id="75124-120">-InstanceDetails</span></span>
<span data-ttu-id="75124-121">Instans Detaljer</span><span class="sxs-lookup"><span data-stu-id="75124-121">Instance Details</span></span>

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

### <span data-ttu-id="75124-122">-Mått</span><span class="sxs-lookup"><span data-stu-id="75124-122">-Metrics</span></span>
<span data-ttu-id="75124-123">Mått</span><span class="sxs-lookup"><span data-stu-id="75124-123">Metrics</span></span>

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

### <span data-ttu-id="75124-124">-Namn</span><span class="sxs-lookup"><span data-stu-id="75124-124">-Name</span></span>
<span data-ttu-id="75124-125">Namn på App Service-abonnemang</span><span class="sxs-lookup"><span data-stu-id="75124-125">App Service Plan Name</span></span>

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

### <span data-ttu-id="75124-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="75124-126">-ResourceGroupName</span></span>
<span data-ttu-id="75124-127">Resurs grupps namn</span><span class="sxs-lookup"><span data-stu-id="75124-127">Resource Group Name</span></span>

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

### <span data-ttu-id="75124-128">-StartTime</span><span class="sxs-lookup"><span data-stu-id="75124-128">-StartTime</span></span>
<span data-ttu-id="75124-129">Start tid i UTC</span><span class="sxs-lookup"><span data-stu-id="75124-129">Start Time in UTC</span></span>

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

### <span data-ttu-id="75124-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="75124-130">CommonParameters</span></span>
<span data-ttu-id="75124-131">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="75124-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="75124-132">Mer information finns i [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="75124-132">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="75124-133">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="75124-133">INPUTS</span></span>

### <span data-ttu-id="75124-134">Microsoft. Azure. commands. webapps. Models. WebApp. PSAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="75124-134">Microsoft.Azure.Commands.WebApps.Models.WebApp.PSAppServicePlan</span></span>

## <span data-ttu-id="75124-135">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="75124-135">OUTPUTS</span></span>

### <span data-ttu-id="75124-136">Microsoft. Azure. Management. webbplatser. Models. ResourceMetric</span><span class="sxs-lookup"><span data-stu-id="75124-136">Microsoft.Azure.Management.WebSites.Models.ResourceMetric</span></span>

## <span data-ttu-id="75124-137">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="75124-137">NOTES</span></span>

## <span data-ttu-id="75124-138">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="75124-138">RELATED LINKS</span></span>
