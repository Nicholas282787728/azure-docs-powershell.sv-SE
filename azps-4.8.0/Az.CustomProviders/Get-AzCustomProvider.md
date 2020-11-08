---
external help file: ''
Module Name: Az.CustomProviders
online version: https://docs.microsoft.com/en-us/powershell/module/az.customproviders/get-azcustomprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CustomProviders/help/Get-AzCustomProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CustomProviders/help/Get-AzCustomProvider.md
ms.openlocfilehash: 42b4059b146a752980b1067272713bf0a22c2c46
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94262793"
---
# <span data-ttu-id="0991f-101">Get-AzCustomProvider</span><span class="sxs-lookup"><span data-stu-id="0991f-101">Get-AzCustomProvider</span></span>

## <span data-ttu-id="0991f-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="0991f-102">SYNOPSIS</span></span>
<span data-ttu-id="0991f-103">Hämtar Custom Resource Provider-manifestet.</span><span class="sxs-lookup"><span data-stu-id="0991f-103">Gets the custom resource provider manifest.</span></span>

## <span data-ttu-id="0991f-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="0991f-104">SYNTAX</span></span>

### <span data-ttu-id="0991f-105">List1 (standard)</span><span class="sxs-lookup"><span data-stu-id="0991f-105">List1 (Default)</span></span>
```
Get-AzCustomProvider [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="0991f-106">Lära</span><span class="sxs-lookup"><span data-stu-id="0991f-106">Get</span></span>
```
Get-AzCustomProvider -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="0991f-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="0991f-107">GetViaIdentity</span></span>
```
Get-AzCustomProvider -InputObject <ICustomProvidersIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="0991f-108">Förteckning</span><span class="sxs-lookup"><span data-stu-id="0991f-108">List</span></span>
```
Get-AzCustomProvider -ResourceGroupName <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="0991f-109">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="0991f-109">DESCRIPTION</span></span>
<span data-ttu-id="0991f-110">Hämtar Custom Resource Provider-manifestet.</span><span class="sxs-lookup"><span data-stu-id="0991f-110">Gets the custom resource provider manifest.</span></span>

## <span data-ttu-id="0991f-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="0991f-111">EXAMPLES</span></span>

### <span data-ttu-id="0991f-112">Exempel 1: lista alla anpassade leverantörer i ett abonnemang</span><span class="sxs-lookup"><span data-stu-id="0991f-112">Example 1: List all Custom Providers in a subscription</span></span>
```powershell
PS C:\> Get-AzCustomProvider

Location  Name             Type
--------  ----             ----
West US 2 Namespace.Type   Microsoft.CustomProviders/resourceproviders
East US 2 Namespace2.Type  Microsoft.CustomProviders/resourceproviders
```

<span data-ttu-id="0991f-113">Visar alla anpassade leverantörer i ett abonnemang</span><span class="sxs-lookup"><span data-stu-id="0991f-113">Lists all the custom providers in a subscription</span></span>

### <span data-ttu-id="0991f-114">Exempel 2: skaffa en enda anpassad leverantör</span><span class="sxs-lookup"><span data-stu-id="0991f-114">Example 2: Get a single custom provider</span></span>
```powershell
PS C:\> Get-AzCustomProvider -ResourceGroupName myRg -Name Namespace.Type | Format-List

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

<span data-ttu-id="0991f-115">Hämtar information för en anpassad leverantör.</span><span class="sxs-lookup"><span data-stu-id="0991f-115">Gets details for a single custom provider.</span></span>
<span data-ttu-id="0991f-116">Använd Format-List för att visa objekt information på skärmen.</span><span class="sxs-lookup"><span data-stu-id="0991f-116">Use Format-List to show object details on the screen.</span></span>

## <span data-ttu-id="0991f-117">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="0991f-117">PARAMETERS</span></span>

### <span data-ttu-id="0991f-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0991f-118">-DefaultProfile</span></span>
<span data-ttu-id="0991f-119">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="0991f-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0991f-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0991f-120">-InputObject</span></span>
<span data-ttu-id="0991f-121">Identitets parameter för att konstruera, se avsnittet anteckningar för INPUTOBJECT-egenskaper och skapa en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="0991f-121">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.CustomProviders.Models.ICustomProvidersIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0991f-122">-Namn</span><span class="sxs-lookup"><span data-stu-id="0991f-122">-Name</span></span>
<span data-ttu-id="0991f-123">Namnet på resurs leverantören.</span><span class="sxs-lookup"><span data-stu-id="0991f-123">The name of the resource provider.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: ResourceProviderName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0991f-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0991f-124">-ResourceGroupName</span></span>
<span data-ttu-id="0991f-125">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="0991f-125">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0991f-126">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="0991f-126">-SubscriptionId</span></span>
<span data-ttu-id="0991f-127">ID för Azure-prenumeration.</span><span class="sxs-lookup"><span data-stu-id="0991f-127">The Azure subscription ID.</span></span>
<span data-ttu-id="0991f-128">Det här är en GUID-formaterad sträng (till exempel 00000000-0000-0000-0000-000000000000)</span><span class="sxs-lookup"><span data-stu-id="0991f-128">This is a GUID-formatted string (e.g. 00000000-0000-0000-0000-000000000000)</span></span>

```yaml
Type: System.String[]
Parameter Sets: Get, List, List1
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0991f-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0991f-129">CommonParameters</span></span>
<span data-ttu-id="0991f-130">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0991f-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0991f-131">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="0991f-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0991f-132">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="0991f-132">INPUTS</span></span>

