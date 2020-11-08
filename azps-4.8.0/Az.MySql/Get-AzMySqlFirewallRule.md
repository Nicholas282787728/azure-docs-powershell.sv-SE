---
external help file: ''
Module Name: Az.MySql
online version: https://docs.microsoft.com/en-us/powershell/module/az.mysql/get-azmysqlfirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Get-AzMySqlFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Get-AzMySqlFirewallRule.md
ms.openlocfilehash: 11278c1d317f6f4e0171513a4503c5681506f1ac
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94261204"
---
# <span data-ttu-id="d8a62-101">Get-AzMySqlFirewallRule</span><span class="sxs-lookup"><span data-stu-id="d8a62-101">Get-AzMySqlFirewallRule</span></span>

## <span data-ttu-id="d8a62-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="d8a62-102">SYNOPSIS</span></span>
<span data-ttu-id="d8a62-103">Hämtar information om en server brand Väggs regel.</span><span class="sxs-lookup"><span data-stu-id="d8a62-103">Gets information about a server firewall rule.</span></span>

## <span data-ttu-id="d8a62-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="d8a62-104">SYNTAX</span></span>

### <span data-ttu-id="d8a62-105">Lista (standard)</span><span class="sxs-lookup"><span data-stu-id="d8a62-105">List (Default)</span></span>
```
Get-AzMySqlFirewallRule -ResourceGroupName <String> -ServerName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="d8a62-106">Lära</span><span class="sxs-lookup"><span data-stu-id="d8a62-106">Get</span></span>
```
Get-AzMySqlFirewallRule -Name <String> -ResourceGroupName <String> -ServerName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="d8a62-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="d8a62-107">GetViaIdentity</span></span>
```
Get-AzMySqlFirewallRule -InputObject <IMySqlIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="d8a62-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="d8a62-108">DESCRIPTION</span></span>
<span data-ttu-id="d8a62-109">Hämtar information om en server brand Väggs regel.</span><span class="sxs-lookup"><span data-stu-id="d8a62-109">Gets information about a server firewall rule.</span></span>

## <span data-ttu-id="d8a62-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="d8a62-110">EXAMPLES</span></span>

### <span data-ttu-id="d8a62-111">Exempel 1: visar alla brand Väggs regler i angiven MySql-Server</span><span class="sxs-lookup"><span data-stu-id="d8a62-111">Example 1: Lists all the Firewall Rules in specified MySql server</span></span>
```powershell
PS C:\> Get-AzMySqlFirewallRule -ResourceGroupName PowershellMySqlTest -ServerName mysql-test

Name Type
---- ----
rule Microsoft.DBforMySQL/servers/firewallRules
```

<span data-ttu-id="d8a62-112">Denna cmdlet visar alla brand Väggs regler i angiven MySql-Server.</span><span class="sxs-lookup"><span data-stu-id="d8a62-112">This cmdlet lists all the Firewall Rule in specified MySql server.</span></span>

### <span data-ttu-id="d8a62-113">Exempel 2: Hämta brand Väggs regel efter namn</span><span class="sxs-lookup"><span data-stu-id="d8a62-113">Example 2: Get Firewall Rule by name</span></span>
```powershell
PS C:\> Get-AzMySqlFirewallRule -Name rule -ResourceGroupName PowershellMySqlTest -ServerName mysql-test

Name Type
---- ----
rule Microsoft.DBforMySQL/servers/firewallRules
```

<span data-ttu-id="d8a62-114">Denna cmdlet får brand Väggs regeln efter namn.</span><span class="sxs-lookup"><span data-stu-id="d8a62-114">This cmdlet gets Firewall Rule by name.</span></span>

### <span data-ttu-id="d8a62-115">Exempel 3: Hämta brand Väggs regel efter identitet</span><span class="sxs-lookup"><span data-stu-id="d8a62-115">Example 3: Get Firewall Rule by identity</span></span>
```powershell
PS C:\> $ID = "/subscriptions/<SubscriptionId>/resourceGroups/PowershellMySqlTest/providers/Microsoft.DBforMySQL/servers/mysql-test/firewallRules/rule"
PS C:\> Get-AzMySqlFirewallRule -InputObject $ID

