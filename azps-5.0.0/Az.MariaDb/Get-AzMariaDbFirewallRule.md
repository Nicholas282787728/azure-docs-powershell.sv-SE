---
external help file: ''
Module Name: Az.MariaDb
online version: https://docs.microsoft.com/en-us/powershell/module/az.mariadb/get-azmariadbfirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/Get-AzMariaDbFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/Get-AzMariaDbFirewallRule.md
ms.openlocfilehash: 2b2f52d8dc4f9e31a86b666b7ee81981fa6bd18c
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94272139"
---
# <span data-ttu-id="210f7-101">Get-AzMariaDbFirewallRule</span><span class="sxs-lookup"><span data-stu-id="210f7-101">Get-AzMariaDbFirewallRule</span></span>

## <span data-ttu-id="210f7-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="210f7-102">SYNOPSIS</span></span>
<span data-ttu-id="210f7-103">Hämtar information om en server brand Väggs regel.</span><span class="sxs-lookup"><span data-stu-id="210f7-103">Gets information about a server firewall rule.</span></span>

## <span data-ttu-id="210f7-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="210f7-104">SYNTAX</span></span>

### <span data-ttu-id="210f7-105">Lista (standard)</span><span class="sxs-lookup"><span data-stu-id="210f7-105">List (Default)</span></span>
```
Get-AzMariaDbFirewallRule -ResourceGroupName <String> -ServerName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="210f7-106">Lära</span><span class="sxs-lookup"><span data-stu-id="210f7-106">Get</span></span>
```
Get-AzMariaDbFirewallRule -Name <String> -ResourceGroupName <String> -ServerName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="210f7-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="210f7-107">GetViaIdentity</span></span>
```
Get-AzMariaDbFirewallRule -InputObject <IMariaDbIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="210f7-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="210f7-108">DESCRIPTION</span></span>
<span data-ttu-id="210f7-109">Hämtar information om en server brand Väggs regel.</span><span class="sxs-lookup"><span data-stu-id="210f7-109">Gets information about a server firewall rule.</span></span>

## <span data-ttu-id="210f7-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="210f7-110">EXAMPLES</span></span>

### <span data-ttu-id="210f7-111">Exempel 1: lista alla brand Väggs regler under en MariaDB</span><span class="sxs-lookup"><span data-stu-id="210f7-111">Example 1: List all firewall rule under a MariaDB</span></span>
```powershell
PS C:\> Get-AzMariaDbFirewallRule -ResourceGroupName mariadb-test-qu5ov0 -ServerName mariadb-test-4rmtig

Name       Type
----       ----
fr-cfgl3y  Microsoft.DBforMariaDB/servers/firewallRules
fr-usc9na  Microsoft.DBforMariaDB/servers/firewallRules
frname-001 Microsoft.DBforMariaDB/servers/firewallRules
```

<span data-ttu-id="210f7-112">Det här kommandot visar alla girewall-regler under en MariaDB.</span><span class="sxs-lookup"><span data-stu-id="210f7-112">This command lists all girewall rule under a MariaDB.</span></span>

### <span data-ttu-id="210f7-113">Exempel 2: skaffa en brand Väggs regel under en MariaDB</span><span class="sxs-lookup"><span data-stu-id="210f7-113">Example 2: Get a firewall rule under a MariaDB</span></span>
```powershell
PS C:\> Get-AzMariaDbFirewallRule -ResourceGroupName mariadb-test-qu5ov0 -ServerName mariadb-test-4rmtig -Name frname-001

