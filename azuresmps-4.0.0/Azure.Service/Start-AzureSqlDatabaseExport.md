---
external help file: Microsoft.WindowsAzure.Commands.SqlDatabase.dll-Help.xml
ms.assetid: 3005E411-9466-4602-8E07-F4EF8804AB2A
online version: ''
schema: 2.0.0
ms.openlocfilehash: 22bff485bf49e0ec5f482e1325af661862583605
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94093478"
---
# <span data-ttu-id="73b50-101">Start-AzureSqlDatabaseExport</span><span class="sxs-lookup"><span data-stu-id="73b50-101">Start-AzureSqlDatabaseExport</span></span>

## <span data-ttu-id="73b50-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="73b50-102">SYNOPSIS</span></span>
<span data-ttu-id="73b50-103">Startar en export från en Azure SQL-databas till en blob-lagring.</span><span class="sxs-lookup"><span data-stu-id="73b50-103">Starts an export operation from an Azure SQL Database to Blob storage.</span></span>

## <span data-ttu-id="73b50-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="73b50-104">SYNTAX</span></span>

### <span data-ttu-id="73b50-105">ByContainerObject</span><span class="sxs-lookup"><span data-stu-id="73b50-105">ByContainerObject</span></span>
```
Start-AzureSqlDatabaseExport -SqlConnectionContext <ISqlServerConnectionInformation>
 -StorageContainer <AzureStorageContainer> -DatabaseName <String> -BlobName <String>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="73b50-106">ByContainerName</span><span class="sxs-lookup"><span data-stu-id="73b50-106">ByContainerName</span></span>
```
Start-AzureSqlDatabaseExport -SqlConnectionContext <ISqlServerConnectionInformation>
 -StorageContext <IStorageContext> -StorageContainerName <String> -DatabaseName <String> -BlobName <String>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="73b50-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="73b50-107">DESCRIPTION</span></span>
<span data-ttu-id="73b50-108">Cmdleten **Start-AzureSqlDatabaseExport** startar en export åtgärd från en Azure SQL-databas till Blob Storage.</span><span class="sxs-lookup"><span data-stu-id="73b50-108">The **Start-AzureSqlDatabaseExport** cmdlet starts an export operation from an Azure SQL Database to Blob storage.</span></span>
<span data-ttu-id="73b50-109">Åtgärden kräver en databas server anslutning.</span><span class="sxs-lookup"><span data-stu-id="73b50-109">The operation requires a database server connection context.</span></span>
<span data-ttu-id="73b50-110">Använd Get-AzureSqlDatabaseImportExportStatus cmdlet för att få statusen för exporten.</span><span class="sxs-lookup"><span data-stu-id="73b50-110">Use the Get-AzureSqlDatabaseImportExportStatus cmdlet to get the status of the export operation.</span></span>

## <span data-ttu-id="73b50-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="73b50-111">EXAMPLES</span></span>

### <span data-ttu-id="73b50-112">Exempel 1: exportera en databas</span><span class="sxs-lookup"><span data-stu-id="73b50-112">Example 1: Export a database</span></span>
```
PS C:\>$Credential = Get-Credential
PS C:\> $SqlContext = New-AzureSqlDatabaseServerContext -ServerName $ServerName -Credential $Credential
PS C:\> $StorageContext = New-AzureStorageContext -StorageAccountName $StorageName -StorageAccountKey $StorageKey
PS C:\> $Container = Get-AzureStorageContainer -Name $ContainerName -Context $StorageContext
PS C:\> $exportRequest = Start-AzureSqlDatabaseExport -SqlConnectionContext $SqlContext -StorageContainer $Container -DatabaseName $DatabaseName -BlobName $BlobName
```

<span data-ttu-id="73b50-113">I det här exemplet startas en export process från den Azure SQL-databas som har namnet som lagras i $DatabaseName-variabeln till blob-lagringen i $BlobName variabel.</span><span class="sxs-lookup"><span data-stu-id="73b50-113">This example initiates an export process from the Azure SQL Database that has the name stored in the $DatabaseName variable to the Blob storage stored in the $BlobName variable.</span></span>

## <span data-ttu-id="73b50-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="73b50-114">PARAMETERS</span></span>

