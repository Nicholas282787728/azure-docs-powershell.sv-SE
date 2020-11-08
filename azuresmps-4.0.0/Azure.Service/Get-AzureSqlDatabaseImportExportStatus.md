---
external help file: Microsoft.WindowsAzure.Commands.SqlDatabase.dll-Help.xml
ms.assetid: 4661C479-6E3B-425D-B9D2-B36D7A83130C
online version: ''
schema: 2.0.0
ms.openlocfilehash: c3c55ebd22337a8078f3ae495b3901317f4201e0
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94099524"
---
# <span data-ttu-id="fb6dc-101">Get-AzureSqlDatabaseImportExportStatus</span><span class="sxs-lookup"><span data-stu-id="fb6dc-101">Get-AzureSqlDatabaseImportExportStatus</span></span>

## <span data-ttu-id="fb6dc-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="fb6dc-102">SYNOPSIS</span></span>
<span data-ttu-id="fb6dc-103">Hämtar statusen för en import-eller export förfrågan.</span><span class="sxs-lookup"><span data-stu-id="fb6dc-103">Gets the status of an import or export request.</span></span>

## <span data-ttu-id="fb6dc-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="fb6dc-104">SYNTAX</span></span>

### <span data-ttu-id="fb6dc-105">ByConnectionInfo</span><span class="sxs-lookup"><span data-stu-id="fb6dc-105">ByConnectionInfo</span></span>
```
Get-AzureSqlDatabaseImportExportStatus -Username <String> -Password <String> -ServerName <String>
 -RequestId <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="fb6dc-106">ByRequestObject</span><span class="sxs-lookup"><span data-stu-id="fb6dc-106">ByRequestObject</span></span>
```
Get-AzureSqlDatabaseImportExportStatus -Request <ImportExportRequest> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="fb6dc-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="fb6dc-107">DESCRIPTION</span></span>
<span data-ttu-id="fb6dc-108">Cmdleten **Get-AzureSqlDatabaseImportExportStatus** får statusen för en import-eller export förfrågan.</span><span class="sxs-lookup"><span data-stu-id="fb6dc-108">The **Get-AzureSqlDatabaseImportExportStatus** cmdlet gets the status of an import or export request.</span></span>
<span data-ttu-id="fb6dc-109">Start-AzureSqlDatabaseImport eller Start-AzureSqlDatabaseExport cmdlet initierar begär Anden.</span><span class="sxs-lookup"><span data-stu-id="fb6dc-109">The Start-AzureSqlDatabaseImport or Start-AzureSqlDatabaseExport cmdlet initiates requests.</span></span>
<span data-ttu-id="fb6dc-110">Du kan ange ett Request-objekt med hjälp av parametern *Request* , eller så kan du identifiera begäran genom att använda parametern *RequestId* och parametrarna *username* , *Password* och *servername* .</span><span class="sxs-lookup"><span data-stu-id="fb6dc-110">You can specify the request object by using the *Request* parameter, or you can identify the request by using the *RequestId* parameter and the *Username* , *Password* , and *ServerName* parameters.</span></span>

## <span data-ttu-id="fb6dc-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="fb6dc-111">EXAMPLES</span></span>

### <span data-ttu-id="fb6dc-112">Exempel 1: få statusen för en export förfrågan</span><span class="sxs-lookup"><span data-stu-id="fb6dc-112">Example 1: Get the status of an export request</span></span>
```
PS C:\> $ExportRequest = Start-AzureSqlDatabaseExport -SqlConnectionContext $SqlContext -StorageContainer $Container -DatabaseName $DatabaseName -BlobName $BlobName
PS C:\> Get-AzureSqlDatabaseImportExportStatus -Request $ExportRequest
```

<span data-ttu-id="fb6dc-113">Det första kommandot skapar en export förfrågan och lagrar den sedan i $ExportRequest variabel.</span><span class="sxs-lookup"><span data-stu-id="fb6dc-113">The first command creates an export request, and then stores it in the $ExportRequest variable.</span></span>

<span data-ttu-id="fb6dc-114">Det andra kommandot får statusen för den exportfiler som är lagrad i $ExportRequest.</span><span class="sxs-lookup"><span data-stu-id="fb6dc-114">The second command gets the status of the export request stored in $ExportRequest.</span></span>

## <span data-ttu-id="fb6dc-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="fb6dc-115">PARAMETERS</span></span>

### <span data-ttu-id="fb6dc-116">-Lösen ord</span><span class="sxs-lookup"><span data-stu-id="fb6dc-116">-Password</span></span>
<span data-ttu-id="fb6dc-117">Anger det lösen ord som krävs för att ansluta till Azure SQL Database-servern.</span><span class="sxs-lookup"><span data-stu-id="fb6dc-117">Specifies the password that is required to connect to the Azure SQL Database server.</span></span>
<span data-ttu-id="fb6dc-118">Du måste ange den här parametern om du har angett parametern *RequestId* .</span><span class="sxs-lookup"><span data-stu-id="fb6dc-118">You must specify this parameter if you specified the *RequestId* parameter.</span></span>

