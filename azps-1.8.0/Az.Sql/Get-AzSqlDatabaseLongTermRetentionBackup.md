---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqldatabaselongtermretentionbackup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseLongTermRetentionBackup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseLongTermRetentionBackup.md
ms.openlocfilehash: 593a9c4764afd70003ee5c807be069eff977c6e5
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93746749"
---
# <span data-ttu-id="cc1d1-101">Get-AzSqlDatabaseLongTermRetentionBackup</span><span class="sxs-lookup"><span data-stu-id="cc1d1-101">Get-AzSqlDatabaseLongTermRetentionBackup</span></span>

## <span data-ttu-id="cc1d1-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="cc1d1-102">SYNOPSIS</span></span>
<span data-ttu-id="cc1d1-103">Hämtar en eller flera säkerhets kopior för längre tid.</span><span class="sxs-lookup"><span data-stu-id="cc1d1-103">Gets one or more long term retention backups.</span></span>

## <span data-ttu-id="cc1d1-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="cc1d1-104">SYNTAX</span></span>

### <span data-ttu-id="cc1d1-105">Plats (standard)</span><span class="sxs-lookup"><span data-stu-id="cc1d1-105">Location (Default)</span></span>
```
Get-AzSqlDatabaseLongTermRetentionBackup [-Location] <String> [-OnlyLatestPerDatabase]
 [-DatabaseState <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cc1d1-106">ServerName</span><span class="sxs-lookup"><span data-stu-id="cc1d1-106">ServerName</span></span>
```
Get-AzSqlDatabaseLongTermRetentionBackup [-Location] <String> [-ServerName] <String> [-DatabaseName <String>]
 [-OnlyLatestPerDatabase] [-DatabaseState <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cc1d1-107">BackupName</span><span class="sxs-lookup"><span data-stu-id="cc1d1-107">BackupName</span></span>
```
Get-AzSqlDatabaseLongTermRetentionBackup [-Location] <String> [-ServerName] <String> -DatabaseName <String>
 [-BackupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cc1d1-108">GetBackupByResourceId</span><span class="sxs-lookup"><span data-stu-id="cc1d1-108">GetBackupByResourceId</span></span>
```
Get-AzSqlDatabaseLongTermRetentionBackup [-Location] <String> [-ResourceId] <String> [-BackupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cc1d1-109">GetBackupsByResourceId</span><span class="sxs-lookup"><span data-stu-id="cc1d1-109">GetBackupsByResourceId</span></span>
```
Get-AzSqlDatabaseLongTermRetentionBackup [-Location] <String> [-ResourceId] <String> [-OnlyLatestPerDatabase]
 [-DatabaseState <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cc1d1-110">GetBackupByInputObject</span><span class="sxs-lookup"><span data-stu-id="cc1d1-110">GetBackupByInputObject</span></span>
```
Get-AzSqlDatabaseLongTermRetentionBackup [-InputObject] <AzureSqlDatabaseModel> [-BackupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cc1d1-111">GetBackupsByInputObject</span><span class="sxs-lookup"><span data-stu-id="cc1d1-111">GetBackupsByInputObject</span></span>
```
Get-AzSqlDatabaseLongTermRetentionBackup [-InputObject] <AzureSqlDatabaseModel> [-OnlyLatestPerDatabase]
 [-DatabaseState <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cc1d1-112">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="cc1d1-112">DESCRIPTION</span></span>
<span data-ttu-id="cc1d1-113">Cmdleten **Get-AzSqlDatabaseLongTermRetentionBackup** alla säkerhets kopior för en lagrings plats, server eller databas eller en särskild säkerhets kopia av den långsiktiga tids perioden.</span><span class="sxs-lookup"><span data-stu-id="cc1d1-113">The **Get-AzSqlDatabaseLongTermRetentionBackup** cmdlet gets all long term retention backups for a location, server, or database or gets a specific long term retention backup.</span></span>

## <span data-ttu-id="cc1d1-114">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="cc1d1-114">EXAMPLES</span></span>

### <span data-ttu-id="cc1d1-115">Exempel 1: Hämta alla säkerhets kopior för en plats</span><span class="sxs-lookup"><span data-stu-id="cc1d1-115">Example 1: Get all backups for a location</span></span>
```powershell
PS C:\> Get-AzSqlDatabaseLongTermRetentionBackup -Location northeurope


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

<span data-ttu-id="cc1d1-116">Med det här kommandot får du säkerhets kopior för alla databaser (som kan vara levande eller borttagna) i northeurope.</span><span class="sxs-lookup"><span data-stu-id="cc1d1-116">This command gets all long term retention backups for all databases (which may be alive or deleted) in northeurope.</span></span>

### <span data-ttu-id="cc1d1-117">Exempel 2: skaffa en särskild säkerhets kopia för långsiktigt bevarande</span><span class="sxs-lookup"><span data-stu-id="cc1d1-117">Example 2: Get a specific long term retention backup</span></span>
```powershell
PS C:\> Get-AzSqlDatabaseLongTermRetentionBackup -Location northeurope -ServerName server01 -DatabaseName database01 -BackupName "601061b7-d10b-46e0-bf77-a2bfb16a6add;131655666550000000"


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

<span data-ttu-id="cc1d1-118">Det här kommandot får säkerhets kopian med namnet 601061b7-d10b-46e0-bf77-a2bfb16a6add; 131655666550000000</span><span class="sxs-lookup"><span data-stu-id="cc1d1-118">This command gets the backup with name 601061b7-d10b-46e0-bf77-a2bfb16a6add;131655666550000000</span></span>

### <span data-ttu-id="cc1d1-119">Exempel 3: Hämta alla långsiktiga säkerhets kopior för en databas</span><span class="sxs-lookup"><span data-stu-id="cc1d1-119">Example 3: Get all long term retention backups for a database</span></span>
```powershell
PS C:\> Get-AzSqlDatabase -ResourceGroupName resourcegroup01 -ServerName server01 -DatabaseName database01 | Get-AzSqlDatabaseLongTermRetentionBackup


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

<span data-ttu-id="cc1d1-120">Det här kommandot får alla säkerhets kopior på lång sikt för database01</span><span class="sxs-lookup"><span data-stu-id="cc1d1-120">This command gets all long term retention backups for database01</span></span>

### <span data-ttu-id="cc1d1-121">Exempel 4: få säkerhets kopior på lång sikt med filtrering</span><span class="sxs-lookup"><span data-stu-id="cc1d1-121">Example 4: Get long term retention backups using filtering</span></span>
```powershell
PS C:\> Get-AzSqlDatabaseLongTermRetentionBackup -Location northeurope -ServerName server01 -DatabaseName database01 -BackupName "601061b7*"

BackupExpirationTime : 3/22/2018 11:43:18 PM
BackupName           : 601061b7-164c-4a4a-88e5-7158d092d503;131656309980000000
BackupTime           : 3/15/2018 11:43:18 PM
DatabaseName         : database02
DatabaseDeletionTime : 3/18/2018 4:36:00 PM
Location         : northeurope
ResourceId           : /subscriptions/371edd6d-9630-4558-a7bd-ee139498e6a1/providers/Microsoft.Sql/locations/northeurope/longTermRetentionServers/server02/longTermRetentionDatabases/database02/longTermRetentionBackups/601061b7-164c-4a4a-88e5-7158d092d503;131656309980000000
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

<span data-ttu-id="cc1d1-122">Det här kommandot får alla säkerhets kopior med namn som börjar med "601061b7"</span><span class="sxs-lookup"><span data-stu-id="cc1d1-122">This command gets all backups with name that starts with "601061b7"</span></span>

## <span data-ttu-id="cc1d1-123">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="cc1d1-123">PARAMETERS</span></span>

### <span data-ttu-id="cc1d1-124">-BackupName</span><span class="sxs-lookup"><span data-stu-id="cc1d1-124">-BackupName</span></span>
<span data-ttu-id="cc1d1-125">Namnet på säkerhets kopian.</span><span class="sxs-lookup"><span data-stu-id="cc1d1-125">The name of the backup.</span></span>

```yaml
Type: System.String
Parameter Sets: BackupName, GetBackupByResourceId, GetBackupByInputObject
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="cc1d1-126">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="cc1d1-126">-DatabaseName</span></span>
<span data-ttu-id="cc1d1-127">Namnet på den Azure SQL-databas som säkerhets kopian kommer från.</span><span class="sxs-lookup"><span data-stu-id="cc1d1-127">The name of the Azure SQL Database the backup is from.</span></span>

```yaml
Type: System.String
Parameter Sets: ServerName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: BackupName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cc1d1-128">-DatabaseState</span><span class="sxs-lookup"><span data-stu-id="cc1d1-128">-DatabaseState</span></span>
<span data-ttu-id="cc1d1-129">Tillståndet för den databas vars säkerhets kopior du vill hitta, använda, ta bort eller alla.</span><span class="sxs-lookup"><span data-stu-id="cc1d1-129">The state of the database whose backups you want to find, Alive, Deleted, or All.</span></span>
<span data-ttu-id="cc1d1-130">Standardvärden för alla</span><span class="sxs-lookup"><span data-stu-id="cc1d1-130">Defaults to All</span></span>

```yaml
Type: System.String
Parameter Sets: Location, ServerName, GetBackupsByResourceId, GetBackupsByInputObject
Aliases:
Accepted values: All, Deleted, Live

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cc1d1-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cc1d1-131">-DefaultProfile</span></span>
<span data-ttu-id="cc1d1-132">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="cc1d1-132">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cc1d1-133">-InputObject</span><span class="sxs-lookup"><span data-stu-id="cc1d1-133">-InputObject</span></span>
<span data-ttu-id="cc1d1-134">Databasobjektet för att hämta säkerhets kopior.</span><span class="sxs-lookup"><span data-stu-id="cc1d1-134">The database object to get backups for.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel
Parameter Sets: GetBackupByInputObject, GetBackupsByInputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="cc1d1-135">-Plats</span><span class="sxs-lookup"><span data-stu-id="cc1d1-135">-Location</span></span>
<span data-ttu-id="cc1d1-136">Platsen för säkerhets kopiornas käll Server.</span><span class="sxs-lookup"><span data-stu-id="cc1d1-136">The location of the backups' source server.</span></span>

```yaml
Type: System.String
Parameter Sets: Location, ServerName, BackupName, GetBackupByResourceId, GetBackupsByResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cc1d1-137">-OnlyLatestPerDatabase</span><span class="sxs-lookup"><span data-stu-id="cc1d1-137">-OnlyLatestPerDatabase</span></span>
<span data-ttu-id="cc1d1-138">Om du vill få den senaste säkerhets kopian per databas eller inte.</span><span class="sxs-lookup"><span data-stu-id="cc1d1-138">Whether or not to only get the latest backup per database.</span></span>
<span data-ttu-id="cc1d1-139">Standardvärdet är falskt.</span><span class="sxs-lookup"><span data-stu-id="cc1d1-139">Defaults to false.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Location, ServerName, GetBackupsByResourceId, GetBackupsByInputObject
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cc1d1-140">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="cc1d1-140">-ResourceId</span></span>
<span data-ttu-id="cc1d1-141">Databas resurs-ID som du kan använda för att hämta säkerhets kopior för.</span><span class="sxs-lookup"><span data-stu-id="cc1d1-141">The database Resource ID to get backups for.</span></span>

```yaml
Type: System.String
Parameter Sets: GetBackupByResourceId, GetBackupsByResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cc1d1-142">-ServerName</span><span class="sxs-lookup"><span data-stu-id="cc1d1-142">-ServerName</span></span>
<span data-ttu-id="cc1d1-143">Namnet på Azure SQL-servern som säkerhets kopiorna är under.</span><span class="sxs-lookup"><span data-stu-id="cc1d1-143">The name of the Azure SQL Server the backups are under.</span></span>

```yaml
Type: System.String
Parameter Sets: ServerName, BackupName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cc1d1-144">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="cc1d1-144">-Confirm</span></span>
<span data-ttu-id="cc1d1-145">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="cc1d1-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cc1d1-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cc1d1-146">-WhatIf</span></span>
<span data-ttu-id="cc1d1-147">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="cc1d1-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cc1d1-148">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="cc1d1-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cc1d1-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cc1d1-149">CommonParameters</span></span>
<span data-ttu-id="cc1d1-150">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cc1d1-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cc1d1-151">Mer information finns i [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="cc1d1-151">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cc1d1-152">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="cc1d1-152">INPUTS</span></span>

### <span data-ttu-id="cc1d1-153">Microsoft. Azure. commands. SQL. Database. Model. AzureSqlDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="cc1d1-153">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span></span>

### <span data-ttu-id="cc1d1-154">System. String</span><span class="sxs-lookup"><span data-stu-id="cc1d1-154">System.String</span></span>

## <span data-ttu-id="cc1d1-155">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="cc1d1-155">OUTPUTS</span></span>

### <span data-ttu-id="cc1d1-156">Microsoft. Azure. commands. SQL. backup. Model. AzureSqlDatabaseLongTermRetentionBackupModel</span><span class="sxs-lookup"><span data-stu-id="cc1d1-156">Microsoft.Azure.Commands.Sql.Backup.Model.AzureSqlDatabaseLongTermRetentionBackupModel</span></span>

## <span data-ttu-id="cc1d1-157">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="cc1d1-157">NOTES</span></span>

## <span data-ttu-id="cc1d1-158">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="cc1d1-158">RELATED LINKS</span></span>

[<span data-ttu-id="cc1d1-159">Remove-AzSqlDatabaseLongTermRetentionBackup</span><span class="sxs-lookup"><span data-stu-id="cc1d1-159">Remove-AzSqlDatabaseLongTermRetentionBackup</span></span>](./Remove-AzSqlDatabaseLongTermRetentionBackup.md)

[<span data-ttu-id="cc1d1-160">Get-AzSqlDatabaseBackupLongTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="cc1d1-160">Get-AzSqlDatabaseBackupLongTermRetentionPolicy</span></span>](./Get-AzSqlDatabaseBackupLongTermRetentionPolicy.md)

[<span data-ttu-id="cc1d1-161">Set-AzSqlDatabaseBackupLongTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="cc1d1-161">Set-AzSqlDatabaseBackupLongTermRetentionPolicy</span></span>](./Set-AzSqlDatabaseBackupLongTermRetentionPolicy.md)

[<span data-ttu-id="cc1d1-162">Dokumentation för SQL-databaser</span><span class="sxs-lookup"><span data-stu-id="cc1d1-162">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)