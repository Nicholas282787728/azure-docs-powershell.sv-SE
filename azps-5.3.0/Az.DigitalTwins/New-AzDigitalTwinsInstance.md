---
external help file: ''
Module Name: Az.DigitalTwins
online version: https://docs.microsoft.com/en-us/powershell/module/az.digitaltwins/new-azdigitaltwinsinstance
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DigitalTwins/help/New-AzDigitalTwinsInstance.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DigitalTwins/help/New-AzDigitalTwinsInstance.md
ms.openlocfilehash: d6a748897b956759ad64056b0d9b83a6e82e91fc
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98522642"
---
# <span data-ttu-id="040c7-101">New-AzDigitalTwinsInstance</span><span class="sxs-lookup"><span data-stu-id="040c7-101">New-AzDigitalTwinsInstance</span></span>

## <span data-ttu-id="040c7-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="040c7-102">SYNOPSIS</span></span>
<span data-ttu-id="040c7-103">Skapa eller uppdatera metadata för en DigitalTwinsInstance.</span><span class="sxs-lookup"><span data-stu-id="040c7-103">Create or update the metadata of a DigitalTwinsInstance.</span></span>
<span data-ttu-id="040c7-104">Det vanliga mönstret för att ändra en egenskap är att hämta DigitalTwinsInstance och säkerhets-metadata och sedan kombinera dem med de ändrade värdena i en ny brödtext och uppdatera DigitalTwinsInstance.</span><span class="sxs-lookup"><span data-stu-id="040c7-104">The usual pattern to modify a property is to retrieve the DigitalTwinsInstance and security metadata, and then combine them with the modified values in a new body to update the DigitalTwinsInstance.</span></span>

## <span data-ttu-id="040c7-105">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="040c7-105">SYNTAX</span></span>

