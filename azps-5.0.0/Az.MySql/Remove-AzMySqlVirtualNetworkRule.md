---
external help file: ''
Module Name: Az.MySql
online version: https://docs.microsoft.com/en-us/powershell/module/az.mysql/remove-azmysqlvirtualnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Remove-AzMySqlVirtualNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Remove-AzMySqlVirtualNetworkRule.md
ms.openlocfilehash: 85690d3602744f6bde45a5f08b5a927124a8460a
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94319851"
---
# <span data-ttu-id="bce82-101">Remove-AzMySqlVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="bce82-101">Remove-AzMySqlVirtualNetworkRule</span></span>

## <span data-ttu-id="bce82-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="bce82-102">SYNOPSIS</span></span>
<span data-ttu-id="bce82-103">Tar bort regeln för virtuella nätverk med det angivna namnet.</span><span class="sxs-lookup"><span data-stu-id="bce82-103">Deletes the virtual network rule with the given name.</span></span>

## <span data-ttu-id="bce82-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="bce82-104">SYNTAX</span></span>

### <span data-ttu-id="bce82-105">Ta bort (standard)</span><span class="sxs-lookup"><span data-stu-id="bce82-105">Delete (Default)</span></span>
```
Remove-AzMySqlVirtualNetworkRule -Name <String> -ResourceGroupName <String> -ServerName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="bce82-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="bce82-106">DeleteViaIdentity</span></span>
```
Remove-AzMySqlVirtualNetworkRule -InputObject <IMySqlIdentity> [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="bce82-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="bce82-107">DESCRIPTION</span></span>
<span data-ttu-id="bce82-108">Tar bort regeln för virtuella nätverk med det angivna namnet.</span><span class="sxs-lookup"><span data-stu-id="bce82-108">Deletes the virtual network rule with the given name.</span></span>

## <span data-ttu-id="bce82-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="bce82-109">EXAMPLES</span></span>

### <span data-ttu-id="bce82-110">Exempel 1: ta bort den virtuella nätverks regeln för MySql server med namn</span><span class="sxs-lookup"><span data-stu-id="bce82-110">Example 1: Remove MySql server Virtual Network Rule by name</span></span>
```powershell
PS C:\> Remove-AzMySqlVirtualNetworkRule -Name vnet -ResourceGroupName PowershellMySqlTest-ServerName mysql-test

```

<span data-ttu-id="bce82-111">Denna cmdlet tar bort MySql Server-regeln per namn.</span><span class="sxs-lookup"><span data-stu-id="bce82-111">This cmdlet removes MySql server Virtual Network Rule by name.</span></span>

### <span data-ttu-id="bce82-112">Exempel 2: ta bort regeln för det virtuella nätverket för MySql-servern efter identitet</span><span class="sxs-lookup"><span data-stu-id="bce82-112">Example 2: Remove MySql server Virtual Network Rule by identity</span></span>
```powershell
PS C:\> $ID = "/subscriptions/<SubscriptionId>/resourceGroups/PowershellMySqlTest/providers/Microsoft.DBforMySQL/servers/mysql-test/virtualNetworkRules/vnet"
PS C:\> Remove-AzMySqlVirtualNetworkRule -InputObject $ID
 
```

<span data-ttu-id="bce82-113">De här cmdletarna tar bort regeln för det virtuella nätverket för MySql-servern efter identitet.</span><span class="sxs-lookup"><span data-stu-id="bce82-113">These cmdlets remove MySql server Virtual Network Rule by identity.</span></span>

## <span data-ttu-id="bce82-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="bce82-114">PARAMETERS</span></span>

### <span data-ttu-id="bce82-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="bce82-115">-AsJob</span></span>
<span data-ttu-id="bce82-116">Köra kommandot som ett jobb</span><span class="sxs-lookup"><span data-stu-id="bce82-116">Run the command as a job</span></span>

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

### <span data-ttu-id="bce82-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bce82-117">-DefaultProfile</span></span>
<span data-ttu-id="bce82-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="bce82-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bce82-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="bce82-119">-InputObject</span></span>
<span data-ttu-id="bce82-120">Identitets parameter för att konstruera, se avsnittet anteckningar för INPUTOBJECT-egenskaper och skapa en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="bce82-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity
Parameter Sets: DeleteViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="bce82-121">-Namn</span><span class="sxs-lookup"><span data-stu-id="bce82-121">-Name</span></span>
<span data-ttu-id="bce82-122">Namnet på den virtuella nätverks regeln.</span><span class="sxs-lookup"><span data-stu-id="bce82-122">The name of the virtual network rule.</span></span>

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

### <span data-ttu-id="bce82-123">-Nowait</span><span class="sxs-lookup"><span data-stu-id="bce82-123">-NoWait</span></span>
<span data-ttu-id="bce82-124">Kör kommandot asynkront</span><span class="sxs-lookup"><span data-stu-id="bce82-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="bce82-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="bce82-125">-PassThru</span></span>
<span data-ttu-id="bce82-126">Returnerar true när kommandot lyckas</span><span class="sxs-lookup"><span data-stu-id="bce82-126">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="bce82-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bce82-127">-ResourceGroupName</span></span>
<span data-ttu-id="bce82-128">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="bce82-128">The name of the resource group.</span></span>
<span data-ttu-id="bce82-129">Namnet är Skift läges okänsligt.</span><span class="sxs-lookup"><span data-stu-id="bce82-129">The name is case insensitive.</span></span>

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

### <span data-ttu-id="bce82-130">-ServerName</span><span class="sxs-lookup"><span data-stu-id="bce82-130">-ServerName</span></span>
<span data-ttu-id="bce82-131">Namnet på servern.</span><span class="sxs-lookup"><span data-stu-id="bce82-131">The name of the server.</span></span>

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

### <span data-ttu-id="bce82-132">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="bce82-132">-SubscriptionId</span></span>
<span data-ttu-id="bce82-133">ID för mål prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="bce82-133">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="bce82-134">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="bce82-134">-Confirm</span></span>
<span data-ttu-id="bce82-135">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="bce82-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bce82-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bce82-136">-WhatIf</span></span>
<span data-ttu-id="bce82-137">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="bce82-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bce82-138">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="bce82-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bce82-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bce82-139">CommonParameters</span></span>
<span data-ttu-id="bce82-140">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bce82-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bce82-141">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="bce82-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bce82-142">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="bce82-142">INPUTS</span></span>

### <span data-ttu-id="bce82-143">Microsoft. Azure. PowerShell. cmdletar. MySql. Models. IMySqlIdentity</span><span class="sxs-lookup"><span data-stu-id="bce82-143">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity</span></span>

## <span data-ttu-id="bce82-144">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="bce82-144">OUTPUTS</span></span>

### <span data-ttu-id="bce82-145">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="bce82-145">System.Boolean</span></span>

## <span data-ttu-id="bce82-146">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="bce82-146">NOTES</span></span>

<span data-ttu-id="bce82-147">ALIAS</span><span class="sxs-lookup"><span data-stu-id="bce82-147">ALIASES</span></span>

<span data-ttu-id="bce82-148">KOMPLEXA PARAMETER EGENSKAPER</span><span class="sxs-lookup"><span data-stu-id="bce82-148">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="bce82-149">Skapa en hash-tabell som innehåller lämpliga egenskaper för att lägga till de parametrar som beskrivs nedan.</span><span class="sxs-lookup"><span data-stu-id="bce82-149">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="bce82-150">Om du vill ha information om hash-tabeller kör Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="bce82-150">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="bce82-151">INPUTOBJECT <IMySqlIdentity> : identitets parameter</span><span class="sxs-lookup"><span data-stu-id="bce82-151">INPUTOBJECT <IMySqlIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="bce82-152">`[ConfigurationName <String>]`: Server konfigurationens namn.</span><span class="sxs-lookup"><span data-stu-id="bce82-152">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="bce82-153">`[DatabaseName <String>]`: Namnet på databasen.</span><span class="sxs-lookup"><span data-stu-id="bce82-153">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="bce82-154">`[FirewallRuleName <String>]`: Namnet på Server brand Väggs regeln.</span><span class="sxs-lookup"><span data-stu-id="bce82-154">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="bce82-155">`[Id <String>]`: Sökväg till resurs identitet</span><span class="sxs-lookup"><span data-stu-id="bce82-155">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="bce82-156">`[LocationName <String>]`: Namnet på platsen.</span><span class="sxs-lookup"><span data-stu-id="bce82-156">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="bce82-157">`[ResourceGroupName <String>]`: Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="bce82-157">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="bce82-158">Namnet är Skift läges okänsligt.</span><span class="sxs-lookup"><span data-stu-id="bce82-158">The name is case insensitive.</span></span>
  - <span data-ttu-id="bce82-159">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: Namnet på säkerhets varnings principen.</span><span class="sxs-lookup"><span data-stu-id="bce82-159">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="bce82-160">`[ServerName <String>]`: Namnet på servern.</span><span class="sxs-lookup"><span data-stu-id="bce82-160">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="bce82-161">`[SubscriptionId <String>]`: Mål prenumerationens ID.</span><span class="sxs-lookup"><span data-stu-id="bce82-161">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="bce82-162">`[VirtualNetworkRuleName <String>]`: Namnet på den virtuella nätverks regeln.</span><span class="sxs-lookup"><span data-stu-id="bce82-162">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="bce82-163">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="bce82-163">RELATED LINKS</span></span>
