---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.Websites
ms.assetid: 3BCEADF3-15DC-4033-A94A-4C8B4F5E7340
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/get-azurermwebappslotmetrics
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Get-AzureRmWebAppSlotMetrics.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Get-AzureRmWebAppSlotMetrics.md
ms.openlocfilehash: 9c336c1bb2c2485c5bef691a5d5560a1b8795360
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93572556"
---
# <span data-ttu-id="895e2-101">Get-AzureRmWebAppSlotMetrics</span><span class="sxs-lookup"><span data-stu-id="895e2-101">Get-AzureRmWebAppSlotMetrics</span></span>

## <span data-ttu-id="895e2-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="895e2-102">SYNOPSIS</span></span>
<span data-ttu-id="895e2-103">Hämtar mått för en Azure Web App-plats.</span><span class="sxs-lookup"><span data-stu-id="895e2-103">Gets metrics for an Azure Web App slot.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="895e2-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="895e2-104">SYNTAX</span></span>

### <span data-ttu-id="895e2-105">S</span><span class="sxs-lookup"><span data-stu-id="895e2-105">S1</span></span>
```
Get-AzureRmWebAppSlotMetrics [-Metrics] <String[]> [-StartTime] <DateTime> [[-EndTime] <DateTime>]
 [-Granularity] <String> [-InstanceDetails] [-ResourceGroupName] <String> [-Name] <String> [-Slot] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="895e2-106">S2</span><span class="sxs-lookup"><span data-stu-id="895e2-106">S2</span></span>
```
Get-AzureRmWebAppSlotMetrics [-Metrics] <String[]> [-StartTime] <DateTime> [[-EndTime] <DateTime>]
 [-Granularity] <String> [-InstanceDetails] [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="895e2-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="895e2-107">DESCRIPTION</span></span>
<span data-ttu-id="895e2-108">**Get-AzureRmWebAppSlotMetrics** hämtar webb programmets mått för den angivna platsen.</span><span class="sxs-lookup"><span data-stu-id="895e2-108">The **Get-AzureRmWebAppSlotMetrics** gets Web App metrics for the specified slot.</span></span>

## <span data-ttu-id="895e2-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="895e2-109">EXAMPLES</span></span>

### <span data-ttu-id="895e2-110">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="895e2-110">Example 1</span></span>
```
PS C:\> Get-AzureRmAppServicePlanMetrics -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -StartTime 2016-11-30T22:00:00Z -EndTime 2016-11-30T22:30:00Z -Granularity PT1M -Metrics ["Requests"]
```

<span data-ttu-id="895e2-111">Det här kommandot får begäran av det angivna webb programmet per minut (PT1M-omröstningen</span><span class="sxs-lookup"><span data-stu-id="895e2-111">This command gets Request of the specified Web App per minute(PT1M - Poll Time 1 minute) between StartTime and EndTime</span></span>

## <span data-ttu-id="895e2-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="895e2-112">PARAMETERS</span></span>

### <span data-ttu-id="895e2-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="895e2-113">-DefaultProfile</span></span>
<span data-ttu-id="895e2-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="895e2-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="895e2-115">-Slut tid</span><span class="sxs-lookup"><span data-stu-id="895e2-115">-EndTime</span></span>
<span data-ttu-id="895e2-116">Slut tid i UTC</span><span class="sxs-lookup"><span data-stu-id="895e2-116">End Time in UTC</span></span>

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

### <span data-ttu-id="895e2-117">-Granularitet</span><span class="sxs-lookup"><span data-stu-id="895e2-117">-Granularity</span></span>
<span data-ttu-id="895e2-118">Granularitet</span><span class="sxs-lookup"><span data-stu-id="895e2-118">Granularity</span></span>

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

### <span data-ttu-id="895e2-119">-InstanceDetails</span><span class="sxs-lookup"><span data-stu-id="895e2-119">-InstanceDetails</span></span>
<span data-ttu-id="895e2-120">Instans Detaljer</span><span class="sxs-lookup"><span data-stu-id="895e2-120">Instance Details</span></span>

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

### <span data-ttu-id="895e2-121">-Mått</span><span class="sxs-lookup"><span data-stu-id="895e2-121">-Metrics</span></span>
<span data-ttu-id="895e2-122">Mått</span><span class="sxs-lookup"><span data-stu-id="895e2-122">Metrics</span></span>

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

### <span data-ttu-id="895e2-123">-Namn</span><span class="sxs-lookup"><span data-stu-id="895e2-123">-Name</span></span>
<span data-ttu-id="895e2-124">WebApp-namn</span><span class="sxs-lookup"><span data-stu-id="895e2-124">WebApp Name</span></span>

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

### <span data-ttu-id="895e2-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="895e2-125">-ResourceGroupName</span></span>
<span data-ttu-id="895e2-126">Resurs grupps namn</span><span class="sxs-lookup"><span data-stu-id="895e2-126">Resource Group Name</span></span>

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

### <span data-ttu-id="895e2-127">-Plats</span><span class="sxs-lookup"><span data-stu-id="895e2-127">-Slot</span></span>
<span data-ttu-id="895e2-128">WebApp-slot</span><span class="sxs-lookup"><span data-stu-id="895e2-128">WebApp Slot Name</span></span>

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

### <span data-ttu-id="895e2-129">-StartTime</span><span class="sxs-lookup"><span data-stu-id="895e2-129">-StartTime</span></span>
<span data-ttu-id="895e2-130">Start tid i UTC</span><span class="sxs-lookup"><span data-stu-id="895e2-130">Start Time in UTC</span></span>

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

### <span data-ttu-id="895e2-131">-WebApp</span><span class="sxs-lookup"><span data-stu-id="895e2-131">-WebApp</span></span>
<span data-ttu-id="895e2-132">WebApp-objekt</span><span class="sxs-lookup"><span data-stu-id="895e2-132">WebApp Object</span></span>

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

### <span data-ttu-id="895e2-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="895e2-133">CommonParameters</span></span>
<span data-ttu-id="895e2-134">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="895e2-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="895e2-135">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="895e2-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="895e2-136">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="895e2-136">INPUTS</span></span>

### <span data-ttu-id="895e2-137">System. String</span><span class="sxs-lookup"><span data-stu-id="895e2-137">System.String</span></span>

### <span data-ttu-id="895e2-138">Microsoft. Azure. Management. webbplatser. Models. site</span><span class="sxs-lookup"><span data-stu-id="895e2-138">Microsoft.Azure.Management.WebSites.Models.Site</span></span>
<span data-ttu-id="895e2-139">Parametrar: WebApp (ByValue)</span><span class="sxs-lookup"><span data-stu-id="895e2-139">Parameters: WebApp (ByValue)</span></span>

## <span data-ttu-id="895e2-140">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="895e2-140">OUTPUTS</span></span>

### <span data-ttu-id="895e2-141">Microsoft. Azure. Management. webbplatser. Models. ResourceMetric</span><span class="sxs-lookup"><span data-stu-id="895e2-141">Microsoft.Azure.Management.WebSites.Models.ResourceMetric</span></span>

## <span data-ttu-id="895e2-142">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="895e2-142">NOTES</span></span>

## <span data-ttu-id="895e2-143">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="895e2-143">RELATED LINKS</span></span>

[<span data-ttu-id="895e2-144">Get-AzureRMAppServicePlanMetrics</span><span class="sxs-lookup"><span data-stu-id="895e2-144">Get-AzureRMAppServicePlanMetrics</span></span>](./Get-AzureRmAppServicePlanMetrics.md)

[<span data-ttu-id="895e2-145">Get-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="895e2-145">Get-AzureRmWebApp</span></span>](./Get-AzureRmWebApp.md)

[<span data-ttu-id="895e2-146">Get-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="895e2-146">Get-AzureRMWebAppSlot</span></span>](./Get-AzureRMWebAppSlot.md)
