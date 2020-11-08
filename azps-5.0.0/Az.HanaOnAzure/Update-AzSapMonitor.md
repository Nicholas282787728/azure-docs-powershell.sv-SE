---
external help file: ''
Module Name: Az.HanaOnAzure
online version: https://docs.microsoft.com/en-us/powershell/module/az.hanaonazure/update-azsapmonitor
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HanaOnAzure/help/Update-AzSapMonitor.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HanaOnAzure/help/Update-AzSapMonitor.md
ms.openlocfilehash: 9d87cfff428a5c3c176bea4deff95d0c652dc45a
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94270619"
---
# <span data-ttu-id="0df28-101">Update-AzSapMonitor</span><span class="sxs-lookup"><span data-stu-id="0df28-101">Update-AzSapMonitor</span></span>

## <span data-ttu-id="0df28-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="0df28-102">SYNOPSIS</span></span>
<span data-ttu-id="0df28-103">Byter till fältet taggar för en SAP-bildskärm för angiven prenumeration, resurs grupp och bildskärms namn.</span><span class="sxs-lookup"><span data-stu-id="0df28-103">Patches the Tags field of a SAP monitor for the specified subscription, resource group, and monitor name.</span></span>

## <span data-ttu-id="0df28-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="0df28-104">SYNTAX</span></span>

### <span data-ttu-id="0df28-105">UpdateExpanded (standard)</span><span class="sxs-lookup"><span data-stu-id="0df28-105">UpdateExpanded (Default)</span></span>
```
Update-AzSapMonitor -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>] [-Tag <Hashtable>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="0df28-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="0df28-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzSapMonitor -InputObject <IHanaOnAzureIdentity> [-Tag <Hashtable>] [-DefaultProfile <PSObject>]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="0df28-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="0df28-107">DESCRIPTION</span></span>
<span data-ttu-id="0df28-108">Byter till fältet taggar för en SAP-bildskärm för angiven prenumeration, resurs grupp och bildskärms namn.</span><span class="sxs-lookup"><span data-stu-id="0df28-108">Patches the Tags field of a SAP monitor for the specified subscription, resource group, and monitor name.</span></span>

## <span data-ttu-id="0df28-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="0df28-109">EXAMPLES</span></span>

### <span data-ttu-id="0df28-110">Exempel 1: uppdatera en SAP-övervakare efter namn</span><span class="sxs-lookup"><span data-stu-id="0df28-110">Example 1: Update a SAP monitor by name</span></span>
```powershell
PS C:\> Update-AzSapMonitor -ResourceGroupName nancyc-hn1 -Name ps-spamonitor-t01 -Tag @{'key'=1;'key2'=2; 'key3'=3}

Location Name              Type
-------- ----              ----
westus2  ps-spamonitor-t01 Microsoft.HanaOnAzure/sapMonitors
```

<span data-ttu-id="0df28-111">Det här kommandot uppdaterar en SAP-bildskärm efter namn.</span><span class="sxs-lookup"><span data-stu-id="0df28-111">This commands updates a SAP monitor by name.</span></span>

### <span data-ttu-id="0df28-112">Exempel 2: uppdatera en SAP-övervakare efter objekt</span><span class="sxs-lookup"><span data-stu-id="0df28-112">Example 2: Update a SAP monitor by object</span></span>
```powershell
PS C:\> $sap = Get-AzSapMonitor -ResourceGroupName nancyc-hn1 -Name ps-sapmonitor-t01
PS C:\> Update-AzSapMonitor -InputObject $sap -Tag @{'key'=1;'key2'=2; 'key3'=3}

