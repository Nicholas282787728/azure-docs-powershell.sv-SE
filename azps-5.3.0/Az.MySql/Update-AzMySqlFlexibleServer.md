---
external help file: ''
Module Name: Az.MySql
online version: https://docs.microsoft.com/en-us/powershell/module/az.mysql/update-azmysqlflexibleserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Update-AzMySqlFlexibleServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Update-AzMySqlFlexibleServer.md
ms.openlocfilehash: 3e1f79f431e5f0ff5c39c03a7f3c41a20c2543e4
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98522514"
---
# <span data-ttu-id="837b1-101">Update-AzMySqlFlexibleServer</span><span class="sxs-lookup"><span data-stu-id="837b1-101">Update-AzMySqlFlexibleServer</span></span>

## <span data-ttu-id="837b1-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="837b1-102">SYNOPSIS</span></span>
<span data-ttu-id="837b1-103">Uppdaterar en befintlig MySQL-server.</span><span class="sxs-lookup"><span data-stu-id="837b1-103">Updates an existing MySQL flexible server.</span></span>
<span data-ttu-id="837b1-104">Meddelande texten kan innehålla en till många av de egenskaper som finns i Server definitionen för normal.</span><span class="sxs-lookup"><span data-stu-id="837b1-104">The request body can contain one to many of the properties present in the normal server definition.</span></span>
<span data-ttu-id="837b1-105">Använd Update-AzMySqlFlexibleServerConfiguration istället om du vill uppdatera Server parametrar som wait_timeout eller net_retry_count.</span><span class="sxs-lookup"><span data-stu-id="837b1-105">Use Update-AzMySqlFlexibleServerConfiguration instead if you want update server parameters such as wait_timeout or net_retry_count.</span></span>

## <span data-ttu-id="837b1-106">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="837b1-106">SYNTAX</span></span>

