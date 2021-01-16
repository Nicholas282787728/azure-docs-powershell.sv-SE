---
external help file: ''
Module Name: Az.MySql
online version: https://docs.microsoft.com/en-us/powershell/module/az.mysql/update-azmysqlflexibleserverfirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Update-AzMySqlFlexibleServerFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Update-AzMySqlFlexibleServerFirewallRule.md
ms.openlocfilehash: 5df722564e899d46a1f68bf8e88ecdaa2b792121
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98410891"
---
# <span data-ttu-id="7be07-101">Update-AzMySqlFlexibleServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="7be07-101">Update-AzMySqlFlexibleServerFirewallRule</span></span>

## <span data-ttu-id="7be07-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="7be07-102">SYNOPSIS</span></span>
<span data-ttu-id="7be07-103">Uppdaterar en befintlig brand Väggs regel.</span><span class="sxs-lookup"><span data-stu-id="7be07-103">Updates an existing firewall rule.</span></span>

## <span data-ttu-id="7be07-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="7be07-104">SYNTAX</span></span>

### <span data-ttu-id="7be07-105">UpdateExpanded (standard)</span><span class="sxs-lookup"><span data-stu-id="7be07-105">UpdateExpanded (Default)</span></span>
```
Update-AzMySqlFlexibleServerFirewallRule -Name <String> -ResourceGroupName <String> -ServerName <String>
 -EndIPAddress <String> -StartIPAddress <String> [-SubscriptionId <String>] [-DefaultProfile <PSObject>]
 [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="7be07-106">ClientIPAddress</span><span class="sxs-lookup"><span data-stu-id="7be07-106">ClientIPAddress</span></span>
```
Update-AzMySqlFlexibleServerFirewallRule -Name <String> -ResourceGroupName <String> -ServerName <String>
 -ClientIPAddress <String> [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="7be07-107">ClientIPAddressViaIdentity</span><span class="sxs-lookup"><span data-stu-id="7be07-107">ClientIPAddressViaIdentity</span></span>
```
Update-AzMySqlFlexibleServerFirewallRule -InputObject <IMySqlIdentity> -ClientIPAddress <String>
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="7be07-108">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="7be07-108">UpdateViaIdentityExpanded</span></span>
```
Update-AzMySqlFlexibleServerFirewallRule -InputObject <IMySqlIdentity> -EndIPAddress <String>
 -StartIPAddress <String> [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="7be07-109">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="7be07-109">DESCRIPTION</span></span>
<span data-ttu-id="7be07-110">Uppdaterar en befintlig brand Väggs regel.</span><span class="sxs-lookup"><span data-stu-id="7be07-110">Updates an existing firewall rule.</span></span>

## <span data-ttu-id="7be07-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="7be07-111">EXAMPLES</span></span>

### <span data-ttu-id="7be07-112">Exempel 1: uppdatera MySql-brandväggsregel efter namn</span><span class="sxs-lookup"><span data-stu-id="7be07-112">Example 1: Update MySql Firewall Rule by name</span></span>
```powershell
PS C:\> Update-AzMySqlFlexibleServerFirewallRule -Name rule -ResourceGroupName PowershellMySqlTest -ServerName mysql-test -EndIPAddress 0.0.0.3 -StartIPAddress 0.0.0.2

Name StartIPAddress EndIPAddress
---- -------------- ------------
rule 0.0.0.2        0.0.0.3
```

<span data-ttu-id="7be07-113">Denna cmdlet uppdaterar MySql Firewall-regel efter namn.</span><span class="sxs-lookup"><span data-stu-id="7be07-113">This cmdlet updates MySql Firewall Rule by name.</span></span>

### <span data-ttu-id="7be07-114">Exempel 2: uppdatera MySql Firewall-regel efter identitet.</span><span class="sxs-lookup"><span data-stu-id="7be07-114">Example 2: Update MySql Firewall Rule by identity.</span></span>
```powershell
PS C:\> $ID = "/subscriptions/<SubscriptionId>/resourceGroups/PowershellMySqlTest/providers/Microsoft.DBForMySql/flexibleServers/mysql-test/firewallRules/rule"
PS C:\> Update-AzMySqlFlexibleServerFirewallRule -InputObject $ID -EndIPAddress 0.0.0.3 -StartIPAddress 0.0.0.2

Name StartIPAddress EndIPAddress
---- -------------- ------------
rule 0.0.0.2        0.0.0.3
```

<span data-ttu-id="7be07-115">Dessa cmdletar uppdaterar MySql Firewall-regel efter identitet.</span><span class="sxs-lookup"><span data-stu-id="7be07-115">These cmdlets update MySql Firewall Rule by identity.</span></span>

## <span data-ttu-id="7be07-116">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="7be07-116">PARAMETERS</span></span>

### <span data-ttu-id="7be07-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="7be07-117">-AsJob</span></span>
<span data-ttu-id="7be07-118">Köra kommandot som ett jobb</span><span class="sxs-lookup"><span data-stu-id="7be07-118">Run the command as a job</span></span>

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

### <span data-ttu-id="7be07-119">-ClientIPAddress</span><span class="sxs-lookup"><span data-stu-id="7be07-119">-ClientIPAddress</span></span>
<span data-ttu-id="7be07-120">Klienten angav en IP-adress för Server brand Väggs regeln.</span><span class="sxs-lookup"><span data-stu-id="7be07-120">Client specified single IP of the server firewall rule.</span></span>
<span data-ttu-id="7be07-121">Måste vara IPv4-format.</span><span class="sxs-lookup"><span data-stu-id="7be07-121">Must be IPv4 format.</span></span>

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

### <span data-ttu-id="7be07-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7be07-122">-DefaultProfile</span></span>
<span data-ttu-id="7be07-123">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="7be07-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7be07-124">-EndIPAddress</span><span class="sxs-lookup"><span data-stu-id="7be07-124">-EndIPAddress</span></span>
<span data-ttu-id="7be07-125">Sista IP-adressen för Server brand Väggs regeln.</span><span class="sxs-lookup"><span data-stu-id="7be07-125">The end IP address of the server firewall rule.</span></span>
<span data-ttu-id="7be07-126">Måste vara IPv4-format.</span><span class="sxs-lookup"><span data-stu-id="7be07-126">Must be IPv4 format.</span></span>

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

### <span data-ttu-id="7be07-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7be07-127">-InputObject</span></span>
<span data-ttu-id="7be07-128">Identitets parameter för att konstruera, se avsnittet anteckningar för INPUTOBJECT-egenskaper och skapa en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="7be07-128">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity
Parameter Sets: ClientIPAddressViaIdentity, UpdateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7be07-129">-Namn</span><span class="sxs-lookup"><span data-stu-id="7be07-129">-Name</span></span>
<span data-ttu-id="7be07-130">Namnet på Server brand Väggs regeln.</span><span class="sxs-lookup"><span data-stu-id="7be07-130">The name of the server firewall rule.</span></span>

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

### <span data-ttu-id="7be07-131">-Nowait</span><span class="sxs-lookup"><span data-stu-id="7be07-131">-NoWait</span></span>
<span data-ttu-id="7be07-132">Kör kommandot asynkront</span><span class="sxs-lookup"><span data-stu-id="7be07-132">Run the command asynchronously</span></span>

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

### <span data-ttu-id="7be07-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7be07-133">-ResourceGroupName</span></span>
<span data-ttu-id="7be07-134">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="7be07-134">The name of the resource group.</span></span>
<span data-ttu-id="7be07-135">Namnet är Skift läges okänsligt.</span><span class="sxs-lookup"><span data-stu-id="7be07-135">The name is case insensitive.</span></span>

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

### <span data-ttu-id="7be07-136">-ServerName</span><span class="sxs-lookup"><span data-stu-id="7be07-136">-ServerName</span></span>
<span data-ttu-id="7be07-137">Namnet på servern.</span><span class="sxs-lookup"><span data-stu-id="7be07-137">The name of the server.</span></span>

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

### <span data-ttu-id="7be07-138">-StartIPAddress</span><span class="sxs-lookup"><span data-stu-id="7be07-138">-StartIPAddress</span></span>
<span data-ttu-id="7be07-139">Den första IP-adressen för Server brand Väggs regeln.</span><span class="sxs-lookup"><span data-stu-id="7be07-139">The start IP address of the server firewall rule.</span></span>
<span data-ttu-id="7be07-140">Måste vara IPv4-format.</span><span class="sxs-lookup"><span data-stu-id="7be07-140">Must be IPv4 format.</span></span>

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

### <span data-ttu-id="7be07-141">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="7be07-141">-SubscriptionId</span></span>
<span data-ttu-id="7be07-142">ID för mål prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="7be07-142">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="7be07-143">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="7be07-143">-Confirm</span></span>
<span data-ttu-id="7be07-144">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="7be07-144">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7be07-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7be07-145">-WhatIf</span></span>
<span data-ttu-id="7be07-146">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="7be07-146">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7be07-147">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="7be07-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7be07-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7be07-148">CommonParameters</span></span>
<span data-ttu-id="7be07-149">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7be07-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7be07-150">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="7be07-150">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7be07-151">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="7be07-151">INPUTS</span></span>

### <span data-ttu-id="7be07-152">Microsoft. Azure. PowerShell. cmdletar. MySql. Models. IMySqlIdentity</span><span class="sxs-lookup"><span data-stu-id="7be07-152">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity</span></span>

## <span data-ttu-id="7be07-153">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="7be07-153">OUTPUTS</span></span>

### <span data-ttu-id="7be07-154">Microsoft. Azure. PowerShell. cmdletar. MySql. Models. Api20171201. IFirewallRule</span><span class="sxs-lookup"><span data-stu-id="7be07-154">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20171201.IFirewallRule</span></span>

## <span data-ttu-id="7be07-155">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="7be07-155">NOTES</span></span>

<span data-ttu-id="7be07-156">ALIAS</span><span class="sxs-lookup"><span data-stu-id="7be07-156">ALIASES</span></span>

<span data-ttu-id="7be07-157">KOMPLEXA PARAMETER EGENSKAPER</span><span class="sxs-lookup"><span data-stu-id="7be07-157">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="7be07-158">Skapa en hash-tabell som innehåller lämpliga egenskaper för att lägga till de parametrar som beskrivs nedan.</span><span class="sxs-lookup"><span data-stu-id="7be07-158">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="7be07-159">Om du vill ha information om hash-tabeller kör Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="7be07-159">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="7be07-160">INPUTOBJECT <IMySqlIdentity> : identitets parameter</span><span class="sxs-lookup"><span data-stu-id="7be07-160">INPUTOBJECT <IMySqlIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="7be07-161">`[ConfigurationName <String>]`: Server konfigurationens namn.</span><span class="sxs-lookup"><span data-stu-id="7be07-161">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="7be07-162">`[DatabaseName <String>]`: Namnet på databasen.</span><span class="sxs-lookup"><span data-stu-id="7be07-162">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="7be07-163">`[FirewallRuleName <String>]`: Namnet på Server brand Väggs regeln.</span><span class="sxs-lookup"><span data-stu-id="7be07-163">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="7be07-164">`[Id <String>]`: Sökväg till resurs identitet</span><span class="sxs-lookup"><span data-stu-id="7be07-164">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="7be07-165">`[KeyName <String>]`: Server namnet.</span><span class="sxs-lookup"><span data-stu-id="7be07-165">`[KeyName <String>]`: The name of the server key.</span></span>
  - <span data-ttu-id="7be07-166">`[LocationName <String>]`: Namnet på platsen.</span><span class="sxs-lookup"><span data-stu-id="7be07-166">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="7be07-167">`[ResourceGroupName <String>]`: Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="7be07-167">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="7be07-168">Namnet är Skift läges okänsligt.</span><span class="sxs-lookup"><span data-stu-id="7be07-168">The name is case insensitive.</span></span>
  - <span data-ttu-id="7be07-169">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: Namnet på säkerhets varnings principen.</span><span class="sxs-lookup"><span data-stu-id="7be07-169">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="7be07-170">`[ServerName <String>]`: Namnet på servern.</span><span class="sxs-lookup"><span data-stu-id="7be07-170">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="7be07-171">`[SubscriptionId <String>]`: Mål prenumerationens ID.</span><span class="sxs-lookup"><span data-stu-id="7be07-171">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="7be07-172">`[VirtualNetworkRuleName <String>]`: Namnet på den virtuella nätverks regeln.</span><span class="sxs-lookup"><span data-stu-id="7be07-172">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="7be07-173">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="7be07-173">RELATED LINKS</span></span>

