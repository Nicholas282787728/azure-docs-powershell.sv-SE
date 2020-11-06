---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.Websites
ms.assetid: 3BCEADF3-15DC-4033-A94A-4C8B4F5E7340
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Get-AzureRmWebAppSlotMetrics.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Get-AzureRmWebAppSlotMetrics.md
ms.openlocfilehash: 93af61d0554435fae4b9d87170b9202026644e49
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93584500"
---
# <span data-ttu-id="6a397-101">Get-AzureRmWebAppSlotMetrics</span><span class="sxs-lookup"><span data-stu-id="6a397-101">Get-AzureRmWebAppSlotMetrics</span></span>

## <span data-ttu-id="6a397-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="6a397-102">SYNOPSIS</span></span>
<span data-ttu-id="6a397-103">Hämtar mått för en Azure Web App-plats.</span><span class="sxs-lookup"><span data-stu-id="6a397-103">Gets metrics for an Azure Web App slot.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6a397-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="6a397-104">SYNTAX</span></span>

### <span data-ttu-id="6a397-105">S</span><span class="sxs-lookup"><span data-stu-id="6a397-105">S1</span></span>
```
Get-AzureRmWebAppSlotMetrics [-Metrics] <String[]> [-StartTime] <DateTime> [[-EndTime] <DateTime>]
 [-Granularity] <String> [-InstanceDetails] [-ResourceGroupName] <String> [-Name] <String> [-Slot] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6a397-106">S2</span><span class="sxs-lookup"><span data-stu-id="6a397-106">S2</span></span>
```
Get-AzureRmWebAppSlotMetrics [-Metrics] <String[]> [-StartTime] <DateTime> [[-EndTime] <DateTime>]
 [-Granularity] <String> [-InstanceDetails] [-WebApp] <Site> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="6a397-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="6a397-107">DESCRIPTION</span></span>
<span data-ttu-id="6a397-108">**Get-AzureRmWebAppSlotMetrics** hämtar webb programmets mått för den angivna platsen.</span><span class="sxs-lookup"><span data-stu-id="6a397-108">The **Get-AzureRmWebAppSlotMetrics** gets Web App metrics for the specified slot.</span></span>

## <span data-ttu-id="6a397-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="6a397-109">EXAMPLES</span></span>

### <span data-ttu-id="6a397-110">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="6a397-110">Example 1</span></span>
```
PS C:\> Get-AzureRmAppServicePlanMetrics -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -StartTime 2016-11-30T22:00:00Z -EndTime 2016-11-30T22:30:00Z -Granularity PT1M -Metrics ["Requests"]
```

<span data-ttu-id="6a397-111">Det här kommandot får begäran av det angivna webb programmet per minut (PT1M-omröstningen</span><span class="sxs-lookup"><span data-stu-id="6a397-111">This command gets Request of the specified Web App per minute(PT1M - Poll Time 1 minute) between StartTime and EndTime</span></span>

## <span data-ttu-id="6a397-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="6a397-112">PARAMETERS</span></span>

### <span data-ttu-id="6a397-113">-Slut tid</span><span class="sxs-lookup"><span data-stu-id="6a397-113">-EndTime</span></span>
<span data-ttu-id="6a397-114">Slut tid i UTC</span><span class="sxs-lookup"><span data-stu-id="6a397-114">End Time in UTC</span></span>

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

### <span data-ttu-id="6a397-115">-Granularitet</span><span class="sxs-lookup"><span data-stu-id="6a397-115">-Granularity</span></span>
<span data-ttu-id="6a397-116">Granularitet</span><span class="sxs-lookup"><span data-stu-id="6a397-116">Granularity</span></span>

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

### <span data-ttu-id="6a397-117">-InstanceDetails</span><span class="sxs-lookup"><span data-stu-id="6a397-117">-InstanceDetails</span></span>
<span data-ttu-id="6a397-118">Instans Detaljer</span><span class="sxs-lookup"><span data-stu-id="6a397-118">Instance Details</span></span>

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

### <span data-ttu-id="6a397-119">-Mått</span><span class="sxs-lookup"><span data-stu-id="6a397-119">-Metrics</span></span>
<span data-ttu-id="6a397-120">Mått</span><span class="sxs-lookup"><span data-stu-id="6a397-120">Metrics</span></span>

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

### <span data-ttu-id="6a397-121">-Namn</span><span class="sxs-lookup"><span data-stu-id="6a397-121">-Name</span></span>
<span data-ttu-id="6a397-122">WebApp-namn</span><span class="sxs-lookup"><span data-stu-id="6a397-122">WebApp Name</span></span>

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

### <span data-ttu-id="6a397-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6a397-123">-ResourceGroupName</span></span>
<span data-ttu-id="6a397-124">Resurs grupps namn</span><span class="sxs-lookup"><span data-stu-id="6a397-124">Resource Group Name</span></span>

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

### <span data-ttu-id="6a397-125">-Plats</span><span class="sxs-lookup"><span data-stu-id="6a397-125">-Slot</span></span>
<span data-ttu-id="6a397-126">WebApp-slot</span><span class="sxs-lookup"><span data-stu-id="6a397-126">WebApp Slot Name</span></span>

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

### <span data-ttu-id="6a397-127">-StartTime</span><span class="sxs-lookup"><span data-stu-id="6a397-127">-StartTime</span></span>
<span data-ttu-id="6a397-128">Start tid i UTC</span><span class="sxs-lookup"><span data-stu-id="6a397-128">Start Time in UTC</span></span>

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

### <span data-ttu-id="6a397-129">-WebApp</span><span class="sxs-lookup"><span data-stu-id="6a397-129">-WebApp</span></span>
<span data-ttu-id="6a397-130">WebApp-objekt</span><span class="sxs-lookup"><span data-stu-id="6a397-130">WebApp Object</span></span>

```yaml
Type: Microsoft.Azure.Management.WebSites.Models.Site
Parameter Sets: S2
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6a397-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6a397-131">-DefaultProfile</span></span>
<span data-ttu-id="6a397-132">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="6a397-132">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6a397-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6a397-133">CommonParameters</span></span>
<span data-ttu-id="6a397-134">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6a397-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6a397-135">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6a397-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6a397-136">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="6a397-136">INPUTS</span></span>

### <span data-ttu-id="6a397-137">Webbplatsmallar</span><span class="sxs-lookup"><span data-stu-id="6a397-137">Site</span></span>
<span data-ttu-id="6a397-138">Parametern ' WebApp ' godkänner värdet av typen ' site ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="6a397-138">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="6a397-139">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="6a397-139">OUTPUTS</span></span>

## <span data-ttu-id="6a397-140">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="6a397-140">NOTES</span></span>

## <span data-ttu-id="6a397-141">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="6a397-141">RELATED LINKS</span></span>

[<span data-ttu-id="6a397-142">Get-AzureRMAppServicePlanMetrics</span><span class="sxs-lookup"><span data-stu-id="6a397-142">Get-AzureRMAppServicePlanMetrics</span></span>](./Get-AzureRmAppServicePlanMetrics.md)

[<span data-ttu-id="6a397-143">Get-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="6a397-143">Get-AzureRmWebApp</span></span>](./Get-AzureRmWebApp.md)

[<span data-ttu-id="6a397-144">Get-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="6a397-144">Get-AzureRMWebAppSlot</span></span>](./Get-AzureRMWebAppSlot.md)
