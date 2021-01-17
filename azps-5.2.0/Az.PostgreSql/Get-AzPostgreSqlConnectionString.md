---
external help file: ''
Module Name: Az.PostgreSql
online version: https://docs.microsoft.com/en-us/powershell/module/az.postgresql/get-azpostgresqlconnectionstring
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Get-AzPostgreSqlConnectionString.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Get-AzPostgreSqlConnectionString.md
ms.openlocfilehash: 8df35a38889e2c91bd74625ae916fd10739d9db1
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98398179"
---
# <span data-ttu-id="cceb1-101">Get-AzPostgreSqlConnectionString</span><span class="sxs-lookup"><span data-stu-id="cceb1-101">Get-AzPostgreSqlConnectionString</span></span>

## <span data-ttu-id="cceb1-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="cceb1-102">SYNOPSIS</span></span>
<span data-ttu-id="cceb1-103">Hämta anslutnings strängen enligt klient anslutnings leverantören.</span><span class="sxs-lookup"><span data-stu-id="cceb1-103">Get the connection string according to client connection provider.</span></span>

## <span data-ttu-id="cceb1-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="cceb1-104">SYNTAX</span></span>

### <span data-ttu-id="cceb1-105">Skaffa (standard)</span><span class="sxs-lookup"><span data-stu-id="cceb1-105">Get (Default)</span></span>
```
Get-AzPostgreSqlConnectionString -Client <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="cceb1-106">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="cceb1-106">GetViaIdentity</span></span>
```
Get-AzPostgreSqlConnectionString -Client <String> -InputObject <IServer> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="cceb1-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="cceb1-107">DESCRIPTION</span></span>
<span data-ttu-id="cceb1-108">Hämta anslutnings strängen enligt klient anslutnings leverantören.</span><span class="sxs-lookup"><span data-stu-id="cceb1-108">Get the connection string according to client connection provider.</span></span>

## <span data-ttu-id="cceb1-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="cceb1-109">EXAMPLES</span></span>

### <span data-ttu-id="cceb1-110">Exempel 1: skaffa PostgreSql Server anslutnings sträng efter resurs grupp och Server namn</span><span class="sxs-lookup"><span data-stu-id="cceb1-110">Example 1: Get PostgreSql server connection string by resource group and server name</span></span>
```powershell
PS C:\> Get-AzPostgreSqlConnectionString -Client ADO.NET -Name PostgreSqlTestServer -ResourceGroupName PostgreSqlTestRG

Server=postgresqltestserver.postgres.database.azure.com;Database={your_database};Port=5432;User Id=pwsh@postgresqltestserver;Password={your_password};Ssl Mode=Require;
```

<span data-ttu-id="cceb1-111">Denna cmdlet hämtar PostgreSql för Server anslutningar efter resurs grupp och Server namn.</span><span class="sxs-lookup"><span data-stu-id="cceb1-111">This cmdlet gets PostgreSql server connection string by resource group and server name.</span></span>

### <span data-ttu-id="cceb1-112">Exempel 2: Hämta PostgreSql Server anslutnings sträng efter identitet</span><span class="sxs-lookup"><span data-stu-id="cceb1-112">Example 2: Get PostgreSql server connection string by identity</span></span>
```powershell
PS C:\> Get-AzPostgreSqlServer -ResourceGroupName PostgreSqlTestRG -ServerName PostgreSqlTestServer | Get-AzPostgreSqlConnectionString -Client PHP

host=postgresqltestserver.postgres.database.azure.com port=5432 dbname={your_database} user=pwsh@postgresqltestserver password={your_password} sslmode=require
```

<span data-ttu-id="cceb1-113">Denna cmdlet får PostgreSql Server anslutnings sträng efter identitet.</span><span class="sxs-lookup"><span data-stu-id="cceb1-113">This cmdlet gets PostgreSql server connection string by identity.</span></span>

## <span data-ttu-id="cceb1-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="cceb1-114">PARAMETERS</span></span>

### <span data-ttu-id="cceb1-115">-Klient</span><span class="sxs-lookup"><span data-stu-id="cceb1-115">-Client</span></span>
<span data-ttu-id="cceb1-116">Klient anslutnings leverantör.</span><span class="sxs-lookup"><span data-stu-id="cceb1-116">Client connection provider.</span></span>

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

