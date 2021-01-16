---
external help file: ''
Module Name: Az.MySql
online version: https://docs.microsoft.com/en-us/powershell/module/az.mysql/get-azmysqlflexibleserverfirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Get-AzMySqlFlexibleServerFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Get-AzMySqlFlexibleServerFirewallRule.md
ms.openlocfilehash: 7f2a3e567da4df9a004c5dac642f480a4cd7388a
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98410184"
---
# <span data-ttu-id="95d4d-101">Get-AzMySqlFlexibleServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="95d4d-101">Get-AzMySqlFlexibleServerFirewallRule</span></span>

## <span data-ttu-id="95d4d-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="95d4d-102">SYNOPSIS</span></span>
<span data-ttu-id="95d4d-103">Hämtar information om en server brand Väggs regel.</span><span class="sxs-lookup"><span data-stu-id="95d4d-103">Gets information about a server firewall rule.</span></span>

## <span data-ttu-id="95d4d-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="95d4d-104">SYNTAX</span></span>

### <span data-ttu-id="95d4d-105">Lista (standard)</span><span class="sxs-lookup"><span data-stu-id="95d4d-105">List (Default)</span></span>
```
Get-AzMySqlFlexibleServerFirewallRule -ResourceGroupName <String> -ServerName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="95d4d-106">Lära</span><span class="sxs-lookup"><span data-stu-id="95d4d-106">Get</span></span>
```
Get-AzMySqlFlexibleServerFirewallRule -Name <String> -ResourceGroupName <String> -ServerName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="95d4d-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="95d4d-107">GetViaIdentity</span></span>
```
Get-AzMySqlFlexibleServerFirewallRule -InputObject <IMySqlIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="95d4d-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="95d4d-108">DESCRIPTION</span></span>
<span data-ttu-id="95d4d-109">Hämtar information om en server brand Väggs regel.</span><span class="sxs-lookup"><span data-stu-id="95d4d-109">Gets information about a server firewall rule.</span></span>

## <span data-ttu-id="95d4d-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="95d4d-110">EXAMPLES</span></span>

### <span data-ttu-id="95d4d-111">Exempel 1: Hämta brand Väggs regler efter namn</span><span class="sxs-lookup"><span data-stu-id="95d4d-111">Example 1: Get firewall rules by name</span></span>
```powershell
PS C:\> Get-AzMySqlFlexibleServerFirewallRule -Name firewallrule-test -ResourceGroupName PowershellMySqlTest -ServerName mysql-test

FirewallRuleName   StartIPAddress   EndIPAddress
-----------------  ---------------  ---------------
firewallrule-test   12.12.12.12     23.23.23.23
```

<span data-ttu-id="95d4d-112">Denna cmdlet får brand Väggs regler efter namn.</span><span class="sxs-lookup"><span data-stu-id="95d4d-112">This cmdlet gets firewall rules by name.</span></span>

### <span data-ttu-id="95d4d-113">Exempel 2: Hämta brand Väggs regler efter identitet</span><span class="sxs-lookup"><span data-stu-id="95d4d-113">Example 2: Get firewall rules by identity</span></span>
```powershell
PS C:\> $ID = "/subscriptions/<SubscriptionId>/resourceGroups/PowershellMySqlTest/providers/Microsoft.DBForMySql/servers/mysql-test/firewallRules/firewallrule-test"
PS C:\> Get-AzMySqlFlexibleServerFirewallRule -InputObject $ID

FirewallRuleName   StartIPAddress   EndIPAddress
-----------------  ---------------  ---------------
firewallrule-test   12.12.12.12     23.23.23.23
```

<span data-ttu-id="95d4d-114">Denna cmdlet får brand Väggs regler efter identitet.</span><span class="sxs-lookup"><span data-stu-id="95d4d-114">This cmdlet gets firewall rules by identity.</span></span>

### <span data-ttu-id="95d4d-115">Exempel 3: visar alla brand Väggs regler i den angivna MySql-servern</span><span class="sxs-lookup"><span data-stu-id="95d4d-115">Example 3: Lists all the firewall rules in the specified MySql server</span></span>
```powershell
PS C:\> Get-AzMySqlFlexibleServerFirewallRule -ResourceGroupName PowershellMySqlTest -ServerName mysql-test

