---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 256AA6F4-D856-4713-A0AC-0DA1A145AA5C
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/get-azurermsqldatabasegeobackup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRMSqlDatabaseGeoBackup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRMSqlDatabaseGeoBackup.md
ms.openlocfilehash: 79e4919278e034c97b224c17538edfebfbf51a43
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93756444"
---
# <span data-ttu-id="4721b-101">Get-AzureRmSqlDatabaseGeoBackup</span><span class="sxs-lookup"><span data-stu-id="4721b-101">Get-AzureRmSqlDatabaseGeoBackup</span></span>

## <span data-ttu-id="4721b-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="4721b-102">SYNOPSIS</span></span>
<span data-ttu-id="4721b-103">Hämtar en Geo-redundant säkerhets kopiering av en databas.</span><span class="sxs-lookup"><span data-stu-id="4721b-103">Gets a geo-redundant backup of a database.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4721b-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="4721b-104">SYNTAX</span></span>

```
Get-AzureRmSqlDatabaseGeoBackup [-ServerName] <String> [[-DatabaseName] <String>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4721b-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="4721b-105">DESCRIPTION</span></span>
<span data-ttu-id="4721b-106">Cmdleten **Get-AzureRMSqlDatabaseGeoBackup** har angiven Geo-redundant säkerhets kopiering av en SQL-databas eller alla tillgängliga geo-redundanta säkerhets kopieringar på en angiven server.</span><span class="sxs-lookup"><span data-stu-id="4721b-106">The **Get-AzureRMSqlDatabaseGeoBackup** cmdlet gets a specified geo-redundant backup of a SQL database or all available geo-redundant backups on a specified server.</span></span>

<span data-ttu-id="4721b-107">En Geo-redundant säkerhets kopiering är en restorable resurs som använder datafiler från en separat geografisk plats.</span><span class="sxs-lookup"><span data-stu-id="4721b-107">A geo-redundant backup is a restorable resource using data files from a separate geographic location.</span></span>
<span data-ttu-id="4721b-108">Du kan använda Geo-Restore för att återställa en Geo-redundant säkerhets kopiering i händelse av ett regionalt avbrott för att återställa databasen till ett nytt område.</span><span class="sxs-lookup"><span data-stu-id="4721b-108">You can use Geo-Restore to restore a geo-redundant backup in the event of a regional outage to recover your database to a new region.</span></span>

<span data-ttu-id="4721b-109">Denna cmdlet stöds också av SQL Server utsträckt databas tjänst på Azure.</span><span class="sxs-lookup"><span data-stu-id="4721b-109">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="4721b-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="4721b-110">EXAMPLES</span></span>

### <span data-ttu-id="4721b-111">Exempel 1: Hämta alla geo-redundanta säkerhets kopior på en server</span><span class="sxs-lookup"><span data-stu-id="4721b-111">Example 1: Get all geo-redundant backups on a server</span></span>
```
PS C:\>Get-AzureRMSqlDatabaseGeoBackup -ResourceGroupName "ContosoResourceGroup" -ServerName "ContosoServer"
```

<span data-ttu-id="4721b-112">Det här kommandot får alla tillgängliga geo-redundanta säkerhets kopieringar på en angiven server.</span><span class="sxs-lookup"><span data-stu-id="4721b-112">This command gets all available geo-redundant backups on a specified server.</span></span>

### <span data-ttu-id="4721b-113">Exempel 2: skaffa en angiven Geo-redundant säkerhets kopiering</span><span class="sxs-lookup"><span data-stu-id="4721b-113">Example 2: Get a specified geo-redundant backup</span></span>
```
PS C:\>Get-AzureRMSqlDatabaseGeoBackup -ResourceGroupName "ContosoResourceGroup" -ServerName "ContosoServer" -DatabaseName "ContosoDatabase"
```

<span data-ttu-id="4721b-114">Det här kommandot får databasen Geo-redundant säkerhets kopiering med namnet ContosoDatabase.</span><span class="sxs-lookup"><span data-stu-id="4721b-114">This command gets the database geo-redundant backup named ContosoDatabase.</span></span>

## <span data-ttu-id="4721b-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="4721b-115">PARAMETERS</span></span>

### <span data-ttu-id="4721b-116">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="4721b-116">-DatabaseName</span></span>
<span data-ttu-id="4721b-117">Anger namnet på den databas som ska visas.</span><span class="sxs-lookup"><span data-stu-id="4721b-117">Specifies the name of the database to get.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4721b-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4721b-118">-DefaultProfile</span></span>
<span data-ttu-id="4721b-119">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="4721b-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4721b-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4721b-120">-ResourceGroupName</span></span>
<span data-ttu-id="4721b-121">Anger namnet på den resurs grupp som SQL-databasfilen har tilldelats till.</span><span class="sxs-lookup"><span data-stu-id="4721b-121">Specifies the name of the resource group to which the SQL database server is assigned.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4721b-122">-ServerName</span><span class="sxs-lookup"><span data-stu-id="4721b-122">-ServerName</span></span>
<span data-ttu-id="4721b-123">Anger namnet på den server som är värd för säkerhets kopian som ska återställas.</span><span class="sxs-lookup"><span data-stu-id="4721b-123">Specifies the name of the server that hosts the backup to restore.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4721b-124">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="4721b-124">-Confirm</span></span>
<span data-ttu-id="4721b-125">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="4721b-125">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4721b-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4721b-126">-WhatIf</span></span>
<span data-ttu-id="4721b-127">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="4721b-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4721b-128">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="4721b-128">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4721b-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4721b-129">CommonParameters</span></span>
<span data-ttu-id="4721b-130">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4721b-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4721b-131">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4721b-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4721b-132">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="4721b-132">INPUTS</span></span>

### <span data-ttu-id="4721b-133">Ingen</span><span class="sxs-lookup"><span data-stu-id="4721b-133">None</span></span>
<span data-ttu-id="4721b-134">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="4721b-134">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="4721b-135">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="4721b-135">OUTPUTS</span></span>

### <span data-ttu-id="4721b-136">Microsoft. Azure. commands. SQL. backup. Model. AzureSqlDatabaseGeoBackupModel</span><span class="sxs-lookup"><span data-stu-id="4721b-136">Microsoft.Azure.Commands.Sql.Backup.Model.AzureSqlDatabaseGeoBackupModel</span></span>

## <span data-ttu-id="4721b-137">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="4721b-137">NOTES</span></span>

## <span data-ttu-id="4721b-138">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="4721b-138">RELATED LINKS</span></span>

[<span data-ttu-id="4721b-139">Översikt: moln rörelse kontinuitet och databas för katastrof återställning med SQL-databas</span><span class="sxs-lookup"><span data-stu-id="4721b-139">Overview: Cloud business continuity and database disaster recovery with SQL Database</span></span>](https://go.microsoft.com/fwlink/?LinkId=746881)

[<span data-ttu-id="4721b-140">Återställa en Azure SQL-databas från ett avbrott</span><span class="sxs-lookup"><span data-stu-id="4721b-140">Recover an Azure SQL Database from an outage</span></span>](https://go.microsoft.com/fwlink/?LinkId=746882)

[<span data-ttu-id="4721b-141">Återställ-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="4721b-141">Restore-AzureRmSqlDatabase</span></span>](./Restore-AzureRmSqlDatabase.md)

[<span data-ttu-id="4721b-142">Dokumentation för SQL-databaser</span><span class="sxs-lookup"><span data-stu-id="4721b-142">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