```yaml
Type: String
Parameter Sets: ByConnectionInfo
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fb6dc-119">-Profil</span><span class="sxs-lookup"><span data-stu-id="fb6dc-119">-Profile</span></span>
<span data-ttu-id="fb6dc-120">Anger den Azure-profil från vilken denna cmdlet läser.</span><span class="sxs-lookup"><span data-stu-id="fb6dc-120">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="fb6dc-121">Om du inte anger en profil läser denna cmdlet från den lokala standard profilen.</span><span class="sxs-lookup"><span data-stu-id="fb6dc-121">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="fb6dc-122">-Begäran</span><span class="sxs-lookup"><span data-stu-id="fb6dc-122">-Request</span></span>
<span data-ttu-id="fb6dc-123">Anger ett **ImportExportRequest** -objekt.</span><span class="sxs-lookup"><span data-stu-id="fb6dc-123">Specifies an **ImportExportRequest** object.</span></span>
<span data-ttu-id="fb6dc-124">Om du vill hämta ett objekt för import eller export, Använd cmdleten Start-AzureSqlDatabaseImport eller Start-AzureSqlDatabaseExport.</span><span class="sxs-lookup"><span data-stu-id="fb6dc-124">To obtain an import or export request object, use the Start-AzureSqlDatabaseImport or Start-AzureSqlDatabaseExport cmdlet.</span></span>

```yaml
Type: ImportExportRequest
Parameter Sets: ByRequestObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fb6dc-125">-Begärande-RequestId</span><span class="sxs-lookup"><span data-stu-id="fb6dc-125">-RequestId</span></span>
<span data-ttu-id="fb6dc-126">Anger GUID för den import-eller export åtgärd som denna cmdlet får status för.</span><span class="sxs-lookup"><span data-stu-id="fb6dc-126">Specifies the GUID of the import or export operation for which this cmdlet gets status.</span></span>
<span data-ttu-id="fb6dc-127">Om du anger den här parametern måste du ange *användar namn* , *lösen ord* och *servername* -parametrar.</span><span class="sxs-lookup"><span data-stu-id="fb6dc-127">If you specify this parameter, you must specify the *UserName* , *Password* , and *ServerName* parameters.</span></span>

```yaml
Type: String
Parameter Sets: ByConnectionInfo
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fb6dc-128">-ServerName</span><span class="sxs-lookup"><span data-stu-id="fb6dc-128">-ServerName</span></span>
<span data-ttu-id="fb6dc-129">Anger namnet på Azure SQL Database-servern.</span><span class="sxs-lookup"><span data-stu-id="fb6dc-129">Specifies the name of the Azure SQL Database server.</span></span>
<span data-ttu-id="fb6dc-130">Du måste ange den här parametern om du har angett parametern *RequestId* .</span><span class="sxs-lookup"><span data-stu-id="fb6dc-130">You must specify this parameter if you specified the *RequestId* parameter.</span></span>

```yaml
Type: String
Parameter Sets: ByConnectionInfo
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fb6dc-131">-Username</span><span class="sxs-lookup"><span data-stu-id="fb6dc-131">-Username</span></span>
<span data-ttu-id="fb6dc-132">Anger det användar namn som krävs för att ansluta till Azure SQL Database-servern.</span><span class="sxs-lookup"><span data-stu-id="fb6dc-132">Specifies the user name required to connect to the Azure SQL Database server.</span></span>
<span data-ttu-id="fb6dc-133">Du måste ange den här parametern om du har angett parametern *RequestId* .</span><span class="sxs-lookup"><span data-stu-id="fb6dc-133">You must specify this parameter if you specified the *RequestId* parameter.</span></span>

```yaml
Type: String
Parameter Sets: ByConnectionInfo
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fb6dc-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fb6dc-134">CommonParameters</span></span>
<span data-ttu-id="fb6dc-135">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fb6dc-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fb6dc-136">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fb6dc-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fb6dc-137">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="fb6dc-137">INPUTS</span></span>

## <span data-ttu-id="fb6dc-138">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="fb6dc-138">OUTPUTS</span></span>

### <span data-ttu-id="fb6dc-139">Microsoft. WindowsAzure. kommandon. SqlDatabase. Services. ImportExport. StatusInfo</span><span class="sxs-lookup"><span data-stu-id="fb6dc-139">Microsoft.WindowsAzure.Commands.SqlDatabase.Services.ImportExport.StatusInfo</span></span>

## <span data-ttu-id="fb6dc-140">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="fb6dc-140">NOTES</span></span>

## <span data-ttu-id="fb6dc-141">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="fb6dc-141">RELATED LINKS</span></span>

[<span data-ttu-id="fb6dc-142">Azure SQL-databas</span><span class="sxs-lookup"><span data-stu-id="fb6dc-142">Azure SQL Database</span></span>](https://azure.microsoft.com/en-us/services/sql-database/)

[<span data-ttu-id="fb6dc-143">Hämta status för importera export databas</span><span class="sxs-lookup"><span data-stu-id="fb6dc-143">Get Import Export Database Status</span></span>](https://msdn.microsoft.com/en-us/library/azure/dn781289.aspx)

[<span data-ttu-id="fb6dc-144">Åtgärder för Azure SQL-databaser</span><span class="sxs-lookup"><span data-stu-id="fb6dc-144">Operations for Azure SQL Databases</span></span>](https://msdn.microsoft.com/en-us/library/azure/dn505719.aspx)

[<span data-ttu-id="fb6dc-145">Start-AzureSqlDatabaseExport</span><span class="sxs-lookup"><span data-stu-id="fb6dc-145">Start-AzureSqlDatabaseExport</span></span>](./Start-AzureSqlDatabaseExport.md)

[<span data-ttu-id="fb6dc-146">Start-AzureSqlDatabaseImport</span><span class="sxs-lookup"><span data-stu-id="fb6dc-146">Start-AzureSqlDatabaseImport</span></span>](./Start-AzureSqlDatabaseImport.md)


