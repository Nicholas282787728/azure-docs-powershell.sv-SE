---
external help file: ''
Module Name: Az.PostgreSql
online version: https://docs.microsoft.com/en-us/powershell/module/az.postgresql/remove-azpostgresqlfirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Remove-AzPostgreSqlFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Remove-AzPostgreSqlFirewallRule.md
ms.openlocfilehash: 27f03ba80a01997d61bc50f6a644b4e3c4cffb7b
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94258075"
---
# <span data-ttu-id="0d83d-101">Remove-AzPostgreSqlFirewallRule</span><span class="sxs-lookup"><span data-stu-id="0d83d-101">Remove-AzPostgreSqlFirewallRule</span></span>

## <span data-ttu-id="0d83d-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="0d83d-102">SYNOPSIS</span></span>
<span data-ttu-id="0d83d-103">Tar bort en regel för en server brand vägg.</span><span class="sxs-lookup"><span data-stu-id="0d83d-103">Deletes a server firewall rule.</span></span>

## <span data-ttu-id="0d83d-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="0d83d-104">SYNTAX</span></span>

### <span data-ttu-id="0d83d-105">Ta bort (standard)</span><span class="sxs-lookup"><span data-stu-id="0d83d-105">Delete (Default)</span></span>
```
Remove-AzPostgreSqlFirewallRule -Name <String> -ResourceGroupName <String> -ServerName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="0d83d-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="0d83d-106">DeleteViaIdentity</span></span>
```
Remove-AzPostgreSqlFirewallRule -InputObject <IPostgreSqlIdentity> [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="0d83d-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="0d83d-107">DESCRIPTION</span></span>
<span data-ttu-id="0d83d-108">Tar bort en regel för en server brand vägg.</span><span class="sxs-lookup"><span data-stu-id="0d83d-108">Deletes a server firewall rule.</span></span>

## <span data-ttu-id="0d83d-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="0d83d-109">EXAMPLES</span></span>

### <span data-ttu-id="0d83d-110">Exempel 1: ta bort PostgreSql brand Väggs regel efter namn</span><span class="sxs-lookup"><span data-stu-id="0d83d-110">Example 1: Remove PostgreSql Firewall Rule by name</span></span>
```powershell
PS C:\> Remove-AzPostgreSqlFirewallRule -Name rule -ResourceGroupName PostgreSqlTestRG -ServerName PostgreSqlTestServer

```

<span data-ttu-id="0d83d-111">Denna cmdlet tar bort PostgreSql efter namn.</span><span class="sxs-lookup"><span data-stu-id="0d83d-111">This cmdlet removes PostgreSql Firewall Rule by name.</span></span>

### <span data-ttu-id="0d83d-112">Exempel 2: ta bort PostgreSql brand Väggs regel efter identitet</span><span class="sxs-lookup"><span data-stu-id="0d83d-112">Example 2: Remove PostgreSql Firewall Rule by identity</span></span>
```powershell
PS C:\> $ID = "/subscriptions/<SubscriptionId>/resourceGroups/PostgreSqlTestRG/providers/Microsoft.DBforPostgreSQL/servers/PostgreSqlTestServer/firewallRules/rule"
PS C:\> Remove-AzPostgreSqlFirewallRule -InputObject $ID
 
```

<span data-ttu-id="0d83d-113">De här cmdletarna tar bort PostgreSql brand Väggs regel efter identitet.</span><span class="sxs-lookup"><span data-stu-id="0d83d-113">These cmdlets remove PostgreSql Firewall Rule by identity.</span></span>

## <span data-ttu-id="0d83d-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="0d83d-114">PARAMETERS</span></span>

### <span data-ttu-id="0d83d-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="0d83d-115">-AsJob</span></span>
<span data-ttu-id="0d83d-116">Köra kommandot som ett jobb</span><span class="sxs-lookup"><span data-stu-id="0d83d-116">Run the command as a job</span></span>

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

### <span data-ttu-id="0d83d-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0d83d-117">-DefaultProfile</span></span>
<span data-ttu-id="0d83d-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="0d83d-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0d83d-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0d83d-119">-InputObject</span></span>
<span data-ttu-id="0d83d-120">Identitets parameter för att konstruera, se avsnittet anteckningar för INPUTOBJECT-egenskaper och skapa en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="0d83d-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="0d83d-121">-Namn</span><span class="sxs-lookup"><span data-stu-id="0d83d-121">-Name</span></span>
<span data-ttu-id="0d83d-122">Namnet på Server brand Väggs regeln.</span><span class="sxs-lookup"><span data-stu-id="0d83d-122">The name of the server firewall rule.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases: FirewallRuleName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0d83d-123">-Nowait</span><span class="sxs-lookup"><span data-stu-id="0d83d-123">-NoWait</span></span>
<span data-ttu-id="0d83d-124">Kör kommandot asynkront</span><span class="sxs-lookup"><span data-stu-id="0d83d-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="0d83d-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="0d83d-125">-PassThru</span></span>
<span data-ttu-id="0d83d-126">Returnerar true när kommandot lyckas</span><span class="sxs-lookup"><span data-stu-id="0d83d-126">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="0d83d-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0d83d-127">-ResourceGroupName</span></span>
<span data-ttu-id="0d83d-128">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="0d83d-128">The name of the resource group.</span></span>
<span data-ttu-id="0d83d-129">Namnet är Skift läges okänsligt.</span><span class="sxs-lookup"><span data-stu-id="0d83d-129">The name is case insensitive.</span></span>

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

### <span data-ttu-id="0d83d-130">-ServerName</span><span class="sxs-lookup"><span data-stu-id="0d83d-130">-ServerName</span></span>
<span data-ttu-id="0d83d-131">Namnet på servern.</span><span class="sxs-lookup"><span data-stu-id="0d83d-131">The name of the server.</span></span>

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

### <span data-ttu-id="0d83d-132">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="0d83d-132">-SubscriptionId</span></span>
<span data-ttu-id="0d83d-133">ID för mål prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="0d83d-133">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="0d83d-134">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="0d83d-134">-Confirm</span></span>
<span data-ttu-id="0d83d-135">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="0d83d-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0d83d-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0d83d-136">-WhatIf</span></span>
<span data-ttu-id="0d83d-137">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="0d83d-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0d83d-138">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="0d83d-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0d83d-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0d83d-139">CommonParameters</span></span>
<span data-ttu-id="0d83d-140">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0d83d-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0d83d-141">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="0d83d-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0d83d-142">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="0d83d-142">INPUTS</span></span>

### <span data-ttu-id="0d83d-143">Microsoft. Azure. PowerShell. cmdletar. PostgreSql. Models. IPostgreSqlIdentity</span><span class="sxs-lookup"><span data-stu-id="0d83d-143">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.IPostgreSqlIdentity</span></span>

## <span data-ttu-id="0d83d-144">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="0d83d-144">OUTPUTS</span></span>

### <span data-ttu-id="0d83d-145">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="0d83d-145">System.Boolean</span></span>

## <span data-ttu-id="0d83d-146">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="0d83d-146">NOTES</span></span>

<span data-ttu-id="0d83d-147">ALIAS</span><span class="sxs-lookup"><span data-stu-id="0d83d-147">ALIASES</span></span>

<span data-ttu-id="0d83d-148">KOMPLEXA PARAMETER EGENSKAPER</span><span class="sxs-lookup"><span data-stu-id="0d83d-148">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="0d83d-149">Skapa en hash-tabell som innehåller lämpliga egenskaper för att lägga till de parametrar som beskrivs nedan.</span><span class="sxs-lookup"><span data-stu-id="0d83d-149">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="0d83d-150">Om du vill ha information om hash-tabeller kör Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="0d83d-150">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="0d83d-151">INPUTOBJECT <IPostgreSqlIdentity> : identitets parameter</span><span class="sxs-lookup"><span data-stu-id="0d83d-151">INPUTOBJECT <IPostgreSqlIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="0d83d-152">`[ConfigurationName <String>]`: Server konfigurationens namn.</span><span class="sxs-lookup"><span data-stu-id="0d83d-152">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="0d83d-153">`[DatabaseName <String>]`: Namnet på databasen.</span><span class="sxs-lookup"><span data-stu-id="0d83d-153">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="0d83d-154">`[FirewallRuleName <String>]`: Namnet på Server brand Väggs regeln.</span><span class="sxs-lookup"><span data-stu-id="0d83d-154">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="0d83d-155">`[Id <String>]`: Sökväg till resurs identitet</span><span class="sxs-lookup"><span data-stu-id="0d83d-155">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="0d83d-156">`[LocationName <String>]`: Namnet på platsen.</span><span class="sxs-lookup"><span data-stu-id="0d83d-156">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="0d83d-157">`[ResourceGroupName <String>]`: Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="0d83d-157">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="0d83d-158">Namnet är Skift läges okänsligt.</span><span class="sxs-lookup"><span data-stu-id="0d83d-158">The name is case insensitive.</span></span>
  - <span data-ttu-id="0d83d-159">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: Namnet på säkerhets varnings principen.</span><span class="sxs-lookup"><span data-stu-id="0d83d-159">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="0d83d-160">`[ServerName <String>]`: Namnet på servern.</span><span class="sxs-lookup"><span data-stu-id="0d83d-160">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="0d83d-161">`[SubscriptionId <String>]`: Mål prenumerationens ID.</span><span class="sxs-lookup"><span data-stu-id="0d83d-161">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="0d83d-162">`[VirtualNetworkRuleName <String>]`: Namnet på den virtuella nätverks regeln.</span><span class="sxs-lookup"><span data-stu-id="0d83d-162">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="0d83d-163">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="0d83d-163">RELATED LINKS</span></span>
