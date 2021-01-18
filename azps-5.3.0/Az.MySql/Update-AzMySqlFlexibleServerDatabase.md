---
external help file: ''
Module Name: Az.MySql
online version: https://docs.microsoft.com/en-us/powershell/module/az.mysql/update-azmysqlflexibleserverdatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Update-AzMySqlFlexibleServerDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Update-AzMySqlFlexibleServerDatabase.md
ms.openlocfilehash: 2867c6f57967da64178e798f3e517715b44d07c2
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98522513"
---
# <span data-ttu-id="ca2c6-101">Update-AzMySqlFlexibleServerDatabase</span><span class="sxs-lookup"><span data-stu-id="ca2c6-101">Update-AzMySqlFlexibleServerDatabase</span></span>

## <span data-ttu-id="ca2c6-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="ca2c6-102">SYNOPSIS</span></span>
<span data-ttu-id="ca2c6-103">Skapar en ny databas eller uppdaterar en befintlig databas.</span><span class="sxs-lookup"><span data-stu-id="ca2c6-103">Creates a new database or updates an existing database.</span></span>

## <span data-ttu-id="ca2c6-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="ca2c6-104">SYNTAX</span></span>

### <span data-ttu-id="ca2c6-105">UpdateExpanded (standard)</span><span class="sxs-lookup"><span data-stu-id="ca2c6-105">UpdateExpanded (Default)</span></span>
```
Update-AzMySqlFlexibleServerDatabase -Name <String> -ResourceGroupName <String> -ServerName <String>
 [-SubscriptionId <String>] [-Charset <String>] [-Collation <String>] [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="ca2c6-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="ca2c6-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzMySqlFlexibleServerDatabase -InputObject <IMySqlIdentity> [-Charset <String>] [-Collation <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="ca2c6-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="ca2c6-107">DESCRIPTION</span></span>
<span data-ttu-id="ca2c6-108">Skapar en ny databas eller uppdaterar en befintlig databas.</span><span class="sxs-lookup"><span data-stu-id="ca2c6-108">Creates a new database or updates an existing database.</span></span>

## <span data-ttu-id="ca2c6-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="ca2c6-109">EXAMPLES</span></span>

### <span data-ttu-id="ca2c6-110">Exempel 1: uppdatera en MySql Server-databas efter namn</span><span class="sxs-lookup"><span data-stu-id="ca2c6-110">Example 1: Update a MySql server database by name</span></span>
```powershell
PS C:\> Update-AzMySqlFlexibleServerDatabase -Name database-test -ResourceGroupName PowershellMySqlTest -ServerName mysql-test -Charset utf8

Name            Charset     Collation              
----            -------- ------------------
databasetest   utf8      latin1_swedish_ci  
```

<span data-ttu-id="ca2c6-111">Uppdatera en databas efter resurs namn.</span><span class="sxs-lookup"><span data-stu-id="ca2c6-111">Update a database by resource name.</span></span>

### <span data-ttu-id="ca2c6-112">Exempel 2: uppdatera MySql-databasen per parameter.</span><span class="sxs-lookup"><span data-stu-id="ca2c6-112">Example 2: Update MySql database by parameter.</span></span>
```powershell
PS C:\> $ID = "/subscriptions/<SubscriptionId>/resourceGroups/PowershellMySqlTest/providers/Microsoft.DBForMySql/servers/mysql-test/databases/databasetest"
PS C:\> Update-AzMySqlFlexibleServerDatabase -Parameter $ID -Charset utf8

