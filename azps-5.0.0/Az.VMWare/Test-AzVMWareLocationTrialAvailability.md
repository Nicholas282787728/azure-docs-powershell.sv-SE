---
external help file: ''
Module Name: Az.VMWare
online version: https://docs.microsoft.com/en-us/powershell/module/az.vmware/test-azvmwarelocationtrialavailability
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMWare/help/Test-AzVMWareLocationTrialAvailability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMWare/help/Test-AzVMWareLocationTrialAvailability.md
ms.openlocfilehash: 942ac0b4a8bca964e88c7dfd327fe460f249a915
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94325427"
---
# <span data-ttu-id="4bcaa-101">Test-AzVMWareLocationTrialAvailability</span><span class="sxs-lookup"><span data-stu-id="4bcaa-101">Test-AzVMWareLocationTrialAvailability</span></span>

## <span data-ttu-id="4bcaa-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="4bcaa-102">SYNOPSIS</span></span>
<span data-ttu-id="4bcaa-103">Returnera utvärderings status för abonnemang per region</span><span class="sxs-lookup"><span data-stu-id="4bcaa-103">Return trial status for subscription by region</span></span>

## <span data-ttu-id="4bcaa-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="4bcaa-104">SYNTAX</span></span>

### <span data-ttu-id="4bcaa-105">Kontrol lera (standard)</span><span class="sxs-lookup"><span data-stu-id="4bcaa-105">Check (Default)</span></span>
```
Test-AzVMWareLocationTrialAvailability -Location <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="4bcaa-106">CheckViaIdentity</span><span class="sxs-lookup"><span data-stu-id="4bcaa-106">CheckViaIdentity</span></span>
```
Test-AzVMWareLocationTrialAvailability -InputObject <IVMWareIdentity> [-DefaultProfile <PSObject>] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="4bcaa-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="4bcaa-107">DESCRIPTION</span></span>
<span data-ttu-id="4bcaa-108">Returnera utvärderings status för abonnemang per region</span><span class="sxs-lookup"><span data-stu-id="4bcaa-108">Return trial status for subscription by region</span></span>

## <span data-ttu-id="4bcaa-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="4bcaa-109">EXAMPLES</span></span>

### <span data-ttu-id="4bcaa-110">Exempel 1: kontrol lera utvärderings versionen</span><span class="sxs-lookup"><span data-stu-id="4bcaa-110">Example 1: Check trial availability</span></span>
```powershell
PS C:\> Test-AzVMWareLocationTrialAvailability -Location australiaeast

AvailableHost Status
------------- ------
0             TrialDisabled
```

<span data-ttu-id="4bcaa-111">Kontrol lera utvärderings versionen</span><span class="sxs-lookup"><span data-stu-id="4bcaa-111">Check trial availability</span></span>

## <span data-ttu-id="4bcaa-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="4bcaa-112">PARAMETERS</span></span>

### <span data-ttu-id="4bcaa-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4bcaa-113">-DefaultProfile</span></span>
<span data-ttu-id="4bcaa-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="4bcaa-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4bcaa-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4bcaa-115">-InputObject</span></span>
<span data-ttu-id="4bcaa-116">Identitets parameter för att konstruera, se avsnittet anteckningar för INPUTOBJECT-egenskaper och skapa en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="4bcaa-116">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.IVMWareIdentity
Parameter Sets: CheckViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4bcaa-117">-Plats</span><span class="sxs-lookup"><span data-stu-id="4bcaa-117">-Location</span></span>
<span data-ttu-id="4bcaa-118">Azure-region</span><span class="sxs-lookup"><span data-stu-id="4bcaa-118">Azure region</span></span>

