---
external help file: ''
Module Name: Az.MySql
online version: https://docs.microsoft.com/en-us/powershell/module/az.mysql/get-azmysqlconnectionstring
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Get-AzMySqlConnectionString.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Get-AzMySqlConnectionString.md
ms.openlocfilehash: d6dda5e26603c2276210e4bf00b8b9c040568f12
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98522895"
---
# <span data-ttu-id="49721-101">Get-AzMySqlConnectionString</span><span class="sxs-lookup"><span data-stu-id="49721-101">Get-AzMySqlConnectionString</span></span>

## <span data-ttu-id="49721-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="49721-102">SYNOPSIS</span></span>
<span data-ttu-id="49721-103">Hämta anslutnings strängen enligt klient anslutnings leverantören.</span><span class="sxs-lookup"><span data-stu-id="49721-103">Get the connection string according to client connection provider.</span></span>

## <span data-ttu-id="49721-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="49721-104">SYNTAX</span></span>

### <span data-ttu-id="49721-105">Skaffa (standard)</span><span class="sxs-lookup"><span data-stu-id="49721-105">Get (Default)</span></span>
```
Get-AzMySqlConnectionString -Client <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="49721-106">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="49721-106">GetViaIdentity</span></span>
```
Get-AzMySqlConnectionString -Client <String> -InputObject <IServer> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="49721-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="49721-107">DESCRIPTION</span></span>
<span data-ttu-id="49721-108">Hämta anslutnings strängen enligt klient anslutnings leverantören.</span><span class="sxs-lookup"><span data-stu-id="49721-108">Get the connection string according to client connection provider.</span></span>

## <span data-ttu-id="49721-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="49721-109">EXAMPLES</span></span>

### <span data-ttu-id="49721-110">Exempel 1: skaffa Server anslutnings sträng för MySql via resurs grupp och Server namn</span><span class="sxs-lookup"><span data-stu-id="49721-110">Example 1: Get MySql server connection string by resource group and server name</span></span>
```powershell
PS C:\> Get-AzMySqlConnectionString -Client ADO.NET -Name mysql-test -ResourceGroupName PowershellMySqlTest

Server=mysql-test.mysql.database.azure.com; Port=3306; Database={your_database}; Uid=mysql_test@mysql-test; Pwd={your_password};
```

<span data-ttu-id="49721-111">Denna cmdlet får MySql Server anslutnings sträng efter resurs grupp och Server namn.</span><span class="sxs-lookup"><span data-stu-id="49721-111">This cmdlet gets MySql server connection string by resource group and server name.</span></span>

### <span data-ttu-id="49721-112">Exempel 2: skaffa Server anslutnings sträng för MySql efter identitet</span><span class="sxs-lookup"><span data-stu-id="49721-112">Example 2: Get MySql server connection string by identity</span></span>
```powershell
PS C:\> Get-AzMySqlServer -ResourceGroupName PowershellMySqlTest -ServerName mysql-test | Get-AzMySqlConnectionString -Client PHP

$con=mysqli_init(); mysqli_real_connect($con, "mysql-test.mysql.database.azure.com", "mysql_test@mysql-test", {your_password}, {your_database}, 3306);
```

<span data-ttu-id="49721-113">Denna cmdlet får MySql Server anslutnings sträng efter identitet.</span><span class="sxs-lookup"><span data-stu-id="49721-113">This cmdlet gets MySql server connection string by identity.</span></span>

## <span data-ttu-id="49721-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="49721-114">PARAMETERS</span></span>

### <span data-ttu-id="49721-115">-Klient</span><span class="sxs-lookup"><span data-stu-id="49721-115">-Client</span></span>
<span data-ttu-id="49721-116">Klient anslutnings leverantör.</span><span class="sxs-lookup"><span data-stu-id="49721-116">Client connection provider.</span></span>

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

