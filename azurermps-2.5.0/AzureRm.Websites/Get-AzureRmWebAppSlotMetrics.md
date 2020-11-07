---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.WebSites
ms.assetid: 3BCEADF3-15DC-4033-A94A-4C8B4F5E7340
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/get-azurermwebappslotmetrics
schema: 2.0.0
ms.openlocfilehash: 9393a2aebbde94dcb42989e80b2763198576f408
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93930461"
---
# <span data-ttu-id="d32c9-101">Get-AzureRmWebAppSlotMetrics</span><span class="sxs-lookup"><span data-stu-id="d32c9-101">Get-AzureRmWebAppSlotMetrics</span></span>

## <span data-ttu-id="d32c9-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="d32c9-102">SYNOPSIS</span></span>
<span data-ttu-id="d32c9-103">Hämtar mått för en Azure Web App-plats.</span><span class="sxs-lookup"><span data-stu-id="d32c9-103">Gets metrics for an Azure Web App slot.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d32c9-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="d32c9-104">SYNTAX</span></span>

### <span data-ttu-id="d32c9-105">S</span><span class="sxs-lookup"><span data-stu-id="d32c9-105">S1</span></span>
```
Get-AzureRmWebAppSlotMetrics [-Metrics] <String[]> [-StartTime] <DateTime> [[-EndTime] <DateTime>]
 [-Granularity] <String> [-InstanceDetails] [-ResourceGroupName] <String> [-Name] <String> [-Slot] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d32c9-106">S2</span><span class="sxs-lookup"><span data-stu-id="d32c9-106">S2</span></span>
```
Get-AzureRmWebAppSlotMetrics [-Metrics] <String[]> [-StartTime] <DateTime> [[-EndTime] <DateTime>]
 [-Granularity] <String> [-InstanceDetails] [-WebApp] <Site> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="d32c9-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="d32c9-107">DESCRIPTION</span></span>
<span data-ttu-id="d32c9-108">**Get-AzureRmWebAppSlotMetrics** hämtar webb programmets mått för den angivna platsen.</span><span class="sxs-lookup"><span data-stu-id="d32c9-108">The **Get-AzureRmWebAppSlotMetrics** gets Web App metrics for the specified slot.</span></span>

## <span data-ttu-id="d32c9-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="d32c9-109">EXAMPLES</span></span>

### <span data-ttu-id="d32c9-110">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="d32c9-110">Example 1</span></span>
```
PS C:\> Get-AzureRmAppServicePlanMetrics -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -StartTime 2016-11-30T22:00:00Z -EndTime 2016-11-30T22:30:00Z -Granularity PT1M -Metrics ["Requests"]
```

<span data-ttu-id="d32c9-111">Det här kommandot får begäran av det angivna webb programmet per minut (PT1M-omröstningen</span><span class="sxs-lookup"><span data-stu-id="d32c9-111">This command gets Request of the specified Web App per minute(PT1M - Poll Time 1 minute) between StartTime and EndTime</span></span>

## <span data-ttu-id="d32c9-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="d32c9-112">PARAMETERS</span></span>

### <span data-ttu-id="d32c9-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d32c9-113">-DefaultProfile</span></span>
<span data-ttu-id="d32c9-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="d32c9-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d32c9-115">-Slut tid</span><span class="sxs-lookup"><span data-stu-id="d32c9-115">-EndTime</span></span>
<span data-ttu-id="d32c9-116">Slut tid i UTC</span><span class="sxs-lookup"><span data-stu-id="d32c9-116">End Time in UTC</span></span>

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

### <span data-ttu-id="d32c9-117">-Granularitet</span><span class="sxs-lookup"><span data-stu-id="d32c9-117">-Granularity</span></span>
<span data-ttu-id="d32c9-118">Granularitet</span><span class="sxs-lookup"><span data-stu-id="d32c9-118">Granularity</span></span>

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

### <span data-ttu-id="d32c9-119">-InstanceDetails</span><span class="sxs-lookup"><span data-stu-id="d32c9-119">-InstanceDetails</span></span>
<span data-ttu-id="d32c9-120">Instans Detaljer</span><span class="sxs-lookup"><span data-stu-id="d32c9-120">Instance Details</span></span>

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

### <span data-ttu-id="d32c9-121">-Mått</span><span class="sxs-lookup"><span data-stu-id="d32c9-121">-Metrics</span></span>
<span data-ttu-id="d32c9-122">Mått</span><span class="sxs-lookup"><span data-stu-id="d32c9-122">Metrics</span></span>

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

### <span data-ttu-id="d32c9-123">-Namn</span><span class="sxs-lookup"><span data-stu-id="d32c9-123">-Name</span></span>
<span data-ttu-id="d32c9-124">WebApp-namn</span><span class="sxs-lookup"><span data-stu-id="d32c9-124">WebApp Name</span></span>

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

### <span data-ttu-id="d32c9-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d32c9-125">-ResourceGroupName</span></span>
<span data-ttu-id="d32c9-126">Resurs grupps namn</span><span class="sxs-lookup"><span data-stu-id="d32c9-126">Resource Group Name</span></span>

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

### <span data-ttu-id="d32c9-127">-Plats</span><span class="sxs-lookup"><span data-stu-id="d32c9-127">-Slot</span></span>
<span data-ttu-id="d32c9-128">WebApp-slot</span><span class="sxs-lookup"><span data-stu-id="d32c9-128">WebApp Slot Name</span></span>

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

### <span data-ttu-id="d32c9-129">-StartTime</span><span class="sxs-lookup"><span data-stu-id="d32c9-129">-StartTime</span></span>
<span data-ttu-id="d32c9-130">Start tid i UTC</span><span class="sxs-lookup"><span data-stu-id="d32c9-130">Start Time in UTC</span></span>

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

### <span data-ttu-id="d32c9-131">-WebApp</span><span class="sxs-lookup"><span data-stu-id="d32c9-131">-WebApp</span></span>
<span data-ttu-id="d32c9-132">WebApp-objekt</span><span class="sxs-lookup"><span data-stu-id="d32c9-132">WebApp Object</span></span>

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

### <span data-ttu-id="d32c9-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d32c9-133">CommonParameters</span></span>
<span data-ttu-id="d32c9-134">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d32c9-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d32c9-135">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d32c9-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d32c9-136">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="d32c9-136">INPUTS</span></span>

### <span data-ttu-id="d32c9-137">Webbplatsmallar</span><span class="sxs-lookup"><span data-stu-id="d32c9-137">Site</span></span>
<span data-ttu-id="d32c9-138">Parametern ' WebApp ' godkänner värdet av typen ' site ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="d32c9-138">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="d32c9-139">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="d32c9-139">OUTPUTS</span></span>

## <span data-ttu-id="d32c9-140">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="d32c9-140">NOTES</span></span>

## <span data-ttu-id="d32c9-141">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="d32c9-141">RELATED LINKS</span></span>

[<span data-ttu-id="d32c9-142">Get-AzureRMAppServicePlanMetrics</span><span class="sxs-lookup"><span data-stu-id="d32c9-142">Get-AzureRMAppServicePlanMetrics</span></span>](./Get-AzureRmAppServicePlanMetrics.md)

[<span data-ttu-id="d32c9-143">Get-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="d32c9-143">Get-AzureRmWebApp</span></span>](./Get-AzureRmWebApp.md)

[<span data-ttu-id="d32c9-144">Get-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="d32c9-144">Get-AzureRMWebAppSlot</span></span>](./Get-AzureRMWebAppSlot.md)
