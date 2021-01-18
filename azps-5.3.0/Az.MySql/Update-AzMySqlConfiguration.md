---
external help file: ''
Module Name: Az.MySql
online version: https://docs.microsoft.com/en-us/powershell/module/az.mysql/update-azmysqlconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Update-AzMySqlConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Update-AzMySqlConfiguration.md
ms.openlocfilehash: 6c7576023e4902caacd204edc97feba0a378f63b
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98522515"
---
# <span data-ttu-id="e44b9-101">Update-AzMySqlConfiguration</span><span class="sxs-lookup"><span data-stu-id="e44b9-101">Update-AzMySqlConfiguration</span></span>

## <span data-ttu-id="e44b9-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="e44b9-102">SYNOPSIS</span></span>
<span data-ttu-id="e44b9-103">Uppdaterar en servers konfiguration.</span><span class="sxs-lookup"><span data-stu-id="e44b9-103">Updates a configuration of a server.</span></span>
<span data-ttu-id="e44b9-104">Använd Update-AzMySqlServer istället om du vill uppdatera AdministratorLoginPassword, SKU etc.</span><span class="sxs-lookup"><span data-stu-id="e44b9-104">Use Update-AzMySqlServer instead if you want update AdministratorLoginPassword, sku, etc.</span></span>

## <span data-ttu-id="e44b9-105">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="e44b9-105">SYNTAX</span></span>