```yaml
Type: System.String
Parameter Sets: Check
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4bcaa-119">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="4bcaa-119">-SubscriptionId</span></span>
<span data-ttu-id="4bcaa-120">ID för mål prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="4bcaa-120">The ID of the target subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: Check
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4bcaa-121">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="4bcaa-121">-Confirm</span></span>
<span data-ttu-id="4bcaa-122">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="4bcaa-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4bcaa-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4bcaa-123">-WhatIf</span></span>
<span data-ttu-id="4bcaa-124">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="4bcaa-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4bcaa-125">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="4bcaa-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4bcaa-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4bcaa-126">CommonParameters</span></span>
<span data-ttu-id="4bcaa-127">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4bcaa-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4bcaa-128">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="4bcaa-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4bcaa-129">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="4bcaa-129">INPUTS</span></span>

### <span data-ttu-id="4bcaa-130">Microsoft. Azure. PowerShell. cmdletar. VMWare. Models. IVMWareIdentity</span><span class="sxs-lookup"><span data-stu-id="4bcaa-130">Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.IVMWareIdentity</span></span>

## <span data-ttu-id="4bcaa-131">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="4bcaa-131">OUTPUTS</span></span>

### <span data-ttu-id="4bcaa-132">Microsoft. Azure. PowerShell. cmdletar. VMWare. Models. Api20200320. ITrial</span><span class="sxs-lookup"><span data-stu-id="4bcaa-132">Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.Api20200320.ITrial</span></span>

## <span data-ttu-id="4bcaa-133">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="4bcaa-133">NOTES</span></span>

<span data-ttu-id="4bcaa-134">ALIAS</span><span class="sxs-lookup"><span data-stu-id="4bcaa-134">ALIASES</span></span>

<span data-ttu-id="4bcaa-135">KOMPLEXA PARAMETER EGENSKAPER</span><span class="sxs-lookup"><span data-stu-id="4bcaa-135">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="4bcaa-136">Skapa en hash-tabell som innehåller lämpliga egenskaper för att lägga till de parametrar som beskrivs nedan.</span><span class="sxs-lookup"><span data-stu-id="4bcaa-136">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="4bcaa-137">Om du vill ha information om hash-tabeller kör Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="4bcaa-137">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="4bcaa-138">INPUTOBJECT <IVMWareIdentity> : identitets parameter</span><span class="sxs-lookup"><span data-stu-id="4bcaa-138">INPUTOBJECT <IVMWareIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="4bcaa-139">`[AuthorizationName <String>]`: Namnet på ExpressRoute-kretsen i det privata molnet</span><span class="sxs-lookup"><span data-stu-id="4bcaa-139">`[AuthorizationName <String>]`: Name of the ExpressRoute Circuit Authorization in the private cloud</span></span>
  - <span data-ttu-id="4bcaa-140">`[ClusterName <String>]`: Namnet på klustret i det privata molnet</span><span class="sxs-lookup"><span data-stu-id="4bcaa-140">`[ClusterName <String>]`: Name of the cluster in the private cloud</span></span>
  - <span data-ttu-id="4bcaa-141">`[HcxEnterpriseSiteName <String>]`: Namnet på den HCX företags webbplatsen i det privata molnet</span><span class="sxs-lookup"><span data-stu-id="4bcaa-141">`[HcxEnterpriseSiteName <String>]`: Name of the HCX Enterprise Site in the private cloud</span></span>
  - <span data-ttu-id="4bcaa-142">`[Id <String>]`: Sökväg till resurs identitet</span><span class="sxs-lookup"><span data-stu-id="4bcaa-142">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="4bcaa-143">`[Location <String>]`: Azure-region</span><span class="sxs-lookup"><span data-stu-id="4bcaa-143">`[Location <String>]`: Azure region</span></span>
  - <span data-ttu-id="4bcaa-144">`[PrivateCloudName <String>]`: Namnet på det privata molnet</span><span class="sxs-lookup"><span data-stu-id="4bcaa-144">`[PrivateCloudName <String>]`: Name of the private cloud</span></span>
  - <span data-ttu-id="4bcaa-145">`[ResourceGroupName <String>]`: Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="4bcaa-145">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="4bcaa-146">Namnet är Skift läges okänsligt.</span><span class="sxs-lookup"><span data-stu-id="4bcaa-146">The name is case insensitive.</span></span>
  - <span data-ttu-id="4bcaa-147">`[SubscriptionId <String>]`: Mål prenumerationens ID.</span><span class="sxs-lookup"><span data-stu-id="4bcaa-147">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>

## <span data-ttu-id="4bcaa-148">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="4bcaa-148">RELATED LINKS</span></span>

