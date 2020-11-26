---
external help file: ''
Module Name: Az.PostgreSql
online version: https://docs.microsoft.com/en-us/powershell/module/az.postgresql/update-azpostgresqlvirtualnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Update-AzPostgreSqlVirtualNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Update-AzPostgreSqlVirtualNetworkRule.md
ms.openlocfilehash: a430247083e84b3d35f820b3c1e2d5f04f4979b5
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94271727"
---
# <span data-ttu-id="7cf66-101">Update-AzPostgreSqlVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="7cf66-101">Update-AzPostgreSqlVirtualNetworkRule</span></span>

## <span data-ttu-id="7cf66-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="7cf66-102">SYNOPSIS</span></span>
<span data-ttu-id="7cf66-103">Skapar eller uppdaterar en befintlig virtuell nätverks regel.</span><span class="sxs-lookup"><span data-stu-id="7cf66-103">Creates or updates an existing virtual network rule.</span></span>

## <span data-ttu-id="7cf66-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="7cf66-104">SYNTAX</span></span>

### <span data-ttu-id="7cf66-105">UpdateExpanded (standard)</span><span class="sxs-lookup"><span data-stu-id="7cf66-105">UpdateExpanded (Default)</span></span>
```
Update-AzPostgreSqlVirtualNetworkRule -Name <String> -ResourceGroupName <String> -ServerName <String>
 -SubnetId <String> [-SubscriptionId <String>] [-IgnoreMissingVnetServiceEndpoint]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="7cf66-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="7cf66-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzPostgreSqlVirtualNetworkRule -InputObject <IPostgreSqlIdentity> -SubnetId <String>
 [-IgnoreMissingVnetServiceEndpoint] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="7cf66-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="7cf66-107">DESCRIPTION</span></span>
<span data-ttu-id="7cf66-108">Skapar eller uppdaterar en befintlig virtuell nätverks regel.</span><span class="sxs-lookup"><span data-stu-id="7cf66-108">Creates or updates an existing virtual network rule.</span></span>

## <span data-ttu-id="7cf66-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="7cf66-109">EXAMPLES</span></span>

### <span data-ttu-id="7cf66-110">Exempel 1: uppdatera PostgreSql för virtuella nätverk efter namn</span><span class="sxs-lookup"><span data-stu-id="7cf66-110">Example 1: Update PostgreSql Virtual Network Rule by name</span></span>
```powershell
PS C:\> $ID = "/subscriptions/<SubscriptionId>/resourceGroups/PostgreSqlTestRG/providers/Microsoft.Network/virtualNetworks/PostgreSqlVNet/subnets/default2"
PS C:\> Update-AzPostgreSqlVirtualNetworkRule -Name vnet -ResourceGroupName PostgreSqlTestRG -ServerName PostgreSqlTestServer -SubnetId $ID

Name Type
---- ----
vnet Microsoft.DBforPostgreSQL/servers/virtualNetworkRules
```

<span data-ttu-id="7cf66-111">Denna cmdlet uppdaterar PostgreSql för ett namn.</span><span class="sxs-lookup"><span data-stu-id="7cf66-111">This cmdlet updates PostgreSql Virtual Network Rule by name.</span></span>

### <span data-ttu-id="7cf66-112">Exempel 2: uppdatera PostgreSql regel för virtuell nätverks trafik efter identitet.</span><span class="sxs-lookup"><span data-stu-id="7cf66-112">Example 2: Update PostgreSql Virtual Network Rule by identity.</span></span>
```powershell
PS C:\> $SubnetID = "/subscriptions/<SubscriptionId>/resourceGroups/PostgreSqlTestRG/providers/Microsoft.Network/virtualNetworks/PostgreSqlVNet/subnets/default"
PS C:\> $VNetID = "/subscriptions/<SubscriptionId>/resourceGroups/PostgreSqlTestRG/providers/Microsoft.DBforPostgreSQL/servers/PostgreSqlTestServer/virtualNetworkRules/vnet"
PS C:\> Update-AzPostgreSqlVirtualNetworkRule -InputObject $VNetID -SubnetId $SubnetID

