---
external help file: ''
Module Name: Az.MariaDb
online version: https://docs.microsoft.com/en-us/powershell/module/az.mariadb/update-azmariadbfirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/Update-AzMariaDbFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/Update-AzMariaDbFirewallRule.md
ms.openlocfilehash: 7d474000ed8c449c95ae7319a960c5f748d80e66
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94259353"
---
# <span data-ttu-id="6997a-101">Update-AzMariaDbFirewallRule</span><span class="sxs-lookup"><span data-stu-id="6997a-101">Update-AzMariaDbFirewallRule</span></span>

## <span data-ttu-id="6997a-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="6997a-102">SYNOPSIS</span></span>
<span data-ttu-id="6997a-103">Skapar en ny brand Väggs regel eller uppdaterar en befintlig brand Väggs regel.</span><span class="sxs-lookup"><span data-stu-id="6997a-103">Creates a new firewall rule or updates an existing firewall rule.</span></span>

## <span data-ttu-id="6997a-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="6997a-104">SYNTAX</span></span>

### <span data-ttu-id="6997a-105">UpdateExpanded (standard)</span><span class="sxs-lookup"><span data-stu-id="6997a-105">UpdateExpanded (Default)</span></span>
```
Update-AzMariaDbFirewallRule -Name <String> -ResourceGroupName <String> -ServerName <String>
 -EndIPAddress <String> -StartIPAddress <String> [-SubscriptionId <String>] [-DefaultProfile <PSObject>]
 [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="6997a-106">ClientIPAddress</span><span class="sxs-lookup"><span data-stu-id="6997a-106">ClientIPAddress</span></span>
```
Update-AzMariaDbFirewallRule -Name <String> -ResourceGroupName <String> -ServerName <String>
 -ClientIPAddress <String> [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="6997a-107">ClientIPAddressViaIdentity</span><span class="sxs-lookup"><span data-stu-id="6997a-107">ClientIPAddressViaIdentity</span></span>
```
Update-AzMariaDbFirewallRule -InputObject <IMariaDbIdentity> -ClientIPAddress <String>
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="6997a-108">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="6997a-108">UpdateViaIdentityExpanded</span></span>
```
Update-AzMariaDbFirewallRule -InputObject <IMariaDbIdentity> -EndIPAddress <String> -StartIPAddress <String>
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="6997a-109">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="6997a-109">DESCRIPTION</span></span>
<span data-ttu-id="6997a-110">Skapar en ny brand Väggs regel eller uppdaterar en befintlig brand Väggs regel.</span><span class="sxs-lookup"><span data-stu-id="6997a-110">Creates a new firewall rule or updates an existing firewall rule.</span></span>

## <span data-ttu-id="6997a-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="6997a-111">EXAMPLES</span></span>

### <span data-ttu-id="6997a-112">Exempel 1: uppdatera MariaDB brand Väggs regel</span><span class="sxs-lookup"><span data-stu-id="6997a-112">Example 1: Update MariaDB firewall rule</span></span>
```powershell
PS C:\> Update-AzMariaDbFirewallRule -Name fr-cfgl3y -ServerName mariadb-test-4rmtig -ResourceGroupName mariadb-test-qu5ov0 -StartIPAddress 0.0.3.1 -EndIPAddress 0.0.3.255

Name      StartIPAddress EndIPAddress
----      -------------- ------------
fr-cfgl3y 0.0.3.1        0.0.3.255
```

<span data-ttu-id="6997a-113">Det här kommandot uppdaterar en MariaDB.</span><span class="sxs-lookup"><span data-stu-id="6997a-113">This command updates a MariaDB firewall rule.</span></span>

### <span data-ttu-id="6997a-114">Exempel 2: uppdatera MariaDB brand Väggs regel efter identitet.</span><span class="sxs-lookup"><span data-stu-id="6997a-114">Example 2: Update MariaDB Firewall Rule by identity.</span></span>
```powershell
PS C:\> $ID = "/subscriptions/<SubscriptionId>/resourceGroups/mariadb-test-qu5ov0/providers/Microsoft.DBforMariaDB/servers/mariadb-test-4rmtig/firewallRules/fr-cfgl3y"
PS C:\> Update-AzMariaDbFirewallRule -InputObject $ID -EndIPAddress 0.0.0.3 -StartIPAddress 0.0.0.2

Name      StartIPAddress EndIPAddress
----      -------------- ------------
fr-cfgl3y 0.0.0.2        0.0.0.3
```

<span data-ttu-id="6997a-115">Cmdleten uppdaterar MariaDB brand Väggs regel efter identitet.</span><span class="sxs-lookup"><span data-stu-id="6997a-115">The cmdlet updates MariaDB Firewall Rule by identity.</span></span>

### <span data-ttu-id="6997a-116">Exempel 3: uppdatera MariaDB brand Väggs regel by-ClientIPAddress.</span><span class="sxs-lookup"><span data-stu-id="6997a-116">Example 3: Update MariaDB Firewall Rule by -ClientIPAddress.</span></span>
```powershell
PS C:\> $ID = "/subscriptions/<SubscriptionId>/resourceGroups/mariadb-test-qu5ov0/providers/Microsoft.DBforMariaDB/servers/mariadb-test-4rmtig/firewallRules/fr-cfgl3y"
PS C:\> Update-AzMariaDbFirewallRule -InputObject $ID --ClientIPAddress 0.0.0.2

Name      StartIPAddress EndIPAddress
----      -------------- ------------
fr-cfgl3y 0.0.0.2        0.0.0.2
```

<span data-ttu-id="6997a-117">Cmdleten uppdaterar MariaDB med-ClientIPAddress.</span><span class="sxs-lookup"><span data-stu-id="6997a-117">The cmdlet updates MariaDB Firewall Rule by -ClientIPAddress.</span></span>

## <span data-ttu-id="6997a-118">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="6997a-118">PARAMETERS</span></span>

### <span data-ttu-id="6997a-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="6997a-119">-AsJob</span></span>
<span data-ttu-id="6997a-120">Köra kommandot som ett jobb</span><span class="sxs-lookup"><span data-stu-id="6997a-120">Run the command as a job</span></span>

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

### <span data-ttu-id="6997a-121">-ClientIPAddress</span><span class="sxs-lookup"><span data-stu-id="6997a-121">-ClientIPAddress</span></span>
<span data-ttu-id="6997a-122">Klienten angav en IP-adress för Server brand Väggs regeln.</span><span class="sxs-lookup"><span data-stu-id="6997a-122">Client specified single IP of the server firewall rule.</span></span>
<span data-ttu-id="6997a-123">Måste vara IPv4-format.</span><span class="sxs-lookup"><span data-stu-id="6997a-123">Must be IPv4 format.</span></span>

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

### <span data-ttu-id="6997a-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6997a-124">-DefaultProfile</span></span>
<span data-ttu-id="6997a-125">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="6997a-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6997a-126">-EndIPAddress</span><span class="sxs-lookup"><span data-stu-id="6997a-126">-EndIPAddress</span></span>
<span data-ttu-id="6997a-127">Sista IP-adressen för Server brand Väggs regeln.</span><span class="sxs-lookup"><span data-stu-id="6997a-127">The end IP address of the server firewall rule.</span></span>
<span data-ttu-id="6997a-128">Måste vara IPv4-format.</span><span class="sxs-lookup"><span data-stu-id="6997a-128">Must be IPv4 format.</span></span>

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

### <span data-ttu-id="6997a-129">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6997a-129">-InputObject</span></span>
<span data-ttu-id="6997a-130">Identitets parameter för att konstruera, se avsnittet anteckningar för INPUTOBJECT-egenskaper och skapa en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="6997a-130">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="6997a-131">-Namn</span><span class="sxs-lookup"><span data-stu-id="6997a-131">-Name</span></span>
<span data-ttu-id="6997a-132">Namnet på Server brand Väggs regeln.</span><span class="sxs-lookup"><span data-stu-id="6997a-132">The name of the server firewall rule.</span></span>

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

### <span data-ttu-id="6997a-133">-Nowait</span><span class="sxs-lookup"><span data-stu-id="6997a-133">-NoWait</span></span>
<span data-ttu-id="6997a-134">Kör kommandot asynkront</span><span class="sxs-lookup"><span data-stu-id="6997a-134">Run the command asynchronously</span></span>

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

### <span data-ttu-id="6997a-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6997a-135">-ResourceGroupName</span></span>
<span data-ttu-id="6997a-136">Namnet på resurs gruppen som innehåller resursen.</span><span class="sxs-lookup"><span data-stu-id="6997a-136">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="6997a-137">Det här värdet kan hämtas från Azure Resource Manager API eller till portalen.</span><span class="sxs-lookup"><span data-stu-id="6997a-137">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="6997a-138">-ServerName</span><span class="sxs-lookup"><span data-stu-id="6997a-138">-ServerName</span></span>
<span data-ttu-id="6997a-139">Namnet på servern.</span><span class="sxs-lookup"><span data-stu-id="6997a-139">The name of the server.</span></span>

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

### <span data-ttu-id="6997a-140">-StartIPAddress</span><span class="sxs-lookup"><span data-stu-id="6997a-140">-StartIPAddress</span></span>
<span data-ttu-id="6997a-141">Den första IP-adressen för Server brand Väggs regeln.</span><span class="sxs-lookup"><span data-stu-id="6997a-141">The start IP address of the server firewall rule.</span></span>
<span data-ttu-id="6997a-142">Måste vara IPv4-format.</span><span class="sxs-lookup"><span data-stu-id="6997a-142">Must be IPv4 format.</span></span>

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

### <span data-ttu-id="6997a-143">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="6997a-143">-SubscriptionId</span></span>
<span data-ttu-id="6997a-144">Det prenumerations-ID som identifierar en Azure-prenumeration.</span><span class="sxs-lookup"><span data-stu-id="6997a-144">The subscription ID that identifies an Azure subscription.</span></span>

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

### <span data-ttu-id="6997a-145">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="6997a-145">-Confirm</span></span>
<span data-ttu-id="6997a-146">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="6997a-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6997a-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6997a-147">-WhatIf</span></span>
<span data-ttu-id="6997a-148">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="6997a-148">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6997a-149">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="6997a-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6997a-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6997a-150">CommonParameters</span></span>
<span data-ttu-id="6997a-151">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6997a-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6997a-152">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="6997a-152">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6997a-153">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="6997a-153">INPUTS</span></span>

### <span data-ttu-id="6997a-154">Microsoft. Azure. PowerShell. cmdletar. MariaDb. Models. IMariaDbIdentity</span><span class="sxs-lookup"><span data-stu-id="6997a-154">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.IMariaDbIdentity</span></span>

## <span data-ttu-id="6997a-155">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="6997a-155">OUTPUTS</span></span>

### <span data-ttu-id="6997a-156">Microsoft. Azure. PowerShell. cmdletar. MariaDb. Models. Api20180601Preview. IFirewallRule</span><span class="sxs-lookup"><span data-stu-id="6997a-156">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.Api20180601Preview.IFirewallRule</span></span>

## <span data-ttu-id="6997a-157">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="6997a-157">NOTES</span></span>

<span data-ttu-id="6997a-158">ALIAS</span><span class="sxs-lookup"><span data-stu-id="6997a-158">ALIASES</span></span>

<span data-ttu-id="6997a-159">KOMPLEXA PARAMETER EGENSKAPER</span><span class="sxs-lookup"><span data-stu-id="6997a-159">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="6997a-160">Skapa en hash-tabell som innehåller lämpliga egenskaper för att lägga till de parametrar som beskrivs nedan.</span><span class="sxs-lookup"><span data-stu-id="6997a-160">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="6997a-161">Om du vill ha information om hash-tabeller kör Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="6997a-161">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="6997a-162">INPUTOBJECT <IMariaDbIdentity> : identitets parameter</span><span class="sxs-lookup"><span data-stu-id="6997a-162">INPUTOBJECT <IMariaDbIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="6997a-163">`[ConfigurationName <String>]`: Server konfigurationens namn.</span><span class="sxs-lookup"><span data-stu-id="6997a-163">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="6997a-164">`[DatabaseName <String>]`: Namnet på databasen.</span><span class="sxs-lookup"><span data-stu-id="6997a-164">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="6997a-165">`[FirewallRuleName <String>]`: Namnet på Server brand Väggs regeln.</span><span class="sxs-lookup"><span data-stu-id="6997a-165">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="6997a-166">`[Id <String>]`: Sökväg till resurs identitet</span><span class="sxs-lookup"><span data-stu-id="6997a-166">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="6997a-167">`[LocationName <String>]`: Namnet på platsen.</span><span class="sxs-lookup"><span data-stu-id="6997a-167">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="6997a-168">`[ResourceGroupName <String>]`: Namnet på resurs gruppen som innehåller resursen.</span><span class="sxs-lookup"><span data-stu-id="6997a-168">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="6997a-169">Det här värdet kan hämtas från Azure Resource Manager API eller till portalen.</span><span class="sxs-lookup"><span data-stu-id="6997a-169">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="6997a-170">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: Namnet på säkerhets varnings principen.</span><span class="sxs-lookup"><span data-stu-id="6997a-170">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="6997a-171">`[ServerName <String>]`: Namnet på servern.</span><span class="sxs-lookup"><span data-stu-id="6997a-171">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="6997a-172">`[SubscriptionId <String>]`: Det prenumerations-ID som identifierar en Azure-prenumeration.</span><span class="sxs-lookup"><span data-stu-id="6997a-172">`[SubscriptionId <String>]`: The subscription ID that identifies an Azure subscription.</span></span>
  - <span data-ttu-id="6997a-173">`[VirtualNetworkRuleName <String>]`: Namnet på den virtuella nätverks regeln.</span><span class="sxs-lookup"><span data-stu-id="6997a-173">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="6997a-174">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="6997a-174">RELATED LINKS</span></span>
