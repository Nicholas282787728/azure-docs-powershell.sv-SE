---
external help file: ''
Module Name: Az.PostgreSql
online version: https://docs.microsoft.com/en-us/powershell/module/az.postgresql/update-azpostgresqlconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Update-AzPostgreSqlConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Update-AzPostgreSqlConfiguration.md
ms.openlocfilehash: e1b0ea3d07a7504e75f8bd6143820c52e73d9cf9
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94272411"
---
# <span data-ttu-id="ad249-101">Update-AzPostgreSqlConfiguration</span><span class="sxs-lookup"><span data-stu-id="ad249-101">Update-AzPostgreSqlConfiguration</span></span>

## <span data-ttu-id="ad249-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="ad249-102">SYNOPSIS</span></span>
<span data-ttu-id="ad249-103">Uppdaterar en servers konfiguration.</span><span class="sxs-lookup"><span data-stu-id="ad249-103">Updates a configuration of a server.</span></span>
<span data-ttu-id="ad249-104">Använd Update-AzPostgreSqlServer istället om du vill uppdatera AdministratorLoginPassword, SKU etc.</span><span class="sxs-lookup"><span data-stu-id="ad249-104">Use Update-AzPostgreSqlServer instead if you want update AdministratorLoginPassword, sku, etc.</span></span>

## <span data-ttu-id="ad249-105">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="ad249-105">SYNTAX</span></span>

