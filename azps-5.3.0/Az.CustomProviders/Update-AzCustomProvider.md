---
external help file: ''
Module Name: Az.CustomProviders
online version: https://docs.microsoft.com/en-us/powershell/module/az.customproviders/update-azcustomprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CustomProviders/help/Update-AzCustomProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CustomProviders/help/Update-AzCustomProvider.md
ms.openlocfilehash: 6691586d454952f92d71a26d5b8ed02904f37bf8
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98526360"
---
# <span data-ttu-id="1bb61-101">Update-AzCustomProvider</span><span class="sxs-lookup"><span data-stu-id="1bb61-101">Update-AzCustomProvider</span></span>

## <span data-ttu-id="1bb61-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="1bb61-102">SYNOPSIS</span></span>
<span data-ttu-id="1bb61-103">Uppdaterar en befintlig anpassad resurs leverantör.</span><span class="sxs-lookup"><span data-stu-id="1bb61-103">Updates an existing custom resource provider.</span></span>
<span data-ttu-id="1bb61-104">Det enda värde som kan uppdateras med PATCH är för tillfället märkningarna.</span><span class="sxs-lookup"><span data-stu-id="1bb61-104">The only value that can be updated via PATCH currently is the tags.</span></span>

## <span data-ttu-id="1bb61-105">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="1bb61-105">SYNTAX</span></span>

