---
external help file: ''
Module Name: Az.MySql
online version: https://docs.microsoft.com/en-us/powershell/module/az.mysql/update-azmysqlflexibleserverconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Update-AzMySqlFlexibleServerConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Update-AzMySqlFlexibleServerConfiguration.md
ms.openlocfilehash: 7e3c3855fb36d1dbc96b399d5348f033ca74908e
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98410904"
---
# <span data-ttu-id="54ca5-101">Update-AzMySqlFlexibleServerConfiguration</span><span class="sxs-lookup"><span data-stu-id="54ca5-101">Update-AzMySqlFlexibleServerConfiguration</span></span>

## <span data-ttu-id="54ca5-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="54ca5-102">SYNOPSIS</span></span>
<span data-ttu-id="54ca5-103">Uppdaterar information om en konfiguration av en MySQL-flexibel Server.</span><span class="sxs-lookup"><span data-stu-id="54ca5-103">Updates information about a configuration of a MySQL flexible server.</span></span>

## <span data-ttu-id="54ca5-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="54ca5-104">SYNTAX</span></span>

### <span data-ttu-id="54ca5-105">UpdateExpanded (standard)</span><span class="sxs-lookup"><span data-stu-id="54ca5-105">UpdateExpanded (Default)</span></span>
```
Update-AzMySqlFlexibleServerConfiguration -Name <String> -ResourceGroupName <String> -ServerName <String>
 [-SubscriptionId <String>] [-Source <String>] [-Value <String>] [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="54ca5-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="54ca5-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzMySqlFlexibleServerConfiguration -InputObject <IMySqlIdentity> [-Source <String>] [-Value <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="54ca5-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="54ca5-107">DESCRIPTION</span></span>
<span data-ttu-id="54ca5-108">Uppdaterar information om en konfiguration av en MySQL-flexibel Server.</span><span class="sxs-lookup"><span data-stu-id="54ca5-108">Updates information about a configuration of a MySQL flexible server.</span></span>

## <span data-ttu-id="54ca5-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="54ca5-109">EXAMPLES</span></span>

### <span data-ttu-id="54ca5-110">Exempel 1: uppdatera MySql-konfigurationen efter namn</span><span class="sxs-lookup"><span data-stu-id="54ca5-110">Example 1: Update MySql configuration by name</span></span>
```powershell
PS C:\> Update-AzMySqlFlexibleServer -Name net_retry_count -ResourceGroupName PowershellMySqlTest -ServerName mysql-test -Value 15

Name          Value   DefaultValue  Source        AllowedValues DataType
----          ------  ------------  -------       ------------- ---------
net_retry_count 15    10            user-override  1-4294967295   Integer
```

<span data-ttu-id="54ca5-111">Denna cmdlet uppdaterar MySql-konfigurationen efter namn.</span><span class="sxs-lookup"><span data-stu-id="54ca5-111">This cmdlet updates MySql configuration by name.</span></span>

### <span data-ttu-id="54ca5-112">Exempel 2: uppdatera MySql-konfigurationen efter identitet.</span><span class="sxs-lookup"><span data-stu-id="54ca5-112">Example 2: Update MySql configuration by identity.</span></span>
```powershell
PS C:\> $ID = "/subscriptions/<SubscriptionId>/resourceGroups/PowershellMySqlTest/providers/Microsoft.DBForMySql/flexibleServers/mysql-test/configurations/wait_timeout"
PS C:\> Update-AzMySqlFlexibleServer -InputObject $ID -Value 150

