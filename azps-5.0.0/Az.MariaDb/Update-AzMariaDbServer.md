---
external help file: ''
Module Name: Az.MariaDb
online version: https://docs.microsoft.com/en-us/powershell/module/az.mariadb/update-azmariadbserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/Update-AzMariaDbServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/Update-AzMariaDbServer.md
ms.openlocfilehash: 0a6286c7574a2bf7226f8d4b80a5cac62c535a47
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94273320"
---
# <span data-ttu-id="22147-101">Update-AzMariaDbServer</span><span class="sxs-lookup"><span data-stu-id="22147-101">Update-AzMariaDbServer</span></span>

## <span data-ttu-id="22147-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="22147-102">SYNOPSIS</span></span>
<span data-ttu-id="22147-103">Uppdaterar en befintlig server.</span><span class="sxs-lookup"><span data-stu-id="22147-103">Updates an existing server.</span></span>
<span data-ttu-id="22147-104">Meddelande texten kan innehålla en till många av de egenskaper som finns i Server definitionen för normal.</span><span class="sxs-lookup"><span data-stu-id="22147-104">The request body can contain one to many of the properties present in the normal server definition.</span></span>
<span data-ttu-id="22147-105">Använd Update-AzMariaDbConfiguration istället om du vill uppdatera Server parametrar som wait_timeout eller net_retry_count.</span><span class="sxs-lookup"><span data-stu-id="22147-105">Use Update-AzMariaDbConfiguration instead if you want update server parameters such as wait_timeout or net_retry_count.</span></span>

## <span data-ttu-id="22147-106">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="22147-106">SYNTAX</span></span>

