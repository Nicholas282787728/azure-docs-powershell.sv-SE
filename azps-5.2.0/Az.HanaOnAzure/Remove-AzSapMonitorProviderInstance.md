---
external help file: ''
Module Name: Az.HanaOnAzure
online version: https://docs.microsoft.com/en-us/powershell/module/az.hanaonazure/remove-azsapmonitorproviderinstance
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HanaOnAzure/help/Remove-AzSapMonitorProviderInstance.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HanaOnAzure/help/Remove-AzSapMonitorProviderInstance.md
ms.openlocfilehash: 53f251b001b4e2f6319840079e9db3111c00b006
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98397171"
---
# <span data-ttu-id="33c98-101">Remove-AzSapMonitorProviderInstance</span><span class="sxs-lookup"><span data-stu-id="33c98-101">Remove-AzSapMonitorProviderInstance</span></span>

## <span data-ttu-id="33c98-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="33c98-102">SYNOPSIS</span></span>
<span data-ttu-id="33c98-103">Tar bort en tjänste instans för angiven prenumeration, resurs grupp, SapMonitor-namn och resurs namn.</span><span class="sxs-lookup"><span data-stu-id="33c98-103">Deletes a provider instance for the specified subscription, resource group, SapMonitor name, and resource name.</span></span>

## <span data-ttu-id="33c98-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="33c98-104">SYNTAX</span></span>

