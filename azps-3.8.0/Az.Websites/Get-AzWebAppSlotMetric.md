---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: 3BCEADF3-15DC-4033-A94A-4C8B4F5E7340
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/get-azwebappslotmetric
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppSlotMetric.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppSlotMetric.md
ms.openlocfilehash: 27800007756f8de91f23feab2f3cc1bd5206aa76
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94089573"
---
# <span data-ttu-id="de3a3-101">Get-AzWebAppSlotMetric</span><span class="sxs-lookup"><span data-stu-id="de3a3-101">Get-AzWebAppSlotMetric</span></span>

## <span data-ttu-id="de3a3-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="de3a3-102">SYNOPSIS</span></span>
<span data-ttu-id="de3a3-103">Hämtar mått för en Azure Web App-plats.</span><span class="sxs-lookup"><span data-stu-id="de3a3-103">Gets metrics for an Azure Web App slot.</span></span>

## <span data-ttu-id="de3a3-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="de3a3-104">SYNTAX</span></span>

### <span data-ttu-id="de3a3-105">S</span><span class="sxs-lookup"><span data-stu-id="de3a3-105">S1</span></span>
```
Get-AzWebAppSlotMetric [-Metrics] <String[]> [-StartTime] <DateTime> [[-EndTime] <DateTime>]
 [-Granularity] <String> [-InstanceDetails] [-ResourceGroupName] <String> [-Name] <String> [-Slot] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="de3a3-106">S2</span><span class="sxs-lookup"><span data-stu-id="de3a3-106">S2</span></span>
```
Get-AzWebAppSlotMetric [-Metrics] <String[]> [-StartTime] <DateTime> [[-EndTime] <DateTime>]
 [-Granularity] <String> [-InstanceDetails] [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="de3a3-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="de3a3-107">DESCRIPTION</span></span>
<span data-ttu-id="de3a3-108">**Get-AzWebAppSlotMetric** hämtar webb programmets mått för den angivna platsen.</span><span class="sxs-lookup"><span data-stu-id="de3a3-108">The **Get-AzWebAppSlotMetric** gets Web App metrics for the specified slot.</span></span>

## <span data-ttu-id="de3a3-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="de3a3-109">EXAMPLES</span></span>

### <span data-ttu-id="de3a3-110">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="de3a3-110">Example 1</span></span>
```
PS C:\> Get-AzWebAppSlotMetric -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -StartTime 2016-11-30T22:00:00Z -EndTime 2016-11-30T22:30:00Z -Granularity PT1M -Metrics ["Requests"]
```

<span data-ttu-id="de3a3-111">Det här kommandot får begäran av det angivna webb programmet per minut (PT1M-omröstningen</span><span class="sxs-lookup"><span data-stu-id="de3a3-111">This command gets Request of the specified Web App per minute(PT1M - Poll Time 1 minute) between StartTime and EndTime</span></span>

## <span data-ttu-id="de3a3-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="de3a3-112">PARAMETERS</span></span>

### <span data-ttu-id="de3a3-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="de3a3-113">-DefaultProfile</span></span>
<span data-ttu-id="de3a3-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="de3a3-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="de3a3-115">-Slut tid</span><span class="sxs-lookup"><span data-stu-id="de3a3-115">-EndTime</span></span>
<span data-ttu-id="de3a3-116">Slut tid i UTC</span><span class="sxs-lookup"><span data-stu-id="de3a3-116">End Time in UTC</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="de3a3-117">-Granularitet</span><span class="sxs-lookup"><span data-stu-id="de3a3-117">-Granularity</span></span>
<span data-ttu-id="de3a3-118">Granularitet</span><span class="sxs-lookup"><span data-stu-id="de3a3-118">Granularity</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="de3a3-119">-InstanceDetails</span><span class="sxs-lookup"><span data-stu-id="de3a3-119">-InstanceDetails</span></span>
<span data-ttu-id="de3a3-120">Instans Detaljer</span><span class="sxs-lookup"><span data-stu-id="de3a3-120">Instance Details</span></span>

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

### <span data-ttu-id="de3a3-121">-Mått</span><span class="sxs-lookup"><span data-stu-id="de3a3-121">-Metrics</span></span>
<span data-ttu-id="de3a3-122">Mått</span><span class="sxs-lookup"><span data-stu-id="de3a3-122">Metrics</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="de3a3-123">-Namn</span><span class="sxs-lookup"><span data-stu-id="de3a3-123">-Name</span></span>
<span data-ttu-id="de3a3-124">WebApp-namn</span><span class="sxs-lookup"><span data-stu-id="de3a3-124">WebApp Name</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="de3a3-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="de3a3-125">-ResourceGroupName</span></span>
<span data-ttu-id="de3a3-126">Resurs grupps namn</span><span class="sxs-lookup"><span data-stu-id="de3a3-126">Resource Group Name</span></span>

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

### <span data-ttu-id="de3a3-127">-Plats</span><span class="sxs-lookup"><span data-stu-id="de3a3-127">-Slot</span></span>
<span data-ttu-id="de3a3-128">WebApp-slot</span><span class="sxs-lookup"><span data-stu-id="de3a3-128">WebApp Slot Name</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="de3a3-129">-StartTime</span><span class="sxs-lookup"><span data-stu-id="de3a3-129">-StartTime</span></span>
<span data-ttu-id="de3a3-130">Start tid i UTC</span><span class="sxs-lookup"><span data-stu-id="de3a3-130">Start Time in UTC</span></span>

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: True
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="de3a3-131">-WebApp</span><span class="sxs-lookup"><span data-stu-id="de3a3-131">-WebApp</span></span>
<span data-ttu-id="de3a3-132">WebApp-objekt</span><span class="sxs-lookup"><span data-stu-id="de3a3-132">WebApp Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.WebApps.Models.PSSite
Parameter Sets: S2
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="de3a3-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="de3a3-133">CommonParameters</span></span>
<span data-ttu-id="de3a3-134">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="de3a3-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="de3a3-135">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="de3a3-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="de3a3-136">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="de3a3-136">INPUTS</span></span>

### <span data-ttu-id="de3a3-137">System. String</span><span class="sxs-lookup"><span data-stu-id="de3a3-137">System.String</span></span>

### <span data-ttu-id="de3a3-138">Microsoft. Azure. commands. webapps. Models. PSSite</span><span class="sxs-lookup"><span data-stu-id="de3a3-138">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="de3a3-139">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="de3a3-139">OUTPUTS</span></span>

### <span data-ttu-id="de3a3-140">Microsoft. Azure. Management. webbplatser. Models. ResourceMetric</span><span class="sxs-lookup"><span data-stu-id="de3a3-140">Microsoft.Azure.Management.WebSites.Models.ResourceMetric</span></span>

## <span data-ttu-id="de3a3-141">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="de3a3-141">NOTES</span></span>

## <span data-ttu-id="de3a3-142">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="de3a3-142">RELATED LINKS</span></span>

[<span data-ttu-id="de3a3-143">Get-AzAppServicePlanMetric</span><span class="sxs-lookup"><span data-stu-id="de3a3-143">Get-AzAppServicePlanMetric</span></span>](./Get-AzAppServicePlanMetric.md)

[<span data-ttu-id="de3a3-144">Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="de3a3-144">Get-AzWebApp</span></span>](./Get-AzWebApp.md)

[<span data-ttu-id="de3a3-145">Get-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="de3a3-145">Get-AzWebAppSlot</span></span>](./Get-AzWebAppSlot.md)