Name Type
---- ----
rule Microsoft.DBforMySQL/servers/firewallRules
```

<span data-ttu-id="d8a62-116">Denna cmdlet får brand Väggs regel efter identitet.</span><span class="sxs-lookup"><span data-stu-id="d8a62-116">This cmdlet gets Firewall Rule by identity.</span></span>

## <span data-ttu-id="d8a62-117">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="d8a62-117">PARAMETERS</span></span>

### <span data-ttu-id="d8a62-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d8a62-118">-DefaultProfile</span></span>
<span data-ttu-id="d8a62-119">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="d8a62-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d8a62-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d8a62-120">-InputObject</span></span>
<span data-ttu-id="d8a62-121">Identitets parameter för att konstruera, se avsnittet anteckningar för INPUTOBJECT-egenskaper och skapa en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="d8a62-121">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="d8a62-122">-Namn</span><span class="sxs-lookup"><span data-stu-id="d8a62-122">-Name</span></span>
<span data-ttu-id="d8a62-123">Namnet på Server brand Väggs regeln.</span><span class="sxs-lookup"><span data-stu-id="d8a62-123">The name of the server firewall rule.</span></span>

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

### <span data-ttu-id="d8a62-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d8a62-124">-ResourceGroupName</span></span>
<span data-ttu-id="d8a62-125">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="d8a62-125">The name of the resource group.</span></span>
<span data-ttu-id="d8a62-126">Namnet är Skift läges okänsligt.</span><span class="sxs-lookup"><span data-stu-id="d8a62-126">The name is case insensitive.</span></span>

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

### <span data-ttu-id="d8a62-127">-ServerName</span><span class="sxs-lookup"><span data-stu-id="d8a62-127">-ServerName</span></span>
<span data-ttu-id="d8a62-128">Namnet på servern.</span><span class="sxs-lookup"><span data-stu-id="d8a62-128">The name of the server.</span></span>

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

### <span data-ttu-id="d8a62-129">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="d8a62-129">-SubscriptionId</span></span>
<span data-ttu-id="d8a62-130">ID för mål prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="d8a62-130">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="d8a62-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d8a62-131">CommonParameters</span></span>
<span data-ttu-id="d8a62-132">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d8a62-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d8a62-133">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d8a62-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d8a62-134">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="d8a62-134">INPUTS</span></span>

### <span data-ttu-id="d8a62-135">Microsoft. Azure. PowerShell. cmdletar. MySql. Models. IMySqlIdentity</span><span class="sxs-lookup"><span data-stu-id="d8a62-135">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity</span></span>

## <span data-ttu-id="d8a62-136">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="d8a62-136">OUTPUTS</span></span>

### <span data-ttu-id="d8a62-137">Microsoft. Azure. PowerShell. cmdletar. MySql. Models. Api20171201. IFirewallRule</span><span class="sxs-lookup"><span data-stu-id="d8a62-137">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20171201.IFirewallRule</span></span>

## <span data-ttu-id="d8a62-138">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="d8a62-138">NOTES</span></span>

<span data-ttu-id="d8a62-139">ALIAS</span><span class="sxs-lookup"><span data-stu-id="d8a62-139">ALIASES</span></span>

<span data-ttu-id="d8a62-140">KOMPLEXA PARAMETER EGENSKAPER</span><span class="sxs-lookup"><span data-stu-id="d8a62-140">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="d8a62-141">Skapa en hash-tabell som innehåller lämpliga egenskaper för att lägga till de parametrar som beskrivs nedan.</span><span class="sxs-lookup"><span data-stu-id="d8a62-141">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="d8a62-142">Om du vill ha information om hash-tabeller kör Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="d8a62-142">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="d8a62-143">INPUTOBJECT <IMySqlIdentity> : identitets parameter</span><span class="sxs-lookup"><span data-stu-id="d8a62-143">INPUTOBJECT <IMySqlIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="d8a62-144">`[ConfigurationName <String>]`: Server konfigurationens namn.</span><span class="sxs-lookup"><span data-stu-id="d8a62-144">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="d8a62-145">`[DatabaseName <String>]`: Namnet på databasen.</span><span class="sxs-lookup"><span data-stu-id="d8a62-145">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="d8a62-146">`[FirewallRuleName <String>]`: Namnet på Server brand Väggs regeln.</span><span class="sxs-lookup"><span data-stu-id="d8a62-146">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="d8a62-147">`[Id <String>]`: Sökväg till resurs identitet</span><span class="sxs-lookup"><span data-stu-id="d8a62-147">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="d8a62-148">`[LocationName <String>]`: Namnet på platsen.</span><span class="sxs-lookup"><span data-stu-id="d8a62-148">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="d8a62-149">`[ResourceGroupName <String>]`: Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="d8a62-149">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="d8a62-150">Namnet är Skift läges okänsligt.</span><span class="sxs-lookup"><span data-stu-id="d8a62-150">The name is case insensitive.</span></span>
  - <span data-ttu-id="d8a62-151">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: Namnet på säkerhets varnings principen.</span><span class="sxs-lookup"><span data-stu-id="d8a62-151">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="d8a62-152">`[ServerName <String>]`: Namnet på servern.</span><span class="sxs-lookup"><span data-stu-id="d8a62-152">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="d8a62-153">`[SubscriptionId <String>]`: Mål prenumerationens ID.</span><span class="sxs-lookup"><span data-stu-id="d8a62-153">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="d8a62-154">`[VirtualNetworkRuleName <String>]`: Namnet på den virtuella nätverks regeln.</span><span class="sxs-lookup"><span data-stu-id="d8a62-154">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="d8a62-155">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="d8a62-155">RELATED LINKS</span></span>