### <span data-ttu-id="040c7-106">CreateExpanded (standard)</span><span class="sxs-lookup"><span data-stu-id="040c7-106">CreateExpanded (Default)</span></span>
```
New-AzDigitalTwinsInstance -ResourceGroupName <String> -ResourceName <String> -Location <String>
 [-SubscriptionId <String>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="040c7-107">Göra</span><span class="sxs-lookup"><span data-stu-id="040c7-107">Create</span></span>
```
New-AzDigitalTwinsInstance -ResourceGroupName <String> -ResourceName <String>
 -DigitalTwinsCreate <IDigitalTwinsDescription> [-SubscriptionId <String>] [-DefaultProfile <PSObject>]
 [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="040c7-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="040c7-108">DESCRIPTION</span></span>
<span data-ttu-id="040c7-109">Skapa eller uppdatera metadata för en DigitalTwinsInstance.</span><span class="sxs-lookup"><span data-stu-id="040c7-109">Create or update the metadata of a DigitalTwinsInstance.</span></span>
<span data-ttu-id="040c7-110">Det vanliga mönstret för att ändra en egenskap är att hämta DigitalTwinsInstance och säkerhets-metadata och sedan kombinera dem med de ändrade värdena i en ny brödtext och uppdatera DigitalTwinsInstance.</span><span class="sxs-lookup"><span data-stu-id="040c7-110">The usual pattern to modify a property is to retrieve the DigitalTwinsInstance and security metadata, and then combine them with the modified values in a new body to update the DigitalTwinsInstance.</span></span>

## <span data-ttu-id="040c7-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="040c7-111">EXAMPLES</span></span>

### <span data-ttu-id="040c7-112">Exempel 1: skapa en AzDigitalTwinsInstance som standard.</span><span class="sxs-lookup"><span data-stu-id="040c7-112">Example 1: Create an AzDigitalTwinsInstance by default.</span></span>
```powershell
PS C:\> New-AzDigitalTwinsInstance -ResourceGroupName youritest -ResourceName youriDigitalTwin -Location eastus

Location Name             SkuName Type
-------- ----             ------- ----
eastus   youriDigitalTwin S1      Microsoft.DigitalTwins/digitalTwinsInstances
```

<span data-ttu-id="040c7-113">Skapa en AzDigitalTwinsInstance som standard</span><span class="sxs-lookup"><span data-stu-id="040c7-113">Create an AzDigitalTwinsInstance by default</span></span>

### <span data-ttu-id="040c7-114">Exempel 2: skapa ett AzDigitalTwinsInstance med AzDigitalTwins-objekt.</span><span class="sxs-lookup"><span data-stu-id="040c7-114">Example 2: Create an AzDigitalTwinsInstance by AzDigitalTwins Object.</span></span>
```powershell
PS C:\> $GetAzDigTwin = Get-AzDigitalTwinsInstance -ResourceGroupName youritemp -ResourceName youriDigitalTwinsTest
New-AzDigitalTwinsInstance -ResourceGroupName youritemp -ResourceName youriDigitalTwinsTest01 -DigitalTwinsCreate $getAzdigitalTwins

Location Name                    Type
-------- ----                    ----
eastus   youriDigitalTwinsTest01 Microsoft.DigitalTwins/digitalTwinsInstances
```

<span data-ttu-id="040c7-115">Skapa en AzDigitalTwinsInstance med AzDigitalTwins-objekt</span><span class="sxs-lookup"><span data-stu-id="040c7-115">Create an AzDigitalTwinsInstance by AzDigitalTwins Object</span></span>

## <span data-ttu-id="040c7-116">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="040c7-116">PARAMETERS</span></span>

### <span data-ttu-id="040c7-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="040c7-117">-AsJob</span></span>
<span data-ttu-id="040c7-118">Köra kommandot som ett jobb</span><span class="sxs-lookup"><span data-stu-id="040c7-118">Run the command as a job</span></span>

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

### <span data-ttu-id="040c7-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="040c7-119">-DefaultProfile</span></span>
<span data-ttu-id="040c7-120">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="040c7-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="040c7-121">-DigitalTwinsCreate</span><span class="sxs-lookup"><span data-stu-id="040c7-121">-DigitalTwinsCreate</span></span>
<span data-ttu-id="040c7-122">Beskrivning av DigitalTwins-tjänsten.</span><span class="sxs-lookup"><span data-stu-id="040c7-122">The description of the DigitalTwins service.</span></span>
<span data-ttu-id="040c7-123">För att konstruera kan du läsa avsnittet anteckningar för DIGITALTWINSCREATE-egenskaper och skapa en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="040c7-123">To construct, see NOTES section for DIGITALTWINSCREATE properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Models.Api20201031.IDigitalTwinsDescription
Parameter Sets: Create
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="040c7-124">-Plats</span><span class="sxs-lookup"><span data-stu-id="040c7-124">-Location</span></span>
<span data-ttu-id="040c7-125">Resurs platsen.</span><span class="sxs-lookup"><span data-stu-id="040c7-125">The resource location.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="040c7-126">-Nowait</span><span class="sxs-lookup"><span data-stu-id="040c7-126">-NoWait</span></span>
<span data-ttu-id="040c7-127">Kör kommandot asynkront</span><span class="sxs-lookup"><span data-stu-id="040c7-127">Run the command asynchronously</span></span>

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

### <span data-ttu-id="040c7-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="040c7-128">-ResourceGroupName</span></span>
<span data-ttu-id="040c7-129">Namnet på resurs gruppen som innehåller DigitalTwinsInstance.</span><span class="sxs-lookup"><span data-stu-id="040c7-129">The name of the resource group that contains the DigitalTwinsInstance.</span></span>

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

### <span data-ttu-id="040c7-130">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="040c7-130">-ResourceName</span></span>
<span data-ttu-id="040c7-131">Namnet på DigitalTwinsInstance.</span><span class="sxs-lookup"><span data-stu-id="040c7-131">The name of the DigitalTwinsInstance.</span></span>

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

### <span data-ttu-id="040c7-132">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="040c7-132">-SubscriptionId</span></span>
<span data-ttu-id="040c7-133">Prenumerations-ID.</span><span class="sxs-lookup"><span data-stu-id="040c7-133">The subscription identifier.</span></span>

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

### <span data-ttu-id="040c7-134">-Tagg</span><span class="sxs-lookup"><span data-stu-id="040c7-134">-Tag</span></span>
<span data-ttu-id="040c7-135">Resource-taggarna.</span><span class="sxs-lookup"><span data-stu-id="040c7-135">The resource tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="040c7-136">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="040c7-136">-Confirm</span></span>
<span data-ttu-id="040c7-137">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="040c7-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="040c7-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="040c7-138">-WhatIf</span></span>
<span data-ttu-id="040c7-139">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="040c7-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="040c7-140">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="040c7-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="040c7-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="040c7-141">CommonParameters</span></span>
<span data-ttu-id="040c7-142">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="040c7-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="040c7-143">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="040c7-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="040c7-144">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="040c7-144">INPUTS</span></span>

### <span data-ttu-id="040c7-145">Microsoft. Azure. PowerShell. cmdletar. DigitalTwins. Models. Api20201031. IDigitalTwinsDescription</span><span class="sxs-lookup"><span data-stu-id="040c7-145">Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Models.Api20201031.IDigitalTwinsDescription</span></span>

## <span data-ttu-id="040c7-146">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="040c7-146">OUTPUTS</span></span>

### <span data-ttu-id="040c7-147">Microsoft. Azure. PowerShell. cmdletar. DigitalTwins. Models. Api20201031. IDigitalTwinsDescription</span><span class="sxs-lookup"><span data-stu-id="040c7-147">Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Models.Api20201031.IDigitalTwinsDescription</span></span>

## <span data-ttu-id="040c7-148">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="040c7-148">NOTES</span></span>

<span data-ttu-id="040c7-149">ALIAS</span><span class="sxs-lookup"><span data-stu-id="040c7-149">ALIASES</span></span>

<span data-ttu-id="040c7-150">KOMPLEXA PARAMETER EGENSKAPER</span><span class="sxs-lookup"><span data-stu-id="040c7-150">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="040c7-151">Skapa en hash-tabell som innehåller lämpliga egenskaper för att lägga till de parametrar som beskrivs nedan.</span><span class="sxs-lookup"><span data-stu-id="040c7-151">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="040c7-152">Om du vill ha information om hash-tabeller kör Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="040c7-152">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="040c7-153">DIGITALTWINSCREATE <IDigitalTwinsDescription> : beskrivningen av DigitalTwins-tjänsten.</span><span class="sxs-lookup"><span data-stu-id="040c7-153">DIGITALTWINSCREATE <IDigitalTwinsDescription>: The description of the DigitalTwins service.</span></span>
  - <span data-ttu-id="040c7-154">`Location <String>`: Resurs platsen.</span><span class="sxs-lookup"><span data-stu-id="040c7-154">`Location <String>`: The resource location.</span></span>
  - <span data-ttu-id="040c7-155">`[Tag <IDigitalTwinsResourceTags>]`: Resurs märkningen.</span><span class="sxs-lookup"><span data-stu-id="040c7-155">`[Tag <IDigitalTwinsResourceTags>]`: The resource tags.</span></span>
    - <span data-ttu-id="040c7-156">`[(Any) <String>]`: Detta indikerar att en egenskap kan läggas till i det här objektet.</span><span class="sxs-lookup"><span data-stu-id="040c7-156">`[(Any) <String>]`: This indicates any property can be added to this object.</span></span>

## <span data-ttu-id="040c7-157">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="040c7-157">RELATED LINKS</span></span>

