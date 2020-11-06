---
external help file: Microsoft.Azure.Commands.DataMigration.dll-Help.xml
Module Name: AzureRM.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datamigration/Get-AzureRmDataMigrationTask
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataMigration/Commands.DataMigration/help/Get-AzureRmDataMigrationTask.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataMigration/Commands.DataMigration/help/Get-AzureRmDataMigrationTask.md
ms.openlocfilehash: caab43824c63e73e7011c0377d0bd7665befe5dd
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93580127"
---
# <span data-ttu-id="ea310-101">Get-AzureRmDataMigrationTask</span><span class="sxs-lookup"><span data-stu-id="ea310-101">Get-AzureRmDataMigrationTask</span></span>

## <span data-ttu-id="ea310-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="ea310-102">SYNOPSIS</span></span>
<span data-ttu-id="ea310-103">Hämtar det PSProjectTask-objekt som är kopplat till en migrering för Azure Database migration service.</span><span class="sxs-lookup"><span data-stu-id="ea310-103">Retrieves the PSProjectTask object associated with an Azure Database Migration Service migration task.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ea310-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="ea310-104">SYNTAX</span></span>

### <span data-ttu-id="ea310-105">ListByComponent (standard)</span><span class="sxs-lookup"><span data-stu-id="ea310-105">ListByComponent (Default)</span></span>
```
Get-AzureRmDataMigrationTask -ResourceGroupName <String> -ServiceName <String> -ProjectName <String>
 [-TaskType <TaskTypeEnum>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ea310-106">ListByInputObject</span><span class="sxs-lookup"><span data-stu-id="ea310-106">ListByInputObject</span></span>
```
Get-AzureRmDataMigrationTask [-InputObject] <PSProject> [-TaskType <TaskTypeEnum>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ea310-107">GetByInputObject</span><span class="sxs-lookup"><span data-stu-id="ea310-107">GetByInputObject</span></span>
```
Get-AzureRmDataMigrationTask [-InputObject] <PSProject> -Name <String> [-Expand]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ea310-108">GetByInputObjectResultType</span><span class="sxs-lookup"><span data-stu-id="ea310-108">GetByInputObjectResultType</span></span>
```
Get-AzureRmDataMigrationTask [-InputObject] <PSProject> -Name <String> [-Expand] -ResultType <ResultTypeEnum>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ea310-109">ListByResourceId</span><span class="sxs-lookup"><span data-stu-id="ea310-109">ListByResourceId</span></span>
```
Get-AzureRmDataMigrationTask [-ResourceId] <String> [-TaskType <TaskTypeEnum>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ea310-110">GetByResourceId</span><span class="sxs-lookup"><span data-stu-id="ea310-110">GetByResourceId</span></span>
```
Get-AzureRmDataMigrationTask [-ResourceId] <String> -Name <String> [-Expand]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ea310-111">GetByResourceIdResultType</span><span class="sxs-lookup"><span data-stu-id="ea310-111">GetByResourceIdResultType</span></span>
```
Get-AzureRmDataMigrationTask [-ResourceId] <String> -Name <String> [-Expand] -ResultType <ResultTypeEnum>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ea310-112">GetByComponent</span><span class="sxs-lookup"><span data-stu-id="ea310-112">GetByComponent</span></span>
```
Get-AzureRmDataMigrationTask -ResourceGroupName <String> -ServiceName <String> -ProjectName <String>
 [-Name <String>] [-Expand] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ea310-113">GetByComponentResultType</span><span class="sxs-lookup"><span data-stu-id="ea310-113">GetByComponentResultType</span></span>
```
Get-AzureRmDataMigrationTask -ResourceGroupName <String> -ServiceName <String> -ProjectName <String>
 -Name <String> [-Expand] -ResultType <ResultTypeEnum> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="ea310-114">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="ea310-114">DESCRIPTION</span></span>
<span data-ttu-id="ea310-115">Get-AzureRmDataMigrationTask cmdlet hämtar egenskaperna som är kopplade till en migrerings aktivitet för Azure Database migration service.</span><span class="sxs-lookup"><span data-stu-id="ea310-115">The Get-AzureRmDataMigrationTask cmdlet retrieves the properties associated with an Azure Database Migration Service migration task.</span></span>

## <span data-ttu-id="ea310-116">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="ea310-116">EXAMPLES</span></span>

### <span data-ttu-id="ea310-117">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="ea310-117">Example 1</span></span>
```
PS C:\> Get -AzureRmDataMigrationTask -TaskName myTestTask -ServiceName myTestService -ProjectName MyTestProject -ResourceGroupName MyResourceGroup -Expand
```

<span data-ttu-id="ea310-118">Exemplet ovan visar hur du använder Get-AzureRmDataMigrationTask cmdlet för att hämta egenskaperna som är kopplade till en uppgraderings aktivitet för Azure Database migration baserat på aktivitets namnet som angavs som indataparameter</span><span class="sxs-lookup"><span data-stu-id="ea310-118">The above example illustrates the use of Get-AzureRmDataMigrationTask cmdlet to retrieve the properties associated with an Azure Database Migration Service migration task based on task name passed in as input parameter</span></span>

### <span data-ttu-id="ea310-119">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="ea310-119">Example 2</span></span>
```
PS C:\> Get -AzureRmDataMigrationTask -Project $myProject
```

<span data-ttu-id="ea310-120">I exemplet ovan visas hur du använder Get-AzureRmDataMigrationTask cmdlet för att hämta alla migreringsåtgärder som är associerade med PSProject-objekt som har överförts som indataparameter</span><span class="sxs-lookup"><span data-stu-id="ea310-120">The above example illustrates the use of Get-AzureRmDataMigrationTask cmdlet to retrieve all of the migration tasks associated with PSProject object passed in as input parameter</span></span>

## <span data-ttu-id="ea310-121">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="ea310-121">PARAMETERS</span></span>

### <span data-ttu-id="ea310-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ea310-122">-DefaultProfile</span></span>
<span data-ttu-id="ea310-123">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="ea310-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ea310-124">-Expandera</span><span class="sxs-lookup"><span data-stu-id="ea310-124">-Expand</span></span>
<span data-ttu-id="ea310-125">Visa utdata</span><span class="sxs-lookup"><span data-stu-id="ea310-125">Expand output</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: GetByInputObject, GetByResourceId, GetByComponent
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: GetByInputObjectResultType, GetByResourceIdResultType, GetByComponentResultType
Aliases:

Required: True
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ea310-126">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ea310-126">-InputObject</span></span>
<span data-ttu-id="ea310-127">PSProject-objekt.</span><span class="sxs-lookup"><span data-stu-id="ea310-127">PSProject Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataMigration.Models.PSProject
Parameter Sets: ListByInputObject
Aliases: Project

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

```yaml
Type: Microsoft.Azure.Commands.DataMigration.Models.PSProject
Parameter Sets: GetByInputObject, GetByInputObjectResultType
Aliases: Project

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ea310-128">-Namn</span><span class="sxs-lookup"><span data-stu-id="ea310-128">-Name</span></span>
<span data-ttu-id="ea310-129">Uppgiftens namn.</span><span class="sxs-lookup"><span data-stu-id="ea310-129">The name of the task.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByInputObject, GetByInputObjectResultType, GetByResourceId, GetByResourceIdResultType, GetByComponentResultType
Aliases: TaskName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: GetByComponent
Aliases: TaskName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ea310-130">-Projektetsnamn</span><span class="sxs-lookup"><span data-stu-id="ea310-130">-ProjectName</span></span>
<span data-ttu-id="ea310-131">Namnet på projektet.</span><span class="sxs-lookup"><span data-stu-id="ea310-131">The name of the project.</span></span>

```yaml
Type: System.String
Parameter Sets: ListByComponent, GetByComponent, GetByComponentResultType
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ea310-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ea310-132">-ResourceGroupName</span></span>
<span data-ttu-id="ea310-133">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="ea310-133">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: ListByComponent, GetByComponent, GetByComponentResultType
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ea310-134">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ea310-134">-ResourceId</span></span>
<span data-ttu-id="ea310-135">Projekt resurs-ID.</span><span class="sxs-lookup"><span data-stu-id="ea310-135">Project Resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: ListByResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: GetByResourceId, GetByResourceIdResultType
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ea310-136">-ResultType</span><span class="sxs-lookup"><span data-stu-id="ea310-136">-ResultType</span></span>
<span data-ttu-id="ea310-137">Expandera utdata från angiven resultat typ.</span><span class="sxs-lookup"><span data-stu-id="ea310-137">Expand output of given result type.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataMigration.Models.ResultTypeEnum
Parameter Sets: GetByInputObjectResultType, GetByResourceIdResultType, GetByComponentResultType
Aliases:
Accepted values: MigrationLevelOutput, DatabaseLevelOutput, TableLevelOutput, MigrationValidationOutput, MigrationValidationDatabaseLevelOutput, LoginLevelOutput, AgentJobLevelOutput

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ea310-138">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="ea310-138">-ServiceName</span></span>
<span data-ttu-id="ea310-139">Tjänst namn för databas migration.</span><span class="sxs-lookup"><span data-stu-id="ea310-139">Database Migration Service Name.</span></span>

```yaml
Type: System.String
Parameter Sets: ListByComponent, GetByComponent, GetByComponentResultType
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ea310-140">-TaskType</span><span class="sxs-lookup"><span data-stu-id="ea310-140">-TaskType</span></span>
<span data-ttu-id="ea310-141">Filtrera efter TaskType.</span><span class="sxs-lookup"><span data-stu-id="ea310-141">Filter by TaskType.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.DataMigration.Models.TaskTypeEnum]
Parameter Sets: ListByComponent, ListByInputObject, ListByResourceId
Aliases:
Accepted values: MigrateSqlServerSqlDb, ConnectToSourceSqlServer, ConnectToTargetSqlDb, GetUserTablesSql, ConnectToTargetSqlDbMi, MigrateSqlServerSqlDbMi, ValidateSqlServerSqlDbMi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ea310-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ea310-142">CommonParameters</span></span>
<span data-ttu-id="ea310-143">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ea310-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ea310-144">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ea310-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ea310-145">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="ea310-145">INPUTS</span></span>

### <span data-ttu-id="ea310-146">Microsoft. Azure. commands. DataMigration. Models. PSProject</span><span class="sxs-lookup"><span data-stu-id="ea310-146">Microsoft.Azure.Commands.DataMigration.Models.PSProject</span></span>
<span data-ttu-id="ea310-147">Parametrar: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="ea310-147">Parameters: InputObject (ByValue)</span></span>

### <span data-ttu-id="ea310-148">System. String</span><span class="sxs-lookup"><span data-stu-id="ea310-148">System.String</span></span>

## <span data-ttu-id="ea310-149">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="ea310-149">OUTPUTS</span></span>

### <span data-ttu-id="ea310-150">Microsoft. Azure. commands. DataMigration. Models. PSProjectTask</span><span class="sxs-lookup"><span data-stu-id="ea310-150">Microsoft.Azure.Commands.DataMigration.Models.PSProjectTask</span></span>

## <span data-ttu-id="ea310-151">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="ea310-151">NOTES</span></span>

## <span data-ttu-id="ea310-152">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="ea310-152">RELATED LINKS</span></span>
