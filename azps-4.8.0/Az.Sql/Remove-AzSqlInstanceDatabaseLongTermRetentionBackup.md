---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/remove-azsqlinstancedatabaselongtermretentionbackup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlInstanceDatabaseLongTermRetentionBackup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlInstanceDatabaseLongTermRetentionBackup.md
ms.openlocfilehash: 3dbcbed2466f9bb6b229a6dcfa710d6745a72eac
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94259039"
---
# <span data-ttu-id="9c901-101">Remove-AzSqlInstanceDatabaseLongTermRetentionBackup</span><span class="sxs-lookup"><span data-stu-id="9c901-101">Remove-AzSqlInstanceDatabaseLongTermRetentionBackup</span></span>

## <span data-ttu-id="9c901-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="9c901-102">SYNOPSIS</span></span>
<span data-ttu-id="9c901-103">Tar bort en långsiktig säkerhets kopiering.</span><span class="sxs-lookup"><span data-stu-id="9c901-103">Deletes a long term retention backup.</span></span>

## <span data-ttu-id="9c901-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="9c901-104">SYNTAX</span></span>

### <span data-ttu-id="9c901-105">RemoveBackupDefault (standard)</span><span class="sxs-lookup"><span data-stu-id="9c901-105">RemoveBackupDefault (Default)</span></span>
```
Remove-AzSqlInstanceDatabaseLongTermRetentionBackup [-Location] <String> [-InstanceName] <String>
 [-DatabaseName] <String> [-BackupName] <String> [-ResourceGroupName <String>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9c901-106">RemoveBackupByInputObject</span><span class="sxs-lookup"><span data-stu-id="9c901-106">RemoveBackupByInputObject</span></span>
```
Remove-AzSqlInstanceDatabaseLongTermRetentionBackup
 [-InputObject] <AzureSqlManagedDatabaseLongTermRetentionBackupModel> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9c901-107">RemoveBackupByResourceId</span><span class="sxs-lookup"><span data-stu-id="9c901-107">RemoveBackupByResourceId</span></span>
```
Remove-AzSqlInstanceDatabaseLongTermRetentionBackup [-ResourceId] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9c901-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="9c901-108">DESCRIPTION</span></span>
<span data-ttu-id="9c901-109">Cmdleten **Remove-AzSqlInstanceDatabaseLongTermRetentionBackup** tar bort den angivna säkerhets kopian.</span><span class="sxs-lookup"><span data-stu-id="9c901-109">The **Remove-AzSqlInstanceDatabaseLongTermRetentionBackup** cmdlet deletes the backup specified.</span></span>

## <span data-ttu-id="9c901-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="9c901-110">EXAMPLES</span></span>

### <span data-ttu-id="9c901-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="9c901-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzSqlInstanceDatabaseLongTermRetentionBackup -Location southeastasia -ResourceGroupName testResourceGroup -InstanceName testInstance -DatabaseName test -BackupName 15be823c-7e2c-49d8-819f-a3fdcad92215;132268250550000000
```

<span data-ttu-id="9c901-112">Tar bort säkerhets kopian med namnet 15be823c-7e2c-49d8-819f-a3fdcad92215; 132268250550000000</span><span class="sxs-lookup"><span data-stu-id="9c901-112">Deletes the backup with name 15be823c-7e2c-49d8-819f-a3fdcad92215;132268250550000000</span></span>

## <span data-ttu-id="9c901-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="9c901-113">PARAMETERS</span></span>

### <span data-ttu-id="9c901-114">-BackupName</span><span class="sxs-lookup"><span data-stu-id="9c901-114">-BackupName</span></span>
<span data-ttu-id="9c901-115">Namnet på säkerhets kopian.</span><span class="sxs-lookup"><span data-stu-id="9c901-115">The name of the backup.</span></span>

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

### <span data-ttu-id="9c901-116">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="9c901-116">-DatabaseName</span></span>
<span data-ttu-id="9c901-117">Namnet på den hanterade databas som säkerhets kopian kommer från.</span><span class="sxs-lookup"><span data-stu-id="9c901-117">The name of the Managed Database the backup is from.</span></span>

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

