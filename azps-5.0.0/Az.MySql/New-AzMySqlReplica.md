---
external help file: ''
Module Name: Az.MySql
online version: https://docs.microsoft.com/en-us/powershell/module/az.mysql/new-azmysqlreplica
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/New-AzMySqlReplica.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/New-AzMySqlReplica.md
ms.openlocfilehash: 5e5d83266dd86ccaf0bd5037c6af01f8b1846a69
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94272621"
---
# <span data-ttu-id="198e3-101">New-AzMySqlReplica</span><span class="sxs-lookup"><span data-stu-id="198e3-101">New-AzMySqlReplica</span></span>

## <span data-ttu-id="198e3-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="198e3-102">SYNOPSIS</span></span>
<span data-ttu-id="198e3-103">Skapar en ny replik från en befintlig databas.</span><span class="sxs-lookup"><span data-stu-id="198e3-103">Creates a new replica from an existing database.</span></span>

## <span data-ttu-id="198e3-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="198e3-104">SYNTAX</span></span>

```
New-AzMySqlReplica -Replica <String> -ResourceGroupName <String> -Master <IServer> [-SubscriptionId <String>]
 [-Location <String>] [-Sku <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="198e3-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="198e3-105">DESCRIPTION</span></span>
<span data-ttu-id="198e3-106">Skapar en ny replik från en befintlig databas.</span><span class="sxs-lookup"><span data-stu-id="198e3-106">Creates a new replica from an existing database.</span></span>

## <span data-ttu-id="198e3-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="198e3-107">EXAMPLES</span></span>

### <span data-ttu-id="198e3-108">Exempel 1: skapa en ny server replik för MySql</span><span class="sxs-lookup"><span data-stu-id="198e3-108">Example 1: Create a new MySql server replica</span></span>
```powershell
PS C:\> Get-AzMySqlServer -ResourceGroupName PowershellMySqlTest -ServerName mysql-test | New-AzMySqlReplica -Replica mysql-test-replica -ResourceGroupName PowershellMySqlTest

Name               Location AdministratorLogin Version StorageProfileStorageMb SkuName   SkuTier        SslEnforcement
----               -------- ------------------ ------- ----------------------- -------   -------        --------------
mysql-test-replica eastus   mysql_test         5.7     10240                   GP_Gen5_4 GeneralPurpose Disabled
```

<span data-ttu-id="198e3-109">Denna cmdlet skapar en ny MySql-gruppserver.</span><span class="sxs-lookup"><span data-stu-id="198e3-109">This cmdlet creates a new MySql server replica.</span></span>

### <span data-ttu-id="198e3-110">Exempel 2: skapa en ny server replik för MySql</span><span class="sxs-lookup"><span data-stu-id="198e3-110">Example 2: Create a new MySql server replica</span></span>
```powershell
PS C:\> $mysql = Get-AzMySqlServer -ResourceGroupName PowershellMySqlTest -ServerName mysql-test
PS C:\> New-AzMySqlReplica -Master $mysql -Replica mysql-test-replica -ResourceGroupName PowershellMySqlTest

