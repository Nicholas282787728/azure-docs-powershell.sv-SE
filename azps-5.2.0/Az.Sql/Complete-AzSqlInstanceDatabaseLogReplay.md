---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/Complete-AzSqlInstanceDatabaseLogReplay
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Complete-AzSqlInstanceDatabaseLogReplay.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Complete-AzSqlInstanceDatabaseLogReplay.md
ms.openlocfilehash: d1d7cead951520944199347ebdbb209c5474eb3e
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98394323"
---
# <span data-ttu-id="98096-101">Complete-AzSqlInstanceDatabaseLogReplay</span><span class="sxs-lookup"><span data-stu-id="98096-101">Complete-AzSqlInstanceDatabaseLogReplay</span></span>

## <span data-ttu-id="98096-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="98096-102">SYNOPSIS</span></span>
<span data-ttu-id="98096-103">Slutför loggnings tjänsten för den angivna databasen.</span><span class="sxs-lookup"><span data-stu-id="98096-103">Completes Log Replay service for the given database.</span></span>

## <span data-ttu-id="98096-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="98096-104">SYNTAX</span></span>

### <span data-ttu-id="98096-105">LogReplayInstanceDatabaseFromInputParameters (standard)</span><span class="sxs-lookup"><span data-stu-id="98096-105">LogReplayInstanceDatabaseFromInputParameters (Default)</span></span>
```
Complete-AzSqlInstanceDatabaseLogReplay -LastBackupName <String> [-Name] <String> [-InstanceName] <String>
 [-ResourceGroupName] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="98096-106">LogReplayInstanceDatabaseFromAzureSqlManagedDatabaseModelInstanceDefinition</span><span class="sxs-lookup"><span data-stu-id="98096-106">LogReplayInstanceDatabaseFromAzureSqlManagedDatabaseModelInstanceDefinition</span></span>
```
Complete-AzSqlInstanceDatabaseLogReplay -LastBackupName <String> [-PassThru]
 [-InputObject] <AzureSqlManagedDatabaseModel> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="98096-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="98096-107">DESCRIPTION</span></span>
<span data-ttu-id="98096-108">Cmdleten **Complete-AzSqlInstanceDatabaseLogReplay** Slutför loggnings tjänsten för en given databas.</span><span class="sxs-lookup"><span data-stu-id="98096-108">The **Complete-AzSqlInstanceDatabaseLogReplay** cmdlet completes the Log Replay service on the given database.</span></span>

## <span data-ttu-id="98096-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="98096-109">EXAMPLES</span></span>

### <span data-ttu-id="98096-110">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="98096-110">Example 1</span></span>
```powershell
PS C:\> Complete-AzSqlInstanceDatabaseLogReplay -ResourceGroupName "ResourceGroup01" -InstanceName "ManagedInstance01" -Name "ManagedDatabaseName" -LastBackupName "last_backup.bak"
```

<span data-ttu-id="98096-111">Det här kommandot slutför logg tjänsten för den angivna databasen efter den senaste säkerhets kopieringen.</span><span class="sxs-lookup"><span data-stu-id="98096-111">This command will complete Log Replay service for the given database after last backup gets restored.</span></span>

## <span data-ttu-id="98096-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="98096-112">PARAMETERS</span></span>

### <span data-ttu-id="98096-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="98096-113">-DefaultProfile</span></span>
<span data-ttu-id="98096-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="98096-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="98096-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="98096-115">-InputObject</span></span>
<span data-ttu-id="98096-116">Instans databas objekt.</span><span class="sxs-lookup"><span data-stu-id="98096-116">The instance database object.</span></span>

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

### <span data-ttu-id="98096-117">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="98096-117">-InstanceName</span></span>
<span data-ttu-id="98096-118">Namnet på instansen.</span><span class="sxs-lookup"><span data-stu-id="98096-118">The name of the instance.</span></span>

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

### <span data-ttu-id="98096-119">-LastBackupName</span><span class="sxs-lookup"><span data-stu-id="98096-119">-LastBackupName</span></span>
<span data-ttu-id="98096-120">Namnet på den senaste säkerhets kopian som ska återställas.</span><span class="sxs-lookup"><span data-stu-id="98096-120">The name of the last backup file to restore.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="98096-121">-Namn</span><span class="sxs-lookup"><span data-stu-id="98096-121">-Name</span></span>
<span data-ttu-id="98096-122">Namnet på instans databasen.</span><span class="sxs-lookup"><span data-stu-id="98096-122">The name of the instance database.</span></span>

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

### <span data-ttu-id="98096-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="98096-123">-PassThru</span></span>
<span data-ttu-id="98096-124">Definierar om synkroniseringsresursen ska returneras.</span><span class="sxs-lookup"><span data-stu-id="98096-124">Defines Whether return the sync group.</span></span>

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

### <span data-ttu-id="98096-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="98096-125">-ResourceGroupName</span></span>
<span data-ttu-id="98096-126">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="98096-126">The name of the resource group.</span></span>

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

### <span data-ttu-id="98096-127">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="98096-127">-Confirm</span></span>
<span data-ttu-id="98096-128">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="98096-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="98096-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="98096-129">-WhatIf</span></span>
<span data-ttu-id="98096-130">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="98096-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="98096-131">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="98096-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="98096-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="98096-132">CommonParameters</span></span>
<span data-ttu-id="98096-133">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="98096-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="98096-134">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="98096-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="98096-135">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="98096-135">INPUTS</span></span>

### <span data-ttu-id="98096-136">System. String</span><span class="sxs-lookup"><span data-stu-id="98096-136">System.String</span></span>

### <span data-ttu-id="98096-137">Microsoft. Azure. commands. SQL. ManagedDatabase. Model. AzureSqlManagedDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="98096-137">Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseModel</span></span>

## <span data-ttu-id="98096-138">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="98096-138">OUTPUTS</span></span>

## <span data-ttu-id="98096-139">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="98096-139">NOTES</span></span>

## <span data-ttu-id="98096-140">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="98096-140">RELATED LINKS</span></span>
