---
external help file: ''
Module Name: Az.MySql
online version: https://docs.microsoft.com/en-us/powershell/module/az.mysql/update-azmysqlvirtualnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Update-AzMySqlVirtualNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Update-AzMySqlVirtualNetworkRule.md
ms.openlocfilehash: f98c24ab0be3b2c35ac43642fb9d4bbf0b421c7e
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94269804"
---
# <span data-ttu-id="d331b-101">Update-AzMySqlVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="d331b-101">Update-AzMySqlVirtualNetworkRule</span></span>

## <span data-ttu-id="d331b-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="d331b-102">SYNOPSIS</span></span>
<span data-ttu-id="d331b-103">Skapar eller uppdaterar en befintlig virtuell nätverks regel.</span><span class="sxs-lookup"><span data-stu-id="d331b-103">Creates or updates an existing virtual network rule.</span></span>

## <span data-ttu-id="d331b-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="d331b-104">SYNTAX</span></span>

### <span data-ttu-id="d331b-105">UpdateExpanded (standard)</span><span class="sxs-lookup"><span data-stu-id="d331b-105">UpdateExpanded (Default)</span></span>
```
Update-AzMySqlVirtualNetworkRule -Name <String> -ResourceGroupName <String> -ServerName <String>
 -SubnetId <String> [-SubscriptionId <String>] [-IgnoreMissingVnetServiceEndpoint]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="d331b-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="d331b-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzMySqlVirtualNetworkRule -InputObject <IMySqlIdentity> -SubnetId <String>
 [-IgnoreMissingVnetServiceEndpoint] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="d331b-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="d331b-107">DESCRIPTION</span></span>
<span data-ttu-id="d331b-108">Skapar eller uppdaterar en befintlig virtuell nätverks regel.</span><span class="sxs-lookup"><span data-stu-id="d331b-108">Creates or updates an existing virtual network rule.</span></span>

## <span data-ttu-id="d331b-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="d331b-109">EXAMPLES</span></span>

### <span data-ttu-id="d331b-110">Exempel 1: uppdatera MySql-regel per namn</span><span class="sxs-lookup"><span data-stu-id="d331b-110">Example 1: Update MySql Virtual Network Rule by name</span></span>
```powershell
PS C:\> $ID = "/subscriptions/<SubscriptionId>/resourceGroups/PowershellMySqlTest/providers/Microsoft.Network/virtualNetworks/MySqlVNet/subnets/MysqlSubnet2"
PS C:\> Update-AzMySqlVirtualNetworkRule -Name $env.VNetName -ResourceGroupName $env.resourceGroup -ServerName $env.serverName -SubnetId $ID

Name Type
---- ----
vnet Microsoft.DBforMySQL/servers/virtualNetworkRules
```

<span data-ttu-id="d331b-111">Denna cmdlet uppdaterar MySql-regel för virtuell nätverks trafik efter namn.</span><span class="sxs-lookup"><span data-stu-id="d331b-111">This cmdlet updates MySql Virtual Network Rule by name.</span></span>

### <span data-ttu-id="d331b-112">Exempel 2: uppdatera MySql-regel för virtuell nätverks trafik efter identitet.</span><span class="sxs-lookup"><span data-stu-id="d331b-112">Example 2: Update MySql Virtual Network Rule by identity.</span></span>
```powershell
PS C:\> $SubnetID = "/subscriptions/<SubscriptionId>/resourceGroups/PowershellMySqlTest/providers/Microsoft.Network/virtualNetworks/MySqlVNet/subnets/MysqlSubnet1"
PS C:\> $VNetID = "/subscriptions/<SubscriptionId>/resourceGroups/PowershellMySqlTest/providers/Microsoft.DBforMySQL/servers/mysql-test/virtualNetworkRules/vnet"
PS C:\> Update-AzMySqlVirtualNetworkRule -InputObject $VNetID -SubnetId $SubnetID

