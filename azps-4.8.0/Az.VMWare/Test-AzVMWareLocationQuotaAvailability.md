---
external help file: ''
Module Name: Az.VMWare
online version: https://docs.microsoft.com/en-us/powershell/module/az.vmware/test-azvmwarelocationquotaavailability
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMWare/help/Test-AzVMWareLocationQuotaAvailability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMWare/help/Test-AzVMWareLocationQuotaAvailability.md
ms.openlocfilehash: 9cb677ff172c986f18c7c11c00e0f8d7e0bbf5bf
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94260184"
---
# <span data-ttu-id="f96bd-101">Test-AzVMWareLocationQuotaAvailability</span><span class="sxs-lookup"><span data-stu-id="f96bd-101">Test-AzVMWareLocationQuotaAvailability</span></span>

## <span data-ttu-id="f96bd-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="f96bd-102">SYNOPSIS</span></span>
<span data-ttu-id="f96bd-103">Returnera kvot för abonnemang per region</span><span class="sxs-lookup"><span data-stu-id="f96bd-103">Return quota for subscription by region</span></span>

## <span data-ttu-id="f96bd-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="f96bd-104">SYNTAX</span></span>

### <span data-ttu-id="f96bd-105">Kontrol lera (standard)</span><span class="sxs-lookup"><span data-stu-id="f96bd-105">Check (Default)</span></span>
```
Test-AzVMWareLocationQuotaAvailability -Location <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="f96bd-106">CheckViaIdentity</span><span class="sxs-lookup"><span data-stu-id="f96bd-106">CheckViaIdentity</span></span>
```
Test-AzVMWareLocationQuotaAvailability -InputObject <IVMWareIdentity> [-DefaultProfile <PSObject>] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="f96bd-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="f96bd-107">DESCRIPTION</span></span>
<span data-ttu-id="f96bd-108">Returnera kvot för abonnemang per region</span><span class="sxs-lookup"><span data-stu-id="f96bd-108">Return quota for subscription by region</span></span>

## <span data-ttu-id="f96bd-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="f96bd-109">EXAMPLES</span></span>

### <span data-ttu-id="f96bd-110">Exempel 1: kontrol lera kvot tillgänglighet</span><span class="sxs-lookup"><span data-stu-id="f96bd-110">Example 1: Check quota availability</span></span>
```powershell
PS C:\> Test-AzVMWareLocationQuotaAvailability -Location eastus

Enabled
-------
Disabled
```

<span data-ttu-id="f96bd-111">Kontrol lera kvot tillgänglighet</span><span class="sxs-lookup"><span data-stu-id="f96bd-111">Check quota availability</span></span>

## <span data-ttu-id="f96bd-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="f96bd-112">PARAMETERS</span></span>

### <span data-ttu-id="f96bd-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f96bd-113">-DefaultProfile</span></span>
<span data-ttu-id="f96bd-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="f96bd-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f96bd-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f96bd-115">-InputObject</span></span>
<span data-ttu-id="f96bd-116">Identitets parameter för att konstruera, se avsnittet anteckningar för INPUTOBJECT-egenskaper och skapa en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="f96bd-116">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="f96bd-117">-Plats</span><span class="sxs-lookup"><span data-stu-id="f96bd-117">-Location</span></span>
<span data-ttu-id="f96bd-118">Azure-region</span><span class="sxs-lookup"><span data-stu-id="f96bd-118">Azure region</span></span>

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

### <span data-ttu-id="f96bd-119">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="f96bd-119">-SubscriptionId</span></span>
<span data-ttu-id="f96bd-120">ID för mål prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="f96bd-120">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="f96bd-121">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="f96bd-121">-Confirm</span></span>
<span data-ttu-id="f96bd-122">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="f96bd-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f96bd-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f96bd-123">-WhatIf</span></span>
<span data-ttu-id="f96bd-124">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="f96bd-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f96bd-125">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="f96bd-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f96bd-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f96bd-126">CommonParameters</span></span>
<span data-ttu-id="f96bd-127">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f96bd-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f96bd-128">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f96bd-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f96bd-129">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="f96bd-129">INPUTS</span></span>

