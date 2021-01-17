---
external help file: ''
Module Name: Az.MariaDb
online version: https://docs.microsoft.com/en-us/powershell/module/az.mariadb/get-azmariadbconnectionstring
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/Get-AzMariaDbConnectionString.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/Get-AzMariaDbConnectionString.md
ms.openlocfilehash: 1a6e96a8b8e030628655bdf95c58b726341dd2cc
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98388521"
---
# <span data-ttu-id="c7277-101">Get-AzMariaDbConnectionString</span><span class="sxs-lookup"><span data-stu-id="c7277-101">Get-AzMariaDbConnectionString</span></span>

## <span data-ttu-id="c7277-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="c7277-102">SYNOPSIS</span></span>
<span data-ttu-id="c7277-103">Få en anslutnings sträng för en MariaDB under ett givet ramverk.</span><span class="sxs-lookup"><span data-stu-id="c7277-103">Get connection string of a MariaDB under a given framework.</span></span>

## <span data-ttu-id="c7277-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="c7277-104">SYNTAX</span></span>

### <span data-ttu-id="c7277-105">Server namn (standard)</span><span class="sxs-lookup"><span data-stu-id="c7277-105">ServerName (Default)</span></span>
```
Get-AzMariaDbConnectionString -Client <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="c7277-106">ServerObject</span><span class="sxs-lookup"><span data-stu-id="c7277-106">ServerObject</span></span>
```
Get-AzMariaDbConnectionString -Client <String> -InputObject <IServer> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="c7277-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="c7277-107">DESCRIPTION</span></span>
<span data-ttu-id="c7277-108">Få en anslutnings sträng för en MariaDB under ett givet ramverk.</span><span class="sxs-lookup"><span data-stu-id="c7277-108">Get connection string of a MariaDB under a given framework.</span></span>

## <span data-ttu-id="c7277-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="c7277-109">EXAMPLES</span></span>

### <span data-ttu-id="c7277-110">Exempel 1: skaffa en anslutnings sträng för MariaDB</span><span class="sxs-lookup"><span data-stu-id="c7277-110">Example 1: Get a connection string of MariaDB</span></span>
```powershell
PS C:\> Get-AzMariaDbConnectionString -ServerName mariadb-asd-01 -ResourceGroupName mariadb-test-qu5ov0 -Client ADO.NET

Server=mariadb-asd-01.mariadb.database.azure.com; Port=3306; Database={your_database}; Uid=adminuser@mariadb-asd-01; Pwd={your_password}; SslMode=Preferred;
```

<span data-ttu-id="c7277-111">Det här kommandot får en anslutnings sträng med MariaDB.</span><span class="sxs-lookup"><span data-stu-id="c7277-111">This command gets a connection string of MariaDB.</span></span>

### <span data-ttu-id="c7277-112">Exempel 2: skaffa en anslutnings sträng för MariaDB</span><span class="sxs-lookup"><span data-stu-id="c7277-112">Example 2: Get a connection string of MariaDB</span></span>
```powershell
PS C:\> Get-AzMariaDbServer -Name mariadb-gp-t03 -ResourceGroupName lucas-manual-test | Get-AzMariaDbConnectionString -Client PHP

$con=mysqli_init();mysqli_ssl_set($con, NULL, NULL, {ca-cert filename}, NULL, NULL); mysqli_real_connect($con, "mariadb-gp-t03.mariadb.database.azure.com", "adminuser@mariadb-gp-t03", {your_password}, {your_database}, 3306);
```

<span data-ttu-id="c7277-113">Det här kommandot får en anslutnings sträng med MariaDB.</span><span class="sxs-lookup"><span data-stu-id="c7277-113">This command gets a connection string of MariaDB.</span></span>

## <span data-ttu-id="c7277-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="c7277-114">PARAMETERS</span></span>

### <span data-ttu-id="c7277-115">-Klient</span><span class="sxs-lookup"><span data-stu-id="c7277-115">-Client</span></span>
<span data-ttu-id="c7277-116">Anslut klient typ</span><span class="sxs-lookup"><span data-stu-id="c7277-116">Connect client type</span></span>

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

### <span data-ttu-id="c7277-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c7277-117">-DefaultProfile</span></span>
<span data-ttu-id="c7277-118">regionen DefaultParameters autentiseringsuppgifterna, kontot, innehavaren och prenumerationen som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="c7277-118">region DefaultParameters The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c7277-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c7277-119">-InputObject</span></span>
<span data-ttu-id="c7277-120">Identitets parameter för att konstruera, se avsnittet anteckningar för INPUTOBJECT-egenskaper och skapa en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="c7277-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.Api20180601Preview.IServer
Parameter Sets: ServerObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c7277-121">-Namn</span><span class="sxs-lookup"><span data-stu-id="c7277-121">-Name</span></span>
<span data-ttu-id="c7277-122">Namnet på servern.</span><span class="sxs-lookup"><span data-stu-id="c7277-122">The name of the server.</span></span>

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

