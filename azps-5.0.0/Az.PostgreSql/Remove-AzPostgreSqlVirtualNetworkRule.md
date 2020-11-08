---
external help file: ''
Module Name: Az.PostgreSql
online version: https://docs.microsoft.com/en-us/powershell/module/az.postgresql/remove-azpostgresqlvirtualnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Remove-AzPostgreSqlVirtualNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Remove-AzPostgreSqlVirtualNetworkRule.md
ms.openlocfilehash: bacd5e1636457fac172cd54c9fcf4407247d88ba
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94270796"
---
# <span data-ttu-id="7df3a-101">Remove-AzPostgreSqlVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="7df3a-101">Remove-AzPostgreSqlVirtualNetworkRule</span></span>

## <span data-ttu-id="7df3a-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="7df3a-102">SYNOPSIS</span></span>
<span data-ttu-id="7df3a-103">Tar bort regeln för virtuella nätverk med det angivna namnet.</span><span class="sxs-lookup"><span data-stu-id="7df3a-103">Deletes the virtual network rule with the given name.</span></span>

## <span data-ttu-id="7df3a-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="7df3a-104">SYNTAX</span></span>

### <span data-ttu-id="7df3a-105">Ta bort (standard)</span><span class="sxs-lookup"><span data-stu-id="7df3a-105">Delete (Default)</span></span>
```
Remove-AzPostgreSqlVirtualNetworkRule -Name <String> -ResourceGroupName <String> -ServerName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="7df3a-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="7df3a-106">DeleteViaIdentity</span></span>
```
Remove-AzPostgreSqlVirtualNetworkRule -InputObject <IPostgreSqlIdentity> [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="7df3a-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="7df3a-107">DESCRIPTION</span></span>
<span data-ttu-id="7df3a-108">Tar bort regeln för virtuella nätverk med det angivna namnet.</span><span class="sxs-lookup"><span data-stu-id="7df3a-108">Deletes the virtual network rule with the given name.</span></span>

## <span data-ttu-id="7df3a-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="7df3a-109">EXAMPLES</span></span>

### <span data-ttu-id="7df3a-110">Exempel 1: ta bort PostgreSql Server-regel per namn</span><span class="sxs-lookup"><span data-stu-id="7df3a-110">Example 1: Remove PostgreSql server Virtual Network Rule by name</span></span>
```powershell
PS C:\> Remove-AzPostgreSqlVirtualNetworkRule -Name vnet -ResourceGroupName PostgreSqlTestRG -ServerName PostgreSqlTestServer

```

<span data-ttu-id="7df3a-111">Denna cmdlet tar bort PostgreSql Server-regel efter namn.</span><span class="sxs-lookup"><span data-stu-id="7df3a-111">This cmdlet removes PostgreSql server Virtual Network Rule by name.</span></span>

### <span data-ttu-id="7df3a-112">Exempel 2: ta bort PostgreSql Server-regel efter identitet</span><span class="sxs-lookup"><span data-stu-id="7df3a-112">Example 2: Remove PostgreSql server Virtual Network Rule by identity</span></span>
```powershell
PS C:\> $ID = "/subscriptions/<SubscriptionId>/resourceGroups/PostgreSqlTestRG/providers/Microsoft.DBforPostgreSQL/servers/PostgreSqlTestServer/virtualNetworkRules/vnet"
PS C:\> Remove-AzPostgreSqlVirtualNetworkRule -InputObject $ID
 
```

<span data-ttu-id="7df3a-113">Dessa cmdletar tar bort PostgreSql Server-regel efter identitet.</span><span class="sxs-lookup"><span data-stu-id="7df3a-113">These cmdlets remove PostgreSql server Virtual Network Rule by identity.</span></span>

## <span data-ttu-id="7df3a-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="7df3a-114">PARAMETERS</span></span>

### <span data-ttu-id="7df3a-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="7df3a-115">-AsJob</span></span>
<span data-ttu-id="7df3a-116">Köra kommandot som ett jobb</span><span class="sxs-lookup"><span data-stu-id="7df3a-116">Run the command as a job</span></span>

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

### <span data-ttu-id="7df3a-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7df3a-117">-DefaultProfile</span></span>
<span data-ttu-id="7df3a-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="7df3a-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7df3a-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7df3a-119">-InputObject</span></span>
<span data-ttu-id="7df3a-120">Identitets parameter för att konstruera, se avsnittet anteckningar för INPUTOBJECT-egenskaper och skapa en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="7df3a-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.IPostgreSqlIdentity
Parameter Sets: DeleteViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7df3a-121">-Namn</span><span class="sxs-lookup"><span data-stu-id="7df3a-121">-Name</span></span>
<span data-ttu-id="7df3a-122">Namnet på den virtuella nätverks regeln.</span><span class="sxs-lookup"><span data-stu-id="7df3a-122">The name of the virtual network rule.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases: VirtualNetworkRuleName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7df3a-123">-Nowait</span><span class="sxs-lookup"><span data-stu-id="7df3a-123">-NoWait</span></span>
<span data-ttu-id="7df3a-124">Kör kommandot asynkront</span><span class="sxs-lookup"><span data-stu-id="7df3a-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="7df3a-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="7df3a-125">-PassThru</span></span>
<span data-ttu-id="7df3a-126">Returnerar true när kommandot lyckas</span><span class="sxs-lookup"><span data-stu-id="7df3a-126">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="7df3a-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7df3a-127">-ResourceGroupName</span></span>
<span data-ttu-id="7df3a-128">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="7df3a-128">The name of the resource group.</span></span>
<span data-ttu-id="7df3a-129">Namnet är Skift läges okänsligt.</span><span class="sxs-lookup"><span data-stu-id="7df3a-129">The name is case insensitive.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7df3a-130">-ServerName</span><span class="sxs-lookup"><span data-stu-id="7df3a-130">-ServerName</span></span>
<span data-ttu-id="7df3a-131">Namnet på servern.</span><span class="sxs-lookup"><span data-stu-id="7df3a-131">The name of the server.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7df3a-132">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="7df3a-132">-SubscriptionId</span></span>
<span data-ttu-id="7df3a-133">ID för mål prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="7df3a-133">The ID of the target subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7df3a-134">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="7df3a-134">-Confirm</span></span>
<span data-ttu-id="7df3a-135">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="7df3a-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7df3a-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7df3a-136">-WhatIf</span></span>
<span data-ttu-id="7df3a-137">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="7df3a-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7df3a-138">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="7df3a-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7df3a-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7df3a-139">CommonParameters</span></span>
<span data-ttu-id="7df3a-140">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7df3a-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7df3a-141">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="7df3a-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7df3a-142">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="7df3a-142">INPUTS</span></span>

### <span data-ttu-id="7df3a-143">Microsoft. Azure. PowerShell. cmdletar. PostgreSql. Models. IPostgreSqlIdentity</span><span class="sxs-lookup"><span data-stu-id="7df3a-143">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.IPostgreSqlIdentity</span></span>

## <span data-ttu-id="7df3a-144">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="7df3a-144">OUTPUTS</span></span>

### <span data-ttu-id="7df3a-145">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="7df3a-145">System.Boolean</span></span>

## <span data-ttu-id="7df3a-146">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="7df3a-146">NOTES</span></span>

<span data-ttu-id="7df3a-147">ALIAS</span><span class="sxs-lookup"><span data-stu-id="7df3a-147">ALIASES</span></span>

<span data-ttu-id="7df3a-148">KOMPLEXA PARAMETER EGENSKAPER</span><span class="sxs-lookup"><span data-stu-id="7df3a-148">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="7df3a-149">Skapa en hash-tabell som innehåller lämpliga egenskaper för att lägga till de parametrar som beskrivs nedan.</span><span class="sxs-lookup"><span data-stu-id="7df3a-149">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="7df3a-150">Om du vill ha information om hash-tabeller kör Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="7df3a-150">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="7df3a-151">INPUTOBJECT <IPostgreSqlIdentity> : identitets parameter</span><span class="sxs-lookup"><span data-stu-id="7df3a-151">INPUTOBJECT <IPostgreSqlIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="7df3a-152">`[ConfigurationName <String>]`: Server konfigurationens namn.</span><span class="sxs-lookup"><span data-stu-id="7df3a-152">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="7df3a-153">`[DatabaseName <String>]`: Namnet på databasen.</span><span class="sxs-lookup"><span data-stu-id="7df3a-153">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="7df3a-154">`[FirewallRuleName <String>]`: Namnet på Server brand Väggs regeln.</span><span class="sxs-lookup"><span data-stu-id="7df3a-154">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="7df3a-155">`[Id <String>]`: Sökväg till resurs identitet</span><span class="sxs-lookup"><span data-stu-id="7df3a-155">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="7df3a-156">`[LocationName <String>]`: Namnet på platsen.</span><span class="sxs-lookup"><span data-stu-id="7df3a-156">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="7df3a-157">`[ResourceGroupName <String>]`: Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="7df3a-157">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="7df3a-158">Namnet är Skift läges okänsligt.</span><span class="sxs-lookup"><span data-stu-id="7df3a-158">The name is case insensitive.</span></span>
  - <span data-ttu-id="7df3a-159">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: Namnet på säkerhets varnings principen.</span><span class="sxs-lookup"><span data-stu-id="7df3a-159">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="7df3a-160">`[ServerName <String>]`: Namnet på servern.</span><span class="sxs-lookup"><span data-stu-id="7df3a-160">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="7df3a-161">`[SubscriptionId <String>]`: Mål prenumerationens ID.</span><span class="sxs-lookup"><span data-stu-id="7df3a-161">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="7df3a-162">`[VirtualNetworkRuleName <String>]`: Namnet på den virtuella nätverks regeln.</span><span class="sxs-lookup"><span data-stu-id="7df3a-162">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="7df3a-163">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="7df3a-163">RELATED LINKS</span></span>

