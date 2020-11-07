---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/get-azurermrecoveryservicesasrevent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrEvent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrEvent.md
ms.openlocfilehash: e32f0b1d12b1cb0399ddef04623ac76557c809b5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93581032"
---
# <span data-ttu-id="674c1-101">Get-AzureRmRecoveryServicesAsrEvent</span><span class="sxs-lookup"><span data-stu-id="674c1-101">Get-AzureRmRecoveryServicesAsrEvent</span></span>

## <span data-ttu-id="674c1-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="674c1-102">SYNOPSIS</span></span>
<span data-ttu-id="674c1-103">Hämtar information om Azure Site Recovery-händelser i valvet.</span><span class="sxs-lookup"><span data-stu-id="674c1-103">Gets details of Azure Site Recovery events in the vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="674c1-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="674c1-104">SYNTAX</span></span>

### <span data-ttu-id="674c1-105">ByParam (standard)</span><span class="sxs-lookup"><span data-stu-id="674c1-105">ByParam (Default)</span></span>
```
Get-AzureRmRecoveryServicesAsrEvent [-AffectedObjectFriendlyName <String>] [-Fabric <ASRFabric>]
 [-Severity <String>] [-StartTime <DateTime>] [-EndTime <DateTime>] [-EventType <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="674c1-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="674c1-106">ByResourceId</span></span>
```
Get-AzureRmRecoveryServicesAsrEvent -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="674c1-107">ByFabricId</span><span class="sxs-lookup"><span data-stu-id="674c1-107">ByFabricId</span></span>
```
Get-AzureRmRecoveryServicesAsrEvent -FabricId <String> [-AffectedObjectFriendlyName <String>]
 [-Severity <String>] [-StartTime <DateTime>] [-EndTime <DateTime>] [-EventType <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="674c1-108">ByName</span><span class="sxs-lookup"><span data-stu-id="674c1-108">ByName</span></span>
```
Get-AzureRmRecoveryServicesAsrEvent -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="674c1-109">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="674c1-109">DESCRIPTION</span></span>
<span data-ttu-id="674c1-110">**Get-AzureRmRecoveryServicesAsrEvent** hämtar listan över händelser i valvet baserat på de angivna urvals filtren.</span><span class="sxs-lookup"><span data-stu-id="674c1-110">The **Get-AzureRmRecoveryServicesAsrEvent** gets the list of events in the vault based on the specified selection filters.</span></span>

## <span data-ttu-id="674c1-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="674c1-111">EXAMPLES</span></span>

### <span data-ttu-id="674c1-112">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="674c1-112">Example 1</span></span>
```
PS C:\> Get-AzureRmRecoveryServicesAsrEvent
```

<span data-ttu-id="674c1-113">Lista över alla händelser.</span><span class="sxs-lookup"><span data-stu-id="674c1-113">List of all events.</span></span>

### <span data-ttu-id="674c1-114">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="674c1-114">Example 2</span></span>
```
PS C:\> Get-AzureRmRecoveryServicesAsrEvent -EventName "VmMonitoringEvent;9091897569816476200_84576304-bafc-4714-8ba6-197a5d09d84f"


AffectedObjectFriendlyName   : V2A-W2K12-400
Description                  : Virtual machine health is in Critical state.
EventCode                    : SRSVMHealthChanged
EventSpecificDetails         :
EventType                    : AgentHealth
FabricId                     : /Subscriptions/xxxxxxxxxxxxxxxxx/resourceGroups/xxxxxxxxxxxx/providers/Microsoft.RecoveryServices/vaults/xxxxxxxxxxxxxxxx/replicationFabrics/xxxxxxxxxxxx
HealthErrors                 : {}
Name                         : VmMonitoringEvent;9091897569816476200_84576304-bafc-4714-8ba6-197a5d09d84f
ProviderSpecificEventDetails : Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRInMageAzureV2EventDetails
Severity                     : Critical
TimeOfOccurence              : 8/17/2017 12:31:43 PM
```

<span data-ttu-id="674c1-115">Hämta händelse efter namn.</span><span class="sxs-lookup"><span data-stu-id="674c1-115">Get event by name.</span></span>

### <span data-ttu-id="674c1-116">Exempel 3</span><span class="sxs-lookup"><span data-stu-id="674c1-116">Example 3</span></span>
```
PS C:\> Get-AzureRmRecoveryServicesAsrEvent -AffectedObjectName xxxxxxxxxxxxx
```

<span data-ttu-id="674c1-117">Lista över händelser för påverkade objekt.</span><span class="sxs-lookup"><span data-stu-id="674c1-117">List of event for affected Object.</span></span>

### <span data-ttu-id="674c1-118">Exempel 4</span><span class="sxs-lookup"><span data-stu-id="674c1-118">Example 4</span></span>
```
PS C:\> Get-AzureRmRecoveryServicesAsrEvent -AffectedObjectName xxxxxxxxxxxx -StartTime "8/17/2017 12:31:40 PM" -EndTime "8/17/2017 12:31:44 PM" -Severity Critical -EventType VmHealth
```

<span data-ttu-id="674c1-119">Lista över händelser mellan start tid och slut tid, allvarlighets gradens kritiska och VmHealth.</span><span class="sxs-lookup"><span data-stu-id="674c1-119">List of event between time start time and end time , severity critical and health type VmHealth.</span></span>

## <span data-ttu-id="674c1-120">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="674c1-120">PARAMETERS</span></span>

