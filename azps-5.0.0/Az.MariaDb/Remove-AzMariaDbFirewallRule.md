---
external help file: ''
Module Name: Az.MariaDb
online version: https://docs.microsoft.com/en-us/powershell/module/az.mariadb/remove-azmariadbfirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/Remove-AzMariaDbFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/Remove-AzMariaDbFirewallRule.md
ms.openlocfilehash: 7775c4adeef0ce4b05efa2b54c6484408256f3eb
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94271871"
---
# <span data-ttu-id="50eca-101">Remove-AzMariaDbFirewallRule</span><span class="sxs-lookup"><span data-stu-id="50eca-101">Remove-AzMariaDbFirewallRule</span></span>

## <span data-ttu-id="50eca-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="50eca-102">SYNOPSIS</span></span>
<span data-ttu-id="50eca-103">Tar bort en regel för en server brand vägg.</span><span class="sxs-lookup"><span data-stu-id="50eca-103">Deletes a server firewall rule.</span></span>

## <span data-ttu-id="50eca-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="50eca-104">SYNTAX</span></span>

### <span data-ttu-id="50eca-105">Ta bort (standard)</span><span class="sxs-lookup"><span data-stu-id="50eca-105">Delete (Default)</span></span>
```
Remove-AzMariaDbFirewallRule -Name <String> -ResourceGroupName <String> -ServerName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="50eca-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="50eca-106">DeleteViaIdentity</span></span>
```
Remove-AzMariaDbFirewallRule -InputObject <IMariaDbIdentity> [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="50eca-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="50eca-107">DESCRIPTION</span></span>
<span data-ttu-id="50eca-108">Tar bort en regel för en server brand vägg.</span><span class="sxs-lookup"><span data-stu-id="50eca-108">Deletes a server firewall rule.</span></span>

## <span data-ttu-id="50eca-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="50eca-109">EXAMPLES</span></span>

### <span data-ttu-id="50eca-110">Exempel 1: ta bort en brand Väggs regel under en MariaDB</span><span class="sxs-lookup"><span data-stu-id="50eca-110">Example 1: Remove a firewall rule under a MariaDB</span></span>
```powershell
PS C:\> Remove-AzMariaDbFirewallRule -Name frname-001 -ResourceGroupName mariadb-test-qu5ov0 -ServerName mariadb-test-4rmtig

```

<span data-ttu-id="50eca-111">Det här kommandot tar bort en brand Väggs regel under en MariaDB.</span><span class="sxs-lookup"><span data-stu-id="50eca-111">This command removes a firewall rule under a MariaDB.</span></span>

## <span data-ttu-id="50eca-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="50eca-112">PARAMETERS</span></span>

### <span data-ttu-id="50eca-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="50eca-113">-AsJob</span></span>
<span data-ttu-id="50eca-114">Köra kommandot som ett jobb</span><span class="sxs-lookup"><span data-stu-id="50eca-114">Run the command as a job</span></span>

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

### <span data-ttu-id="50eca-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="50eca-115">-DefaultProfile</span></span>
<span data-ttu-id="50eca-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="50eca-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="50eca-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="50eca-117">-InputObject</span></span>
<span data-ttu-id="50eca-118">Identitets parameter för att konstruera, se avsnittet anteckningar för INPUTOBJECT-egenskaper och skapa en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="50eca-118">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.IMariaDbIdentity
Parameter Sets: DeleteViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="50eca-119">-Namn</span><span class="sxs-lookup"><span data-stu-id="50eca-119">-Name</span></span>
<span data-ttu-id="50eca-120">Namnet på Server brand Väggs regeln.</span><span class="sxs-lookup"><span data-stu-id="50eca-120">The name of the server firewall rule.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases: FirewallRuleName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="50eca-121">-Nowait</span><span class="sxs-lookup"><span data-stu-id="50eca-121">-NoWait</span></span>
<span data-ttu-id="50eca-122">Kör kommandot asynkront</span><span class="sxs-lookup"><span data-stu-id="50eca-122">Run the command asynchronously</span></span>

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

### <span data-ttu-id="50eca-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="50eca-123">-PassThru</span></span>
<span data-ttu-id="50eca-124">Returnerar true när kommandot lyckas</span><span class="sxs-lookup"><span data-stu-id="50eca-124">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="50eca-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="50eca-125">-ResourceGroupName</span></span>
<span data-ttu-id="50eca-126">Namnet på resurs gruppen som innehåller resursen.</span><span class="sxs-lookup"><span data-stu-id="50eca-126">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="50eca-127">Det här värdet kan hämtas från Azure Resource Manager API eller till portalen.</span><span class="sxs-lookup"><span data-stu-id="50eca-127">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="50eca-128">-ServerName</span><span class="sxs-lookup"><span data-stu-id="50eca-128">-ServerName</span></span>
<span data-ttu-id="50eca-129">Namnet på servern.</span><span class="sxs-lookup"><span data-stu-id="50eca-129">The name of the server.</span></span>

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

### <span data-ttu-id="50eca-130">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="50eca-130">-SubscriptionId</span></span>
<span data-ttu-id="50eca-131">Det prenumerations-ID som identifierar en Azure-prenumeration.</span><span class="sxs-lookup"><span data-stu-id="50eca-131">The subscription ID that identifies an Azure subscription.</span></span>

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

### <span data-ttu-id="50eca-132">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="50eca-132">-Confirm</span></span>
<span data-ttu-id="50eca-133">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="50eca-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="50eca-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="50eca-134">-WhatIf</span></span>
<span data-ttu-id="50eca-135">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="50eca-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="50eca-136">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="50eca-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="50eca-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="50eca-137">CommonParameters</span></span>
<span data-ttu-id="50eca-138">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="50eca-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="50eca-139">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="50eca-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="50eca-140">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="50eca-140">INPUTS</span></span>

### <span data-ttu-id="50eca-141">Microsoft. Azure. PowerShell. cmdletar. MariaDb. Models. IMariaDbIdentity</span><span class="sxs-lookup"><span data-stu-id="50eca-141">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.IMariaDbIdentity</span></span>

## <span data-ttu-id="50eca-142">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="50eca-142">OUTPUTS</span></span>

### <span data-ttu-id="50eca-143">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="50eca-143">System.Boolean</span></span>

## <span data-ttu-id="50eca-144">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="50eca-144">NOTES</span></span>

<span data-ttu-id="50eca-145">ALIAS</span><span class="sxs-lookup"><span data-stu-id="50eca-145">ALIASES</span></span>

<span data-ttu-id="50eca-146">KOMPLEXA PARAMETER EGENSKAPER</span><span class="sxs-lookup"><span data-stu-id="50eca-146">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="50eca-147">Skapa en hash-tabell som innehåller lämpliga egenskaper för att lägga till de parametrar som beskrivs nedan.</span><span class="sxs-lookup"><span data-stu-id="50eca-147">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="50eca-148">Om du vill ha information om hash-tabeller kör Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="50eca-148">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="50eca-149">INPUTOBJECT <IMariaDbIdentity> : identitets parameter</span><span class="sxs-lookup"><span data-stu-id="50eca-149">INPUTOBJECT <IMariaDbIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="50eca-150">`[ConfigurationName <String>]`: Server konfigurationens namn.</span><span class="sxs-lookup"><span data-stu-id="50eca-150">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="50eca-151">`[DatabaseName <String>]`: Namnet på databasen.</span><span class="sxs-lookup"><span data-stu-id="50eca-151">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="50eca-152">`[FirewallRuleName <String>]`: Namnet på Server brand Väggs regeln.</span><span class="sxs-lookup"><span data-stu-id="50eca-152">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="50eca-153">`[Id <String>]`: Sökväg till resurs identitet</span><span class="sxs-lookup"><span data-stu-id="50eca-153">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="50eca-154">`[LocationName <String>]`: Namnet på platsen.</span><span class="sxs-lookup"><span data-stu-id="50eca-154">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="50eca-155">`[ResourceGroupName <String>]`: Namnet på resurs gruppen som innehåller resursen.</span><span class="sxs-lookup"><span data-stu-id="50eca-155">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="50eca-156">Det här värdet kan hämtas från Azure Resource Manager API eller till portalen.</span><span class="sxs-lookup"><span data-stu-id="50eca-156">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="50eca-157">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: Namnet på säkerhets varnings principen.</span><span class="sxs-lookup"><span data-stu-id="50eca-157">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="50eca-158">`[ServerName <String>]`: Namnet på servern.</span><span class="sxs-lookup"><span data-stu-id="50eca-158">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="50eca-159">`[SubscriptionId <String>]`: Det prenumerations-ID som identifierar en Azure-prenumeration.</span><span class="sxs-lookup"><span data-stu-id="50eca-159">`[SubscriptionId <String>]`: The subscription ID that identifies an Azure subscription.</span></span>
  - <span data-ttu-id="50eca-160">`[VirtualNetworkRuleName <String>]`: Namnet på den virtuella nätverks regeln.</span><span class="sxs-lookup"><span data-stu-id="50eca-160">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="50eca-161">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="50eca-161">RELATED LINKS</span></span>