FirewallRuleName   StartIPAddress   EndIPAddress
-----------------  ---------------  ---------------
firewallrule-test   12.12.12.12     23.23.23.23
firewallrule-test2  12.12.12.15     23.23.23.25
```

<span data-ttu-id="95d4d-116">Denna cmdlet visar alla brand Väggs regler i angiven MySql-Server.</span><span class="sxs-lookup"><span data-stu-id="95d4d-116">This cmdlet lists all the firewall rule in specified MySql server.</span></span>

## <span data-ttu-id="95d4d-117">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="95d4d-117">PARAMETERS</span></span>

### <span data-ttu-id="95d4d-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="95d4d-118">-DefaultProfile</span></span>
<span data-ttu-id="95d4d-119">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="95d4d-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="95d4d-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="95d4d-120">-InputObject</span></span>
<span data-ttu-id="95d4d-121">Identitets parameter för att konstruera, se avsnittet anteckningar för INPUTOBJECT-egenskaper och skapa en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="95d4d-121">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="95d4d-122">-Namn</span><span class="sxs-lookup"><span data-stu-id="95d4d-122">-Name</span></span>
<span data-ttu-id="95d4d-123">Namnet på Server brand Väggs regeln.</span><span class="sxs-lookup"><span data-stu-id="95d4d-123">The name of the server firewall rule.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: FirewallRuleName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="95d4d-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="95d4d-124">-ResourceGroupName</span></span>
<span data-ttu-id="95d4d-125">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="95d4d-125">The name of the resource group.</span></span>
<span data-ttu-id="95d4d-126">Namnet är Skift läges okänsligt.</span><span class="sxs-lookup"><span data-stu-id="95d4d-126">The name is case insensitive.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="95d4d-127">-ServerName</span><span class="sxs-lookup"><span data-stu-id="95d4d-127">-ServerName</span></span>
<span data-ttu-id="95d4d-128">Namnet på servern.</span><span class="sxs-lookup"><span data-stu-id="95d4d-128">The name of the server.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="95d4d-129">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="95d4d-129">-SubscriptionId</span></span>
<span data-ttu-id="95d4d-130">ID för mål prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="95d4d-130">The ID of the target subscription.</span></span>

```yaml
Type: System.String[]
Parameter Sets: Get, List
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="95d4d-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="95d4d-131">CommonParameters</span></span>
<span data-ttu-id="95d4d-132">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="95d4d-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="95d4d-133">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="95d4d-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="95d4d-134">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="95d4d-134">INPUTS</span></span>

### <span data-ttu-id="95d4d-135">Microsoft. Azure. PowerShell. cmdletar. MySql. Models. IMySqlIdentity</span><span class="sxs-lookup"><span data-stu-id="95d4d-135">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity</span></span>

## <span data-ttu-id="95d4d-136">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="95d4d-136">OUTPUTS</span></span>

### <span data-ttu-id="95d4d-137">Microsoft. Azure. PowerShell. cmdletar. MySql. Models. Api20171201. IFirewallRule</span><span class="sxs-lookup"><span data-stu-id="95d4d-137">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20171201.IFirewallRule</span></span>

## <span data-ttu-id="95d4d-138">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="95d4d-138">NOTES</span></span>

<span data-ttu-id="95d4d-139">ALIAS</span><span class="sxs-lookup"><span data-stu-id="95d4d-139">ALIASES</span></span>

<span data-ttu-id="95d4d-140">KOMPLEXA PARAMETER EGENSKAPER</span><span class="sxs-lookup"><span data-stu-id="95d4d-140">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="95d4d-141">Skapa en hash-tabell som innehåller lämpliga egenskaper för att lägga till de parametrar som beskrivs nedan.</span><span class="sxs-lookup"><span data-stu-id="95d4d-141">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="95d4d-142">Om du vill ha information om hash-tabeller kör Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="95d4d-142">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="95d4d-143">INPUTOBJECT <IMySqlIdentity> : identitets parameter</span><span class="sxs-lookup"><span data-stu-id="95d4d-143">INPUTOBJECT <IMySqlIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="95d4d-144">`[ConfigurationName <String>]`: Server konfigurationens namn.</span><span class="sxs-lookup"><span data-stu-id="95d4d-144">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="95d4d-145">`[DatabaseName <String>]`: Namnet på databasen.</span><span class="sxs-lookup"><span data-stu-id="95d4d-145">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="95d4d-146">`[FirewallRuleName <String>]`: Namnet på Server brand Väggs regeln.</span><span class="sxs-lookup"><span data-stu-id="95d4d-146">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="95d4d-147">`[Id <String>]`: Sökväg till resurs identitet</span><span class="sxs-lookup"><span data-stu-id="95d4d-147">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="95d4d-148">`[KeyName <String>]`: Server namnet.</span><span class="sxs-lookup"><span data-stu-id="95d4d-148">`[KeyName <String>]`: The name of the server key.</span></span>
  - <span data-ttu-id="95d4d-149">`[LocationName <String>]`: Namnet på platsen.</span><span class="sxs-lookup"><span data-stu-id="95d4d-149">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="95d4d-150">`[ResourceGroupName <String>]`: Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="95d4d-150">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="95d4d-151">Namnet är Skift läges okänsligt.</span><span class="sxs-lookup"><span data-stu-id="95d4d-151">The name is case insensitive.</span></span>
  - <span data-ttu-id="95d4d-152">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: Namnet på säkerhets varnings principen.</span><span class="sxs-lookup"><span data-stu-id="95d4d-152">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="95d4d-153">`[ServerName <String>]`: Namnet på servern.</span><span class="sxs-lookup"><span data-stu-id="95d4d-153">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="95d4d-154">`[SubscriptionId <String>]`: Mål prenumerationens ID.</span><span class="sxs-lookup"><span data-stu-id="95d4d-154">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="95d4d-155">`[VirtualNetworkRuleName <String>]`: Namnet på den virtuella nätverks regeln.</span><span class="sxs-lookup"><span data-stu-id="95d4d-155">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="95d4d-156">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="95d4d-156">RELATED LINKS</span></span>