### <span data-ttu-id="9c901-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9c901-118">-DefaultProfile</span></span>
<span data-ttu-id="9c901-119">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="9c901-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9c901-120">-Force</span><span class="sxs-lookup"><span data-stu-id="9c901-120">-Force</span></span>
<span data-ttu-id="9c901-121">Hoppa över bekräftelse meddelande för att utföra åtgärden</span><span class="sxs-lookup"><span data-stu-id="9c901-121">Skip confirmation message for performing the action</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9c901-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9c901-122">-InputObject</span></span>
<span data-ttu-id="9c901-123">Databasens säkerhets kopie rad lagrings objekt som ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="9c901-123">The Database Long Term Retention Backup object to remove.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.ManagedDatabaseBackup.Model.AzureSqlManagedDatabaseLongTermRetentionBackupModel
Parameter Sets: RemoveBackupByInputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9c901-124">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="9c901-124">-InstanceName</span></span>
<span data-ttu-id="9c901-125">Namnet på den hanterade instans som säkerhets kopian finns under.</span><span class="sxs-lookup"><span data-stu-id="9c901-125">The name of the Managed Instance the backup is under.</span></span>

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

### <span data-ttu-id="9c901-126">-Plats</span><span class="sxs-lookup"><span data-stu-id="9c901-126">-Location</span></span>
<span data-ttu-id="9c901-127">Platsen för säkerhets kopiornas hanterade instanser.</span><span class="sxs-lookup"><span data-stu-id="9c901-127">The location of the backups' source Managed Instance.</span></span>

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

### <span data-ttu-id="9c901-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9c901-128">-ResourceGroupName</span></span>
<span data-ttu-id="9c901-129">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="9c901-129">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveBackupDefault
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9c901-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9c901-130">-ResourceId</span></span>
<span data-ttu-id="9c901-131">Resurs-ID för databasens tids lagrings säkerhets kopia som tas bort.</span><span class="sxs-lookup"><span data-stu-id="9c901-131">The Resource ID of the Database Long Term Retention Backup to remove.</span></span>

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

### <span data-ttu-id="9c901-132">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="9c901-132">-Confirm</span></span>
<span data-ttu-id="9c901-133">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="9c901-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9c901-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9c901-134">-WhatIf</span></span>
<span data-ttu-id="9c901-135">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="9c901-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9c901-136">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="9c901-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9c901-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9c901-137">CommonParameters</span></span>
<span data-ttu-id="9c901-138">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9c901-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9c901-139">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="9c901-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9c901-140">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="9c901-140">INPUTS</span></span>

### <span data-ttu-id="9c901-141">Microsoft. Azure. commands. SQL. ManagedDatabaseBackup. Model. AzureSqlManagedDatabaseLongTermRetentionBackupModel</span><span class="sxs-lookup"><span data-stu-id="9c901-141">Microsoft.Azure.Commands.Sql.ManagedDatabaseBackup.Model.AzureSqlManagedDatabaseLongTermRetentionBackupModel</span></span>

### <span data-ttu-id="9c901-142">System. String</span><span class="sxs-lookup"><span data-stu-id="9c901-142">System.String</span></span>

## <span data-ttu-id="9c901-143">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="9c901-143">OUTPUTS</span></span>

### <span data-ttu-id="9c901-144">Microsoft. Azure. commands. SQL. ManagedDatabaseBackup. Model. AzureSqlManagedDatabaseLongTermRetentionBackupModel</span><span class="sxs-lookup"><span data-stu-id="9c901-144">Microsoft.Azure.Commands.Sql.ManagedDatabaseBackup.Model.AzureSqlManagedDatabaseLongTermRetentionBackupModel</span></span>

## <span data-ttu-id="9c901-145">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="9c901-145">NOTES</span></span>

## <span data-ttu-id="9c901-146">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="9c901-146">RELATED LINKS</span></span>

[<span data-ttu-id="9c901-147">Get-AzSqlInstanceDatabaseLongTermRetentionBackup</span><span class="sxs-lookup"><span data-stu-id="9c901-147">Get-AzSqlInstanceDatabaseLongTermRetentionBackup</span></span>](./Get-AzSqlInstanceDatabaseLongTermRetentionBackup.md)

[<span data-ttu-id="9c901-148">Get-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="9c901-148">Get-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy</span></span>](./Get-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy.md)

[<span data-ttu-id="9c901-149">Set-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="9c901-149">Set-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy</span></span>](./Set-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy.md)

[<span data-ttu-id="9c901-150">Dokumentation för SQL-databaser</span><span class="sxs-lookup"><span data-stu-id="9c901-150">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)