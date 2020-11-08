---
external help file: ''
Module Name: Az.PostgreSql
online version: https://docs.microsoft.com/en-us/powershell/module/az.postgresql/update-azpostgresqlfirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Update-AzPostgreSqlFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Update-AzPostgreSqlFirewallRule.md
ms.openlocfilehash: 43cf2d06c45d545b1d311cea474a8ec69fd49021
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94258064"
---
# <span data-ttu-id="70b2b-101">Update-AzPostgreSqlFirewallRule</span><span class="sxs-lookup"><span data-stu-id="70b2b-101">Update-AzPostgreSqlFirewallRule</span></span>

## <span data-ttu-id="70b2b-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="70b2b-102">SYNOPSIS</span></span>
<span data-ttu-id="70b2b-103">Skapar en ny brand Väggs regel eller uppdaterar en befintlig brand Väggs regel.</span><span class="sxs-lookup"><span data-stu-id="70b2b-103">Creates a new firewall rule or updates an existing firewall rule.</span></span>

## <span data-ttu-id="70b2b-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="70b2b-104">SYNTAX</span></span>

### <span data-ttu-id="70b2b-105">UpdateExpanded (standard)</span><span class="sxs-lookup"><span data-stu-id="70b2b-105">UpdateExpanded (Default)</span></span>
```
Update-AzPostgreSqlFirewallRule -Name <String> -ResourceGroupName <String> -ServerName <String>
 -EndIPAddress <String> -StartIPAddress <String> [-SubscriptionId <String>] [-DefaultProfile <PSObject>]
 [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="70b2b-106">ClientIPAddress</span><span class="sxs-lookup"><span data-stu-id="70b2b-106">ClientIPAddress</span></span>
```
Update-AzPostgreSqlFirewallRule -Name <String> -ResourceGroupName <String> -ServerName <String>
 -ClientIPAddress <String> [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="70b2b-107">ClientIPAddressViaIdentity</span><span class="sxs-lookup"><span data-stu-id="70b2b-107">ClientIPAddressViaIdentity</span></span>
```
Update-AzPostgreSqlFirewallRule -InputObject <IPostgreSqlIdentity> -ClientIPAddress <String>
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="70b2b-108">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="70b2b-108">UpdateViaIdentityExpanded</span></span>
```
Update-AzPostgreSqlFirewallRule -InputObject <IPostgreSqlIdentity> -EndIPAddress <String>
 -StartIPAddress <String> [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="70b2b-109">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="70b2b-109">DESCRIPTION</span></span>
<span data-ttu-id="70b2b-110">Skapar en ny brand Väggs regel eller uppdaterar en befintlig brand Väggs regel.</span><span class="sxs-lookup"><span data-stu-id="70b2b-110">Creates a new firewall rule or updates an existing firewall rule.</span></span>

## <span data-ttu-id="70b2b-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="70b2b-111">EXAMPLES</span></span>

### <span data-ttu-id="70b2b-112">Exempel 1: uppdatera PostgreSql brand Väggs regel efter namn</span><span class="sxs-lookup"><span data-stu-id="70b2b-112">Example 1: Update PostgreSql Firewall Rule by name</span></span>
```powershell
PS C:\> Update-AzPostgreSqlFirewallRule -Name rule -ResourceGroupName PostgreSqlTestRG -ServerName PostgreSqlTestServer -EndIPAddress 0.0.0.3 -StartIPAddress 0.0.0.2

Name StartIPAddress EndIPAddress
---- -------------- ------------
rule 0.0.0.2        0.0.0.3
```

<span data-ttu-id="70b2b-113">Denna cmdlet uppdaterar PostgreSql efter namn.</span><span class="sxs-lookup"><span data-stu-id="70b2b-113">This cmdlet updates PostgreSql Firewall Rule by name.</span></span>

### <span data-ttu-id="70b2b-114">Exempel 2: uppdatera PostgreSql brand Väggs regel efter identitet.</span><span class="sxs-lookup"><span data-stu-id="70b2b-114">Example 2: Update PostgreSql Firewall Rule by identity.</span></span>
```powershell
PS C:\> $ID = "/subscriptions/<SubscriptionId>/resourceGroups/PostgreSqlTestRG/providers/Microsoft.DBforPostgreSQL/servers/PostgreSqlTestServer/firewallRules/rule"
PS C:\> Update-AzPostgreSqlFirewallRule -InputObject $ID -EndIPAddress 0.0.0.1 -StartIPAddress 0.0.0.0

Name StartIPAddress EndIPAddress
---- -------------- ------------
rule 0.0.0.0        0.0.0.1
```

<span data-ttu-id="70b2b-115">Dessa cmdletar uppdaterar PostgreSql brand Väggs regel efter identitet.</span><span class="sxs-lookup"><span data-stu-id="70b2b-115">These cmdlets update PostgreSql Firewall Rule by identity.</span></span>

### <span data-ttu-id="70b2b-116">Exempel 3: uppdatera PostgreSql brand Väggs regel by-ClientIPAddress.</span><span class="sxs-lookup"><span data-stu-id="70b2b-116">Example 3: Update PostgreSql Firewall Rule by -ClientIPAddress.</span></span>
```powershell
PS C:\> $ID = "/subscriptions/<SubscriptionId>/resourceGroups/PowershellPostgreSqlTest/providers/Microsoft.DBforPostgreSQL/servers/PostgreSqlTestServer/firewallRules/rule"
PS C:\> Update-AzPostgreSqlFirewallRule -InputObject $ID --ClientIPAddress 0.0.0.2

Name StartIPAddress EndIPAddress
---- -------------- ------------
rule 0.0.0.2        0.0.0.2
```

<span data-ttu-id="70b2b-117">Dessa cmdletar uppdaterar PostgreSql Firewall by-ClientIPAddress.</span><span class="sxs-lookup"><span data-stu-id="70b2b-117">These cmdlets update PostgreSql Firewall Rule by -ClientIPAddress.</span></span>

## <span data-ttu-id="70b2b-118">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="70b2b-118">PARAMETERS</span></span>

### <span data-ttu-id="70b2b-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="70b2b-119">-AsJob</span></span>
<span data-ttu-id="70b2b-120">Köra kommandot som ett jobb</span><span class="sxs-lookup"><span data-stu-id="70b2b-120">Run the command as a job</span></span>

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

### <span data-ttu-id="70b2b-121">-ClientIPAddress</span><span class="sxs-lookup"><span data-stu-id="70b2b-121">-ClientIPAddress</span></span>
<span data-ttu-id="70b2b-122">Klienten angav en IP-adress för Server brand Väggs regeln.</span><span class="sxs-lookup"><span data-stu-id="70b2b-122">Client specified single IP of the server firewall rule.</span></span>
<span data-ttu-id="70b2b-123">Måste vara IPv4-format.</span><span class="sxs-lookup"><span data-stu-id="70b2b-123">Must be IPv4 format.</span></span>

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

### <span data-ttu-id="70b2b-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="70b2b-124">-DefaultProfile</span></span>
<span data-ttu-id="70b2b-125">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="70b2b-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="70b2b-126">-EndIPAddress</span><span class="sxs-lookup"><span data-stu-id="70b2b-126">-EndIPAddress</span></span>
<span data-ttu-id="70b2b-127">Sista IP-adressen för Server brand Väggs regeln.</span><span class="sxs-lookup"><span data-stu-id="70b2b-127">The end IP address of the server firewall rule.</span></span>
<span data-ttu-id="70b2b-128">Måste vara IPv4-format.</span><span class="sxs-lookup"><span data-stu-id="70b2b-128">Must be IPv4 format.</span></span>

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

### <span data-ttu-id="70b2b-129">-InputObject</span><span class="sxs-lookup"><span data-stu-id="70b2b-129">-InputObject</span></span>
<span data-ttu-id="70b2b-130">Identitets parameter för att konstruera, se avsnittet anteckningar för INPUTOBJECT-egenskaper och skapa en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="70b2b-130">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.IPostgreSqlIdentity
Parameter Sets: ClientIPAddressViaIdentity, UpdateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="70b2b-131">-Namn</span><span class="sxs-lookup"><span data-stu-id="70b2b-131">-Name</span></span>
<span data-ttu-id="70b2b-132">Namnet på Server brand Väggs regeln.</span><span class="sxs-lookup"><span data-stu-id="70b2b-132">The name of the server firewall rule.</span></span>

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

### <span data-ttu-id="70b2b-133">-Nowait</span><span class="sxs-lookup"><span data-stu-id="70b2b-133">-NoWait</span></span>
<span data-ttu-id="70b2b-134">Kör kommandot asynkront</span><span class="sxs-lookup"><span data-stu-id="70b2b-134">Run the command asynchronously</span></span>

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

### <span data-ttu-id="70b2b-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="70b2b-135">-ResourceGroupName</span></span>
<span data-ttu-id="70b2b-136">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="70b2b-136">The name of the resource group.</span></span>
<span data-ttu-id="70b2b-137">Namnet är Skift läges okänsligt.</span><span class="sxs-lookup"><span data-stu-id="70b2b-137">The name is case insensitive.</span></span>

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

### <span data-ttu-id="70b2b-138">-ServerName</span><span class="sxs-lookup"><span data-stu-id="70b2b-138">-ServerName</span></span>
<span data-ttu-id="70b2b-139">Namnet på servern.</span><span class="sxs-lookup"><span data-stu-id="70b2b-139">The name of the server.</span></span>

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

### <span data-ttu-id="70b2b-140">-StartIPAddress</span><span class="sxs-lookup"><span data-stu-id="70b2b-140">-StartIPAddress</span></span>
<span data-ttu-id="70b2b-141">Den första IP-adressen för Server brand Väggs regeln.</span><span class="sxs-lookup"><span data-stu-id="70b2b-141">The start IP address of the server firewall rule.</span></span>
<span data-ttu-id="70b2b-142">Måste vara IPv4-format.</span><span class="sxs-lookup"><span data-stu-id="70b2b-142">Must be IPv4 format.</span></span>

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

### <span data-ttu-id="70b2b-143">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="70b2b-143">-SubscriptionId</span></span>
<span data-ttu-id="70b2b-144">ID för mål prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="70b2b-144">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="70b2b-145">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="70b2b-145">-Confirm</span></span>
<span data-ttu-id="70b2b-146">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="70b2b-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="70b2b-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="70b2b-147">-WhatIf</span></span>
<span data-ttu-id="70b2b-148">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="70b2b-148">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="70b2b-149">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="70b2b-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="70b2b-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="70b2b-150">CommonParameters</span></span>
<span data-ttu-id="70b2b-151">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="70b2b-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="70b2b-152">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="70b2b-152">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="70b2b-153">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="70b2b-153">INPUTS</span></span>

### <span data-ttu-id="70b2b-154">Microsoft. Azure. PowerShell. cmdletar. PostgreSql. Models. IPostgreSqlIdentity</span><span class="sxs-lookup"><span data-stu-id="70b2b-154">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.IPostgreSqlIdentity</span></span>

## <span data-ttu-id="70b2b-155">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="70b2b-155">OUTPUTS</span></span>

### <span data-ttu-id="70b2b-156">Microsoft. Azure. PowerShell. cmdletar. PostgreSql. Models. Api20171201. IFirewallRule</span><span class="sxs-lookup"><span data-stu-id="70b2b-156">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.Api20171201.IFirewallRule</span></span>

## <span data-ttu-id="70b2b-157">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="70b2b-157">NOTES</span></span>

<span data-ttu-id="70b2b-158">ALIAS</span><span class="sxs-lookup"><span data-stu-id="70b2b-158">ALIASES</span></span>

<span data-ttu-id="70b2b-159">KOMPLEXA PARAMETER EGENSKAPER</span><span class="sxs-lookup"><span data-stu-id="70b2b-159">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="70b2b-160">Skapa en hash-tabell som innehåller lämpliga egenskaper för att lägga till de parametrar som beskrivs nedan.</span><span class="sxs-lookup"><span data-stu-id="70b2b-160">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="70b2b-161">Om du vill ha information om hash-tabeller kör Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="70b2b-161">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="70b2b-162">INPUTOBJECT <IPostgreSqlIdentity> : identitets parameter</span><span class="sxs-lookup"><span data-stu-id="70b2b-162">INPUTOBJECT <IPostgreSqlIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="70b2b-163">`[ConfigurationName <String>]`: Server konfigurationens namn.</span><span class="sxs-lookup"><span data-stu-id="70b2b-163">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="70b2b-164">`[DatabaseName <String>]`: Namnet på databasen.</span><span class="sxs-lookup"><span data-stu-id="70b2b-164">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="70b2b-165">`[FirewallRuleName <String>]`: Namnet på Server brand Väggs regeln.</span><span class="sxs-lookup"><span data-stu-id="70b2b-165">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="70b2b-166">`[Id <String>]`: Sökväg till resurs identitet</span><span class="sxs-lookup"><span data-stu-id="70b2b-166">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="70b2b-167">`[LocationName <String>]`: Namnet på platsen.</span><span class="sxs-lookup"><span data-stu-id="70b2b-167">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="70b2b-168">`[ResourceGroupName <String>]`: Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="70b2b-168">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="70b2b-169">Namnet är Skift läges okänsligt.</span><span class="sxs-lookup"><span data-stu-id="70b2b-169">The name is case insensitive.</span></span>
  - <span data-ttu-id="70b2b-170">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: Namnet på säkerhets varnings principen.</span><span class="sxs-lookup"><span data-stu-id="70b2b-170">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="70b2b-171">`[ServerName <String>]`: Namnet på servern.</span><span class="sxs-lookup"><span data-stu-id="70b2b-171">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="70b2b-172">`[SubscriptionId <String>]`: Mål prenumerationens ID.</span><span class="sxs-lookup"><span data-stu-id="70b2b-172">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="70b2b-173">`[VirtualNetworkRuleName <String>]`: Namnet på den virtuella nätverks regeln.</span><span class="sxs-lookup"><span data-stu-id="70b2b-173">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="70b2b-174">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="70b2b-174">RELATED LINKS</span></span>

