---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Maintenance.dll-Help.xml
Module Name: Az.Maintenance
online version: https://docs.microsoft.com/en-us/powershell/module/az.maintenance/new-azmaintenanceconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maintenance/Maintenance/help/New-AzMaintenanceConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maintenance/Maintenance/help/New-AzMaintenanceConfiguration.md
ms.openlocfilehash: bc2932f91bd2f7361d98ebbe6516ae8bec1513cc
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94270928"
---
# <span data-ttu-id="3d77e-101">New-AzMaintenanceConfiguration</span><span class="sxs-lookup"><span data-stu-id="3d77e-101">New-AzMaintenanceConfiguration</span></span>

## <span data-ttu-id="3d77e-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="3d77e-102">SYNOPSIS</span></span>
<span data-ttu-id="3d77e-103">Skapa eller uppdatera konfigurations post</span><span class="sxs-lookup"><span data-stu-id="3d77e-103">Create or Update configuration record</span></span>

## <span data-ttu-id="3d77e-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="3d77e-104">SYNTAX</span></span>

```
New-AzMaintenanceConfiguration [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [-Tag <Hashtable>] [-ExtensionProperty <Hashtable>] [-MaintenanceScope <String>] [-StartDateTime <String>]
 [-ExpirationDateTime <String>] [-Timezone <String>] [-Duration <TimeSpan>] [-Visibility <String>]
 [-RecurEvery <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="3d77e-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="3d77e-105">DESCRIPTION</span></span>
<span data-ttu-id="3d77e-106">Skapa eller uppdatera konfigurations post</span><span class="sxs-lookup"><span data-stu-id="3d77e-106">Create or Update configuration record</span></span>

## <span data-ttu-id="3d77e-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="3d77e-107">EXAMPLES</span></span>

### <span data-ttu-id="3d77e-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="3d77e-108">Example 1</span></span>
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

<span data-ttu-id="3d77e-109">Skapa en underhålls konfiguration med scope-värden</span><span class="sxs-lookup"><span data-stu-id="3d77e-109">Create a maintenance configuration with scope Host</span></span>

## <span data-ttu-id="3d77e-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="3d77e-110">PARAMETERS</span></span>

### <span data-ttu-id="3d77e-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="3d77e-111">-AsJob</span></span>
<span data-ttu-id="3d77e-112">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="3d77e-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="3d77e-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3d77e-113">-DefaultProfile</span></span>
<span data-ttu-id="3d77e-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="3d77e-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3d77e-115">-Varaktighet</span><span class="sxs-lookup"><span data-stu-id="3d77e-115">-Duration</span></span>
<span data-ttu-id="3d77e-116">Varaktigheten</span><span class="sxs-lookup"><span data-stu-id="3d77e-116">The duration</span></span>


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

### <span data-ttu-id="3d77e-117">-ExpirationDateTime</span><span class="sxs-lookup"><span data-stu-id="3d77e-117">-ExpirationDateTime</span></span>
<span data-ttu-id="3d77e-118">ExpirationDateTime i schemat i formatet ÅÅÅÅ-MM-DD hh: mm</span><span class="sxs-lookup"><span data-stu-id="3d77e-118">The expirationDateTime of the schedule in format YYYY-MM-DD hh:mm</span></span>

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

### <span data-ttu-id="3d77e-119">-ExtensionProperty</span><span class="sxs-lookup"><span data-stu-id="3d77e-119">-ExtensionProperty</span></span>
<span data-ttu-id="3d77e-120">Anknytnings egenskaper per resurs.</span><span class="sxs-lookup"><span data-stu-id="3d77e-120">The Extension properties per resource.</span></span>

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

### <span data-ttu-id="3d77e-121">-Plats</span><span class="sxs-lookup"><span data-stu-id="3d77e-121">-Location</span></span>
<span data-ttu-id="3d77e-122">Platsen för underhålls konfiguration.</span><span class="sxs-lookup"><span data-stu-id="3d77e-122">The maintenance configuration location.</span></span>

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

### <span data-ttu-id="3d77e-123">-MaintenanceScope</span><span class="sxs-lookup"><span data-stu-id="3d77e-123">-MaintenanceScope</span></span>
<span data-ttu-id="3d77e-124">Underhålls omfattning.</span><span class="sxs-lookup"><span data-stu-id="3d77e-124">The Maintenance Scope.</span></span>

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

### <span data-ttu-id="3d77e-125">-Namn</span><span class="sxs-lookup"><span data-stu-id="3d77e-125">-Name</span></span>
<span data-ttu-id="3d77e-126">Konfigurations namn för underhåll.</span><span class="sxs-lookup"><span data-stu-id="3d77e-126">The maintenance configuration Name.</span></span>

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

### <span data-ttu-id="3d77e-127">-RecurEvery</span><span class="sxs-lookup"><span data-stu-id="3d77e-127">-RecurEvery</span></span>
<span data-ttu-id="3d77e-128">Schemat</span><span class="sxs-lookup"><span data-stu-id="3d77e-128">The schedule recurrence</span></span>

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

### <span data-ttu-id="3d77e-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3d77e-129">-ResourceGroupName</span></span>
<span data-ttu-id="3d77e-130">Resurs gruppens namn.</span><span class="sxs-lookup"><span data-stu-id="3d77e-130">The resource Group Name.</span></span>

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

### <span data-ttu-id="3d77e-131">-StartDateTime</span><span class="sxs-lookup"><span data-stu-id="3d77e-131">-StartDateTime</span></span>
<span data-ttu-id="3d77e-132">StartDateTime i schemat i formatet ÅÅÅÅ-MM-DD hh: mm</span><span class="sxs-lookup"><span data-stu-id="3d77e-132">The StartDateTime of the schedule in format YYYY-MM-DD hh:mm</span></span>

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

### <span data-ttu-id="3d77e-133">-Tagg</span><span class="sxs-lookup"><span data-stu-id="3d77e-133">-Tag</span></span>
<span data-ttu-id="3d77e-134">ARM-taggarna.</span><span class="sxs-lookup"><span data-stu-id="3d77e-134">The ARM Tags.</span></span>

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

### <span data-ttu-id="3d77e-135">-Timezone</span><span class="sxs-lookup"><span data-stu-id="3d77e-135">-Timezone</span></span>
<span data-ttu-id="3d77e-136">Tids zonen</span><span class="sxs-lookup"><span data-stu-id="3d77e-136">The timezone</span></span>

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

### <span data-ttu-id="3d77e-137">-Synlighet</span><span class="sxs-lookup"><span data-stu-id="3d77e-137">-Visibility</span></span>
<span data-ttu-id="3d77e-138">Synligheten för omfattningen</span><span class="sxs-lookup"><span data-stu-id="3d77e-138">The visibility of the scope</span></span>

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

### <span data-ttu-id="3d77e-139">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="3d77e-139">-Confirm</span></span>
<span data-ttu-id="3d77e-140">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="3d77e-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3d77e-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3d77e-141">-WhatIf</span></span>
<span data-ttu-id="3d77e-142">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="3d77e-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3d77e-143">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="3d77e-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3d77e-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3d77e-144">CommonParameters</span></span>
<span data-ttu-id="3d77e-145">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3d77e-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3d77e-146">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3d77e-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3d77e-147">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="3d77e-147">INPUTS</span></span>

### <span data-ttu-id="3d77e-148">System. String</span><span class="sxs-lookup"><span data-stu-id="3d77e-148">System.String</span></span>

## <span data-ttu-id="3d77e-149">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="3d77e-149">OUTPUTS</span></span>

### <span data-ttu-id="3d77e-150">Microsoft. Azure. commands. Maintenance. Models. PSMaintenanceConfiguration</span><span class="sxs-lookup"><span data-stu-id="3d77e-150">Microsoft.Azure.Commands.Maintenance.Models.PSMaintenanceConfiguration</span></span>

## <span data-ttu-id="3d77e-151">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="3d77e-151">NOTES</span></span>

## <span data-ttu-id="3d77e-152">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="3d77e-152">RELATED LINKS</span></span>
