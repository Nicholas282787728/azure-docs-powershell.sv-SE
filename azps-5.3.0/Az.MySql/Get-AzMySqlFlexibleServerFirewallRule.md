---
external help file: ''
Module Name: Az.MySql
online version: https://docs.microsoft.com/en-us/powershell/module/az.mysql/get-azmysqlflexibleserverfirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Get-AzMySqlFlexibleServerFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Get-AzMySqlFlexibleServerFirewallRule.md
ms.openlocfilehash: 7f2a3e567da4df9a004c5dac642f480a4cd7388a
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98525900"
---
# <span data-ttu-id="961f1-101">Get-AzMySqlFlexibleServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="961f1-101">Get-AzMySqlFlexibleServerFirewallRule</span></span>

## <span data-ttu-id="961f1-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="961f1-102">SYNOPSIS</span></span>
<span data-ttu-id="961f1-103">Hämtar information om en server brand Väggs regel.</span><span class="sxs-lookup"><span data-stu-id="961f1-103">Gets information about a server firewall rule.</span></span>

## <span data-ttu-id="961f1-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="961f1-104">SYNTAX</span></span>

### <span data-ttu-id="961f1-105">Lista (standard)</span><span class="sxs-lookup"><span data-stu-id="961f1-105">List (Default)</span></span>
```
Get-AzMySqlFlexibleServerFirewallRule -ResourceGroupName <String> -ServerName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="961f1-106">Lära</span><span class="sxs-lookup"><span data-stu-id="961f1-106">Get</span></span>
```
Get-AzMySqlFlexibleServerFirewallRule -Name <String> -ResourceGroupName <String> -ServerName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="961f1-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="961f1-107">GetViaIdentity</span></span>
```
Get-AzMySqlFlexibleServerFirewallRule -InputObject <IMySqlIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="961f1-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="961f1-108">DESCRIPTION</span></span>
<span data-ttu-id="961f1-109">Hämtar information om en server brand Väggs regel.</span><span class="sxs-lookup"><span data-stu-id="961f1-109">Gets information about a server firewall rule.</span></span>

## <span data-ttu-id="961f1-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="961f1-110">EXAMPLES</span></span>

### <span data-ttu-id="961f1-111">Exempel 1: Hämta brand Väggs regler efter namn</span><span class="sxs-lookup"><span data-stu-id="961f1-111">Example 1: Get firewall rules by name</span></span>
```powershell
PS C:\> Get-AzMySqlFlexibleServerFirewallRule -Name firewallrule-test -ResourceGroupName PowershellMySqlTest -ServerName mysql-test

FirewallRuleName   StartIPAddress   EndIPAddress
-----------------  ---------------  ---------------
firewallrule-test   12.12.12.12     23.23.23.23
```

<span data-ttu-id="961f1-112">Denna cmdlet får brand Väggs regler efter namn.</span><span class="sxs-lookup"><span data-stu-id="961f1-112">This cmdlet gets firewall rules by name.</span></span>

### <span data-ttu-id="961f1-113">Exempel 2: Hämta brand Väggs regler efter identitet</span><span class="sxs-lookup"><span data-stu-id="961f1-113">Example 2: Get firewall rules by identity</span></span>
```powershell
PS C:\> $ID = "/subscriptions/<SubscriptionId>/resourceGroups/PowershellMySqlTest/providers/Microsoft.DBForMySql/servers/mysql-test/firewallRules/firewallrule-test"
PS C:\> Get-AzMySqlFlexibleServerFirewallRule -InputObject $ID

FirewallRuleName   StartIPAddress   EndIPAddress
-----------------  ---------------  ---------------
firewallrule-test   12.12.12.12     23.23.23.23
```

<span data-ttu-id="961f1-114">Denna cmdlet får brand Väggs regler efter identitet.</span><span class="sxs-lookup"><span data-stu-id="961f1-114">This cmdlet gets firewall rules by identity.</span></span>

### <span data-ttu-id="961f1-115">Exempel 3: visar alla brand Väggs regler i den angivna MySql-servern</span><span class="sxs-lookup"><span data-stu-id="961f1-115">Example 3: Lists all the firewall rules in the specified MySql server</span></span>
```powershell
PS C:\> Get-AzMySqlFlexibleServerFirewallRule -ResourceGroupName PowershellMySqlTest -ServerName mysql-test