Name          Value   DefaultValue  Source        AllowedValues DataType
----          ------  ------------  -------       ------------- ---------
wait_timeout   150    28800         system-default   1-31536000   Integer
```

<span data-ttu-id="54ca5-113">Dessa cmdletar uppdaterar MySql-konfigurationen efter identitet.</span><span class="sxs-lookup"><span data-stu-id="54ca5-113">These cmdlets update MySql configuration by identity.</span></span>

## <span data-ttu-id="54ca5-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="54ca5-114">PARAMETERS</span></span>

### <span data-ttu-id="54ca5-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="54ca5-115">-AsJob</span></span>
<span data-ttu-id="54ca5-116">Köra kommandot som ett jobb</span><span class="sxs-lookup"><span data-stu-id="54ca5-116">Run the command as a job</span></span>

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

### <span data-ttu-id="54ca5-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="54ca5-117">-DefaultProfile</span></span>
<span data-ttu-id="54ca5-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="54ca5-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="54ca5-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="54ca5-119">-InputObject</span></span>
<span data-ttu-id="54ca5-120">Identitets parameter för att konstruera, se avsnittet anteckningar för INPUTOBJECT-egenskaper och skapa en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="54ca5-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="54ca5-121">-Namn</span><span class="sxs-lookup"><span data-stu-id="54ca5-121">-Name</span></span>
<span data-ttu-id="54ca5-122">Server konfigurationens namn.</span><span class="sxs-lookup"><span data-stu-id="54ca5-122">The name of the server configuration.</span></span>

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

### <span data-ttu-id="54ca5-123">-Nowait</span><span class="sxs-lookup"><span data-stu-id="54ca5-123">-NoWait</span></span>
<span data-ttu-id="54ca5-124">Kör kommandot asynkront</span><span class="sxs-lookup"><span data-stu-id="54ca5-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="54ca5-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="54ca5-125">-ResourceGroupName</span></span>
<span data-ttu-id="54ca5-126">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="54ca5-126">The name of the resource group.</span></span>
<span data-ttu-id="54ca5-127">Namnet är Skift läges okänsligt.</span><span class="sxs-lookup"><span data-stu-id="54ca5-127">The name is case insensitive.</span></span>

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

### <span data-ttu-id="54ca5-128">-ServerName</span><span class="sxs-lookup"><span data-stu-id="54ca5-128">-ServerName</span></span>
<span data-ttu-id="54ca5-129">Namnet på servern.</span><span class="sxs-lookup"><span data-stu-id="54ca5-129">The name of the server.</span></span>

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

### <span data-ttu-id="54ca5-130">-Källa</span><span class="sxs-lookup"><span data-stu-id="54ca5-130">-Source</span></span>
<span data-ttu-id="54ca5-131">Källan för uppdatering svärdet.</span><span class="sxs-lookup"><span data-stu-id="54ca5-131">The source of the updating value.</span></span>
<span data-ttu-id="54ca5-132">Standardvärdet är user-override</span><span class="sxs-lookup"><span data-stu-id="54ca5-132">The default value is user-override</span></span>

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

### <span data-ttu-id="54ca5-133">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="54ca5-133">-SubscriptionId</span></span>
<span data-ttu-id="54ca5-134">ID för mål prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="54ca5-134">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="54ca5-135">-Värde</span><span class="sxs-lookup"><span data-stu-id="54ca5-135">-Value</span></span>
<span data-ttu-id="54ca5-136">Konfigurationens värde.</span><span class="sxs-lookup"><span data-stu-id="54ca5-136">Value of the configuration.</span></span>

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

### <span data-ttu-id="54ca5-137">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="54ca5-137">-Confirm</span></span>
<span data-ttu-id="54ca5-138">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="54ca5-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="54ca5-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="54ca5-139">-WhatIf</span></span>
<span data-ttu-id="54ca5-140">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="54ca5-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="54ca5-141">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="54ca5-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="54ca5-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="54ca5-142">CommonParameters</span></span>
<span data-ttu-id="54ca5-143">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="54ca5-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="54ca5-144">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="54ca5-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="54ca5-145">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="54ca5-145">INPUTS</span></span>

### <span data-ttu-id="54ca5-146">Microsoft. Azure. PowerShell. cmdletar. MySql. Models. IMySqlIdentity</span><span class="sxs-lookup"><span data-stu-id="54ca5-146">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity</span></span>

## <span data-ttu-id="54ca5-147">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="54ca5-147">OUTPUTS</span></span>

### <span data-ttu-id="54ca5-148">Microsoft. Azure. PowerShell. cmdletar. MySql. Models. Api20200701Preview. IConfigurationAutoGenerated</span><span class="sxs-lookup"><span data-stu-id="54ca5-148">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20200701Preview.IConfigurationAutoGenerated</span></span>

## <span data-ttu-id="54ca5-149">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="54ca5-149">NOTES</span></span>

<span data-ttu-id="54ca5-150">ALIAS</span><span class="sxs-lookup"><span data-stu-id="54ca5-150">ALIASES</span></span>

<span data-ttu-id="54ca5-151">KOMPLEXA PARAMETER EGENSKAPER</span><span class="sxs-lookup"><span data-stu-id="54ca5-151">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="54ca5-152">Skapa en hash-tabell som innehåller lämpliga egenskaper för att lägga till de parametrar som beskrivs nedan.</span><span class="sxs-lookup"><span data-stu-id="54ca5-152">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="54ca5-153">Om du vill ha information om hash-tabeller kör Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="54ca5-153">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="54ca5-154">INPUTOBJECT <IMySqlIdentity> : identitets parameter</span><span class="sxs-lookup"><span data-stu-id="54ca5-154">INPUTOBJECT <IMySqlIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="54ca5-155">`[ConfigurationName <String>]`: Server konfigurationens namn.</span><span class="sxs-lookup"><span data-stu-id="54ca5-155">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="54ca5-156">`[DatabaseName <String>]`: Namnet på databasen.</span><span class="sxs-lookup"><span data-stu-id="54ca5-156">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="54ca5-157">`[FirewallRuleName <String>]`: Namnet på Server brand Väggs regeln.</span><span class="sxs-lookup"><span data-stu-id="54ca5-157">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="54ca5-158">`[Id <String>]`: Sökväg till resurs identitet</span><span class="sxs-lookup"><span data-stu-id="54ca5-158">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="54ca5-159">`[KeyName <String>]`: Server namnet.</span><span class="sxs-lookup"><span data-stu-id="54ca5-159">`[KeyName <String>]`: The name of the server key.</span></span>
  - <span data-ttu-id="54ca5-160">`[LocationName <String>]`: Namnet på platsen.</span><span class="sxs-lookup"><span data-stu-id="54ca5-160">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="54ca5-161">`[ResourceGroupName <String>]`: Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="54ca5-161">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="54ca5-162">Namnet är Skift läges okänsligt.</span><span class="sxs-lookup"><span data-stu-id="54ca5-162">The name is case insensitive.</span></span>
  - <span data-ttu-id="54ca5-163">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: Namnet på säkerhets varnings principen.</span><span class="sxs-lookup"><span data-stu-id="54ca5-163">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="54ca5-164">`[ServerName <String>]`: Namnet på servern.</span><span class="sxs-lookup"><span data-stu-id="54ca5-164">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="54ca5-165">`[SubscriptionId <String>]`: Mål prenumerationens ID.</span><span class="sxs-lookup"><span data-stu-id="54ca5-165">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="54ca5-166">`[VirtualNetworkRuleName <String>]`: Namnet på den virtuella nätverks regeln.</span><span class="sxs-lookup"><span data-stu-id="54ca5-166">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="54ca5-167">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="54ca5-167">RELATED LINKS</span></span>

