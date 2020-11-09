---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesasrevent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrEvent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrEvent.md
ms.openlocfilehash: 8ed57766ba36607503994d331cec5381d9f43bbf
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94322451"
---
# <span data-ttu-id="7a514-101">Get-AzRecoveryServicesAsrEvent</span><span class="sxs-lookup"><span data-stu-id="7a514-101">Get-AzRecoveryServicesAsrEvent</span></span>

## <span data-ttu-id="7a514-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="7a514-102">SYNOPSIS</span></span>
<span data-ttu-id="7a514-103">Hämtar information om Azure Site Recovery-händelser i valvet.</span><span class="sxs-lookup"><span data-stu-id="7a514-103">Gets details of Azure Site Recovery events in the vault.</span></span>

## <span data-ttu-id="7a514-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="7a514-104">SYNTAX</span></span>

### <span data-ttu-id="7a514-105">ByParam (standard)</span><span class="sxs-lookup"><span data-stu-id="7a514-105">ByParam (Default)</span></span>
```
Get-AzRecoveryServicesAsrEvent [-AffectedObjectFriendlyName <String>] [-Fabric <ASRFabric>]
 [-Severity <String>] [-StartTime <DateTime>] [-EndTime <DateTime>] [-EventType <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7a514-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="7a514-106">ByResourceId</span></span>
```
Get-AzRecoveryServicesAsrEvent -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="7a514-107">ByFabricId</span><span class="sxs-lookup"><span data-stu-id="7a514-107">ByFabricId</span></span>
```
Get-AzRecoveryServicesAsrEvent -FabricId <String> [-AffectedObjectFriendlyName <String>] [-Severity <String>]
 [-StartTime <DateTime>] [-EndTime <DateTime>] [-EventType <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="7a514-108">ByName</span><span class="sxs-lookup"><span data-stu-id="7a514-108">ByName</span></span>
```
Get-AzRecoveryServicesAsrEvent -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7a514-109">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="7a514-109">DESCRIPTION</span></span>
<span data-ttu-id="7a514-110">**Get-AzRecoveryServicesAsrEvent** hämtar listan över händelser i valvet baserat på de angivna urvals filtren.</span><span class="sxs-lookup"><span data-stu-id="7a514-110">The **Get-AzRecoveryServicesAsrEvent** gets the list of events in the vault based on the specified selection filters.</span></span>

## <span data-ttu-id="7a514-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="7a514-111">EXAMPLES</span></span>

### <span data-ttu-id="7a514-112">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="7a514-112">Example 1</span></span>
```
PS C:\> Get-AzRecoveryServicesAsrEvent
```

<span data-ttu-id="7a514-113">Lista över alla händelser.</span><span class="sxs-lookup"><span data-stu-id="7a514-113">List of all events.</span></span>

### <span data-ttu-id="7a514-114">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="7a514-114">Example 2</span></span>
```
PS C:\> Get-AzRecoveryServicesAsrEvent -EventName "VmMonitoringEvent;9091897569816476200_84576304-bafc-4714-8ba6-197a5d09d84f"


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

<span data-ttu-id="7a514-115">Hämta händelse efter namn.</span><span class="sxs-lookup"><span data-stu-id="7a514-115">Get event by name.</span></span>

### <span data-ttu-id="7a514-116">Exempel 3</span><span class="sxs-lookup"><span data-stu-id="7a514-116">Example 3</span></span>
```
PS C:\> Get-AzRecoveryServicesAsrEvent -AffectedObjectName xxxxxxxxxxxxx
```

<span data-ttu-id="7a514-117">Lista över händelser för påverkade objekt.</span><span class="sxs-lookup"><span data-stu-id="7a514-117">List of event for affected Object.</span></span>

### <span data-ttu-id="7a514-118">Exempel 4</span><span class="sxs-lookup"><span data-stu-id="7a514-118">Example 4</span></span>
```
PS C:\> Get-AzRecoveryServicesAsrEvent -AffectedObjectName xxxxxxxxxxxx -StartTime "8/17/2017 12:31:40 PM" -EndTime "8/17/2017 12:31:44 PM" -Severity Critical -EventType VmHealth
```

<span data-ttu-id="7a514-119">Lista över händelser mellan start tid och slut tid, allvarlighets gradens kritiska och VmHealth.</span><span class="sxs-lookup"><span data-stu-id="7a514-119">List of event between time start time and end time , severity critical and health type VmHealth.</span></span>

## <span data-ttu-id="7a514-120">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="7a514-120">PARAMETERS</span></span>

### <span data-ttu-id="7a514-121">-AffectedObjectFriendlyName</span><span class="sxs-lookup"><span data-stu-id="7a514-121">-AffectedObjectFriendlyName</span></span>
<span data-ttu-id="7a514-122">Anger AffectedObject FriendlyName för sökningen.</span><span class="sxs-lookup"><span data-stu-id="7a514-122">Specifies AffectedObject FriendlyName for the search.</span></span>

```yaml
Type: System.String
Parameter Sets: ByParam, ByFabricId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7a514-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7a514-123">-DefaultProfile</span></span>
<span data-ttu-id="7a514-124">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="7a514-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7a514-125">-Slut tid</span><span class="sxs-lookup"><span data-stu-id="7a514-125">-EndTime</span></span>
<span data-ttu-id="7a514-126">Anger slut tiden för sökfönstret.</span><span class="sxs-lookup"><span data-stu-id="7a514-126">Specifies the end time of the search window.</span></span> <span data-ttu-id="7a514-127">Använd den här parametern för att endast få händelser som har inträffat före angiven tid.</span><span class="sxs-lookup"><span data-stu-id="7a514-127">Use this parameter to get only those events that have occurred before the specified time.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: ByParam, ByFabricId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7a514-128">-EventType</span><span class="sxs-lookup"><span data-stu-id="7a514-128">-EventType</span></span>
<span data-ttu-id="7a514-129">Filtrera händelser efter händelse typ.</span><span class="sxs-lookup"><span data-stu-id="7a514-129">Filter events by the event type.</span></span>

