---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/Complete-AzSqlInstanceDatabaseLogReplay
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Complete-AzSqlInstanceDatabaseLogReplay.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Complete-AzSqlInstanceDatabaseLogReplay.md
ms.openlocfilehash: d1d7cead951520944199347ebdbb209c5474eb3e
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94270230"
---
# <span data-ttu-id="c2289-101">Complete-AzSqlInstanceDatabaseLogReplay</span><span class="sxs-lookup"><span data-stu-id="c2289-101">Complete-AzSqlInstanceDatabaseLogReplay</span></span>

## <span data-ttu-id="c2289-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="c2289-102">SYNOPSIS</span></span>
<span data-ttu-id="c2289-103">Slutför loggnings tjänsten för den angivna databasen.</span><span class="sxs-lookup"><span data-stu-id="c2289-103">Completes Log Replay service for the given database.</span></span>

## <span data-ttu-id="c2289-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="c2289-104">SYNTAX</span></span>

### <span data-ttu-id="c2289-105">LogReplayInstanceDatabaseFromInputParameters (standard)</span><span class="sxs-lookup"><span data-stu-id="c2289-105">LogReplayInstanceDatabaseFromInputParameters (Default)</span></span>
```
Complete-AzSqlInstanceDatabaseLogReplay -LastBackupName <String> [-Name] <String> [-InstanceName] <String>
 [-ResourceGroupName] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="c2289-106">LogReplayInstanceDatabaseFromAzureSqlManagedDatabaseModelInstanceDefinition</span><span class="sxs-lookup"><span data-stu-id="c2289-106">LogReplayInstanceDatabaseFromAzureSqlManagedDatabaseModelInstanceDefinition</span></span>
```
Complete-AzSqlInstanceDatabaseLogReplay -LastBackupName <String> [-PassThru]
 [-InputObject] <AzureSqlManagedDatabaseModel> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="c2289-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="c2289-107">DESCRIPTION</span></span>
<span data-ttu-id="c2289-108">Cmdleten **Complete-AzSqlInstanceDatabaseLogReplay** Slutför loggnings tjänsten för en given databas.</span><span class="sxs-lookup"><span data-stu-id="c2289-108">The **Complete-AzSqlInstanceDatabaseLogReplay** cmdlet completes the Log Replay service on the given database.</span></span>

## <span data-ttu-id="c2289-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="c2289-109">EXAMPLES</span></span>

### <span data-ttu-id="c2289-110">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="c2289-110">Example 1</span></span>
```powershell
PS C:\> Complete-AzSqlInstanceDatabaseLogReplay -ResourceGroupName "ResourceGroup01" -InstanceName "ManagedInstance01" -Name "ManagedDatabaseName" -LastBackupName "last_backup.bak"
```

<span data-ttu-id="c2289-111">Det här kommandot slutför logg tjänsten för den angivna databasen efter den senaste säkerhets kopieringen.</span><span class="sxs-lookup"><span data-stu-id="c2289-111">This command will complete Log Replay service for the given database after last backup gets restored.</span></span>

## <span data-ttu-id="c2289-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="c2289-112">PARAMETERS</span></span>

### <span data-ttu-id="c2289-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c2289-113">-DefaultProfile</span></span>
<span data-ttu-id="c2289-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="c2289-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c2289-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c2289-115">-InputObject</span></span>
<span data-ttu-id="c2289-116">Instans databas objekt.</span><span class="sxs-lookup"><span data-stu-id="c2289-116">The instance database object.</span></span>

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

### <span data-ttu-id="c2289-117">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="c2289-117">-InstanceName</span></span>
<span data-ttu-id="c2289-118">Namnet på instansen.</span><span class="sxs-lookup"><span data-stu-id="c2289-118">The name of the instance.</span></span>

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

### <span data-ttu-id="c2289-119">-LastBackupName</span><span class="sxs-lookup"><span data-stu-id="c2289-119">-LastBackupName</span></span>
<span data-ttu-id="c2289-120">Namnet på den senaste säkerhets kopian som ska återställas.</span><span class="sxs-lookup"><span data-stu-id="c2289-120">The name of the last backup file to restore.</span></span>

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

### <span data-ttu-id="c2289-121">-Namn</span><span class="sxs-lookup"><span data-stu-id="c2289-121">-Name</span></span>
<span data-ttu-id="c2289-122">Namnet på instans databasen.</span><span class="sxs-lookup"><span data-stu-id="c2289-122">The name of the instance database.</span></span>

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

### <span data-ttu-id="c2289-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c2289-123">-PassThru</span></span>
<span data-ttu-id="c2289-124">Definierar om synkroniseringsresursen ska returneras.</span><span class="sxs-lookup"><span data-stu-id="c2289-124">Defines Whether return the sync group.</span></span>

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

### <span data-ttu-id="c2289-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c2289-125">-ResourceGroupName</span></span>
<span data-ttu-id="c2289-126">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="c2289-126">The name of the resource group.</span></span>

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

### <span data-ttu-id="c2289-127">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="c2289-127">-Confirm</span></span>
<span data-ttu-id="c2289-128">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="c2289-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c2289-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c2289-129">-WhatIf</span></span>
<span data-ttu-id="c2289-130">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="c2289-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="c2289-131">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="c2289-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c2289-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c2289-132">CommonParameters</span></span>
<span data-ttu-id="c2289-133">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c2289-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c2289-134">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c2289-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c2289-135">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="c2289-135">INPUTS</span></span>

### <span data-ttu-id="c2289-136">System. String</span><span class="sxs-lookup"><span data-stu-id="c2289-136">System.String</span></span>

### <span data-ttu-id="c2289-137">Microsoft. Azure. commands. SQL. ManagedDatabase. Model. AzureSqlManagedDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="c2289-137">Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseModel</span></span>

## <span data-ttu-id="c2289-138">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="c2289-138">OUTPUTS</span></span>

## <span data-ttu-id="c2289-139">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="c2289-139">NOTES</span></span>

## <span data-ttu-id="c2289-140">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="c2289-140">RELATED LINKS</span></span>
