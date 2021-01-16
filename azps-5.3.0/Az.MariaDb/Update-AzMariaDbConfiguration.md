---
external help file: ''
Module Name: Az.MariaDb
online version: https://docs.microsoft.com/en-us/powershell/module/az.mariadb/update-azmariadbconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/Update-AzMariaDbConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/Update-AzMariaDbConfiguration.md
ms.openlocfilehash: 4ee32822f6fb4872a9fa01d020ed0f0bf92b0456
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98523454"
---
# <span data-ttu-id="4bfb4-101">Update-AzMariaDbConfiguration</span><span class="sxs-lookup"><span data-stu-id="4bfb4-101">Update-AzMariaDbConfiguration</span></span>

## <span data-ttu-id="4bfb4-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="4bfb4-102">SYNOPSIS</span></span>
<span data-ttu-id="4bfb4-103">Uppdaterar en servers konfiguration.</span><span class="sxs-lookup"><span data-stu-id="4bfb4-103">Updates a configuration of a server.</span></span>
<span data-ttu-id="4bfb4-104">Använd Update-AzMariaDbServer istället om du vill uppdatera AdministratorLoginPassword, SKU etc.</span><span class="sxs-lookup"><span data-stu-id="4bfb4-104">Use Update-AzMariaDbServer instead if you want update AdministratorLoginPassword, sku, etc.</span></span>

## <span data-ttu-id="4bfb4-105">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="4bfb4-105">SYNTAX</span></span>

