---
external help file: ''
Module Name: Az.MySql
online version: https://docs.microsoft.com/en-us/powershell/module/az.mysql/get-azmysqlvirtualnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Get-AzMySqlVirtualNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Get-AzMySqlVirtualNetworkRule.md
ms.openlocfilehash: 91d774931ac7ef4b8f1d41a70953d4a5b3a322cb
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94270920"
---
# <span data-ttu-id="5a566-101">Get-AzMySqlVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="5a566-101">Get-AzMySqlVirtualNetworkRule</span></span>

## <span data-ttu-id="5a566-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="5a566-102">SYNOPSIS</span></span>
<span data-ttu-id="5a566-103">Hämtar en regel för ett virtuellt nätverk.</span><span class="sxs-lookup"><span data-stu-id="5a566-103">Gets a virtual network rule.</span></span>

## <span data-ttu-id="5a566-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="5a566-104">SYNTAX</span></span>

### <span data-ttu-id="5a566-105">Lista (standard)</span><span class="sxs-lookup"><span data-stu-id="5a566-105">List (Default)</span></span>
```
Get-AzMySqlVirtualNetworkRule -ResourceGroupName <String> -ServerName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [-PassThru] [<CommonParameters>]
```

### <span data-ttu-id="5a566-106">Lära</span><span class="sxs-lookup"><span data-stu-id="5a566-106">Get</span></span>
```
Get-AzMySqlVirtualNetworkRule -Name <String> -ResourceGroupName <String> -ServerName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [-PassThru] [<CommonParameters>]
```

### <span data-ttu-id="5a566-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="5a566-107">GetViaIdentity</span></span>
```
Get-AzMySqlVirtualNetworkRule -InputObject <IMySqlIdentity> [-DefaultProfile <PSObject>] [-PassThru]
 [<CommonParameters>]
```

## <span data-ttu-id="5a566-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="5a566-108">DESCRIPTION</span></span>
<span data-ttu-id="5a566-109">Hämtar en regel för ett virtuellt nätverk.</span><span class="sxs-lookup"><span data-stu-id="5a566-109">Gets a virtual network rule.</span></span>

## <span data-ttu-id="5a566-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="5a566-110">EXAMPLES</span></span>

### <span data-ttu-id="5a566-111">Exempel 1: visar alla virtuella nätverks regler i angiven MySql-Server</span><span class="sxs-lookup"><span data-stu-id="5a566-111">Example 1: Lists all the Virtual Network Rules in specified MySql server</span></span>
```powershell
PS C:\> Get-AzMySqlVirtualNetworkRule -ResourceGroupName PowershellMySqlTest -ServerName mysql-test

Name Type
---- ----
vnet Microsoft.DBforMySQL/servers/virtualNetworkRules
```

<span data-ttu-id="5a566-112">Denna cmdlet visar alla virtuella nätverks regler i angiven MySql-Server.</span><span class="sxs-lookup"><span data-stu-id="5a566-112">This cmdlet lists all the Virtual Network Rules in specified MySql server.</span></span>

### <span data-ttu-id="5a566-113">Exempel 2: Hämta regel för virtuell nätverks trafik efter namn</span><span class="sxs-lookup"><span data-stu-id="5a566-113">Example 2: Get Virtual Network Rule by name</span></span>
```powershell
PS C:\> Get-AzMySqlVirtualNetworkRule -Name vnet -ResourceGroupName PowershellMySqlTest -ServerName mysql-test

Name Type
---- ----
vnet Microsoft.DBforMySQL/servers/virtualNetworkRules
```

<span data-ttu-id="5a566-114">Denna cmdlet hämtar regeln för virtuell nätverks trafik efter namn.</span><span class="sxs-lookup"><span data-stu-id="5a566-114">This cmdlet gets Virtual Network Rule by name.</span></span>

### <span data-ttu-id="5a566-115">Exempel 3: Hämta regel för virtuella nätverk efter identitet</span><span class="sxs-lookup"><span data-stu-id="5a566-115">Example 3: Get Virtual Network Rule by identity</span></span>
```powershell
PS C:\> $ID = "/subscriptions/<SubscriptionId>/resourceGroups/PowershellMySqlTest/providers/Microsoft.DBforMySQL/servers/mysql-test/virtualNetworkRules/vnet"
PS C:\> Get-AzMySqlVirtualNetworkRule -InputObject $ID

Name Type
---- ----
vnet Microsoft.DBforMySQL/servers/virtualNetworkRules
```

<span data-ttu-id="5a566-116">Denna cmdlet hämtar regeln för virtuell nätverks trafik efter identitet.</span><span class="sxs-lookup"><span data-stu-id="5a566-116">This cmdlet gets Virtual Network Rule by identity.</span></span>

## <span data-ttu-id="5a566-117">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="5a566-117">PARAMETERS</span></span>

