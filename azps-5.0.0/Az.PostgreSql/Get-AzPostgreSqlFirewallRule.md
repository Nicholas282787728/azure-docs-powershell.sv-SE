---
external help file: ''
Module Name: Az.PostgreSql
online version: https://docs.microsoft.com/en-us/powershell/module/az.postgresql/get-azpostgresqlfirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Get-AzPostgreSqlFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Get-AzPostgreSqlFirewallRule.md
ms.openlocfilehash: a5691b1d8181d210770802c8d3aa4526b6bd72f2
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94271456"
---
# <span data-ttu-id="b4765-101">Get-AzPostgreSqlFirewallRule</span><span class="sxs-lookup"><span data-stu-id="b4765-101">Get-AzPostgreSqlFirewallRule</span></span>

## <span data-ttu-id="b4765-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="b4765-102">SYNOPSIS</span></span>
<span data-ttu-id="b4765-103">Hämtar information om en server brand Väggs regel.</span><span class="sxs-lookup"><span data-stu-id="b4765-103">Gets information about a server firewall rule.</span></span>

## <span data-ttu-id="b4765-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="b4765-104">SYNTAX</span></span>

### <span data-ttu-id="b4765-105">Lista (standard)</span><span class="sxs-lookup"><span data-stu-id="b4765-105">List (Default)</span></span>
```
Get-AzPostgreSqlFirewallRule -ResourceGroupName <String> -ServerName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="b4765-106">Lära</span><span class="sxs-lookup"><span data-stu-id="b4765-106">Get</span></span>
```
Get-AzPostgreSqlFirewallRule -Name <String> -ResourceGroupName <String> -ServerName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="b4765-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="b4765-107">GetViaIdentity</span></span>
```
Get-AzPostgreSqlFirewallRule -InputObject <IPostgreSqlIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="b4765-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="b4765-108">DESCRIPTION</span></span>
<span data-ttu-id="b4765-109">Hämtar information om en server brand Väggs regel.</span><span class="sxs-lookup"><span data-stu-id="b4765-109">Gets information about a server firewall rule.</span></span>

## <span data-ttu-id="b4765-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="b4765-110">EXAMPLES</span></span>

### <span data-ttu-id="b4765-111">Exempel 1: visar alla brand Väggs regler i angiven PostgreSql-Server</span><span class="sxs-lookup"><span data-stu-id="b4765-111">Example 1: Lists all the Firewall Rules in specified PostgreSql server</span></span>
```powershell
PS C:\> Get-AzPostgreSqlFirewallRule -ResourceGroupName PostgreSqlTestRG -ServerName PostgreSqlTestServer

Name StartIPAddress EndIPAddress
---- -------------- ------------
rule 0.0.0.0        0.0.0.1
```

<span data-ttu-id="b4765-112">Denna cmdlet visar alla brand Väggs regler i angiven PostgreSql-Server.</span><span class="sxs-lookup"><span data-stu-id="b4765-112">This cmdlet lists all the Firewall Rule in specified PostgreSql server.</span></span>

### <span data-ttu-id="b4765-113">Exempel 2: Hämta brand Väggs regel efter namn</span><span class="sxs-lookup"><span data-stu-id="b4765-113">Example 2: Get Firewall Rule by name</span></span>
```powershell
PS C:\> Get-AzPostgreSqlFirewallRule -Name rule -ResourceGroupName PostgreSqlTestRG -ServerName PostgreSqlTestServer

Name StartIPAddress EndIPAddress
---- -------------- ------------
rule 0.0.0.0        0.0.0.1
```

<span data-ttu-id="b4765-114">Denna cmdlet får brand Väggs regeln efter namn.</span><span class="sxs-lookup"><span data-stu-id="b4765-114">This cmdlet gets Firewall Rule by name.</span></span>

### <span data-ttu-id="b4765-115">Exempel 3: Hämta brand Väggs regel efter identitet</span><span class="sxs-lookup"><span data-stu-id="b4765-115">Example 3: Get Firewall Rule by identity</span></span>
```powershell
PS C:\> $ID = "/subscriptions/<SubscriptionId>/resourceGroups/PostgreSqlTestRG/providers/Microsoft.DBforPostgreSQL/servers/PostgreSqlTestServer/firewallRules/rule"
PS C:\> Get-AzPostgreSqlFirewallRule -InputObject $ID

