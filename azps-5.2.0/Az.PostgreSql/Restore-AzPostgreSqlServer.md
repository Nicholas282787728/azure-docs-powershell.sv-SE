---
external help file: ''
Module Name: Az.PostgreSql
online version: https://docs.microsoft.com/en-us/powershell/module/az.postgresql/restore-azpostgresqlserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Restore-AzPostgreSqlServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Restore-AzPostgreSqlServer.md
ms.openlocfilehash: c9e4134b6787f78442a18836c15ce190c3e685d8
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98391899"
---
# <span data-ttu-id="1ec18-101">Restore-AzPostgreSqlServer</span><span class="sxs-lookup"><span data-stu-id="1ec18-101">Restore-AzPostgreSqlServer</span></span>

## <span data-ttu-id="1ec18-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="1ec18-102">SYNOPSIS</span></span>
<span data-ttu-id="1ec18-103">Återställa en server från en befintlig säkerhets kopia</span><span class="sxs-lookup"><span data-stu-id="1ec18-103">Restore a server from an existing backup</span></span>

## <span data-ttu-id="1ec18-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="1ec18-104">SYNTAX</span></span>

### <span data-ttu-id="1ec18-105">Återställnings format (standard)</span><span class="sxs-lookup"><span data-stu-id="1ec18-105">GeoRestore (Default)</span></span>
```
Restore-AzPostgreSqlServer -Name <String> -ResourceGroupName <String> -InputObject <IServer> -UseGeoRestore
 [-SubscriptionId <String>] [-Location <String>] [-Sku <String>] [-Tag <Hashtable>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="1ec18-106">PointInTimeRestore</span><span class="sxs-lookup"><span data-stu-id="1ec18-106">PointInTimeRestore</span></span>
```
Restore-AzPostgreSqlServer -Name <String> -ResourceGroupName <String> -InputObject <IServer>
 -RestorePointInTime <DateTime> -UsePointInTimeRestore [-SubscriptionId <String>] [-Location <String>]
 [-Sku <String>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="1ec18-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="1ec18-107">DESCRIPTION</span></span>
<span data-ttu-id="1ec18-108">Återställa en server från en befintlig säkerhets kopia</span><span class="sxs-lookup"><span data-stu-id="1ec18-108">Restore a server from an existing backup</span></span>

## <span data-ttu-id="1ec18-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="1ec18-109">EXAMPLES</span></span>

### <span data-ttu-id="1ec18-110">Exempel 1: Återställ PostgreSql server med återställning av en replik</span><span class="sxs-lookup"><span data-stu-id="1ec18-110">Example 1: Restore PostgreSql server using GeoReplica Restore</span></span>
```powershell
PS C:\> Get-AzPostgreSqlServer -ResourceGroupName PostgreSqlTestRG -ServerName postgresqltestserverreplica | Restore-AzPostgreSqlServer -Name PostgreSqlTestServer -ResourceGroupName PostgreSqlTestRG -UseGeoRestore

Name                 Location AdministratorLogin Version StorageProfileStorageMb SkuName   SkuTier        SslEnforcement
----                 -------- ------------------ ------- ----------------------- -------   -------        --------------
postgresqltestserver eastus   pwsh               9.6     5120                    GP_Gen5_4 GeneralPurpose Enabled
```

<span data-ttu-id="1ec18-111">Denna cmdlet återställer PostgreSql-servern med återställning av en kopia.</span><span class="sxs-lookup"><span data-stu-id="1ec18-111">This cmdlet restores PostgreSql server using GeoReplica Restore.</span></span>

### <span data-ttu-id="1ec18-112">Exempel 2: Återställ PostgreSql server med PointInTime-återställning</span><span class="sxs-lookup"><span data-stu-id="1ec18-112">Example 2: Restore PostgreSql server using PointInTime Restore</span></span>
```powershell
PS C:\> $restorePointInTime = (Get-Date).AddMinutes(-10)
PS C:\> Get-AzPostgreSqlServer -ResourceGroupName PostgreSqlTestRG -ServerName PostgreSqlTestServer | Restore-AzPostgreSqlServer -Name PostgreSqlTestServerGEO -ResourceGroupName PostgreSqlTestRG -RestorePointInTime $restorePointInTime -UsePointInTimeRestore

Name                    Location AdministratorLogin Version StorageProfileStorageMb SkuName   SkuTier        SslEnforcement
----                    -------- ------------------ ------- ----------------------- -------   -------        --------------
postgresqltestservergeo eastus   pwsh               9.6     5120                    GP_Gen5_4 GeneralPurpose Enabled
```

<span data-ttu-id="1ec18-113">De här cmdletarna återställer PostgreSql-servern med PointInTime-återställning.</span><span class="sxs-lookup"><span data-stu-id="1ec18-113">These cmdlets restore PostgreSql server using PointInTime Restore.</span></span>

## <span data-ttu-id="1ec18-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="1ec18-114">PARAMETERS</span></span>

### <span data-ttu-id="1ec18-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="1ec18-115">-AsJob</span></span>
<span data-ttu-id="1ec18-116">Kör kommandot som ett jobb.</span><span class="sxs-lookup"><span data-stu-id="1ec18-116">Run the command as a job.</span></span>

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

### <span data-ttu-id="1ec18-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1ec18-117">-DefaultProfile</span></span>
<span data-ttu-id="1ec18-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="1ec18-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1ec18-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1ec18-119">-InputObject</span></span>
<span data-ttu-id="1ec18-120">Käll Server objekt att återställa från.</span><span class="sxs-lookup"><span data-stu-id="1ec18-120">The source server object to restore from.</span></span>
<span data-ttu-id="1ec18-121">För att konstruera kan du läsa avsnittet anteckningar för INPUTOBJECT-egenskaper och skapa en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="1ec18-121">To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.Api20171201.IServer
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1ec18-122">-Plats</span><span class="sxs-lookup"><span data-stu-id="1ec18-122">-Location</span></span>
<span data-ttu-id="1ec18-123">Platsen som resursen finns i.</span><span class="sxs-lookup"><span data-stu-id="1ec18-123">The location the resource resides in.</span></span>

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

### <span data-ttu-id="1ec18-124">-Namn</span><span class="sxs-lookup"><span data-stu-id="1ec18-124">-Name</span></span>
<span data-ttu-id="1ec18-125">Namnet på servern.</span><span class="sxs-lookup"><span data-stu-id="1ec18-125">The name of the server.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ServerName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1ec18-126">-Nowait</span><span class="sxs-lookup"><span data-stu-id="1ec18-126">-NoWait</span></span>
<span data-ttu-id="1ec18-127">Kör kommandot asynkront.</span><span class="sxs-lookup"><span data-stu-id="1ec18-127">Run the command asynchronously.</span></span>

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

### <span data-ttu-id="1ec18-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1ec18-128">-ResourceGroupName</span></span>
<span data-ttu-id="1ec18-129">Namnet på resurs gruppen som innehåller resursen kan du hämta det här värdet från Azure Resource Manager API eller portalen.</span><span class="sxs-lookup"><span data-stu-id="1ec18-129">The name of the resource group that contains the resource, You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1ec18-130">-RestorePointInTime</span><span class="sxs-lookup"><span data-stu-id="1ec18-130">-RestorePointInTime</span></span>
<span data-ttu-id="1ec18-131">Platsen som resursen finns i.</span><span class="sxs-lookup"><span data-stu-id="1ec18-131">The location the resource resides in.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: PointInTimeRestore
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1ec18-132">-SKU</span><span class="sxs-lookup"><span data-stu-id="1ec18-132">-Sku</span></span>
<span data-ttu-id="1ec18-133">Namnet på SKU: n, vanligt vis nivå + Family + cores, till exempel B_Gen4_1 GP_Gen5_8.</span><span class="sxs-lookup"><span data-stu-id="1ec18-133">The name of the sku, typically, tier + family + cores, e.g. B_Gen4_1, GP_Gen5_8.</span></span>

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

### <span data-ttu-id="1ec18-134">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="1ec18-134">-SubscriptionId</span></span>
<span data-ttu-id="1ec18-135">Det prenumerations-ID som identifierar en Azure-prenumeration.</span><span class="sxs-lookup"><span data-stu-id="1ec18-135">The subscription ID that identifies an Azure subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1ec18-136">-Tagg</span><span class="sxs-lookup"><span data-stu-id="1ec18-136">-Tag</span></span>
<span data-ttu-id="1ec18-137">Programspecifika metadata i form av par med nyckelvärdena.</span><span class="sxs-lookup"><span data-stu-id="1ec18-137">Application-specific metadata in the form of key-value pairs.</span></span>

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

### <span data-ttu-id="1ec18-138">-UseGeoRestore</span><span class="sxs-lookup"><span data-stu-id="1ec18-138">-UseGeoRestore</span></span>
<span data-ttu-id="1ec18-139">Använda geo-läge för att återställa</span><span class="sxs-lookup"><span data-stu-id="1ec18-139">Use Geo mode to restore</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: GeoRestore
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1ec18-140">-UsePointInTimeRestore</span><span class="sxs-lookup"><span data-stu-id="1ec18-140">-UsePointInTimeRestore</span></span>
<span data-ttu-id="1ec18-141">Använda PointInTime-läget för att återställa</span><span class="sxs-lookup"><span data-stu-id="1ec18-141">Use PointInTime mode to restore</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: PointInTimeRestore
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1ec18-142">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="1ec18-142">-Confirm</span></span>
<span data-ttu-id="1ec18-143">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="1ec18-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1ec18-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1ec18-144">-WhatIf</span></span>
<span data-ttu-id="1ec18-145">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="1ec18-145">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1ec18-146">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="1ec18-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1ec18-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1ec18-147">CommonParameters</span></span>
<span data-ttu-id="1ec18-148">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1ec18-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1ec18-149">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="1ec18-149">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1ec18-150">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="1ec18-150">INPUTS</span></span>

### <span data-ttu-id="1ec18-151">Microsoft. Azure. PowerShell. cmdletar. PostgreSql. Models. Api20171201. IServer</span><span class="sxs-lookup"><span data-stu-id="1ec18-151">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.Api20171201.IServer</span></span>

## <span data-ttu-id="1ec18-152">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="1ec18-152">OUTPUTS</span></span>

### <span data-ttu-id="1ec18-153">Microsoft. Azure. PowerShell. cmdletar. PostgreSql. Models. Api20171201. IServer</span><span class="sxs-lookup"><span data-stu-id="1ec18-153">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.Api20171201.IServer</span></span>

## <span data-ttu-id="1ec18-154">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="1ec18-154">NOTES</span></span>

<span data-ttu-id="1ec18-155">ALIAS</span><span class="sxs-lookup"><span data-stu-id="1ec18-155">ALIASES</span></span>

<span data-ttu-id="1ec18-156">KOMPLEXA PARAMETER EGENSKAPER</span><span class="sxs-lookup"><span data-stu-id="1ec18-156">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="1ec18-157">Skapa en hash-tabell som innehåller lämpliga egenskaper för att lägga till de parametrar som beskrivs nedan.</span><span class="sxs-lookup"><span data-stu-id="1ec18-157">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="1ec18-158">Om du vill ha information om hash-tabeller kör Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="1ec18-158">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="1ec18-159">INPUTOBJECT <IServer> : käll Server objekt som ska återställas från.</span><span class="sxs-lookup"><span data-stu-id="1ec18-159">INPUTOBJECT <IServer>: The source server object to restore from.</span></span>
  - <span data-ttu-id="1ec18-160">`Location <String>`: Platsen som resursen finns i.</span><span class="sxs-lookup"><span data-stu-id="1ec18-160">`Location <String>`: The location the resource resides in.</span></span>
  - <span data-ttu-id="1ec18-161">`[Tag <ITrackedResourceTags>]`: Programspecifika metadata i form av par med nyckelvärdena.</span><span class="sxs-lookup"><span data-stu-id="1ec18-161">`[Tag <ITrackedResourceTags>]`: Application-specific metadata in the form of key-value pairs.</span></span>
    - <span data-ttu-id="1ec18-162">`[(Any) <String>]`: Detta indikerar att en egenskap kan läggas till i det här objektet.</span><span class="sxs-lookup"><span data-stu-id="1ec18-162">`[(Any) <String>]`: This indicates any property can be added to this object.</span></span>
  - <span data-ttu-id="1ec18-163">`[AdministratorLogin <String>]`: Administratörens inloggnings namn för en server.</span><span class="sxs-lookup"><span data-stu-id="1ec18-163">`[AdministratorLogin <String>]`: The administrator's login name of a server.</span></span> <span data-ttu-id="1ec18-164">Kan bara anges när servern skapas (och krävs för att skapa).</span><span class="sxs-lookup"><span data-stu-id="1ec18-164">Can only be specified when the server is being created (and is required for creation).</span></span>
  - <span data-ttu-id="1ec18-165">`[EarliestRestoreDate <DateTime?>]`: Tidig skapelse tid för återställnings punkt (ISO8601-format)</span><span class="sxs-lookup"><span data-stu-id="1ec18-165">`[EarliestRestoreDate <DateTime?>]`: Earliest restore point creation time (ISO8601 format)</span></span>
  - <span data-ttu-id="1ec18-166">`[FullyQualifiedDomainName <String>]`: Serverns fullkvalificerade domän namn.</span><span class="sxs-lookup"><span data-stu-id="1ec18-166">`[FullyQualifiedDomainName <String>]`: The fully qualified domain name of a server.</span></span>
  - <span data-ttu-id="1ec18-167">`[IdentityType <IdentityType?>]`: Identitets typen.</span><span class="sxs-lookup"><span data-stu-id="1ec18-167">`[IdentityType <IdentityType?>]`: The identity type.</span></span> <span data-ttu-id="1ec18-168">Ställ in detta på ' SystemAssigned ' för att automatiskt skapa och tilldela en Azure Active Directory-Huvudplats för resursen.</span><span class="sxs-lookup"><span data-stu-id="1ec18-168">Set this to 'SystemAssigned' in order to automatically create and assign an Azure Active Directory principal for the resource.</span></span>
  - <span data-ttu-id="1ec18-169">`[InfrastructureEncryption <InfrastructureEncryption?>]`: Status som visar om infrastrukturen för infrastruktur är aktive rad.</span><span class="sxs-lookup"><span data-stu-id="1ec18-169">`[InfrastructureEncryption <InfrastructureEncryption?>]`: Status showing whether the server enabled infrastructure encryption.</span></span>
  - <span data-ttu-id="1ec18-170">`[MasterServerId <String>]`: Huvud serverns ID för en replik Server.</span><span class="sxs-lookup"><span data-stu-id="1ec18-170">`[MasterServerId <String>]`: The master server id of a replica server.</span></span>
  - <span data-ttu-id="1ec18-171">`[MinimalTlsVersion <MinimalTlsVersionEnum?>]`: Påtvinga en minimal TLS-version för servern.</span><span class="sxs-lookup"><span data-stu-id="1ec18-171">`[MinimalTlsVersion <MinimalTlsVersionEnum?>]`: Enforce a minimal Tls version for the server.</span></span>
  - <span data-ttu-id="1ec18-172">`[PublicNetworkAccess <PublicNetworkAccessEnum?>]`: Oberoende nätverks åtkomst tillåts för den här servern.</span><span class="sxs-lookup"><span data-stu-id="1ec18-172">`[PublicNetworkAccess <PublicNetworkAccessEnum?>]`: Whether or not public network access is allowed for this server.</span></span> <span data-ttu-id="1ec18-173">Värdet är valfritt, men om det är skickat måste det vara aktiverat eller inaktiverat</span><span class="sxs-lookup"><span data-stu-id="1ec18-173">Value is optional but if passed in, must be 'Enabled' or 'Disabled'</span></span>
  - <span data-ttu-id="1ec18-174">`[ReplicaCapacity <Int32?>]`: Det högsta antalet repliker som en huvud server kan ha.</span><span class="sxs-lookup"><span data-stu-id="1ec18-174">`[ReplicaCapacity <Int32?>]`: The maximum number of replicas that a master server can have.</span></span>
  - <span data-ttu-id="1ec18-175">`[ReplicationRole <String>]`: Serverns replikeringsrelation.</span><span class="sxs-lookup"><span data-stu-id="1ec18-175">`[ReplicationRole <String>]`: The replication role of the server.</span></span>
  - <span data-ttu-id="1ec18-176">`[SkuCapacity <Int32?>]`: Skalan upp/ut-kapacitet som representerar serverns beräknade enheter.</span><span class="sxs-lookup"><span data-stu-id="1ec18-176">`[SkuCapacity <Int32?>]`: The scale up/out capacity, representing server's compute units.</span></span>
  - <span data-ttu-id="1ec18-177">`[SkuFamily <String>]`: Produkt familjen.</span><span class="sxs-lookup"><span data-stu-id="1ec18-177">`[SkuFamily <String>]`: The family of hardware.</span></span>
  - <span data-ttu-id="1ec18-178">`[SkuName <String>]`: Namnet på SKU: n, vanligt vis nivå + Family + cores, till exempel B_Gen4_1 GP_Gen5_8.</span><span class="sxs-lookup"><span data-stu-id="1ec18-178">`[SkuName <String>]`: The name of the sku, typically, tier + family + cores, e.g. B_Gen4_1, GP_Gen5_8.</span></span>
  - <span data-ttu-id="1ec18-179">`[SkuSize <String>]`: Storleks koden, som ska tolkas av resursen.</span><span class="sxs-lookup"><span data-stu-id="1ec18-179">`[SkuSize <String>]`: The size code, to be interpreted by resource as appropriate.</span></span>
  - <span data-ttu-id="1ec18-180">`[SkuTier <SkuTier?>]`: Nivån för den aktuella SKU: n, t. ex.</span><span class="sxs-lookup"><span data-stu-id="1ec18-180">`[SkuTier <SkuTier?>]`: The tier of the particular SKU, e.g. Basic.</span></span>
  - <span data-ttu-id="1ec18-181">`[SslEnforcement <SslEnforcementEnum?>]`: Aktivera SSL-tvång eller inte vid anslutning till server.</span><span class="sxs-lookup"><span data-stu-id="1ec18-181">`[SslEnforcement <SslEnforcementEnum?>]`: Enable ssl enforcement or not when connect to server.</span></span>
  - <span data-ttu-id="1ec18-182">`[StorageProfileBackupRetentionDay <Int32?>]`: Bevarande dagar för säkerhets kopior för servern.</span><span class="sxs-lookup"><span data-stu-id="1ec18-182">`[StorageProfileBackupRetentionDay <Int32?>]`: Backup retention days for the server.</span></span>
  - <span data-ttu-id="1ec18-183">`[StorageProfileGeoRedundantBackup <GeoRedundantBackup?>]`: Aktivera Geo-redundant eller ej för säkerhets kopiering av Server.</span><span class="sxs-lookup"><span data-stu-id="1ec18-183">`[StorageProfileGeoRedundantBackup <GeoRedundantBackup?>]`: Enable Geo-redundant or not for server backup.</span></span>
  - <span data-ttu-id="1ec18-184">`[StorageProfileStorageAutogrow <StorageAutogrow?>]`: Aktivera automatisk tillväxt av lagring.</span><span class="sxs-lookup"><span data-stu-id="1ec18-184">`[StorageProfileStorageAutogrow <StorageAutogrow?>]`: Enable Storage Auto Grow.</span></span>
  - <span data-ttu-id="1ec18-185">`[StorageProfileStorageMb <Int32?>]`: Högsta tillåtna lagrings utrymme för en server.</span><span class="sxs-lookup"><span data-stu-id="1ec18-185">`[StorageProfileStorageMb <Int32?>]`: Max storage allowed for a server.</span></span>
  - <span data-ttu-id="1ec18-186">`[UserVisibleState <ServerState?>]`: Ett tillstånd för en server som är synlig för användaren.</span><span class="sxs-lookup"><span data-stu-id="1ec18-186">`[UserVisibleState <ServerState?>]`: A state of a server that is visible to user.</span></span>
  - <span data-ttu-id="1ec18-187">`[Version <ServerVersion?>]`: Server version.</span><span class="sxs-lookup"><span data-stu-id="1ec18-187">`[Version <ServerVersion?>]`: Server version.</span></span>

## <span data-ttu-id="1ec18-188">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="1ec18-188">RELATED LINKS</span></span>