### <span data-ttu-id="49721-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="49721-117">-DefaultProfile</span></span>
<span data-ttu-id="49721-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="49721-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="49721-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="49721-119">-InputObject</span></span>
<span data-ttu-id="49721-120">Käll Server objekt för att skapa replik från.</span><span class="sxs-lookup"><span data-stu-id="49721-120">The source server object to create replica from.</span></span>
<span data-ttu-id="49721-121">För att konstruera kan du läsa avsnittet anteckningar för INPUTOBJECT-egenskaper och skapa en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="49721-121">To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20171201.IServer
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="49721-122">-Namn</span><span class="sxs-lookup"><span data-stu-id="49721-122">-Name</span></span>
<span data-ttu-id="49721-123">Namnet på servern.</span><span class="sxs-lookup"><span data-stu-id="49721-123">The name of the server.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: ServerName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="49721-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="49721-124">-ResourceGroupName</span></span>
<span data-ttu-id="49721-125">Namnet på resurs gruppen som innehåller resursen kan du hämta det här värdet från Azure Resource Manager API eller portalen.</span><span class="sxs-lookup"><span data-stu-id="49721-125">The name of the resource group that contains the resource, You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="49721-126">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="49721-126">-SubscriptionId</span></span>
<span data-ttu-id="49721-127">Det prenumerations-ID som identifierar en Azure-prenumeration.</span><span class="sxs-lookup"><span data-stu-id="49721-127">The subscription ID that identifies an Azure subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="49721-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="49721-128">CommonParameters</span></span>
<span data-ttu-id="49721-129">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="49721-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="49721-130">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="49721-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="49721-131">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="49721-131">INPUTS</span></span>

### <span data-ttu-id="49721-132">Microsoft. Azure. PowerShell. cmdletar. MySql. Models. Api20171201. IServer</span><span class="sxs-lookup"><span data-stu-id="49721-132">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20171201.IServer</span></span>

## <span data-ttu-id="49721-133">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="49721-133">OUTPUTS</span></span>

### <span data-ttu-id="49721-134">System. String</span><span class="sxs-lookup"><span data-stu-id="49721-134">System.String</span></span>

## <span data-ttu-id="49721-135">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="49721-135">NOTES</span></span>

<span data-ttu-id="49721-136">ALIAS</span><span class="sxs-lookup"><span data-stu-id="49721-136">ALIASES</span></span>

