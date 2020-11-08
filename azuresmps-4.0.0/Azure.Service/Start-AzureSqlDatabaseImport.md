---
external help file: Microsoft.WindowsAzure.Commands.SqlDatabase.dll-Help.xml
ms.assetid: 5EE936CA-DD9A-4BC6-B835-E22AE633B46D
online version: ''
schema: 2.0.0
ms.openlocfilehash: 4bc7c8f39f1bdbd35cfffeb59b3b4f184f30845e
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94093153"
---
# <span data-ttu-id="efb9c-101">Start-AzureSqlDatabaseImport</span><span class="sxs-lookup"><span data-stu-id="efb9c-101">Start-AzureSqlDatabaseImport</span></span>

## <span data-ttu-id="efb9c-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="efb9c-102">SYNOPSIS</span></span>
<span data-ttu-id="efb9c-103">Startar en import åtgärd från Blob Storage till en Azure SQL-databas.</span><span class="sxs-lookup"><span data-stu-id="efb9c-103">Starts an import operation from blob storage to an Azure SQL Database.</span></span>

## <span data-ttu-id="efb9c-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="efb9c-104">SYNTAX</span></span>

### <span data-ttu-id="efb9c-105">ByContainerObject</span><span class="sxs-lookup"><span data-stu-id="efb9c-105">ByContainerObject</span></span>
```
Start-AzureSqlDatabaseImport -SqlConnectionContext <ISqlServerConnectionInformation>
 -StorageContainer <AzureStorageContainer> -DatabaseName <String> -BlobName <String>
 [-Edition <DatabaseEdition>] [-DatabaseMaxSize <Int32>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="efb9c-106">ByContainerName</span><span class="sxs-lookup"><span data-stu-id="efb9c-106">ByContainerName</span></span>
```
Start-AzureSqlDatabaseImport -SqlConnectionContext <ISqlServerConnectionInformation>
 -StorageContext <IStorageContext> -StorageContainerName <String> -DatabaseName <String> -BlobName <String>
 [-Edition <DatabaseEdition>] [-DatabaseMaxSize <Int32>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="efb9c-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="efb9c-107">DESCRIPTION</span></span>
<span data-ttu-id="efb9c-108">Cmdleten **Start-AzureSqlDatabaseImport** startar en import operation från Azure Blob Storage till en Azure SQL-databas.</span><span class="sxs-lookup"><span data-stu-id="efb9c-108">The **Start-AzureSqlDatabaseImport** cmdlet starts an import operation from Azure Blob storage to an Azure SQL Database.</span></span>
<span data-ttu-id="efb9c-109">Om databasen inte finns skapar den här cmdleten den med hjälp av värdena för storlek och utgåva som du anger.</span><span class="sxs-lookup"><span data-stu-id="efb9c-109">If the database does not exist, this cmdlet creates it by using the size and edition values that you specify.</span></span>
<span data-ttu-id="efb9c-110">Åtgärden kräver en databas server anslutning.</span><span class="sxs-lookup"><span data-stu-id="efb9c-110">The operation requires a database server connection context.</span></span>
<span data-ttu-id="efb9c-111">Använd Get-AzureSqlDatabaseImportExportStatus cmdlet för att få statusen för importen.</span><span class="sxs-lookup"><span data-stu-id="efb9c-111">Use the Get-AzureSqlDatabaseImportExportStatus cmdlet to get the status of the import operation.</span></span>

## <span data-ttu-id="efb9c-112">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="efb9c-112">EXAMPLES</span></span>

### <span data-ttu-id="efb9c-113">Exempel 1: importera en databas</span><span class="sxs-lookup"><span data-stu-id="efb9c-113">Example 1: Import a database</span></span>
```
PS C:\>$Credential = Get-Credential
PS C:\> $SqlContext = New-AzureSqlDatabaseServerContext -ServerName $ServerName -Credentials $Credential
PS C:\> $StorageContext = New-AzureStorageContext -StorageAccountName $StorageName -StorageAccountKey $StorageKey
PS C:\> $Container = Get-AzureStorageContainer -Name $ContainerName -Context $StorageContext
PS C:\> $ImportRequest = Start-AzureSqlDatabaseImport -SqlConnectionContext $SqlContext -StorageContainer $Container -DatabaseName $DatabaseName -BlobName $BlobName
```

<span data-ttu-id="efb9c-114">I det här exemplet startas en import process från blob-lagringen i $BlobName-variabeln till den Azure SQL-databas som heter DatabaseName.</span><span class="sxs-lookup"><span data-stu-id="efb9c-114">This example initiates an import process from the Blob storage in the $BlobName variable into the Azure SQL Database named DatabaseName.</span></span>

## <span data-ttu-id="efb9c-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="efb9c-115">PARAMETERS</span></span>

### <span data-ttu-id="efb9c-116">-BlobName</span><span class="sxs-lookup"><span data-stu-id="efb9c-116">-BlobName</span></span>
<span data-ttu-id="efb9c-117">Anger namnet på den Azure Blob-lagring från vilken denna cmdlet importerar databasen.</span><span class="sxs-lookup"><span data-stu-id="efb9c-117">Specifies the name of the Azure Blob storage from which this cmdlet imports the database.</span></span>

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

### <span data-ttu-id="efb9c-118">-DatabaseMaxSize</span><span class="sxs-lookup"><span data-stu-id="efb9c-118">-DatabaseMaxSize</span></span>
<span data-ttu-id="efb9c-119">Anger den maximala storleken i GB för databasen.</span><span class="sxs-lookup"><span data-stu-id="efb9c-119">Specifies the maximum size, in gigabytes, for the database.</span></span>
<span data-ttu-id="efb9c-120">Om databasen inte finns skapar den här cmdleten den utifrån den maximala storleken.</span><span class="sxs-lookup"><span data-stu-id="efb9c-120">If the database does not exist, this cmdlet creates it based on this maximum size.</span></span>
<span data-ttu-id="efb9c-121">De acceptabla värdena varierar beroende på utgåva.</span><span class="sxs-lookup"><span data-stu-id="efb9c-121">The acceptable values differ based on edition.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="efb9c-122">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="efb9c-122">-DatabaseName</span></span>
<span data-ttu-id="efb9c-123">Anger ett namn för databasen.</span><span class="sxs-lookup"><span data-stu-id="efb9c-123">Specifies a name for the database.</span></span>
<span data-ttu-id="efb9c-124">Om databasen inte finns skapar den här cmdlet den och tilldelar namnet som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="efb9c-124">If the database does not exist, this cmdlet creates it, and assigns the name that this parameter specifies.</span></span>

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

### <span data-ttu-id="efb9c-125">-Utgåva</span><span class="sxs-lookup"><span data-stu-id="efb9c-125">-Edition</span></span>
<span data-ttu-id="efb9c-126">Anger versionen för databasen.</span><span class="sxs-lookup"><span data-stu-id="efb9c-126">Specifies the edition of the database.</span></span>
<span data-ttu-id="efb9c-127">Om databasen inte finns skapar den här cmdlet den som den här versionen.</span><span class="sxs-lookup"><span data-stu-id="efb9c-127">If the database does not exist, this cmdlet creates it as this edition.</span></span>
<span data-ttu-id="efb9c-128">Giltiga värden är:</span><span class="sxs-lookup"><span data-stu-id="efb9c-128">Valid values are:</span></span> 

- <span data-ttu-id="efb9c-129">Ingen</span><span class="sxs-lookup"><span data-stu-id="efb9c-129">None</span></span>
- <span data-ttu-id="efb9c-130">Webben</span><span class="sxs-lookup"><span data-stu-id="efb9c-130">Web</span></span> 
- <span data-ttu-id="efb9c-131">Uppmana</span><span class="sxs-lookup"><span data-stu-id="efb9c-131">Business</span></span> 
- <span data-ttu-id="efb9c-132">Basisk</span><span class="sxs-lookup"><span data-stu-id="efb9c-132">Basic</span></span>
- <span data-ttu-id="efb9c-133">Standar</span><span class="sxs-lookup"><span data-stu-id="efb9c-133">Standard</span></span>
- <span data-ttu-id="efb9c-134">Beta</span><span class="sxs-lookup"><span data-stu-id="efb9c-134">Premium</span></span>

<span data-ttu-id="efb9c-135">Standard är Internet.</span><span class="sxs-lookup"><span data-stu-id="efb9c-135">The default is Web.</span></span>

```yaml
Type: DatabaseEdition
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="efb9c-136">-Profil</span><span class="sxs-lookup"><span data-stu-id="efb9c-136">-Profile</span></span>
<span data-ttu-id="efb9c-137">Anger den Azure-profil från vilken denna cmdlet läser.</span><span class="sxs-lookup"><span data-stu-id="efb9c-137">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="efb9c-138">Om du inte anger en profil läser denna cmdlet från den lokala standard profilen.</span><span class="sxs-lookup"><span data-stu-id="efb9c-138">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="efb9c-139">-SqlConnectionContext</span><span class="sxs-lookup"><span data-stu-id="efb9c-139">-SqlConnectionContext</span></span>
<span data-ttu-id="efb9c-140">Anger den anslutnings kontext för en server som innehåller databasen.</span><span class="sxs-lookup"><span data-stu-id="efb9c-140">Specifies the connection context of a server that contains the database.</span></span>

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

### <span data-ttu-id="efb9c-141">-StorageContainer</span><span class="sxs-lookup"><span data-stu-id="efb9c-141">-StorageContainer</span></span>
<span data-ttu-id="efb9c-142">Anger lagrings behållaren som innehåller blobben som den här cmdleten importerar en databas från.</span><span class="sxs-lookup"><span data-stu-id="efb9c-142">Specifies the storage container that contains the Blob from which this cmdlet imports a database.</span></span>

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

### <span data-ttu-id="efb9c-143">-StorageContainerName</span><span class="sxs-lookup"><span data-stu-id="efb9c-143">-StorageContainerName</span></span>
<span data-ttu-id="efb9c-144">Anger namnet på BLOB-lagringsplatsen.</span><span class="sxs-lookup"><span data-stu-id="efb9c-144">Specifies the name of the Blob storage container.</span></span>

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

### <span data-ttu-id="efb9c-145">-StorageContext</span><span class="sxs-lookup"><span data-stu-id="efb9c-145">-StorageContext</span></span>
<span data-ttu-id="efb9c-146">Anger kontexten för Blob storage-behållaren.</span><span class="sxs-lookup"><span data-stu-id="efb9c-146">Specifies the context of the Blob storage container.</span></span>

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

### <span data-ttu-id="efb9c-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="efb9c-147">CommonParameters</span></span>
<span data-ttu-id="efb9c-148">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="efb9c-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="efb9c-149">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="efb9c-149">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="efb9c-150">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="efb9c-150">INPUTS</span></span>

## <span data-ttu-id="efb9c-151">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="efb9c-151">OUTPUTS</span></span>

### <span data-ttu-id="efb9c-152">Microsoft. WindowsAzure. kommandon. SqlDatabase. Services. ImportExportRequest</span><span class="sxs-lookup"><span data-stu-id="efb9c-152">Microsoft.WindowsAzure.Commands.SqlDatabase.Services.ImportExportRequest</span></span>

## <span data-ttu-id="efb9c-153">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="efb9c-153">NOTES</span></span>

## <span data-ttu-id="efb9c-154">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="efb9c-154">RELATED LINKS</span></span>

[<span data-ttu-id="efb9c-155">Azure SQL-databas</span><span class="sxs-lookup"><span data-stu-id="efb9c-155">Azure SQL Database</span></span>](https://azure.microsoft.com/en-us/services/sql-database/)

[<span data-ttu-id="efb9c-156">Importera databas</span><span class="sxs-lookup"><span data-stu-id="efb9c-156">Import Database</span></span>](https://msdn.microsoft.com/en-us/library/azure/dn781284.aspx)

[<span data-ttu-id="efb9c-157">Åtgärder för Azure SQL-databaser</span><span class="sxs-lookup"><span data-stu-id="efb9c-157">Operations for Azure SQL Databases</span></span>](https://msdn.microsoft.com/en-us/library/azure/dn505719.aspx)

[<span data-ttu-id="efb9c-158">Get-AzureSqlDatabaseImportExportStatus</span><span class="sxs-lookup"><span data-stu-id="efb9c-158">Get-AzureSqlDatabaseImportExportStatus</span></span>](./Get-AzureSqlDatabaseImportExportStatus.md)

[<span data-ttu-id="efb9c-159">Start-AzureSqlDatabaseExport</span><span class="sxs-lookup"><span data-stu-id="efb9c-159">Start-AzureSqlDatabaseExport</span></span>](./Start-AzureSqlDatabaseExport.md)


