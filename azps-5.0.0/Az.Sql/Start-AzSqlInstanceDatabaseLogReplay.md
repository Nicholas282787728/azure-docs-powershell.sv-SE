---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/Start-AzSqlInstanceDatabaseLogReplay
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Start-AzSqlInstanceDatabaseLogReplay.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Start-AzSqlInstanceDatabaseLogReplay.md
ms.openlocfilehash: 61a87f61efaa889af830cc7bdaa44bcf0b7fc698
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94263374"
---
# <span data-ttu-id="53f4b-101">Start-AzSqlInstanceDatabaseLogReplay</span><span class="sxs-lookup"><span data-stu-id="53f4b-101">Start-AzSqlInstanceDatabaseLogReplay</span></span>

## <span data-ttu-id="53f4b-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="53f4b-102">SYNOPSIS</span></span>
<span data-ttu-id="53f4b-103">Startar en logg-Replay med angivna parametrar.</span><span class="sxs-lookup"><span data-stu-id="53f4b-103">Starts a Log Replay service with the given parameters.</span></span>

## <span data-ttu-id="53f4b-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="53f4b-104">SYNTAX</span></span>

### <span data-ttu-id="53f4b-105">LogReplayInstanceDatabaseFromInputParameters (standard)</span><span class="sxs-lookup"><span data-stu-id="53f4b-105">LogReplayInstanceDatabaseFromInputParameters (Default)</span></span>
```
Start-AzSqlInstanceDatabaseLogReplay -StorageContainerUri <String> -StorageContainerSasToken <String>
 [-AutoCompleteRestore] [-LastBackupName <String>] [-Collation <String>] [-Name] <String>
 [-InstanceName] <String> [-ResourceGroupName] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="53f4b-106">LogReplayInstanceDatabaseFromAzureSqlManagedDatabaseModelInstanceDefinition</span><span class="sxs-lookup"><span data-stu-id="53f4b-106">LogReplayInstanceDatabaseFromAzureSqlManagedDatabaseModelInstanceDefinition</span></span>
```
Start-AzSqlInstanceDatabaseLogReplay -StorageContainerUri <String> -StorageContainerSasToken <String>
 [-AutoCompleteRestore] [-LastBackupName <String>] [-Collation <String>] [-PassThru]
 [-InputObject] <AzureSqlManagedDatabaseModel> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="53f4b-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="53f4b-107">DESCRIPTION</span></span>
<span data-ttu-id="53f4b-108">Cmdleten **Start-AzSqlInstanceDatabaseLogReplay** Start of the logganalys service.</span><span class="sxs-lookup"><span data-stu-id="53f4b-108">The **Start-AzSqlInstanceDatabaseLogReplay** cmdlet initiate start of the log replay service.</span></span>

## <span data-ttu-id="53f4b-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="53f4b-109">EXAMPLES</span></span>

### <span data-ttu-id="53f4b-110">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="53f4b-110">Example 1</span></span>
```powershell
PS C:\> Start-AzSqlInstanceDatabaseLogReplay -ResourceGroupName "ResourceGroup01" -InstanceName "ManagedInstance01" -Name "ManagedDatabaseName"
    -Collation "SQL_Latin1_General_CP1_CI_AS" -StorageContainerUri "https://test.blob.core.windows.net/testing"
    -StorageContainerSasToken "sv=2019-02-02&ss=b&srt=sco&sp=rl&se=2023-12-02T00:09:14Z&st=2019-11-25T16:09:14Z&spr=https&sig=92kAe4QYmXaht%2Fgjocqwerqwer41s%3D"
    -AutoComplete -LastBackupName "last_backup.bak"
```

<span data-ttu-id="53f4b-111">Det här kommandot skapar en ny hanterad databas och börjar återställa säkerhets kopior från den angivna behållaren tills last_backup. bak återställs.</span><span class="sxs-lookup"><span data-stu-id="53f4b-111">This command will create new managed database and will start restoring backups from the given container until last_backup.bak is restored.</span></span>

### <span data-ttu-id="53f4b-112">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="53f4b-112">Example 2</span></span>
```powershell
PS C:\> Start-AzSqlInstanceDatabaseLogReplay -ResourceGroupName "ResourceGroup01" -InstanceName "ManagedInstance01" -Name "ManagedDatabaseName"
    -Collation "SQL_Latin1_General_CP1_CI_AS" -StorageContainerUri "https://test.blob.core.windows.net/testing"
    -StorageContainerSasToken "sv=2019-02-02&ss=b&srt=sco&sp=rl&se=2023-12-02T00:09:14Z&st=2019-11-25T16:09:14Z&spr=https&sig=92kAe4QYmXaht%2Fgjocqwerqwer41s%3D"
```

<span data-ttu-id="53f4b-113">Det här kommandot skapar en ny hanterad databas och börjar återställa säkerhets kopior från den angivna behållaren tills Complete-AzSqlInstanceDatabaseLogReplay anropas med den senaste säkerhets kopian.</span><span class="sxs-lookup"><span data-stu-id="53f4b-113">This command will create new managed database and will start restoring backups from the given container until Complete-AzSqlInstanceDatabaseLogReplay is called with the last backup wanted.</span></span>

