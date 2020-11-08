---
external help file: ''
Module Name: Az.MariaDb
online version: https://docs.microsoft.com/en-us/powershell/module/az.mariadb/new-azmariadbreplica
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/New-AzMariaDbReplica.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/New-AzMariaDbReplica.md
ms.openlocfilehash: 0ce25af607d2460abf2ec4585dacc124a1f2e65c
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94271878"
---
# <span data-ttu-id="0ca46-101">New-AzMariaDbReplica</span><span class="sxs-lookup"><span data-stu-id="0ca46-101">New-AzMariaDbReplica</span></span>

## <span data-ttu-id="0ca46-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="0ca46-102">SYNOPSIS</span></span>
<span data-ttu-id="0ca46-103">Skapar en replik av en MariaDB-Server.</span><span class="sxs-lookup"><span data-stu-id="0ca46-103">Creates a replica of a MariaDB server.</span></span>

## <span data-ttu-id="0ca46-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="0ca46-104">SYNTAX</span></span>

### <span data-ttu-id="0ca46-105">Server namn (standard)</span><span class="sxs-lookup"><span data-stu-id="0ca46-105">ServerName (Default)</span></span>
```
New-AzMariaDbReplica -MasterName <String> -ReplicaName <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-Location <String>] [-Sku <String>] [-Tag <Hashtable>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="0ca46-106">ServerObject</span><span class="sxs-lookup"><span data-stu-id="0ca46-106">ServerObject</span></span>
```
New-AzMariaDbReplica -Master <IServer> -ReplicaName <String> [-SubscriptionId <String>] [-Location <String>]
 [-Sku <String>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="0ca46-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="0ca46-107">DESCRIPTION</span></span>
<span data-ttu-id="0ca46-108">Skapar en replik av en MariaDB-Server.</span><span class="sxs-lookup"><span data-stu-id="0ca46-108">Creates a replica of a MariaDB server.</span></span>

## <span data-ttu-id="0ca46-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="0ca46-109">EXAMPLES</span></span>

### <span data-ttu-id="0ca46-110">Exempel 1: skapa en replik databas för en MariaDB</span><span class="sxs-lookup"><span data-stu-id="0ca46-110">Example 1: Create a replica db for a MariaDB</span></span>
```powershell
PS C:\> New-AzMariaDbReplica -MasterName mariadb-test-9pebvn -ReplicaName mariadb-test-9pebvn-rep01 -ResourceGroupName mariadb-test-qu5ov0

Name                      Location AdministratorLogin Version StorageProfileStorageMb SkuName   SkuTier        SslEnforcement
----                      -------- ------------------ ------- ----------------------- -------   -------        --------------
mariadb-test-9pebvn-rep01 eastus   xpwjyfdgui         10.2    7168                    GP_Gen5_4 GeneralPurpose Enabled
```

<span data-ttu-id="0ca46-111">Det här kommandot skapar en replik databas för en MariaDB.</span><span class="sxs-lookup"><span data-stu-id="0ca46-111">This command creates a replica db for a MariaDB.</span></span>

### <span data-ttu-id="0ca46-112">Exempel 2: skapa en replik databas för en MariaDB</span><span class="sxs-lookup"><span data-stu-id="0ca46-112">Example 2: Create a replica db for a MariaDB</span></span>
```powershell
PS C:\> Get-AzMariaDbServer -Name mariadb-test-9pebvn -ResourceGroupName mariadb-test-qu5ov0 | New-AzMariaDbReplica -ReplicaName mariadb-test-9pebvn-rep02

Name                      Location AdministratorLogin Version StorageProfileStorageMb SkuName   SkuTier        SslEnforcement
----                      -------- ------------------ ------- ----------------------- -------   -------        --------------
mariadb-test-9pebvn-rep02 eastus   xpwjyfdgui         10.2    7168                    GP_Gen5_4 GeneralPurpose Enabled
```

<span data-ttu-id="0ca46-113">Det här kommandot skapar en replik databas för en MariaDB.</span><span class="sxs-lookup"><span data-stu-id="0ca46-113">This command creates a replica db for a MariaDB.</span></span>

### <span data-ttu-id="0ca46-114">Exempel 3: skapa en replik databas för en MariaDB</span><span class="sxs-lookup"><span data-stu-id="0ca46-114">Example 3: Create a replica db for a MariaDB</span></span>
```powershell
PS C:\> $mariaDb = Get-AzMariaDbServer -Name mariadb-test-9pebvn -ResourceGroupName mariadb-test-qu5ov0 
PS C:\> New-AzMariaDbReplica -Master $mariaDb -ReplicaName mariadb-test-9pebvn-rep03

Name                      Location AdministratorLogin Version StorageProfileStorageMb SkuName   SkuTier        SslEnforcement
----                      -------- ------------------ ------- ----------------------- -------   -------        --------------
mariadb-test-9pebvn-rep03 eastus   xpwjyfdgui         10.2    7168                    GP_Gen5_4 GeneralPurpose Enabled
```

<span data-ttu-id="0ca46-115">Det här kommandot med parametern InputObject skapar en replik databas med parametern InputObject för en MariaDB.</span><span class="sxs-lookup"><span data-stu-id="0ca46-115">This command with parameter inputobject creates a replica db with parameter inputobject for a MariaDB.</span></span>

## <span data-ttu-id="0ca46-116">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="0ca46-116">PARAMETERS</span></span>

### <span data-ttu-id="0ca46-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="0ca46-117">-AsJob</span></span>
<span data-ttu-id="0ca46-118">Köra kommandot som ett jobb</span><span class="sxs-lookup"><span data-stu-id="0ca46-118">Run the command as a job</span></span>

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

### <span data-ttu-id="0ca46-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0ca46-119">-DefaultProfile</span></span>
<span data-ttu-id="0ca46-120">regionen DefaultParameters autentiseringsuppgifterna, kontot, innehavaren och prenumerationen som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="0ca46-120">region DefaultParameters The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0ca46-121">-Plats</span><span class="sxs-lookup"><span data-stu-id="0ca46-121">-Location</span></span>
<span data-ttu-id="0ca46-122">Platsen som resursen finns i.</span><span class="sxs-lookup"><span data-stu-id="0ca46-122">The location the resource resides in.</span></span>

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

### <span data-ttu-id="0ca46-123">-Master</span><span class="sxs-lookup"><span data-stu-id="0ca46-123">-Master</span></span>
<span data-ttu-id="0ca46-124">Käll Server objekt att återställa från.</span><span class="sxs-lookup"><span data-stu-id="0ca46-124">The source server object to restore from.</span></span>
<span data-ttu-id="0ca46-125">För att konstruera kan du läsa avsnittet anteckningar för huvud egenskaper och skapa en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="0ca46-125">To construct, see NOTES section for MASTER properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.Api20180601Preview.IServer
Parameter Sets: ServerObject
Aliases: InputObject

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0ca46-126">-MasterName</span><span class="sxs-lookup"><span data-stu-id="0ca46-126">-MasterName</span></span>
<span data-ttu-id="0ca46-127">MariaDB Server namn.</span><span class="sxs-lookup"><span data-stu-id="0ca46-127">MariaDB server name.</span></span>

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

### <span data-ttu-id="0ca46-128">-Nowait</span><span class="sxs-lookup"><span data-stu-id="0ca46-128">-NoWait</span></span>
<span data-ttu-id="0ca46-129">Kör kommandot asynkront</span><span class="sxs-lookup"><span data-stu-id="0ca46-129">Run the command asynchronously</span></span>

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

### <span data-ttu-id="0ca46-130">-ReplicaName</span><span class="sxs-lookup"><span data-stu-id="0ca46-130">-ReplicaName</span></span>
<span data-ttu-id="0ca46-131">Replik namn.</span><span class="sxs-lookup"><span data-stu-id="0ca46-131">Replica name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ReplicaServerName, Name

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0ca46-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0ca46-132">-ResourceGroupName</span></span>
<span data-ttu-id="0ca46-133">Det här värdet kan hämtas från Azure Resource Manager API eller till portalen.</span><span class="sxs-lookup"><span data-stu-id="0ca46-133">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="0ca46-134">-SKU</span><span class="sxs-lookup"><span data-stu-id="0ca46-134">-Sku</span></span>
<span data-ttu-id="0ca46-135">Namnet på SKU: n, vanligt vis nivå + Family + cores, till exempel B_Gen4_1 GP_Gen5_8.</span><span class="sxs-lookup"><span data-stu-id="0ca46-135">The name of the sku, typically, tier + family + cores, e.g. B_Gen4_1, GP_Gen5_8.</span></span>

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

### <span data-ttu-id="0ca46-136">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="0ca46-136">-SubscriptionId</span></span>
<span data-ttu-id="0ca46-137">Prenumerations-ID är en del av URI: n för varje service samtal.</span><span class="sxs-lookup"><span data-stu-id="0ca46-137">The subscription ID is part of the URI for every service call.</span></span>

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

### <span data-ttu-id="0ca46-138">-Tagg</span><span class="sxs-lookup"><span data-stu-id="0ca46-138">-Tag</span></span>
<span data-ttu-id="0ca46-139">Programspecifika metadata i form av par med nyckelvärdena.</span><span class="sxs-lookup"><span data-stu-id="0ca46-139">Application-specific metadata in the form of key-value pairs.</span></span>

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

### <span data-ttu-id="0ca46-140">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="0ca46-140">-Confirm</span></span>
<span data-ttu-id="0ca46-141">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="0ca46-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0ca46-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0ca46-142">-WhatIf</span></span>
<span data-ttu-id="0ca46-143">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="0ca46-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0ca46-144">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="0ca46-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0ca46-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0ca46-145">CommonParameters</span></span>
<span data-ttu-id="0ca46-146">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0ca46-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0ca46-147">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="0ca46-147">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0ca46-148">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="0ca46-148">INPUTS</span></span>

### <span data-ttu-id="0ca46-149">Microsoft. Azure. PowerShell. cmdletar. MariaDb. Models. Api20180601Preview. IServer</span><span class="sxs-lookup"><span data-stu-id="0ca46-149">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.Api20180601Preview.IServer</span></span>

## <span data-ttu-id="0ca46-150">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="0ca46-150">OUTPUTS</span></span>

### <span data-ttu-id="0ca46-151">Microsoft. Azure. PowerShell. cmdletar. MariaDb. Models. Api20180601Preview. IServer</span><span class="sxs-lookup"><span data-stu-id="0ca46-151">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.Api20180601Preview.IServer</span></span>

## <span data-ttu-id="0ca46-152">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="0ca46-152">NOTES</span></span>

<span data-ttu-id="0ca46-153">ALIAS</span><span class="sxs-lookup"><span data-stu-id="0ca46-153">ALIASES</span></span>

<span data-ttu-id="0ca46-154">KOMPLEXA PARAMETER EGENSKAPER</span><span class="sxs-lookup"><span data-stu-id="0ca46-154">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="0ca46-155">Skapa en hash-tabell som innehåller lämpliga egenskaper för att lägga till de parametrar som beskrivs nedan.</span><span class="sxs-lookup"><span data-stu-id="0ca46-155">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="0ca46-156">Om du vill ha information om hash-tabeller kör Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="0ca46-156">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="0ca46-157">MASTER <IServer> : det käll Server objekt som du återställer från.</span><span class="sxs-lookup"><span data-stu-id="0ca46-157">MASTER <IServer>: The source server object to restore from.</span></span>
  - <span data-ttu-id="0ca46-158">`Location <String>`: Platsen som resursen finns i.</span><span class="sxs-lookup"><span data-stu-id="0ca46-158">`Location <String>`: The location the resource resides in.</span></span>
  - <span data-ttu-id="0ca46-159">`[Tag <ITrackedResourceTags>]`: Programspecifika metadata i form av par med nyckelvärdena.</span><span class="sxs-lookup"><span data-stu-id="0ca46-159">`[Tag <ITrackedResourceTags>]`: Application-specific metadata in the form of key-value pairs.</span></span>
    - <span data-ttu-id="0ca46-160">`[(Any) <String>]`: Detta indikerar att en egenskap kan läggas till i det här objektet.</span><span class="sxs-lookup"><span data-stu-id="0ca46-160">`[(Any) <String>]`: This indicates any property can be added to this object.</span></span>
  - <span data-ttu-id="0ca46-161">`[AdministratorLogin <String>]`: Administratörens inloggnings namn för en server.</span><span class="sxs-lookup"><span data-stu-id="0ca46-161">`[AdministratorLogin <String>]`: The administrator's login name of a server.</span></span> <span data-ttu-id="0ca46-162">Kan bara anges när servern skapas (och krävs för att skapa).</span><span class="sxs-lookup"><span data-stu-id="0ca46-162">Can only be specified when the server is being created (and is required for creation).</span></span>
  - <span data-ttu-id="0ca46-163">`[EarliestRestoreDate <DateTime?>]`: Tidig skapelse tid för återställnings punkt (ISO8601-format)</span><span class="sxs-lookup"><span data-stu-id="0ca46-163">`[EarliestRestoreDate <DateTime?>]`: Earliest restore point creation time (ISO8601 format)</span></span>
  - <span data-ttu-id="0ca46-164">`[FullyQualifiedDomainName <String>]`: Serverns fullkvalificerade domän namn.</span><span class="sxs-lookup"><span data-stu-id="0ca46-164">`[FullyQualifiedDomainName <String>]`: The fully qualified domain name of a server.</span></span>
  - <span data-ttu-id="0ca46-165">`[IdentityType <IdentityType?>]`: Identitets typen.</span><span class="sxs-lookup"><span data-stu-id="0ca46-165">`[IdentityType <IdentityType?>]`: The identity type.</span></span> <span data-ttu-id="0ca46-166">Ställ in detta på ' SystemAssigned ' för att automatiskt skapa och tilldela en Azure Active Directory-Huvudplats för resursen.</span><span class="sxs-lookup"><span data-stu-id="0ca46-166">Set this to 'SystemAssigned' in order to automatically create and assign an Azure Active Directory principal for the resource.</span></span>
  - <span data-ttu-id="0ca46-167">`[MasterServerId <String>]`: Huvud serverns ID för en replik Server.</span><span class="sxs-lookup"><span data-stu-id="0ca46-167">`[MasterServerId <String>]`: The master server id of a replica server.</span></span>
  - <span data-ttu-id="0ca46-168">`[ReplicaCapacity <Int32?>]`: Det högsta antalet repliker som en huvud server kan ha.</span><span class="sxs-lookup"><span data-stu-id="0ca46-168">`[ReplicaCapacity <Int32?>]`: The maximum number of replicas that a master server can have.</span></span>
  - <span data-ttu-id="0ca46-169">`[ReplicationRole <String>]`: Serverns replikeringsrelation.</span><span class="sxs-lookup"><span data-stu-id="0ca46-169">`[ReplicationRole <String>]`: The replication role of the server.</span></span>
  - <span data-ttu-id="0ca46-170">`[SkuCapacity <Int32?>]`: Skalan upp/ut-kapacitet som representerar serverns beräknade enheter.</span><span class="sxs-lookup"><span data-stu-id="0ca46-170">`[SkuCapacity <Int32?>]`: The scale up/out capacity, representing server's compute units.</span></span>
  - <span data-ttu-id="0ca46-171">`[SkuFamily <String>]`: Produkt familjen.</span><span class="sxs-lookup"><span data-stu-id="0ca46-171">`[SkuFamily <String>]`: The family of hardware.</span></span>
  - <span data-ttu-id="0ca46-172">`[SkuName <String>]`: Namnet på SKU: n, vanligt vis nivå + Family + cores, till exempel B_Gen4_1 GP_Gen5_8.</span><span class="sxs-lookup"><span data-stu-id="0ca46-172">`[SkuName <String>]`: The name of the sku, typically, tier + family + cores, e.g. B_Gen4_1, GP_Gen5_8.</span></span>
  - <span data-ttu-id="0ca46-173">`[SkuSize <String>]`: Storleks koden, som ska tolkas av resursen.</span><span class="sxs-lookup"><span data-stu-id="0ca46-173">`[SkuSize <String>]`: The size code, to be interpreted by resource as appropriate.</span></span>
  - <span data-ttu-id="0ca46-174">`[SkuTier <SkuTier?>]`: Nivån för den aktuella SKU: n, t. ex.</span><span class="sxs-lookup"><span data-stu-id="0ca46-174">`[SkuTier <SkuTier?>]`: The tier of the particular SKU, e.g. Basic.</span></span>
  - <span data-ttu-id="0ca46-175">`[SslEnforcement <SslEnforcementEnum?>]`: Aktivera SSL-tvång eller inte vid anslutning till server.</span><span class="sxs-lookup"><span data-stu-id="0ca46-175">`[SslEnforcement <SslEnforcementEnum?>]`: Enable ssl enforcement or not when connect to server.</span></span>
  - <span data-ttu-id="0ca46-176">`[StorageProfileBackupRetentionDay <Int32?>]`: Bevarande dagar för säkerhets kopior för servern.</span><span class="sxs-lookup"><span data-stu-id="0ca46-176">`[StorageProfileBackupRetentionDay <Int32?>]`: Backup retention days for the server.</span></span>
  - <span data-ttu-id="0ca46-177">`[StorageProfileGeoRedundantBackup <GeoRedundantBackup?>]`: Aktivera Geo-redundant eller ej för säkerhets kopiering av Server.</span><span class="sxs-lookup"><span data-stu-id="0ca46-177">`[StorageProfileGeoRedundantBackup <GeoRedundantBackup?>]`: Enable Geo-redundant or not for server backup.</span></span>
  - <span data-ttu-id="0ca46-178">`[StorageProfileStorageAutogrow <StorageAutogrow?>]`: Aktivera automatisk tillväxt av lagring.</span><span class="sxs-lookup"><span data-stu-id="0ca46-178">`[StorageProfileStorageAutogrow <StorageAutogrow?>]`: Enable Storage Auto Grow.</span></span>
  - <span data-ttu-id="0ca46-179">`[StorageProfileStorageMb <Int32?>]`: Högsta tillåtna lagrings utrymme för en server.</span><span class="sxs-lookup"><span data-stu-id="0ca46-179">`[StorageProfileStorageMb <Int32?>]`: Max storage allowed for a server.</span></span>
  - <span data-ttu-id="0ca46-180">`[UserVisibleState <ServerState?>]`: Ett tillstånd för en server som är synlig för användaren.</span><span class="sxs-lookup"><span data-stu-id="0ca46-180">`[UserVisibleState <ServerState?>]`: A state of a server that is visible to user.</span></span>
  - <span data-ttu-id="0ca46-181">`[Version <ServerVersion?>]`: Server version.</span><span class="sxs-lookup"><span data-stu-id="0ca46-181">`[Version <ServerVersion?>]`: Server version.</span></span>

## <span data-ttu-id="0ca46-182">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="0ca46-182">RELATED LINKS</span></span>