### <span data-ttu-id="73b50-115">-BlobName</span><span class="sxs-lookup"><span data-stu-id="73b50-115">-BlobName</span></span>
<span data-ttu-id="73b50-116">Anger namnet på den Azure Blob-lagring där denna cmdlet exporterar databasen.</span><span class="sxs-lookup"><span data-stu-id="73b50-116">Specifies the name of the Azure Blob storage into which this cmdlet exports the database.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="73b50-117">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="73b50-117">-DatabaseName</span></span>
<span data-ttu-id="73b50-118">Anger namnet på den databas som denna cmdlet exporterar data från.</span><span class="sxs-lookup"><span data-stu-id="73b50-118">Specifies the name of the database from which this cmdlet exports data.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="73b50-119">-Profil</span><span class="sxs-lookup"><span data-stu-id="73b50-119">-Profile</span></span>
<span data-ttu-id="73b50-120">Anger den Azure-profil från vilken denna cmdlet läser.</span><span class="sxs-lookup"><span data-stu-id="73b50-120">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="73b50-121">Om du inte anger en profil läser denna cmdlet från den lokala standard profilen.</span><span class="sxs-lookup"><span data-stu-id="73b50-121">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="73b50-122">-SqlConnectionContext</span><span class="sxs-lookup"><span data-stu-id="73b50-122">-SqlConnectionContext</span></span>
<span data-ttu-id="73b50-123">Anger den anslutnings kontext för en server som innehåller databasen.</span><span class="sxs-lookup"><span data-stu-id="73b50-123">Specifies the connection context of a server that contains the database.</span></span>

```yaml
Type: ISqlServerConnectionInformation
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="73b50-124">-StorageContainer</span><span class="sxs-lookup"><span data-stu-id="73b50-124">-StorageContainer</span></span>
<span data-ttu-id="73b50-125">Anger lagrings behållaren som innehåller blobben som denna cmdlet exporterar en databas till.</span><span class="sxs-lookup"><span data-stu-id="73b50-125">Specifies the storage container that contains the Blob into which this cmdlet export a database.</span></span>

```yaml
Type: AzureStorageContainer
Parameter Sets: ByContainerObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="73b50-126">-StorageContainerName</span><span class="sxs-lookup"><span data-stu-id="73b50-126">-StorageContainerName</span></span>
<span data-ttu-id="73b50-127">Anger namnet på den lagrings behållare som innehåller den BLOB dit denna cmdlet exporterar en databas.</span><span class="sxs-lookup"><span data-stu-id="73b50-127">Specifies the name of the storage container that contains the Blob into which this cmdlet exports a database.</span></span>

```yaml
Type: String
Parameter Sets: ByContainerName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="73b50-128">-StorageContext</span><span class="sxs-lookup"><span data-stu-id="73b50-128">-StorageContext</span></span>
<span data-ttu-id="73b50-129">Anger kontexten för Blob storage-behållaren.</span><span class="sxs-lookup"><span data-stu-id="73b50-129">Specifies the context of the Blob storage container.</span></span>

```yaml
Type: IStorageContext
Parameter Sets: ByContainerName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="73b50-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="73b50-130">CommonParameters</span></span>
<span data-ttu-id="73b50-131">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="73b50-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="73b50-132">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="73b50-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="73b50-133">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="73b50-133">INPUTS</span></span>

## <span data-ttu-id="73b50-134">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="73b50-134">OUTPUTS</span></span>

### <span data-ttu-id="73b50-135">Microsoft. WindowsAzure. kommandon. SqlDatabase. Services. ImportExportRequest</span><span class="sxs-lookup"><span data-stu-id="73b50-135">Microsoft.WindowsAzure.Commands.SqlDatabase.Services.ImportExportRequest</span></span>

## <span data-ttu-id="73b50-136">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="73b50-136">NOTES</span></span>

## <span data-ttu-id="73b50-137">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="73b50-137">RELATED LINKS</span></span>

[<span data-ttu-id="73b50-138">Azure SQL-databas</span><span class="sxs-lookup"><span data-stu-id="73b50-138">Azure SQL Database</span></span>](https://azure.microsoft.com/en-us/services/sql-database/)

[<span data-ttu-id="73b50-139">Exportera databas</span><span class="sxs-lookup"><span data-stu-id="73b50-139">Export Database</span></span>](https://msdn.microsoft.com/en-us/library/azure/dn781282.aspx)

[<span data-ttu-id="73b50-140">Åtgärder för Azure SQL-databaser</span><span class="sxs-lookup"><span data-stu-id="73b50-140">Operations for Azure SQL Databases</span></span>](https://msdn.microsoft.com/en-us/library/azure/dn505719.aspx)

[<span data-ttu-id="73b50-141">Get-AzureSqlDatabaseImportExportStatus</span><span class="sxs-lookup"><span data-stu-id="73b50-141">Get-AzureSqlDatabaseImportExportStatus</span></span>](./Get-AzureSqlDatabaseImportExportStatus.md)

[<span data-ttu-id="73b50-142">Start-AzureSqlDatabaseImport</span><span class="sxs-lookup"><span data-stu-id="73b50-142">Start-AzureSqlDatabaseImport</span></span>](./Start-AzureSqlDatabaseImport.md)


