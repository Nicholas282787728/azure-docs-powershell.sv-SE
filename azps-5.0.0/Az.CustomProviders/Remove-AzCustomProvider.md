---
external help file: ''
Module Name: Az.CustomProviders
online version: https://docs.microsoft.com/en-us/powershell/module/az.customproviders/remove-azcustomprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CustomProviders/help/Remove-AzCustomProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CustomProviders/help/Remove-AzCustomProvider.md
ms.openlocfilehash: b9b9c746390df42a678177a506ffc6cd398af03e
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94321287"
---
# <span data-ttu-id="bc7fc-101">Remove-AzCustomProvider</span><span class="sxs-lookup"><span data-stu-id="bc7fc-101">Remove-AzCustomProvider</span></span>

## <span data-ttu-id="bc7fc-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="bc7fc-102">SYNOPSIS</span></span>
<span data-ttu-id="bc7fc-103">Tar bort den anpassade resurs leverantören.</span><span class="sxs-lookup"><span data-stu-id="bc7fc-103">Deletes the custom resource provider.</span></span>

## <span data-ttu-id="bc7fc-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="bc7fc-104">SYNTAX</span></span>

### <span data-ttu-id="bc7fc-105">Ta bort (standard)</span><span class="sxs-lookup"><span data-stu-id="bc7fc-105">Delete (Default)</span></span>
```
Remove-AzCustomProvider -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="bc7fc-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="bc7fc-106">DeleteViaIdentity</span></span>
```
Remove-AzCustomProvider -InputObject <ICustomProvidersIdentity> [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="bc7fc-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="bc7fc-107">DESCRIPTION</span></span>
<span data-ttu-id="bc7fc-108">Tar bort den anpassade resurs leverantören.</span><span class="sxs-lookup"><span data-stu-id="bc7fc-108">Deletes the custom resource provider.</span></span>

## <span data-ttu-id="bc7fc-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="bc7fc-109">EXAMPLES</span></span>

### <span data-ttu-id="bc7fc-110">Exempel 1: ta bort en anpassad leverantör.</span><span class="sxs-lookup"><span data-stu-id="bc7fc-110">Example 1: Remove a custom provider.</span></span>
```powershell
PS C:\> PS C:\> Remove-AzCustomProvider -ResourceGroupName myRg -Name Namespace.Type
```

<span data-ttu-id="bc7fc-111">Ta bort en anpassad leverantör</span><span class="sxs-lookup"><span data-stu-id="bc7fc-111">Remove a custom provider</span></span>

### <span data-ttu-id="bc7fc-112">Exempel 2: ta bort en anpassad leverantör med PassThru</span><span class="sxs-lookup"><span data-stu-id="bc7fc-112">Example 2: Remove a custom provider with PassThru</span></span>
```powershell
PS C:\> PS C:\> Remove-AzCustomProvider -ResourceGroupName myRg -Name Namespace.Type -PassThru

True
```

<span data-ttu-id="bc7fc-113">Ta bort en anpassad Provider med funktionen PassThru för att indikera framgång eller misslyckande.</span><span class="sxs-lookup"><span data-stu-id="bc7fc-113">Remove a custom provider, using the PassThru feature to indicate success or failure.</span></span>

## <span data-ttu-id="bc7fc-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="bc7fc-114">PARAMETERS</span></span>

### <span data-ttu-id="bc7fc-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="bc7fc-115">-AsJob</span></span>
<span data-ttu-id="bc7fc-116">Köra kommandot som ett jobb</span><span class="sxs-lookup"><span data-stu-id="bc7fc-116">Run the command as a job</span></span>

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

### <span data-ttu-id="bc7fc-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bc7fc-117">-DefaultProfile</span></span>
<span data-ttu-id="bc7fc-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="bc7fc-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bc7fc-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="bc7fc-119">-InputObject</span></span>
<span data-ttu-id="bc7fc-120">Identitets parameter för att konstruera, se avsnittet anteckningar för INPUTOBJECT-egenskaper och skapa en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="bc7fc-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="bc7fc-121">-Namn</span><span class="sxs-lookup"><span data-stu-id="bc7fc-121">-Name</span></span>
<span data-ttu-id="bc7fc-122">Namnet på resurs leverantören.</span><span class="sxs-lookup"><span data-stu-id="bc7fc-122">The name of the resource provider.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases: ResourceProviderName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bc7fc-123">-Nowait</span><span class="sxs-lookup"><span data-stu-id="bc7fc-123">-NoWait</span></span>
<span data-ttu-id="bc7fc-124">Kör kommandot asynkront</span><span class="sxs-lookup"><span data-stu-id="bc7fc-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="bc7fc-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="bc7fc-125">-PassThru</span></span>
<span data-ttu-id="bc7fc-126">Returnerar true när kommandot lyckas</span><span class="sxs-lookup"><span data-stu-id="bc7fc-126">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="bc7fc-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bc7fc-127">-ResourceGroupName</span></span>
<span data-ttu-id="bc7fc-128">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="bc7fc-128">The name of the resource group.</span></span>

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

### <span data-ttu-id="bc7fc-129">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="bc7fc-129">-SubscriptionId</span></span>
<span data-ttu-id="bc7fc-130">ID för Azure-prenumeration.</span><span class="sxs-lookup"><span data-stu-id="bc7fc-130">The Azure subscription ID.</span></span>
<span data-ttu-id="bc7fc-131">Det här är en GUID-formaterad sträng (till exempel 00000000-0000-0000-0000-000000000000)</span><span class="sxs-lookup"><span data-stu-id="bc7fc-131">This is a GUID-formatted string (e.g. 00000000-0000-0000-0000-000000000000)</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bc7fc-132">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="bc7fc-132">-Confirm</span></span>
<span data-ttu-id="bc7fc-133">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="bc7fc-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bc7fc-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bc7fc-134">-WhatIf</span></span>
<span data-ttu-id="bc7fc-135">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="bc7fc-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bc7fc-136">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="bc7fc-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bc7fc-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bc7fc-137">CommonParameters</span></span>
<span data-ttu-id="bc7fc-138">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bc7fc-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bc7fc-139">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="bc7fc-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bc7fc-140">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="bc7fc-140">INPUTS</span></span>

### <span data-ttu-id="bc7fc-141">Microsoft. Azure. PowerShell. cmdletar. CustomProviders. Models. ICustomProvidersIdentity</span><span class="sxs-lookup"><span data-stu-id="bc7fc-141">Microsoft.Azure.PowerShell.Cmdlets.CustomProviders.Models.ICustomProvidersIdentity</span></span>

## <span data-ttu-id="bc7fc-142">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="bc7fc-142">OUTPUTS</span></span>

### <span data-ttu-id="bc7fc-143">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="bc7fc-143">System.Boolean</span></span>

## <span data-ttu-id="bc7fc-144">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="bc7fc-144">NOTES</span></span>

<span data-ttu-id="bc7fc-145">ALIAS</span><span class="sxs-lookup"><span data-stu-id="bc7fc-145">ALIASES</span></span>

<span data-ttu-id="bc7fc-146">KOMPLEXA PARAMETER EGENSKAPER</span><span class="sxs-lookup"><span data-stu-id="bc7fc-146">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="bc7fc-147">Skapa en hash-tabell som innehåller lämpliga egenskaper för att lägga till de parametrar som beskrivs nedan.</span><span class="sxs-lookup"><span data-stu-id="bc7fc-147">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="bc7fc-148">Om du vill ha information om hash-tabeller kör Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="bc7fc-148">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="bc7fc-149">INPUTOBJECT <ICustomProvidersIdentity> : identitets parameter</span><span class="sxs-lookup"><span data-stu-id="bc7fc-149">INPUTOBJECT <ICustomProvidersIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="bc7fc-150">`[AssociationName <String>]`: Namnet på kopplingen.</span><span class="sxs-lookup"><span data-stu-id="bc7fc-150">`[AssociationName <String>]`: The name of the association.</span></span>
  - <span data-ttu-id="bc7fc-151">`[Id <String>]`: Sökväg till resurs identitet</span><span class="sxs-lookup"><span data-stu-id="bc7fc-151">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="bc7fc-152">`[ResourceGroupName <String>]`: Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="bc7fc-152">`[ResourceGroupName <String>]`: The name of the resource group.</span></span>
  - <span data-ttu-id="bc7fc-153">`[ResourceProviderName <String>]`: Resurs leverantörens namn.</span><span class="sxs-lookup"><span data-stu-id="bc7fc-153">`[ResourceProviderName <String>]`: The name of the resource provider.</span></span>
  - <span data-ttu-id="bc7fc-154">`[Scope <String>]`: Associationens omfattning.</span><span class="sxs-lookup"><span data-stu-id="bc7fc-154">`[Scope <String>]`: The scope of the association.</span></span>
  - <span data-ttu-id="bc7fc-155">`[SubscriptionId <String>]`: ID för Azure-prenumeration.</span><span class="sxs-lookup"><span data-stu-id="bc7fc-155">`[SubscriptionId <String>]`: The Azure subscription ID.</span></span> <span data-ttu-id="bc7fc-156">Det här är en GUID-formaterad sträng (till exempel 00000000-0000-0000-0000-000000000000)</span><span class="sxs-lookup"><span data-stu-id="bc7fc-156">This is a GUID-formatted string (e.g. 00000000-0000-0000-0000-000000000000)</span></span>

## <span data-ttu-id="bc7fc-157">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="bc7fc-157">RELATED LINKS</span></span>