FirewallRuleName   StartIPAddress   EndIPAddress
-----------------  ---------------  ---------------
firewallrule-test   12.12.12.12     23.23.23.23
firewallrule-test2  12.12.12.15     23.23.23.25
```

<span data-ttu-id="961f1-116">Denna cmdlet visar alla brand Väggs regler i angiven MySql-Server.</span><span class="sxs-lookup"><span data-stu-id="961f1-116">This cmdlet lists all the firewall rule in specified MySql server.</span></span>

## <span data-ttu-id="961f1-117">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="961f1-117">PARAMETERS</span></span>

### <span data-ttu-id="961f1-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="961f1-118">-DefaultProfile</span></span>
<span data-ttu-id="961f1-119">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="961f1-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="961f1-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="961f1-120">-InputObject</span></span>
<span data-ttu-id="961f1-121">Identitets parameter för att konstruera, se avsnittet anteckningar för INPUTOBJECT-egenskaper och skapa en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="961f1-121">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="961f1-122">-Namn</span><span class="sxs-lookup"><span data-stu-id="961f1-122">-Name</span></span>
<span data-ttu-id="961f1-123">Namnet på Server brand Väggs regeln.</span><span class="sxs-lookup"><span data-stu-id="961f1-123">The name of the server firewall rule.</span></span>

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

### <span data-ttu-id="961f1-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="961f1-124">-ResourceGroupName</span></span>
<span data-ttu-id="961f1-125">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="961f1-125">The name of the resource group.</span></span>
<span data-ttu-id="961f1-126">Namnet är Skift läges okänsligt.</span><span class="sxs-lookup"><span data-stu-id="961f1-126">The name is case insensitive.</span></span>

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

### <span data-ttu-id="961f1-127">-ServerName</span><span class="sxs-lookup"><span data-stu-id="961f1-127">-ServerName</span></span>
<span data-ttu-id="961f1-128">Namnet på servern.</span><span class="sxs-lookup"><span data-stu-id="961f1-128">The name of the server.</span></span>

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

### <span data-ttu-id="961f1-129">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="961f1-129">-SubscriptionId</span></span>
<span data-ttu-id="961f1-130">ID för mål prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="961f1-130">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="961f1-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="961f1-131">CommonParameters</span></span>
<span data-ttu-id="961f1-132">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="961f1-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="961f1-133">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="961f1-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="961f1-134">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="961f1-134">INPUTS</span></span>

### <span data-ttu-id="961f1-135">Microsoft. Azure. PowerShell. cmdletar. MySql. Models. IMySqlIdentity</span><span class="sxs-lookup"><span data-stu-id="961f1-135">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity</span></span>

## <span data-ttu-id="961f1-136">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="961f1-136">OUTPUTS</span></span>

### <span data-ttu-id="961f1-137">Microsoft. Azure. PowerShell. cmdletar. MySql. Models. Api20171201. IFirewallRule</span><span class="sxs-lookup"><span data-stu-id="961f1-137">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20171201.IFirewallRule</span></span>

## <span data-ttu-id="961f1-138">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="961f1-138">NOTES</span></span>

<span data-ttu-id="961f1-139">ALIAS</span><span class="sxs-lookup"><span data-stu-id="961f1-139">ALIASES</span></span>

<span data-ttu-id="961f1-140">KOMPLEXA PARAMETER EGENSKAPER</span><span class="sxs-lookup"><span data-stu-id="961f1-140">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="961f1-141">Skapa en hash-tabell som innehåller lämpliga egenskaper för att lägga till de parametrar som beskrivs nedan.</span><span class="sxs-lookup"><span data-stu-id="961f1-141">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="961f1-142">Om du vill ha information om hash-tabeller kör Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="961f1-142">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="961f1-143">INPUTOBJECT <IMySqlIdentity> : identitets parameter</span><span class="sxs-lookup"><span data-stu-id="961f1-143">INPUTOBJECT <IMySqlIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="961f1-144">`[ConfigurationName <String>]`: Server konfigurationens namn.</span><span class="sxs-lookup"><span data-stu-id="961f1-144">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="961f1-145">`[DatabaseName <String>]`: Namnet på databasen.</span><span class="sxs-lookup"><span data-stu-id="961f1-145">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="961f1-146">`[FirewallRuleName <String>]`: Namnet på Server brand Väggs regeln.</span><span class="sxs-lookup"><span data-stu-id="961f1-146">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="961f1-147">`[Id <String>]`: Sökväg till resurs identitet</span><span class="sxs-lookup"><span data-stu-id="961f1-147">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="961f1-148">`[KeyName <String>]`: Server namnet.</span><span class="sxs-lookup"><span data-stu-id="961f1-148">`[KeyName <String>]`: The name of the server key.</span></span>
  - <span data-ttu-id="961f1-149">`[LocationName <String>]`: Namnet på platsen.</span><span class="sxs-lookup"><span data-stu-id="961f1-149">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="961f1-150">`[ResourceGroupName <String>]`: Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="961f1-150">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="961f1-151">Namnet är Skift läges okänsligt.</span><span class="sxs-lookup"><span data-stu-id="961f1-151">The name is case insensitive.</span></span>
  - <span data-ttu-id="961f1-152">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: Namnet på säkerhets varnings principen.</span><span class="sxs-lookup"><span data-stu-id="961f1-152">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="961f1-153">`[ServerName <String>]`: Namnet på servern.</span><span class="sxs-lookup"><span data-stu-id="961f1-153">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="961f1-154">`[SubscriptionId <String>]`: Mål prenumerationens ID.</span><span class="sxs-lookup"><span data-stu-id="961f1-154">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="961f1-155">`[VirtualNetworkRuleName <String>]`: Namnet på den virtuella nätverks regeln.</span><span class="sxs-lookup"><span data-stu-id="961f1-155">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="961f1-156">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="961f1-156">RELATED LINKS</span></span>

