---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/remove-azsqldatabaselongtermretentionbackup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlDatabaseLongTermRetentionBackup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlDatabaseLongTermRetentionBackup.md
ms.openlocfilehash: 8fd76e227951afefcbb8f7b04cf4ae3616ef5ef7
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93746584"
---
# <span data-ttu-id="8a766-101">Remove-AzSqlDatabaseLongTermRetentionBackup</span><span class="sxs-lookup"><span data-stu-id="8a766-101">Remove-AzSqlDatabaseLongTermRetentionBackup</span></span>

## <span data-ttu-id="8a766-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="8a766-102">SYNOPSIS</span></span>
<span data-ttu-id="8a766-103">Tar bort en långsiktig säkerhets kopiering.</span><span class="sxs-lookup"><span data-stu-id="8a766-103">Deletes a long term retention backup.</span></span>

## <span data-ttu-id="8a766-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="8a766-104">SYNTAX</span></span>

### <span data-ttu-id="8a766-105">RemoveBackupDefault (standard)</span><span class="sxs-lookup"><span data-stu-id="8a766-105">RemoveBackupDefault (Default)</span></span>
```
Remove-AzSqlDatabaseLongTermRetentionBackup [-Location] <String> [-ServerName] <String>
 [-DatabaseName] <String> [-BackupName] <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8a766-106">RemoveBackupByInputObject</span><span class="sxs-lookup"><span data-stu-id="8a766-106">RemoveBackupByInputObject</span></span>
```
Remove-AzSqlDatabaseLongTermRetentionBackup [-InputObject] <AzureSqlDatabaseLongTermRetentionBackupModel>
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8a766-107">RemoveBackupByResourceId</span><span class="sxs-lookup"><span data-stu-id="8a766-107">RemoveBackupByResourceId</span></span>
```
Remove-AzSqlDatabaseLongTermRetentionBackup [-ResourceId] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8a766-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="8a766-108">DESCRIPTION</span></span>
<span data-ttu-id="8a766-109">Cmdleten **Remove-AzSqlDatabaseLongTermRetentionBackup** tar bort den angivna säkerhets kopian.</span><span class="sxs-lookup"><span data-stu-id="8a766-109">The **Remove-AzSqlDatabaseLongTermRetentionBackup** cmdlet deletes the backup specified.</span></span>

## <span data-ttu-id="8a766-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="8a766-110">EXAMPLES</span></span>

### <span data-ttu-id="8a766-111">Exempel 1: ta bort en enda säkerhets kopia</span><span class="sxs-lookup"><span data-stu-id="8a766-111">Example 1: Delete a single backup</span></span>
```powershell
PS C:\> Remove-AzSqlDatabaseLongTermRetentionBackup -Location northeurope -ServerName server01 -DatabaseName database01 -BackupName "601061b7-d10b-46e0-bf77-a2bfb16a6add;131655666550000000"


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

<span data-ttu-id="8a766-112">Tar bort säkerhets kopian med namnet 601061b7-d10b-46e0-bf77-a2bfb16a6add; 131655666550000000</span><span class="sxs-lookup"><span data-stu-id="8a766-112">Deletes the backup with name 601061b7-d10b-46e0-bf77-a2bfb16a6add;131655666550000000</span></span>