Name               Location AdministratorLogin Version StorageProfileStorageMb SkuName   SkuTier        SslEnforcement
----               -------- ------------------ ------- ----------------------- -------   -------        --------------
mysql-test-replica eastus   mysql_test         5.7     10240                   GP_Gen5_4 GeneralPurpose Disabled
```

<span data-ttu-id="198e3-111">Denna cmdlet med parameter huvud (InputObject) skapar en ny MySql Server-replik.</span><span class="sxs-lookup"><span data-stu-id="198e3-111">This cmdlet with parameter master(inputobject) creates a new MySql server replica.</span></span>

## <span data-ttu-id="198e3-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="198e3-112">PARAMETERS</span></span>

### <span data-ttu-id="198e3-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="198e3-113">-AsJob</span></span>
<span data-ttu-id="198e3-114">Kör kommandot som ett jobb.</span><span class="sxs-lookup"><span data-stu-id="198e3-114">Run the command as a job.</span></span>

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

### <span data-ttu-id="198e3-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="198e3-115">-DefaultProfile</span></span>
<span data-ttu-id="198e3-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="198e3-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="198e3-117">-Plats</span><span class="sxs-lookup"><span data-stu-id="198e3-117">-Location</span></span>
<span data-ttu-id="198e3-118">Platsen som resursen finns i.</span><span class="sxs-lookup"><span data-stu-id="198e3-118">The location the resource resides in.</span></span>

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

### <span data-ttu-id="198e3-119">-Master</span><span class="sxs-lookup"><span data-stu-id="198e3-119">-Master</span></span>
<span data-ttu-id="198e3-120">Käll Server objekt för att skapa replik från.</span><span class="sxs-lookup"><span data-stu-id="198e3-120">The source server object to create replica from.</span></span>
<span data-ttu-id="198e3-121">För att konstruera kan du läsa avsnittet anteckningar för huvud egenskaper och skapa en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="198e3-121">To construct, see NOTES section for MASTER properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20171201.IServer
Parameter Sets: (All)
Aliases: InputObject

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="198e3-122">-Nowait</span><span class="sxs-lookup"><span data-stu-id="198e3-122">-NoWait</span></span>
<span data-ttu-id="198e3-123">Kör kommandot asynkront.</span><span class="sxs-lookup"><span data-stu-id="198e3-123">Run the command asynchronously.</span></span>

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

### <span data-ttu-id="198e3-124">-Replik</span><span class="sxs-lookup"><span data-stu-id="198e3-124">-Replica</span></span>
<span data-ttu-id="198e3-125">Namnet på servern.</span><span class="sxs-lookup"><span data-stu-id="198e3-125">The name of the server.</span></span>

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

### <span data-ttu-id="198e3-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="198e3-126">-ResourceGroupName</span></span>
<span data-ttu-id="198e3-127">Namnet på resurs gruppen som innehåller resursen kan du hämta det här värdet från Azure Resource Manager API eller portalen.</span><span class="sxs-lookup"><span data-stu-id="198e3-127">The name of the resource group that contains the resource, You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="198e3-128">-SKU</span><span class="sxs-lookup"><span data-stu-id="198e3-128">-Sku</span></span>
<span data-ttu-id="198e3-129">Namnet på SKU: n, vanligt vis nivå + Family + cores, till exempel B_Gen4_1 GP_Gen5_8.</span><span class="sxs-lookup"><span data-stu-id="198e3-129">The name of the sku, typically, tier + family + cores, e.g. B_Gen4_1, GP_Gen5_8.</span></span>

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

### <span data-ttu-id="198e3-130">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="198e3-130">-SubscriptionId</span></span>
<span data-ttu-id="198e3-131">Det prenumerations-ID som identifierar en Azure-prenumeration.</span><span class="sxs-lookup"><span data-stu-id="198e3-131">The subscription ID that identifies an Azure subscription.</span></span>

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

### <span data-ttu-id="198e3-132">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="198e3-132">-Confirm</span></span>
<span data-ttu-id="198e3-133">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="198e3-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="198e3-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="198e3-134">-WhatIf</span></span>
<span data-ttu-id="198e3-135">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="198e3-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="198e3-136">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="198e3-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="198e3-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="198e3-137">CommonParameters</span></span>
<span data-ttu-id="198e3-138">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="198e3-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="198e3-139">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="198e3-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="198e3-140">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="198e3-140">INPUTS</span></span>

### <span data-ttu-id="198e3-141">Microsoft. Azure. PowerShell. cmdletar. MySql. Models. Api20171201. IServer</span><span class="sxs-lookup"><span data-stu-id="198e3-141">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20171201.IServer</span></span>

## <span data-ttu-id="198e3-142">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="198e3-142">OUTPUTS</span></span>

### <span data-ttu-id="198e3-143">Microsoft. Azure. PowerShell. cmdletar. MySql. Models. Api20171201. IServer</span><span class="sxs-lookup"><span data-stu-id="198e3-143">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20171201.IServer</span></span>

## <span data-ttu-id="198e3-144">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="198e3-144">NOTES</span></span>

<span data-ttu-id="198e3-145">ALIAS</span><span class="sxs-lookup"><span data-stu-id="198e3-145">ALIASES</span></span>

<span data-ttu-id="198e3-146">KOMPLEXA PARAMETER EGENSKAPER</span><span class="sxs-lookup"><span data-stu-id="198e3-146">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="198e3-147">Skapa en hash-tabell som innehåller lämpliga egenskaper för att lägga till de parametrar som beskrivs nedan.</span><span class="sxs-lookup"><span data-stu-id="198e3-147">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="198e3-148">Om du vill ha information om hash-tabeller kör Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="198e3-148">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="198e3-149">MASTER <IServer> : käll Server objekt för att skapa replik från.</span><span class="sxs-lookup"><span data-stu-id="198e3-149">MASTER <IServer>: The source server object to create replica from.</span></span>
  - <span data-ttu-id="198e3-150">`Location <String>`: Platsen som resursen finns i.</span><span class="sxs-lookup"><span data-stu-id="198e3-150">`Location <String>`: The location the resource resides in.</span></span>
  - <span data-ttu-id="198e3-151">`[Tag <ITrackedResourceTags>]`: Programspecifika metadata i form av par med nyckelvärdena.</span><span class="sxs-lookup"><span data-stu-id="198e3-151">`[Tag <ITrackedResourceTags>]`: Application-specific metadata in the form of key-value pairs.</span></span>
    - <span data-ttu-id="198e3-152">`[(Any) <String>]`: Detta indikerar att en egenskap kan läggas till i det här objektet.</span><span class="sxs-lookup"><span data-stu-id="198e3-152">`[(Any) <String>]`: This indicates any property can be added to this object.</span></span>
  - <span data-ttu-id="198e3-153">`[AdministratorLogin <String>]`: Administratörens inloggnings namn för en server.</span><span class="sxs-lookup"><span data-stu-id="198e3-153">`[AdministratorLogin <String>]`: The administrator's login name of a server.</span></span> <span data-ttu-id="198e3-154">Kan bara anges när servern skapas (och krävs för att skapa).</span><span class="sxs-lookup"><span data-stu-id="198e3-154">Can only be specified when the server is being created (and is required for creation).</span></span>
  - <span data-ttu-id="198e3-155">`[EarliestRestoreDate <DateTime?>]`: Tidig skapelse tid för återställnings punkt (ISO8601-format)</span><span class="sxs-lookup"><span data-stu-id="198e3-155">`[EarliestRestoreDate <DateTime?>]`: Earliest restore point creation time (ISO8601 format)</span></span>
  - <span data-ttu-id="198e3-156">`[FullyQualifiedDomainName <String>]`: Serverns fullkvalificerade domän namn.</span><span class="sxs-lookup"><span data-stu-id="198e3-156">`[FullyQualifiedDomainName <String>]`: The fully qualified domain name of a server.</span></span>
  - <span data-ttu-id="198e3-157">`[IdentityType <IdentityType?>]`: Identitets typen.</span><span class="sxs-lookup"><span data-stu-id="198e3-157">`[IdentityType <IdentityType?>]`: The identity type.</span></span> <span data-ttu-id="198e3-158">Ställ in detta på ' SystemAssigned ' för att automatiskt skapa och tilldela en Azure Active Directory-Huvudplats för resursen.</span><span class="sxs-lookup"><span data-stu-id="198e3-158">Set this to 'SystemAssigned' in order to automatically create and assign an Azure Active Directory principal for the resource.</span></span>
  - <span data-ttu-id="198e3-159">`[InfrastructureEncryption <InfrastructureEncryption?>]`: Status som visar om infrastrukturen för infrastruktur är aktive rad.</span><span class="sxs-lookup"><span data-stu-id="198e3-159">`[InfrastructureEncryption <InfrastructureEncryption?>]`: Status showing whether the server enabled infrastructure encryption.</span></span>
  - <span data-ttu-id="198e3-160">`[MasterServerId <String>]`: Huvud serverns ID för en replik Server.</span><span class="sxs-lookup"><span data-stu-id="198e3-160">`[MasterServerId <String>]`: The master server id of a replica server.</span></span>
  - <span data-ttu-id="198e3-161">`[MinimalTlsVersion <MinimalTlsVersionEnum?>]`: Påtvinga en minimal TLS-version för servern.</span><span class="sxs-lookup"><span data-stu-id="198e3-161">`[MinimalTlsVersion <MinimalTlsVersionEnum?>]`: Enforce a minimal Tls version for the server.</span></span>
  - <span data-ttu-id="198e3-162">`[PublicNetworkAccess <PublicNetworkAccessEnum?>]`: Oberoende nätverks åtkomst tillåts för den här servern.</span><span class="sxs-lookup"><span data-stu-id="198e3-162">`[PublicNetworkAccess <PublicNetworkAccessEnum?>]`: Whether or not public network access is allowed for this server.</span></span> <span data-ttu-id="198e3-163">Värdet är valfritt, men om det är skickat måste det vara aktiverat eller inaktiverat</span><span class="sxs-lookup"><span data-stu-id="198e3-163">Value is optional but if passed in, must be 'Enabled' or 'Disabled'</span></span>
  - <span data-ttu-id="198e3-164">`[ReplicaCapacity <Int32?>]`: Det högsta antalet repliker som en huvud server kan ha.</span><span class="sxs-lookup"><span data-stu-id="198e3-164">`[ReplicaCapacity <Int32?>]`: The maximum number of replicas that a master server can have.</span></span>
  - <span data-ttu-id="198e3-165">`[ReplicationRole <String>]`: Serverns replikeringsrelation.</span><span class="sxs-lookup"><span data-stu-id="198e3-165">`[ReplicationRole <String>]`: The replication role of the server.</span></span>
  - <span data-ttu-id="198e3-166">`[SkuCapacity <Int32?>]`: Skalan upp/ut-kapacitet som representerar serverns beräknade enheter.</span><span class="sxs-lookup"><span data-stu-id="198e3-166">`[SkuCapacity <Int32?>]`: The scale up/out capacity, representing server's compute units.</span></span>
  - <span data-ttu-id="198e3-167">`[SkuFamily <String>]`: Produkt familjen.</span><span class="sxs-lookup"><span data-stu-id="198e3-167">`[SkuFamily <String>]`: The family of hardware.</span></span>
  - <span data-ttu-id="198e3-168">`[SkuName <String>]`: Namnet på SKU: n, vanligt vis nivå + Family + cores, till exempel B_Gen4_1 GP_Gen5_8.</span><span class="sxs-lookup"><span data-stu-id="198e3-168">`[SkuName <String>]`: The name of the sku, typically, tier + family + cores, e.g. B_Gen4_1, GP_Gen5_8.</span></span>
  - <span data-ttu-id="198e3-169">`[SkuSize <String>]`: Storleks koden, som ska tolkas av resursen.</span><span class="sxs-lookup"><span data-stu-id="198e3-169">`[SkuSize <String>]`: The size code, to be interpreted by resource as appropriate.</span></span>
  - <span data-ttu-id="198e3-170">`[SkuTier <SkuTier?>]`: Nivån för den aktuella SKU: n, t. ex.</span><span class="sxs-lookup"><span data-stu-id="198e3-170">`[SkuTier <SkuTier?>]`: The tier of the particular SKU, e.g. Basic.</span></span>
  - <span data-ttu-id="198e3-171">`[SslEnforcement <SslEnforcementEnum?>]`: Aktivera SSL-tvång eller inte vid anslutning till server.</span><span class="sxs-lookup"><span data-stu-id="198e3-171">`[SslEnforcement <SslEnforcementEnum?>]`: Enable ssl enforcement or not when connect to server.</span></span>
  - <span data-ttu-id="198e3-172">`[StorageProfileBackupRetentionDay <Int32?>]`: Bevarande dagar för säkerhets kopior för servern.</span><span class="sxs-lookup"><span data-stu-id="198e3-172">`[StorageProfileBackupRetentionDay <Int32?>]`: Backup retention days for the server.</span></span>
  - <span data-ttu-id="198e3-173">`[StorageProfileGeoRedundantBackup <GeoRedundantBackup?>]`: Aktivera Geo-redundant eller ej för säkerhets kopiering av Server.</span><span class="sxs-lookup"><span data-stu-id="198e3-173">`[StorageProfileGeoRedundantBackup <GeoRedundantBackup?>]`: Enable Geo-redundant or not for server backup.</span></span>
  - <span data-ttu-id="198e3-174">`[StorageProfileStorageAutogrow <StorageAutogrow?>]`: Aktivera automatisk tillväxt av lagring.</span><span class="sxs-lookup"><span data-stu-id="198e3-174">`[StorageProfileStorageAutogrow <StorageAutogrow?>]`: Enable Storage Auto Grow.</span></span>
  - <span data-ttu-id="198e3-175">`[StorageProfileStorageMb <Int32?>]`: Högsta tillåtna lagrings utrymme för en server.</span><span class="sxs-lookup"><span data-stu-id="198e3-175">`[StorageProfileStorageMb <Int32?>]`: Max storage allowed for a server.</span></span>
  - <span data-ttu-id="198e3-176">`[UserVisibleState <ServerState?>]`: Ett tillstånd för en server som är synlig för användaren.</span><span class="sxs-lookup"><span data-stu-id="198e3-176">`[UserVisibleState <ServerState?>]`: A state of a server that is visible to user.</span></span>
  - <span data-ttu-id="198e3-177">`[Version <ServerVersion?>]`: Server version.</span><span class="sxs-lookup"><span data-stu-id="198e3-177">`[Version <ServerVersion?>]`: Server version.</span></span>

## <span data-ttu-id="198e3-178">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="198e3-178">RELATED LINKS</span></span>