### <span data-ttu-id="674c1-121">-AffectedObjectFriendlyName</span><span class="sxs-lookup"><span data-stu-id="674c1-121">-AffectedObjectFriendlyName</span></span>
<span data-ttu-id="674c1-122">Anger AffectedObject FriendlyName för sökningen.</span><span class="sxs-lookup"><span data-stu-id="674c1-122">Specifies AffectedObject FriendlyName for the search.</span></span>

```yaml
Type: String
Parameter Sets: ByParam, ByFabricId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="674c1-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="674c1-123">-DefaultProfile</span></span>
<span data-ttu-id="674c1-124">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="674c1-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="674c1-125">-Slut tid</span><span class="sxs-lookup"><span data-stu-id="674c1-125">-EndTime</span></span>
<span data-ttu-id="674c1-126">Anger slut tiden för sökfönstret.</span><span class="sxs-lookup"><span data-stu-id="674c1-126">Specifies the end time of the search window.</span></span> <span data-ttu-id="674c1-127">Använd den här parametern för att endast få händelser som har inträffat före angiven tid.</span><span class="sxs-lookup"><span data-stu-id="674c1-127">Use this parameter to get only those events that have occurred before the specified time.</span></span>

```yaml
Type: DateTime
Parameter Sets: ByParam, ByFabricId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="674c1-128">-EventType</span><span class="sxs-lookup"><span data-stu-id="674c1-128">-EventType</span></span>
<span data-ttu-id="674c1-129">Filtrera händelser efter händelse typ.</span><span class="sxs-lookup"><span data-stu-id="674c1-129">Filter events by the event type.</span></span>

```yaml
Type: String
Parameter Sets: ByParam, ByFabricId
Aliases:
Accepted values: VmHealth, ServerHealth, AgentHealth

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="674c1-130">-Fabric</span><span class="sxs-lookup"><span data-stu-id="674c1-130">-Fabric</span></span>
<span data-ttu-id="674c1-131">Filtrera händelser efter den angivna infrastruktur resursen.</span><span class="sxs-lookup"><span data-stu-id="674c1-131">Filter events by the specified fabric.</span></span>

```yaml
Type: ASRFabric
Parameter Sets: ByParam
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="674c1-132">-FabricId</span><span class="sxs-lookup"><span data-stu-id="674c1-132">-FabricId</span></span>
<span data-ttu-id="674c1-133">Anger den fabricId som ska filtreras.</span><span class="sxs-lookup"><span data-stu-id="674c1-133">Specifies the fabricId to filter.</span></span>

```yaml
Type: String
Parameter Sets: ByFabricId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="674c1-134">-Namn</span><span class="sxs-lookup"><span data-stu-id="674c1-134">-Name</span></span>
<span data-ttu-id="674c1-135">Anger namnet på händelsen för sökning.</span><span class="sxs-lookup"><span data-stu-id="674c1-135">Specifies name of the event for search.</span></span>

```yaml
Type: String
Parameter Sets: ByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="674c1-136">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="674c1-136">-ResourceId</span></span>
<span data-ttu-id="674c1-137">Specifes händelse händelsen ReourceId.</span><span class="sxs-lookup"><span data-stu-id="674c1-137">Specifes the event ReourceId of event.</span></span>

```yaml
Type: String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="674c1-138">– Allvarlighets grad</span><span class="sxs-lookup"><span data-stu-id="674c1-138">-Severity</span></span>
<span data-ttu-id="674c1-139">Händelse allvarlighets grad att filtrera på.</span><span class="sxs-lookup"><span data-stu-id="674c1-139">Event severity to filter on.</span></span>

```yaml
Type: String
Parameter Sets: ByParam, ByFabricId
Aliases:
Accepted values: Critical, Warning, OK, Unknown

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="674c1-140">-StartTime</span><span class="sxs-lookup"><span data-stu-id="674c1-140">-StartTime</span></span>
<span data-ttu-id="674c1-141">Anger start tiden för sökfönstret.</span><span class="sxs-lookup"><span data-stu-id="674c1-141">Specifies the start time of the search window.</span></span> <span data-ttu-id="674c1-142">Använd den här parametern för att endast få händelser som har inträffat efter den angivna tiden.</span><span class="sxs-lookup"><span data-stu-id="674c1-142">Use this parameter to get only those events that have occurred after the specified time.</span></span>

```yaml
Type: DateTime
Parameter Sets: ByParam, ByFabricId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="674c1-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="674c1-143">CommonParameters</span></span>
<span data-ttu-id="674c1-144">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="674c1-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="674c1-145">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="674c1-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="674c1-146">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="674c1-146">INPUTS</span></span>

### <span data-ttu-id="674c1-147">Microsoft. Azure. commands. RecoveryServices. SiteRecovery. ASRFabric</span><span class="sxs-lookup"><span data-stu-id="674c1-147">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric</span></span>

## <span data-ttu-id="674c1-148">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="674c1-148">OUTPUTS</span></span>

### <span data-ttu-id="674c1-149">System. Collections. Generic. IEnumerable ' 1 [[Microsoft. Azure. commands. RecoveryServices. SiteRecovery. ASREvent, Microsoft. Azure. commands. RecoveryServices. SiteRecovery, version = 0.1.0.0, Culture = neutralt, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="674c1-149">System.Collections.Generic.IEnumerable\`1[[Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASREvent, Microsoft.Azure.Commands.RecoveryServices.SiteRecovery, Version=0.1.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="674c1-150">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="674c1-150">NOTES</span></span>

## <span data-ttu-id="674c1-151">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="674c1-151">RELATED LINKS</span></span>