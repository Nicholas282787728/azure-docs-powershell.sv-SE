---
external help file: ''
Module Name: Az.Migrate
online version: https://docs.microsoft.com/en-us/powershell/module/az.migrate/new-azmigrateproject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/New-AzMigrateProject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/New-AzMigrateProject.md
ms.openlocfilehash: 32c4799f574e94eecee1f7ebf810c2f27bc5eccf
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98425491"
---
# <span data-ttu-id="e071a-101">New-AzMigrateProject</span><span class="sxs-lookup"><span data-stu-id="e071a-101">New-AzMigrateProject</span></span>

## <span data-ttu-id="e071a-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="e071a-102">SYNOPSIS</span></span>
<span data-ttu-id="e071a-103">Skapar ett nytt migrera projekt.</span><span class="sxs-lookup"><span data-stu-id="e071a-103">Creates a new Migrate project.</span></span>

## <span data-ttu-id="e071a-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="e071a-104">SYNTAX</span></span>

```
New-AzMigrateProject -Location <String> -Name <String> -ResourceGroupName <String> [-ETag <String>]
 [-Property <IMigrateProjectProperties>] [-SubscriptionId <String>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="e071a-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="e071a-105">DESCRIPTION</span></span>
<span data-ttu-id="e071a-106">Skapar ett nytt migrera projekt.</span><span class="sxs-lookup"><span data-stu-id="e071a-106">Creates a new Migrate project.</span></span>

## <span data-ttu-id="e071a-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="e071a-107">EXAMPLES</span></span>

### <span data-ttu-id="e071a-108">Exempel 1: skapa (standard)</span><span class="sxs-lookup"><span data-stu-id="e071a-108">Example 1: Create (Default)</span></span>
```powershell
PS C:\> New-AzMigrateProject -SubscriptionId xxx-xxx-xxx -ResourceGroupName kuchaturimpkocrg1 -Name kuchaturimpkocrg1pwshp14 -Location "centralus"

ETag Location  Name                     Type
---- --------  ----                     ----
     centralus kuchaturimpkocrg1pwshp14 Microsoft.Migrate/MigrateProjects

```

<span data-ttu-id="e071a-109">Metod för att skapa ett nytt migrera projekt.</span><span class="sxs-lookup"><span data-stu-id="e071a-109">Method to create a new migrate project.</span></span>

## <span data-ttu-id="e071a-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="e071a-110">PARAMETERS</span></span>

### <span data-ttu-id="e071a-111">-ETag</span><span class="sxs-lookup"><span data-stu-id="e071a-111">-ETag</span></span>
<span data-ttu-id="e071a-112">Anger VMware-datorns namn.</span><span class="sxs-lookup"><span data-stu-id="e071a-112">Specifies the VMware machine name.</span></span>

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

### <span data-ttu-id="e071a-113">-Plats</span><span class="sxs-lookup"><span data-stu-id="e071a-113">-Location</span></span>
<span data-ttu-id="e071a-114">Anger VMware-datorns namn.</span><span class="sxs-lookup"><span data-stu-id="e071a-114">Specifies the VMware machine name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e071a-115">-Namn</span><span class="sxs-lookup"><span data-stu-id="e071a-115">-Name</span></span>
<span data-ttu-id="e071a-116">Anger det migrerande projekt namnet.</span><span class="sxs-lookup"><span data-stu-id="e071a-116">Specifies the migrate project name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e071a-117">-Egenskap</span><span class="sxs-lookup"><span data-stu-id="e071a-117">-Property</span></span>
<span data-ttu-id="e071a-118">Anger projekt egenskaper.</span><span class="sxs-lookup"><span data-stu-id="e071a-118">Specifies the project properties.</span></span>
<span data-ttu-id="e071a-119">Om du vill skapa läser du avsnittet anteckningar för EGENSKAPs egenskaper och skapar en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="e071a-119">To construct, see NOTES section for PROPERTY properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180901Preview.IMigrateProjectProperties
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e071a-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e071a-120">-ResourceGroupName</span></span>
<span data-ttu-id="e071a-121">Anger resurs gruppens namn.</span><span class="sxs-lookup"><span data-stu-id="e071a-121">Specifies the resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e071a-122">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="e071a-122">-SubscriptionId</span></span>
<span data-ttu-id="e071a-123">Anger abonnemangs-ID.</span><span class="sxs-lookup"><span data-stu-id="e071a-123">Specifies the subscription id.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e071a-124">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="e071a-124">-Confirm</span></span>
<span data-ttu-id="e071a-125">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="e071a-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e071a-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e071a-126">-WhatIf</span></span>
<span data-ttu-id="e071a-127">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="e071a-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e071a-128">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="e071a-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e071a-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e071a-129">CommonParameters</span></span>
<span data-ttu-id="e071a-130">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e071a-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e071a-131">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e071a-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e071a-132">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="e071a-132">INPUTS</span></span>

## <span data-ttu-id="e071a-133">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="e071a-133">OUTPUTS</span></span>

## <span data-ttu-id="e071a-134">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="e071a-134">NOTES</span></span>

<span data-ttu-id="e071a-135">ALIAS</span><span class="sxs-lookup"><span data-stu-id="e071a-135">ALIASES</span></span>

<span data-ttu-id="e071a-136">KOMPLEXA PARAMETER EGENSKAPER</span><span class="sxs-lookup"><span data-stu-id="e071a-136">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="e071a-137">Skapa en hash-tabell som innehåller lämpliga egenskaper för att lägga till de parametrar som beskrivs nedan.</span><span class="sxs-lookup"><span data-stu-id="e071a-137">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="e071a-138">Om du vill ha information om hash-tabeller kör Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="e071a-138">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="e071a-139">EGENSKAP <IMigrateProjectProperties> : anger projekt egenskaper.</span><span class="sxs-lookup"><span data-stu-id="e071a-139">PROPERTY <IMigrateProjectProperties>: Specifies the project properties.</span></span>
  - <span data-ttu-id="e071a-140">`[ProvisioningState <ProvisioningState?>]`: Etablerings status för det migrerande projektet.</span><span class="sxs-lookup"><span data-stu-id="e071a-140">`[ProvisioningState <ProvisioningState?>]`: Provisioning state of the migrate project.</span></span>
  - <span data-ttu-id="e071a-141">`[RegisteredTool <String[]>]`: Hämtar eller anger listan över verktyg som är registrerade i det migrerande projektet.</span><span class="sxs-lookup"><span data-stu-id="e071a-141">`[RegisteredTool <String[]>]`: Gets or sets the list of tools registered with the migrate project.</span></span>

## <span data-ttu-id="e071a-142">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="e071a-142">RELATED LINKS</span></span>