### <span data-ttu-id="837b1-107">UpdateExpanded (standard)</span><span class="sxs-lookup"><span data-stu-id="837b1-107">UpdateExpanded (Default)</span></span>
```
Update-AzMySqlFlexibleServer -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-AdministratorLoginPassword <SecureString>] [-BackupRetentionDay <Int32>] [-HaEnabled <HaEnabledEnum>]
 [-ReplicationRole <String>] [-Sku <String>] [-SkuTier <SkuTier>] [-SslEnforcement <SslEnforcementEnum>]
 [-StorageAutogrow <StorageAutogrow>] [-StorageInMb <Int32>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>]
 [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="837b1-108">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="837b1-108">UpdateViaIdentityExpanded</span></span>
```
Update-AzMySqlFlexibleServer -InputObject <IMySqlIdentity> [-AdministratorLoginPassword <SecureString>]
 [-BackupRetentionDay <Int32>] [-HaEnabled <HaEnabledEnum>] [-ReplicationRole <String>] [-Sku <String>]
 [-SkuTier <SkuTier>] [-SslEnforcement <SslEnforcementEnum>] [-StorageAutogrow <StorageAutogrow>]
 [-StorageInMb <Int32>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="837b1-109">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="837b1-109">DESCRIPTION</span></span>
<span data-ttu-id="837b1-110">Uppdaterar en befintlig MySQL-server.</span><span class="sxs-lookup"><span data-stu-id="837b1-110">Updates an existing MySQL flexible server.</span></span>
<span data-ttu-id="837b1-111">Meddelande texten kan innehålla en till många av de egenskaper som finns i Server definitionen för normal.</span><span class="sxs-lookup"><span data-stu-id="837b1-111">The request body can contain one to many of the properties present in the normal server definition.</span></span>
<span data-ttu-id="837b1-112">Använd Update-AzMySqlFlexibleServerConfiguration istället om du vill uppdatera Server parametrar som wait_timeout eller net_retry_count.</span><span class="sxs-lookup"><span data-stu-id="837b1-112">Use Update-AzMySqlFlexibleServerConfiguration instead if you want update server parameters such as wait_timeout or net_retry_count.</span></span>

## <span data-ttu-id="837b1-113">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="837b1-113">EXAMPLES</span></span>

### <span data-ttu-id="837b1-114">Exempel 1: uppdatera MySql-servern efter resurs grupp och Server namn</span><span class="sxs-lookup"><span data-stu-id="837b1-114">Example 1: Update MySql server by resource group and server name</span></span>
```powershell
PS C:\> Update-AzMySqlFlexibleServer -ResourceGroupName PowershellMySqlTest -Name mysql-test -Sku Standard_D4ds_v4

Name          Location AdministratorLogin Version StorageProfileStorageMb SkuName          SkuTier        
----          -------- ------------------ ------- ----------------------- ---------------- -------------
mysql-test    westus2   mysql_test         5.7     5120                    Standard_D4ds_v4 GeneralPurpose
```

<span data-ttu-id="837b1-115">Denna cmdlet uppdaterar MySql-servern efter resurs grupp och Server namn.</span><span class="sxs-lookup"><span data-stu-id="837b1-115">This cmdlet updates MySql server by resource group and server name.</span></span>

### <span data-ttu-id="837b1-116">Exempel 2: uppdatera MySql-servern efter identitet.</span><span class="sxs-lookup"><span data-stu-id="837b1-116">Example 2: Update MySql server by identity.</span></span>
```powershell
PS C:\> Get-AzMySqlFlexibleServer -ResourceGroupName PowershellMySqlTest -ServerName mysql-test | Update-AzMySqlFlexibleServer -BackupRetentionDay 23 -StorageInMb 10240

Name          Location AdministratorLogin Version StorageProfileStorageMb SkuName          SkuTier        
----          -------- ------------------ ------- ----------------------- ---------------- -------------
mysql-test    westus2   mysql_test         5.7     5120                    Standard_D2ds_v4 GeneralPurpose
```

<span data-ttu-id="837b1-117">Denna cmdlet uppdaterar MySql-servern efter identitet.</span><span class="sxs-lookup"><span data-stu-id="837b1-117">This cmdlet updates MySql server by identity.</span></span>

## <span data-ttu-id="837b1-118">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="837b1-118">PARAMETERS</span></span>

### <span data-ttu-id="837b1-119">-AdministratorLoginPassword</span><span class="sxs-lookup"><span data-stu-id="837b1-119">-AdministratorLoginPassword</span></span>
<span data-ttu-id="837b1-120">Lösen ordet för administratörs inloggningen.</span><span class="sxs-lookup"><span data-stu-id="837b1-120">The password of the administrator login.</span></span>

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

### <span data-ttu-id="837b1-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="837b1-121">-AsJob</span></span>
<span data-ttu-id="837b1-122">Kör kommandot som ett jobb.</span><span class="sxs-lookup"><span data-stu-id="837b1-122">Run the command as a job.</span></span>

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

### <span data-ttu-id="837b1-123">-BackupRetentionDay</span><span class="sxs-lookup"><span data-stu-id="837b1-123">-BackupRetentionDay</span></span>
<span data-ttu-id="837b1-124">Dagar för säkerhets kopiering av Server.</span><span class="sxs-lookup"><span data-stu-id="837b1-124">Backup retention days for the server.</span></span>
<span data-ttu-id="837b1-125">Antalet dagar är mellan 7 och 35.</span><span class="sxs-lookup"><span data-stu-id="837b1-125">Day count is between 7 and 35.</span></span>

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

### <span data-ttu-id="837b1-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="837b1-126">-DefaultProfile</span></span>
<span data-ttu-id="837b1-127">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="837b1-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="837b1-128">-HaEnabled</span><span class="sxs-lookup"><span data-stu-id="837b1-128">-HaEnabled</span></span>
<span data-ttu-id="837b1-129">Aktivera eller inaktivera funktionen för hög tillgänglighet.</span><span class="sxs-lookup"><span data-stu-id="837b1-129">Enable or disable high availability feature.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.MySql.Support.HaEnabledEnum
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="837b1-130">-InputObject</span><span class="sxs-lookup"><span data-stu-id="837b1-130">-InputObject</span></span>
<span data-ttu-id="837b1-131">Identitets parameter.</span><span class="sxs-lookup"><span data-stu-id="837b1-131">Identity Parameter.</span></span>
<span data-ttu-id="837b1-132">För att konstruera kan du läsa avsnittet anteckningar för INPUTOBJECT-egenskaper och skapa en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="837b1-132">To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="837b1-133">-Namn</span><span class="sxs-lookup"><span data-stu-id="837b1-133">-Name</span></span>
<span data-ttu-id="837b1-134">Namnet på servern.</span><span class="sxs-lookup"><span data-stu-id="837b1-134">The name of the server.</span></span>

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

### <span data-ttu-id="837b1-135">-Nowait</span><span class="sxs-lookup"><span data-stu-id="837b1-135">-NoWait</span></span>
<span data-ttu-id="837b1-136">Kör kommandot asynkront.</span><span class="sxs-lookup"><span data-stu-id="837b1-136">Run the command asynchronously.</span></span>

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

### <span data-ttu-id="837b1-137">-ReplicationRole</span><span class="sxs-lookup"><span data-stu-id="837b1-137">-ReplicationRole</span></span>
<span data-ttu-id="837b1-138">Serverns replikeringsrelation.</span><span class="sxs-lookup"><span data-stu-id="837b1-138">The replication role of the server.</span></span>

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

### <span data-ttu-id="837b1-139">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="837b1-139">-ResourceGroupName</span></span>
<span data-ttu-id="837b1-140">Namnet på resurs gruppen som innehåller resursen.</span><span class="sxs-lookup"><span data-stu-id="837b1-140">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="837b1-141">Det här värdet kan hämtas från Azure Resource Manager API eller till portalen.</span><span class="sxs-lookup"><span data-stu-id="837b1-141">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="837b1-142">-SKU</span><span class="sxs-lookup"><span data-stu-id="837b1-142">-Sku</span></span>
<span data-ttu-id="837b1-143">Namnet på SKU: n, vanligt vis nivå + Family + cores, till exempel B_Gen4_1 GP_Gen5_8.</span><span class="sxs-lookup"><span data-stu-id="837b1-143">The name of the sku, typically, tier + family + cores, e.g. B_Gen4_1, GP_Gen5_8.</span></span>

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

### <span data-ttu-id="837b1-144">-SkuTier</span><span class="sxs-lookup"><span data-stu-id="837b1-144">-SkuTier</span></span>
<span data-ttu-id="837b1-145">Nivån för en viss SKU, t. ex.</span><span class="sxs-lookup"><span data-stu-id="837b1-145">The tier of the particular SKU, e.g. Basic.</span></span>

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

### <span data-ttu-id="837b1-146">-SslEnforcement</span><span class="sxs-lookup"><span data-stu-id="837b1-146">-SslEnforcement</span></span>
<span data-ttu-id="837b1-147">Aktivera SSL-tvång eller inte vid anslutning till server.</span><span class="sxs-lookup"><span data-stu-id="837b1-147">Enable ssl enforcement or not when connect to server.</span></span>

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

### <span data-ttu-id="837b1-148">-StorageAutogrow</span><span class="sxs-lookup"><span data-stu-id="837b1-148">-StorageAutogrow</span></span>
<span data-ttu-id="837b1-149">Aktivera automatisk tillväxt av lagring.</span><span class="sxs-lookup"><span data-stu-id="837b1-149">Enable Storage Auto Grow.</span></span>

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

### <span data-ttu-id="837b1-150">-StorageInMb</span><span class="sxs-lookup"><span data-stu-id="837b1-150">-StorageInMb</span></span>
<span data-ttu-id="837b1-151">Högsta tillåtna lagrings utrymme för en server.</span><span class="sxs-lookup"><span data-stu-id="837b1-151">Max storage allowed for a server.</span></span>

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

### <span data-ttu-id="837b1-152">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="837b1-152">-SubscriptionId</span></span>
<span data-ttu-id="837b1-153">Det prenumerations-ID som identifierar en Azure-prenumeration.</span><span class="sxs-lookup"><span data-stu-id="837b1-153">The subscription ID that identifies an Azure subscription.</span></span>

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

### <span data-ttu-id="837b1-154">-Tagg</span><span class="sxs-lookup"><span data-stu-id="837b1-154">-Tag</span></span>
<span data-ttu-id="837b1-155">Programspecifika metadata i form av par med nyckelvärdena.</span><span class="sxs-lookup"><span data-stu-id="837b1-155">Application-specific metadata in the form of key-value pairs.</span></span>

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

### <span data-ttu-id="837b1-156">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="837b1-156">-Confirm</span></span>
<span data-ttu-id="837b1-157">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="837b1-157">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="837b1-158">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="837b1-158">-WhatIf</span></span>
<span data-ttu-id="837b1-159">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="837b1-159">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="837b1-160">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="837b1-160">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="837b1-161">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="837b1-161">CommonParameters</span></span>
<span data-ttu-id="837b1-162">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="837b1-162">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="837b1-163">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="837b1-163">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="837b1-164">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="837b1-164">INPUTS</span></span>

### <span data-ttu-id="837b1-165">Microsoft. Azure. PowerShell. cmdletar. MySql. Models. IMySqlIdentity</span><span class="sxs-lookup"><span data-stu-id="837b1-165">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity</span></span>

## <span data-ttu-id="837b1-166">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="837b1-166">OUTPUTS</span></span>

### <span data-ttu-id="837b1-167">Microsoft. Azure. PowerShell. cmdletar. MySql. Models. Api20200701Preview. IServerAutoGenerated</span><span class="sxs-lookup"><span data-stu-id="837b1-167">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20200701Preview.IServerAutoGenerated</span></span>

## <span data-ttu-id="837b1-168">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="837b1-168">NOTES</span></span>

<span data-ttu-id="837b1-169">ALIAS</span><span class="sxs-lookup"><span data-stu-id="837b1-169">ALIASES</span></span>

<span data-ttu-id="837b1-170">KOMPLEXA PARAMETER EGENSKAPER</span><span class="sxs-lookup"><span data-stu-id="837b1-170">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="837b1-171">Skapa en hash-tabell som innehåller lämpliga egenskaper för att lägga till de parametrar som beskrivs nedan.</span><span class="sxs-lookup"><span data-stu-id="837b1-171">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="837b1-172">Om du vill ha information om hash-tabeller kör Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="837b1-172">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="837b1-173">INPUTOBJECT <IMySqlIdentity> : identitets parameter.</span><span class="sxs-lookup"><span data-stu-id="837b1-173">INPUTOBJECT <IMySqlIdentity>: Identity Parameter.</span></span>
  - <span data-ttu-id="837b1-174">`[ConfigurationName <String>]`: Server konfigurationens namn.</span><span class="sxs-lookup"><span data-stu-id="837b1-174">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="837b1-175">`[DatabaseName <String>]`: Namnet på databasen.</span><span class="sxs-lookup"><span data-stu-id="837b1-175">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="837b1-176">`[FirewallRuleName <String>]`: Namnet på Server brand Väggs regeln.</span><span class="sxs-lookup"><span data-stu-id="837b1-176">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="837b1-177">`[Id <String>]`: Sökväg till resurs identitet</span><span class="sxs-lookup"><span data-stu-id="837b1-177">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="837b1-178">`[KeyName <String>]`: Server namnet.</span><span class="sxs-lookup"><span data-stu-id="837b1-178">`[KeyName <String>]`: The name of the server key.</span></span>
  - <span data-ttu-id="837b1-179">`[LocationName <String>]`: Namnet på platsen.</span><span class="sxs-lookup"><span data-stu-id="837b1-179">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="837b1-180">`[ResourceGroupName <String>]`: Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="837b1-180">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="837b1-181">Namnet är Skift läges okänsligt.</span><span class="sxs-lookup"><span data-stu-id="837b1-181">The name is case insensitive.</span></span>
  - <span data-ttu-id="837b1-182">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: Namnet på säkerhets varnings principen.</span><span class="sxs-lookup"><span data-stu-id="837b1-182">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="837b1-183">`[ServerName <String>]`: Namnet på servern.</span><span class="sxs-lookup"><span data-stu-id="837b1-183">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="837b1-184">`[SubscriptionId <String>]`: Mål prenumerationens ID.</span><span class="sxs-lookup"><span data-stu-id="837b1-184">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="837b1-185">`[VirtualNetworkRuleName <String>]`: Namnet på den virtuella nätverks regeln.</span><span class="sxs-lookup"><span data-stu-id="837b1-185">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="837b1-186">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="837b1-186">RELATED LINKS</span></span>