### <span data-ttu-id="cceb1-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cceb1-117">-DefaultProfile</span></span>
<span data-ttu-id="cceb1-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="cceb1-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cceb1-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="cceb1-119">-InputObject</span></span>
<span data-ttu-id="cceb1-120">Käll Server objekt för att skapa replik från.</span><span class="sxs-lookup"><span data-stu-id="cceb1-120">The source server object to create replica from.</span></span>
<span data-ttu-id="cceb1-121">För att konstruera kan du läsa avsnittet anteckningar för INPUTOBJECT-egenskaper och skapa en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="cceb1-121">To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.Api20171201.IServer
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="cceb1-122">-Namn</span><span class="sxs-lookup"><span data-stu-id="cceb1-122">-Name</span></span>
<span data-ttu-id="cceb1-123">Namnet på servern.</span><span class="sxs-lookup"><span data-stu-id="cceb1-123">The name of the server.</span></span>

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

### <span data-ttu-id="cceb1-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cceb1-124">-ResourceGroupName</span></span>
<span data-ttu-id="cceb1-125">Namnet på resurs gruppen som innehåller resursen kan du hämta det här värdet från Azure Resource Manager API eller portalen.</span><span class="sxs-lookup"><span data-stu-id="cceb1-125">The name of the resource group that contains the resource, You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="cceb1-126">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="cceb1-126">-SubscriptionId</span></span>
<span data-ttu-id="cceb1-127">Det prenumerations-ID som identifierar en Azure-prenumeration.</span><span class="sxs-lookup"><span data-stu-id="cceb1-127">The subscription ID that identifies an Azure subscription.</span></span>

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

### <span data-ttu-id="cceb1-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cceb1-128">CommonParameters</span></span>
<span data-ttu-id="cceb1-129">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cceb1-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cceb1-130">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="cceb1-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cceb1-131">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="cceb1-131">INPUTS</span></span>

### <span data-ttu-id="cceb1-132">Microsoft. Azure. PowerShell. cmdletar. PostgreSql. Models. Api20171201. IServer</span><span class="sxs-lookup"><span data-stu-id="cceb1-132">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.Api20171201.IServer</span></span>

## <span data-ttu-id="cceb1-133">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="cceb1-133">OUTPUTS</span></span>

### <span data-ttu-id="cceb1-134">System. String</span><span class="sxs-lookup"><span data-stu-id="cceb1-134">System.String</span></span>

## <span data-ttu-id="cceb1-135">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="cceb1-135">NOTES</span></span>

<span data-ttu-id="cceb1-136">ALIAS</span><span class="sxs-lookup"><span data-stu-id="cceb1-136">ALIASES</span></span>