### <span data-ttu-id="0991f-133">Microsoft. Azure. PowerShell. cmdletar. CustomProviders. Models. ICustomProvidersIdentity</span><span class="sxs-lookup"><span data-stu-id="0991f-133">Microsoft.Azure.PowerShell.Cmdlets.CustomProviders.Models.ICustomProvidersIdentity</span></span>

## <span data-ttu-id="0991f-134">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="0991f-134">OUTPUTS</span></span>

### <span data-ttu-id="0991f-135">Microsoft. Azure. PowerShell. cmdletar. CustomProviders. Models. Api20180901Preview. ICustomRpManifest</span><span class="sxs-lookup"><span data-stu-id="0991f-135">Microsoft.Azure.PowerShell.Cmdlets.CustomProviders.Models.Api20180901Preview.ICustomRpManifest</span></span>

## <span data-ttu-id="0991f-136">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="0991f-136">NOTES</span></span>

<span data-ttu-id="0991f-137">ALIAS</span><span class="sxs-lookup"><span data-stu-id="0991f-137">ALIASES</span></span>

<span data-ttu-id="0991f-138">KOMPLEXA PARAMETER EGENSKAPER</span><span class="sxs-lookup"><span data-stu-id="0991f-138">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="0991f-139">Skapa en hash-tabell som innehåller lämpliga egenskaper för att lägga till de parametrar som beskrivs nedan.</span><span class="sxs-lookup"><span data-stu-id="0991f-139">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="0991f-140">Om du vill ha information om hash-tabeller kör Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="0991f-140">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="0991f-141">INPUTOBJECT <ICustomProvidersIdentity> : identitets parameter</span><span class="sxs-lookup"><span data-stu-id="0991f-141">INPUTOBJECT <ICustomProvidersIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="0991f-142">`[AssociationName <String>]`: Namnet på kopplingen.</span><span class="sxs-lookup"><span data-stu-id="0991f-142">`[AssociationName <String>]`: The name of the association.</span></span>
  - <span data-ttu-id="0991f-143">`[Id <String>]`: Sökväg till resurs identitet</span><span class="sxs-lookup"><span data-stu-id="0991f-143">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="0991f-144">`[ResourceGroupName <String>]`: Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="0991f-144">`[ResourceGroupName <String>]`: The name of the resource group.</span></span>
  - <span data-ttu-id="0991f-145">`[ResourceProviderName <String>]`: Resurs leverantörens namn.</span><span class="sxs-lookup"><span data-stu-id="0991f-145">`[ResourceProviderName <String>]`: The name of the resource provider.</span></span>
  - <span data-ttu-id="0991f-146">`[Scope <String>]`: Associationens omfattning.</span><span class="sxs-lookup"><span data-stu-id="0991f-146">`[Scope <String>]`: The scope of the association.</span></span>
  - <span data-ttu-id="0991f-147">`[SubscriptionId <String>]`: ID för Azure-prenumeration.</span><span class="sxs-lookup"><span data-stu-id="0991f-147">`[SubscriptionId <String>]`: The Azure subscription ID.</span></span> <span data-ttu-id="0991f-148">Det här är en GUID-formaterad sträng (till exempel 00000000-0000-0000-0000-000000000000)</span><span class="sxs-lookup"><span data-stu-id="0991f-148">This is a GUID-formatted string (e.g. 00000000-0000-0000-0000-000000000000)</span></span>

## <span data-ttu-id="0991f-149">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="0991f-149">RELATED LINKS</span></span>

