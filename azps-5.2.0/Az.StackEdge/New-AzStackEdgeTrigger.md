---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.stackedge/new-azstackedgetrigger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/New-AzStackEdgeTrigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/New-AzStackEdgeTrigger.md
ms.openlocfilehash: d13498df4c91c8d31b8bfe2e19e9f7fa23f99998
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98404480"
---
# <span data-ttu-id="d441a-101">New-AzStackEdgeTrigger</span><span class="sxs-lookup"><span data-stu-id="d441a-101">New-AzStackEdgeTrigger</span></span>

## <span data-ttu-id="d441a-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="d441a-102">SYNOPSIS</span></span>
<span data-ttu-id="d441a-103">Konfigurerar en utlösare på enheten.</span><span class="sxs-lookup"><span data-stu-id="d441a-103">Configures a trigger on the device.</span></span>

## <span data-ttu-id="d441a-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="d441a-104">SYNTAX</span></span>

### <span data-ttu-id="d441a-105">FileEventTriggerParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="d441a-105">FileEventTriggerParameterSet (Default)</span></span>
```
New-AzStackEdgeTrigger [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String> -RoleName <String>
 [-FileEvent] -ShareName <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d441a-106">PeriodicTimerTriggerParameterSet</span><span class="sxs-lookup"><span data-stu-id="d441a-106">PeriodicTimerTriggerParameterSet</span></span>
```
New-AzStackEdgeTrigger [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String> -RoleName <String>
 [-PeriodicTimerEvent] [-AsJob] [-DefaultProfile <IAzureContextContainer>] -Schedule <String>
 -StartTime <DateTime> -Topic <String> [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d441a-107">FileEventTriggerResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="d441a-107">FileEventTriggerResourceIdParameterSet</span></span>
```
New-AzStackEdgeTrigger [-FileEvent] -ShareId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d441a-108">PeriodicTimerTriggerResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="d441a-108">PeriodicTimerTriggerResourceIdParameterSet</span></span>
```
New-AzStackEdgeTrigger [-PeriodicTimerEvent] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 -Schedule <String> -StartTime <DateTime> -Topic <String> [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d441a-109">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="d441a-109">DESCRIPTION</span></span>
<span data-ttu-id="d441a-110">Cmdleten **New-AzStackEdgeTrigger** konfigurerar en trigger på stack Edge-enheten.</span><span class="sxs-lookup"><span data-stu-id="d441a-110">The **New-AzStackEdgeTrigger** cmdlet configures a trigger on the Stack Edge device.</span></span> 

## <span data-ttu-id="d441a-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="d441a-111">EXAMPLES</span></span>

### <span data-ttu-id="d441a-112">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="d441a-112">Example 1</span></span>
```powershell
PS C:\> New-AzStackEdgeTrigger -ResourceGroupName resourceGroupName -DeviceName deviceName -PeriodicTimerEvent -Name periodic-trigger -RoleName IOTRole -Schedule "00:00" -StartTime "2019-10-28 12:00:00" -Topic sample-topic
Name                  Kind               
----                  ----               
periodic-trigger      PeriodicTimerEvent
```

## <span data-ttu-id="d441a-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="d441a-113">PARAMETERS</span></span>

### <span data-ttu-id="d441a-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d441a-114">-AsJob</span></span>
<span data-ttu-id="d441a-115">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="d441a-115">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d441a-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d441a-116">-DefaultProfile</span></span>
<span data-ttu-id="d441a-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="d441a-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d441a-118">-Enhets namn</span><span class="sxs-lookup"><span data-stu-id="d441a-118">-DeviceName</span></span>
<span data-ttu-id="d441a-119">Enhetens namn</span><span class="sxs-lookup"><span data-stu-id="d441a-119">Device Name</span></span>

```yaml
Type: System.String
Parameter Sets: FileEventTriggerParameterSet, PeriodicTimerTriggerParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d441a-120">-FileEvent</span><span class="sxs-lookup"><span data-stu-id="d441a-120">-FileEvent</span></span>
<span data-ttu-id="d441a-121">Överför denna växel parameter för att konfigurera FileEvent-utlösaren</span><span class="sxs-lookup"><span data-stu-id="d441a-121">Pass this switch parameter to configure FileEvent Trigger</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: FileEventTriggerParameterSet, FileEventTriggerResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d441a-122">-Namn</span><span class="sxs-lookup"><span data-stu-id="d441a-122">-Name</span></span>
<span data-ttu-id="d441a-123">Resurs namn</span><span class="sxs-lookup"><span data-stu-id="d441a-123">Resource Name</span></span>

```yaml
Type: System.String
Parameter Sets: FileEventTriggerParameterSet, PeriodicTimerTriggerParameterSet
Aliases: TriggerName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d441a-124">-PeriodicTimerEvent</span><span class="sxs-lookup"><span data-stu-id="d441a-124">-PeriodicTimerEvent</span></span>
<span data-ttu-id="d441a-125">Överför denna växel parameter för att konfigurera PeriodicTimerEvent-utlösaren</span><span class="sxs-lookup"><span data-stu-id="d441a-125">Pass this switch parameter to configure PeriodicTimerEvent Trigger</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: PeriodicTimerTriggerParameterSet, PeriodicTimerTriggerResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d441a-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d441a-126">-ResourceGroupName</span></span>
<span data-ttu-id="d441a-127">Resurs grupps namn</span><span class="sxs-lookup"><span data-stu-id="d441a-127">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: FileEventTriggerParameterSet, PeriodicTimerTriggerParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d441a-128">-RoleName</span><span class="sxs-lookup"><span data-stu-id="d441a-128">-RoleName</span></span>
<span data-ttu-id="d441a-129">Beräknings roll som händelser höjs mot.</span><span class="sxs-lookup"><span data-stu-id="d441a-129">Compute role against which events will be raised.</span></span>

```yaml
Type: System.String
Parameter Sets: FileEventTriggerParameterSet, PeriodicTimerTriggerParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d441a-130">– Schema</span><span class="sxs-lookup"><span data-stu-id="d441a-130">-Schedule</span></span>
<span data-ttu-id="d441a-131">Frekvens där timer-händelsen måste höjas.</span><span class="sxs-lookup"><span data-stu-id="d441a-131">Periodic frequency at which timer event needs to be raised.</span></span> <span data-ttu-id="d441a-132">Ange ett schema i antingen dagar (mellan 1 och 365), timmar (mellan 1 och 23) eller minuter (mellan 1 och 59).</span><span class="sxs-lookup"><span data-stu-id="d441a-132">Specify a schedule in either days (between 1 and 365) , hours (between 1 and 23), or minutes (between 1 and 59).</span></span>

```yaml
Type: System.String
Parameter Sets: PeriodicTimerTriggerParameterSet, PeriodicTimerTriggerResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d441a-133">-ShareId</span><span class="sxs-lookup"><span data-stu-id="d441a-133">-ShareId</span></span>
<span data-ttu-id="d441a-134">Fildelnings-ID som ska överföras i FileEvent-utlösare</span><span class="sxs-lookup"><span data-stu-id="d441a-134">File share ID to be passed in FileEvent Trigger</span></span>

```yaml
Type: System.String
Parameter Sets: FileEventTriggerResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d441a-135">-ShareName</span><span class="sxs-lookup"><span data-stu-id="d441a-135">-ShareName</span></span>
<span data-ttu-id="d441a-136">Fildelnings-ID som ska överföras i FileEvent-utlösare</span><span class="sxs-lookup"><span data-stu-id="d441a-136">File share ID to be passed in FileEvent Trigger</span></span>

```yaml
Type: System.String
Parameter Sets: FileEventTriggerParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d441a-137">-StartTime</span><span class="sxs-lookup"><span data-stu-id="d441a-137">-StartTime</span></span>
<span data-ttu-id="d441a-138">Klock slaget som resulterar i en giltig utlösare.</span><span class="sxs-lookup"><span data-stu-id="d441a-138">The time of the day that results in a valid trigger.</span></span> <span data-ttu-id="d441a-139">Schemat beräknas med en referens till tiden som är angiven till sekunder.</span><span class="sxs-lookup"><span data-stu-id="d441a-139">Schedule is computed with reference to the time specified up to seconds.</span></span> <span data-ttu-id="d441a-140">Om tidszon inte anges anses tiden vara i enhetens tidszon.</span><span class="sxs-lookup"><span data-stu-id="d441a-140">If timezone is not specified the time will considered to be in device timezone.</span></span> <span data-ttu-id="d441a-141">Värdet returneras alltid som UTC-tid.</span><span class="sxs-lookup"><span data-stu-id="d441a-141">The value will always be returned as UTC time.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: PeriodicTimerTriggerParameterSet, PeriodicTimerTriggerResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d441a-142">-Ämne</span><span class="sxs-lookup"><span data-stu-id="d441a-142">-Topic</span></span>
<span data-ttu-id="d441a-143">Ämne där periodiska händelser publiceras till IoT-enhet.</span><span class="sxs-lookup"><span data-stu-id="d441a-143">Topic where periodic events are published to IoT device.</span></span>

```yaml
Type: System.String
Parameter Sets: PeriodicTimerTriggerParameterSet, PeriodicTimerTriggerResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d441a-144">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="d441a-144">-Confirm</span></span>
<span data-ttu-id="d441a-145">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="d441a-145">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d441a-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d441a-146">-WhatIf</span></span>
<span data-ttu-id="d441a-147">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="d441a-147">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="d441a-148">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="d441a-148">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d441a-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d441a-149">CommonParameters</span></span>
<span data-ttu-id="d441a-150">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d441a-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d441a-151">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d441a-151">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d441a-152">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="d441a-152">INPUTS</span></span>

### <span data-ttu-id="d441a-153">Ingen</span><span class="sxs-lookup"><span data-stu-id="d441a-153">None</span></span>

## <span data-ttu-id="d441a-154">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="d441a-154">OUTPUTS</span></span>

### <span data-ttu-id="d441a-155">Microsoft. Azure. PowerShell. cmdletar. StackEdge. Models. PSStackEdgeTrigger</span><span class="sxs-lookup"><span data-stu-id="d441a-155">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeTrigger</span></span>

## <span data-ttu-id="d441a-156">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="d441a-156">NOTES</span></span>

## <span data-ttu-id="d441a-157">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="d441a-157">RELATED LINKS</span></span>
