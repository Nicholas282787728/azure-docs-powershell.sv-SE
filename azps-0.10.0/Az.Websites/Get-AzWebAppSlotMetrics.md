---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.WebSites
ms.assetid: 3BCEADF3-15DC-4033-A94A-4C8B4F5E7340
online version: https://docs.microsoft.com/en-us/powershell/module/Az.websites/get-Azwebappslotmetrics
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Websites/Websites/help/Get-AzWebAppSlotMetrics.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Websites/Websites/help/Get-AzWebAppSlotMetrics.md
ms.openlocfilehash: 474f5a450adba9f01ef56fe99875d062ece1689d
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93923338"
---
# <span data-ttu-id="fc9a6-101">Get-AzWebAppSlotMetrics</span><span class="sxs-lookup"><span data-stu-id="fc9a6-101">Get-AzWebAppSlotMetrics</span></span>

## <span data-ttu-id="fc9a6-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="fc9a6-102">SYNOPSIS</span></span>
<span data-ttu-id="fc9a6-103">Hämtar mått för en Azure Web App-plats.</span><span class="sxs-lookup"><span data-stu-id="fc9a6-103">Gets metrics for an Azure Web App slot.</span></span>

## <span data-ttu-id="fc9a6-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="fc9a6-104">SYNTAX</span></span>

### <span data-ttu-id="fc9a6-105">S</span><span class="sxs-lookup"><span data-stu-id="fc9a6-105">S1</span></span>
```
Get-AzWebAppSlotMetrics [-Metrics] <String[]> [-StartTime] <DateTime> [[-EndTime] <DateTime>]
 [-Granularity] <String> [-InstanceDetails] [-ResourceGroupName] <String> [-Name] <String> [-Slot] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fc9a6-106">S2</span><span class="sxs-lookup"><span data-stu-id="fc9a6-106">S2</span></span>
```
Get-AzWebAppSlotMetrics [-Metrics] <String[]> [-StartTime] <DateTime> [[-EndTime] <DateTime>]
 [-Granularity] <String> [-InstanceDetails] [-WebApp] <Site> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="fc9a6-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="fc9a6-107">DESCRIPTION</span></span>
<span data-ttu-id="fc9a6-108">**Get-AzWebAppSlotMetrics** hämtar webb programmets mått för den angivna platsen.</span><span class="sxs-lookup"><span data-stu-id="fc9a6-108">The **Get-AzWebAppSlotMetrics** gets Web App metrics for the specified slot.</span></span>

## <span data-ttu-id="fc9a6-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="fc9a6-109">EXAMPLES</span></span>

### <span data-ttu-id="fc9a6-110">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="fc9a6-110">Example 1</span></span>
```
PS C:\> Get-AzAppServicePlanMetrics -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -StartTime 2016-11-30T22:00:00Z -EndTime 2016-11-30T22:30:00Z -Granularity PT1M -Metrics ["Requests"]
```