Name            Charset     Collation              
----            -------- ------------------
databasetest   utf8      latin1_swedish_ci  
```

<span data-ttu-id="ca2c6-113">Uppdatera en databas efter parameter</span><span class="sxs-lookup"><span data-stu-id="ca2c6-113">Update a database by parameter</span></span>

## <span data-ttu-id="ca2c6-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="ca2c6-114">PARAMETERS</span></span>

### <span data-ttu-id="ca2c6-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ca2c6-115">-AsJob</span></span>
<span data-ttu-id="ca2c6-116">Köra kommandot som ett jobb</span><span class="sxs-lookup"><span data-stu-id="ca2c6-116">Run the command as a job</span></span>

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

### <span data-ttu-id="ca2c6-117">-Charset</span><span class="sxs-lookup"><span data-stu-id="ca2c6-117">-Charset</span></span>
<span data-ttu-id="ca2c6-118">Charset för databasen.</span><span class="sxs-lookup"><span data-stu-id="ca2c6-118">The charset of the database.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ca2c6-119">-Sortering</span><span class="sxs-lookup"><span data-stu-id="ca2c6-119">-Collation</span></span>
<span data-ttu-id="ca2c6-120">Sortering av databasen.</span><span class="sxs-lookup"><span data-stu-id="ca2c6-120">The collation of the database.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ca2c6-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ca2c6-121">-DefaultProfile</span></span>
<span data-ttu-id="ca2c6-122">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="ca2c6-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ca2c6-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ca2c6-123">-InputObject</span></span>
<span data-ttu-id="ca2c6-124">Identitets parameter för att konstruera, se avsnittet anteckningar för INPUTOBJECT-egenskaper och skapa en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="ca2c6-124">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="ca2c6-125">-Namn</span><span class="sxs-lookup"><span data-stu-id="ca2c6-125">-Name</span></span>
<span data-ttu-id="ca2c6-126">Namnet på databasen.</span><span class="sxs-lookup"><span data-stu-id="ca2c6-126">The name of the database.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases: DatabaseName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ca2c6-127">-Nowait</span><span class="sxs-lookup"><span data-stu-id="ca2c6-127">-NoWait</span></span>
<span data-ttu-id="ca2c6-128">Kör kommandot asynkront</span><span class="sxs-lookup"><span data-stu-id="ca2c6-128">Run the command asynchronously</span></span>

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

### <span data-ttu-id="ca2c6-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ca2c6-129">-ResourceGroupName</span></span>
<span data-ttu-id="ca2c6-130">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="ca2c6-130">The name of the resource group.</span></span>
<span data-ttu-id="ca2c6-131">Namnet är Skift läges okänsligt.</span><span class="sxs-lookup"><span data-stu-id="ca2c6-131">The name is case insensitive.</span></span>

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

### <span data-ttu-id="ca2c6-132">-ServerName</span><span class="sxs-lookup"><span data-stu-id="ca2c6-132">-ServerName</span></span>
<span data-ttu-id="ca2c6-133">Namnet på servern.</span><span class="sxs-lookup"><span data-stu-id="ca2c6-133">The name of the server.</span></span>

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

### <span data-ttu-id="ca2c6-134">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="ca2c6-134">-SubscriptionId</span></span>
<span data-ttu-id="ca2c6-135">ID för mål prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="ca2c6-135">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="ca2c6-136">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="ca2c6-136">-Confirm</span></span>
<span data-ttu-id="ca2c6-137">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="ca2c6-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ca2c6-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ca2c6-138">-WhatIf</span></span>
<span data-ttu-id="ca2c6-139">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="ca2c6-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ca2c6-140">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="ca2c6-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ca2c6-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ca2c6-141">CommonParameters</span></span>
<span data-ttu-id="ca2c6-142">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ca2c6-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ca2c6-143">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ca2c6-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ca2c6-144">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="ca2c6-144">INPUTS</span></span>

### <span data-ttu-id="ca2c6-145">Microsoft. Azure. PowerShell. cmdletar. MySql. Models. IMySqlIdentity</span><span class="sxs-lookup"><span data-stu-id="ca2c6-145">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity</span></span>

## <span data-ttu-id="ca2c6-146">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="ca2c6-146">OUTPUTS</span></span>

### <span data-ttu-id="ca2c6-147">Microsoft. Azure. PowerShell. cmdletar. MySql. Models. Api20171201. IDatabase</span><span class="sxs-lookup"><span data-stu-id="ca2c6-147">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20171201.IDatabase</span></span>

## <span data-ttu-id="ca2c6-148">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="ca2c6-148">NOTES</span></span>

<span data-ttu-id="ca2c6-149">ALIAS</span><span class="sxs-lookup"><span data-stu-id="ca2c6-149">ALIASES</span></span>

<span data-ttu-id="ca2c6-150">KOMPLEXA PARAMETER EGENSKAPER</span><span class="sxs-lookup"><span data-stu-id="ca2c6-150">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="ca2c6-151">Skapa en hash-tabell som innehåller lämpliga egenskaper för att lägga till de parametrar som beskrivs nedan.</span><span class="sxs-lookup"><span data-stu-id="ca2c6-151">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="ca2c6-152">Om du vill ha information om hash-tabeller kör Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="ca2c6-152">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="ca2c6-153">INPUTOBJECT <IMySqlIdentity> : identitets parameter</span><span class="sxs-lookup"><span data-stu-id="ca2c6-153">INPUTOBJECT <IMySqlIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="ca2c6-154">`[ConfigurationName <String>]`: Server konfigurationens namn.</span><span class="sxs-lookup"><span data-stu-id="ca2c6-154">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="ca2c6-155">`[DatabaseName <String>]`: Namnet på databasen.</span><span class="sxs-lookup"><span data-stu-id="ca2c6-155">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="ca2c6-156">`[FirewallRuleName <String>]`: Namnet på Server brand Väggs regeln.</span><span class="sxs-lookup"><span data-stu-id="ca2c6-156">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="ca2c6-157">`[Id <String>]`: Sökväg till resurs identitet</span><span class="sxs-lookup"><span data-stu-id="ca2c6-157">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="ca2c6-158">`[KeyName <String>]`: Server namnet.</span><span class="sxs-lookup"><span data-stu-id="ca2c6-158">`[KeyName <String>]`: The name of the server key.</span></span>
  - <span data-ttu-id="ca2c6-159">`[LocationName <String>]`: Namnet på platsen.</span><span class="sxs-lookup"><span data-stu-id="ca2c6-159">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="ca2c6-160">`[ResourceGroupName <String>]`: Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="ca2c6-160">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="ca2c6-161">Namnet är Skift läges okänsligt.</span><span class="sxs-lookup"><span data-stu-id="ca2c6-161">The name is case insensitive.</span></span>
  - <span data-ttu-id="ca2c6-162">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: Namnet på säkerhets varnings principen.</span><span class="sxs-lookup"><span data-stu-id="ca2c6-162">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="ca2c6-163">`[ServerName <String>]`: Namnet på servern.</span><span class="sxs-lookup"><span data-stu-id="ca2c6-163">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="ca2c6-164">`[SubscriptionId <String>]`: Mål prenumerationens ID.</span><span class="sxs-lookup"><span data-stu-id="ca2c6-164">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="ca2c6-165">`[VirtualNetworkRuleName <String>]`: Namnet på den virtuella nätverks regeln.</span><span class="sxs-lookup"><span data-stu-id="ca2c6-165">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="ca2c6-166">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="ca2c6-166">RELATED LINKS</span></span>

