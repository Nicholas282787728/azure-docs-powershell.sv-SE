---
external help file: ''
Module Name: Az.MySql
online version: https://docs.microsoft.com/en-us/powershell/module/az.mysql/update-azmysqlconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Update-AzMySqlConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Update-AzMySqlConfiguration.md
ms.openlocfilehash: c4eb244dd2d1a0d685bf18f39deedf9992b5597e
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94102207"
---
# <span data-ttu-id="4ab8f-101">Update-AzMySqlConfiguration</span><span class="sxs-lookup"><span data-stu-id="4ab8f-101">Update-AzMySqlConfiguration</span></span>

## <span data-ttu-id="4ab8f-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="4ab8f-102">SYNOPSIS</span></span>
<span data-ttu-id="4ab8f-103">Uppdaterar en servers konfiguration.</span><span class="sxs-lookup"><span data-stu-id="4ab8f-103">Updates a configuration of a server.</span></span>
<span data-ttu-id="4ab8f-104">Använd Update-AzMySqlServer istället om du vill uppdatera AdministratorLoginPassword, SKU etc.</span><span class="sxs-lookup"><span data-stu-id="4ab8f-104">Use Update-AzMySqlServer instead if you want update AdministratorLoginPassword, sku, etc.</span></span>

## <span data-ttu-id="4ab8f-105">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="4ab8f-105">SYNTAX</span></span>