<span data-ttu-id="fc9a6-111">Det här kommandot får begäran av det angivna webb programmet per minut (PT1M-omröstningen</span><span class="sxs-lookup"><span data-stu-id="fc9a6-111">This command gets Request of the specified Web App per minute(PT1M - Poll Time 1 minute) between StartTime and EndTime</span></span>

## <span data-ttu-id="fc9a6-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="fc9a6-112">PARAMETERS</span></span>

### <span data-ttu-id="fc9a6-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fc9a6-113">-DefaultProfile</span></span>
<span data-ttu-id="fc9a6-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="fc9a6-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fc9a6-115">-Slut tid</span><span class="sxs-lookup"><span data-stu-id="fc9a6-115">-EndTime</span></span>
<span data-ttu-id="fc9a6-116">Slut tid i UTC</span><span class="sxs-lookup"><span data-stu-id="fc9a6-116">End Time in UTC</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fc9a6-117">-Granularitet</span><span class="sxs-lookup"><span data-stu-id="fc9a6-117">-Granularity</span></span>
<span data-ttu-id="fc9a6-118">Granularitet</span><span class="sxs-lookup"><span data-stu-id="fc9a6-118">Granularity</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fc9a6-119">-InstanceDetails</span><span class="sxs-lookup"><span data-stu-id="fc9a6-119">-InstanceDetails</span></span>
<span data-ttu-id="fc9a6-120">Instans Detaljer</span><span class="sxs-lookup"><span data-stu-id="fc9a6-120">Instance Details</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fc9a6-121">-Mått</span><span class="sxs-lookup"><span data-stu-id="fc9a6-121">-Metrics</span></span>
<span data-ttu-id="fc9a6-122">Mått</span><span class="sxs-lookup"><span data-stu-id="fc9a6-122">Metrics</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fc9a6-123">-Namn</span><span class="sxs-lookup"><span data-stu-id="fc9a6-123">-Name</span></span>
<span data-ttu-id="fc9a6-124">WebApp-namn</span><span class="sxs-lookup"><span data-stu-id="fc9a6-124">WebApp Name</span></span>

```yaml
Type: String
Parameter Sets: S1
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fc9a6-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fc9a6-125">-ResourceGroupName</span></span>
<span data-ttu-id="fc9a6-126">Resurs grupps namn</span><span class="sxs-lookup"><span data-stu-id="fc9a6-126">Resource Group Name</span></span>

```yaml
Type: String
Parameter Sets: S1
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fc9a6-127">-Plats</span><span class="sxs-lookup"><span data-stu-id="fc9a6-127">-Slot</span></span>
<span data-ttu-id="fc9a6-128">WebApp-slot</span><span class="sxs-lookup"><span data-stu-id="fc9a6-128">WebApp Slot Name</span></span>

```yaml
Type: String
Parameter Sets: S1
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fc9a6-129">-StartTime</span><span class="sxs-lookup"><span data-stu-id="fc9a6-129">-StartTime</span></span>
<span data-ttu-id="fc9a6-130">Start tid i UTC</span><span class="sxs-lookup"><span data-stu-id="fc9a6-130">Start Time in UTC</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: True
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fc9a6-131">-WebApp</span><span class="sxs-lookup"><span data-stu-id="fc9a6-131">-WebApp</span></span>
<span data-ttu-id="fc9a6-132">WebApp-objekt</span><span class="sxs-lookup"><span data-stu-id="fc9a6-132">WebApp Object</span></span>

```yaml
Type: Site
Parameter Sets: S2
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="fc9a6-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fc9a6-133">CommonParameters</span></span>
<span data-ttu-id="fc9a6-134">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fc9a6-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fc9a6-135">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fc9a6-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fc9a6-136">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="fc9a6-136">INPUTS</span></span>

### <span data-ttu-id="fc9a6-137">Webbplatsmallar</span><span class="sxs-lookup"><span data-stu-id="fc9a6-137">Site</span></span>
<span data-ttu-id="fc9a6-138">Parametern ' WebApp ' godkänner värdet av typen ' site ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="fc9a6-138">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="fc9a6-139">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="fc9a6-139">OUTPUTS</span></span>

## <span data-ttu-id="fc9a6-140">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="fc9a6-140">NOTES</span></span>

## <span data-ttu-id="fc9a6-141">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="fc9a6-141">RELATED LINKS</span></span>

[<span data-ttu-id="fc9a6-142">Get-AzAppServicePlanMetrics</span><span class="sxs-lookup"><span data-stu-id="fc9a6-142">Get-AzAppServicePlanMetrics</span></span>](./Get-AzAppServicePlanMetrics.md)

[<span data-ttu-id="fc9a6-143">Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="fc9a6-143">Get-AzWebApp</span></span>](./Get-AzWebApp.md)

[<span data-ttu-id="fc9a6-144">Get-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="fc9a6-144">Get-AzWebAppSlot</span></span>](./Get-AzWebAppSlot.md)