Name       Type
----       ----
frname-001 Microsoft.DBforMariaDB/servers/firewallRules
```

<span data-ttu-id="210f7-114">Det här kommandot får en brand Väggs regel under en MariaDB.</span><span class="sxs-lookup"><span data-stu-id="210f7-114">This command gets a firewall rule under a MariaDB.</span></span>

## <span data-ttu-id="210f7-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="210f7-115">PARAMETERS</span></span>

### <span data-ttu-id="210f7-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="210f7-116">-DefaultProfile</span></span>
<span data-ttu-id="210f7-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="210f7-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="210f7-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="210f7-118">-InputObject</span></span>
<span data-ttu-id="210f7-119">Identitets parameter för att konstruera, se avsnittet anteckningar för INPUTOBJECT-egenskaper och skapa en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="210f7-119">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.IMariaDbIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="210f7-120">-Namn</span><span class="sxs-lookup"><span data-stu-id="210f7-120">-Name</span></span>
<span data-ttu-id="210f7-121">Namnet på Server brand Väggs regeln.</span><span class="sxs-lookup"><span data-stu-id="210f7-121">The name of the server firewall rule.</span></span>

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

### <span data-ttu-id="210f7-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="210f7-122">-ResourceGroupName</span></span>
<span data-ttu-id="210f7-123">Namnet på resurs gruppen som innehåller resursen.</span><span class="sxs-lookup"><span data-stu-id="210f7-123">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="210f7-124">Det här värdet kan hämtas från Azure Resource Manager API eller till portalen.</span><span class="sxs-lookup"><span data-stu-id="210f7-124">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="210f7-125">-ServerName</span><span class="sxs-lookup"><span data-stu-id="210f7-125">-ServerName</span></span>
<span data-ttu-id="210f7-126">Namnet på servern.</span><span class="sxs-lookup"><span data-stu-id="210f7-126">The name of the server.</span></span>

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

### <span data-ttu-id="210f7-127">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="210f7-127">-SubscriptionId</span></span>
<span data-ttu-id="210f7-128">Det prenumerations-ID som identifierar en Azure-prenumeration.</span><span class="sxs-lookup"><span data-stu-id="210f7-128">The subscription ID that identifies an Azure subscription.</span></span>

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

### <span data-ttu-id="210f7-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="210f7-129">CommonParameters</span></span>
<span data-ttu-id="210f7-130">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="210f7-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="210f7-131">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="210f7-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="210f7-132">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="210f7-132">INPUTS</span></span>

### <span data-ttu-id="210f7-133">Microsoft. Azure. PowerShell. cmdletar. MariaDb. Models. IMariaDbIdentity</span><span class="sxs-lookup"><span data-stu-id="210f7-133">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.IMariaDbIdentity</span></span>

## <span data-ttu-id="210f7-134">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="210f7-134">OUTPUTS</span></span>

### <span data-ttu-id="210f7-135">Microsoft. Azure. PowerShell. cmdletar. MariaDb. Models. Api20180601Preview. IFirewallRule</span><span class="sxs-lookup"><span data-stu-id="210f7-135">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.Api20180601Preview.IFirewallRule</span></span>

## <span data-ttu-id="210f7-136">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="210f7-136">NOTES</span></span>

<span data-ttu-id="210f7-137">ALIAS</span><span class="sxs-lookup"><span data-stu-id="210f7-137">ALIASES</span></span>

<span data-ttu-id="210f7-138">KOMPLEXA PARAMETER EGENSKAPER</span><span class="sxs-lookup"><span data-stu-id="210f7-138">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="210f7-139">Skapa en hash-tabell som innehåller lämpliga egenskaper för att lägga till de parametrar som beskrivs nedan.</span><span class="sxs-lookup"><span data-stu-id="210f7-139">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="210f7-140">Om du vill ha information om hash-tabeller kör Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="210f7-140">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="210f7-141">INPUTOBJECT <IMariaDbIdentity> : identitets parameter</span><span class="sxs-lookup"><span data-stu-id="210f7-141">INPUTOBJECT <IMariaDbIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="210f7-142">`[ConfigurationName <String>]`: Server konfigurationens namn.</span><span class="sxs-lookup"><span data-stu-id="210f7-142">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="210f7-143">`[DatabaseName <String>]`: Namnet på databasen.</span><span class="sxs-lookup"><span data-stu-id="210f7-143">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="210f7-144">`[FirewallRuleName <String>]`: Namnet på Server brand Väggs regeln.</span><span class="sxs-lookup"><span data-stu-id="210f7-144">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="210f7-145">`[Id <String>]`: Sökväg till resurs identitet</span><span class="sxs-lookup"><span data-stu-id="210f7-145">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="210f7-146">`[LocationName <String>]`: Namnet på platsen.</span><span class="sxs-lookup"><span data-stu-id="210f7-146">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="210f7-147">`[ResourceGroupName <String>]`: Namnet på resurs gruppen som innehåller resursen.</span><span class="sxs-lookup"><span data-stu-id="210f7-147">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="210f7-148">Det här värdet kan hämtas från Azure Resource Manager API eller till portalen.</span><span class="sxs-lookup"><span data-stu-id="210f7-148">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="210f7-149">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: Namnet på säkerhets varnings principen.</span><span class="sxs-lookup"><span data-stu-id="210f7-149">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="210f7-150">`[ServerName <String>]`: Namnet på servern.</span><span class="sxs-lookup"><span data-stu-id="210f7-150">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="210f7-151">`[SubscriptionId <String>]`: Det prenumerations-ID som identifierar en Azure-prenumeration.</span><span class="sxs-lookup"><span data-stu-id="210f7-151">`[SubscriptionId <String>]`: The subscription ID that identifies an Azure subscription.</span></span>
  - <span data-ttu-id="210f7-152">`[VirtualNetworkRuleName <String>]`: Namnet på den virtuella nätverks regeln.</span><span class="sxs-lookup"><span data-stu-id="210f7-152">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="210f7-153">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="210f7-153">RELATED LINKS</span></span>