### <span data-ttu-id="8a766-113">Exempel 2: ta bort alla säkerhets kopior för en plats</span><span class="sxs-lookup"><span data-stu-id="8a766-113">Example 2: Delete all backups for a location</span></span>
```powershell
PS C:\> Get-AzSqlDatabaseLongTermRetentionBackup -Location northeurope | Remove-AzSqlDatabaseLongTermRetentionBackup


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

<span data-ttu-id="8a766-114">Det här kommandot tar bort alla säkerhets kopior för den northeurope platsen.</span><span class="sxs-lookup"><span data-stu-id="8a766-114">This command deletes all long term retention backups for the northeurope location.</span></span>

## <span data-ttu-id="8a766-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="8a766-115">PARAMETERS</span></span>

### <span data-ttu-id="8a766-116">-BackupName</span><span class="sxs-lookup"><span data-stu-id="8a766-116">-BackupName</span></span>
<span data-ttu-id="8a766-117">Namnet på säkerhets kopian.</span><span class="sxs-lookup"><span data-stu-id="8a766-117">The name of the backup.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveBackupDefault
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8a766-118">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="8a766-118">-DatabaseName</span></span>
<span data-ttu-id="8a766-119">Namnet på den Azure SQL-databas som säkerhets kopian kommer från.</span><span class="sxs-lookup"><span data-stu-id="8a766-119">The name of the Azure SQL Database the backup is from.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveBackupDefault
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8a766-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8a766-120">-DefaultProfile</span></span>
<span data-ttu-id="8a766-121">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="8a766-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8a766-122">-Force</span><span class="sxs-lookup"><span data-stu-id="8a766-122">-Force</span></span>
<span data-ttu-id="8a766-123">Hoppa över bekräftelse meddelande för att utföra åtgärden</span><span class="sxs-lookup"><span data-stu-id="8a766-123">Skip confirmation message for performing the action</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8a766-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8a766-124">-InputObject</span></span>
<span data-ttu-id="8a766-125">Databasens säkerhets kopie rad lagrings objekt som ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="8a766-125">The Database Long Term Retention Backup object to remove.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.Backup.Model.AzureSqlDatabaseLongTermRetentionBackupModel
Parameter Sets: RemoveBackupByInputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8a766-126">-Plats</span><span class="sxs-lookup"><span data-stu-id="8a766-126">-Location</span></span>
<span data-ttu-id="8a766-127">Platsen för säkerhets kopiornas käll Server.</span><span class="sxs-lookup"><span data-stu-id="8a766-127">The location of the backups' source server.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveBackupDefault
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8a766-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8a766-128">-ResourceId</span></span>
<span data-ttu-id="8a766-129">Resurs-ID för databasens tids lagrings säkerhets kopia som tas bort.</span><span class="sxs-lookup"><span data-stu-id="8a766-129">The Resource ID of the Database Long Term Retention Backup to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveBackupByResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8a766-130">-ServerName</span><span class="sxs-lookup"><span data-stu-id="8a766-130">-ServerName</span></span>
<span data-ttu-id="8a766-131">Namnet på Azure SQL-servern som säkerhets kopian finns under.</span><span class="sxs-lookup"><span data-stu-id="8a766-131">The name of the Azure SQL Server the backup is under.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveBackupDefault
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8a766-132">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="8a766-132">-Confirm</span></span>
<span data-ttu-id="8a766-133">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="8a766-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8a766-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8a766-134">-WhatIf</span></span>
<span data-ttu-id="8a766-135">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="8a766-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8a766-136">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="8a766-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8a766-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8a766-137">CommonParameters</span></span>
<span data-ttu-id="8a766-138">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8a766-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8a766-139">Mer information finns i [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8a766-139">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8a766-140">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="8a766-140">INPUTS</span></span>

### <span data-ttu-id="8a766-141">System. String</span><span class="sxs-lookup"><span data-stu-id="8a766-141">System.String</span></span>

## <span data-ttu-id="8a766-142">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="8a766-142">OUTPUTS</span></span>

### <span data-ttu-id="8a766-143">Microsoft. Azure. commands. SQL. backup. Model. AzureSqlDatabaseLongTermRetentionBackupModel</span><span class="sxs-lookup"><span data-stu-id="8a766-143">Microsoft.Azure.Commands.Sql.Backup.Model.AzureSqlDatabaseLongTermRetentionBackupModel</span></span>

## <span data-ttu-id="8a766-144">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="8a766-144">NOTES</span></span>

## <span data-ttu-id="8a766-145">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="8a766-145">RELATED LINKS</span></span>

[<span data-ttu-id="8a766-146">Get-AzSqlDatabaseLongTermRetentionBackup</span><span class="sxs-lookup"><span data-stu-id="8a766-146">Get-AzSqlDatabaseLongTermRetentionBackup</span></span>](./Get-AzSqlDatabaseLongTermRetentionBackup.md)

[<span data-ttu-id="8a766-147">Get-AzSqlDatabaseBackupLongTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="8a766-147">Get-AzSqlDatabaseBackupLongTermRetentionPolicy</span></span>](./Get-AzSqlDatabaseBackupLongTermRetentionPolicy.md)

[<span data-ttu-id="8a766-148">Set-AzSqlDatabaseBackupLongTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="8a766-148">Set-AzSqlDatabaseBackupLongTermRetentionPolicy</span></span>](./Set-AzSqlDatabaseBackupLongTermRetentionPolicy.md)

[<span data-ttu-id="8a766-149">Dokumentation för SQL-databaser</span><span class="sxs-lookup"><span data-stu-id="8a766-149">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)