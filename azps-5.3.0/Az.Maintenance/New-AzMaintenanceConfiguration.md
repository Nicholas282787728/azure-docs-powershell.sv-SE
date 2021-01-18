---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Maintenance.dll-Help.xml
Module Name: Az.Maintenance
online version: https://docs.microsoft.com/en-us/powershell/module/az.maintenance/new-azmaintenanceconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maintenance/Maintenance/help/New-AzMaintenanceConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maintenance/Maintenance/help/New-AzMaintenanceConfiguration.md
ms.openlocfilehash: bc2932f91bd2f7361d98ebbe6516ae8bec1513cc
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98524056"
---
# <span data-ttu-id="d6e39-101">New-AzMaintenanceConfiguration</span><span class="sxs-lookup"><span data-stu-id="d6e39-101">New-AzMaintenanceConfiguration</span></span>

## <span data-ttu-id="d6e39-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="d6e39-102">SYNOPSIS</span></span>
<span data-ttu-id="d6e39-103">Skapa eller uppdatera konfigurations post</span><span class="sxs-lookup"><span data-stu-id="d6e39-103">Create or Update configuration record</span></span>

## <span data-ttu-id="d6e39-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="d6e39-104">SYNTAX</span></span>

```
New-AzMaintenanceConfiguration [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [-Tag <Hashtable>] [-ExtensionProperty <Hashtable>] [-MaintenanceScope <String>] [-StartDateTime <String>]
 [-ExpirationDateTime <String>] [-Timezone <String>] [-Duration <TimeSpan>] [-Visibility <String>]
 [-RecurEvery <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="d6e39-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="d6e39-105">DESCRIPTION</span></span>
<span data-ttu-id="d6e39-106">Skapa eller uppdatera konfigurations post</span><span class="sxs-lookup"><span data-stu-id="d6e39-106">Create or Update configuration record</span></span>

## <span data-ttu-id="d6e39-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="d6e39-107">EXAMPLES</span></span>

### <span data-ttu-id="d6e39-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="d6e39-108">Example 1</span></span>
```powershell
PS C:\> New-AzMaintenanceConfiguration -ResourceGroupName smdtest -Name workervmscentralus -MaintenanceScope Host -Location centralus -StartDateTime 2020-08-01 00:00 -ExpirationDateTime 2021-08-04 00:00 -TimeZone Pacific Standard Time -Duration 05:00 -RecurEvery Day


