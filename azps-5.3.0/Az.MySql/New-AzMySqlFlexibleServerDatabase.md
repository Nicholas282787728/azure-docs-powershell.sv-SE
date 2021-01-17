---
external help file: ''
Module Name: Az.MySql
online version: https://docs.microsoft.com/en-us/powershell/module/az.mysql/new-azmysqlflexibleserverdatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/New-AzMySqlFlexibleServerDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/New-AzMySqlFlexibleServerDatabase.md
ms.openlocfilehash: 9d8933aad3b3e24893062e43a3b3232bd0b57cfb
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98422563"
---
# <span data-ttu-id="d4baf-101">New-AzMySqlFlexibleServerDatabase</span><span class="sxs-lookup"><span data-stu-id="d4baf-101">New-AzMySqlFlexibleServerDatabase</span></span>

## <span data-ttu-id="d4baf-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="d4baf-102">SYNOPSIS</span></span>
<span data-ttu-id="d4baf-103">Skapar en ny databas eller uppdaterar en befintlig databas.</span><span class="sxs-lookup"><span data-stu-id="d4baf-103">Creates a new database or updates an existing database.</span></span>

## <span data-ttu-id="d4baf-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="d4baf-104">SYNTAX</span></span>

### <span data-ttu-id="d4baf-105">CreateExpanded (standard)</span><span class="sxs-lookup"><span data-stu-id="d4baf-105">CreateExpanded (Default)</span></span>
```
New-AzMySqlFlexibleServerDatabase -Name <String> -ResourceGroupName <String> -ServerName <String>
 [-SubscriptionId <String>] [-Charset <String>] [-Collation <String>] [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="d4baf-106">CreateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="d4baf-106">CreateViaIdentityExpanded</span></span>
```
New-AzMySqlFlexibleServerDatabase -InputObject <IMySqlIdentity> [-Charset <String>] [-Collation <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="d4baf-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="d4baf-107">DESCRIPTION</span></span>
<span data-ttu-id="d4baf-108">Skapar en ny databas eller uppdaterar en befintlig databas.</span><span class="sxs-lookup"><span data-stu-id="d4baf-108">Creates a new database or updates an existing database.</span></span>

## <span data-ttu-id="d4baf-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="d4baf-109">EXAMPLES</span></span>

### <span data-ttu-id="d4baf-110">Exempel 1: skapa en ny MySql Server-databas</span><span class="sxs-lookup"><span data-stu-id="d4baf-110">Example 1: Create a new MySql server database</span></span>
```powershell
PS C:\> New-AzMySqlFlexibleServerDatabase -Name databasetest -ResourceGroupName PowershellMySqlTest -ServerName mysql-test

Name            Charset     Collation              
----            -------- ------------------
databasetest   latin1   latin1_swedish_ci  
```

<span data-ttu-id="d4baf-111">Skapa en databas med standardinställningar.</span><span class="sxs-lookup"><span data-stu-id="d4baf-111">Create a database with default settings.</span></span>

## <span data-ttu-id="d4baf-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="d4baf-112">PARAMETERS</span></span>

### <span data-ttu-id="d4baf-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d4baf-113">-AsJob</span></span>
<span data-ttu-id="d4baf-114">Köra kommandot som ett jobb</span><span class="sxs-lookup"><span data-stu-id="d4baf-114">Run the command as a job</span></span>

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

### <span data-ttu-id="d4baf-115">-Charset</span><span class="sxs-lookup"><span data-stu-id="d4baf-115">-Charset</span></span>
<span data-ttu-id="d4baf-116">Charset för databasen.</span><span class="sxs-lookup"><span data-stu-id="d4baf-116">The charset of the database.</span></span>

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

### <span data-ttu-id="d4baf-117">-Sortering</span><span class="sxs-lookup"><span data-stu-id="d4baf-117">-Collation</span></span>
<span data-ttu-id="d4baf-118">Sortering av databasen.</span><span class="sxs-lookup"><span data-stu-id="d4baf-118">The collation of the database.</span></span>

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

### <span data-ttu-id="d4baf-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d4baf-119">-DefaultProfile</span></span>
<span data-ttu-id="d4baf-120">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="d4baf-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d4baf-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d4baf-121">-InputObject</span></span>
<span data-ttu-id="d4baf-122">Identitets parameter för att konstruera, se avsnittet anteckningar för INPUTOBJECT-egenskaper och skapa en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="d4baf-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity
Parameter Sets: CreateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d4baf-123">-Namn</span><span class="sxs-lookup"><span data-stu-id="d4baf-123">-Name</span></span>
<span data-ttu-id="d4baf-124">Namnet på databasen.</span><span class="sxs-lookup"><span data-stu-id="d4baf-124">The name of the database.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateExpanded
Aliases: DatabaseName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d4baf-125">-Nowait</span><span class="sxs-lookup"><span data-stu-id="d4baf-125">-NoWait</span></span>
<span data-ttu-id="d4baf-126">Kör kommandot asynkront</span><span class="sxs-lookup"><span data-stu-id="d4baf-126">Run the command asynchronously</span></span>

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

### <span data-ttu-id="d4baf-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d4baf-127">-ResourceGroupName</span></span>
<span data-ttu-id="d4baf-128">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="d4baf-128">The name of the resource group.</span></span>
<span data-ttu-id="d4baf-129">Namnet är Skift läges okänsligt.</span><span class="sxs-lookup"><span data-stu-id="d4baf-129">The name is case insensitive.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d4baf-130">-ServerName</span><span class="sxs-lookup"><span data-stu-id="d4baf-130">-ServerName</span></span>
<span data-ttu-id="d4baf-131">Namnet på servern.</span><span class="sxs-lookup"><span data-stu-id="d4baf-131">The name of the server.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d4baf-132">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="d4baf-132">-SubscriptionId</span></span>
<span data-ttu-id="d4baf-133">ID för mål prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="d4baf-133">The ID of the target subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d4baf-134">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="d4baf-134">-Confirm</span></span>
<span data-ttu-id="d4baf-135">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="d4baf-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d4baf-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d4baf-136">-WhatIf</span></span>
<span data-ttu-id="d4baf-137">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="d4baf-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d4baf-138">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="d4baf-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d4baf-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d4baf-139">CommonParameters</span></span>
<span data-ttu-id="d4baf-140">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d4baf-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d4baf-141">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d4baf-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d4baf-142">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="d4baf-142">INPUTS</span></span>

### <span data-ttu-id="d4baf-143">Microsoft. Azure. PowerShell. cmdletar. MySql. Models. IMySqlIdentity</span><span class="sxs-lookup"><span data-stu-id="d4baf-143">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity</span></span>

## <span data-ttu-id="d4baf-144">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="d4baf-144">OUTPUTS</span></span>

### <span data-ttu-id="d4baf-145">Microsoft. Azure. PowerShell. cmdletar. MySql. Models. Api20171201. IDatabase</span><span class="sxs-lookup"><span data-stu-id="d4baf-145">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20171201.IDatabase</span></span>

## <span data-ttu-id="d4baf-146">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="d4baf-146">NOTES</span></span>

<span data-ttu-id="d4baf-147">ALIAS</span><span class="sxs-lookup"><span data-stu-id="d4baf-147">ALIASES</span></span>

<span data-ttu-id="d4baf-148">KOMPLEXA PARAMETER EGENSKAPER</span><span class="sxs-lookup"><span data-stu-id="d4baf-148">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="d4baf-149">Skapa en hash-tabell som innehåller lämpliga egenskaper för att lägga till de parametrar som beskrivs nedan.</span><span class="sxs-lookup"><span data-stu-id="d4baf-149">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="d4baf-150">Om du vill ha information om hash-tabeller kör Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="d4baf-150">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="d4baf-151">INPUTOBJECT <IMySqlIdentity> : identitets parameter</span><span class="sxs-lookup"><span data-stu-id="d4baf-151">INPUTOBJECT <IMySqlIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="d4baf-152">`[ConfigurationName <String>]`: Server konfigurationens namn.</span><span class="sxs-lookup"><span data-stu-id="d4baf-152">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="d4baf-153">`[DatabaseName <String>]`: Namnet på databasen.</span><span class="sxs-lookup"><span data-stu-id="d4baf-153">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="d4baf-154">`[FirewallRuleName <String>]`: Namnet på Server brand Väggs regeln.</span><span class="sxs-lookup"><span data-stu-id="d4baf-154">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="d4baf-155">`[Id <String>]`: Sökväg till resurs identitet</span><span class="sxs-lookup"><span data-stu-id="d4baf-155">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="d4baf-156">`[KeyName <String>]`: Server namnet.</span><span class="sxs-lookup"><span data-stu-id="d4baf-156">`[KeyName <String>]`: The name of the server key.</span></span>
  - <span data-ttu-id="d4baf-157">`[LocationName <String>]`: Namnet på platsen.</span><span class="sxs-lookup"><span data-stu-id="d4baf-157">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="d4baf-158">`[ResourceGroupName <String>]`: Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="d4baf-158">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="d4baf-159">Namnet är Skift läges okänsligt.</span><span class="sxs-lookup"><span data-stu-id="d4baf-159">The name is case insensitive.</span></span>
  - <span data-ttu-id="d4baf-160">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: Namnet på säkerhets varnings principen.</span><span class="sxs-lookup"><span data-stu-id="d4baf-160">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="d4baf-161">`[ServerName <String>]`: Namnet på servern.</span><span class="sxs-lookup"><span data-stu-id="d4baf-161">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="d4baf-162">`[SubscriptionId <String>]`: Mål prenumerationens ID.</span><span class="sxs-lookup"><span data-stu-id="d4baf-162">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="d4baf-163">`[VirtualNetworkRuleName <String>]`: Namnet på den virtuella nätverks regeln.</span><span class="sxs-lookup"><span data-stu-id="d4baf-163">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="d4baf-164">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="d4baf-164">RELATED LINKS</span></span>