```yaml
Type: System.String
Parameter Sets: ByParam, ByFabricId
Aliases:
Accepted values: VmHealth, ServerHealth, AgentHealth

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7a514-130">-Fabric</span><span class="sxs-lookup"><span data-stu-id="7a514-130">-Fabric</span></span>
<span data-ttu-id="7a514-131">Filtrera händelser efter den angivna infrastruktur resursen.</span><span class="sxs-lookup"><span data-stu-id="7a514-131">Filter events by the specified fabric.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric
Parameter Sets: ByParam
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7a514-132">-FabricId</span><span class="sxs-lookup"><span data-stu-id="7a514-132">-FabricId</span></span>
<span data-ttu-id="7a514-133">Anger den fabricId som ska filtreras.</span><span class="sxs-lookup"><span data-stu-id="7a514-133">Specifies the fabricId to filter.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFabricId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7a514-134">-Namn</span><span class="sxs-lookup"><span data-stu-id="7a514-134">-Name</span></span>
<span data-ttu-id="7a514-135">Anger namnet på händelsen för sökning.</span><span class="sxs-lookup"><span data-stu-id="7a514-135">Specifies name of the event for search.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7a514-136">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7a514-136">-ResourceId</span></span>
<span data-ttu-id="7a514-137">Anger händelse-ResourceId för händelse.</span><span class="sxs-lookup"><span data-stu-id="7a514-137">Specifies the event ResourceId of event.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7a514-138">– Allvarlighets grad</span><span class="sxs-lookup"><span data-stu-id="7a514-138">-Severity</span></span>
<span data-ttu-id="7a514-139">Händelse allvarlighets grad att filtrera på.</span><span class="sxs-lookup"><span data-stu-id="7a514-139">Event severity to filter on.</span></span>

```yaml
Type: System.String
Parameter Sets: ByParam, ByFabricId
Aliases:
Accepted values: Critical, Warning, OK, Unknown

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7a514-140">-StartTime</span><span class="sxs-lookup"><span data-stu-id="7a514-140">-StartTime</span></span>
<span data-ttu-id="7a514-141">Anger start tiden för sökfönstret.</span><span class="sxs-lookup"><span data-stu-id="7a514-141">Specifies the start time of the search window.</span></span> <span data-ttu-id="7a514-142">Använd den här parametern för att endast få händelser som har inträffat efter den angivna tiden.</span><span class="sxs-lookup"><span data-stu-id="7a514-142">Use this parameter to get only those events that have occurred after the specified time.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: ByParam, ByFabricId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7a514-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7a514-143">CommonParameters</span></span>
<span data-ttu-id="7a514-144">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7a514-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7a514-145">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="7a514-145">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7a514-146">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="7a514-146">INPUTS</span></span>

### <span data-ttu-id="7a514-147">System. String</span><span class="sxs-lookup"><span data-stu-id="7a514-147">System.String</span></span>

## <span data-ttu-id="7a514-148">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="7a514-148">OUTPUTS</span></span>

### <span data-ttu-id="7a514-149">Microsoft. Azure. commands. RecoveryServices. SiteRecovery. ASREvent</span><span class="sxs-lookup"><span data-stu-id="7a514-149">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASREvent</span></span>

## <span data-ttu-id="7a514-150">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="7a514-150">NOTES</span></span>

## <span data-ttu-id="7a514-151">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="7a514-151">RELATED LINKS</span></span>
