---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/remove-azurermsqldatalongtermretentionbackup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlDatabaseLongTermRetentionBackup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlDatabaseLongTermRetentionBackup.md
ms.openlocfilehash: 93895a7fffe40309b73c3929f88ffebfe203767f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93581927"
---
# <span data-ttu-id="ac3b9-101">Remove-AzureRmSqlDatabaseLongTermRetentionBackup</span><span class="sxs-lookup"><span data-stu-id="ac3b9-101">Remove-AzureRmSqlDatabaseLongTermRetentionBackup</span></span>

## <span data-ttu-id="ac3b9-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="ac3b9-102">SYNOPSIS</span></span>
<span data-ttu-id="ac3b9-103">Tar bort en långsiktig säkerhets kopiering.</span><span class="sxs-lookup"><span data-stu-id="ac3b9-103">Deletes a long term retention backup.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ac3b9-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="ac3b9-104">SYNTAX</span></span>

### <span data-ttu-id="ac3b9-105">RemoveBackupDefault (standard)</span><span class="sxs-lookup"><span data-stu-id="ac3b9-105">RemoveBackupDefault (Default)</span></span>
```
Remove-AzureRmSqlDatabaseLongTermRetentionBackup -Location <String> [-ServerName] <String>
 [-DatabaseName] <String> [-BackupName] <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ac3b9-106">RemoveBackupByInputObject</span><span class="sxs-lookup"><span data-stu-id="ac3b9-106">RemoveBackupByInputObject</span></span>
```
Remove-AzureRmSqlDatabaseLongTermRetentionBackup [-InputObject] <AzureSqlDatabaseLongTermRetentionBackupModel>
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ac3b9-107">RemoveBackupByResourceId</span><span class="sxs-lookup"><span data-stu-id="ac3b9-107">RemoveBackupByResourceId</span></span>
```
Remove-AzureRmSqlDatabaseLongTermRetentionBackup [-ResourceId] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ac3b9-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="ac3b9-108">DESCRIPTION</span></span>
<span data-ttu-id="ac3b9-109">Cmdleten **Remove-AzureRmSqlDatabaseLongTermRetentionBackup** tar bort den angivna säkerhets kopian.</span><span class="sxs-lookup"><span data-stu-id="ac3b9-109">The **Remove-AzureRmSqlDatabaseLongTermRetentionBackup** cmdlet deletes the backup specified.</span></span>

## <span data-ttu-id="ac3b9-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="ac3b9-110">EXAMPLES</span></span>

### <span data-ttu-id="ac3b9-111">Exempel 1: ta bort en enda säkerhets kopia</span><span class="sxs-lookup"><span data-stu-id="ac3b9-111">Example 1: Delete a single backup</span></span>
```powershell
PS C:\> Remove-AzureRmSqlDatabaseLongTermRetentionBackup -Location northeurope -ServerName server01 -DatabaseName database01 -BackupName "601061b7-d10b-46e0-bf77-a2bfb16a6add;131655666550000000"


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

<span data-ttu-id="ac3b9-112">Tar bort säkerhets kopian med namnet 601061b7-d10b-46e0-bf77-a2bfb16a6add; 131655666550000000</span><span class="sxs-lookup"><span data-stu-id="ac3b9-112">Deletes the backup with name 601061b7-d10b-46e0-bf77-a2bfb16a6add;131655666550000000</span></span>

### <span data-ttu-id="ac3b9-113">Exempel 2: ta bort alla säkerhets kopior för en plats</span><span class="sxs-lookup"><span data-stu-id="ac3b9-113">Example 2: Delete all backups for a location</span></span>
```powershell
PS C:\> Get-AzureRmSqlDatabaseLongTermRetentionBackup -Location northeurope | Remove-AzureRmSqlDatabaseLongTermRetentionBackup


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

<span data-ttu-id="ac3b9-114">Det här kommandot tar bort alla säkerhets kopior för den northeurope platsen.</span><span class="sxs-lookup"><span data-stu-id="ac3b9-114">This command deletes all long term retention backups for the northeurope location.</span></span>

## <span data-ttu-id="ac3b9-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="ac3b9-115">PARAMETERS</span></span>

### <span data-ttu-id="ac3b9-116">-BackupName</span><span class="sxs-lookup"><span data-stu-id="ac3b9-116">-BackupName</span></span>
<span data-ttu-id="ac3b9-117">Namnet på säkerhets kopian.</span><span class="sxs-lookup"><span data-stu-id="ac3b9-117">The name of the backup.</span></span>

```yaml
Type: String
Parameter Sets: RemoveBackupDefault
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ac3b9-118">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="ac3b9-118">-DatabaseName</span></span>
<span data-ttu-id="ac3b9-119">Namnet på den Azure SQL-databas som säkerhets kopian kommer från.</span><span class="sxs-lookup"><span data-stu-id="ac3b9-119">The name of the Azure SQL Database the backup is from.</span></span>

