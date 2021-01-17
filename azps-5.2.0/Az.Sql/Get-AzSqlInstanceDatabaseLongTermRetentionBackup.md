---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlinstancedatabaselongtermretentionbackup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlInstanceDatabaseLongTermRetentionBackup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlInstanceDatabaseLongTermRetentionBackup.md
ms.openlocfilehash: ccd716b493640afef7b5adea0b2e834c10893c3c
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98389217"
---
# <span data-ttu-id="0d1c4-101">Get-AzSqlInstanceDatabaseLongTermRetentionBackup</span><span class="sxs-lookup"><span data-stu-id="0d1c4-101">Get-AzSqlInstanceDatabaseLongTermRetentionBackup</span></span>

## <span data-ttu-id="0d1c4-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="0d1c4-102">SYNOPSIS</span></span>
<span data-ttu-id="0d1c4-103">Hämtar långsiktiga säkerhets kopieringar.</span><span class="sxs-lookup"><span data-stu-id="0d1c4-103">Gets long term retention backup(s).</span></span>

## <span data-ttu-id="0d1c4-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="0d1c4-104">SYNTAX</span></span>

### <span data-ttu-id="0d1c4-105">Plats (standard)</span><span class="sxs-lookup"><span data-stu-id="0d1c4-105">Location (Default)</span></span>
```
Get-AzSqlInstanceDatabaseLongTermRetentionBackup [-Location] <String> [-ResourceGroupName <String>]
 [-OnlyLatestPerDatabase] [-DatabaseState <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0d1c4-106">Namn</span><span class="sxs-lookup"><span data-stu-id="0d1c4-106">InstanceName</span></span>
```
Get-AzSqlInstanceDatabaseLongTermRetentionBackup [-Location] <String> [-InstanceName] <String>
 [-ResourceGroupName <String>] [-OnlyLatestPerDatabase] [-DatabaseState <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0d1c4-107">Databas</span><span class="sxs-lookup"><span data-stu-id="0d1c4-107">DatabaseName</span></span>
```
Get-AzSqlInstanceDatabaseLongTermRetentionBackup [-Location] <String> [-InstanceName] <String>
 [-DatabaseName] <String> [-ResourceGroupName <String>] [-OnlyLatestPerDatabase]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0d1c4-108">BackupName</span><span class="sxs-lookup"><span data-stu-id="0d1c4-108">BackupName</span></span>
```
Get-AzSqlInstanceDatabaseLongTermRetentionBackup [-Location] <String> [-InstanceName] <String>
 [-DatabaseName] <String> [-BackupName] <String> [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0d1c4-109">GetBackupByResourceId</span><span class="sxs-lookup"><span data-stu-id="0d1c4-109">GetBackupByResourceId</span></span>
```
Get-AzSqlInstanceDatabaseLongTermRetentionBackup [-Location] <String> [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0d1c4-110">GetBackupByInputObject</span><span class="sxs-lookup"><span data-stu-id="0d1c4-110">GetBackupByInputObject</span></span>
```
Get-AzSqlInstanceDatabaseLongTermRetentionBackup [-InputObject] <AzureSqlManagedDatabaseModel>
 [-BackupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0d1c4-111">GetBackupsByInputObject</span><span class="sxs-lookup"><span data-stu-id="0d1c4-111">GetBackupsByInputObject</span></span>
```
Get-AzSqlInstanceDatabaseLongTermRetentionBackup [-InputObject] <AzureSqlManagedDatabaseModel>
 [-OnlyLatestPerDatabase] [-DatabaseState <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0d1c4-112">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="0d1c4-112">DESCRIPTION</span></span>
<span data-ttu-id="0d1c4-113">{{Fyll i beskrivningen}}</span><span class="sxs-lookup"><span data-stu-id="0d1c4-113">{{ Fill in the Description }}</span></span>

## <span data-ttu-id="0d1c4-114">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="0d1c4-114">EXAMPLES</span></span>

### <span data-ttu-id="0d1c4-115">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="0d1c4-115">Example 1</span></span>
```powershell
PS C:\> Get-AzSqlInstanceDatabaseLongTermRetentionBackup -Location southeastasia -ResourceGroupName testResourceGroup -InstanceName testInstance -DatabaseName test


BackupExpirationTime : 3/10/2020 1:10:45 PM
BackupName           : 15be823c-7e2c-49d8-819f-a3fdcad92215;132268250550000000
BackupTime           : 2/22/2020 6:04:15 AM
DatabaseName         : test
DatabaseDeletionTime : 2/24/2020 2:56:44 PM
Location             : southeastasia
ResourceId           : /subscriptions/f46521f3-5bb0-4eea-a3c2-c2d5987df96b/resourceGroups/testResourceGroup/providers/Microsoft.Sql/locations/southeastasia/longTermRetentionManaged
                       Instances/testInstance/longTermRetentionDatabases/test/longTermRetentionManagedInstanceBackups/15be823c-7e2c-49d8-819f-a3fdcad92215;132268250550000000
ManagedInstanceName  : testInstance
InstanceCreateTime   : 10/17/2019 4:52:10 PM
ResourceGroupName    : testResourceGroup
```

<span data-ttu-id="0d1c4-116">Hämtar alla långsiktiga säkerhets kopior för en viss databas.</span><span class="sxs-lookup"><span data-stu-id="0d1c4-116">Gets all long term retention backups for a particular database.</span></span>  <span data-ttu-id="0d1c4-117">Resurs gruppen är valfri.</span><span class="sxs-lookup"><span data-stu-id="0d1c4-117">Resource Group is optional.</span></span> 

## <span data-ttu-id="0d1c4-118">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="0d1c4-118">PARAMETERS</span></span>

### <span data-ttu-id="0d1c4-119">-BackupName</span><span class="sxs-lookup"><span data-stu-id="0d1c4-119">-BackupName</span></span>
<span data-ttu-id="0d1c4-120">Namnet på säkerhets kopian.</span><span class="sxs-lookup"><span data-stu-id="0d1c4-120">The name of the backup.</span></span>

```yaml
Type: System.String
Parameter Sets: BackupName, GetBackupByInputObject
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0d1c4-121">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="0d1c4-121">-DatabaseName</span></span>
<span data-ttu-id="0d1c4-122">Namnet på den hanterade databas som säkerhets kopiorna ligger under.</span><span class="sxs-lookup"><span data-stu-id="0d1c4-122">The name of the Managed Database the backups are under.</span></span>

```yaml
Type: System.String
Parameter Sets: DatabaseName, BackupName
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0d1c4-123">-DatabaseState</span><span class="sxs-lookup"><span data-stu-id="0d1c4-123">-DatabaseState</span></span>
<span data-ttu-id="0d1c4-124">Tillståndet för den databas vars säkerhets kopior du vill hitta, använda, ta bort eller alla.</span><span class="sxs-lookup"><span data-stu-id="0d1c4-124">The state of the database whose backups you want to find, Alive, Deleted, or All.</span></span>
<span data-ttu-id="0d1c4-125">Standardvärden för alla</span><span class="sxs-lookup"><span data-stu-id="0d1c4-125">Defaults to All</span></span>

```yaml
Type: System.String
Parameter Sets: Location, InstanceName, GetBackupsByInputObject
Aliases:
Accepted values: All, Deleted, Live

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0d1c4-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0d1c4-126">-DefaultProfile</span></span>
<span data-ttu-id="0d1c4-127">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="0d1c4-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0d1c4-128">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0d1c4-128">-InputObject</span></span>
<span data-ttu-id="0d1c4-129">Databasobjektet för att hämta säkerhets kopior.</span><span class="sxs-lookup"><span data-stu-id="0d1c4-129">The database object to get backups for.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseModel
Parameter Sets: GetBackupByInputObject, GetBackupsByInputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0d1c4-130">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="0d1c4-130">-InstanceName</span></span>
<span data-ttu-id="0d1c4-131">Namnet på den hanterade instans som säkerhets kopiorna står under.</span><span class="sxs-lookup"><span data-stu-id="0d1c4-131">The name of the Managed Instance the backups are under.</span></span>

```yaml
Type: System.String
Parameter Sets: InstanceName, DatabaseName, BackupName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0d1c4-132">-Plats</span><span class="sxs-lookup"><span data-stu-id="0d1c4-132">-Location</span></span>
<span data-ttu-id="0d1c4-133">Platsen för säkerhets kopiornas hanterade instanser.</span><span class="sxs-lookup"><span data-stu-id="0d1c4-133">The location of the backups' source Managed Instance.</span></span>

```yaml
Type: System.String
Parameter Sets: Location, InstanceName, DatabaseName, BackupName, GetBackupByResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0d1c4-134">-OnlyLatestPerDatabase</span><span class="sxs-lookup"><span data-stu-id="0d1c4-134">-OnlyLatestPerDatabase</span></span>
<span data-ttu-id="0d1c4-135">Om du vill få den senaste säkerhets kopian per databas eller inte.</span><span class="sxs-lookup"><span data-stu-id="0d1c4-135">Whether or not to only get the latest backup per database.</span></span>
<span data-ttu-id="0d1c4-136">Standardvärdet är falskt.</span><span class="sxs-lookup"><span data-stu-id="0d1c4-136">Defaults to false.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Location, InstanceName, DatabaseName, GetBackupsByInputObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0d1c4-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0d1c4-137">-ResourceGroupName</span></span>
<span data-ttu-id="0d1c4-138">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="0d1c4-138">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: Location, InstanceName, DatabaseName, BackupName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0d1c4-139">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="0d1c4-139">-ResourceId</span></span>
<span data-ttu-id="0d1c4-140">Databas resurs-ID som du kan använda för att hämta säkerhets kopior för.</span><span class="sxs-lookup"><span data-stu-id="0d1c4-140">The database Resource ID to get backups for.</span></span>

```yaml
Type: System.String
Parameter Sets: GetBackupByResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0d1c4-141">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="0d1c4-141">-Confirm</span></span>
<span data-ttu-id="0d1c4-142">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="0d1c4-142">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0d1c4-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0d1c4-143">-WhatIf</span></span>
<span data-ttu-id="0d1c4-144">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="0d1c4-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0d1c4-145">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="0d1c4-145">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0d1c4-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0d1c4-146">CommonParameters</span></span>
<span data-ttu-id="0d1c4-147">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0d1c4-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0d1c4-148">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="0d1c4-148">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0d1c4-149">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="0d1c4-149">INPUTS</span></span>

### <span data-ttu-id="0d1c4-150">Microsoft. Azure. commands. SQL. ManagedDatabase. Model. AzureSqlManagedDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="0d1c4-150">Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseModel</span></span>

### <span data-ttu-id="0d1c4-151">System. String</span><span class="sxs-lookup"><span data-stu-id="0d1c4-151">System.String</span></span>

## <span data-ttu-id="0d1c4-152">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="0d1c4-152">OUTPUTS</span></span>

### <span data-ttu-id="0d1c4-153">Microsoft. Azure. commands. SQL. ManagedDatabaseBackup. Model. AzureSqlManagedDatabaseLongTermRetentionBackupModel</span><span class="sxs-lookup"><span data-stu-id="0d1c4-153">Microsoft.Azure.Commands.Sql.ManagedDatabaseBackup.Model.AzureSqlManagedDatabaseLongTermRetentionBackupModel</span></span>

## <span data-ttu-id="0d1c4-154">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="0d1c4-154">NOTES</span></span>

## <span data-ttu-id="0d1c4-155">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="0d1c4-155">RELATED LINKS</span></span>

[<span data-ttu-id="0d1c4-156">Remove-AzSqlInstanceDatabaseLongTermRetentionBackup</span><span class="sxs-lookup"><span data-stu-id="0d1c4-156">Remove-AzSqlInstanceDatabaseLongTermRetentionBackup</span></span>](./Remove-AzSqlInstanceDatabaseLongTermRetentionBackup.md)

[<span data-ttu-id="0d1c4-157">Get-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="0d1c4-157">Get-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy</span></span>](./Get-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy.md)

[<span data-ttu-id="0d1c4-158">Set-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="0d1c4-158">Set-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy</span></span>](./Set-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy.md)

[<span data-ttu-id="0d1c4-159">Dokumentation för SQL-databaser</span><span class="sxs-lookup"><span data-stu-id="0d1c4-159">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)