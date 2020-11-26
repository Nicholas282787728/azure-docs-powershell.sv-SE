---
external help file: ''
Module Name: Az.HanaOnAzure
online version: https://docs.microsoft.com/en-us/powershell/module/az.hanaonazure/remove-azsapmonitor
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HanaOnAzure/help/Remove-AzSapMonitor.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HanaOnAzure/help/Remove-AzSapMonitor.md
ms.openlocfilehash: bcba06d87bce2f9ccc8016afc9f08dff75e29b1c
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94263067"
---
# <span data-ttu-id="da846-101">Remove-AzSapMonitor</span><span class="sxs-lookup"><span data-stu-id="da846-101">Remove-AzSapMonitor</span></span>

## <span data-ttu-id="da846-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="da846-102">SYNOPSIS</span></span>
<span data-ttu-id="da846-103">Tar bort en SAP-övervakare med angiven prenumeration, resurs grupp och övervakarens namn.</span><span class="sxs-lookup"><span data-stu-id="da846-103">Deletes a SAP monitor with the specified subscription, resource group, and monitor name.</span></span>

## <span data-ttu-id="da846-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="da846-104">SYNTAX</span></span>

### <span data-ttu-id="da846-105">Ta bort (standard)</span><span class="sxs-lookup"><span data-stu-id="da846-105">Delete (Default)</span></span>
```
Remove-AzSapMonitor -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="da846-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="da846-106">DeleteViaIdentity</span></span>
```
Remove-AzSapMonitor -InputObject <IHanaOnAzureIdentity> [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="da846-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="da846-107">DESCRIPTION</span></span>
<span data-ttu-id="da846-108">Tar bort en SAP-övervakare med angiven prenumeration, resurs grupp och övervakarens namn.</span><span class="sxs-lookup"><span data-stu-id="da846-108">Deletes a SAP monitor with the specified subscription, resource group, and monitor name.</span></span>

## <span data-ttu-id="da846-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="da846-109">EXAMPLES</span></span>

### <span data-ttu-id="da846-110">Exempel 1: ta bort en SAP-övervakare efter namn</span><span class="sxs-lookup"><span data-stu-id="da846-110">Example 1: Remove a SAP monitor by name</span></span>
```powershell
PS C:\> Remove-AzSapMonitor -ResourceGroupName nancyc-hn1 -Name ps-sapmonitor-t02

```

<span data-ttu-id="da846-111">Det här kommandot tar bort en SAP-skärm med namn.</span><span class="sxs-lookup"><span data-stu-id="da846-111">This command removes a SAP monitor by name.</span></span>

### <span data-ttu-id="da846-112">Exempel 2: ta bort en SAP-övervakare efter objekt</span><span class="sxs-lookup"><span data-stu-id="da846-112">Example 2: Remove a SAP monitor by object</span></span>
```powershell
PS C:\> $sap = Get-AzSapMonitor -ResourceGroupName nancyc-hn1 -Name ps-sapmonitor-t01
PS C:\> Remove-AzSapMonitor -InputObject $sap

```

<span data-ttu-id="da846-113">Det här kommandot tar bort en SAP-skärm efter objekt.</span><span class="sxs-lookup"><span data-stu-id="da846-113">This command removes a SAP monitor by object.</span></span>

## <span data-ttu-id="da846-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="da846-114">PARAMETERS</span></span>

### <span data-ttu-id="da846-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="da846-115">-AsJob</span></span>
<span data-ttu-id="da846-116">Köra kommandot som ett jobb</span><span class="sxs-lookup"><span data-stu-id="da846-116">Run the command as a job</span></span>

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

### <span data-ttu-id="da846-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="da846-117">-DefaultProfile</span></span>
<span data-ttu-id="da846-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="da846-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="da846-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="da846-119">-InputObject</span></span>
<span data-ttu-id="da846-120">Identitets parameter för att konstruera, se avsnittet anteckningar för INPUTOBJECT-egenskaper och skapa en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="da846-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.HanaOnAzure.Models.IHanaOnAzureIdentity
Parameter Sets: DeleteViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="da846-121">-Namn</span><span class="sxs-lookup"><span data-stu-id="da846-121">-Name</span></span>
<span data-ttu-id="da846-122">Namnet på SAP Monitor-resursen.</span><span class="sxs-lookup"><span data-stu-id="da846-122">Name of the SAP monitor resource.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases: SapMonitorName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="da846-123">-Nowait</span><span class="sxs-lookup"><span data-stu-id="da846-123">-NoWait</span></span>
<span data-ttu-id="da846-124">Kör kommandot asynkront</span><span class="sxs-lookup"><span data-stu-id="da846-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="da846-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="da846-125">-PassThru</span></span>
<span data-ttu-id="da846-126">Returnerar true när kommandot lyckas</span><span class="sxs-lookup"><span data-stu-id="da846-126">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="da846-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="da846-127">-ResourceGroupName</span></span>
<span data-ttu-id="da846-128">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="da846-128">Name of the resource group.</span></span>

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

### <span data-ttu-id="da846-129">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="da846-129">-SubscriptionId</span></span>
<span data-ttu-id="da846-130">Abonnemangs-ID som unikt identifierar Microsoft Azure-prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="da846-130">Subscription ID which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="da846-131">Prenumerations-ID: t utgör en del av URI: n för varje service samtal.</span><span class="sxs-lookup"><span data-stu-id="da846-131">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="da846-132">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="da846-132">-Confirm</span></span>
<span data-ttu-id="da846-133">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="da846-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="da846-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="da846-134">-WhatIf</span></span>
<span data-ttu-id="da846-135">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="da846-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="da846-136">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="da846-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="da846-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="da846-137">CommonParameters</span></span>
<span data-ttu-id="da846-138">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="da846-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="da846-139">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="da846-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="da846-140">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="da846-140">INPUTS</span></span>

### <span data-ttu-id="da846-141">Microsoft. Azure. PowerShell. cmdletar. HanaOnAzure. Models. IHanaOnAzureIdentity</span><span class="sxs-lookup"><span data-stu-id="da846-141">Microsoft.Azure.PowerShell.Cmdlets.HanaOnAzure.Models.IHanaOnAzureIdentity</span></span>

## <span data-ttu-id="da846-142">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="da846-142">OUTPUTS</span></span>

### <span data-ttu-id="da846-143">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="da846-143">System.Boolean</span></span>

## <span data-ttu-id="da846-144">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="da846-144">NOTES</span></span>

<span data-ttu-id="da846-145">ALIAS</span><span class="sxs-lookup"><span data-stu-id="da846-145">ALIASES</span></span>

<span data-ttu-id="da846-146">KOMPLEXA PARAMETER EGENSKAPER</span><span class="sxs-lookup"><span data-stu-id="da846-146">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="da846-147">Skapa en hash-tabell som innehåller lämpliga egenskaper för att lägga till de parametrar som beskrivs nedan.</span><span class="sxs-lookup"><span data-stu-id="da846-147">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="da846-148">Om du vill ha information om hash-tabeller kör Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="da846-148">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="da846-149">INPUTOBJECT <IHanaOnAzureIdentity> : identitets parameter</span><span class="sxs-lookup"><span data-stu-id="da846-149">INPUTOBJECT <IHanaOnAzureIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="da846-150">`[Id <String>]`: Sökväg till resurs identitet</span><span class="sxs-lookup"><span data-stu-id="da846-150">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="da846-151">`[Location <String>]`: Platsen för det borttagna valvet.</span><span class="sxs-lookup"><span data-stu-id="da846-151">`[Location <String>]`: The location of the deleted vault.</span></span>
  - <span data-ttu-id="da846-152">`[OperationKind <AccessPolicyUpdateKind?>]`: Åtgärdens namn</span><span class="sxs-lookup"><span data-stu-id="da846-152">`[OperationKind <AccessPolicyUpdateKind?>]`: Name of the operation</span></span>
  - <span data-ttu-id="da846-153">`[ProviderInstanceName <String>]`: Namnet på leverantörs instansen.</span><span class="sxs-lookup"><span data-stu-id="da846-153">`[ProviderInstanceName <String>]`: Name of the provider instance.</span></span>
  - <span data-ttu-id="da846-154">`[ResourceGroupName <String>]`: Resurs gruppens namn.</span><span class="sxs-lookup"><span data-stu-id="da846-154">`[ResourceGroupName <String>]`: Name of the resource group.</span></span>
  - <span data-ttu-id="da846-155">`[ResourceName <String>]`: Namnet på identitets resursen.</span><span class="sxs-lookup"><span data-stu-id="da846-155">`[ResourceName <String>]`: The name of the identity resource.</span></span>
  - <span data-ttu-id="da846-156">`[SapMonitorName <String>]`: Namnet på SAP Monitor-resursen.</span><span class="sxs-lookup"><span data-stu-id="da846-156">`[SapMonitorName <String>]`: Name of the SAP monitor resource.</span></span>
  - <span data-ttu-id="da846-157">`[Scope <String>]`: Resursens resurs leverantörs omfattning.</span><span class="sxs-lookup"><span data-stu-id="da846-157">`[Scope <String>]`: The resource provider scope of the resource.</span></span> <span data-ttu-id="da846-158">Överordnad resurs som utökas av hanterade identiteter.</span><span class="sxs-lookup"><span data-stu-id="da846-158">Parent resource being extended by Managed Identities.</span></span>
  - <span data-ttu-id="da846-159">`[SubscriptionId <String>]`: Prenumerations-ID som unikt identifierar Microsoft Azure-prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="da846-159">`[SubscriptionId <String>]`: Subscription ID which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="da846-160">Prenumerations-ID: t utgör en del av URI: n för varje service samtal.</span><span class="sxs-lookup"><span data-stu-id="da846-160">The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="da846-161">`[VaultName <String>]`: Namnet på valvet</span><span class="sxs-lookup"><span data-stu-id="da846-161">`[VaultName <String>]`: Name of the vault</span></span>

## <span data-ttu-id="da846-162">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="da846-162">RELATED LINKS</span></span>
