---
external help file: ''
Module Name: Az.CustomProviders
online version: https://docs.microsoft.com/en-us/powershell/module/az.customproviders/remove-azcustomproviderassociation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CustomProviders/help/Remove-AzCustomProviderAssociation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CustomProviders/help/Remove-AzCustomProviderAssociation.md
ms.openlocfilehash: 708bac976e32c2af114576d971c05843fd58ef93
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94262785"
---
# <span data-ttu-id="5e860-101">Remove-AzCustomProviderAssociation</span><span class="sxs-lookup"><span data-stu-id="5e860-101">Remove-AzCustomProviderAssociation</span></span>

## <span data-ttu-id="5e860-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="5e860-102">SYNOPSIS</span></span>
<span data-ttu-id="5e860-103">Ta bort en koppling.</span><span class="sxs-lookup"><span data-stu-id="5e860-103">Delete an association.</span></span>

## <span data-ttu-id="5e860-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="5e860-104">SYNTAX</span></span>

### <span data-ttu-id="5e860-105">Ta bort (standard)</span><span class="sxs-lookup"><span data-stu-id="5e860-105">Delete (Default)</span></span>
```
Remove-AzCustomProviderAssociation -Name <String> -Scope <String> [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="5e860-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="5e860-106">DeleteViaIdentity</span></span>
```
Remove-AzCustomProviderAssociation -InputObject <ICustomProvidersIdentity> [-DefaultProfile <PSObject>]
 [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="5e860-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="5e860-107">DESCRIPTION</span></span>
<span data-ttu-id="5e860-108">Ta bort en koppling.</span><span class="sxs-lookup"><span data-stu-id="5e860-108">Delete an association.</span></span>

## <span data-ttu-id="5e860-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="5e860-109">EXAMPLES</span></span>

### <span data-ttu-id="5e860-110">Exempel 1: ta bort en anpassad leverantörs koppling.</span><span class="sxs-lookup"><span data-stu-id="5e860-110">Example 1: Remove a custom provider association.</span></span>
```powershell
PS C:\> PS C:\> Remove-AzCustomProviderAssociation -Scope $id -Name Namespace.Type
```

<span data-ttu-id="5e860-111">Ta bort en anpassad leverantörs koppling.</span><span class="sxs-lookup"><span data-stu-id="5e860-111">Remove a custom provider association.</span></span>

### <span data-ttu-id="5e860-112">Exempel 2: ta bort en anpassad operatör med rör</span><span class="sxs-lookup"><span data-stu-id="5e860-112">Example 2: Remove a custom provider association with Piping</span></span>
```powershell
PS C:\> PS C:\> Get-AzCustomProviderAssociation | Remove-AzCustomProviderAssociation -PassThru

True
```

<span data-ttu-id="5e860-113">Ta bort en anpassad leverantörs koppling genom att använda ledning och PassThru-funktionen för att indikera framgång eller misslyckande.</span><span class="sxs-lookup"><span data-stu-id="5e860-113">Remove a custom provider association, using piping and the PassThru feature to indicate success or failure.</span></span>

## <span data-ttu-id="5e860-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="5e860-114">PARAMETERS</span></span>

### <span data-ttu-id="5e860-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="5e860-115">-AsJob</span></span>
<span data-ttu-id="5e860-116">Köra kommandot som ett jobb</span><span class="sxs-lookup"><span data-stu-id="5e860-116">Run the command as a job</span></span>

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

### <span data-ttu-id="5e860-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5e860-117">-DefaultProfile</span></span>
<span data-ttu-id="5e860-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="5e860-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5e860-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5e860-119">-InputObject</span></span>
<span data-ttu-id="5e860-120">Identitets parameter för att konstruera, se avsnittet anteckningar för INPUTOBJECT-egenskaper och skapa en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="5e860-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.CustomProviders.Models.ICustomProvidersIdentity
Parameter Sets: DeleteViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5e860-121">-Namn</span><span class="sxs-lookup"><span data-stu-id="5e860-121">-Name</span></span>
<span data-ttu-id="5e860-122">Namnet på kopplingen.</span><span class="sxs-lookup"><span data-stu-id="5e860-122">The name of the association.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases: AssociationName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5e860-123">-Nowait</span><span class="sxs-lookup"><span data-stu-id="5e860-123">-NoWait</span></span>
<span data-ttu-id="5e860-124">Kör kommandot asynkront</span><span class="sxs-lookup"><span data-stu-id="5e860-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="5e860-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="5e860-125">-PassThru</span></span>
<span data-ttu-id="5e860-126">Returnerar true när kommandot lyckas</span><span class="sxs-lookup"><span data-stu-id="5e860-126">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="5e860-127">-Omfattning</span><span class="sxs-lookup"><span data-stu-id="5e860-127">-Scope</span></span>
<span data-ttu-id="5e860-128">Associeringens omfattning.</span><span class="sxs-lookup"><span data-stu-id="5e860-128">The scope of the association.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5e860-129">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="5e860-129">-Confirm</span></span>
<span data-ttu-id="5e860-130">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="5e860-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5e860-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5e860-131">-WhatIf</span></span>
<span data-ttu-id="5e860-132">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="5e860-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5e860-133">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="5e860-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5e860-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5e860-134">CommonParameters</span></span>
<span data-ttu-id="5e860-135">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5e860-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5e860-136">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="5e860-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5e860-137">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="5e860-137">INPUTS</span></span>

### <span data-ttu-id="5e860-138">Microsoft. Azure. PowerShell. cmdletar. CustomProviders. Models. ICustomProvidersIdentity</span><span class="sxs-lookup"><span data-stu-id="5e860-138">Microsoft.Azure.PowerShell.Cmdlets.CustomProviders.Models.ICustomProvidersIdentity</span></span>

## <span data-ttu-id="5e860-139">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="5e860-139">OUTPUTS</span></span>

### <span data-ttu-id="5e860-140">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="5e860-140">System.Boolean</span></span>

## <span data-ttu-id="5e860-141">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="5e860-141">NOTES</span></span>

<span data-ttu-id="5e860-142">ALIAS</span><span class="sxs-lookup"><span data-stu-id="5e860-142">ALIASES</span></span>

<span data-ttu-id="5e860-143">KOMPLEXA PARAMETER EGENSKAPER</span><span class="sxs-lookup"><span data-stu-id="5e860-143">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="5e860-144">Skapa en hash-tabell som innehåller lämpliga egenskaper för att lägga till de parametrar som beskrivs nedan.</span><span class="sxs-lookup"><span data-stu-id="5e860-144">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="5e860-145">Om du vill ha information om hash-tabeller kör Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="5e860-145">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="5e860-146">INPUTOBJECT <ICustomProvidersIdentity> : identitets parameter</span><span class="sxs-lookup"><span data-stu-id="5e860-146">INPUTOBJECT <ICustomProvidersIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="5e860-147">`[AssociationName <String>]`: Namnet på kopplingen.</span><span class="sxs-lookup"><span data-stu-id="5e860-147">`[AssociationName <String>]`: The name of the association.</span></span>
  - <span data-ttu-id="5e860-148">`[Id <String>]`: Sökväg till resurs identitet</span><span class="sxs-lookup"><span data-stu-id="5e860-148">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="5e860-149">`[ResourceGroupName <String>]`: Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="5e860-149">`[ResourceGroupName <String>]`: The name of the resource group.</span></span>
  - <span data-ttu-id="5e860-150">`[ResourceProviderName <String>]`: Resurs leverantörens namn.</span><span class="sxs-lookup"><span data-stu-id="5e860-150">`[ResourceProviderName <String>]`: The name of the resource provider.</span></span>
  - <span data-ttu-id="5e860-151">`[Scope <String>]`: Associationens omfattning.</span><span class="sxs-lookup"><span data-stu-id="5e860-151">`[Scope <String>]`: The scope of the association.</span></span>
  - <span data-ttu-id="5e860-152">`[SubscriptionId <String>]`: ID för Azure-prenumeration.</span><span class="sxs-lookup"><span data-stu-id="5e860-152">`[SubscriptionId <String>]`: The Azure subscription ID.</span></span> <span data-ttu-id="5e860-153">Det här är en GUID-formaterad sträng (till exempel 00000000-0000-0000-0000-000000000000)</span><span class="sxs-lookup"><span data-stu-id="5e860-153">This is a GUID-formatted string (e.g. 00000000-0000-0000-0000-000000000000)</span></span>

## <span data-ttu-id="5e860-154">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="5e860-154">RELATED LINKS</span></span>

