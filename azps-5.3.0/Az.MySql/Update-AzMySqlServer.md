---
external help file: ''
Module Name: Az.MySql
online version: https://docs.microsoft.com/en-us/powershell/module/az.mysql/update-azmysqlserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Update-AzMySqlServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Update-AzMySqlServer.md
ms.openlocfilehash: b205f3d4eb9b1ebce360596714ea2524fb2e3be2
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98522502"
---
# <span data-ttu-id="6d5db-101">Update-AzMySqlServer</span><span class="sxs-lookup"><span data-stu-id="6d5db-101">Update-AzMySqlServer</span></span>

## <span data-ttu-id="6d5db-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="6d5db-102">SYNOPSIS</span></span>
<span data-ttu-id="6d5db-103">Uppdaterar en befintlig server.</span><span class="sxs-lookup"><span data-stu-id="6d5db-103">Updates an existing server.</span></span>
<span data-ttu-id="6d5db-104">Meddelande texten kan innehålla en till många av de egenskaper som finns i Server definitionen för normal.</span><span class="sxs-lookup"><span data-stu-id="6d5db-104">The request body can contain one to many of the properties present in the normal server definition.</span></span>
<span data-ttu-id="6d5db-105">Använd Update-AzMySqlConfiguration istället om du vill uppdatera Server parametrar som wait_timeout eller net_retry_count.</span><span class="sxs-lookup"><span data-stu-id="6d5db-105">Use Update-AzMySqlConfiguration instead if you want update server parameters such as wait_timeout or net_retry_count.</span></span>

## <span data-ttu-id="6d5db-106">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="6d5db-106">SYNTAX</span></span>