### <span data-ttu-id="f96bd-130">Microsoft. Azure. PowerShell. cmdletar. VMWare. Models. IVMWareIdentity</span><span class="sxs-lookup"><span data-stu-id="f96bd-130">Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.IVMWareIdentity</span></span>

## <span data-ttu-id="f96bd-131">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="f96bd-131">OUTPUTS</span></span>

### <span data-ttu-id="f96bd-132">Microsoft. Azure. PowerShell. cmdletar. VMWare. Models. Api20200320. IQuota</span><span class="sxs-lookup"><span data-stu-id="f96bd-132">Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.Api20200320.IQuota</span></span>

## <span data-ttu-id="f96bd-133">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="f96bd-133">NOTES</span></span>

<span data-ttu-id="f96bd-134">ALIAS</span><span class="sxs-lookup"><span data-stu-id="f96bd-134">ALIASES</span></span>

<span data-ttu-id="f96bd-135">KOMPLEXA PARAMETER EGENSKAPER</span><span class="sxs-lookup"><span data-stu-id="f96bd-135">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="f96bd-136">Skapa en hash-tabell som innehåller lämpliga egenskaper för att lägga till de parametrar som beskrivs nedan.</span><span class="sxs-lookup"><span data-stu-id="f96bd-136">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="f96bd-137">Om du vill ha information om hash-tabeller kör Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="f96bd-137">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="f96bd-138">INPUTOBJECT <IVMWareIdentity> : identitets parameter</span><span class="sxs-lookup"><span data-stu-id="f96bd-138">INPUTOBJECT <IVMWareIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="f96bd-139">`[AuthorizationName <String>]`: Namnet på ExpressRoute-kretsen i det privata molnet</span><span class="sxs-lookup"><span data-stu-id="f96bd-139">`[AuthorizationName <String>]`: Name of the ExpressRoute Circuit Authorization in the private cloud</span></span>
  - <span data-ttu-id="f96bd-140">`[ClusterName <String>]`: Namnet på klustret i det privata molnet</span><span class="sxs-lookup"><span data-stu-id="f96bd-140">`[ClusterName <String>]`: Name of the cluster in the private cloud</span></span>
  - <span data-ttu-id="f96bd-141">`[HcxEnterpriseSiteName <String>]`: Namnet på den HCX företags webbplatsen i det privata molnet</span><span class="sxs-lookup"><span data-stu-id="f96bd-141">`[HcxEnterpriseSiteName <String>]`: Name of the HCX Enterprise Site in the private cloud</span></span>
  - <span data-ttu-id="f96bd-142">`[Id <String>]`: Sökväg till resurs identitet</span><span class="sxs-lookup"><span data-stu-id="f96bd-142">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="f96bd-143">`[Location <String>]`: Azure-region</span><span class="sxs-lookup"><span data-stu-id="f96bd-143">`[Location <String>]`: Azure region</span></span>
  - <span data-ttu-id="f96bd-144">`[PrivateCloudName <String>]`: Namnet på det privata molnet</span><span class="sxs-lookup"><span data-stu-id="f96bd-144">`[PrivateCloudName <String>]`: Name of the private cloud</span></span>
  - <span data-ttu-id="f96bd-145">`[ResourceGroupName <String>]`: Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="f96bd-145">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="f96bd-146">Namnet är Skift läges okänsligt.</span><span class="sxs-lookup"><span data-stu-id="f96bd-146">The name is case insensitive.</span></span>
  - <span data-ttu-id="f96bd-147">`[SubscriptionId <String>]`: Mål prenumerationens ID.</span><span class="sxs-lookup"><span data-stu-id="f96bd-147">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>

## <span data-ttu-id="f96bd-148">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="f96bd-148">RELATED LINKS</span></span>