### <span data-ttu-id="4bfb4-106">UpdateExpanded (standard)</span><span class="sxs-lookup"><span data-stu-id="4bfb4-106">UpdateExpanded (Default)</span></span>
```
Update-AzMariaDbConfiguration -Name <String> -ResourceGroupName <String> -ServerName <String>
 [-SubscriptionId <String>] [-Source <String>] [-Value <String>] [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="4bfb4-107">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="4bfb4-107">UpdateViaIdentityExpanded</span></span>
```
Update-AzMariaDbConfiguration -InputObject <IMariaDbIdentity> [-Source <String>] [-Value <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="4bfb4-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="4bfb4-108">DESCRIPTION</span></span>
<span data-ttu-id="4bfb4-109">Uppdaterar en servers konfiguration.</span><span class="sxs-lookup"><span data-stu-id="4bfb4-109">Updates a configuration of a server.</span></span>
<span data-ttu-id="4bfb4-110">Använd Update-AzMariaDberver istället om du vill uppdatera AdministratorLoginPassword, SKU etc.</span><span class="sxs-lookup"><span data-stu-id="4bfb4-110">Use Update-AzMariaDberver instead if you want update AdministratorLoginPassword, sku, etc.</span></span>

## <span data-ttu-id="4bfb4-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="4bfb4-111">EXAMPLES</span></span>

### <span data-ttu-id="4bfb4-112">Exempel 1: uppdatera MariaDB-konfiguration</span><span class="sxs-lookup"><span data-stu-id="4bfb4-112">Example 1: Update MariaDB configuration</span></span>
```powershell
PS C:\> Update-AzMariaDbConfiguration -Name delayed_insert_timeout -Value 200 -ServerName mariadb-test-h3pame -ResourceGroupName mariadb-test-qu5ov0 

Name                   Type
----                   ----
delayed_insert_timeout Microsoft.DBforMariaDB/servers/configurations
```

<span data-ttu-id="4bfb4-113">Det här kommandot uppdaterar en MariaDB-konfiguration.</span><span class="sxs-lookup"><span data-stu-id="4bfb4-113">This command updates a MariaDB configuration.</span></span>

## <span data-ttu-id="4bfb4-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="4bfb4-114">PARAMETERS</span></span>

### <span data-ttu-id="4bfb4-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="4bfb4-115">-AsJob</span></span>
<span data-ttu-id="4bfb4-116">Köra kommandot som ett jobb</span><span class="sxs-lookup"><span data-stu-id="4bfb4-116">Run the command as a job</span></span>

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

### <span data-ttu-id="4bfb4-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4bfb4-117">-DefaultProfile</span></span>
<span data-ttu-id="4bfb4-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="4bfb4-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4bfb4-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4bfb4-119">-InputObject</span></span>
<span data-ttu-id="4bfb4-120">Identitets parameter för att konstruera, se avsnittet anteckningar för INPUTOBJECT-egenskaper och skapa en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="4bfb4-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.IMariaDbIdentity
Parameter Sets: UpdateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4bfb4-121">-Namn</span><span class="sxs-lookup"><span data-stu-id="4bfb4-121">-Name</span></span>
<span data-ttu-id="4bfb4-122">Server konfigurationens namn.</span><span class="sxs-lookup"><span data-stu-id="4bfb4-122">The name of the server configuration.</span></span>

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

### <span data-ttu-id="4bfb4-123">-Nowait</span><span class="sxs-lookup"><span data-stu-id="4bfb4-123">-NoWait</span></span>
<span data-ttu-id="4bfb4-124">Kör kommandot asynkront</span><span class="sxs-lookup"><span data-stu-id="4bfb4-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="4bfb4-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4bfb4-125">-ResourceGroupName</span></span>
<span data-ttu-id="4bfb4-126">Namnet på resurs gruppen som innehåller resursen.</span><span class="sxs-lookup"><span data-stu-id="4bfb4-126">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="4bfb4-127">Det här värdet kan hämtas från Azure Resource Manager API eller till portalen.</span><span class="sxs-lookup"><span data-stu-id="4bfb4-127">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="4bfb4-128">-ServerName</span><span class="sxs-lookup"><span data-stu-id="4bfb4-128">-ServerName</span></span>
<span data-ttu-id="4bfb4-129">Namnet på servern.</span><span class="sxs-lookup"><span data-stu-id="4bfb4-129">The name of the server.</span></span>

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

### <span data-ttu-id="4bfb4-130">-Källa</span><span class="sxs-lookup"><span data-stu-id="4bfb4-130">-Source</span></span>
<span data-ttu-id="4bfb4-131">Källa för konfigurationen.</span><span class="sxs-lookup"><span data-stu-id="4bfb4-131">Source of the configuration.</span></span>

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

### <span data-ttu-id="4bfb4-132">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="4bfb4-132">-SubscriptionId</span></span>
<span data-ttu-id="4bfb4-133">Det prenumerations-ID som identifierar en Azure-prenumeration.</span><span class="sxs-lookup"><span data-stu-id="4bfb4-133">The subscription ID that identifies an Azure subscription.</span></span>

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

### <span data-ttu-id="4bfb4-134">-Värde</span><span class="sxs-lookup"><span data-stu-id="4bfb4-134">-Value</span></span>
<span data-ttu-id="4bfb4-135">Konfigurationens värde.</span><span class="sxs-lookup"><span data-stu-id="4bfb4-135">Value of the configuration.</span></span>

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

### <span data-ttu-id="4bfb4-136">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="4bfb4-136">-Confirm</span></span>
<span data-ttu-id="4bfb4-137">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="4bfb4-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4bfb4-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4bfb4-138">-WhatIf</span></span>
<span data-ttu-id="4bfb4-139">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="4bfb4-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4bfb4-140">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="4bfb4-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4bfb4-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4bfb4-141">CommonParameters</span></span>
<span data-ttu-id="4bfb4-142">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4bfb4-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4bfb4-143">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="4bfb4-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4bfb4-144">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="4bfb4-144">INPUTS</span></span>

### <span data-ttu-id="4bfb4-145">Microsoft. Azure. PowerShell. cmdletar. MariaDb. Models. IMariaDbIdentity</span><span class="sxs-lookup"><span data-stu-id="4bfb4-145">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.IMariaDbIdentity</span></span>

## <span data-ttu-id="4bfb4-146">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="4bfb4-146">OUTPUTS</span></span>

### <span data-ttu-id="4bfb4-147">Microsoft. Azure. PowerShell. cmdletar. MariaDb. Models. Api20180601Preview. IConfiguration</span><span class="sxs-lookup"><span data-stu-id="4bfb4-147">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.Api20180601Preview.IConfiguration</span></span>

## <span data-ttu-id="4bfb4-148">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="4bfb4-148">NOTES</span></span>

<span data-ttu-id="4bfb4-149">ALIAS</span><span class="sxs-lookup"><span data-stu-id="4bfb4-149">ALIASES</span></span>

<span data-ttu-id="4bfb4-150">KOMPLEXA PARAMETER EGENSKAPER</span><span class="sxs-lookup"><span data-stu-id="4bfb4-150">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="4bfb4-151">Skapa en hash-tabell som innehåller lämpliga egenskaper för att lägga till de parametrar som beskrivs nedan.</span><span class="sxs-lookup"><span data-stu-id="4bfb4-151">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="4bfb4-152">Om du vill ha information om hash-tabeller kör Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="4bfb4-152">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="4bfb4-153">INPUTOBJECT <IMariaDbIdentity> : identitets parameter</span><span class="sxs-lookup"><span data-stu-id="4bfb4-153">INPUTOBJECT <IMariaDbIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="4bfb4-154">`[ConfigurationName <String>]`: Server konfigurationens namn.</span><span class="sxs-lookup"><span data-stu-id="4bfb4-154">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="4bfb4-155">`[DatabaseName <String>]`: Namnet på databasen.</span><span class="sxs-lookup"><span data-stu-id="4bfb4-155">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="4bfb4-156">`[FirewallRuleName <String>]`: Namnet på Server brand Väggs regeln.</span><span class="sxs-lookup"><span data-stu-id="4bfb4-156">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="4bfb4-157">`[Id <String>]`: Sökväg till resurs identitet</span><span class="sxs-lookup"><span data-stu-id="4bfb4-157">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="4bfb4-158">`[LocationName <String>]`: Namnet på platsen.</span><span class="sxs-lookup"><span data-stu-id="4bfb4-158">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="4bfb4-159">`[ResourceGroupName <String>]`: Namnet på resurs gruppen som innehåller resursen.</span><span class="sxs-lookup"><span data-stu-id="4bfb4-159">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="4bfb4-160">Det här värdet kan hämtas från Azure Resource Manager API eller till portalen.</span><span class="sxs-lookup"><span data-stu-id="4bfb4-160">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="4bfb4-161">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: Namnet på säkerhets varnings principen.</span><span class="sxs-lookup"><span data-stu-id="4bfb4-161">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="4bfb4-162">`[ServerName <String>]`: Namnet på servern.</span><span class="sxs-lookup"><span data-stu-id="4bfb4-162">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="4bfb4-163">`[SubscriptionId <String>]`: Det prenumerations-ID som identifierar en Azure-prenumeration.</span><span class="sxs-lookup"><span data-stu-id="4bfb4-163">`[SubscriptionId <String>]`: The subscription ID that identifies an Azure subscription.</span></span>
  - <span data-ttu-id="4bfb4-164">`[VirtualNetworkRuleName <String>]`: Namnet på den virtuella nätverks regeln.</span><span class="sxs-lookup"><span data-stu-id="4bfb4-164">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="4bfb4-165">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="4bfb4-165">RELATED LINKS</span></span>

