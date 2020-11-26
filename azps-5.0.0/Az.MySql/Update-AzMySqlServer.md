---
external help file: ''
Module Name: Az.MySql
online version: https://docs.microsoft.com/en-us/powershell/module/az.mysql/update-azmysqlserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Update-AzMySqlServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Update-AzMySqlServer.md
ms.openlocfilehash: e23cc8b942033805d8ed8cd122b19e6a59bf457c
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94270845"
---
# <span data-ttu-id="52eb0-101">Update-AzMySqlServer</span><span class="sxs-lookup"><span data-stu-id="52eb0-101">Update-AzMySqlServer</span></span>

## <span data-ttu-id="52eb0-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="52eb0-102">SYNOPSIS</span></span>
<span data-ttu-id="52eb0-103">Uppdaterar en befintlig server.</span><span class="sxs-lookup"><span data-stu-id="52eb0-103">Updates an existing server.</span></span>
<span data-ttu-id="52eb0-104">Meddelande texten kan innehålla en till många av de egenskaper som finns i Server definitionen för normal.</span><span class="sxs-lookup"><span data-stu-id="52eb0-104">The request body can contain one to many of the properties present in the normal server definition.</span></span>
<span data-ttu-id="52eb0-105">Använd Update-AzMySqlConfiguration istället om du vill uppdatera Server parametrar som wait_timeout eller net_retry_count.</span><span class="sxs-lookup"><span data-stu-id="52eb0-105">Use Update-AzMySqlConfiguration instead if you want update server parameters such as wait_timeout or net_retry_count.</span></span>

## <span data-ttu-id="52eb0-106">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="52eb0-106">SYNTAX</span></span>