### <span data-ttu-id="c7277-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c7277-123">-ResourceGroupName</span></span>
<span data-ttu-id="c7277-124">Namnet på resurs gruppen som innehåller resursen.</span><span class="sxs-lookup"><span data-stu-id="c7277-124">The name of the resource group that contains the resource.</span></span>

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

### <span data-ttu-id="c7277-125">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="c7277-125">-SubscriptionId</span></span>
<span data-ttu-id="c7277-126">Prenumerations-ID är en del av URI: n för varje service samtal</span><span class="sxs-lookup"><span data-stu-id="c7277-126">The subscription ID is part of the URI for every service call</span></span>

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

### <span data-ttu-id="c7277-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c7277-127">CommonParameters</span></span>
<span data-ttu-id="c7277-128">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c7277-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c7277-129">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c7277-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c7277-130">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="c7277-130">INPUTS</span></span>

### <span data-ttu-id="c7277-131">Microsoft. Azure. PowerShell. cmdletar. MariaDb. Models. Api20180601Preview. IServer</span><span class="sxs-lookup"><span data-stu-id="c7277-131">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.Api20180601Preview.IServer</span></span>

## <span data-ttu-id="c7277-132">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="c7277-132">OUTPUTS</span></span>

### <span data-ttu-id="c7277-133">System. String</span><span class="sxs-lookup"><span data-stu-id="c7277-133">System.String</span></span>

## <span data-ttu-id="c7277-134">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="c7277-134">NOTES</span></span>

<span data-ttu-id="c7277-135">ALIAS</span><span class="sxs-lookup"><span data-stu-id="c7277-135">ALIASES</span></span>