### <span data-ttu-id="ad249-106">UpdateExpanded (standard)</span><span class="sxs-lookup"><span data-stu-id="ad249-106">UpdateExpanded (Default)</span></span>
```
Update-AzPostgreSqlConfiguration -Name <String> -ResourceGroupName <String> -ServerName <String>
 [-SubscriptionId <String>] [-Source <String>] [-Value <String>] [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="ad249-107">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="ad249-107">UpdateViaIdentityExpanded</span></span>
```
Update-AzPostgreSqlConfiguration -InputObject <IPostgreSqlIdentity> [-Source <String>] [-Value <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="ad249-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="ad249-108">DESCRIPTION</span></span>
<span data-ttu-id="ad249-109">Uppdaterar en servers konfiguration.</span><span class="sxs-lookup"><span data-stu-id="ad249-109">Updates a configuration of a server.</span></span>
<span data-ttu-id="ad249-110">Använd Update-AzPostgreSqlServer istället om du vill uppdatera AdministratorLoginPassword, SKU etc.</span><span class="sxs-lookup"><span data-stu-id="ad249-110">Use Update-AzPostgreSqlServer instead if you want update AdministratorLoginPassword, sku, etc.</span></span>

## <span data-ttu-id="ad249-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="ad249-111">EXAMPLES</span></span>

### <span data-ttu-id="ad249-112">Exempel 1: uppdatera PostgreSql-konfigurationen utifrån namn</span><span class="sxs-lookup"><span data-stu-id="ad249-112">Example 1: Update PostgreSql configuration by name</span></span>
```powershell
PS C:\> Update-AzPostgreSqlConfiguration -Name intervalstyle -ResourceGroupName PostgreSqlTestRG -ServerName PostgreSqlTestServer -Value SQL_STANDARD

Name          Value
----          -----
intervalstyle SQL_STANDARD
```

<span data-ttu-id="ad249-113">Denna cmdlet uppdaterar PostgreSql-konfigurationen efter namn.</span><span class="sxs-lookup"><span data-stu-id="ad249-113">This cmdlet updates PostgreSql configuration by name.</span></span>

### <span data-ttu-id="ad249-114">Exempel 2: uppdatera PostgreSql-konfigurationen efter identitet.</span><span class="sxs-lookup"><span data-stu-id="ad249-114">Example 2: Update PostgreSql configuration by identity.</span></span>
```powershell
PS C:\> $ID = "/subscriptions/<SubscriptionId>/resourceGroups/PostgreSqlTestRG/providers/Microsoft.DBforPostgreSQL/servers/PostgreSqlTestServer/configurations/deadlock_timeout"
PS C:\> Update-AzPostgreSqlConfiguration -InputObject $ID -Value 2000

Name             Value
----             -----
deadlock_timeout 2000
```

<span data-ttu-id="ad249-115">Dessa cmdletar uppdaterar PostgreSql-konfigurationen efter identitet.</span><span class="sxs-lookup"><span data-stu-id="ad249-115">These cmdlets update PostgreSql configuration by identity.</span></span>

## <span data-ttu-id="ad249-116">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="ad249-116">PARAMETERS</span></span>

### <span data-ttu-id="ad249-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ad249-117">-AsJob</span></span>
<span data-ttu-id="ad249-118">Köra kommandot som ett jobb</span><span class="sxs-lookup"><span data-stu-id="ad249-118">Run the command as a job</span></span>

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

### <span data-ttu-id="ad249-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ad249-119">-DefaultProfile</span></span>
<span data-ttu-id="ad249-120">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="ad249-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ad249-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ad249-121">-InputObject</span></span>
<span data-ttu-id="ad249-122">Identitets parameter för att konstruera, se avsnittet anteckningar för INPUTOBJECT-egenskaper och skapa en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="ad249-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="ad249-123">-Namn</span><span class="sxs-lookup"><span data-stu-id="ad249-123">-Name</span></span>
<span data-ttu-id="ad249-124">Server konfigurationens namn.</span><span class="sxs-lookup"><span data-stu-id="ad249-124">The name of the server configuration.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases: ConfigurationName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ad249-125">-Nowait</span><span class="sxs-lookup"><span data-stu-id="ad249-125">-NoWait</span></span>
<span data-ttu-id="ad249-126">Kör kommandot asynkront</span><span class="sxs-lookup"><span data-stu-id="ad249-126">Run the command asynchronously</span></span>

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

### <span data-ttu-id="ad249-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ad249-127">-ResourceGroupName</span></span>
<span data-ttu-id="ad249-128">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="ad249-128">The name of the resource group.</span></span>
<span data-ttu-id="ad249-129">Namnet är Skift läges okänsligt.</span><span class="sxs-lookup"><span data-stu-id="ad249-129">The name is case insensitive.</span></span>

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

### <span data-ttu-id="ad249-130">-ServerName</span><span class="sxs-lookup"><span data-stu-id="ad249-130">-ServerName</span></span>
<span data-ttu-id="ad249-131">Namnet på servern.</span><span class="sxs-lookup"><span data-stu-id="ad249-131">The name of the server.</span></span>

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

### <span data-ttu-id="ad249-132">-Källa</span><span class="sxs-lookup"><span data-stu-id="ad249-132">-Source</span></span>
<span data-ttu-id="ad249-133">Källa för konfigurationen.</span><span class="sxs-lookup"><span data-stu-id="ad249-133">Source of the configuration.</span></span>

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

### <span data-ttu-id="ad249-134">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="ad249-134">-SubscriptionId</span></span>
<span data-ttu-id="ad249-135">ID för mål prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="ad249-135">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="ad249-136">-Värde</span><span class="sxs-lookup"><span data-stu-id="ad249-136">-Value</span></span>
<span data-ttu-id="ad249-137">Konfigurationens värde.</span><span class="sxs-lookup"><span data-stu-id="ad249-137">Value of the configuration.</span></span>

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

### <span data-ttu-id="ad249-138">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="ad249-138">-Confirm</span></span>
<span data-ttu-id="ad249-139">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="ad249-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ad249-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ad249-140">-WhatIf</span></span>
<span data-ttu-id="ad249-141">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="ad249-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ad249-142">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="ad249-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ad249-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ad249-143">CommonParameters</span></span>
<span data-ttu-id="ad249-144">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ad249-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ad249-145">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ad249-145">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ad249-146">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="ad249-146">INPUTS</span></span>

### <span data-ttu-id="ad249-147">Microsoft. Azure. PowerShell. cmdletar. PostgreSql. Models. IPostgreSqlIdentity</span><span class="sxs-lookup"><span data-stu-id="ad249-147">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.IPostgreSqlIdentity</span></span>

## <span data-ttu-id="ad249-148">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="ad249-148">OUTPUTS</span></span>

### <span data-ttu-id="ad249-149">Microsoft. Azure. PowerShell. cmdletar. PostgreSql. Models. Api20171201. IConfiguration</span><span class="sxs-lookup"><span data-stu-id="ad249-149">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.Api20171201.IConfiguration</span></span>

## <span data-ttu-id="ad249-150">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="ad249-150">NOTES</span></span>

<span data-ttu-id="ad249-151">ALIAS</span><span class="sxs-lookup"><span data-stu-id="ad249-151">ALIASES</span></span>

<span data-ttu-id="ad249-152">KOMPLEXA PARAMETER EGENSKAPER</span><span class="sxs-lookup"><span data-stu-id="ad249-152">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="ad249-153">Skapa en hash-tabell som innehåller lämpliga egenskaper för att lägga till de parametrar som beskrivs nedan.</span><span class="sxs-lookup"><span data-stu-id="ad249-153">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="ad249-154">Om du vill ha information om hash-tabeller kör Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="ad249-154">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="ad249-155">INPUTOBJECT <IPostgreSqlIdentity> : identitets parameter</span><span class="sxs-lookup"><span data-stu-id="ad249-155">INPUTOBJECT <IPostgreSqlIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="ad249-156">`[ConfigurationName <String>]`: Server konfigurationens namn.</span><span class="sxs-lookup"><span data-stu-id="ad249-156">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="ad249-157">`[DatabaseName <String>]`: Namnet på databasen.</span><span class="sxs-lookup"><span data-stu-id="ad249-157">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="ad249-158">`[FirewallRuleName <String>]`: Namnet på Server brand Väggs regeln.</span><span class="sxs-lookup"><span data-stu-id="ad249-158">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="ad249-159">`[Id <String>]`: Sökväg till resurs identitet</span><span class="sxs-lookup"><span data-stu-id="ad249-159">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="ad249-160">`[LocationName <String>]`: Namnet på platsen.</span><span class="sxs-lookup"><span data-stu-id="ad249-160">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="ad249-161">`[ResourceGroupName <String>]`: Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="ad249-161">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="ad249-162">Namnet är Skift läges okänsligt.</span><span class="sxs-lookup"><span data-stu-id="ad249-162">The name is case insensitive.</span></span>
  - <span data-ttu-id="ad249-163">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: Namnet på säkerhets varnings principen.</span><span class="sxs-lookup"><span data-stu-id="ad249-163">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="ad249-164">`[ServerName <String>]`: Namnet på servern.</span><span class="sxs-lookup"><span data-stu-id="ad249-164">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="ad249-165">`[SubscriptionId <String>]`: Mål prenumerationens ID.</span><span class="sxs-lookup"><span data-stu-id="ad249-165">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="ad249-166">`[VirtualNetworkRuleName <String>]`: Namnet på den virtuella nätverks regeln.</span><span class="sxs-lookup"><span data-stu-id="ad249-166">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="ad249-167">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="ad249-167">RELATED LINKS</span></span>

