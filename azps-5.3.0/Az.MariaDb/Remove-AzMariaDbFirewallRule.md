---
external help file: ''
Module Name: Az.MariaDb
online version: https://docs.microsoft.com/en-us/powershell/module/az.mariadb/remove-azmariadbfirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/Remove-AzMariaDbFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/Remove-AzMariaDbFirewallRule.md
ms.openlocfilehash: 7775c4adeef0ce4b05efa2b54c6484408256f3eb
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98522569"
---
# <span data-ttu-id="1f4b1-101">Remove-AzMariaDbFirewallRule</span><span class="sxs-lookup"><span data-stu-id="1f4b1-101">Remove-AzMariaDbFirewallRule</span></span>

## <span data-ttu-id="1f4b1-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="1f4b1-102">SYNOPSIS</span></span>
<span data-ttu-id="1f4b1-103">Tar bort en regel för en server brand vägg.</span><span class="sxs-lookup"><span data-stu-id="1f4b1-103">Deletes a server firewall rule.</span></span>

## <span data-ttu-id="1f4b1-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="1f4b1-104">SYNTAX</span></span>

### <span data-ttu-id="1f4b1-105">Ta bort (standard)</span><span class="sxs-lookup"><span data-stu-id="1f4b1-105">Delete (Default)</span></span>
```
Remove-AzMariaDbFirewallRule -Name <String> -ResourceGroupName <String> -ServerName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="1f4b1-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="1f4b1-106">DeleteViaIdentity</span></span>
```
Remove-AzMariaDbFirewallRule -InputObject <IMariaDbIdentity> [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="1f4b1-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="1f4b1-107">DESCRIPTION</span></span>
<span data-ttu-id="1f4b1-108">Tar bort en regel för en server brand vägg.</span><span class="sxs-lookup"><span data-stu-id="1f4b1-108">Deletes a server firewall rule.</span></span>

## <span data-ttu-id="1f4b1-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="1f4b1-109">EXAMPLES</span></span>

### <span data-ttu-id="1f4b1-110">Exempel 1: ta bort en brand Väggs regel under en MariaDB</span><span class="sxs-lookup"><span data-stu-id="1f4b1-110">Example 1: Remove a firewall rule under a MariaDB</span></span>
```powershell
PS C:\> Remove-AzMariaDbFirewallRule -Name frname-001 -ResourceGroupName mariadb-test-qu5ov0 -ServerName mariadb-test-4rmtig

```

<span data-ttu-id="1f4b1-111">Det här kommandot tar bort en brand Väggs regel under en MariaDB.</span><span class="sxs-lookup"><span data-stu-id="1f4b1-111">This command removes a firewall rule under a MariaDB.</span></span>

## <span data-ttu-id="1f4b1-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="1f4b1-112">PARAMETERS</span></span>

### <span data-ttu-id="1f4b1-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="1f4b1-113">-AsJob</span></span>
<span data-ttu-id="1f4b1-114">Köra kommandot som ett jobb</span><span class="sxs-lookup"><span data-stu-id="1f4b1-114">Run the command as a job</span></span>

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

### <span data-ttu-id="1f4b1-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1f4b1-115">-DefaultProfile</span></span>
<span data-ttu-id="1f4b1-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="1f4b1-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1f4b1-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1f4b1-117">-InputObject</span></span>
<span data-ttu-id="1f4b1-118">Identitets parameter för att konstruera, se avsnittet anteckningar för INPUTOBJECT-egenskaper och skapa en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="1f4b1-118">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="1f4b1-119">-Namn</span><span class="sxs-lookup"><span data-stu-id="1f4b1-119">-Name</span></span>
<span data-ttu-id="1f4b1-120">Namnet på Server brand Väggs regeln.</span><span class="sxs-lookup"><span data-stu-id="1f4b1-120">The name of the server firewall rule.</span></span>

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

### <span data-ttu-id="1f4b1-121">-Nowait</span><span class="sxs-lookup"><span data-stu-id="1f4b1-121">-NoWait</span></span>
<span data-ttu-id="1f4b1-122">Kör kommandot asynkront</span><span class="sxs-lookup"><span data-stu-id="1f4b1-122">Run the command asynchronously</span></span>

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

### <span data-ttu-id="1f4b1-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="1f4b1-123">-PassThru</span></span>
<span data-ttu-id="1f4b1-124">Returnerar true när kommandot lyckas</span><span class="sxs-lookup"><span data-stu-id="1f4b1-124">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="1f4b1-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1f4b1-125">-ResourceGroupName</span></span>
<span data-ttu-id="1f4b1-126">Namnet på resurs gruppen som innehåller resursen.</span><span class="sxs-lookup"><span data-stu-id="1f4b1-126">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="1f4b1-127">Det här värdet kan hämtas från Azure Resource Manager API eller till portalen.</span><span class="sxs-lookup"><span data-stu-id="1f4b1-127">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="1f4b1-128">-ServerName</span><span class="sxs-lookup"><span data-stu-id="1f4b1-128">-ServerName</span></span>
<span data-ttu-id="1f4b1-129">Namnet på servern.</span><span class="sxs-lookup"><span data-stu-id="1f4b1-129">The name of the server.</span></span>

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

### <span data-ttu-id="1f4b1-130">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="1f4b1-130">-SubscriptionId</span></span>
<span data-ttu-id="1f4b1-131">Det prenumerations-ID som identifierar en Azure-prenumeration.</span><span class="sxs-lookup"><span data-stu-id="1f4b1-131">The subscription ID that identifies an Azure subscription.</span></span>

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

### <span data-ttu-id="1f4b1-132">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="1f4b1-132">-Confirm</span></span>
<span data-ttu-id="1f4b1-133">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="1f4b1-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1f4b1-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1f4b1-134">-WhatIf</span></span>
<span data-ttu-id="1f4b1-135">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="1f4b1-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1f4b1-136">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="1f4b1-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1f4b1-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1f4b1-137">CommonParameters</span></span>
<span data-ttu-id="1f4b1-138">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1f4b1-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1f4b1-139">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="1f4b1-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1f4b1-140">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="1f4b1-140">INPUTS</span></span>

### <span data-ttu-id="1f4b1-141">Microsoft. Azure. PowerShell. cmdletar. MariaDb. Models. IMariaDbIdentity</span><span class="sxs-lookup"><span data-stu-id="1f4b1-141">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.IMariaDbIdentity</span></span>

## <span data-ttu-id="1f4b1-142">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="1f4b1-142">OUTPUTS</span></span>

### <span data-ttu-id="1f4b1-143">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="1f4b1-143">System.Boolean</span></span>

## <span data-ttu-id="1f4b1-144">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="1f4b1-144">NOTES</span></span>

<span data-ttu-id="1f4b1-145">ALIAS</span><span class="sxs-lookup"><span data-stu-id="1f4b1-145">ALIASES</span></span>

<span data-ttu-id="1f4b1-146">KOMPLEXA PARAMETER EGENSKAPER</span><span class="sxs-lookup"><span data-stu-id="1f4b1-146">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="1f4b1-147">Skapa en hash-tabell som innehåller lämpliga egenskaper för att lägga till de parametrar som beskrivs nedan.</span><span class="sxs-lookup"><span data-stu-id="1f4b1-147">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="1f4b1-148">Om du vill ha information om hash-tabeller kör Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="1f4b1-148">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="1f4b1-149">INPUTOBJECT <IMariaDbIdentity> : identitets parameter</span><span class="sxs-lookup"><span data-stu-id="1f4b1-149">INPUTOBJECT <IMariaDbIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="1f4b1-150">`[ConfigurationName <String>]`: Server konfigurationens namn.</span><span class="sxs-lookup"><span data-stu-id="1f4b1-150">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="1f4b1-151">`[DatabaseName <String>]`: Namnet på databasen.</span><span class="sxs-lookup"><span data-stu-id="1f4b1-151">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="1f4b1-152">`[FirewallRuleName <String>]`: Namnet på Server brand Väggs regeln.</span><span class="sxs-lookup"><span data-stu-id="1f4b1-152">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="1f4b1-153">`[Id <String>]`: Sökväg till resurs identitet</span><span class="sxs-lookup"><span data-stu-id="1f4b1-153">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="1f4b1-154">`[LocationName <String>]`: Namnet på platsen.</span><span class="sxs-lookup"><span data-stu-id="1f4b1-154">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="1f4b1-155">`[ResourceGroupName <String>]`: Namnet på resurs gruppen som innehåller resursen.</span><span class="sxs-lookup"><span data-stu-id="1f4b1-155">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="1f4b1-156">Det här värdet kan hämtas från Azure Resource Manager API eller till portalen.</span><span class="sxs-lookup"><span data-stu-id="1f4b1-156">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="1f4b1-157">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: Namnet på säkerhets varnings principen.</span><span class="sxs-lookup"><span data-stu-id="1f4b1-157">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="1f4b1-158">`[ServerName <String>]`: Namnet på servern.</span><span class="sxs-lookup"><span data-stu-id="1f4b1-158">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="1f4b1-159">`[SubscriptionId <String>]`: Det prenumerations-ID som identifierar en Azure-prenumeration.</span><span class="sxs-lookup"><span data-stu-id="1f4b1-159">`[SubscriptionId <String>]`: The subscription ID that identifies an Azure subscription.</span></span>
  - <span data-ttu-id="1f4b1-160">`[VirtualNetworkRuleName <String>]`: Namnet på den virtuella nätverks regeln.</span><span class="sxs-lookup"><span data-stu-id="1f4b1-160">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="1f4b1-161">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="1f4b1-161">RELATED LINKS</span></span>

