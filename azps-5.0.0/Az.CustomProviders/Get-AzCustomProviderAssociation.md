---
external help file: ''
Module Name: Az.CustomProviders
online version: https://docs.microsoft.com/en-us/powershell/module/az.customproviders/get-azcustomproviderassociation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CustomProviders/help/Get-AzCustomProviderAssociation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CustomProviders/help/Get-AzCustomProviderAssociation.md
ms.openlocfilehash: 08d760c73256b71842fac36a7d095db2aab21128
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94321304"
---
# <span data-ttu-id="4d677-101">Get-AzCustomProviderAssociation</span><span class="sxs-lookup"><span data-stu-id="4d677-101">Get-AzCustomProviderAssociation</span></span>

## <span data-ttu-id="4d677-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="4d677-102">SYNOPSIS</span></span>
<span data-ttu-id="4d677-103">Skaffa en koppling.</span><span class="sxs-lookup"><span data-stu-id="4d677-103">Get an association.</span></span>

## <span data-ttu-id="4d677-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="4d677-104">SYNTAX</span></span>

### <span data-ttu-id="4d677-105">Lista (standard)</span><span class="sxs-lookup"><span data-stu-id="4d677-105">List (Default)</span></span>
```
Get-AzCustomProviderAssociation -Scope <String> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="4d677-106">Lära</span><span class="sxs-lookup"><span data-stu-id="4d677-106">Get</span></span>
```
Get-AzCustomProviderAssociation -Name <String> -Scope <String> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="4d677-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="4d677-107">GetViaIdentity</span></span>
```
Get-AzCustomProviderAssociation -InputObject <ICustomProvidersIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="4d677-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="4d677-108">DESCRIPTION</span></span>
<span data-ttu-id="4d677-109">Skaffa en koppling.</span><span class="sxs-lookup"><span data-stu-id="4d677-109">Get an association.</span></span>

## <span data-ttu-id="4d677-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="4d677-110">EXAMPLES</span></span>

### <span data-ttu-id="4d677-111">Exempel 1: lista med anpassade leverantörs kopplingar</span><span class="sxs-lookup"><span data-stu-id="4d677-111">Example 1: List custom provider associations</span></span>
```powershell
PS C:\> Get-AzCustomProviderAssociation

Location  Name             Type
--------  ----             ----
East US 2 MyAssoc   Microsoft.CustomProviders/associations
```

<span data-ttu-id="4d677-112">Lista alla egna leverantörs associationer för ett givet område.</span><span class="sxs-lookup"><span data-stu-id="4d677-112">List all custom provider associations for a given scope.</span></span>

### <span data-ttu-id="4d677-113">Exempel 2: skaffa en Association</span><span class="sxs-lookup"><span data-stu-id="4d677-113">Example 2: Get an association</span></span>
```powershell
PS C:\> Get-AzCustomProviderAssociation -Scope $resourceId -Name MyAssoc

