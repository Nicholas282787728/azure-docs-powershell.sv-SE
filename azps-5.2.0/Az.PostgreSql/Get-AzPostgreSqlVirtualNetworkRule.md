---
external help file: ''
Module Name: Az.PostgreSql
online version: https://docs.microsoft.com/en-us/powershell/module/az.postgresql/get-azpostgresqlvirtualnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Get-AzPostgreSqlVirtualNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Get-AzPostgreSqlVirtualNetworkRule.md
ms.openlocfilehash: eb8fc13bd2c1ef4e829cf5d4626453909b6ff773
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98410120"
---
# <span data-ttu-id="3f1d9-101">Get-AzPostgreSqlVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="3f1d9-101">Get-AzPostgreSqlVirtualNetworkRule</span></span>

## <span data-ttu-id="3f1d9-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="3f1d9-102">SYNOPSIS</span></span>
<span data-ttu-id="3f1d9-103">Hämtar en regel för ett virtuellt nätverk.</span><span class="sxs-lookup"><span data-stu-id="3f1d9-103">Gets a virtual network rule.</span></span>

## <span data-ttu-id="3f1d9-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="3f1d9-104">SYNTAX</span></span>

### <span data-ttu-id="3f1d9-105">Lista (standard)</span><span class="sxs-lookup"><span data-stu-id="3f1d9-105">List (Default)</span></span>
```
Get-AzPostgreSqlVirtualNetworkRule -ResourceGroupName <String> -ServerName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [-PassThru] [<CommonParameters>]
```

### <span data-ttu-id="3f1d9-106">Lära</span><span class="sxs-lookup"><span data-stu-id="3f1d9-106">Get</span></span>
```
Get-AzPostgreSqlVirtualNetworkRule -Name <String> -ResourceGroupName <String> -ServerName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [-PassThru] [<CommonParameters>]
```

### <span data-ttu-id="3f1d9-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="3f1d9-107">GetViaIdentity</span></span>
```
Get-AzPostgreSqlVirtualNetworkRule -InputObject <IPostgreSqlIdentity> [-DefaultProfile <PSObject>] [-PassThru]
 [<CommonParameters>]
```

## <span data-ttu-id="3f1d9-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="3f1d9-108">DESCRIPTION</span></span>
<span data-ttu-id="3f1d9-109">Hämtar en regel för ett virtuellt nätverk.</span><span class="sxs-lookup"><span data-stu-id="3f1d9-109">Gets a virtual network rule.</span></span>

## <span data-ttu-id="3f1d9-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="3f1d9-110">EXAMPLES</span></span>

### <span data-ttu-id="3f1d9-111">Exempel 1: visar alla virtuella nätverks regler i angiven PostgreSql-Server</span><span class="sxs-lookup"><span data-stu-id="3f1d9-111">Example 1: Lists all the Virtual Network Rules in specified PostgreSql server</span></span>
```powershell
PS C:\> Get-AzPostgreSqlVirtualNetworkRule -ResourceGroupName PostgreSqlTestRG -ServerName PostgreSqlTestServer 

Name Type
---- ----
vnet Microsoft.DBforPostgreSQL/servers/virtualNetworkRules
```

<span data-ttu-id="3f1d9-112">Denna cmdlet visar alla virtuella nätverks regler i angiven PostgreSql-Server.</span><span class="sxs-lookup"><span data-stu-id="3f1d9-112">This cmdlet lists all the Virtual Network Rules in specified PostgreSql server.</span></span>

### <span data-ttu-id="3f1d9-113">Exempel 2: Hämta regel för virtuell nätverks trafik efter namn</span><span class="sxs-lookup"><span data-stu-id="3f1d9-113">Example 2: Get Virtual Network Rule by name</span></span>
```powershell
PS C:\> Get-AzPostgreSqlVirtualNetworkRule -Name vnet -ResourceGroupName PostgreSqlTestRG -ServerName PostgreSqlTestServer

Name Type
---- ----
vnet Microsoft.DBforPostgreSQL/servers/virtualNetworkRules
```

<span data-ttu-id="3f1d9-114">Denna cmdlet hämtar regeln för virtuell nätverks trafik efter namn.</span><span class="sxs-lookup"><span data-stu-id="3f1d9-114">This cmdlet gets Virtual Network Rule by name.</span></span>

### <span data-ttu-id="3f1d9-115">Exempel 3: Hämta regel för virtuella nätverk efter identitet</span><span class="sxs-lookup"><span data-stu-id="3f1d9-115">Example 3: Get Virtual Network Rule by identity</span></span>
```powershell
PS C:\> $ID = "/subscriptions/<SubscriptionId>/resourceGroups/PostgreSqlTestRG/providers/Microsoft.DBforPostgreSQL/servers/PostgreSqlTestServer/virtualNetworkRules/vnet"
PS C:\> Get-AzPostgreSqlVirtualNetworkRule -InputObject $ID

Name Type
---- ----
vnet Microsoft.DBforPostgreSQL/servers/virtualNetworkRules
```

<span data-ttu-id="3f1d9-116">Denna cmdlet hämtar regeln för virtuell nätverks trafik efter identitet.</span><span class="sxs-lookup"><span data-stu-id="3f1d9-116">This cmdlet gets Virtual Network Rule by identity.</span></span>

## <span data-ttu-id="3f1d9-117">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="3f1d9-117">PARAMETERS</span></span>

