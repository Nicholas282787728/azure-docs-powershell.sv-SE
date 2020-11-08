---
external help file: ''
Module Name: Az.MariaDb
online version: https://docs.microsoft.com/en-us/powershell/module/az.mariadb/update-azmariadbfirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/Update-AzMariaDbFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/Update-AzMariaDbFirewallRule.md
ms.openlocfilehash: 7d474000ed8c449c95ae7319a960c5f748d80e66
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94273321"
---
# <span data-ttu-id="599ce-101">Update-AzMariaDbFirewallRule</span><span class="sxs-lookup"><span data-stu-id="599ce-101">Update-AzMariaDbFirewallRule</span></span>

## <span data-ttu-id="599ce-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="599ce-102">SYNOPSIS</span></span>
<span data-ttu-id="599ce-103">Skapar en ny brand Väggs regel eller uppdaterar en befintlig brand Väggs regel.</span><span class="sxs-lookup"><span data-stu-id="599ce-103">Creates a new firewall rule or updates an existing firewall rule.</span></span>

## <span data-ttu-id="599ce-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="599ce-104">SYNTAX</span></span>

### <span data-ttu-id="599ce-105">UpdateExpanded (standard)</span><span class="sxs-lookup"><span data-stu-id="599ce-105">UpdateExpanded (Default)</span></span>
```
Update-AzMariaDbFirewallRule -Name <String> -ResourceGroupName <String> -ServerName <String>
 -EndIPAddress <String> -StartIPAddress <String> [-SubscriptionId <String>] [-DefaultProfile <PSObject>]
 [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="599ce-106">ClientIPAddress</span><span class="sxs-lookup"><span data-stu-id="599ce-106">ClientIPAddress</span></span>
```
Update-AzMariaDbFirewallRule -Name <String> -ResourceGroupName <String> -ServerName <String>
 -ClientIPAddress <String> [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="599ce-107">ClientIPAddressViaIdentity</span><span class="sxs-lookup"><span data-stu-id="599ce-107">ClientIPAddressViaIdentity</span></span>
```
Update-AzMariaDbFirewallRule -InputObject <IMariaDbIdentity> -ClientIPAddress <String>
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="599ce-108">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="599ce-108">UpdateViaIdentityExpanded</span></span>
```
Update-AzMariaDbFirewallRule -InputObject <IMariaDbIdentity> -EndIPAddress <String> -StartIPAddress <String>
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="599ce-109">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="599ce-109">DESCRIPTION</span></span>
<span data-ttu-id="599ce-110">Skapar en ny brand Väggs regel eller uppdaterar en befintlig brand Väggs regel.</span><span class="sxs-lookup"><span data-stu-id="599ce-110">Creates a new firewall rule or updates an existing firewall rule.</span></span>

## <span data-ttu-id="599ce-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="599ce-111">EXAMPLES</span></span>

### <span data-ttu-id="599ce-112">Exempel 1: uppdatera MariaDB brand Väggs regel</span><span class="sxs-lookup"><span data-stu-id="599ce-112">Example 1: Update MariaDB firewall rule</span></span>
```powershell
PS C:\> Update-AzMariaDbFirewallRule -Name fr-cfgl3y -ServerName mariadb-test-4rmtig -ResourceGroupName mariadb-test-qu5ov0 -StartIPAddress 0.0.3.1 -EndIPAddress 0.0.3.255

Name      StartIPAddress EndIPAddress
----      -------------- ------------
fr-cfgl3y 0.0.3.1        0.0.3.255
```

<span data-ttu-id="599ce-113">Det här kommandot uppdaterar en MariaDB.</span><span class="sxs-lookup"><span data-stu-id="599ce-113">This command updates a MariaDB firewall rule.</span></span>

### <span data-ttu-id="599ce-114">Exempel 2: uppdatera MariaDB brand Väggs regel efter identitet.</span><span class="sxs-lookup"><span data-stu-id="599ce-114">Example 2: Update MariaDB Firewall Rule by identity.</span></span>
```powershell
PS C:\> $ID = "/subscriptions/<SubscriptionId>/resourceGroups/mariadb-test-qu5ov0/providers/Microsoft.DBforMariaDB/servers/mariadb-test-4rmtig/firewallRules/fr-cfgl3y"
PS C:\> Update-AzMariaDbFirewallRule -InputObject $ID -EndIPAddress 0.0.0.3 -StartIPAddress 0.0.0.2

Name      StartIPAddress EndIPAddress
----      -------------- ------------
fr-cfgl3y 0.0.0.2        0.0.0.3
```

<span data-ttu-id="599ce-115">Cmdleten uppdaterar MariaDB brand Väggs regel efter identitet.</span><span class="sxs-lookup"><span data-stu-id="599ce-115">The cmdlet updates MariaDB Firewall Rule by identity.</span></span>

### <span data-ttu-id="599ce-116">Exempel 3: uppdatera MariaDB brand Väggs regel by-ClientIPAddress.</span><span class="sxs-lookup"><span data-stu-id="599ce-116">Example 3: Update MariaDB Firewall Rule by -ClientIPAddress.</span></span>
```powershell
PS C:\> $ID = "/subscriptions/<SubscriptionId>/resourceGroups/mariadb-test-qu5ov0/providers/Microsoft.DBforMariaDB/servers/mariadb-test-4rmtig/firewallRules/fr-cfgl3y"
PS C:\> Update-AzMariaDbFirewallRule -InputObject $ID --ClientIPAddress 0.0.0.2

Name      StartIPAddress EndIPAddress
----      -------------- ------------
fr-cfgl3y 0.0.0.2        0.0.0.2
```

<span data-ttu-id="599ce-117">Cmdleten uppdaterar MariaDB med-ClientIPAddress.</span><span class="sxs-lookup"><span data-stu-id="599ce-117">The cmdlet updates MariaDB Firewall Rule by -ClientIPAddress.</span></span>

## <span data-ttu-id="599ce-118">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="599ce-118">PARAMETERS</span></span>

### <span data-ttu-id="599ce-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="599ce-119">-AsJob</span></span>
<span data-ttu-id="599ce-120">Köra kommandot som ett jobb</span><span class="sxs-lookup"><span data-stu-id="599ce-120">Run the command as a job</span></span>

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

### <span data-ttu-id="599ce-121">-ClientIPAddress</span><span class="sxs-lookup"><span data-stu-id="599ce-121">-ClientIPAddress</span></span>
<span data-ttu-id="599ce-122">Klienten angav en IP-adress för Server brand Väggs regeln.</span><span class="sxs-lookup"><span data-stu-id="599ce-122">Client specified single IP of the server firewall rule.</span></span>
<span data-ttu-id="599ce-123">Måste vara IPv4-format.</span><span class="sxs-lookup"><span data-stu-id="599ce-123">Must be IPv4 format.</span></span>

```yaml
Type: System.String
Parameter Sets: ClientIPAddress, ClientIPAddressViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="599ce-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="599ce-124">-DefaultProfile</span></span>
<span data-ttu-id="599ce-125">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="599ce-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="599ce-126">-EndIPAddress</span><span class="sxs-lookup"><span data-stu-id="599ce-126">-EndIPAddress</span></span>
<span data-ttu-id="599ce-127">Sista IP-adressen för Server brand Väggs regeln.</span><span class="sxs-lookup"><span data-stu-id="599ce-127">The end IP address of the server firewall rule.</span></span>
<span data-ttu-id="599ce-128">Måste vara IPv4-format.</span><span class="sxs-lookup"><span data-stu-id="599ce-128">Must be IPv4 format.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded, UpdateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="599ce-129">-InputObject</span><span class="sxs-lookup"><span data-stu-id="599ce-129">-InputObject</span></span>
<span data-ttu-id="599ce-130">Identitets parameter för att konstruera, se avsnittet anteckningar för INPUTOBJECT-egenskaper och skapa en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="599ce-130">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.IMariaDbIdentity
Parameter Sets: ClientIPAddressViaIdentity, UpdateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="599ce-131">-Namn</span><span class="sxs-lookup"><span data-stu-id="599ce-131">-Name</span></span>
<span data-ttu-id="599ce-132">Namnet på Server brand Väggs regeln.</span><span class="sxs-lookup"><span data-stu-id="599ce-132">The name of the server firewall rule.</span></span>

```yaml
Type: System.String
Parameter Sets: ClientIPAddress, UpdateExpanded
Aliases: FirewallRuleName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="599ce-133">-Nowait</span><span class="sxs-lookup"><span data-stu-id="599ce-133">-NoWait</span></span>
<span data-ttu-id="599ce-134">Kör kommandot asynkront</span><span class="sxs-lookup"><span data-stu-id="599ce-134">Run the command asynchronously</span></span>

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

### <span data-ttu-id="599ce-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="599ce-135">-ResourceGroupName</span></span>
<span data-ttu-id="599ce-136">Namnet på resurs gruppen som innehåller resursen.</span><span class="sxs-lookup"><span data-stu-id="599ce-136">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="599ce-137">Det här värdet kan hämtas från Azure Resource Manager API eller till portalen.</span><span class="sxs-lookup"><span data-stu-id="599ce-137">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

```yaml
Type: System.String
Parameter Sets: ClientIPAddress, UpdateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="599ce-138">-ServerName</span><span class="sxs-lookup"><span data-stu-id="599ce-138">-ServerName</span></span>
<span data-ttu-id="599ce-139">Namnet på servern.</span><span class="sxs-lookup"><span data-stu-id="599ce-139">The name of the server.</span></span>

```yaml
Type: System.String
Parameter Sets: ClientIPAddress, UpdateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="599ce-140">-StartIPAddress</span><span class="sxs-lookup"><span data-stu-id="599ce-140">-StartIPAddress</span></span>
<span data-ttu-id="599ce-141">Den första IP-adressen för Server brand Väggs regeln.</span><span class="sxs-lookup"><span data-stu-id="599ce-141">The start IP address of the server firewall rule.</span></span>
<span data-ttu-id="599ce-142">Måste vara IPv4-format.</span><span class="sxs-lookup"><span data-stu-id="599ce-142">Must be IPv4 format.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded, UpdateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="599ce-143">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="599ce-143">-SubscriptionId</span></span>
<span data-ttu-id="599ce-144">Det prenumerations-ID som identifierar en Azure-prenumeration.</span><span class="sxs-lookup"><span data-stu-id="599ce-144">The subscription ID that identifies an Azure subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: ClientIPAddress, UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="599ce-145">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="599ce-145">-Confirm</span></span>
<span data-ttu-id="599ce-146">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="599ce-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="599ce-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="599ce-147">-WhatIf</span></span>
<span data-ttu-id="599ce-148">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="599ce-148">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="599ce-149">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="599ce-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="599ce-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="599ce-150">CommonParameters</span></span>
<span data-ttu-id="599ce-151">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="599ce-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="599ce-152">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="599ce-152">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="599ce-153">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="599ce-153">INPUTS</span></span>

### <span data-ttu-id="599ce-154">Microsoft. Azure. PowerShell. cmdletar. MariaDb. Models. IMariaDbIdentity</span><span class="sxs-lookup"><span data-stu-id="599ce-154">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.IMariaDbIdentity</span></span>

## <span data-ttu-id="599ce-155">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="599ce-155">OUTPUTS</span></span>

### <span data-ttu-id="599ce-156">Microsoft. Azure. PowerShell. cmdletar. MariaDb. Models. Api20180601Preview. IFirewallRule</span><span class="sxs-lookup"><span data-stu-id="599ce-156">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.Api20180601Preview.IFirewallRule</span></span>

## <span data-ttu-id="599ce-157">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="599ce-157">NOTES</span></span>

<span data-ttu-id="599ce-158">ALIAS</span><span class="sxs-lookup"><span data-stu-id="599ce-158">ALIASES</span></span>

<span data-ttu-id="599ce-159">KOMPLEXA PARAMETER EGENSKAPER</span><span class="sxs-lookup"><span data-stu-id="599ce-159">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="599ce-160">Skapa en hash-tabell som innehåller lämpliga egenskaper för att lägga till de parametrar som beskrivs nedan.</span><span class="sxs-lookup"><span data-stu-id="599ce-160">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="599ce-161">Om du vill ha information om hash-tabeller kör Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="599ce-161">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="599ce-162">INPUTOBJECT <IMariaDbIdentity> : identitets parameter</span><span class="sxs-lookup"><span data-stu-id="599ce-162">INPUTOBJECT <IMariaDbIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="599ce-163">`[ConfigurationName <String>]`: Server konfigurationens namn.</span><span class="sxs-lookup"><span data-stu-id="599ce-163">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="599ce-164">`[DatabaseName <String>]`: Namnet på databasen.</span><span class="sxs-lookup"><span data-stu-id="599ce-164">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="599ce-165">`[FirewallRuleName <String>]`: Namnet på Server brand Väggs regeln.</span><span class="sxs-lookup"><span data-stu-id="599ce-165">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="599ce-166">`[Id <String>]`: Sökväg till resurs identitet</span><span class="sxs-lookup"><span data-stu-id="599ce-166">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="599ce-167">`[LocationName <String>]`: Namnet på platsen.</span><span class="sxs-lookup"><span data-stu-id="599ce-167">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="599ce-168">`[ResourceGroupName <String>]`: Namnet på resurs gruppen som innehåller resursen.</span><span class="sxs-lookup"><span data-stu-id="599ce-168">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="599ce-169">Det här värdet kan hämtas från Azure Resource Manager API eller till portalen.</span><span class="sxs-lookup"><span data-stu-id="599ce-169">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="599ce-170">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: Namnet på säkerhets varnings principen.</span><span class="sxs-lookup"><span data-stu-id="599ce-170">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="599ce-171">`[ServerName <String>]`: Namnet på servern.</span><span class="sxs-lookup"><span data-stu-id="599ce-171">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="599ce-172">`[SubscriptionId <String>]`: Det prenumerations-ID som identifierar en Azure-prenumeration.</span><span class="sxs-lookup"><span data-stu-id="599ce-172">`[SubscriptionId <String>]`: The subscription ID that identifies an Azure subscription.</span></span>
  - <span data-ttu-id="599ce-173">`[VirtualNetworkRuleName <String>]`: Namnet på den virtuella nätverks regeln.</span><span class="sxs-lookup"><span data-stu-id="599ce-173">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="599ce-174">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="599ce-174">RELATED LINKS</span></span>