Location  Name             Type
--------  ----             ----
East US 2 MyAssoc   Microsoft.CustomProviders/associations
```

<span data-ttu-id="4d677-114">Få information om en enda CustomProvider-associering</span><span class="sxs-lookup"><span data-stu-id="4d677-114">Get details for a single CustomProvider association</span></span>

## <span data-ttu-id="4d677-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="4d677-115">PARAMETERS</span></span>

### <span data-ttu-id="4d677-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4d677-116">-DefaultProfile</span></span>
<span data-ttu-id="4d677-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="4d677-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4d677-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4d677-118">-InputObject</span></span>
<span data-ttu-id="4d677-119">Identitets parameter för att konstruera, se avsnittet anteckningar för INPUTOBJECT-egenskaper och skapa en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="4d677-119">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="4d677-120">-Namn</span><span class="sxs-lookup"><span data-stu-id="4d677-120">-Name</span></span>
<span data-ttu-id="4d677-121">Namnet på kopplingen.</span><span class="sxs-lookup"><span data-stu-id="4d677-121">The name of the association.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: AssociationName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4d677-122">-Omfattning</span><span class="sxs-lookup"><span data-stu-id="4d677-122">-Scope</span></span>
<span data-ttu-id="4d677-123">Associeringens omfattning.</span><span class="sxs-lookup"><span data-stu-id="4d677-123">The scope of the association.</span></span>

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

### <span data-ttu-id="4d677-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4d677-124">CommonParameters</span></span>
<span data-ttu-id="4d677-125">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4d677-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4d677-126">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="4d677-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4d677-127">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="4d677-127">INPUTS</span></span>

### <span data-ttu-id="4d677-128">Microsoft. Azure. PowerShell. cmdletar. CustomProviders. Models. ICustomProvidersIdentity</span><span class="sxs-lookup"><span data-stu-id="4d677-128">Microsoft.Azure.PowerShell.Cmdlets.CustomProviders.Models.ICustomProvidersIdentity</span></span>

## <span data-ttu-id="4d677-129">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="4d677-129">OUTPUTS</span></span>

### <span data-ttu-id="4d677-130">Microsoft. Azure. PowerShell. cmdletar. CustomProviders. Models. Api20180901Preview. IAssociation</span><span class="sxs-lookup"><span data-stu-id="4d677-130">Microsoft.Azure.PowerShell.Cmdlets.CustomProviders.Models.Api20180901Preview.IAssociation</span></span>

## <span data-ttu-id="4d677-131">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="4d677-131">NOTES</span></span>

<span data-ttu-id="4d677-132">ALIAS</span><span class="sxs-lookup"><span data-stu-id="4d677-132">ALIASES</span></span>

<span data-ttu-id="4d677-133">KOMPLEXA PARAMETER EGENSKAPER</span><span class="sxs-lookup"><span data-stu-id="4d677-133">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="4d677-134">Skapa en hash-tabell som innehåller lämpliga egenskaper för att lägga till de parametrar som beskrivs nedan.</span><span class="sxs-lookup"><span data-stu-id="4d677-134">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="4d677-135">Om du vill ha information om hash-tabeller kör Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="4d677-135">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="4d677-136">INPUTOBJECT <ICustomProvidersIdentity> : identitets parameter</span><span class="sxs-lookup"><span data-stu-id="4d677-136">INPUTOBJECT <ICustomProvidersIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="4d677-137">`[AssociationName <String>]`: Namnet på kopplingen.</span><span class="sxs-lookup"><span data-stu-id="4d677-137">`[AssociationName <String>]`: The name of the association.</span></span>
  - <span data-ttu-id="4d677-138">`[Id <String>]`: Sökväg till resurs identitet</span><span class="sxs-lookup"><span data-stu-id="4d677-138">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="4d677-139">`[ResourceGroupName <String>]`: Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="4d677-139">`[ResourceGroupName <String>]`: The name of the resource group.</span></span>
  - <span data-ttu-id="4d677-140">`[ResourceProviderName <String>]`: Resurs leverantörens namn.</span><span class="sxs-lookup"><span data-stu-id="4d677-140">`[ResourceProviderName <String>]`: The name of the resource provider.</span></span>
  - <span data-ttu-id="4d677-141">`[Scope <String>]`: Associationens omfattning.</span><span class="sxs-lookup"><span data-stu-id="4d677-141">`[Scope <String>]`: The scope of the association.</span></span>
  - <span data-ttu-id="4d677-142">`[SubscriptionId <String>]`: ID för Azure-prenumeration.</span><span class="sxs-lookup"><span data-stu-id="4d677-142">`[SubscriptionId <String>]`: The Azure subscription ID.</span></span> <span data-ttu-id="4d677-143">Det här är en GUID-formaterad sträng (till exempel 00000000-0000-0000-0000-000000000000)</span><span class="sxs-lookup"><span data-stu-id="4d677-143">This is a GUID-formatted string (e.g. 00000000-0000-0000-0000-000000000000)</span></span>

## <span data-ttu-id="4d677-144">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="4d677-144">RELATED LINKS</span></span>
