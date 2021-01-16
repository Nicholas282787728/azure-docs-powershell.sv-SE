---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataMigration.dll-Help.xml
Module Name: Az.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/az.datamigration/New-AzDataMigrationTask
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/New-AzDataMigrationTask.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/New-AzDataMigrationTask.md
ms.openlocfilehash: 0222900be337cfe9eab97da31fc9d2dd84744e43
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98409443"
---
# <span data-ttu-id="5121a-101">New-AzDataMigrationTask</span><span class="sxs-lookup"><span data-stu-id="5121a-101">New-AzDataMigrationTask</span></span>

## <span data-ttu-id="5121a-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="5121a-102">SYNOPSIS</span></span>
<span data-ttu-id="5121a-103">Skapar och startar en datamigrering i Azure Database migration service.</span><span class="sxs-lookup"><span data-stu-id="5121a-103">Creates and starts a data migration task in the Azure Database Migration Service.</span></span>

## <span data-ttu-id="5121a-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="5121a-104">SYNTAX</span></span>

### <span data-ttu-id="5121a-105">ComponentNameParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="5121a-105">ComponentNameParameterSet (Default)</span></span>
```
New-AzDataMigrationTask -TaskType <TaskTypeEnum> -ResourceGroupName <String> -ServiceName <String>
 -ProjectName <String> -Name <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="5121a-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="5121a-106">ComponentObjectParameterSet</span></span>
```
New-AzDataMigrationTask [-InputObject] <PSProject> -TaskType <TaskTypeEnum> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5121a-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="5121a-107">ResourceIdParameterSet</span></span>
```
New-AzDataMigrationTask [-ResourceId] <String> -TaskType <TaskTypeEnum> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5121a-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="5121a-108">DESCRIPTION</span></span>
<span data-ttu-id="5121a-109">New-AzDataMigrationTask cmdlet skapar datamigrering.</span><span class="sxs-lookup"><span data-stu-id="5121a-109">The New-AzDataMigrationTask cmdlet creates data migration task.</span></span> <span data-ttu-id="5121a-110">Denna cmdlet tar upp parametrar för aktivitets typens uppräknare, Azure resurs grupp, namnet på den associerade tjänsten för Azure Database migration och Project som indata.</span><span class="sxs-lookup"><span data-stu-id="5121a-110">This cmdlet takes in parameters for Task Type enumerator, Azure Resource Group, name of associated Azure Database Migration Service and Project as input.</span></span> 

## <span data-ttu-id="5121a-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="5121a-111">EXAMPLES</span></span>

### <span data-ttu-id="5121a-112">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="5121a-112">Example 1</span></span>
```
PS C:\> New-AzDmsTask -TaskType MigrateSqlServerSqlDb -ResourceGroupName myResourceGroup -ServiceName TestService -ProjectName myDMSProject -TaskName MyMigrationTask -SourceConnection $sourceConnInfo -SourceCred $sourceCred -TargetConnection $targetConnInfo -TargetCred $targetCred -SelectedDatabase  $selectedDbs -MigrationValidation $validationTask
```

<span data-ttu-id="5121a-113">Det här exemplet visar hur du skapar en ny datamigrerings aktivitet med namnet MyMigrationTask i projektet med namnet myDMSProject och tjänsten som heter TestService.</span><span class="sxs-lookup"><span data-stu-id="5121a-113">This example script shows how to create a new Data Migration Task named MyMigrationTask in the project named myDMSProject and service named TestService.</span></span> 

## <span data-ttu-id="5121a-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="5121a-114">PARAMETERS</span></span>

### <span data-ttu-id="5121a-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5121a-115">-DefaultProfile</span></span>
<span data-ttu-id="5121a-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="5121a-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5121a-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5121a-117">-InputObject</span></span>
<span data-ttu-id="5121a-118">PSProject-objekt.</span><span class="sxs-lookup"><span data-stu-id="5121a-118">PSProject Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataMigration.Models.PSProject
Parameter Sets: ComponentObjectParameterSet
Aliases: Project

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5121a-119">-Namn</span><span class="sxs-lookup"><span data-stu-id="5121a-119">-Name</span></span>
<span data-ttu-id="5121a-120">Uppgiftens namn.</span><span class="sxs-lookup"><span data-stu-id="5121a-120">The name of the task.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: TaskName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5121a-121">-Projektetsnamn</span><span class="sxs-lookup"><span data-stu-id="5121a-121">-ProjectName</span></span>
<span data-ttu-id="5121a-122">Namnet på projektet.</span><span class="sxs-lookup"><span data-stu-id="5121a-122">The name of the project.</span></span>

```yaml
Type: System.String
Parameter Sets: ComponentNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5121a-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5121a-123">-ResourceGroupName</span></span>
<span data-ttu-id="5121a-124">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="5121a-124">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: ComponentNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5121a-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="5121a-125">-ResourceId</span></span>
<span data-ttu-id="5121a-126">Projekt resurs-ID.</span><span class="sxs-lookup"><span data-stu-id="5121a-126">Project Resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5121a-127">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="5121a-127">-ServiceName</span></span>
<span data-ttu-id="5121a-128">Tjänst namn för databas migration.</span><span class="sxs-lookup"><span data-stu-id="5121a-128">Database Migration Service Name.</span></span>

