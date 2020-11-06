---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/get-azurermsqldatalongtermretentionbackup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlDatabaseLongTermRetentionBackup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlDatabaseLongTermRetentionBackup.md
ms.openlocfilehash: da3b47923f39e6910566a210ddbd325d9da76ca7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93573196"
---
# <span data-ttu-id="6feb8-101">Get-AzureRmSqlDatabaseLongTermRetentionBackup</span><span class="sxs-lookup"><span data-stu-id="6feb8-101">Get-AzureRmSqlDatabaseLongTermRetentionBackup</span></span>

## <span data-ttu-id="6feb8-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="6feb8-102">SYNOPSIS</span></span>
<span data-ttu-id="6feb8-103">Hämtar en eller flera säkerhets kopior för längre tid.</span><span class="sxs-lookup"><span data-stu-id="6feb8-103">Gets one or more long term retention backups.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6feb8-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="6feb8-104">SYNTAX</span></span>

### <span data-ttu-id="6feb8-105">Plats (standard)</span><span class="sxs-lookup"><span data-stu-id="6feb8-105">Location (Default)</span></span>
```
Get-AzureRmSqlDatabaseLongTermRetentionBackup -Location <String> [-OnlyLatestPerDatabase]
 [[-DatabaseState] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="6feb8-106">ServerName</span><span class="sxs-lookup"><span data-stu-id="6feb8-106">ServerName</span></span>
```
Get-AzureRmSqlDatabaseLongTermRetentionBackup -Location <String> [-ServerName] <String>
 [[-DatabaseName] <String>] [-OnlyLatestPerDatabase] [[-DatabaseState] <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6feb8-107">BackupName</span><span class="sxs-lookup"><span data-stu-id="6feb8-107">BackupName</span></span>
```
Get-AzureRmSqlDatabaseLongTermRetentionBackup -Location <String> [-ServerName] <String>
 [-DatabaseName] <String> [-BackupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6feb8-108">GetBackupByResourceId</span><span class="sxs-lookup"><span data-stu-id="6feb8-108">GetBackupByResourceId</span></span>
```
Get-AzureRmSqlDatabaseLongTermRetentionBackup -Location <String> [-ResourceId] <String> [-BackupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6feb8-109">GetBackupsByResourceId</span><span class="sxs-lookup"><span data-stu-id="6feb8-109">GetBackupsByResourceId</span></span>
```
Get-AzureRmSqlDatabaseLongTermRetentionBackup -Location <String> [-ResourceId] <String>
 [-OnlyLatestPerDatabase] [[-DatabaseState] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6feb8-110">GetBackupByInputObject</span><span class="sxs-lookup"><span data-stu-id="6feb8-110">GetBackupByInputObject</span></span>
```
Get-AzureRmSqlDatabaseLongTermRetentionBackup [-InputObject] <AzureSqlDatabaseModel> [-BackupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6feb8-111">GetBackupsByInputObject</span><span class="sxs-lookup"><span data-stu-id="6feb8-111">GetBackupsByInputObject</span></span>
```
Get-AzureRmSqlDatabaseLongTermRetentionBackup [-InputObject] <AzureSqlDatabaseModel> [-OnlyLatestPerDatabase]
 [[-DatabaseState] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="6feb8-112">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="6feb8-112">DESCRIPTION</span></span>
<span data-ttu-id="6feb8-113">Cmdleten **Get-AzureRmSqlDatabaseLongTermRetentionBackup** alla säkerhets kopior för en lagrings plats, server eller databas eller en särskild säkerhets kopia av den långsiktiga tids perioden.</span><span class="sxs-lookup"><span data-stu-id="6feb8-113">The **Get-AzureRmSqlDatabaseLongTermRetentionBackup** cmdlet gets all long term retention backups for a location, server, or database or gets a specific long term retention backup.</span></span>

## <span data-ttu-id="6feb8-114">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="6feb8-114">EXAMPLES</span></span>

### <span data-ttu-id="6feb8-115">Exempel 1: Hämta alla säkerhets kopior för en plats</span><span class="sxs-lookup"><span data-stu-id="6feb8-115">Example 1: Get all backups for a location</span></span>
```powershell
PS C:\> Get-AzureRmSqlDatabaseLongTermRetentionBackup -Location northeurope


BackupExpirationTime : 3/22/2018 11:43:18 PM
BackupName           : 55970792-164c-4a4a-88e5-7158d092d503;131656309980000000
BackupTime           : 3/15/2018 11:43:18 PM
DatabaseName         : database02
DatabaseDeletionTime : 3/18/2018 4:36:00 PM
Location         : northeurope
ResourceId           : /subscriptions/371edd6d-9630-4558-a7bd-ee139498e6a1/providers/Microsoft.Sql/locations/northeurope/longTermRetentionServers/server02/longTermRetentionDatabases/database02/longTermRetentionBackups/55970792-164c-4a4a-88e5-7158d092d503;131656309980000000
ServerName           : server02
ServerCreateTime     : 2/28/2018 12:12:19 AM

BackupExpirationTime : 3/22/2018 5:50:55 AM
BackupName           : 601061b7-d10b-46e0-bf77-a2bfb16a6add;131655666550000000
BackupTime           : 3/15/2018 5:50:55 AM
DatabaseName         : database01
DatabaseDeletionTime :
Location         : northeurope
ResourceId           : /subscriptions/371edd6d-9630-4558-a7bd-ee139498e6a1/providers/Microsoft.Sql/locations/northeurope/longTermRetentionServers/server01/longTermRetentionDatabases/database01/longTermRetentionBackups/601061b7-d10b-46e0-bf77-a2bfb16a6add;131655666550000000
ServerName           : server01
ServerCreateTime     : 2/29/2018 12:12:19 AM
```

<span data-ttu-id="6feb8-116">Med det här kommandot får du säkerhets kopior för alla databaser (som kan vara levande eller borttagna) i northeurope.</span><span class="sxs-lookup"><span data-stu-id="6feb8-116">This command gets all long term retention backups for all databases (which may be alive or deleted) in northeurope.</span></span>

### <span data-ttu-id="6feb8-117">Exempel 2: skaffa en särskild säkerhets kopia för långsiktigt bevarande</span><span class="sxs-lookup"><span data-stu-id="6feb8-117">Example 2: Get a specific long term retention backup</span></span>
```powershell
PS C:\> Get-AzureRmSqlDatabaseLongTermRetentionBackup -Location northeurope -ServerName server01 -DatabaseName database01 -BackupName "601061b7-d10b-46e0-bf77-a2bfb16a6add;131655666550000000"


BackupExpirationTime : 3/22/2018 5:50:55 AM
BackupName           : 601061b7-d10b-46e0-bf77-a2bfb16a6add;131655666550000000
BackupTime           : 3/15/2018 5:50:55 AM
DatabaseName         : database01
DatabaseDeletionTime :
Location         : northeurope
ResourceId           : /subscriptions/371edd6d-9630-4558-a7bd-ee139498e6a1/providers/Microsoft.Sql/locations/northeurope/longTermRetentionServers/server01/longTermRetentionDatabases/database01/longTermRetentionBackups/601061b7-d10b-46e0-bf77-a2bfb16a6add;131655666550000000
ServerName           : server01
ServerCreateTime     : 2/29/2018 12:12:19 AM
```

<span data-ttu-id="6feb8-118">Det här kommandot får säkerhets kopian med namnet 601061b7-d10b-46e0-bf77-a2bfb16a6add; 131655666550000000</span><span class="sxs-lookup"><span data-stu-id="6feb8-118">This command gets the backup with name 601061b7-d10b-46e0-bf77-a2bfb16a6add;131655666550000000</span></span>

### <span data-ttu-id="6feb8-119">Exempel 3: Hämta alla långsiktiga säkerhets kopior för en databas</span><span class="sxs-lookup"><span data-stu-id="6feb8-119">Example 3: Get all long term retention backups for a database</span></span>
```powershell
PS C:\> Get-AzureRmSqlDatabase -ResourceGroupName resourcegroup01 -ServerName server01 -DatabaseName database01 | Get-AzureRmSqlDatabaseLongTermRetentionBackup


BackupExpirationTime : 3/22/2018 5:50:55 AM
BackupName           : 601061b7-d10b-46e0-bf77-a2bfb16a6add;131655666550000000
BackupTime           : 3/15/2018 5:50:55 AM
DatabaseName         : database01
DatabaseDeletionTime :
Location         : northeurope
ResourceId           : /subscriptions/371edd6d-9630-4558-a7bd-ee139498e6a1/providers/Microsoft.Sql/locations/northeurope/longTermRetentionServers/server01/longTermRetentionDatabases/database01/longTermRetentionBackups/601061b7-d10b-46e0-bf77-a2bfb16a6add;131655666550000000
ServerName           : server01
ServerCreateTime     : 2/29/2018 12:12:19 AM
```

<span data-ttu-id="6feb8-120">Det här kommandot får alla säkerhets kopior på lång sikt för database01</span><span class="sxs-lookup"><span data-stu-id="6feb8-120">This command gets all long term retention backups for database01</span></span>

## <span data-ttu-id="6feb8-121">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="6feb8-121">PARAMETERS</span></span>

### <span data-ttu-id="6feb8-122">-BackupName</span><span class="sxs-lookup"><span data-stu-id="6feb8-122">-BackupName</span></span>
<span data-ttu-id="6feb8-123">Namnet på säkerhets kopian.</span><span class="sxs-lookup"><span data-stu-id="6feb8-123">The name of the backup.</span></span>

```yaml
Type: String
Parameter Sets: BackupName, GetBackupByResourceId, GetBackupByInputObject
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6feb8-124">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="6feb8-124">-DatabaseName</span></span>
<span data-ttu-id="6feb8-125">Namnet på den Azure SQL-databas som säkerhets kopian kommer från.</span><span class="sxs-lookup"><span data-stu-id="6feb8-125">The name of the Azure SQL Database the backup is from.</span></span>

```yaml
Type: String
Parameter Sets: ServerName
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: BackupName
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6feb8-126">-DatabaseState</span><span class="sxs-lookup"><span data-stu-id="6feb8-126">-DatabaseState</span></span>
<span data-ttu-id="6feb8-127">Tillståndet för den databas vars säkerhets kopior du vill hitta, använda, ta bort eller alla.</span><span class="sxs-lookup"><span data-stu-id="6feb8-127">The state of the database whose backups you want to find, Alive, Deleted, or All.</span></span>
<span data-ttu-id="6feb8-128">Standardvärden för alla</span><span class="sxs-lookup"><span data-stu-id="6feb8-128">Defaults to All</span></span>

```yaml
Type: String
Parameter Sets: Location, ServerName, GetBackupsByResourceId, GetBackupsByInputObject
Aliases:
Accepted values: All, Deleted, Live

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6feb8-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6feb8-129">-DefaultProfile</span></span>
<span data-ttu-id="6feb8-130">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="6feb8-130">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6feb8-131">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6feb8-131">-InputObject</span></span>
<span data-ttu-id="6feb8-132">Databasobjektet för att hämta säkerhets kopior.</span><span class="sxs-lookup"><span data-stu-id="6feb8-132">The database object to get backups for.</span></span>

```yaml
Type: AzureSqlDatabaseModel
Parameter Sets: GetBackupByInputObject, GetBackupsByInputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6feb8-133">-Plats</span><span class="sxs-lookup"><span data-stu-id="6feb8-133">-Location</span></span>
<span data-ttu-id="6feb8-134">Platsen för säkerhets kopiornas käll Server.</span><span class="sxs-lookup"><span data-stu-id="6feb8-134">The location of the backups' source server.</span></span>

```yaml
Type: String
Parameter Sets: Location, ServerName, BackupName, GetBackupByResourceId, GetBackupsByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6feb8-135">-OnlyLatestPerDatabase</span><span class="sxs-lookup"><span data-stu-id="6feb8-135">-OnlyLatestPerDatabase</span></span>
<span data-ttu-id="6feb8-136">Om du vill få den senaste säkerhets kopian per databas eller inte.</span><span class="sxs-lookup"><span data-stu-id="6feb8-136">Whether or not to only get the latest backup per database.</span></span>
<span data-ttu-id="6feb8-137">Standardvärdet är falskt.</span><span class="sxs-lookup"><span data-stu-id="6feb8-137">Defaults to false.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: Location, ServerName, GetBackupsByResourceId, GetBackupsByInputObject
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6feb8-138">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="6feb8-138">-ResourceId</span></span>
<span data-ttu-id="6feb8-139">Databas resurs-ID som du kan använda för att hämta säkerhets kopior för.</span><span class="sxs-lookup"><span data-stu-id="6feb8-139">The database Resource ID to get backups for.</span></span>

```yaml
Type: String
Parameter Sets: GetBackupByResourceId, GetBackupsByResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6feb8-140">-ServerName</span><span class="sxs-lookup"><span data-stu-id="6feb8-140">-ServerName</span></span>
<span data-ttu-id="6feb8-141">Namnet på Azure SQL-servern som säkerhets kopiorna är under.</span><span class="sxs-lookup"><span data-stu-id="6feb8-141">The name of the Azure SQL Server the backups are under.</span></span>

```yaml
Type: String
Parameter Sets: ServerName, BackupName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6feb8-142">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="6feb8-142">-Confirm</span></span>
<span data-ttu-id="6feb8-143">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="6feb8-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6feb8-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6feb8-144">-WhatIf</span></span>
<span data-ttu-id="6feb8-145">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="6feb8-145">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6feb8-146">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="6feb8-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6feb8-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6feb8-147">CommonParameters</span></span>
<span data-ttu-id="6feb8-148">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6feb8-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="6feb8-149">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6feb8-149">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6feb8-150">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="6feb8-150">INPUTS</span></span>

### <span data-ttu-id="6feb8-151">System. String</span><span class="sxs-lookup"><span data-stu-id="6feb8-151">System.String</span></span>
<span data-ttu-id="6feb8-152">Microsoft. Azure. commands. SQL. Database. Model. AzureSqlDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="6feb8-152">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span></span>

## <span data-ttu-id="6feb8-153">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="6feb8-153">OUTPUTS</span></span>

### <span data-ttu-id="6feb8-154">Microsoft. Azure. commands. SQL. backup. Model. AzureSqlDatabaseLongTermRetentionBackupModel</span><span class="sxs-lookup"><span data-stu-id="6feb8-154">Microsoft.Azure.Commands.Sql.Backup.Model.AzureSqlDatabaseLongTermRetentionBackupModel</span></span>

## <span data-ttu-id="6feb8-155">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="6feb8-155">NOTES</span></span>

## <span data-ttu-id="6feb8-156">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="6feb8-156">RELATED LINKS</span></span>

[<span data-ttu-id="6feb8-157">Remove-AzureRmSqlDatabaseLongTermRetentionBackup</span><span class="sxs-lookup"><span data-stu-id="6feb8-157">Remove-AzureRmSqlDatabaseLongTermRetentionBackup</span></span>](./Remove-AzureRmSqlDatabaseLongTermRetentionBackup.md)

[<span data-ttu-id="6feb8-158">Get-AzureRmSqlDatabaseBackupLongTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="6feb8-158">Get-AzureRmSqlDatabaseBackupLongTermRetentionPolicy</span></span>](./Get-AzureRmSqlDatabaseBackupLongTermRetentionPolicy.md)

[<span data-ttu-id="6feb8-159">Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="6feb8-159">Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy</span></span>](./Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy.md)

[<span data-ttu-id="6feb8-160">Dokumentation för SQL-databaser</span><span class="sxs-lookup"><span data-stu-id="6feb8-160">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