### <span data-ttu-id="3f1d9-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3f1d9-118">-DefaultProfile</span></span>
<span data-ttu-id="3f1d9-119">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="3f1d9-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3f1d9-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3f1d9-120">-InputObject</span></span>
<span data-ttu-id="3f1d9-121">Identitets parameter för att konstruera, se avsnittet anteckningar för INPUTOBJECT-egenskaper och skapa en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="3f1d9-121">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="3f1d9-122">-Namn</span><span class="sxs-lookup"><span data-stu-id="3f1d9-122">-Name</span></span>
<span data-ttu-id="3f1d9-123">Namnet på den virtuella nätverks regeln.</span><span class="sxs-lookup"><span data-stu-id="3f1d9-123">The name of the virtual network rule.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: VirtualNetworkRuleName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3f1d9-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="3f1d9-124">-PassThru</span></span>
<span data-ttu-id="3f1d9-125">Returnerar true när kommandot lyckas</span><span class="sxs-lookup"><span data-stu-id="3f1d9-125">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="3f1d9-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3f1d9-126">-ResourceGroupName</span></span>
<span data-ttu-id="3f1d9-127">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="3f1d9-127">The name of the resource group.</span></span>
<span data-ttu-id="3f1d9-128">Namnet är Skift läges okänsligt.</span><span class="sxs-lookup"><span data-stu-id="3f1d9-128">The name is case insensitive.</span></span>

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

### <span data-ttu-id="3f1d9-129">-ServerName</span><span class="sxs-lookup"><span data-stu-id="3f1d9-129">-ServerName</span></span>
<span data-ttu-id="3f1d9-130">Namnet på servern.</span><span class="sxs-lookup"><span data-stu-id="3f1d9-130">The name of the server.</span></span>

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

### <span data-ttu-id="3f1d9-131">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="3f1d9-131">-SubscriptionId</span></span>
<span data-ttu-id="3f1d9-132">ID för mål prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="3f1d9-132">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="3f1d9-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3f1d9-133">CommonParameters</span></span>
<span data-ttu-id="3f1d9-134">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3f1d9-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3f1d9-135">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3f1d9-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3f1d9-136">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="3f1d9-136">INPUTS</span></span>

### <span data-ttu-id="3f1d9-137">Microsoft. Azure. PowerShell. cmdletar. PostgreSql. Models. IPostgreSqlIdentity</span><span class="sxs-lookup"><span data-stu-id="3f1d9-137">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.IPostgreSqlIdentity</span></span>

## <span data-ttu-id="3f1d9-138">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="3f1d9-138">OUTPUTS</span></span>

### <span data-ttu-id="3f1d9-139">Microsoft. Azure. PowerShell. cmdletar. PostgreSql. Models. Api20171201. IVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="3f1d9-139">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.Api20171201.IVirtualNetworkRule</span></span>

## <span data-ttu-id="3f1d9-140">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="3f1d9-140">NOTES</span></span>

<span data-ttu-id="3f1d9-141">ALIAS</span><span class="sxs-lookup"><span data-stu-id="3f1d9-141">ALIASES</span></span>

<span data-ttu-id="3f1d9-142">KOMPLEXA PARAMETER EGENSKAPER</span><span class="sxs-lookup"><span data-stu-id="3f1d9-142">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="3f1d9-143">Skapa en hash-tabell som innehåller lämpliga egenskaper för att lägga till de parametrar som beskrivs nedan.</span><span class="sxs-lookup"><span data-stu-id="3f1d9-143">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="3f1d9-144">Om du vill ha information om hash-tabeller kör Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="3f1d9-144">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="3f1d9-145">INPUTOBJECT <IPostgreSqlIdentity> : identitets parameter</span><span class="sxs-lookup"><span data-stu-id="3f1d9-145">INPUTOBJECT <IPostgreSqlIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="3f1d9-146">`[ConfigurationName <String>]`: Server konfigurationens namn.</span><span class="sxs-lookup"><span data-stu-id="3f1d9-146">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="3f1d9-147">`[DatabaseName <String>]`: Namnet på databasen.</span><span class="sxs-lookup"><span data-stu-id="3f1d9-147">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="3f1d9-148">`[FirewallRuleName <String>]`: Namnet på Server brand Väggs regeln.</span><span class="sxs-lookup"><span data-stu-id="3f1d9-148">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="3f1d9-149">`[Id <String>]`: Sökväg till resurs identitet</span><span class="sxs-lookup"><span data-stu-id="3f1d9-149">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="3f1d9-150">`[LocationName <String>]`: Namnet på platsen.</span><span class="sxs-lookup"><span data-stu-id="3f1d9-150">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="3f1d9-151">`[ResourceGroupName <String>]`: Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="3f1d9-151">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="3f1d9-152">Namnet är Skift läges okänsligt.</span><span class="sxs-lookup"><span data-stu-id="3f1d9-152">The name is case insensitive.</span></span>
  - <span data-ttu-id="3f1d9-153">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: Namnet på säkerhets varnings principen.</span><span class="sxs-lookup"><span data-stu-id="3f1d9-153">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="3f1d9-154">`[ServerName <String>]`: Namnet på servern.</span><span class="sxs-lookup"><span data-stu-id="3f1d9-154">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="3f1d9-155">`[SubscriptionId <String>]`: Mål prenumerationens ID.</span><span class="sxs-lookup"><span data-stu-id="3f1d9-155">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="3f1d9-156">`[VirtualNetworkRuleName <String>]`: Namnet på den virtuella nätverks regeln.</span><span class="sxs-lookup"><span data-stu-id="3f1d9-156">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="3f1d9-157">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="3f1d9-157">RELATED LINKS</span></span>