Name StartIPAddress EndIPAddress
---- -------------- ------------
rule 0.0.0.0        0.0.0.1
```

<span data-ttu-id="b4765-116">Denna cmdlet får brand Väggs regel efter identitet.</span><span class="sxs-lookup"><span data-stu-id="b4765-116">This cmdlet gets Firewall Rule by identity.</span></span>

## <span data-ttu-id="b4765-117">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="b4765-117">PARAMETERS</span></span>

### <span data-ttu-id="b4765-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b4765-118">-DefaultProfile</span></span>
<span data-ttu-id="b4765-119">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="b4765-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b4765-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b4765-120">-InputObject</span></span>
<span data-ttu-id="b4765-121">Identitets parameter för att konstruera, se avsnittet anteckningar för INPUTOBJECT-egenskaper och skapa en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="b4765-121">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.IPostgreSqlIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b4765-122">-Namn</span><span class="sxs-lookup"><span data-stu-id="b4765-122">-Name</span></span>
<span data-ttu-id="b4765-123">Namnet på Server brand Väggs regeln.</span><span class="sxs-lookup"><span data-stu-id="b4765-123">The name of the server firewall rule.</span></span>

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

### <span data-ttu-id="b4765-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b4765-124">-ResourceGroupName</span></span>
<span data-ttu-id="b4765-125">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="b4765-125">The name of the resource group.</span></span>
<span data-ttu-id="b4765-126">Namnet är Skift läges okänsligt.</span><span class="sxs-lookup"><span data-stu-id="b4765-126">The name is case insensitive.</span></span>

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

### <span data-ttu-id="b4765-127">-ServerName</span><span class="sxs-lookup"><span data-stu-id="b4765-127">-ServerName</span></span>
<span data-ttu-id="b4765-128">Namnet på servern.</span><span class="sxs-lookup"><span data-stu-id="b4765-128">The name of the server.</span></span>

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

### <span data-ttu-id="b4765-129">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="b4765-129">-SubscriptionId</span></span>
<span data-ttu-id="b4765-130">ID för mål prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="b4765-130">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="b4765-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b4765-131">CommonParameters</span></span>
<span data-ttu-id="b4765-132">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b4765-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b4765-133">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b4765-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b4765-134">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="b4765-134">INPUTS</span></span>

### <span data-ttu-id="b4765-135">Microsoft. Azure. PowerShell. cmdletar. PostgreSql. Models. IPostgreSqlIdentity</span><span class="sxs-lookup"><span data-stu-id="b4765-135">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.IPostgreSqlIdentity</span></span>

## <span data-ttu-id="b4765-136">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="b4765-136">OUTPUTS</span></span>

### <span data-ttu-id="b4765-137">Microsoft. Azure. PowerShell. cmdletar. PostgreSql. Models. Api20171201. IFirewallRule</span><span class="sxs-lookup"><span data-stu-id="b4765-137">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.Api20171201.IFirewallRule</span></span>

## <span data-ttu-id="b4765-138">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="b4765-138">NOTES</span></span>

<span data-ttu-id="b4765-139">ALIAS</span><span class="sxs-lookup"><span data-stu-id="b4765-139">ALIASES</span></span>

<span data-ttu-id="b4765-140">KOMPLEXA PARAMETER EGENSKAPER</span><span class="sxs-lookup"><span data-stu-id="b4765-140">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="b4765-141">Skapa en hash-tabell som innehåller lämpliga egenskaper för att lägga till de parametrar som beskrivs nedan.</span><span class="sxs-lookup"><span data-stu-id="b4765-141">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="b4765-142">Om du vill ha information om hash-tabeller kör Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="b4765-142">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="b4765-143">INPUTOBJECT <IPostgreSqlIdentity> : identitets parameter</span><span class="sxs-lookup"><span data-stu-id="b4765-143">INPUTOBJECT <IPostgreSqlIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="b4765-144">`[ConfigurationName <String>]`: Server konfigurationens namn.</span><span class="sxs-lookup"><span data-stu-id="b4765-144">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="b4765-145">`[DatabaseName <String>]`: Namnet på databasen.</span><span class="sxs-lookup"><span data-stu-id="b4765-145">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="b4765-146">`[FirewallRuleName <String>]`: Namnet på Server brand Väggs regeln.</span><span class="sxs-lookup"><span data-stu-id="b4765-146">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="b4765-147">`[Id <String>]`: Sökväg till resurs identitet</span><span class="sxs-lookup"><span data-stu-id="b4765-147">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="b4765-148">`[LocationName <String>]`: Namnet på platsen.</span><span class="sxs-lookup"><span data-stu-id="b4765-148">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="b4765-149">`[ResourceGroupName <String>]`: Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="b4765-149">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="b4765-150">Namnet är Skift läges okänsligt.</span><span class="sxs-lookup"><span data-stu-id="b4765-150">The name is case insensitive.</span></span>
  - <span data-ttu-id="b4765-151">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: Namnet på säkerhets varnings principen.</span><span class="sxs-lookup"><span data-stu-id="b4765-151">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="b4765-152">`[ServerName <String>]`: Namnet på servern.</span><span class="sxs-lookup"><span data-stu-id="b4765-152">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="b4765-153">`[SubscriptionId <String>]`: Mål prenumerationens ID.</span><span class="sxs-lookup"><span data-stu-id="b4765-153">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="b4765-154">`[VirtualNetworkRuleName <String>]`: Namnet på den virtuella nätverks regeln.</span><span class="sxs-lookup"><span data-stu-id="b4765-154">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="b4765-155">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="b4765-155">RELATED LINKS</span></span>