### <span data-ttu-id="5a566-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5a566-118">-DefaultProfile</span></span>
<span data-ttu-id="5a566-119">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="5a566-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5a566-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5a566-120">-InputObject</span></span>
<span data-ttu-id="5a566-121">Identitets parameter för att konstruera, se avsnittet anteckningar för INPUTOBJECT-egenskaper och skapa en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="5a566-121">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="5a566-122">-Namn</span><span class="sxs-lookup"><span data-stu-id="5a566-122">-Name</span></span>
<span data-ttu-id="5a566-123">Namnet på den virtuella nätverks regeln.</span><span class="sxs-lookup"><span data-stu-id="5a566-123">The name of the virtual network rule.</span></span>

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

### <span data-ttu-id="5a566-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="5a566-124">-PassThru</span></span>
<span data-ttu-id="5a566-125">Returnerar true när kommandot lyckas</span><span class="sxs-lookup"><span data-stu-id="5a566-125">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="5a566-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5a566-126">-ResourceGroupName</span></span>
<span data-ttu-id="5a566-127">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="5a566-127">The name of the resource group.</span></span>
<span data-ttu-id="5a566-128">Namnet är Skift läges okänsligt.</span><span class="sxs-lookup"><span data-stu-id="5a566-128">The name is case insensitive.</span></span>

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

### <span data-ttu-id="5a566-129">-ServerName</span><span class="sxs-lookup"><span data-stu-id="5a566-129">-ServerName</span></span>
<span data-ttu-id="5a566-130">Namnet på servern.</span><span class="sxs-lookup"><span data-stu-id="5a566-130">The name of the server.</span></span>

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

### <span data-ttu-id="5a566-131">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="5a566-131">-SubscriptionId</span></span>
<span data-ttu-id="5a566-132">ID för mål prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="5a566-132">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="5a566-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5a566-133">CommonParameters</span></span>
<span data-ttu-id="5a566-134">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5a566-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5a566-135">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="5a566-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5a566-136">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="5a566-136">INPUTS</span></span>

### <span data-ttu-id="5a566-137">Microsoft. Azure. PowerShell. cmdletar. MySql. Models. IMySqlIdentity</span><span class="sxs-lookup"><span data-stu-id="5a566-137">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity</span></span>

## <span data-ttu-id="5a566-138">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="5a566-138">OUTPUTS</span></span>

### <span data-ttu-id="5a566-139">Microsoft. Azure. PowerShell. cmdletar. MySql. Models. Api20171201. IVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="5a566-139">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20171201.IVirtualNetworkRule</span></span>

## <span data-ttu-id="5a566-140">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="5a566-140">NOTES</span></span>

<span data-ttu-id="5a566-141">ALIAS</span><span class="sxs-lookup"><span data-stu-id="5a566-141">ALIASES</span></span>

<span data-ttu-id="5a566-142">KOMPLEXA PARAMETER EGENSKAPER</span><span class="sxs-lookup"><span data-stu-id="5a566-142">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="5a566-143">Skapa en hash-tabell som innehåller lämpliga egenskaper för att lägga till de parametrar som beskrivs nedan.</span><span class="sxs-lookup"><span data-stu-id="5a566-143">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="5a566-144">Om du vill ha information om hash-tabeller kör Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="5a566-144">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="5a566-145">INPUTOBJECT <IMySqlIdentity> : identitets parameter</span><span class="sxs-lookup"><span data-stu-id="5a566-145">INPUTOBJECT <IMySqlIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="5a566-146">`[ConfigurationName <String>]`: Server konfigurationens namn.</span><span class="sxs-lookup"><span data-stu-id="5a566-146">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="5a566-147">`[DatabaseName <String>]`: Namnet på databasen.</span><span class="sxs-lookup"><span data-stu-id="5a566-147">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="5a566-148">`[FirewallRuleName <String>]`: Namnet på Server brand Väggs regeln.</span><span class="sxs-lookup"><span data-stu-id="5a566-148">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="5a566-149">`[Id <String>]`: Sökväg till resurs identitet</span><span class="sxs-lookup"><span data-stu-id="5a566-149">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="5a566-150">`[LocationName <String>]`: Namnet på platsen.</span><span class="sxs-lookup"><span data-stu-id="5a566-150">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="5a566-151">`[ResourceGroupName <String>]`: Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="5a566-151">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="5a566-152">Namnet är Skift läges okänsligt.</span><span class="sxs-lookup"><span data-stu-id="5a566-152">The name is case insensitive.</span></span>
  - <span data-ttu-id="5a566-153">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: Namnet på säkerhets varnings principen.</span><span class="sxs-lookup"><span data-stu-id="5a566-153">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="5a566-154">`[ServerName <String>]`: Namnet på servern.</span><span class="sxs-lookup"><span data-stu-id="5a566-154">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="5a566-155">`[SubscriptionId <String>]`: Mål prenumerationens ID.</span><span class="sxs-lookup"><span data-stu-id="5a566-155">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="5a566-156">`[VirtualNetworkRuleName <String>]`: Namnet på den virtuella nätverks regeln.</span><span class="sxs-lookup"><span data-stu-id="5a566-156">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="5a566-157">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="5a566-157">RELATED LINKS</span></span>