## <span data-ttu-id="53f4b-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="53f4b-114">PARAMETERS</span></span>

### <span data-ttu-id="53f4b-115">-AutoCompleteRestore</span><span class="sxs-lookup"><span data-stu-id="53f4b-115">-AutoCompleteRestore</span></span>
<span data-ttu-id="53f4b-116">Indikatorn som automatiskt Slutför återställning vid slut för ande.</span><span class="sxs-lookup"><span data-stu-id="53f4b-116">The indicator whether or not to auto-complete restore upon completion.</span></span>

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

### <span data-ttu-id="53f4b-117">-Sortering</span><span class="sxs-lookup"><span data-stu-id="53f4b-117">-Collation</span></span>
<span data-ttu-id="53f4b-118">Sortering av instans databasen som ska användas.</span><span class="sxs-lookup"><span data-stu-id="53f4b-118">The collation of the instance database to use.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="53f4b-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="53f4b-119">-DefaultProfile</span></span>
<span data-ttu-id="53f4b-120">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="53f4b-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="53f4b-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="53f4b-121">-InputObject</span></span>
<span data-ttu-id="53f4b-122">Instans databas objekt.</span><span class="sxs-lookup"><span data-stu-id="53f4b-122">The instance database object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseModel
Parameter Sets: LogReplayInstanceDatabaseFromAzureSqlManagedDatabaseModelInstanceDefinition
Aliases: InstanceDatabase

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="53f4b-123">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="53f4b-123">-InstanceName</span></span>
<span data-ttu-id="53f4b-124">Namnet på instansen.</span><span class="sxs-lookup"><span data-stu-id="53f4b-124">The name of the instance.</span></span>

```yaml
Type: System.String
Parameter Sets: LogReplayInstanceDatabaseFromInputParameters
Aliases: ManagedInstanceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="53f4b-125">-LastBackupName</span><span class="sxs-lookup"><span data-stu-id="53f4b-125">-LastBackupName</span></span>
<span data-ttu-id="53f4b-126">Namnet på den senaste säkerhets kopian som ska återställas.</span><span class="sxs-lookup"><span data-stu-id="53f4b-126">The name of the last backup file to restore.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="53f4b-127">-Namn</span><span class="sxs-lookup"><span data-stu-id="53f4b-127">-Name</span></span>
<span data-ttu-id="53f4b-128">Namnet på instans databasen.</span><span class="sxs-lookup"><span data-stu-id="53f4b-128">The name of the instance database.</span></span>

```yaml
Type: System.String
Parameter Sets: LogReplayInstanceDatabaseFromInputParameters
Aliases: InstanceDatabaseName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="53f4b-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="53f4b-129">-PassThru</span></span>
<span data-ttu-id="53f4b-130">Definierar om synkroniseringsresursen ska returneras.</span><span class="sxs-lookup"><span data-stu-id="53f4b-130">Defines Whether return the sync group.</span></span>

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

### <span data-ttu-id="53f4b-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="53f4b-131">-ResourceGroupName</span></span>
<span data-ttu-id="53f4b-132">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="53f4b-132">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: LogReplayInstanceDatabaseFromInputParameters
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="53f4b-133">-StorageContainerSasToken</span><span class="sxs-lookup"><span data-stu-id="53f4b-133">-StorageContainerSasToken</span></span>
<span data-ttu-id="53f4b-134">SAS-token för lagrings behållare.</span><span class="sxs-lookup"><span data-stu-id="53f4b-134">The storage container Sas token.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: SasToken

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="53f4b-135">-StorageContainerUri</span><span class="sxs-lookup"><span data-stu-id="53f4b-135">-StorageContainerUri</span></span>
<span data-ttu-id="53f4b-136">URI för lagrings behållare.</span><span class="sxs-lookup"><span data-stu-id="53f4b-136">The storage container URI.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Storage

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="53f4b-137">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="53f4b-137">-Confirm</span></span>
<span data-ttu-id="53f4b-138">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="53f4b-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="53f4b-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="53f4b-139">-WhatIf</span></span>
<span data-ttu-id="53f4b-140">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="53f4b-140">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="53f4b-141">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="53f4b-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="53f4b-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="53f4b-142">CommonParameters</span></span>
<span data-ttu-id="53f4b-143">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="53f4b-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="53f4b-144">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="53f4b-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="53f4b-145">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="53f4b-145">INPUTS</span></span>

### <span data-ttu-id="53f4b-146">System. String</span><span class="sxs-lookup"><span data-stu-id="53f4b-146">System.String</span></span>

### <span data-ttu-id="53f4b-147">Microsoft. Azure. commands. SQL. ManagedDatabase. Model. AzureSqlManagedDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="53f4b-147">Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseModel</span></span>

## <span data-ttu-id="53f4b-148">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="53f4b-148">OUTPUTS</span></span>

### <span data-ttu-id="53f4b-149">Microsoft. Azure. commands. SQL. ManagedDatabase. Model. AzureSqlManagedDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="53f4b-149">Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseModel</span></span>

## <span data-ttu-id="53f4b-150">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="53f4b-150">NOTES</span></span>

## <span data-ttu-id="53f4b-151">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="53f4b-151">RELATED LINKS</span></span>