```yaml
Type: System.String
Parameter Sets: ComponentNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5121a-129">-TaskType</span><span class="sxs-lookup"><span data-stu-id="5121a-129">-TaskType</span></span>
<span data-ttu-id="5121a-130">Aktivitets typ.</span><span class="sxs-lookup"><span data-stu-id="5121a-130">Task Type.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataMigration.Models.TaskTypeEnum
Parameter Sets: (All)
Aliases:
Accepted values: MigrateSqlServerSqlDb, ConnectToSourceSqlServer, ConnectToTargetSqlDb, GetUserTablesSql, ConnectToTargetSqlDbMi, MigrateSqlServerSqlDbMi, ValidateSqlServerSqlDbMi, MigrateSqlServerSqlDbSync, ConnectToSourceSqlServerSync, ConnectToTargetSqlSync, GetUserTablesSqlSync, ValidateSqlServerSqlDbSync, ConnectToSourceMongoDb, ConnectToTargetMongoDb, MigrateMongoDb, ValidateMongoDbMigration, ConnectToTargetSqlDbMiSync, ValidateSqlServerSqlDbMiSync, MigrateSqlServerSqlDbMiSync

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5121a-131">-MigrationValidation</span><span class="sxs-lookup"><span data-stu-id="5121a-131">-MigrationValidation</span></span> 
<span data-ttu-id="5121a-132">Uppgifts svars objekt efter verifierings samtal, valfritt men rekommenderas.</span><span class="sxs-lookup"><span data-stu-id="5121a-132">Task response object by validation call, optional but recommended.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataMigration.Models.PSProjectTask
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5121a-133">-Vänta</span><span class="sxs-lookup"><span data-stu-id="5121a-133">-Wait</span></span>
<span data-ttu-id="5121a-134">Om uppgiften ska avslut ATS.</span><span class="sxs-lookup"><span data-stu-id="5121a-134">Whether to wait for task to finish.</span></span> <span data-ttu-id="5121a-135">Om flaggan är inställd kontrollerar du var en sekund tills aktiviteten slutar och återgår till användare aktivitetens egenskaper där utdata eller fel kan kontrol leras.</span><span class="sxs-lookup"><span data-stu-id="5121a-135">If the flag is set, checks every one seconds till the task finishes and return to user the task properties where output or error can be inspected.</span></span> 
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

### <span data-ttu-id="5121a-136">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="5121a-136">-Confirm</span></span>
<span data-ttu-id="5121a-137">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="5121a-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5121a-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5121a-138">-WhatIf</span></span>
<span data-ttu-id="5121a-139">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="5121a-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5121a-140">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="5121a-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5121a-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5121a-141">CommonParameters</span></span>
<span data-ttu-id="5121a-142">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5121a-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5121a-143">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5121a-143">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5121a-144">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="5121a-144">INPUTS</span></span>

### <span data-ttu-id="5121a-145">Microsoft. Azure. commands. DataMigration. Models. PSProject</span><span class="sxs-lookup"><span data-stu-id="5121a-145">Microsoft.Azure.Commands.DataMigration.Models.PSProject</span></span>

### <span data-ttu-id="5121a-146">System. String</span><span class="sxs-lookup"><span data-stu-id="5121a-146">System.String</span></span>

## <span data-ttu-id="5121a-147">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="5121a-147">OUTPUTS</span></span>

### <span data-ttu-id="5121a-148">Microsoft. Azure. commands. DataMigration. Models. PSProjectTask</span><span class="sxs-lookup"><span data-stu-id="5121a-148">Microsoft.Azure.Commands.DataMigration.Models.PSProjectTask</span></span>

## <span data-ttu-id="5121a-149">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="5121a-149">NOTES</span></span>

## <span data-ttu-id="5121a-150">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="5121a-150">RELATED LINKS</span></span>