<span data-ttu-id="c7277-136">KOMPLEXA PARAMETER EGENSKAPER</span><span class="sxs-lookup"><span data-stu-id="c7277-136">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="c7277-137">Skapa en hash-tabell som innehåller lämpliga egenskaper för att lägga till de parametrar som beskrivs nedan.</span><span class="sxs-lookup"><span data-stu-id="c7277-137">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="c7277-138">Om du vill ha information om hash-tabeller kör Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="c7277-138">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="c7277-139">INPUTOBJECT <IServer> : identitets parameter</span><span class="sxs-lookup"><span data-stu-id="c7277-139">INPUTOBJECT <IServer>: Identity Parameter</span></span>
  - <span data-ttu-id="c7277-140">`Location <String>`: Platsen som resursen finns i.</span><span class="sxs-lookup"><span data-stu-id="c7277-140">`Location <String>`: The location the resource resides in.</span></span>
  - <span data-ttu-id="c7277-141">`[Tag <ITrackedResourceTags>]`: Programspecifika metadata i form av par med nyckelvärdena.</span><span class="sxs-lookup"><span data-stu-id="c7277-141">`[Tag <ITrackedResourceTags>]`: Application-specific metadata in the form of key-value pairs.</span></span>
    - <span data-ttu-id="c7277-142">`[(Any) <String>]`: Detta indikerar att en egenskap kan läggas till i det här objektet.</span><span class="sxs-lookup"><span data-stu-id="c7277-142">`[(Any) <String>]`: This indicates any property can be added to this object.</span></span>
  - <span data-ttu-id="c7277-143">`[AdministratorLogin <String>]`: Administratörens inloggnings namn för en server.</span><span class="sxs-lookup"><span data-stu-id="c7277-143">`[AdministratorLogin <String>]`: The administrator's login name of a server.</span></span> <span data-ttu-id="c7277-144">Kan bara anges när servern skapas (och krävs för att skapa).</span><span class="sxs-lookup"><span data-stu-id="c7277-144">Can only be specified when the server is being created (and is required for creation).</span></span>
  - <span data-ttu-id="c7277-145">`[EarliestRestoreDate <DateTime?>]`: Tidig skapelse tid för återställnings punkt (ISO8601-format)</span><span class="sxs-lookup"><span data-stu-id="c7277-145">`[EarliestRestoreDate <DateTime?>]`: Earliest restore point creation time (ISO8601 format)</span></span>
  - <span data-ttu-id="c7277-146">`[FullyQualifiedDomainName <String>]`: Serverns fullkvalificerade domän namn.</span><span class="sxs-lookup"><span data-stu-id="c7277-146">`[FullyQualifiedDomainName <String>]`: The fully qualified domain name of a server.</span></span>
  - <span data-ttu-id="c7277-147">`[IdentityType <IdentityType?>]`: Identitets typen.</span><span class="sxs-lookup"><span data-stu-id="c7277-147">`[IdentityType <IdentityType?>]`: The identity type.</span></span> <span data-ttu-id="c7277-148">Ställ in detta på ' SystemAssigned ' för att automatiskt skapa och tilldela en Azure Active Directory-Huvudplats för resursen.</span><span class="sxs-lookup"><span data-stu-id="c7277-148">Set this to 'SystemAssigned' in order to automatically create and assign an Azure Active Directory principal for the resource.</span></span>
  - <span data-ttu-id="c7277-149">`[MasterServerId <String>]`: Huvud serverns ID för en replik Server.</span><span class="sxs-lookup"><span data-stu-id="c7277-149">`[MasterServerId <String>]`: The master server id of a replica server.</span></span>
  - <span data-ttu-id="c7277-150">`[ReplicaCapacity <Int32?>]`: Det högsta antalet repliker som en huvud server kan ha.</span><span class="sxs-lookup"><span data-stu-id="c7277-150">`[ReplicaCapacity <Int32?>]`: The maximum number of replicas that a master server can have.</span></span>
  - <span data-ttu-id="c7277-151">`[ReplicationRole <String>]`: Serverns replikeringsrelation.</span><span class="sxs-lookup"><span data-stu-id="c7277-151">`[ReplicationRole <String>]`: The replication role of the server.</span></span>
  - <span data-ttu-id="c7277-152">`[SkuCapacity <Int32?>]`: Skalan upp/ut-kapacitet som representerar serverns beräknade enheter.</span><span class="sxs-lookup"><span data-stu-id="c7277-152">`[SkuCapacity <Int32?>]`: The scale up/out capacity, representing server's compute units.</span></span>
  - <span data-ttu-id="c7277-153">`[SkuFamily <String>]`: Produkt familjen.</span><span class="sxs-lookup"><span data-stu-id="c7277-153">`[SkuFamily <String>]`: The family of hardware.</span></span>
  - <span data-ttu-id="c7277-154">`[SkuName <String>]`: Namnet på SKU: n, vanligt vis nivå + Family + cores, till exempel B_Gen4_1 GP_Gen5_8.</span><span class="sxs-lookup"><span data-stu-id="c7277-154">`[SkuName <String>]`: The name of the sku, typically, tier + family + cores, e.g. B_Gen4_1, GP_Gen5_8.</span></span>
  - <span data-ttu-id="c7277-155">`[SkuSize <String>]`: Storleks koden, som ska tolkas av resursen.</span><span class="sxs-lookup"><span data-stu-id="c7277-155">`[SkuSize <String>]`: The size code, to be interpreted by resource as appropriate.</span></span>
  - <span data-ttu-id="c7277-156">`[SkuTier <SkuTier?>]`: Nivån för den aktuella SKU: n, t. ex.</span><span class="sxs-lookup"><span data-stu-id="c7277-156">`[SkuTier <SkuTier?>]`: The tier of the particular SKU, e.g. Basic.</span></span>
  - <span data-ttu-id="c7277-157">`[SslEnforcement <SslEnforcementEnum?>]`: Aktivera SSL-tvång eller inte vid anslutning till server.</span><span class="sxs-lookup"><span data-stu-id="c7277-157">`[SslEnforcement <SslEnforcementEnum?>]`: Enable ssl enforcement or not when connect to server.</span></span>
  - <span data-ttu-id="c7277-158">`[StorageProfileBackupRetentionDay <Int32?>]`: Bevarande dagar för säkerhets kopior för servern.</span><span class="sxs-lookup"><span data-stu-id="c7277-158">`[StorageProfileBackupRetentionDay <Int32?>]`: Backup retention days for the server.</span></span>
  - <span data-ttu-id="c7277-159">`[StorageProfileGeoRedundantBackup <GeoRedundantBackup?>]`: Aktivera Geo-redundant eller ej för säkerhets kopiering av Server.</span><span class="sxs-lookup"><span data-stu-id="c7277-159">`[StorageProfileGeoRedundantBackup <GeoRedundantBackup?>]`: Enable Geo-redundant or not for server backup.</span></span>
  - <span data-ttu-id="c7277-160">`[StorageProfileStorageAutogrow <StorageAutogrow?>]`: Aktivera automatisk tillväxt av lagring.</span><span class="sxs-lookup"><span data-stu-id="c7277-160">`[StorageProfileStorageAutogrow <StorageAutogrow?>]`: Enable Storage Auto Grow.</span></span>
  - <span data-ttu-id="c7277-161">`[StorageProfileStorageMb <Int32?>]`: Högsta tillåtna lagrings utrymme för en server.</span><span class="sxs-lookup"><span data-stu-id="c7277-161">`[StorageProfileStorageMb <Int32?>]`: Max storage allowed for a server.</span></span>
  - <span data-ttu-id="c7277-162">`[UserVisibleState <ServerState?>]`: Ett tillstånd för en server som är synlig för användaren.</span><span class="sxs-lookup"><span data-stu-id="c7277-162">`[UserVisibleState <ServerState?>]`: A state of a server that is visible to user.</span></span>
  - <span data-ttu-id="c7277-163">`[Version <ServerVersion?>]`: Server version.</span><span class="sxs-lookup"><span data-stu-id="c7277-163">`[Version <ServerVersion?>]`: Server version.</span></span>

## <span data-ttu-id="c7277-164">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="c7277-164">RELATED LINKS</span></span>

