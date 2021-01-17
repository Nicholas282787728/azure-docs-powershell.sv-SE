---
external help file: ''
Module Name: Az.PostgreSql
online version: https://docs.microsoft.com/en-us/powershell/module/az.postgresql/restart-azpostgresqlserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Restart-AzPostgreSqlServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Restart-AzPostgreSqlServer.md
ms.openlocfilehash: aa5e58522aaeb1094ef2a7280b33b45e20fe03fc
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98391904"
---
# <span data-ttu-id="17b0c-101">Restart-AzPostgreSqlServer</span><span class="sxs-lookup"><span data-stu-id="17b0c-101">Restart-AzPostgreSqlServer</span></span>

## <span data-ttu-id="17b0c-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="17b0c-102">SYNOPSIS</span></span>
<span data-ttu-id="17b0c-103">Startar om en server.</span><span class="sxs-lookup"><span data-stu-id="17b0c-103">Restarts a server.</span></span>

## <span data-ttu-id="17b0c-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="17b0c-104">SYNTAX</span></span>

### <span data-ttu-id="17b0c-105">Starta om (standard)</span><span class="sxs-lookup"><span data-stu-id="17b0c-105">Restart (Default)</span></span>
```
Restart-AzPostgreSqlServer -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="17b0c-106">RestartViaIdentity</span><span class="sxs-lookup"><span data-stu-id="17b0c-106">RestartViaIdentity</span></span>
```
Restart-AzPostgreSqlServer -InputObject <IPostgreSqlIdentity> [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="17b0c-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="17b0c-107">DESCRIPTION</span></span>
<span data-ttu-id="17b0c-108">Startar om en server.</span><span class="sxs-lookup"><span data-stu-id="17b0c-108">Restarts a server.</span></span>

## <span data-ttu-id="17b0c-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="17b0c-109">EXAMPLES</span></span>

### <span data-ttu-id="17b0c-110">Exempel 1: starta om PostgreSql-servern efter resurs grupp och Server namn</span><span class="sxs-lookup"><span data-stu-id="17b0c-110">Example 1: Restart PostgreSql server by resource group and server name</span></span>
```powershell
PS C:\> Restart-AzPostgreSqlServer -ResourceGroupName PostgreSqlTestRG -Name PostgreSqlTestServer

```

<span data-ttu-id="17b0c-111">Denna cmdlet startar om PostgreSql-servern efter resurs grupp och Server namn.</span><span class="sxs-lookup"><span data-stu-id="17b0c-111">This cmdlet restarts PostgreSql server by resource group and server name.</span></span>

### <span data-ttu-id="17b0c-112">Exempel 2: starta om PostgreSql-servern efter identitet</span><span class="sxs-lookup"><span data-stu-id="17b0c-112">Example 2: Restart PostgreSql server by identity</span></span>
```powershell
PS C:\> $ID = "/subscriptions/<SubscriptionId>/resourceGroups/PostgreSqlTestRG/providers/Microsoft.DBforPostgreSQL/servers/PostgreSqlTestServer/restart"
PS C:\> Restart-AzPostgreSqlServer -InputObject $ID
 
```

<span data-ttu-id="17b0c-113">Dessa cmdletar startar om PostgreSql-servern efter identitet.</span><span class="sxs-lookup"><span data-stu-id="17b0c-113">These cmdlets restart PostgreSql server by identity.</span></span>

## <span data-ttu-id="17b0c-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="17b0c-114">PARAMETERS</span></span>

### <span data-ttu-id="17b0c-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="17b0c-115">-AsJob</span></span>
<span data-ttu-id="17b0c-116">Köra kommandot som ett jobb</span><span class="sxs-lookup"><span data-stu-id="17b0c-116">Run the command as a job</span></span>

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

### <span data-ttu-id="17b0c-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="17b0c-117">-DefaultProfile</span></span>
<span data-ttu-id="17b0c-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="17b0c-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="17b0c-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="17b0c-119">-InputObject</span></span>
<span data-ttu-id="17b0c-120">Identitets parameter för att konstruera, se avsnittet anteckningar för INPUTOBJECT-egenskaper och skapa en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="17b0c-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.IPostgreSqlIdentity
Parameter Sets: RestartViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="17b0c-121">-Namn</span><span class="sxs-lookup"><span data-stu-id="17b0c-121">-Name</span></span>
<span data-ttu-id="17b0c-122">Namnet på servern.</span><span class="sxs-lookup"><span data-stu-id="17b0c-122">The name of the server.</span></span>

```yaml
Type: System.String
Parameter Sets: Restart
Aliases: ServerName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="17b0c-123">-Nowait</span><span class="sxs-lookup"><span data-stu-id="17b0c-123">-NoWait</span></span>
<span data-ttu-id="17b0c-124">Kör kommandot asynkront</span><span class="sxs-lookup"><span data-stu-id="17b0c-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="17b0c-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="17b0c-125">-PassThru</span></span>
<span data-ttu-id="17b0c-126">Returnerar true när kommandot lyckas</span><span class="sxs-lookup"><span data-stu-id="17b0c-126">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="17b0c-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="17b0c-127">-ResourceGroupName</span></span>
<span data-ttu-id="17b0c-128">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="17b0c-128">The name of the resource group.</span></span>
<span data-ttu-id="17b0c-129">Namnet är Skift läges okänsligt.</span><span class="sxs-lookup"><span data-stu-id="17b0c-129">The name is case insensitive.</span></span>

```yaml
Type: System.String
Parameter Sets: Restart
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="17b0c-130">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="17b0c-130">-SubscriptionId</span></span>
<span data-ttu-id="17b0c-131">ID för mål prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="17b0c-131">The ID of the target subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: Restart
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="17b0c-132">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="17b0c-132">-Confirm</span></span>
<span data-ttu-id="17b0c-133">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="17b0c-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="17b0c-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="17b0c-134">-WhatIf</span></span>
<span data-ttu-id="17b0c-135">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="17b0c-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="17b0c-136">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="17b0c-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="17b0c-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="17b0c-137">CommonParameters</span></span>
<span data-ttu-id="17b0c-138">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="17b0c-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="17b0c-139">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="17b0c-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="17b0c-140">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="17b0c-140">INPUTS</span></span>

### <span data-ttu-id="17b0c-141">Microsoft. Azure. PowerShell. cmdletar. PostgreSql. Models. IPostgreSqlIdentity</span><span class="sxs-lookup"><span data-stu-id="17b0c-141">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.IPostgreSqlIdentity</span></span>

## <span data-ttu-id="17b0c-142">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="17b0c-142">OUTPUTS</span></span>

### <span data-ttu-id="17b0c-143">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="17b0c-143">System.Boolean</span></span>

## <span data-ttu-id="17b0c-144">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="17b0c-144">NOTES</span></span>

<span data-ttu-id="17b0c-145">ALIAS</span><span class="sxs-lookup"><span data-stu-id="17b0c-145">ALIASES</span></span>

<span data-ttu-id="17b0c-146">KOMPLEXA PARAMETER EGENSKAPER</span><span class="sxs-lookup"><span data-stu-id="17b0c-146">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="17b0c-147">Skapa en hash-tabell som innehåller lämpliga egenskaper för att lägga till de parametrar som beskrivs nedan.</span><span class="sxs-lookup"><span data-stu-id="17b0c-147">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="17b0c-148">Om du vill ha information om hash-tabeller kör Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="17b0c-148">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="17b0c-149">INPUTOBJECT <IPostgreSqlIdentity> : identitets parameter</span><span class="sxs-lookup"><span data-stu-id="17b0c-149">INPUTOBJECT <IPostgreSqlIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="17b0c-150">`[ConfigurationName <String>]`: Server konfigurationens namn.</span><span class="sxs-lookup"><span data-stu-id="17b0c-150">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="17b0c-151">`[DatabaseName <String>]`: Namnet på databasen.</span><span class="sxs-lookup"><span data-stu-id="17b0c-151">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="17b0c-152">`[FirewallRuleName <String>]`: Namnet på Server brand Väggs regeln.</span><span class="sxs-lookup"><span data-stu-id="17b0c-152">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="17b0c-153">`[Id <String>]`: Sökväg till resurs identitet</span><span class="sxs-lookup"><span data-stu-id="17b0c-153">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="17b0c-154">`[LocationName <String>]`: Namnet på platsen.</span><span class="sxs-lookup"><span data-stu-id="17b0c-154">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="17b0c-155">`[ResourceGroupName <String>]`: Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="17b0c-155">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="17b0c-156">Namnet är Skift läges okänsligt.</span><span class="sxs-lookup"><span data-stu-id="17b0c-156">The name is case insensitive.</span></span>
  - <span data-ttu-id="17b0c-157">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: Namnet på säkerhets varnings principen.</span><span class="sxs-lookup"><span data-stu-id="17b0c-157">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="17b0c-158">`[ServerName <String>]`: Namnet på servern.</span><span class="sxs-lookup"><span data-stu-id="17b0c-158">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="17b0c-159">`[SubscriptionId <String>]`: Mål prenumerationens ID.</span><span class="sxs-lookup"><span data-stu-id="17b0c-159">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="17b0c-160">`[VirtualNetworkRuleName <String>]`: Namnet på den virtuella nätverks regeln.</span><span class="sxs-lookup"><span data-stu-id="17b0c-160">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="17b0c-161">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="17b0c-161">RELATED LINKS</span></span>