### <span data-ttu-id="4ab8f-106">UpdateExpanded (standard)</span><span class="sxs-lookup"><span data-stu-id="4ab8f-106">UpdateExpanded (Default)</span></span>
```
Update-AzMySqlConfiguration -Name <String> -ResourceGroupName <String> -ServerName <String>
 [-SubscriptionId <String>] [-Source <String>] [-Value <String>] [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="4ab8f-107">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="4ab8f-107">UpdateViaIdentityExpanded</span></span>
```
Update-AzMySqlConfiguration -InputObject <IMySqlIdentity> [-Source <String>] [-Value <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="4ab8f-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="4ab8f-108">DESCRIPTION</span></span>
<span data-ttu-id="4ab8f-109">Uppdaterar en servers konfiguration.</span><span class="sxs-lookup"><span data-stu-id="4ab8f-109">Updates a configuration of a server.</span></span>
<span data-ttu-id="4ab8f-110">Använd Update-AzMySqlServer istället om du vill uppdatera AdministratorLoginPassword, SKU etc.</span><span class="sxs-lookup"><span data-stu-id="4ab8f-110">Use Update-AzMySqlServer instead if you want update AdministratorLoginPassword, sku, etc.</span></span>

## <span data-ttu-id="4ab8f-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="4ab8f-111">EXAMPLES</span></span>

### <span data-ttu-id="4ab8f-112">Exempel 1: uppdatera MySql-konfigurationen efter namn</span><span class="sxs-lookup"><span data-stu-id="4ab8f-112">Example 1: Update MySql configuration by name</span></span>
```powershell
PS C:\> Update-AzMySqlConfiguration -Name net_retry_count -ResourceGroupName PowershellMySqlTest -ServerName mysql-test -Value 15

Name            Value
----            -----
net_retry_count 15
```

<span data-ttu-id="4ab8f-113">Denna cmdlet uppdaterar MySql-konfigurationen efter namn.</span><span class="sxs-lookup"><span data-stu-id="4ab8f-113">This cmdlet updates MySql configuration by name.</span></span>

### <span data-ttu-id="4ab8f-114">Exempel 2: uppdatera MySql-konfigurationen efter identitet.</span><span class="sxs-lookup"><span data-stu-id="4ab8f-114">Example 2: Update MySql configuration by identity.</span></span>
```powershell
PS C:\> $ID = "/subscriptions/<SubscriptionId>/resourceGroups/PowershellMySqlTest/providers/Microsoft.DBforMySQL/servers/mysql-test/configurations/wait_timeout"
PS C:\> Update-AzMySqlConfiguration -InputObject $ID -Value 150

Name         Value
----         -----
wait_timeout 150
```

<span data-ttu-id="4ab8f-115">Dessa cmdletar uppdaterar MySql-konfigurationen efter identitet.</span><span class="sxs-lookup"><span data-stu-id="4ab8f-115">These cmdlets update MySql configuration by identity.</span></span>

## <span data-ttu-id="4ab8f-116">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="4ab8f-116">PARAMETERS</span></span>

### <span data-ttu-id="4ab8f-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="4ab8f-117">-AsJob</span></span>
<span data-ttu-id="4ab8f-118">Köra kommandot som ett jobb</span><span class="sxs-lookup"><span data-stu-id="4ab8f-118">Run the command as a job</span></span>

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

### <span data-ttu-id="4ab8f-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4ab8f-119">-DefaultProfile</span></span>
<span data-ttu-id="4ab8f-120">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="4ab8f-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4ab8f-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4ab8f-121">-InputObject</span></span>
<span data-ttu-id="4ab8f-122">Identitets parameter.</span><span class="sxs-lookup"><span data-stu-id="4ab8f-122">Identity Parameter.</span></span>
<span data-ttu-id="4ab8f-123">För att konstruera kan du läsa avsnittet anteckningar för INPUTOBJECT-egenskaper och skapa en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="4ab8f-123">To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="4ab8f-124">-Namn</span><span class="sxs-lookup"><span data-stu-id="4ab8f-124">-Name</span></span>
<span data-ttu-id="4ab8f-125">Server konfigurationens namn.</span><span class="sxs-lookup"><span data-stu-id="4ab8f-125">The name of the server configuration.</span></span>

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

### <span data-ttu-id="4ab8f-126">-Nowait</span><span class="sxs-lookup"><span data-stu-id="4ab8f-126">-NoWait</span></span>
<span data-ttu-id="4ab8f-127">Kör kommandot asynkront</span><span class="sxs-lookup"><span data-stu-id="4ab8f-127">Run the command asynchronously</span></span>

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

### <span data-ttu-id="4ab8f-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4ab8f-128">-ResourceGroupName</span></span>
<span data-ttu-id="4ab8f-129">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="4ab8f-129">The name of the resource group.</span></span>
<span data-ttu-id="4ab8f-130">Namnet är Skift läges okänsligt.</span><span class="sxs-lookup"><span data-stu-id="4ab8f-130">The name is case insensitive.</span></span>

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

### <span data-ttu-id="4ab8f-131">-ServerName</span><span class="sxs-lookup"><span data-stu-id="4ab8f-131">-ServerName</span></span>
<span data-ttu-id="4ab8f-132">Namnet på servern.</span><span class="sxs-lookup"><span data-stu-id="4ab8f-132">The name of the server.</span></span>

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

### <span data-ttu-id="4ab8f-133">-Källa</span><span class="sxs-lookup"><span data-stu-id="4ab8f-133">-Source</span></span>
<span data-ttu-id="4ab8f-134">Källa för konfigurationen.</span><span class="sxs-lookup"><span data-stu-id="4ab8f-134">Source of the configuration.</span></span>

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

### <span data-ttu-id="4ab8f-135">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="4ab8f-135">-SubscriptionId</span></span>
<span data-ttu-id="4ab8f-136">ID för mål prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="4ab8f-136">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="4ab8f-137">-Värde</span><span class="sxs-lookup"><span data-stu-id="4ab8f-137">-Value</span></span>
<span data-ttu-id="4ab8f-138">Konfigurationens värde.</span><span class="sxs-lookup"><span data-stu-id="4ab8f-138">Value of the configuration.</span></span>

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

### <span data-ttu-id="4ab8f-139">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="4ab8f-139">-Confirm</span></span>
<span data-ttu-id="4ab8f-140">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="4ab8f-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4ab8f-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4ab8f-141">-WhatIf</span></span>
<span data-ttu-id="4ab8f-142">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="4ab8f-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4ab8f-143">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="4ab8f-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4ab8f-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4ab8f-144">CommonParameters</span></span>
<span data-ttu-id="4ab8f-145">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4ab8f-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4ab8f-146">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="4ab8f-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4ab8f-147">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="4ab8f-147">INPUTS</span></span>

### <span data-ttu-id="4ab8f-148">Microsoft. Azure. PowerShell. cmdletar. MySql. Models. IMySqlIdentity</span><span class="sxs-lookup"><span data-stu-id="4ab8f-148">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity</span></span>

## <span data-ttu-id="4ab8f-149">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="4ab8f-149">OUTPUTS</span></span>

### <span data-ttu-id="4ab8f-150">Microsoft. Azure. PowerShell. cmdletar. MySql. Models. Api20171201. IConfiguration</span><span class="sxs-lookup"><span data-stu-id="4ab8f-150">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20171201.IConfiguration</span></span>

## <span data-ttu-id="4ab8f-151">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="4ab8f-151">NOTES</span></span>

<span data-ttu-id="4ab8f-152">ALIAS</span><span class="sxs-lookup"><span data-stu-id="4ab8f-152">ALIASES</span></span>

<span data-ttu-id="4ab8f-153">KOMPLEXA PARAMETER EGENSKAPER</span><span class="sxs-lookup"><span data-stu-id="4ab8f-153">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="4ab8f-154">Skapa en hash-tabell som innehåller lämpliga egenskaper för att lägga till de parametrar som beskrivs nedan.</span><span class="sxs-lookup"><span data-stu-id="4ab8f-154">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="4ab8f-155">Om du vill ha information om hash-tabeller kör Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="4ab8f-155">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="4ab8f-156">INPUTOBJECT <IMySqlIdentity> : identitets parameter.</span><span class="sxs-lookup"><span data-stu-id="4ab8f-156">INPUTOBJECT <IMySqlIdentity>: Identity Parameter.</span></span>
  - <span data-ttu-id="4ab8f-157">`[ConfigurationName <String>]`: Server konfigurationens namn.</span><span class="sxs-lookup"><span data-stu-id="4ab8f-157">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="4ab8f-158">`[DatabaseName <String>]`: Namnet på databasen.</span><span class="sxs-lookup"><span data-stu-id="4ab8f-158">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="4ab8f-159">`[FirewallRuleName <String>]`: Namnet på Server brand Väggs regeln.</span><span class="sxs-lookup"><span data-stu-id="4ab8f-159">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="4ab8f-160">`[Id <String>]`: Sökväg till resurs identitet</span><span class="sxs-lookup"><span data-stu-id="4ab8f-160">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="4ab8f-161">`[LocationName <String>]`: Namnet på platsen.</span><span class="sxs-lookup"><span data-stu-id="4ab8f-161">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="4ab8f-162">`[ResourceGroupName <String>]`: Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="4ab8f-162">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="4ab8f-163">Namnet är Skift läges okänsligt.</span><span class="sxs-lookup"><span data-stu-id="4ab8f-163">The name is case insensitive.</span></span>
  - <span data-ttu-id="4ab8f-164">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: Namnet på säkerhets varnings principen.</span><span class="sxs-lookup"><span data-stu-id="4ab8f-164">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="4ab8f-165">`[ServerName <String>]`: Namnet på servern.</span><span class="sxs-lookup"><span data-stu-id="4ab8f-165">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="4ab8f-166">`[SubscriptionId <String>]`: Mål prenumerationens ID.</span><span class="sxs-lookup"><span data-stu-id="4ab8f-166">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="4ab8f-167">`[VirtualNetworkRuleName <String>]`: Namnet på den virtuella nätverks regeln.</span><span class="sxs-lookup"><span data-stu-id="4ab8f-167">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="4ab8f-168">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="4ab8f-168">RELATED LINKS</span></span>