### <span data-ttu-id="1bb61-106">UpdateExpanded (standard)</span><span class="sxs-lookup"><span data-stu-id="1bb61-106">UpdateExpanded (Default)</span></span>
```
Update-AzCustomProvider -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="1bb61-107">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="1bb61-107">UpdateViaIdentityExpanded</span></span>
```
Update-AzCustomProvider -InputObject <ICustomProvidersIdentity> [-Tag <Hashtable>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="1bb61-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="1bb61-108">DESCRIPTION</span></span>
<span data-ttu-id="1bb61-109">Uppdaterar en befintlig anpassad resurs leverantör.</span><span class="sxs-lookup"><span data-stu-id="1bb61-109">Updates an existing custom resource provider.</span></span>
<span data-ttu-id="1bb61-110">Det enda värde som kan uppdateras med PATCH är för tillfället märkningarna.</span><span class="sxs-lookup"><span data-stu-id="1bb61-110">The only value that can be updated via PATCH currently is the tags.</span></span>

## <span data-ttu-id="1bb61-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="1bb61-111">EXAMPLES</span></span>

### <span data-ttu-id="1bb61-112">Exempel 1: lägga till taggar till en anpassad leverantör</span><span class="sxs-lookup"><span data-stu-id="1bb61-112">Example 1: Add Tags to a custom Provider</span></span>
```powershell
PS C:\> Update-AzCustomProvider -ResourceGroupName myRg -Name Namespace.Type -Tag @{MyTag="MyValue"} | Format-List

Action            :
Id                : /subscriptions/xxxxx-yyyyy-xxxx-yyyy/resourceGroups/mc-cp01/providers/Microsoft.CustomProviders/resourceproviders/Namespace.Type
Location          : West US 2
Name              : Namespace.Type
ProvisioningState : Succeeded
ResourceType      : {CustomRoute1, associations}
Tag               : Microsoft.Azure.PowerShell.Cmdlets.CustomProviders.Models.Api20180901Preview.ResourceTags
Type              : Microsoft.CustomProviders/resourceproviders
Validation        :
```

<span data-ttu-id="1bb61-113">Uppdatera taggarna för en anpassad leverantör.</span><span class="sxs-lookup"><span data-stu-id="1bb61-113">Update the tags of a custom provider.</span></span>

### <span data-ttu-id="1bb61-114">Exempel 2: uppdatera en anpassad leverantör med rör</span><span class="sxs-lookup"><span data-stu-id="1bb61-114">Example 2: Update custom provider with piping</span></span>
```powershell
PS C:\> PS C:\> Get-AzCustomProvider -ResourceGroupName myRg -Name Namespace.Type | Update-AzCustomProvider -Tag @{MyTag="MyValue"}

Location  Name             Type
--------  ----             ----
West US 2 Namespace.Type   Microsoft.CustomProviders/resourceproviders
```

<span data-ttu-id="1bb61-115">Uppdatera en anpassad leverantör med rör.</span><span class="sxs-lookup"><span data-stu-id="1bb61-115">Update a custom provider using piping.</span></span>

## <span data-ttu-id="1bb61-116">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="1bb61-116">PARAMETERS</span></span>

### <span data-ttu-id="1bb61-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1bb61-117">-DefaultProfile</span></span>
<span data-ttu-id="1bb61-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="1bb61-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1bb61-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1bb61-119">-InputObject</span></span>
<span data-ttu-id="1bb61-120">Identitets parameter för att konstruera, se avsnittet anteckningar för INPUTOBJECT-egenskaper och skapa en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="1bb61-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.CustomProviders.Models.ICustomProvidersIdentity
Parameter Sets: UpdateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1bb61-121">-Namn</span><span class="sxs-lookup"><span data-stu-id="1bb61-121">-Name</span></span>
<span data-ttu-id="1bb61-122">Namnet på resurs leverantören.</span><span class="sxs-lookup"><span data-stu-id="1bb61-122">The name of the resource provider.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases: ResourceProviderName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1bb61-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1bb61-123">-ResourceGroupName</span></span>
<span data-ttu-id="1bb61-124">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="1bb61-124">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1bb61-125">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="1bb61-125">-SubscriptionId</span></span>
<span data-ttu-id="1bb61-126">ID för Azure-prenumeration.</span><span class="sxs-lookup"><span data-stu-id="1bb61-126">The Azure subscription ID.</span></span>
<span data-ttu-id="1bb61-127">Det här är en GUID-formaterad sträng (till exempel 00000000-0000-0000-0000-000000000000)</span><span class="sxs-lookup"><span data-stu-id="1bb61-127">This is a GUID-formatted string (e.g. 00000000-0000-0000-0000-000000000000)</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1bb61-128">-Tagg</span><span class="sxs-lookup"><span data-stu-id="1bb61-128">-Tag</span></span>
<span data-ttu-id="1bb61-129">Resursfiler</span><span class="sxs-lookup"><span data-stu-id="1bb61-129">Resource tags</span></span>

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

### <span data-ttu-id="1bb61-130">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="1bb61-130">-Confirm</span></span>
<span data-ttu-id="1bb61-131">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="1bb61-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1bb61-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1bb61-132">-WhatIf</span></span>
<span data-ttu-id="1bb61-133">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="1bb61-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1bb61-134">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="1bb61-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1bb61-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1bb61-135">CommonParameters</span></span>
<span data-ttu-id="1bb61-136">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1bb61-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1bb61-137">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="1bb61-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1bb61-138">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="1bb61-138">INPUTS</span></span>

### <span data-ttu-id="1bb61-139">Microsoft. Azure. PowerShell. cmdletar. CustomProviders. Models. ICustomProvidersIdentity</span><span class="sxs-lookup"><span data-stu-id="1bb61-139">Microsoft.Azure.PowerShell.Cmdlets.CustomProviders.Models.ICustomProvidersIdentity</span></span>

## <span data-ttu-id="1bb61-140">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="1bb61-140">OUTPUTS</span></span>

### <span data-ttu-id="1bb61-141">Microsoft. Azure. PowerShell. cmdletar. CustomProviders. Models. Api20180901Preview. ICustomRpManifest</span><span class="sxs-lookup"><span data-stu-id="1bb61-141">Microsoft.Azure.PowerShell.Cmdlets.CustomProviders.Models.Api20180901Preview.ICustomRpManifest</span></span>

## <span data-ttu-id="1bb61-142">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="1bb61-142">NOTES</span></span>

<span data-ttu-id="1bb61-143">ALIAS</span><span class="sxs-lookup"><span data-stu-id="1bb61-143">ALIASES</span></span>

<span data-ttu-id="1bb61-144">KOMPLEXA PARAMETER EGENSKAPER</span><span class="sxs-lookup"><span data-stu-id="1bb61-144">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="1bb61-145">Skapa en hash-tabell som innehåller lämpliga egenskaper för att lägga till de parametrar som beskrivs nedan.</span><span class="sxs-lookup"><span data-stu-id="1bb61-145">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="1bb61-146">Om du vill ha information om hash-tabeller kör Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="1bb61-146">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="1bb61-147">INPUTOBJECT <ICustomProvidersIdentity> : identitets parameter</span><span class="sxs-lookup"><span data-stu-id="1bb61-147">INPUTOBJECT <ICustomProvidersIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="1bb61-148">`[AssociationName <String>]`: Namnet på kopplingen.</span><span class="sxs-lookup"><span data-stu-id="1bb61-148">`[AssociationName <String>]`: The name of the association.</span></span>
  - <span data-ttu-id="1bb61-149">`[Id <String>]`: Sökväg till resurs identitet</span><span class="sxs-lookup"><span data-stu-id="1bb61-149">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="1bb61-150">`[ResourceGroupName <String>]`: Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="1bb61-150">`[ResourceGroupName <String>]`: The name of the resource group.</span></span>
  - <span data-ttu-id="1bb61-151">`[ResourceProviderName <String>]`: Resurs leverantörens namn.</span><span class="sxs-lookup"><span data-stu-id="1bb61-151">`[ResourceProviderName <String>]`: The name of the resource provider.</span></span>
  - <span data-ttu-id="1bb61-152">`[Scope <String>]`: Associationens omfattning.</span><span class="sxs-lookup"><span data-stu-id="1bb61-152">`[Scope <String>]`: The scope of the association.</span></span>
  - <span data-ttu-id="1bb61-153">`[SubscriptionId <String>]`: ID för Azure-prenumeration.</span><span class="sxs-lookup"><span data-stu-id="1bb61-153">`[SubscriptionId <String>]`: The Azure subscription ID.</span></span> <span data-ttu-id="1bb61-154">Det här är en GUID-formaterad sträng (till exempel 00000000-0000-0000-0000-000000000000)</span><span class="sxs-lookup"><span data-stu-id="1bb61-154">This is a GUID-formatted string (e.g. 00000000-0000-0000-0000-000000000000)</span></span>

## <span data-ttu-id="1bb61-155">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="1bb61-155">RELATED LINKS</span></span>