```yaml
Type: String
Parameter Sets: RemoveBackupDefault
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ac3b9-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ac3b9-120">-DefaultProfile</span></span>
<span data-ttu-id="ac3b9-121">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="ac3b9-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ac3b9-122">-Force</span><span class="sxs-lookup"><span data-stu-id="ac3b9-122">-Force</span></span>
<span data-ttu-id="ac3b9-123">Hoppa över bekräftelse meddelande för att utföra åtgärden</span><span class="sxs-lookup"><span data-stu-id="ac3b9-123">Skip confirmation message for performing the action</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ac3b9-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ac3b9-124">-InputObject</span></span>
<span data-ttu-id="ac3b9-125">Databasens säkerhets kopie rad lagrings objekt som ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="ac3b9-125">The Database Long Term Retention Backup object to remove.</span></span>

```yaml
Type: AzureSqlDatabaseLongTermRetentionBackupModel
Parameter Sets: RemoveBackupByInputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ac3b9-126">-Plats</span><span class="sxs-lookup"><span data-stu-id="ac3b9-126">-Location</span></span>
<span data-ttu-id="ac3b9-127">Platsen för säkerhets kopiornas käll Server.</span><span class="sxs-lookup"><span data-stu-id="ac3b9-127">The location of the backups' source server.</span></span>

```yaml
Type: String
Parameter Sets: RemoveBackupDefault
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ac3b9-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ac3b9-128">-ResourceId</span></span>
<span data-ttu-id="ac3b9-129">Resurs-ID för databasens tids lagrings säkerhets kopia som tas bort.</span><span class="sxs-lookup"><span data-stu-id="ac3b9-129">The Resource ID of the Database Long Term Retention Backup to remove.</span></span>

```yaml
Type: String
Parameter Sets: RemoveBackupByResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ac3b9-130">-ServerName</span><span class="sxs-lookup"><span data-stu-id="ac3b9-130">-ServerName</span></span>
<span data-ttu-id="ac3b9-131">Namnet på Azure SQL-servern som säkerhets kopian finns under.</span><span class="sxs-lookup"><span data-stu-id="ac3b9-131">The name of the Azure SQL Server the backup is under.</span></span>

```yaml
Type: String
Parameter Sets: RemoveBackupDefault
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ac3b9-132">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="ac3b9-132">-Confirm</span></span>
<span data-ttu-id="ac3b9-133">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="ac3b9-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ac3b9-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ac3b9-134">-WhatIf</span></span>
<span data-ttu-id="ac3b9-135">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="ac3b9-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ac3b9-136">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="ac3b9-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ac3b9-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ac3b9-137">CommonParameters</span></span>
<span data-ttu-id="ac3b9-138">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ac3b9-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="ac3b9-139">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ac3b9-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ac3b9-140">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="ac3b9-140">INPUTS</span></span>

### <span data-ttu-id="ac3b9-141">System. String</span><span class="sxs-lookup"><span data-stu-id="ac3b9-141">System.String</span></span>
<span data-ttu-id="ac3b9-142">Microsoft. Azure. commands. SQL. backup. Model. AzureSqlDatabaseLongTermRetentionBackupModel</span><span class="sxs-lookup"><span data-stu-id="ac3b9-142">Microsoft.Azure.Commands.Sql.Backup.Model.AzureSqlDatabaseLongTermRetentionBackupModel</span></span>

## <span data-ttu-id="ac3b9-143">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="ac3b9-143">OUTPUTS</span></span>

### <span data-ttu-id="ac3b9-144">Microsoft. Azure. commands. SQL. backup. Model. AzureSqlDatabaseLongTermRetentionBackupModel</span><span class="sxs-lookup"><span data-stu-id="ac3b9-144">Microsoft.Azure.Commands.Sql.Backup.Model.AzureSqlDatabaseLongTermRetentionBackupModel</span></span>

## <span data-ttu-id="ac3b9-145">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="ac3b9-145">NOTES</span></span>

## <span data-ttu-id="ac3b9-146">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="ac3b9-146">RELATED LINKS</span></span>

[<span data-ttu-id="ac3b9-147">Get-AzureRmSqlDatabaseLongTermRetentionBackup</span><span class="sxs-lookup"><span data-stu-id="ac3b9-147">Get-AzureRmSqlDatabaseLongTermRetentionBackup</span></span>](./Get-AzureRmSqlDatabaseLongTermRetentionBackup.md)

[<span data-ttu-id="ac3b9-148">Get-AzureRmSqlDatabaseBackupLongTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="ac3b9-148">Get-AzureRmSqlDatabaseBackupLongTermRetentionPolicy</span></span>](./Get-AzureRmSqlDatabaseBackupLongTermRetentionPolicy.md)

[<span data-ttu-id="ac3b9-149">Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="ac3b9-149">Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy</span></span>](./Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy.md)

[<span data-ttu-id="ac3b9-150">Dokumentation för SQL-databaser</span><span class="sxs-lookup"><span data-stu-id="ac3b9-150">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
