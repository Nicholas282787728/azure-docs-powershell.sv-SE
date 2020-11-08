---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 256AA6F4-D856-4713-A0AC-0DA1A145AA5C
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqldatabasegeobackup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseGeoBackup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseGeoBackup.md
ms.openlocfilehash: 0ca3a6c467ab5fd7dd681164d88686a6360394ee
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94272832"
---
# <span data-ttu-id="a0a97-101">Get-AzSqlDatabaseGeoBackup</span><span class="sxs-lookup"><span data-stu-id="a0a97-101">Get-AzSqlDatabaseGeoBackup</span></span>

## <span data-ttu-id="a0a97-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="a0a97-102">SYNOPSIS</span></span>
<span data-ttu-id="a0a97-103">Hämtar en Geo-redundant säkerhets kopiering av en databas.</span><span class="sxs-lookup"><span data-stu-id="a0a97-103">Gets a geo-redundant backup of a database.</span></span>

## <span data-ttu-id="a0a97-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="a0a97-104">SYNTAX</span></span>

```
Get-AzSqlDatabaseGeoBackup [-ServerName] <String> [[-DatabaseName] <String>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a0a97-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="a0a97-105">DESCRIPTION</span></span>
<span data-ttu-id="a0a97-106">Cmdleten **Get-AzSqlDatabaseGeoBackup** har angiven Geo-redundant säkerhets kopiering av en SQL-databas eller alla tillgängliga geo-redundanta säkerhets kopieringar på en angiven server.</span><span class="sxs-lookup"><span data-stu-id="a0a97-106">The **Get-AzSqlDatabaseGeoBackup** cmdlet gets a specified geo-redundant backup of a SQL database or all available geo-redundant backups on a specified server.</span></span>
<span data-ttu-id="a0a97-107">En Geo-redundant säkerhets kopiering är en restorable resurs som använder datafiler från en separat geografisk plats.</span><span class="sxs-lookup"><span data-stu-id="a0a97-107">A geo-redundant backup is a restorable resource using data files from a separate geographic location.</span></span>
<span data-ttu-id="a0a97-108">Du kan använda Geo-Restore för att återställa en Geo-redundant säkerhets kopiering i händelse av ett regionalt avbrott för att återställa databasen till ett nytt område.</span><span class="sxs-lookup"><span data-stu-id="a0a97-108">You can use Geo-Restore to restore a geo-redundant backup in the event of a regional outage to recover your database to a new region.</span></span>
<span data-ttu-id="a0a97-109">Denna cmdlet stöds också av SQL Server utsträckt databas tjänst på Azure.</span><span class="sxs-lookup"><span data-stu-id="a0a97-109">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="a0a97-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="a0a97-110">EXAMPLES</span></span>

### <span data-ttu-id="a0a97-111">Exempel 1: Hämta alla geo-redundanta säkerhets kopior på en server</span><span class="sxs-lookup"><span data-stu-id="a0a97-111">Example 1: Get all geo-redundant backups on a server</span></span>
```
PS C:\>Get-AzSqlDatabaseGeoBackup -ResourceGroupName "ContosoResourceGroup" -ServerName "ContosoServer"
```

<span data-ttu-id="a0a97-112">Det här kommandot får alla tillgängliga geo-redundanta säkerhets kopieringar på en angiven server.</span><span class="sxs-lookup"><span data-stu-id="a0a97-112">This command gets all available geo-redundant backups on a specified server.</span></span>

### <span data-ttu-id="a0a97-113">Exempel 2: skaffa en angiven Geo-redundant säkerhets kopiering</span><span class="sxs-lookup"><span data-stu-id="a0a97-113">Example 2: Get a specified geo-redundant backup</span></span>
```
PS C:\>Get-AzSqlDatabaseGeoBackup -ResourceGroupName "ContosoResourceGroup" -ServerName "ContosoServer" -DatabaseName "ContosoDatabase"
```

<span data-ttu-id="a0a97-114">Det här kommandot får databasen Geo-redundant säkerhets kopiering med namnet ContosoDatabase.</span><span class="sxs-lookup"><span data-stu-id="a0a97-114">This command gets the database geo-redundant backup named ContosoDatabase.</span></span>

### <span data-ttu-id="a0a97-115">Exempel 3: Hämta alla geo-redundanta säkerhets kopieringar på en server med filter</span><span class="sxs-lookup"><span data-stu-id="a0a97-115">Example 3: Get all geo-redundant backups on a server using filtering</span></span>
```
PS C:\>Get-AzSqlDatabaseGeoBackup -ResourceGroupName "ContosoResourceGroup" -ServerName "ContosoServer" -DatabaseName "Contoso*"
```

<span data-ttu-id="a0a97-116">Det här kommandot får alla tillgängliga geo-redundanta säkerhets kopieringar på en angiven server som börjar med "contoso".</span><span class="sxs-lookup"><span data-stu-id="a0a97-116">This command gets all available geo-redundant backups on a specified server that start with "Contoso".</span></span>

## <span data-ttu-id="a0a97-117">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="a0a97-117">PARAMETERS</span></span>

### <span data-ttu-id="a0a97-118">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="a0a97-118">-DatabaseName</span></span>
<span data-ttu-id="a0a97-119">Anger namnet på den databas som ska visas.</span><span class="sxs-lookup"><span data-stu-id="a0a97-119">Specifies the name of the database to get.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a0a97-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a0a97-120">-DefaultProfile</span></span>
<span data-ttu-id="a0a97-121">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="a0a97-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a0a97-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a0a97-122">-ResourceGroupName</span></span>
<span data-ttu-id="a0a97-123">Anger namnet på den resurs grupp som SQL-databasfilen har tilldelats till.</span><span class="sxs-lookup"><span data-stu-id="a0a97-123">Specifies the name of the resource group to which the SQL database server is assigned.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a0a97-124">-ServerName</span><span class="sxs-lookup"><span data-stu-id="a0a97-124">-ServerName</span></span>
<span data-ttu-id="a0a97-125">Anger namnet på den server som är värd för säkerhets kopian som ska återställas.</span><span class="sxs-lookup"><span data-stu-id="a0a97-125">Specifies the name of the server that hosts the backup to restore.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a0a97-126">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="a0a97-126">-Confirm</span></span>
<span data-ttu-id="a0a97-127">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="a0a97-127">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a0a97-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a0a97-128">-WhatIf</span></span>
<span data-ttu-id="a0a97-129">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="a0a97-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a0a97-130">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="a0a97-130">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a0a97-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a0a97-131">CommonParameters</span></span>
<span data-ttu-id="a0a97-132">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a0a97-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a0a97-133">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a0a97-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a0a97-134">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="a0a97-134">INPUTS</span></span>

### <span data-ttu-id="a0a97-135">System. String</span><span class="sxs-lookup"><span data-stu-id="a0a97-135">System.String</span></span>

## <span data-ttu-id="a0a97-136">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="a0a97-136">OUTPUTS</span></span>

### <span data-ttu-id="a0a97-137">Microsoft. Azure. commands. SQL. backup. Model. AzureSqlDatabaseGeoBackupModel</span><span class="sxs-lookup"><span data-stu-id="a0a97-137">Microsoft.Azure.Commands.Sql.Backup.Model.AzureSqlDatabaseGeoBackupModel</span></span>

## <span data-ttu-id="a0a97-138">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="a0a97-138">NOTES</span></span>

## <span data-ttu-id="a0a97-139">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="a0a97-139">RELATED LINKS</span></span>

[<span data-ttu-id="a0a97-140">Översikt: moln rörelse kontinuitet och databas för katastrof återställning med SQL-databas</span><span class="sxs-lookup"><span data-stu-id="a0a97-140">Overview: Cloud business continuity and database disaster recovery with SQL Database</span></span>](http://go.microsoft.com/fwlink/?LinkId=746881)

[<span data-ttu-id="a0a97-141">Återställa en Azure SQL-databas från ett avbrott</span><span class="sxs-lookup"><span data-stu-id="a0a97-141">Recover an Azure SQL Database from an outage</span></span>](http://go.microsoft.com/fwlink/?LinkId=746882)

[<span data-ttu-id="a0a97-142">Återställ-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="a0a97-142">Restore-AzSqlDatabase</span></span>](./Restore-AzSqlDatabase.md)

[<span data-ttu-id="a0a97-143">Dokumentation för SQL-databaser</span><span class="sxs-lookup"><span data-stu-id="a0a97-143">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