### <span data-ttu-id="33c98-105">Ta bort (standard)</span><span class="sxs-lookup"><span data-stu-id="33c98-105">Delete (Default)</span></span>
```
Remove-AzSapMonitorProviderInstance -Name <String> -ResourceGroupName <String> -SapMonitorName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="33c98-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="33c98-106">DeleteViaIdentity</span></span>
```
Remove-AzSapMonitorProviderInstance -InputObject <IHanaOnAzureIdentity> [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="33c98-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="33c98-107">DESCRIPTION</span></span>
<span data-ttu-id="33c98-108">Tar bort en tjänste instans för angiven prenumeration, resurs grupp, SapMonitor-namn och resurs namn.</span><span class="sxs-lookup"><span data-stu-id="33c98-108">Deletes a provider instance for the specified subscription, resource group, SapMonitor name, and resource name.</span></span>

## <span data-ttu-id="33c98-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="33c98-109">EXAMPLES</span></span>

### <span data-ttu-id="33c98-110">Exempel 1: ta bort en instans av SAP Monitor utifrån namn</span><span class="sxs-lookup"><span data-stu-id="33c98-110">Example 1: Remove instance of SAP monitor by name</span></span>
```powershell
PS C:\> Remove-AzSapMonitorProviderInstance -ResourceGroupName nancyc-hn1 -SapMonitorName ps-spamonitor-t01 -Name ps-sapmonitorins-t02

```

<span data-ttu-id="33c98-111">Det här kommandot tar bort en instans av SAP monitor med namn.</span><span class="sxs-lookup"><span data-stu-id="33c98-111">This command removes instance of SAP monitor by name.</span></span>

### <span data-ttu-id="33c98-112">Exempel 2: ta bort instans av SAP Monitor by-objekt</span><span class="sxs-lookup"><span data-stu-id="33c98-112">Example 2: Remove instance of SAP monitor by object</span></span>
```powershell
PS C:\> $sapIns = Get-AzSapMonitorProviderInstance -ResourceGroupName nancyc-hn1 -SapMonitorName ps-spamonitor-t01 -Name ps-sapmonitorins-t01
PS C:\> Remove-AzSapMonitorProviderInstance -InputObject $sapIns

```

<span data-ttu-id="33c98-113">Det här kommandot tar bort en instans av SAP Monitor by objekt.</span><span class="sxs-lookup"><span data-stu-id="33c98-113">This command removes instance of SAP monitor by object.</span></span>

## <span data-ttu-id="33c98-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="33c98-114">PARAMETERS</span></span>

### <span data-ttu-id="33c98-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="33c98-115">-AsJob</span></span>
<span data-ttu-id="33c98-116">Köra kommandot som ett jobb</span><span class="sxs-lookup"><span data-stu-id="33c98-116">Run the command as a job</span></span>

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

### <span data-ttu-id="33c98-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="33c98-117">-DefaultProfile</span></span>
<span data-ttu-id="33c98-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="33c98-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="33c98-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="33c98-119">-InputObject</span></span>
<span data-ttu-id="33c98-120">Identitets parameter för att konstruera, se avsnittet anteckningar för INPUTOBJECT-egenskaper och skapa en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="33c98-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="33c98-121">-Namn</span><span class="sxs-lookup"><span data-stu-id="33c98-121">-Name</span></span>
<span data-ttu-id="33c98-122">Namn på leverantörs instansen.</span><span class="sxs-lookup"><span data-stu-id="33c98-122">Name of the provider instance.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases: ProviderInstanceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="33c98-123">-Nowait</span><span class="sxs-lookup"><span data-stu-id="33c98-123">-NoWait</span></span>
<span data-ttu-id="33c98-124">Kör kommandot asynkront</span><span class="sxs-lookup"><span data-stu-id="33c98-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="33c98-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="33c98-125">-PassThru</span></span>
<span data-ttu-id="33c98-126">Returnerar true när kommandot lyckas</span><span class="sxs-lookup"><span data-stu-id="33c98-126">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="33c98-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="33c98-127">-ResourceGroupName</span></span>
<span data-ttu-id="33c98-128">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="33c98-128">Name of the resource group.</span></span>

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

### <span data-ttu-id="33c98-129">-SapMonitorName</span><span class="sxs-lookup"><span data-stu-id="33c98-129">-SapMonitorName</span></span>
<span data-ttu-id="33c98-130">Namnet på SAP Monitor-resursen.</span><span class="sxs-lookup"><span data-stu-id="33c98-130">Name of the SAP monitor resource.</span></span>

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

### <span data-ttu-id="33c98-131">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="33c98-131">-SubscriptionId</span></span>
<span data-ttu-id="33c98-132">Abonnemangs-ID som unikt identifierar Microsoft Azure-prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="33c98-132">Subscription ID which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="33c98-133">Prenumerations-ID: t utgör en del av URI: n för varje service samtal.</span><span class="sxs-lookup"><span data-stu-id="33c98-133">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="33c98-134">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="33c98-134">-Confirm</span></span>
<span data-ttu-id="33c98-135">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="33c98-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="33c98-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="33c98-136">-WhatIf</span></span>
<span data-ttu-id="33c98-137">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="33c98-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="33c98-138">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="33c98-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="33c98-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="33c98-139">CommonParameters</span></span>
<span data-ttu-id="33c98-140">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="33c98-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="33c98-141">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="33c98-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="33c98-142">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="33c98-142">INPUTS</span></span>

### <span data-ttu-id="33c98-143">Microsoft. Azure. PowerShell. cmdletar. HanaOnAzure. Models. IHanaOnAzureIdentity</span><span class="sxs-lookup"><span data-stu-id="33c98-143">Microsoft.Azure.PowerShell.Cmdlets.HanaOnAzure.Models.IHanaOnAzureIdentity</span></span>

## <span data-ttu-id="33c98-144">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="33c98-144">OUTPUTS</span></span>

### <span data-ttu-id="33c98-145">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="33c98-145">System.Boolean</span></span>

## <span data-ttu-id="33c98-146">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="33c98-146">NOTES</span></span>

<span data-ttu-id="33c98-147">ALIAS</span><span class="sxs-lookup"><span data-stu-id="33c98-147">ALIASES</span></span>

<span data-ttu-id="33c98-148">KOMPLEXA PARAMETER EGENSKAPER</span><span class="sxs-lookup"><span data-stu-id="33c98-148">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="33c98-149">Skapa en hash-tabell som innehåller lämpliga egenskaper för att lägga till de parametrar som beskrivs nedan.</span><span class="sxs-lookup"><span data-stu-id="33c98-149">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="33c98-150">Om du vill ha information om hash-tabeller kör Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="33c98-150">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="33c98-151">INPUTOBJECT <IHanaOnAzureIdentity> : identitets parameter</span><span class="sxs-lookup"><span data-stu-id="33c98-151">INPUTOBJECT <IHanaOnAzureIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="33c98-152">`[Id <String>]`: Sökväg till resurs identitet</span><span class="sxs-lookup"><span data-stu-id="33c98-152">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="33c98-153">`[Location <String>]`: Platsen för det borttagna valvet.</span><span class="sxs-lookup"><span data-stu-id="33c98-153">`[Location <String>]`: The location of the deleted vault.</span></span>
  - <span data-ttu-id="33c98-154">`[OperationKind <AccessPolicyUpdateKind?>]`: Åtgärdens namn</span><span class="sxs-lookup"><span data-stu-id="33c98-154">`[OperationKind <AccessPolicyUpdateKind?>]`: Name of the operation</span></span>
  - <span data-ttu-id="33c98-155">`[ProviderInstanceName <String>]`: Namnet på leverantörs instansen.</span><span class="sxs-lookup"><span data-stu-id="33c98-155">`[ProviderInstanceName <String>]`: Name of the provider instance.</span></span>
  - <span data-ttu-id="33c98-156">`[ResourceGroupName <String>]`: Resurs gruppens namn.</span><span class="sxs-lookup"><span data-stu-id="33c98-156">`[ResourceGroupName <String>]`: Name of the resource group.</span></span>
  - <span data-ttu-id="33c98-157">`[ResourceName <String>]`: Namnet på identitets resursen.</span><span class="sxs-lookup"><span data-stu-id="33c98-157">`[ResourceName <String>]`: The name of the identity resource.</span></span>
  - <span data-ttu-id="33c98-158">`[SapMonitorName <String>]`: Namnet på SAP Monitor-resursen.</span><span class="sxs-lookup"><span data-stu-id="33c98-158">`[SapMonitorName <String>]`: Name of the SAP monitor resource.</span></span>
  - <span data-ttu-id="33c98-159">`[Scope <String>]`: Resursens resurs leverantörs omfattning.</span><span class="sxs-lookup"><span data-stu-id="33c98-159">`[Scope <String>]`: The resource provider scope of the resource.</span></span> <span data-ttu-id="33c98-160">Överordnad resurs som utökas av hanterade identiteter.</span><span class="sxs-lookup"><span data-stu-id="33c98-160">Parent resource being extended by Managed Identities.</span></span>
  - <span data-ttu-id="33c98-161">`[SubscriptionId <String>]`: Prenumerations-ID som unikt identifierar Microsoft Azure-prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="33c98-161">`[SubscriptionId <String>]`: Subscription ID which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="33c98-162">Prenumerations-ID: t utgör en del av URI: n för varje service samtal.</span><span class="sxs-lookup"><span data-stu-id="33c98-162">The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="33c98-163">`[VaultName <String>]`: Namnet på valvet</span><span class="sxs-lookup"><span data-stu-id="33c98-163">`[VaultName <String>]`: Name of the vault</span></span>

## <span data-ttu-id="33c98-164">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="33c98-164">RELATED LINKS</span></span>