Name Type
---- ----
vnet Microsoft.DBforMySQL/servers/virtualNetworkRules
```

<span data-ttu-id="d331b-113">Dessa cmdletar uppdaterar MySql-regel för virtuell nätverks trafik efter identitet.</span><span class="sxs-lookup"><span data-stu-id="d331b-113">These cmdlets update MySql Virtual Network Rule by identity.</span></span>

## <span data-ttu-id="d331b-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="d331b-114">PARAMETERS</span></span>

### <span data-ttu-id="d331b-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d331b-115">-AsJob</span></span>
<span data-ttu-id="d331b-116">Köra kommandot som ett jobb</span><span class="sxs-lookup"><span data-stu-id="d331b-116">Run the command as a job</span></span>

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

### <span data-ttu-id="d331b-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d331b-117">-DefaultProfile</span></span>
<span data-ttu-id="d331b-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="d331b-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d331b-119">-IgnoreMissingVnetServiceEndpoint</span><span class="sxs-lookup"><span data-stu-id="d331b-119">-IgnoreMissingVnetServiceEndpoint</span></span>
<span data-ttu-id="d331b-120">Skapa brand Väggs regel innan slut punkts tjänst för virtuellt nätverk har Aktiver ATS för tjänsten.</span><span class="sxs-lookup"><span data-stu-id="d331b-120">Create firewall rule before the virtual network has vnet service endpoint enabled.</span></span>

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

### <span data-ttu-id="d331b-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d331b-121">-InputObject</span></span>
<span data-ttu-id="d331b-122">Identitets parameter för att konstruera, se avsnittet anteckningar för INPUTOBJECT-egenskaper och skapa en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="d331b-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity
Parameter Sets: UpdateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d331b-123">-Namn</span><span class="sxs-lookup"><span data-stu-id="d331b-123">-Name</span></span>
<span data-ttu-id="d331b-124">Namnet på den virtuella nätverks regeln.</span><span class="sxs-lookup"><span data-stu-id="d331b-124">The name of the virtual network rule.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases: VirtualNetworkRuleName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d331b-125">-Nowait</span><span class="sxs-lookup"><span data-stu-id="d331b-125">-NoWait</span></span>
<span data-ttu-id="d331b-126">Kör kommandot asynkront</span><span class="sxs-lookup"><span data-stu-id="d331b-126">Run the command asynchronously</span></span>

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

### <span data-ttu-id="d331b-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d331b-127">-PassThru</span></span>
<span data-ttu-id="d331b-128">Returnerar true när kommandot lyckas</span><span class="sxs-lookup"><span data-stu-id="d331b-128">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="d331b-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d331b-129">-ResourceGroupName</span></span>
<span data-ttu-id="d331b-130">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="d331b-130">The name of the resource group.</span></span>
<span data-ttu-id="d331b-131">Namnet är Skift läges okänsligt.</span><span class="sxs-lookup"><span data-stu-id="d331b-131">The name is case insensitive.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d331b-132">-ServerName</span><span class="sxs-lookup"><span data-stu-id="d331b-132">-ServerName</span></span>
<span data-ttu-id="d331b-133">Namnet på servern.</span><span class="sxs-lookup"><span data-stu-id="d331b-133">The name of the server.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d331b-134">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="d331b-134">-SubnetId</span></span>
<span data-ttu-id="d331b-135">ARM-resurs-ID för det virtuella nätverkets undernät.</span><span class="sxs-lookup"><span data-stu-id="d331b-135">The ARM resource id of the virtual network subnet.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d331b-136">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="d331b-136">-SubscriptionId</span></span>
<span data-ttu-id="d331b-137">ID för mål prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="d331b-137">The ID of the target subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d331b-138">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="d331b-138">-Confirm</span></span>
<span data-ttu-id="d331b-139">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="d331b-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d331b-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d331b-140">-WhatIf</span></span>
<span data-ttu-id="d331b-141">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="d331b-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d331b-142">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="d331b-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d331b-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d331b-143">CommonParameters</span></span>
<span data-ttu-id="d331b-144">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d331b-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d331b-145">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d331b-145">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d331b-146">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="d331b-146">INPUTS</span></span>

### <span data-ttu-id="d331b-147">Microsoft. Azure. PowerShell. cmdletar. MySql. Models. IMySqlIdentity</span><span class="sxs-lookup"><span data-stu-id="d331b-147">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity</span></span>

## <span data-ttu-id="d331b-148">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="d331b-148">OUTPUTS</span></span>

### <span data-ttu-id="d331b-149">Microsoft. Azure. PowerShell. cmdletar. MySql. Models. Api20171201. IVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="d331b-149">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20171201.IVirtualNetworkRule</span></span>

## <span data-ttu-id="d331b-150">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="d331b-150">NOTES</span></span>

<span data-ttu-id="d331b-151">ALIAS</span><span class="sxs-lookup"><span data-stu-id="d331b-151">ALIASES</span></span>

<span data-ttu-id="d331b-152">KOMPLEXA PARAMETER EGENSKAPER</span><span class="sxs-lookup"><span data-stu-id="d331b-152">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="d331b-153">Skapa en hash-tabell som innehåller lämpliga egenskaper för att lägga till de parametrar som beskrivs nedan.</span><span class="sxs-lookup"><span data-stu-id="d331b-153">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="d331b-154">Om du vill ha information om hash-tabeller kör Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="d331b-154">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="d331b-155">INPUTOBJECT <IMySqlIdentity> : identitets parameter</span><span class="sxs-lookup"><span data-stu-id="d331b-155">INPUTOBJECT <IMySqlIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="d331b-156">`[ConfigurationName <String>]`: Server konfigurationens namn.</span><span class="sxs-lookup"><span data-stu-id="d331b-156">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="d331b-157">`[DatabaseName <String>]`: Namnet på databasen.</span><span class="sxs-lookup"><span data-stu-id="d331b-157">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="d331b-158">`[FirewallRuleName <String>]`: Namnet på Server brand Väggs regeln.</span><span class="sxs-lookup"><span data-stu-id="d331b-158">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="d331b-159">`[Id <String>]`: Sökväg till resurs identitet</span><span class="sxs-lookup"><span data-stu-id="d331b-159">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="d331b-160">`[LocationName <String>]`: Namnet på platsen.</span><span class="sxs-lookup"><span data-stu-id="d331b-160">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="d331b-161">`[ResourceGroupName <String>]`: Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="d331b-161">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="d331b-162">Namnet är Skift läges okänsligt.</span><span class="sxs-lookup"><span data-stu-id="d331b-162">The name is case insensitive.</span></span>
  - <span data-ttu-id="d331b-163">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: Namnet på säkerhets varnings principen.</span><span class="sxs-lookup"><span data-stu-id="d331b-163">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="d331b-164">`[ServerName <String>]`: Namnet på servern.</span><span class="sxs-lookup"><span data-stu-id="d331b-164">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="d331b-165">`[SubscriptionId <String>]`: Mål prenumerationens ID.</span><span class="sxs-lookup"><span data-stu-id="d331b-165">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="d331b-166">`[VirtualNetworkRuleName <String>]`: Namnet på den virtuella nätverks regeln.</span><span class="sxs-lookup"><span data-stu-id="d331b-166">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="d331b-167">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="d331b-167">RELATED LINKS</span></span>