<span data-ttu-id="cceb1-137">KOMPLEXA PARAMETER EGENSKAPER</span><span class="sxs-lookup"><span data-stu-id="cceb1-137">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="cceb1-138">Skapa en hash-tabell som innehåller lämpliga egenskaper för att lägga till de parametrar som beskrivs nedan.</span><span class="sxs-lookup"><span data-stu-id="cceb1-138">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="cceb1-139">Om du vill ha information om hash-tabeller kör Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="cceb1-139">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="cceb1-140">INPUTOBJECT <IServer> : käll Server objekt för att skapa replik från.</span><span class="sxs-lookup"><span data-stu-id="cceb1-140">INPUTOBJECT <IServer>: The source server object to create replica from.</span></span>
  - <span data-ttu-id="cceb1-141">`Location <String>`: Platsen som resursen finns i.</span><span class="sxs-lookup"><span data-stu-id="cceb1-141">`Location <String>`: The location the resource resides in.</span></span>
  - <span data-ttu-id="cceb1-142">`[Tag <ITrackedResourceTags>]`: Programspecifika metadata i form av par med nyckelvärdena.</span><span class="sxs-lookup"><span data-stu-id="cceb1-142">`[Tag <ITrackedResourceTags>]`: Application-specific metadata in the form of key-value pairs.</span></span>
    - <span data-ttu-id="cceb1-143">`[(Any) <String>]`: Detta indikerar att en egenskap kan läggas till i det här objektet.</span><span class="sxs-lookup"><span data-stu-id="cceb1-143">`[(Any) <String>]`: This indicates any property can be added to this object.</span></span>
  - <span data-ttu-id="cceb1-144">`[AdministratorLogin <String>]`: Administratörens inloggnings namn för en server.</span><span class="sxs-lookup"><span data-stu-id="cceb1-144">`[AdministratorLogin <String>]`: The administrator's login name of a server.</span></span> <span data-ttu-id="cceb1-145">Kan bara anges när servern skapas (och krävs för att skapa).</span><span class="sxs-lookup"><span data-stu-id="cceb1-145">Can only be specified when the server is being created (and is required for creation).</span></span>
  - <span data-ttu-id="cceb1-146">`[EarliestRestoreDate <DateTime?>]`: Tidig skapelse tid för återställnings punkt (ISO8601-format)</span><span class="sxs-lookup"><span data-stu-id="cceb1-146">`[EarliestRestoreDate <DateTime?>]`: Earliest restore point creation time (ISO8601 format)</span></span>
  - <span data-ttu-id="cceb1-147">`[FullyQualifiedDomainName <String>]`: Serverns fullkvalificerade domän namn.</span><span class="sxs-lookup"><span data-stu-id="cceb1-147">`[FullyQualifiedDomainName <String>]`: The fully qualified domain name of a server.</span></span>
  - <span data-ttu-id="cceb1-148">`[IdentityType <IdentityType?>]`: Identitets typen.</span><span class="sxs-lookup"><span data-stu-id="cceb1-148">`[IdentityType <IdentityType?>]`: The identity type.</span></span> <span data-ttu-id="cceb1-149">Ställ in detta på ' SystemAssigned ' för att automatiskt skapa och tilldela en Azure Active Directory-Huvudplats för resursen.</span><span class="sxs-lookup"><span data-stu-id="cceb1-149">Set this to 'SystemAssigned' in order to automatically create and assign an Azure Active Directory principal for the resource.</span></span>
  - <span data-ttu-id="cceb1-150">`[InfrastructureEncryption <InfrastructureEncryption?>]`: Status som visar om infrastrukturen för infrastruktur är aktive rad.</span><span class="sxs-lookup"><span data-stu-id="cceb1-150">`[InfrastructureEncryption <InfrastructureEncryption?>]`: Status showing whether the server enabled infrastructure encryption.</span></span>
  - <span data-ttu-id="cceb1-151">`[MasterServerId <String>]`: Huvud serverns ID för en replik Server.</span><span class="sxs-lookup"><span data-stu-id="cceb1-151">`[MasterServerId <String>]`: The master server id of a replica server.</span></span>
  - <span data-ttu-id="cceb1-152">`[MinimalTlsVersion <MinimalTlsVersionEnum?>]`: Påtvinga en minimal TLS-version för servern.</span><span class="sxs-lookup"><span data-stu-id="cceb1-152">`[MinimalTlsVersion <MinimalTlsVersionEnum?>]`: Enforce a minimal Tls version for the server.</span></span>
  - <span data-ttu-id="cceb1-153">`[PublicNetworkAccess <PublicNetworkAccessEnum?>]`: Oberoende nätverks åtkomst tillåts för den här servern.</span><span class="sxs-lookup"><span data-stu-id="cceb1-153">`[PublicNetworkAccess <PublicNetworkAccessEnum?>]`: Whether or not public network access is allowed for this server.</span></span> <span data-ttu-id="cceb1-154">Värdet är valfritt, men om det är skickat måste det vara aktiverat eller inaktiverat</span><span class="sxs-lookup"><span data-stu-id="cceb1-154">Value is optional but if passed in, must be 'Enabled' or 'Disabled'</span></span>
  - <span data-ttu-id="cceb1-155">`[ReplicaCapacity <Int32?>]`: Det högsta antalet repliker som en huvud server kan ha.</span><span class="sxs-lookup"><span data-stu-id="cceb1-155">`[ReplicaCapacity <Int32?>]`: The maximum number of replicas that a master server can have.</span></span>
  - <span data-ttu-id="cceb1-156">`[ReplicationRole <String>]`: Serverns replikeringsrelation.</span><span class="sxs-lookup"><span data-stu-id="cceb1-156">`[ReplicationRole <String>]`: The replication role of the server.</span></span>
  - <span data-ttu-id="cceb1-157">`[SkuCapacity <Int32?>]`: Skalan upp/ut-kapacitet som representerar serverns beräknade enheter.</span><span class="sxs-lookup"><span data-stu-id="cceb1-157">`[SkuCapacity <Int32?>]`: The scale up/out capacity, representing server's compute units.</span></span>
  - <span data-ttu-id="cceb1-158">`[SkuFamily <String>]`: Produkt familjen.</span><span class="sxs-lookup"><span data-stu-id="cceb1-158">`[SkuFamily <String>]`: The family of hardware.</span></span>
  - <span data-ttu-id="cceb1-159">`[SkuName <String>]`: Namnet på SKU: n, vanligt vis nivå + Family + cores, till exempel B_Gen4_1 GP_Gen5_8.</span><span class="sxs-lookup"><span data-stu-id="cceb1-159">`[SkuName <String>]`: The name of the sku, typically, tier + family + cores, e.g. B_Gen4_1, GP_Gen5_8.</span></span>
  - <span data-ttu-id="cceb1-160">`[SkuSize <String>]`: Storleks koden, som ska tolkas av resursen.</span><span class="sxs-lookup"><span data-stu-id="cceb1-160">`[SkuSize <String>]`: The size code, to be interpreted by resource as appropriate.</span></span>
  - <span data-ttu-id="cceb1-161">`[SkuTier <SkuTier?>]`: Nivån för den aktuella SKU: n, t. ex.</span><span class="sxs-lookup"><span data-stu-id="cceb1-161">`[SkuTier <SkuTier?>]`: The tier of the particular SKU, e.g. Basic.</span></span>
  - <span data-ttu-id="cceb1-162">`[SslEnforcement <SslEnforcementEnum?>]`: Aktivera SSL-tvång eller inte vid anslutning till server.</span><span class="sxs-lookup"><span data-stu-id="cceb1-162">`[SslEnforcement <SslEnforcementEnum?>]`: Enable ssl enforcement or not when connect to server.</span></span>
  - <span data-ttu-id="cceb1-163">`[StorageProfileBackupRetentionDay <Int32?>]`: Bevarande dagar för säkerhets kopior för servern.</span><span class="sxs-lookup"><span data-stu-id="cceb1-163">`[StorageProfileBackupRetentionDay <Int32?>]`: Backup retention days for the server.</span></span>
  - <span data-ttu-id="cceb1-164">`[StorageProfileGeoRedundantBackup <GeoRedundantBackup?>]`: Aktivera Geo-redundant eller ej för säkerhets kopiering av Server.</span><span class="sxs-lookup"><span data-stu-id="cceb1-164">`[StorageProfileGeoRedundantBackup <GeoRedundantBackup?>]`: Enable Geo-redundant or not for server backup.</span></span>
  - <span data-ttu-id="cceb1-165">`[StorageProfileStorageAutogrow <StorageAutogrow?>]`: Aktivera automatisk tillväxt av lagring.</span><span class="sxs-lookup"><span data-stu-id="cceb1-165">`[StorageProfileStorageAutogrow <StorageAutogrow?>]`: Enable Storage Auto Grow.</span></span>
  - <span data-ttu-id="cceb1-166">`[StorageProfileStorageMb <Int32?>]`: Högsta tillåtna lagrings utrymme för en server.</span><span class="sxs-lookup"><span data-stu-id="cceb1-166">`[StorageProfileStorageMb <Int32?>]`: Max storage allowed for a server.</span></span>
  - <span data-ttu-id="cceb1-167">`[UserVisibleState <ServerState?>]`: Ett tillstånd för en server som är synlig för användaren.</span><span class="sxs-lookup"><span data-stu-id="cceb1-167">`[UserVisibleState <ServerState?>]`: A state of a server that is visible to user.</span></span>
  - <span data-ttu-id="cceb1-168">`[Version <ServerVersion?>]`: Server version.</span><span class="sxs-lookup"><span data-stu-id="cceb1-168">`[Version <ServerVersion?>]`: Server version.</span></span>

## <span data-ttu-id="cceb1-169">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="cceb1-169">RELATED LINKS</span></span>