Location            : centralus
Tags                : {}
ExtensionProperties : {}
MaintenanceScope    : Host
StartDateTime       : 2020-08-01 00:00
ExpirationDateTime  : 2021-08-04 00:00
TimeZone            : Pacific Standard Time
RecurEvery          : Day
Duration            : 05:00
MaintenanceScope    : Host
Visibility          : Custom
Id                  : /subscriptions/42c974dd-2c03-4f1b-96ad-b07f050aaa74/resourcegroups/smdtest/providers/Microsoft.Maintenance/maintenanceConfigurations/workervmscentralus
Name                : workervmscentralus
Type                : Microsoft.Maintenance/maintenanceConfigurations
```

<span data-ttu-id="d6e39-109">Skapa en underhålls konfiguration med scope-värden</span><span class="sxs-lookup"><span data-stu-id="d6e39-109">Create a maintenance configuration with scope Host</span></span>

## <span data-ttu-id="d6e39-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="d6e39-110">PARAMETERS</span></span>

### <span data-ttu-id="d6e39-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d6e39-111">-AsJob</span></span>
<span data-ttu-id="d6e39-112">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="d6e39-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="d6e39-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d6e39-113">-DefaultProfile</span></span>
<span data-ttu-id="d6e39-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="d6e39-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d6e39-115">-Varaktighet</span><span class="sxs-lookup"><span data-stu-id="d6e39-115">-Duration</span></span>
<span data-ttu-id="d6e39-116">Varaktigheten</span><span class="sxs-lookup"><span data-stu-id="d6e39-116">The duration</span></span>


```yaml
Type: System.TimeSpan
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d6e39-117">-ExpirationDateTime</span><span class="sxs-lookup"><span data-stu-id="d6e39-117">-ExpirationDateTime</span></span>
<span data-ttu-id="d6e39-118">ExpirationDateTime i schemat i formatet ÅÅÅÅ-MM-DD hh: mm</span><span class="sxs-lookup"><span data-stu-id="d6e39-118">The expirationDateTime of the schedule in format YYYY-MM-DD hh:mm</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d6e39-119">-ExtensionProperty</span><span class="sxs-lookup"><span data-stu-id="d6e39-119">-ExtensionProperty</span></span>
<span data-ttu-id="d6e39-120">Anknytnings egenskaper per resurs.</span><span class="sxs-lookup"><span data-stu-id="d6e39-120">The Extension properties per resource.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d6e39-121">-Plats</span><span class="sxs-lookup"><span data-stu-id="d6e39-121">-Location</span></span>
<span data-ttu-id="d6e39-122">Platsen för underhålls konfiguration.</span><span class="sxs-lookup"><span data-stu-id="d6e39-122">The maintenance configuration location.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d6e39-123">-MaintenanceScope</span><span class="sxs-lookup"><span data-stu-id="d6e39-123">-MaintenanceScope</span></span>
<span data-ttu-id="d6e39-124">Underhålls omfattning.</span><span class="sxs-lookup"><span data-stu-id="d6e39-124">The Maintenance Scope.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d6e39-125">-Namn</span><span class="sxs-lookup"><span data-stu-id="d6e39-125">-Name</span></span>
<span data-ttu-id="d6e39-126">Konfigurations namn för underhåll.</span><span class="sxs-lookup"><span data-stu-id="d6e39-126">The maintenance configuration Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d6e39-127">-RecurEvery</span><span class="sxs-lookup"><span data-stu-id="d6e39-127">-RecurEvery</span></span>
<span data-ttu-id="d6e39-128">Schemat</span><span class="sxs-lookup"><span data-stu-id="d6e39-128">The schedule recurrence</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d6e39-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d6e39-129">-ResourceGroupName</span></span>
<span data-ttu-id="d6e39-130">Resurs gruppens namn.</span><span class="sxs-lookup"><span data-stu-id="d6e39-130">The resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d6e39-131">-StartDateTime</span><span class="sxs-lookup"><span data-stu-id="d6e39-131">-StartDateTime</span></span>
<span data-ttu-id="d6e39-132">StartDateTime i schemat i formatet ÅÅÅÅ-MM-DD hh: mm</span><span class="sxs-lookup"><span data-stu-id="d6e39-132">The StartDateTime of the schedule in format YYYY-MM-DD hh:mm</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d6e39-133">-Tagg</span><span class="sxs-lookup"><span data-stu-id="d6e39-133">-Tag</span></span>
<span data-ttu-id="d6e39-134">ARM-taggarna.</span><span class="sxs-lookup"><span data-stu-id="d6e39-134">The ARM Tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d6e39-135">-Timezone</span><span class="sxs-lookup"><span data-stu-id="d6e39-135">-Timezone</span></span>
<span data-ttu-id="d6e39-136">Tids zonen</span><span class="sxs-lookup"><span data-stu-id="d6e39-136">The timezone</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d6e39-137">-Synlighet</span><span class="sxs-lookup"><span data-stu-id="d6e39-137">-Visibility</span></span>
<span data-ttu-id="d6e39-138">Synligheten för omfattningen</span><span class="sxs-lookup"><span data-stu-id="d6e39-138">The visibility of the scope</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d6e39-139">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="d6e39-139">-Confirm</span></span>
<span data-ttu-id="d6e39-140">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="d6e39-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d6e39-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d6e39-141">-WhatIf</span></span>
<span data-ttu-id="d6e39-142">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="d6e39-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d6e39-143">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="d6e39-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d6e39-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d6e39-144">CommonParameters</span></span>
<span data-ttu-id="d6e39-145">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d6e39-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d6e39-146">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d6e39-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d6e39-147">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="d6e39-147">INPUTS</span></span>

### <span data-ttu-id="d6e39-148">System. String</span><span class="sxs-lookup"><span data-stu-id="d6e39-148">System.String</span></span>

## <span data-ttu-id="d6e39-149">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="d6e39-149">OUTPUTS</span></span>

### <span data-ttu-id="d6e39-150">Microsoft. Azure. commands. Maintenance. Models. PSMaintenanceConfiguration</span><span class="sxs-lookup"><span data-stu-id="d6e39-150">Microsoft.Azure.Commands.Maintenance.Models.PSMaintenanceConfiguration</span></span>

## <span data-ttu-id="d6e39-151">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="d6e39-151">NOTES</span></span>

## <span data-ttu-id="d6e39-152">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="d6e39-152">RELATED LINKS</span></span>