### <span data-ttu-id="6d5db-107">UpdateExpanded (standard)</span><span class="sxs-lookup"><span data-stu-id="6d5db-107">UpdateExpanded (Default)</span></span>
```
Update-AzMySqlServer -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-AdministratorLoginPassword <SecureString>] [-BackupRetentionDay <Int32>] [-ReplicationRole <String>]
 [-Sku <String>] [-SkuCapacity <Int32>] [-SkuFamily <String>] [-SkuTier <SkuTier>]
 [-SslEnforcement <SslEnforcementEnum>] [-StorageAutogrow <StorageAutogrow>] [-StorageInMb <Int32>]
 [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="6d5db-108">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="6d5db-108">UpdateViaIdentityExpanded</span></span>
```
Update-AzMySqlServer -InputObject <IMySqlIdentity> [-AdministratorLoginPassword <SecureString>]
 [-BackupRetentionDay <Int32>] [-ReplicationRole <String>] [-Sku <String>] [-SkuCapacity <Int32>]
 [-SkuFamily <String>] [-SkuTier <SkuTier>] [-SslEnforcement <SslEnforcementEnum>]
 [-StorageAutogrow <StorageAutogrow>] [-StorageInMb <Int32>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>]
 [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="6d5db-109">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="6d5db-109">DESCRIPTION</span></span>
<span data-ttu-id="6d5db-110">Uppdaterar en befintlig server.</span><span class="sxs-lookup"><span data-stu-id="6d5db-110">Updates an existing server.</span></span>
<span data-ttu-id="6d5db-111">Meddelande texten kan innehålla en till många av de egenskaper som finns i Server definitionen för normal.</span><span class="sxs-lookup"><span data-stu-id="6d5db-111">The request body can contain one to many of the properties present in the normal server definition.</span></span>
<span data-ttu-id="6d5db-112">Använd Update-AzMySqlConfiguration istället om du vill uppdatera Server parametrar som wait_timeout eller net_retry_count.</span><span class="sxs-lookup"><span data-stu-id="6d5db-112">Use Update-AzMySqlConfiguration instead if you want update server parameters such as wait_timeout or net_retry_count.</span></span>

## <span data-ttu-id="6d5db-113">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="6d5db-113">EXAMPLES</span></span>

### <span data-ttu-id="6d5db-114">Exempel 1: uppdatera MySql-servern efter resurs grupp och Server namn</span><span class="sxs-lookup"><span data-stu-id="6d5db-114">Example 1: Update MySql server by resource group and server name</span></span>
```powershell
PS C:\> Update-AzMySqlServer -ResourceGroupName PowershellMySqlTest -ServerName mysql-test -SslEnforcement Disabled

Name          Location AdministratorLogin Version StorageProfileStorageMb SkuName   SkuTier        SslEnforcement
----          -------- ------------------ ------- ----------------------- -------   -------        --------------
mysql-test    eastus   mysql_test         5.7     5120                    GP_Gen5_4 GeneralPurpose Disabled
```

<span data-ttu-id="6d5db-115">Denna cmdlet uppdaterar MySql-servern efter resurs grupp och Server namn.</span><span class="sxs-lookup"><span data-stu-id="6d5db-115">This cmdlet updates MySql server by resource group and server name.</span></span>

### <span data-ttu-id="6d5db-116">Exempel 2: uppdatera MySql-servern efter identitet.</span><span class="sxs-lookup"><span data-stu-id="6d5db-116">Example 2: Update MySql server by identity.</span></span>
```powershell
PS C:\> Get-AzMySqlServer -ResourceGroupName PowershellMySqlTest -ServerName mysql-test | Update-AzMySqlServer -BackupRetentionDay 23 -StorageMb 10240

Name          Location AdministratorLogin Version StorageProfileStorageMb SkuName   SkuTier        SslEnforcement
----          -------- ------------------ ------- ----------------------- -------   -------        --------------
mysql-test    eastus   mysql_test         5.7     10240                   GP_Gen5_4 GeneralPurpose Disabled
```

<span data-ttu-id="6d5db-117">Denna cmdlet uppdaterar MySql-servern efter identitet.</span><span class="sxs-lookup"><span data-stu-id="6d5db-117">This cmdlet updates MySql server by identity.</span></span>

## <span data-ttu-id="6d5db-118">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="6d5db-118">PARAMETERS</span></span>

### <span data-ttu-id="6d5db-119">-AdministratorLoginPassword</span><span class="sxs-lookup"><span data-stu-id="6d5db-119">-AdministratorLoginPassword</span></span>
<span data-ttu-id="6d5db-120">Lösen ordet för administratörs inloggningen.</span><span class="sxs-lookup"><span data-stu-id="6d5db-120">The password of the administrator login.</span></span>

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

### <span data-ttu-id="6d5db-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="6d5db-121">-AsJob</span></span>
<span data-ttu-id="6d5db-122">Kör kommandot som ett jobb.</span><span class="sxs-lookup"><span data-stu-id="6d5db-122">Run the command as a job.</span></span>

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

### <span data-ttu-id="6d5db-123">-BackupRetentionDay</span><span class="sxs-lookup"><span data-stu-id="6d5db-123">-BackupRetentionDay</span></span>
<span data-ttu-id="6d5db-124">Dagar för säkerhets kopiering av Server.</span><span class="sxs-lookup"><span data-stu-id="6d5db-124">Backup retention days for the server.</span></span>
<span data-ttu-id="6d5db-125">Antalet dagar är mellan 7 och 35.</span><span class="sxs-lookup"><span data-stu-id="6d5db-125">Day count is between 7 and 35.</span></span>

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

### <span data-ttu-id="6d5db-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6d5db-126">-DefaultProfile</span></span>
<span data-ttu-id="6d5db-127">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="6d5db-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6d5db-128">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6d5db-128">-InputObject</span></span>
<span data-ttu-id="6d5db-129">Identitets parameter.</span><span class="sxs-lookup"><span data-stu-id="6d5db-129">Identity Parameter.</span></span>
<span data-ttu-id="6d5db-130">För att konstruera kan du läsa avsnittet anteckningar för INPUTOBJECT-egenskaper och skapa en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="6d5db-130">To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="6d5db-131">-Namn</span><span class="sxs-lookup"><span data-stu-id="6d5db-131">-Name</span></span>
<span data-ttu-id="6d5db-132">Namnet på servern.</span><span class="sxs-lookup"><span data-stu-id="6d5db-132">The name of the server.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases: ServerName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6d5db-133">-Nowait</span><span class="sxs-lookup"><span data-stu-id="6d5db-133">-NoWait</span></span>
<span data-ttu-id="6d5db-134">Kör kommandot asynkront.</span><span class="sxs-lookup"><span data-stu-id="6d5db-134">Run the command asynchronously.</span></span>

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

### <span data-ttu-id="6d5db-135">-ReplicationRole</span><span class="sxs-lookup"><span data-stu-id="6d5db-135">-ReplicationRole</span></span>
<span data-ttu-id="6d5db-136">Serverns replikeringsrelation.</span><span class="sxs-lookup"><span data-stu-id="6d5db-136">The replication role of the server.</span></span>

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

### <span data-ttu-id="6d5db-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6d5db-137">-ResourceGroupName</span></span>
<span data-ttu-id="6d5db-138">Namnet på resurs gruppen som innehåller resursen.</span><span class="sxs-lookup"><span data-stu-id="6d5db-138">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="6d5db-139">Det här värdet kan hämtas från Azure Resource Manager API eller till portalen.</span><span class="sxs-lookup"><span data-stu-id="6d5db-139">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="6d5db-140">-SKU</span><span class="sxs-lookup"><span data-stu-id="6d5db-140">-Sku</span></span>
<span data-ttu-id="6d5db-141">Namnet på SKU: n, vanligt vis nivå + Family + cores, till exempel B_Gen4_1 GP_Gen5_8.</span><span class="sxs-lookup"><span data-stu-id="6d5db-141">The name of the sku, typically, tier + family + cores, e.g. B_Gen4_1, GP_Gen5_8.</span></span>

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

### <span data-ttu-id="6d5db-142">-SkuCapacity</span><span class="sxs-lookup"><span data-stu-id="6d5db-142">-SkuCapacity</span></span>
<span data-ttu-id="6d5db-143">Skala upp-och utgångs kapacitet som representerar serverns beräknade enheter.</span><span class="sxs-lookup"><span data-stu-id="6d5db-143">The scale up/out capacity, representing server's compute units.</span></span>

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

### <span data-ttu-id="6d5db-144">-SkuFamily</span><span class="sxs-lookup"><span data-stu-id="6d5db-144">-SkuFamily</span></span>
<span data-ttu-id="6d5db-145">Familjen av hård vara.</span><span class="sxs-lookup"><span data-stu-id="6d5db-145">The family of hardware.</span></span>

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

### <span data-ttu-id="6d5db-146">-SkuTier</span><span class="sxs-lookup"><span data-stu-id="6d5db-146">-SkuTier</span></span>
<span data-ttu-id="6d5db-147">Nivån för en viss SKU, t. ex.</span><span class="sxs-lookup"><span data-stu-id="6d5db-147">The tier of the particular SKU, e.g. Basic.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.MySql.Support.SkuTier
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6d5db-148">-SslEnforcement</span><span class="sxs-lookup"><span data-stu-id="6d5db-148">-SslEnforcement</span></span>
<span data-ttu-id="6d5db-149">Aktivera SSL-tvång eller inte vid anslutning till server.</span><span class="sxs-lookup"><span data-stu-id="6d5db-149">Enable ssl enforcement or not when connect to server.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.MySql.Support.SslEnforcementEnum
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6d5db-150">-StorageAutogrow</span><span class="sxs-lookup"><span data-stu-id="6d5db-150">-StorageAutogrow</span></span>
<span data-ttu-id="6d5db-151">Aktivera automatisk tillväxt av lagring.</span><span class="sxs-lookup"><span data-stu-id="6d5db-151">Enable Storage Auto Grow.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.MySql.Support.StorageAutogrow
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6d5db-152">-StorageInMb</span><span class="sxs-lookup"><span data-stu-id="6d5db-152">-StorageInMb</span></span>
<span data-ttu-id="6d5db-153">Högsta tillåtna lagrings utrymme för en server.</span><span class="sxs-lookup"><span data-stu-id="6d5db-153">Max storage allowed for a server.</span></span>

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

### <span data-ttu-id="6d5db-154">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="6d5db-154">-SubscriptionId</span></span>
<span data-ttu-id="6d5db-155">Det prenumerations-ID som identifierar en Azure-prenumeration.</span><span class="sxs-lookup"><span data-stu-id="6d5db-155">The subscription ID that identifies an Azure subscription.</span></span>

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

### <span data-ttu-id="6d5db-156">-Tagg</span><span class="sxs-lookup"><span data-stu-id="6d5db-156">-Tag</span></span>
<span data-ttu-id="6d5db-157">Programspecifika metadata i form av par med nyckelvärdena.</span><span class="sxs-lookup"><span data-stu-id="6d5db-157">Application-specific metadata in the form of key-value pairs.</span></span>

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

### <span data-ttu-id="6d5db-158">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="6d5db-158">-Confirm</span></span>
<span data-ttu-id="6d5db-159">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="6d5db-159">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6d5db-160">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6d5db-160">-WhatIf</span></span>
<span data-ttu-id="6d5db-161">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="6d5db-161">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6d5db-162">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="6d5db-162">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6d5db-163">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6d5db-163">CommonParameters</span></span>
<span data-ttu-id="6d5db-164">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6d5db-164">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6d5db-165">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="6d5db-165">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6d5db-166">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="6d5db-166">INPUTS</span></span>

### <span data-ttu-id="6d5db-167">Microsoft. Azure. PowerShell. cmdletar. MySql. Models. IMySqlIdentity</span><span class="sxs-lookup"><span data-stu-id="6d5db-167">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity</span></span>

## <span data-ttu-id="6d5db-168">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="6d5db-168">OUTPUTS</span></span>

### <span data-ttu-id="6d5db-169">Microsoft. Azure. PowerShell. cmdletar. MySql. Models. Api20171201. IServer</span><span class="sxs-lookup"><span data-stu-id="6d5db-169">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20171201.IServer</span></span>

## <span data-ttu-id="6d5db-170">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="6d5db-170">NOTES</span></span>

<span data-ttu-id="6d5db-171">ALIAS</span><span class="sxs-lookup"><span data-stu-id="6d5db-171">ALIASES</span></span>

<span data-ttu-id="6d5db-172">KOMPLEXA PARAMETER EGENSKAPER</span><span class="sxs-lookup"><span data-stu-id="6d5db-172">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="6d5db-173">Skapa en hash-tabell som innehåller lämpliga egenskaper för att lägga till de parametrar som beskrivs nedan.</span><span class="sxs-lookup"><span data-stu-id="6d5db-173">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="6d5db-174">Om du vill ha information om hash-tabeller kör Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="6d5db-174">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="6d5db-175">INPUTOBJECT <IMySqlIdentity> : identitets parameter.</span><span class="sxs-lookup"><span data-stu-id="6d5db-175">INPUTOBJECT <IMySqlIdentity>: Identity Parameter.</span></span>
  - <span data-ttu-id="6d5db-176">`[ConfigurationName <String>]`: Server konfigurationens namn.</span><span class="sxs-lookup"><span data-stu-id="6d5db-176">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="6d5db-177">`[DatabaseName <String>]`: Namnet på databasen.</span><span class="sxs-lookup"><span data-stu-id="6d5db-177">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="6d5db-178">`[FirewallRuleName <String>]`: Namnet på Server brand Väggs regeln.</span><span class="sxs-lookup"><span data-stu-id="6d5db-178">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="6d5db-179">`[Id <String>]`: Sökväg till resurs identitet</span><span class="sxs-lookup"><span data-stu-id="6d5db-179">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="6d5db-180">`[KeyName <String>]`: Server namnet.</span><span class="sxs-lookup"><span data-stu-id="6d5db-180">`[KeyName <String>]`: The name of the server key.</span></span>
  - <span data-ttu-id="6d5db-181">`[LocationName <String>]`: Namnet på platsen.</span><span class="sxs-lookup"><span data-stu-id="6d5db-181">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="6d5db-182">`[ResourceGroupName <String>]`: Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="6d5db-182">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="6d5db-183">Namnet är Skift läges okänsligt.</span><span class="sxs-lookup"><span data-stu-id="6d5db-183">The name is case insensitive.</span></span>
  - <span data-ttu-id="6d5db-184">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: Namnet på säkerhets varnings principen.</span><span class="sxs-lookup"><span data-stu-id="6d5db-184">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="6d5db-185">`[ServerName <String>]`: Namnet på servern.</span><span class="sxs-lookup"><span data-stu-id="6d5db-185">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="6d5db-186">`[SubscriptionId <String>]`: Mål prenumerationens ID.</span><span class="sxs-lookup"><span data-stu-id="6d5db-186">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="6d5db-187">`[VirtualNetworkRuleName <String>]`: Namnet på den virtuella nätverks regeln.</span><span class="sxs-lookup"><span data-stu-id="6d5db-187">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="6d5db-188">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="6d5db-188">RELATED LINKS</span></span>