Location Name              Type
-------- ----              ----
westus2  ps-sapmonitor-t01 Microsoft.HanaOnAzure/sapMonitors
```

<span data-ttu-id="0df28-113">Det här kommandot uppdaterar en SAP-skärm efter objekt.</span><span class="sxs-lookup"><span data-stu-id="0df28-113">This commands updates a SAP monitor by object.</span></span>

## <span data-ttu-id="0df28-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="0df28-114">PARAMETERS</span></span>

### <span data-ttu-id="0df28-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0df28-115">-DefaultProfile</span></span>
<span data-ttu-id="0df28-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="0df28-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0df28-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0df28-117">-InputObject</span></span>
<span data-ttu-id="0df28-118">Identitets parameter för att konstruera, se avsnittet anteckningar för INPUTOBJECT-egenskaper och skapa en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="0df28-118">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.HanaOnAzure.Models.IHanaOnAzureIdentity
Parameter Sets: UpdateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0df28-119">-Namn</span><span class="sxs-lookup"><span data-stu-id="0df28-119">-Name</span></span>
<span data-ttu-id="0df28-120">Namnet på SAP Monitor-resursen.</span><span class="sxs-lookup"><span data-stu-id="0df28-120">Name of the SAP monitor resource.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases: SapMonitorName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0df28-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0df28-121">-ResourceGroupName</span></span>
<span data-ttu-id="0df28-122">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="0df28-122">Name of the resource group.</span></span>

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

### <span data-ttu-id="0df28-123">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="0df28-123">-SubscriptionId</span></span>
<span data-ttu-id="0df28-124">Abonnemangs-ID som unikt identifierar Microsoft Azure-prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="0df28-124">Subscription ID which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="0df28-125">Prenumerations-ID: t utgör en del av URI: n för varje service samtal.</span><span class="sxs-lookup"><span data-stu-id="0df28-125">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="0df28-126">-Tagg</span><span class="sxs-lookup"><span data-stu-id="0df28-126">-Tag</span></span>
<span data-ttu-id="0df28-127">Fältet taggar för resursen.</span><span class="sxs-lookup"><span data-stu-id="0df28-127">Tags field of the resource.</span></span>

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

### <span data-ttu-id="0df28-128">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="0df28-128">-Confirm</span></span>
<span data-ttu-id="0df28-129">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="0df28-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0df28-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0df28-130">-WhatIf</span></span>
<span data-ttu-id="0df28-131">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="0df28-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0df28-132">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="0df28-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0df28-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0df28-133">CommonParameters</span></span>
<span data-ttu-id="0df28-134">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0df28-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0df28-135">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="0df28-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0df28-136">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="0df28-136">INPUTS</span></span>

### <span data-ttu-id="0df28-137">Microsoft. Azure. PowerShell. cmdletar. HanaOnAzure. Models. IHanaOnAzureIdentity</span><span class="sxs-lookup"><span data-stu-id="0df28-137">Microsoft.Azure.PowerShell.Cmdlets.HanaOnAzure.Models.IHanaOnAzureIdentity</span></span>

## <span data-ttu-id="0df28-138">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="0df28-138">OUTPUTS</span></span>

### <span data-ttu-id="0df28-139">Microsoft. Azure. PowerShell. cmdletar. HanaOnAzure. Models. Api20200207Preview. ISapMonitor</span><span class="sxs-lookup"><span data-stu-id="0df28-139">Microsoft.Azure.PowerShell.Cmdlets.HanaOnAzure.Models.Api20200207Preview.ISapMonitor</span></span>

## <span data-ttu-id="0df28-140">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="0df28-140">NOTES</span></span>

<span data-ttu-id="0df28-141">ALIAS</span><span class="sxs-lookup"><span data-stu-id="0df28-141">ALIASES</span></span>

<span data-ttu-id="0df28-142">KOMPLEXA PARAMETER EGENSKAPER</span><span class="sxs-lookup"><span data-stu-id="0df28-142">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="0df28-143">Skapa en hash-tabell som innehåller lämpliga egenskaper för att lägga till de parametrar som beskrivs nedan.</span><span class="sxs-lookup"><span data-stu-id="0df28-143">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="0df28-144">Om du vill ha information om hash-tabeller kör Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="0df28-144">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="0df28-145">INPUTOBJECT <IHanaOnAzureIdentity> : identitets parameter</span><span class="sxs-lookup"><span data-stu-id="0df28-145">INPUTOBJECT <IHanaOnAzureIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="0df28-146">`[Id <String>]`: Sökväg till resurs identitet</span><span class="sxs-lookup"><span data-stu-id="0df28-146">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="0df28-147">`[Location <String>]`: Platsen för det borttagna valvet.</span><span class="sxs-lookup"><span data-stu-id="0df28-147">`[Location <String>]`: The location of the deleted vault.</span></span>
  - <span data-ttu-id="0df28-148">`[OperationKind <AccessPolicyUpdateKind?>]`: Åtgärdens namn</span><span class="sxs-lookup"><span data-stu-id="0df28-148">`[OperationKind <AccessPolicyUpdateKind?>]`: Name of the operation</span></span>
  - <span data-ttu-id="0df28-149">`[ProviderInstanceName <String>]`: Namnet på leverantörs instansen.</span><span class="sxs-lookup"><span data-stu-id="0df28-149">`[ProviderInstanceName <String>]`: Name of the provider instance.</span></span>
  - <span data-ttu-id="0df28-150">`[ResourceGroupName <String>]`: Resurs gruppens namn.</span><span class="sxs-lookup"><span data-stu-id="0df28-150">`[ResourceGroupName <String>]`: Name of the resource group.</span></span>
  - <span data-ttu-id="0df28-151">`[ResourceName <String>]`: Namnet på identitets resursen.</span><span class="sxs-lookup"><span data-stu-id="0df28-151">`[ResourceName <String>]`: The name of the identity resource.</span></span>
  - <span data-ttu-id="0df28-152">`[SapMonitorName <String>]`: Namnet på SAP Monitor-resursen.</span><span class="sxs-lookup"><span data-stu-id="0df28-152">`[SapMonitorName <String>]`: Name of the SAP monitor resource.</span></span>
  - <span data-ttu-id="0df28-153">`[Scope <String>]`: Resursens resurs leverantörs omfattning.</span><span class="sxs-lookup"><span data-stu-id="0df28-153">`[Scope <String>]`: The resource provider scope of the resource.</span></span> <span data-ttu-id="0df28-154">Överordnad resurs som utökas av hanterade identiteter.</span><span class="sxs-lookup"><span data-stu-id="0df28-154">Parent resource being extended by Managed Identities.</span></span>
  - <span data-ttu-id="0df28-155">`[SubscriptionId <String>]`: Prenumerations-ID som unikt identifierar Microsoft Azure-prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="0df28-155">`[SubscriptionId <String>]`: Subscription ID which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="0df28-156">Prenumerations-ID: t utgör en del av URI: n för varje service samtal.</span><span class="sxs-lookup"><span data-stu-id="0df28-156">The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="0df28-157">`[VaultName <String>]`: Namnet på valvet</span><span class="sxs-lookup"><span data-stu-id="0df28-157">`[VaultName <String>]`: Name of the vault</span></span>

## <span data-ttu-id="0df28-158">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="0df28-158">RELATED LINKS</span></span>