### <span data-ttu-id="22147-107">Server namn (standard)</span><span class="sxs-lookup"><span data-stu-id="22147-107">ServerName (Default)</span></span>
```
Update-AzMariaDbServer -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-AdministratorLoginPassword <SecureString>] [-BackupRetentionDay <Int32>]
 [-GeoRedundantBackup <GeoRedundantBackup>] [-ReplicationRole <String>] [-Sku <String>]
 [-SslEnforcement <SslEnforcementEnum>] [-StorageAutogrow <StorageAutogrow>] [-StorageInMb <Int32>]
 [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="22147-108">ServerObject</span><span class="sxs-lookup"><span data-stu-id="22147-108">ServerObject</span></span>
```
Update-AzMariaDbServer -InputObject <IMariaDbIdentity> [-AdministratorLoginPassword <SecureString>]
 [-BackupRetentionDay <Int32>] [-GeoRedundantBackup <GeoRedundantBackup>] [-ReplicationRole <String>]
 [-Sku <String>] [-SslEnforcement <SslEnforcementEnum>] [-StorageAutogrow <StorageAutogrow>]
 [-StorageInMb <Int32>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="22147-109">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="22147-109">DESCRIPTION</span></span>
<span data-ttu-id="22147-110">Uppdaterar en befintlig server.</span><span class="sxs-lookup"><span data-stu-id="22147-110">Updates an existing server.</span></span>
<span data-ttu-id="22147-111">Meddelande texten kan innehålla en till många av de egenskaper som finns i Server definitionen för normal.</span><span class="sxs-lookup"><span data-stu-id="22147-111">The request body can contain one to many of the properties present in the normal server definition.</span></span>
<span data-ttu-id="22147-112">Använd Update-AzMariaDbConfiguration istället om du vill uppdatera Server parametrar som wait_timeout eller net_retry_count.</span><span class="sxs-lookup"><span data-stu-id="22147-112">Use Update-AzMariaDbConfiguration instead if you want update server parameters such as wait_timeout or net_retry_count.</span></span>

## <span data-ttu-id="22147-113">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="22147-113">EXAMPLES</span></span>

### <span data-ttu-id="22147-114">Exempel 1: uppdatera MariaDB</span><span class="sxs-lookup"><span data-stu-id="22147-114">Example 1: Update MariaDB</span></span>
```powershell
PS C:\> Update-AzMariaDbServer -Name mariadb-test-4rmtig -ResourceGroupName mariadb-test-qu5ov0 -StorageInMb 8192

Name                Location AdministratorLogin Version StorageProfileStorageMb SkuName  SkuTier SslEnforcement
----                -------- ------------------ ------- ----------------------- -------  ------- --------------
mariadb-test-4rmtig eastus   xofavpndqj         10.2    8192                    B_Gen5_1 Basic   Enabled
```

<span data-ttu-id="22147-115">Det här kommandot uppdaterar en MariaDB.</span><span class="sxs-lookup"><span data-stu-id="22147-115">This command updates a MariaDB.</span></span>

### <span data-ttu-id="22147-116">Exempel 2: Update MariaDB</span><span class="sxs-lookup"><span data-stu-id="22147-116">Example 2: Update MariaDB</span></span>
```powershell
PS C:\> Get-AzMariaDbServer -Name mariadb-test-4rmtig -ResourceGroupName mariadb-test-qu5ov0 | Update-AzMariaDbServer -StorageInMb (8192+1024)

Name                Location AdministratorLogin Version StorageProfileStorageMb SkuName  SkuTier SslEnforcement
----                -------- ------------------ ------- ----------------------- -------  ------- --------------
mariadb-test-4rmtig eastus   xofavpndqj         10.2    9216                    B_Gen5_1 Basic   Enabled
```

<span data-ttu-id="22147-117">Det här kommandot uppdaterar en MariaDB.</span><span class="sxs-lookup"><span data-stu-id="22147-117">This command updates a MariaDB.</span></span>

## <span data-ttu-id="22147-118">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="22147-118">PARAMETERS</span></span>

### <span data-ttu-id="22147-119">-AdministratorLoginPassword</span><span class="sxs-lookup"><span data-stu-id="22147-119">-AdministratorLoginPassword</span></span>
<span data-ttu-id="22147-120">Lösen ordet för administratörs inloggningen.</span><span class="sxs-lookup"><span data-stu-id="22147-120">The password of the administrator login.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="22147-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="22147-121">-AsJob</span></span>
<span data-ttu-id="22147-122">Köra kommandot som ett jobb</span><span class="sxs-lookup"><span data-stu-id="22147-122">Run the command as a job</span></span>

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

### <span data-ttu-id="22147-123">-BackupRetentionDay</span><span class="sxs-lookup"><span data-stu-id="22147-123">-BackupRetentionDay</span></span>
<span data-ttu-id="22147-124">Dagar för säkerhets kopiering av Server.</span><span class="sxs-lookup"><span data-stu-id="22147-124">Backup retention days for the server.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="22147-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="22147-125">-DefaultProfile</span></span>
<span data-ttu-id="22147-126">regionen DefaultParameters autentiseringsuppgifterna, kontot, innehavaren och prenumerationen som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="22147-126">region DefaultParameters The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="22147-127">-GeoRedundantBackup</span><span class="sxs-lookup"><span data-stu-id="22147-127">-GeoRedundantBackup</span></span>
<span data-ttu-id="22147-128">Aktivera Geo-redundant eller inte för säkerhets kopiering av Server.</span><span class="sxs-lookup"><span data-stu-id="22147-128">Enable Geo-redundant or not for server backup.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Support.GeoRedundantBackup
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="22147-129">-InputObject</span><span class="sxs-lookup"><span data-stu-id="22147-129">-InputObject</span></span>
<span data-ttu-id="22147-130">Identitets parameter för att konstruera, se avsnittet anteckningar för INPUTOBJECT-egenskaper och skapa en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="22147-130">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.IMariaDbIdentity
Parameter Sets: ServerObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="22147-131">-Namn</span><span class="sxs-lookup"><span data-stu-id="22147-131">-Name</span></span>
<span data-ttu-id="22147-132">MariaDB Server namn</span><span class="sxs-lookup"><span data-stu-id="22147-132">MariaDB server name</span></span>

```yaml
Type: System.String
Parameter Sets: ServerName
Aliases: ServerName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="22147-133">-Nowait</span><span class="sxs-lookup"><span data-stu-id="22147-133">-NoWait</span></span>
<span data-ttu-id="22147-134">Kör kommandot asynkront</span><span class="sxs-lookup"><span data-stu-id="22147-134">Run the command asynchronously</span></span>

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

### <span data-ttu-id="22147-135">-ReplicationRole</span><span class="sxs-lookup"><span data-stu-id="22147-135">-ReplicationRole</span></span>
<span data-ttu-id="22147-136">Serverns replikeringsrelation.</span><span class="sxs-lookup"><span data-stu-id="22147-136">The replication role of the server.</span></span>

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

### <span data-ttu-id="22147-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="22147-137">-ResourceGroupName</span></span>
<span data-ttu-id="22147-138">Namnet på resurs gruppen som innehåller resursen.</span><span class="sxs-lookup"><span data-stu-id="22147-138">The name of the resource group that contains the resource.</span></span>

```yaml
Type: System.String
Parameter Sets: ServerName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="22147-139">-SKU</span><span class="sxs-lookup"><span data-stu-id="22147-139">-Sku</span></span>
<span data-ttu-id="22147-140">Namnet på SKU: n, vanligt vis nivå + Family + cores, till exempel B_Gen4_1 GP_Gen5_8.</span><span class="sxs-lookup"><span data-stu-id="22147-140">The name of the sku, typically, tier + family + cores, e.g. B_Gen4_1, GP_Gen5_8.</span></span>

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

### <span data-ttu-id="22147-141">-SslEnforcement</span><span class="sxs-lookup"><span data-stu-id="22147-141">-SslEnforcement</span></span>
<span data-ttu-id="22147-142">Aktivera SSL-tvång eller inte vid anslutning till server.</span><span class="sxs-lookup"><span data-stu-id="22147-142">Enable ssl enforcement or not when connect to server.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Support.SslEnforcementEnum
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="22147-143">-StorageAutogrow</span><span class="sxs-lookup"><span data-stu-id="22147-143">-StorageAutogrow</span></span>
<span data-ttu-id="22147-144">Aktivera automatisk tillväxt av lagring.</span><span class="sxs-lookup"><span data-stu-id="22147-144">Enable Storage Auto Grow.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Support.StorageAutogrow
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="22147-145">-StorageInMb</span><span class="sxs-lookup"><span data-stu-id="22147-145">-StorageInMb</span></span>
<span data-ttu-id="22147-146">Högsta tillåtna lagrings utrymme för en server.</span><span class="sxs-lookup"><span data-stu-id="22147-146">Max storage allowed for a server.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="22147-147">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="22147-147">-SubscriptionId</span></span>
<span data-ttu-id="22147-148">Prenumerations-ID är en del av URI: n för varje service samtal</span><span class="sxs-lookup"><span data-stu-id="22147-148">The subscription ID is part of the URI for every service call</span></span>

```yaml
Type: System.String
Parameter Sets: ServerName
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="22147-149">-Tagg</span><span class="sxs-lookup"><span data-stu-id="22147-149">-Tag</span></span>
<span data-ttu-id="22147-150">Programspecifika metadata i form av par med nyckelvärdena.</span><span class="sxs-lookup"><span data-stu-id="22147-150">Application-specific metadata in the form of key-value pairs.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="22147-151">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="22147-151">-Confirm</span></span>
<span data-ttu-id="22147-152">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="22147-152">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="22147-153">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="22147-153">-WhatIf</span></span>
<span data-ttu-id="22147-154">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="22147-154">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="22147-155">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="22147-155">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="22147-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="22147-156">CommonParameters</span></span>
<span data-ttu-id="22147-157">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="22147-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="22147-158">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="22147-158">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="22147-159">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="22147-159">INPUTS</span></span>

### <span data-ttu-id="22147-160">Microsoft. Azure. PowerShell. cmdletar. MariaDb. Models. IMariaDbIdentity</span><span class="sxs-lookup"><span data-stu-id="22147-160">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.IMariaDbIdentity</span></span>

## <span data-ttu-id="22147-161">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="22147-161">OUTPUTS</span></span>

### <span data-ttu-id="22147-162">Microsoft. Azure. PowerShell. cmdletar. MariaDb. Models. Api20180601Preview. IServer</span><span class="sxs-lookup"><span data-stu-id="22147-162">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.Api20180601Preview.IServer</span></span>

## <span data-ttu-id="22147-163">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="22147-163">NOTES</span></span>

<span data-ttu-id="22147-164">ALIAS</span><span class="sxs-lookup"><span data-stu-id="22147-164">ALIASES</span></span>

<span data-ttu-id="22147-165">KOMPLEXA PARAMETER EGENSKAPER</span><span class="sxs-lookup"><span data-stu-id="22147-165">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="22147-166">Skapa en hash-tabell som innehåller lämpliga egenskaper för att lägga till de parametrar som beskrivs nedan.</span><span class="sxs-lookup"><span data-stu-id="22147-166">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="22147-167">Om du vill ha information om hash-tabeller kör Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="22147-167">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="22147-168">INPUTOBJECT <IMariaDbIdentity> : identitets parameter</span><span class="sxs-lookup"><span data-stu-id="22147-168">INPUTOBJECT <IMariaDbIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="22147-169">`[ConfigurationName <String>]`: Server konfigurationens namn.</span><span class="sxs-lookup"><span data-stu-id="22147-169">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="22147-170">`[DatabaseName <String>]`: Namnet på databasen.</span><span class="sxs-lookup"><span data-stu-id="22147-170">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="22147-171">`[FirewallRuleName <String>]`: Namnet på Server brand Väggs regeln.</span><span class="sxs-lookup"><span data-stu-id="22147-171">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="22147-172">`[Id <String>]`: Sökväg till resurs identitet</span><span class="sxs-lookup"><span data-stu-id="22147-172">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="22147-173">`[LocationName <String>]`: Namnet på platsen.</span><span class="sxs-lookup"><span data-stu-id="22147-173">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="22147-174">`[ResourceGroupName <String>]`: Namnet på resurs gruppen som innehåller resursen.</span><span class="sxs-lookup"><span data-stu-id="22147-174">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="22147-175">Det här värdet kan hämtas från Azure Resource Manager API eller till portalen.</span><span class="sxs-lookup"><span data-stu-id="22147-175">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="22147-176">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: Namnet på säkerhets varnings principen.</span><span class="sxs-lookup"><span data-stu-id="22147-176">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="22147-177">`[ServerName <String>]`: Namnet på servern.</span><span class="sxs-lookup"><span data-stu-id="22147-177">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="22147-178">`[SubscriptionId <String>]`: Det prenumerations-ID som identifierar en Azure-prenumeration.</span><span class="sxs-lookup"><span data-stu-id="22147-178">`[SubscriptionId <String>]`: The subscription ID that identifies an Azure subscription.</span></span>
  - <span data-ttu-id="22147-179">`[VirtualNetworkRuleName <String>]`: Namnet på den virtuella nätverks regeln.</span><span class="sxs-lookup"><span data-stu-id="22147-179">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="22147-180">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="22147-180">RELATED LINKS</span></span>