### <span data-ttu-id="52eb0-107">UpdateExpanded (standard)</span><span class="sxs-lookup"><span data-stu-id="52eb0-107">UpdateExpanded (Default)</span></span>
```
Update-AzMySqlServer -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-AdministratorLoginPassword <SecureString>] [-BackupRetentionDay <Int32>] [-ReplicationRole <String>]
 [-Sku <String>] [-SkuCapacity <Int32>] [-SkuFamily <String>] [-SkuTier <SkuTier>]
 [-SslEnforcement <SslEnforcementEnum>] [-StorageAutogrow <StorageAutogrow>] [-StorageInMb <Int32>]
 [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="52eb0-108">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="52eb0-108">UpdateViaIdentityExpanded</span></span>
```
Update-AzMySqlServer -InputObject <IMySqlIdentity> [-AdministratorLoginPassword <SecureString>]
 [-BackupRetentionDay <Int32>] [-ReplicationRole <String>] [-Sku <String>] [-SkuCapacity <Int32>]
 [-SkuFamily <String>] [-SkuTier <SkuTier>] [-SslEnforcement <SslEnforcementEnum>]
 [-StorageAutogrow <StorageAutogrow>] [-StorageInMb <Int32>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>]
 [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="52eb0-109">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="52eb0-109">DESCRIPTION</span></span>
<span data-ttu-id="52eb0-110">Uppdaterar en befintlig server.</span><span class="sxs-lookup"><span data-stu-id="52eb0-110">Updates an existing server.</span></span>
<span data-ttu-id="52eb0-111">Meddelande texten kan innehålla en till många av de egenskaper som finns i Server definitionen för normal.</span><span class="sxs-lookup"><span data-stu-id="52eb0-111">The request body can contain one to many of the properties present in the normal server definition.</span></span>
<span data-ttu-id="52eb0-112">Använd Update-AzMySqlConfiguration istället om du vill uppdatera Server parametrar som wait_timeout eller net_retry_count.</span><span class="sxs-lookup"><span data-stu-id="52eb0-112">Use Update-AzMySqlConfiguration instead if you want update server parameters such as wait_timeout or net_retry_count.</span></span>

## <span data-ttu-id="52eb0-113">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="52eb0-113">EXAMPLES</span></span>

### <span data-ttu-id="52eb0-114">Exempel 1: uppdatera MySql-servern efter resurs grupp och Server namn</span><span class="sxs-lookup"><span data-stu-id="52eb0-114">Example 1: Update MySql server by resource group and server name</span></span>
```powershell
PS C:\> Update-AzMySqlServer -ResourceGroupName PowershellMySqlTest -ServerName mysql-test -SslEnforcement Disabled

Name          Location AdministratorLogin Version StorageProfileStorageMb SkuName   SkuTier        SslEnforcement
----          -------- ------------------ ------- ----------------------- -------   -------        --------------
mysql-test    eastus   mysql_test         5.7     5120                    GP_Gen5_4 GeneralPurpose Disabled
```

<span data-ttu-id="52eb0-115">Denna cmdlet uppdaterar MySql-servern efter resurs grupp och Server namn.</span><span class="sxs-lookup"><span data-stu-id="52eb0-115">This cmdlet updates MySql server by resource group and server name.</span></span>

### <span data-ttu-id="52eb0-116">Exempel 2: uppdatera MySql-servern efter identitet.</span><span class="sxs-lookup"><span data-stu-id="52eb0-116">Example 2: Update MySql server by identity.</span></span>
```powershell
PS C:\> Get-AzMySqlServer -ResourceGroupName PowershellMySqlTest -ServerName mysql-test | Update-AzMySqlServer -BackupRetentionDay 23 -StorageMb 10240

Name          Location AdministratorLogin Version StorageProfileStorageMb SkuName   SkuTier        SslEnforcement
----          -------- ------------------ ------- ----------------------- -------   -------        --------------
mysql-test    eastus   mysql_test         5.7     10240                   GP_Gen5_4 GeneralPurpose Disabled
```

<span data-ttu-id="52eb0-117">Denna cmdlet uppdaterar MySql-servern efter identitet.</span><span class="sxs-lookup"><span data-stu-id="52eb0-117">This cmdlet updates MySql server by identity.</span></span>

## <span data-ttu-id="52eb0-118">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="52eb0-118">PARAMETERS</span></span>

### <span data-ttu-id="52eb0-119">-AdministratorLoginPassword</span><span class="sxs-lookup"><span data-stu-id="52eb0-119">-AdministratorLoginPassword</span></span>
<span data-ttu-id="52eb0-120">Lösen ordet för administratörs inloggningen.</span><span class="sxs-lookup"><span data-stu-id="52eb0-120">The password of the administrator login.</span></span>

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

### <span data-ttu-id="52eb0-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="52eb0-121">-AsJob</span></span>
<span data-ttu-id="52eb0-122">Kör kommandot som ett jobb.</span><span class="sxs-lookup"><span data-stu-id="52eb0-122">Run the command as a job.</span></span>

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

### <span data-ttu-id="52eb0-123">-BackupRetentionDay</span><span class="sxs-lookup"><span data-stu-id="52eb0-123">-BackupRetentionDay</span></span>
<span data-ttu-id="52eb0-124">Dagar för säkerhets kopiering av Server.</span><span class="sxs-lookup"><span data-stu-id="52eb0-124">Backup retention days for the server.</span></span>
<span data-ttu-id="52eb0-125">Antalet dagar är mellan 7 och 35.</span><span class="sxs-lookup"><span data-stu-id="52eb0-125">Day count is between 7 and 35.</span></span>

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

### <span data-ttu-id="52eb0-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="52eb0-126">-DefaultProfile</span></span>
<span data-ttu-id="52eb0-127">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="52eb0-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="52eb0-128">-InputObject</span><span class="sxs-lookup"><span data-stu-id="52eb0-128">-InputObject</span></span>
<span data-ttu-id="52eb0-129">Identitets parameter.</span><span class="sxs-lookup"><span data-stu-id="52eb0-129">Identity Parameter.</span></span>
<span data-ttu-id="52eb0-130">För att konstruera kan du läsa avsnittet anteckningar för INPUTOBJECT-egenskaper och skapa en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="52eb0-130">To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="52eb0-131">-Namn</span><span class="sxs-lookup"><span data-stu-id="52eb0-131">-Name</span></span>
<span data-ttu-id="52eb0-132">Namnet på servern.</span><span class="sxs-lookup"><span data-stu-id="52eb0-132">The name of the server.</span></span>

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

### <span data-ttu-id="52eb0-133">-Nowait</span><span class="sxs-lookup"><span data-stu-id="52eb0-133">-NoWait</span></span>
<span data-ttu-id="52eb0-134">Kör kommandot asynkront.</span><span class="sxs-lookup"><span data-stu-id="52eb0-134">Run the command asynchronously.</span></span>

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

### <span data-ttu-id="52eb0-135">-ReplicationRole</span><span class="sxs-lookup"><span data-stu-id="52eb0-135">-ReplicationRole</span></span>
<span data-ttu-id="52eb0-136">Serverns replikeringsrelation.</span><span class="sxs-lookup"><span data-stu-id="52eb0-136">The replication role of the server.</span></span>

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

### <span data-ttu-id="52eb0-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="52eb0-137">-ResourceGroupName</span></span>
<span data-ttu-id="52eb0-138">Namnet på resurs gruppen som innehåller resursen.</span><span class="sxs-lookup"><span data-stu-id="52eb0-138">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="52eb0-139">Det här värdet kan hämtas från Azure Resource Manager API eller till portalen.</span><span class="sxs-lookup"><span data-stu-id="52eb0-139">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="52eb0-140">-SKU</span><span class="sxs-lookup"><span data-stu-id="52eb0-140">-Sku</span></span>
<span data-ttu-id="52eb0-141">Namnet på SKU: n, vanligt vis nivå + Family + cores, till exempel B_Gen4_1 GP_Gen5_8.</span><span class="sxs-lookup"><span data-stu-id="52eb0-141">The name of the sku, typically, tier + family + cores, e.g. B_Gen4_1, GP_Gen5_8.</span></span>

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

### <span data-ttu-id="52eb0-142">-SkuCapacity</span><span class="sxs-lookup"><span data-stu-id="52eb0-142">-SkuCapacity</span></span>
<span data-ttu-id="52eb0-143">Skala upp-och utgångs kapacitet som representerar serverns beräknade enheter.</span><span class="sxs-lookup"><span data-stu-id="52eb0-143">The scale up/out capacity, representing server's compute units.</span></span>

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

### <span data-ttu-id="52eb0-144">-SkuFamily</span><span class="sxs-lookup"><span data-stu-id="52eb0-144">-SkuFamily</span></span>
<span data-ttu-id="52eb0-145">Familjen av hård vara.</span><span class="sxs-lookup"><span data-stu-id="52eb0-145">The family of hardware.</span></span>

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

### <span data-ttu-id="52eb0-146">-SkuTier</span><span class="sxs-lookup"><span data-stu-id="52eb0-146">-SkuTier</span></span>
<span data-ttu-id="52eb0-147">Nivån för en viss SKU, t. ex.</span><span class="sxs-lookup"><span data-stu-id="52eb0-147">The tier of the particular SKU, e.g. Basic.</span></span>

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

### <span data-ttu-id="52eb0-148">-SslEnforcement</span><span class="sxs-lookup"><span data-stu-id="52eb0-148">-SslEnforcement</span></span>
<span data-ttu-id="52eb0-149">Aktivera SSL-tvång eller inte vid anslutning till server.</span><span class="sxs-lookup"><span data-stu-id="52eb0-149">Enable ssl enforcement or not when connect to server.</span></span>

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

### <span data-ttu-id="52eb0-150">-StorageAutogrow</span><span class="sxs-lookup"><span data-stu-id="52eb0-150">-StorageAutogrow</span></span>
<span data-ttu-id="52eb0-151">Aktivera automatisk tillväxt av lagring.</span><span class="sxs-lookup"><span data-stu-id="52eb0-151">Enable Storage Auto Grow.</span></span>

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

### <span data-ttu-id="52eb0-152">-StorageInMb</span><span class="sxs-lookup"><span data-stu-id="52eb0-152">-StorageInMb</span></span>
<span data-ttu-id="52eb0-153">Högsta tillåtna lagrings utrymme för en server.</span><span class="sxs-lookup"><span data-stu-id="52eb0-153">Max storage allowed for a server.</span></span>

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

### <span data-ttu-id="52eb0-154">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="52eb0-154">-SubscriptionId</span></span>
<span data-ttu-id="52eb0-155">Det prenumerations-ID som identifierar en Azure-prenumeration.</span><span class="sxs-lookup"><span data-stu-id="52eb0-155">The subscription ID that identifies an Azure subscription.</span></span>

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

### <span data-ttu-id="52eb0-156">-Tagg</span><span class="sxs-lookup"><span data-stu-id="52eb0-156">-Tag</span></span>
<span data-ttu-id="52eb0-157">Programspecifika metadata i form av par med nyckelvärdena.</span><span class="sxs-lookup"><span data-stu-id="52eb0-157">Application-specific metadata in the form of key-value pairs.</span></span>

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

### <span data-ttu-id="52eb0-158">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="52eb0-158">-Confirm</span></span>
<span data-ttu-id="52eb0-159">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="52eb0-159">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="52eb0-160">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="52eb0-160">-WhatIf</span></span>
<span data-ttu-id="52eb0-161">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="52eb0-161">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="52eb0-162">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="52eb0-162">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="52eb0-163">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="52eb0-163">CommonParameters</span></span>
<span data-ttu-id="52eb0-164">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="52eb0-164">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="52eb0-165">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="52eb0-165">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="52eb0-166">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="52eb0-166">INPUTS</span></span>

### <span data-ttu-id="52eb0-167">Microsoft. Azure. PowerShell. cmdletar. MySql. Models. IMySqlIdentity</span><span class="sxs-lookup"><span data-stu-id="52eb0-167">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity</span></span>

## <span data-ttu-id="52eb0-168">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="52eb0-168">OUTPUTS</span></span>

### <span data-ttu-id="52eb0-169">Microsoft. Azure. PowerShell. cmdletar. MySql. Models. Api20171201. IServer</span><span class="sxs-lookup"><span data-stu-id="52eb0-169">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20171201.IServer</span></span>

## <span data-ttu-id="52eb0-170">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="52eb0-170">NOTES</span></span>

<span data-ttu-id="52eb0-171">ALIAS</span><span class="sxs-lookup"><span data-stu-id="52eb0-171">ALIASES</span></span>

<span data-ttu-id="52eb0-172">KOMPLEXA PARAMETER EGENSKAPER</span><span class="sxs-lookup"><span data-stu-id="52eb0-172">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="52eb0-173">Skapa en hash-tabell som innehåller lämpliga egenskaper för att lägga till de parametrar som beskrivs nedan.</span><span class="sxs-lookup"><span data-stu-id="52eb0-173">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="52eb0-174">Om du vill ha information om hash-tabeller kör Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="52eb0-174">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="52eb0-175">INPUTOBJECT <IMySqlIdentity> : identitets parameter.</span><span class="sxs-lookup"><span data-stu-id="52eb0-175">INPUTOBJECT <IMySqlIdentity>: Identity Parameter.</span></span>
  - <span data-ttu-id="52eb0-176">`[ConfigurationName <String>]`: Server konfigurationens namn.</span><span class="sxs-lookup"><span data-stu-id="52eb0-176">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="52eb0-177">`[DatabaseName <String>]`: Namnet på databasen.</span><span class="sxs-lookup"><span data-stu-id="52eb0-177">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="52eb0-178">`[FirewallRuleName <String>]`: Namnet på Server brand Väggs regeln.</span><span class="sxs-lookup"><span data-stu-id="52eb0-178">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="52eb0-179">`[Id <String>]`: Sökväg till resurs identitet</span><span class="sxs-lookup"><span data-stu-id="52eb0-179">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="52eb0-180">`[LocationName <String>]`: Namnet på platsen.</span><span class="sxs-lookup"><span data-stu-id="52eb0-180">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="52eb0-181">`[ResourceGroupName <String>]`: Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="52eb0-181">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="52eb0-182">Namnet är Skift läges okänsligt.</span><span class="sxs-lookup"><span data-stu-id="52eb0-182">The name is case insensitive.</span></span>
  - <span data-ttu-id="52eb0-183">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: Namnet på säkerhets varnings principen.</span><span class="sxs-lookup"><span data-stu-id="52eb0-183">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="52eb0-184">`[ServerName <String>]`: Namnet på servern.</span><span class="sxs-lookup"><span data-stu-id="52eb0-184">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="52eb0-185">`[SubscriptionId <String>]`: Mål prenumerationens ID.</span><span class="sxs-lookup"><span data-stu-id="52eb0-185">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="52eb0-186">`[VirtualNetworkRuleName <String>]`: Namnet på den virtuella nätverks regeln.</span><span class="sxs-lookup"><span data-stu-id="52eb0-186">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="52eb0-187">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="52eb0-187">RELATED LINKS</span></span>