Name Type
---- ----
vnet Microsoft.DBforPostgreSQL/servers/virtualNetworkRules
```

<span data-ttu-id="7cf66-113">Dessa cmdletar uppdaterar PostgreSql för en identitet.</span><span class="sxs-lookup"><span data-stu-id="7cf66-113">These cmdlets update PostgreSql Virtual Network Rule by identity.</span></span>

## <span data-ttu-id="7cf66-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="7cf66-114">PARAMETERS</span></span>

### <span data-ttu-id="7cf66-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="7cf66-115">-AsJob</span></span>
<span data-ttu-id="7cf66-116">Köra kommandot som ett jobb</span><span class="sxs-lookup"><span data-stu-id="7cf66-116">Run the command as a job</span></span>

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

### <span data-ttu-id="7cf66-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7cf66-117">-DefaultProfile</span></span>
<span data-ttu-id="7cf66-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="7cf66-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7cf66-119">-IgnoreMissingVnetServiceEndpoint</span><span class="sxs-lookup"><span data-stu-id="7cf66-119">-IgnoreMissingVnetServiceEndpoint</span></span>
<span data-ttu-id="7cf66-120">Skapa brand Väggs regel innan slut punkts tjänst för virtuellt nätverk har Aktiver ATS för tjänsten.</span><span class="sxs-lookup"><span data-stu-id="7cf66-120">Create firewall rule before the virtual network has vnet service endpoint enabled.</span></span>

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

### <span data-ttu-id="7cf66-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7cf66-121">-InputObject</span></span>
<span data-ttu-id="7cf66-122">Identitets parameter för att konstruera, se avsnittet anteckningar för INPUTOBJECT-egenskaper och skapa en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="7cf66-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.IPostgreSqlIdentity
Parameter Sets: UpdateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7cf66-123">-Namn</span><span class="sxs-lookup"><span data-stu-id="7cf66-123">-Name</span></span>
<span data-ttu-id="7cf66-124">Namnet på den virtuella nätverks regeln.</span><span class="sxs-lookup"><span data-stu-id="7cf66-124">The name of the virtual network rule.</span></span>

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

### <span data-ttu-id="7cf66-125">-Nowait</span><span class="sxs-lookup"><span data-stu-id="7cf66-125">-NoWait</span></span>
<span data-ttu-id="7cf66-126">Kör kommandot asynkront</span><span class="sxs-lookup"><span data-stu-id="7cf66-126">Run the command asynchronously</span></span>

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

### <span data-ttu-id="7cf66-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="7cf66-127">-PassThru</span></span>
<span data-ttu-id="7cf66-128">Returnerar true när kommandot lyckas</span><span class="sxs-lookup"><span data-stu-id="7cf66-128">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="7cf66-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7cf66-129">-ResourceGroupName</span></span>
<span data-ttu-id="7cf66-130">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="7cf66-130">The name of the resource group.</span></span>
<span data-ttu-id="7cf66-131">Namnet är Skift läges okänsligt.</span><span class="sxs-lookup"><span data-stu-id="7cf66-131">The name is case insensitive.</span></span>

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

### <span data-ttu-id="7cf66-132">-ServerName</span><span class="sxs-lookup"><span data-stu-id="7cf66-132">-ServerName</span></span>
<span data-ttu-id="7cf66-133">Namnet på servern.</span><span class="sxs-lookup"><span data-stu-id="7cf66-133">The name of the server.</span></span>

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

### <span data-ttu-id="7cf66-134">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="7cf66-134">-SubnetId</span></span>
<span data-ttu-id="7cf66-135">ARM-resurs-ID för det virtuella nätverkets undernät.</span><span class="sxs-lookup"><span data-stu-id="7cf66-135">The ARM resource id of the virtual network subnet.</span></span>

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

### <span data-ttu-id="7cf66-136">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="7cf66-136">-SubscriptionId</span></span>
<span data-ttu-id="7cf66-137">ID för mål prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="7cf66-137">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="7cf66-138">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="7cf66-138">-Confirm</span></span>
<span data-ttu-id="7cf66-139">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="7cf66-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7cf66-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7cf66-140">-WhatIf</span></span>
<span data-ttu-id="7cf66-141">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="7cf66-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7cf66-142">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="7cf66-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7cf66-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7cf66-143">CommonParameters</span></span>
<span data-ttu-id="7cf66-144">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7cf66-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7cf66-145">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="7cf66-145">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7cf66-146">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="7cf66-146">INPUTS</span></span>

### <span data-ttu-id="7cf66-147">Microsoft. Azure. PowerShell. cmdletar. PostgreSql. Models. IPostgreSqlIdentity</span><span class="sxs-lookup"><span data-stu-id="7cf66-147">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.IPostgreSqlIdentity</span></span>

## <span data-ttu-id="7cf66-148">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="7cf66-148">OUTPUTS</span></span>

### <span data-ttu-id="7cf66-149">Microsoft. Azure. PowerShell. cmdletar. PostgreSql. Models. Api20171201. IVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="7cf66-149">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.Api20171201.IVirtualNetworkRule</span></span>

## <span data-ttu-id="7cf66-150">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="7cf66-150">NOTES</span></span>

<span data-ttu-id="7cf66-151">ALIAS</span><span class="sxs-lookup"><span data-stu-id="7cf66-151">ALIASES</span></span>

<span data-ttu-id="7cf66-152">KOMPLEXA PARAMETER EGENSKAPER</span><span class="sxs-lookup"><span data-stu-id="7cf66-152">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="7cf66-153">Skapa en hash-tabell som innehåller lämpliga egenskaper för att lägga till de parametrar som beskrivs nedan.</span><span class="sxs-lookup"><span data-stu-id="7cf66-153">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="7cf66-154">Om du vill ha information om hash-tabeller kör Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="7cf66-154">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="7cf66-155">INPUTOBJECT <IPostgreSqlIdentity> : identitets parameter</span><span class="sxs-lookup"><span data-stu-id="7cf66-155">INPUTOBJECT <IPostgreSqlIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="7cf66-156">`[ConfigurationName <String>]`: Server konfigurationens namn.</span><span class="sxs-lookup"><span data-stu-id="7cf66-156">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="7cf66-157">`[DatabaseName <String>]`: Namnet på databasen.</span><span class="sxs-lookup"><span data-stu-id="7cf66-157">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="7cf66-158">`[FirewallRuleName <String>]`: Namnet på Server brand Väggs regeln.</span><span class="sxs-lookup"><span data-stu-id="7cf66-158">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="7cf66-159">`[Id <String>]`: Sökväg till resurs identitet</span><span class="sxs-lookup"><span data-stu-id="7cf66-159">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="7cf66-160">`[LocationName <String>]`: Namnet på platsen.</span><span class="sxs-lookup"><span data-stu-id="7cf66-160">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="7cf66-161">`[ResourceGroupName <String>]`: Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="7cf66-161">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="7cf66-162">Namnet är Skift läges okänsligt.</span><span class="sxs-lookup"><span data-stu-id="7cf66-162">The name is case insensitive.</span></span>
  - <span data-ttu-id="7cf66-163">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: Namnet på säkerhets varnings principen.</span><span class="sxs-lookup"><span data-stu-id="7cf66-163">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="7cf66-164">`[ServerName <String>]`: Namnet på servern.</span><span class="sxs-lookup"><span data-stu-id="7cf66-164">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="7cf66-165">`[SubscriptionId <String>]`: Mål prenumerationens ID.</span><span class="sxs-lookup"><span data-stu-id="7cf66-165">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="7cf66-166">`[VirtualNetworkRuleName <String>]`: Namnet på den virtuella nätverks regeln.</span><span class="sxs-lookup"><span data-stu-id="7cf66-166">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="7cf66-167">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="7cf66-167">RELATED LINKS</span></span>