<span data-ttu-id="49721-137">KOMPLEXA PARAMETER EGENSKAPER</span><span class="sxs-lookup"><span data-stu-id="49721-137">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="49721-138">Skapa en hash-tabell som innehåller lämpliga egenskaper för att lägga till de parametrar som beskrivs nedan.</span><span class="sxs-lookup"><span data-stu-id="49721-138">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="49721-139">Om du vill ha information om hash-tabeller kör Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="49721-139">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="49721-140">INPUTOBJECT <IServer> : käll Server objekt för att skapa replik från.</span><span class="sxs-lookup"><span data-stu-id="49721-140">INPUTOBJECT <IServer>: The source server object to create replica from.</span></span>
  - <span data-ttu-id="49721-141">`Location <String>`: Den Geo-plats där resursen bor</span><span class="sxs-lookup"><span data-stu-id="49721-141">`Location <String>`: The geo-location where the resource lives</span></span>
  - <span data-ttu-id="49721-142">`SkuName <String>`: Namnet på SKU: n, vanligt vis nivå + Family + cores, till exempel B_Gen4_1 GP_Gen5_8.</span><span class="sxs-lookup"><span data-stu-id="49721-142">`SkuName <String>`: The name of the sku, typically, tier + family + cores, e.g. B_Gen4_1, GP_Gen5_8.</span></span>
  - <span data-ttu-id="49721-143">`[Tag <ITrackedResourceTags>]`: Resursfiler.</span><span class="sxs-lookup"><span data-stu-id="49721-143">`[Tag <ITrackedResourceTags>]`: Resource tags.</span></span>
    - <span data-ttu-id="49721-144">`[(Any) <String>]`: Detta indikerar att en egenskap kan läggas till i det här objektet.</span><span class="sxs-lookup"><span data-stu-id="49721-144">`[(Any) <String>]`: This indicates any property can be added to this object.</span></span>
  - <span data-ttu-id="49721-145">`[AdministratorLogin <String>]`: Administratörens inloggnings namn för en server.</span><span class="sxs-lookup"><span data-stu-id="49721-145">`[AdministratorLogin <String>]`: The administrator's login name of a server.</span></span> <span data-ttu-id="49721-146">Kan bara anges när servern skapas (och krävs för att skapa).</span><span class="sxs-lookup"><span data-stu-id="49721-146">Can only be specified when the server is being created (and is required for creation).</span></span>
  - <span data-ttu-id="49721-147">`[EarliestRestoreDate <DateTime?>]`: Tidig skapelse tid för återställnings punkt (ISO8601-format)</span><span class="sxs-lookup"><span data-stu-id="49721-147">`[EarliestRestoreDate <DateTime?>]`: Earliest restore point creation time (ISO8601 format)</span></span>
  - <span data-ttu-id="49721-148">`[FullyQualifiedDomainName <String>]`: Serverns fullkvalificerade domän namn.</span><span class="sxs-lookup"><span data-stu-id="49721-148">`[FullyQualifiedDomainName <String>]`: The fully qualified domain name of a server.</span></span>
  - <span data-ttu-id="49721-149">`[IdentityType <IdentityType?>]`: Identitets typen.</span><span class="sxs-lookup"><span data-stu-id="49721-149">`[IdentityType <IdentityType?>]`: The identity type.</span></span> <span data-ttu-id="49721-150">Ställ in detta på ' SystemAssigned ' för att automatiskt skapa och tilldela en Azure Active Directory-Huvudplats för resursen.</span><span class="sxs-lookup"><span data-stu-id="49721-150">Set this to 'SystemAssigned' in order to automatically create and assign an Azure Active Directory principal for the resource.</span></span>
  - <span data-ttu-id="49721-151">`[InfrastructureEncryption <InfrastructureEncryption?>]`: Status som visar om infrastrukturen för infrastruktur är aktive rad.</span><span class="sxs-lookup"><span data-stu-id="49721-151">`[InfrastructureEncryption <InfrastructureEncryption?>]`: Status showing whether the server enabled infrastructure encryption.</span></span>
  - <span data-ttu-id="49721-152">`[MasterServerId <String>]`: Huvud serverns ID för en replik Server.</span><span class="sxs-lookup"><span data-stu-id="49721-152">`[MasterServerId <String>]`: The master server id of a replica server.</span></span>
  - <span data-ttu-id="49721-153">`[MinimalTlsVersion <MinimalTlsVersionEnum?>]`: Påtvinga en minimal TLS-version för servern.</span><span class="sxs-lookup"><span data-stu-id="49721-153">`[MinimalTlsVersion <MinimalTlsVersionEnum?>]`: Enforce a minimal Tls version for the server.</span></span>
  - <span data-ttu-id="49721-154">`[PublicNetworkAccess <PublicNetworkAccessEnum?>]`: Oberoende nätverks åtkomst tillåts för den här servern.</span><span class="sxs-lookup"><span data-stu-id="49721-154">`[PublicNetworkAccess <PublicNetworkAccessEnum?>]`: Whether or not public network access is allowed for this server.</span></span> <span data-ttu-id="49721-155">Värdet är valfritt, men om det är skickat måste det vara aktiverat eller inaktiverat</span><span class="sxs-lookup"><span data-stu-id="49721-155">Value is optional but if passed in, must be 'Enabled' or 'Disabled'</span></span>
  - <span data-ttu-id="49721-156">`[ReplicaCapacity <Int32?>]`: Det högsta antalet repliker som en huvud server kan ha.</span><span class="sxs-lookup"><span data-stu-id="49721-156">`[ReplicaCapacity <Int32?>]`: The maximum number of replicas that a master server can have.</span></span>
  - <span data-ttu-id="49721-157">`[ReplicationRole <String>]`: Serverns replikeringsrelation.</span><span class="sxs-lookup"><span data-stu-id="49721-157">`[ReplicationRole <String>]`: The replication role of the server.</span></span>
  - <span data-ttu-id="49721-158">`[SkuCapacity <Int32?>]`: Skalan upp/ut-kapacitet som representerar serverns beräknade enheter.</span><span class="sxs-lookup"><span data-stu-id="49721-158">`[SkuCapacity <Int32?>]`: The scale up/out capacity, representing server's compute units.</span></span>
  - <span data-ttu-id="49721-159">`[SkuFamily <String>]`: Produkt familjen.</span><span class="sxs-lookup"><span data-stu-id="49721-159">`[SkuFamily <String>]`: The family of hardware.</span></span>
  - <span data-ttu-id="49721-160">`[SkuSize <String>]`: Storleks koden, som ska tolkas av resursen.</span><span class="sxs-lookup"><span data-stu-id="49721-160">`[SkuSize <String>]`: The size code, to be interpreted by resource as appropriate.</span></span>
  - <span data-ttu-id="49721-161">`[SkuTier <SkuTier?>]`: Nivån för den aktuella SKU: n, t. ex.</span><span class="sxs-lookup"><span data-stu-id="49721-161">`[SkuTier <SkuTier?>]`: The tier of the particular SKU, e.g. Basic.</span></span>
  - <span data-ttu-id="49721-162">`[SslEnforcement <SslEnforcementEnum?>]`: Aktivera SSL-tvång eller inte vid anslutning till server.</span><span class="sxs-lookup"><span data-stu-id="49721-162">`[SslEnforcement <SslEnforcementEnum?>]`: Enable ssl enforcement or not when connect to server.</span></span>
  - <span data-ttu-id="49721-163">`[StorageProfileBackupRetentionDay <Int32?>]`: Bevarande dagar för säkerhets kopior för servern.</span><span class="sxs-lookup"><span data-stu-id="49721-163">`[StorageProfileBackupRetentionDay <Int32?>]`: Backup retention days for the server.</span></span>
  - <span data-ttu-id="49721-164">`[StorageProfileGeoRedundantBackup <GeoRedundantBackup?>]`: Aktivera Geo-redundant eller ej för säkerhets kopiering av Server.</span><span class="sxs-lookup"><span data-stu-id="49721-164">`[StorageProfileGeoRedundantBackup <GeoRedundantBackup?>]`: Enable Geo-redundant or not for server backup.</span></span>
  - <span data-ttu-id="49721-165">`[StorageProfileStorageAutogrow <StorageAutogrow?>]`: Aktivera automatisk tillväxt av lagring.</span><span class="sxs-lookup"><span data-stu-id="49721-165">`[StorageProfileStorageAutogrow <StorageAutogrow?>]`: Enable Storage Auto Grow.</span></span>
  - <span data-ttu-id="49721-166">`[StorageProfileStorageMb <Int32?>]`: Högsta tillåtna lagrings utrymme för en server.</span><span class="sxs-lookup"><span data-stu-id="49721-166">`[StorageProfileStorageMb <Int32?>]`: Max storage allowed for a server.</span></span>
  - <span data-ttu-id="49721-167">`[UserVisibleState <ServerState?>]`: Ett tillstånd för en server som är synlig för användaren.</span><span class="sxs-lookup"><span data-stu-id="49721-167">`[UserVisibleState <ServerState?>]`: A state of a server that is visible to user.</span></span>
  - <span data-ttu-id="49721-168">`[Version <ServerVersion?>]`: Server version.</span><span class="sxs-lookup"><span data-stu-id="49721-168">`[Version <ServerVersion?>]`: Server version.</span></span>

## <span data-ttu-id="49721-169">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="49721-169">RELATED LINKS</span></span>