### <span data-ttu-id="e44b9-106">UpdateExpanded (standard)</span><span class="sxs-lookup"><span data-stu-id="e44b9-106">UpdateExpanded (Default)</span></span>
```
Update-AzMySqlConfiguration -Name <String> -ResourceGroupName <String> -ServerName <String>
 [-SubscriptionId <String>] [-Source <String>] [-Value <String>] [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="e44b9-107">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="e44b9-107">UpdateViaIdentityExpanded</span></span>
```
Update-AzMySqlConfiguration -InputObject <IMySqlIdentity> [-Source <String>] [-Value <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="e44b9-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="e44b9-108">DESCRIPTION</span></span>
<span data-ttu-id="e44b9-109">Uppdaterar en servers konfiguration.</span><span class="sxs-lookup"><span data-stu-id="e44b9-109">Updates a configuration of a server.</span></span>
<span data-ttu-id="e44b9-110">Använd Update-AzMySqlServer istället om du vill uppdatera AdministratorLoginPassword, SKU etc.</span><span class="sxs-lookup"><span data-stu-id="e44b9-110">Use Update-AzMySqlServer instead if you want update AdministratorLoginPassword, sku, etc.</span></span>

## <span data-ttu-id="e44b9-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="e44b9-111">EXAMPLES</span></span>

### <span data-ttu-id="e44b9-112">Exempel 1: uppdatera MySql-konfigurationen efter namn</span><span class="sxs-lookup"><span data-stu-id="e44b9-112">Example 1: Update MySql configuration by name</span></span>
```powershell
PS C:\> Update-AzMySqlConfiguration -Name net_retry_count -ResourceGroupName PowershellMySqlTest -ServerName mysql-test -Value 15

Name            Value
----            -----
net_retry_count 15
```

<span data-ttu-id="e44b9-113">Denna cmdlet uppdaterar MySql-konfigurationen efter namn.</span><span class="sxs-lookup"><span data-stu-id="e44b9-113">This cmdlet updates MySql configuration by name.</span></span>

### <span data-ttu-id="e44b9-114">Exempel 2: uppdatera MySql-konfigurationen efter identitet.</span><span class="sxs-lookup"><span data-stu-id="e44b9-114">Example 2: Update MySql configuration by identity.</span></span>
```powershell
PS C:\> $ID = "/subscriptions/<SubscriptionId>/resourceGroups/PowershellMySqlTest/providers/Microsoft.DBforMySQL/servers/mysql-test/configurations/wait_timeout"
PS C:\> Update-AzMySqlConfiguration -InputObject $ID -Value 150

Name         Value
----         -----
wait_timeout 150
```

<span data-ttu-id="e44b9-115">Dessa cmdletar uppdaterar MySql-konfigurationen efter identitet.</span><span class="sxs-lookup"><span data-stu-id="e44b9-115">These cmdlets update MySql configuration by identity.</span></span>

## <span data-ttu-id="e44b9-116">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="e44b9-116">PARAMETERS</span></span>

### <span data-ttu-id="e44b9-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e44b9-117">-AsJob</span></span>
<span data-ttu-id="e44b9-118">Köra kommandot som ett jobb</span><span class="sxs-lookup"><span data-stu-id="e44b9-118">Run the command as a job</span></span>

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

### <span data-ttu-id="e44b9-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e44b9-119">-DefaultProfile</span></span>
<span data-ttu-id="e44b9-120">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="e44b9-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e44b9-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e44b9-121">-InputObject</span></span>
<span data-ttu-id="e44b9-122">Identitets parameter.</span><span class="sxs-lookup"><span data-stu-id="e44b9-122">Identity Parameter.</span></span>
<span data-ttu-id="e44b9-123">För att konstruera kan du läsa avsnittet anteckningar för INPUTOBJECT-egenskaper och skapa en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="e44b9-123">To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="e44b9-124">-Namn</span><span class="sxs-lookup"><span data-stu-id="e44b9-124">-Name</span></span>
<span data-ttu-id="e44b9-125">Server konfigurationens namn.</span><span class="sxs-lookup"><span data-stu-id="e44b9-125">The name of the server configuration.</span></span>

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

### <span data-ttu-id="e44b9-126">-Nowait</span><span class="sxs-lookup"><span data-stu-id="e44b9-126">-NoWait</span></span>
<span data-ttu-id="e44b9-127">Kör kommandot asynkront</span><span class="sxs-lookup"><span data-stu-id="e44b9-127">Run the command asynchronously</span></span>

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

### <span data-ttu-id="e44b9-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e44b9-128">-ResourceGroupName</span></span>
<span data-ttu-id="e44b9-129">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="e44b9-129">The name of the resource group.</span></span>
<span data-ttu-id="e44b9-130">Namnet är Skift läges okänsligt.</span><span class="sxs-lookup"><span data-stu-id="e44b9-130">The name is case insensitive.</span></span>

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

### <span data-ttu-id="e44b9-131">-ServerName</span><span class="sxs-lookup"><span data-stu-id="e44b9-131">-ServerName</span></span>
<span data-ttu-id="e44b9-132">Namnet på servern.</span><span class="sxs-lookup"><span data-stu-id="e44b9-132">The name of the server.</span></span>

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

### <span data-ttu-id="e44b9-133">-Källa</span><span class="sxs-lookup"><span data-stu-id="e44b9-133">-Source</span></span>
<span data-ttu-id="e44b9-134">Källa för konfigurationen.</span><span class="sxs-lookup"><span data-stu-id="e44b9-134">Source of the configuration.</span></span>

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

### <span data-ttu-id="e44b9-135">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="e44b9-135">-SubscriptionId</span></span>
<span data-ttu-id="e44b9-136">ID för mål prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="e44b9-136">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="e44b9-137">-Värde</span><span class="sxs-lookup"><span data-stu-id="e44b9-137">-Value</span></span>
<span data-ttu-id="e44b9-138">Konfigurationens värde.</span><span class="sxs-lookup"><span data-stu-id="e44b9-138">Value of the configuration.</span></span>

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

### <span data-ttu-id="e44b9-139">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="e44b9-139">-Confirm</span></span>
<span data-ttu-id="e44b9-140">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="e44b9-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e44b9-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e44b9-141">-WhatIf</span></span>
<span data-ttu-id="e44b9-142">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="e44b9-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e44b9-143">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="e44b9-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e44b9-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e44b9-144">CommonParameters</span></span>
<span data-ttu-id="e44b9-145">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e44b9-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e44b9-146">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e44b9-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e44b9-147">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="e44b9-147">INPUTS</span></span>

### <span data-ttu-id="e44b9-148">Microsoft. Azure. PowerShell. cmdletar. MySql. Models. IMySqlIdentity</span><span class="sxs-lookup"><span data-stu-id="e44b9-148">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity</span></span>

## <span data-ttu-id="e44b9-149">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="e44b9-149">OUTPUTS</span></span>

### <span data-ttu-id="e44b9-150">Microsoft. Azure. PowerShell. cmdletar. MySql. Models. Api20171201. IConfiguration</span><span class="sxs-lookup"><span data-stu-id="e44b9-150">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20171201.IConfiguration</span></span>

## <span data-ttu-id="e44b9-151">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="e44b9-151">NOTES</span></span>

<span data-ttu-id="e44b9-152">ALIAS</span><span class="sxs-lookup"><span data-stu-id="e44b9-152">ALIASES</span></span>

<span data-ttu-id="e44b9-153">KOMPLEXA PARAMETER EGENSKAPER</span><span class="sxs-lookup"><span data-stu-id="e44b9-153">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="e44b9-154">Skapa en hash-tabell som innehåller lämpliga egenskaper för att lägga till de parametrar som beskrivs nedan.</span><span class="sxs-lookup"><span data-stu-id="e44b9-154">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="e44b9-155">Om du vill ha information om hash-tabeller kör Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="e44b9-155">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="e44b9-156">INPUTOBJECT <IMySqlIdentity> : identitets parameter.</span><span class="sxs-lookup"><span data-stu-id="e44b9-156">INPUTOBJECT <IMySqlIdentity>: Identity Parameter.</span></span>
  - <span data-ttu-id="e44b9-157">`[ConfigurationName <String>]`: Server konfigurationens namn.</span><span class="sxs-lookup"><span data-stu-id="e44b9-157">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="e44b9-158">`[DatabaseName <String>]`: Namnet på databasen.</span><span class="sxs-lookup"><span data-stu-id="e44b9-158">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="e44b9-159">`[FirewallRuleName <String>]`: Namnet på Server brand Väggs regeln.</span><span class="sxs-lookup"><span data-stu-id="e44b9-159">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="e44b9-160">`[Id <String>]`: Sökväg till resurs identitet</span><span class="sxs-lookup"><span data-stu-id="e44b9-160">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="e44b9-161">`[KeyName <String>]`: Server namnet.</span><span class="sxs-lookup"><span data-stu-id="e44b9-161">`[KeyName <String>]`: The name of the server key.</span></span>
  - <span data-ttu-id="e44b9-162">`[LocationName <String>]`: Namnet på platsen.</span><span class="sxs-lookup"><span data-stu-id="e44b9-162">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="e44b9-163">`[ResourceGroupName <String>]`: Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="e44b9-163">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="e44b9-164">Namnet är Skift läges okänsligt.</span><span class="sxs-lookup"><span data-stu-id="e44b9-164">The name is case insensitive.</span></span>
  - <span data-ttu-id="e44b9-165">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: Namnet på säkerhets varnings principen.</span><span class="sxs-lookup"><span data-stu-id="e44b9-165">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="e44b9-166">`[ServerName <String>]`: Namnet på servern.</span><span class="sxs-lookup"><span data-stu-id="e44b9-166">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="e44b9-167">`[SubscriptionId <String>]`: Mål prenumerationens ID.</span><span class="sxs-lookup"><span data-stu-id="e44b9-167">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="e44b9-168">`[VirtualNetworkRuleName <String>]`: Namnet på den virtuella nätverks regeln.</span><span class="sxs-lookup"><span data-stu-id="e44b9-168">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="e44b9-169">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="e44b9-169">RELATED LINKS</span></span>

