---
external help file: Microsoft.Azure.Commands.DataMigration.dll-Help.xml
Module Name: AzureRM.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datamigration/get-azurermdatamigrationtask
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataMigration/Commands.DataMigration/help/Get-AzureRmDataMigrationTask.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataMigration/Commands.DataMigration/help/Get-AzureRmDataMigrationTask.md
ms.openlocfilehash: 5ca6edfa811a1b73cbdaae59e8d3b0e2f76cc15f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93576546"
---
# <span data-ttu-id="07e6f-101">Get-AzureRmDataMigrationTask</span><span class="sxs-lookup"><span data-stu-id="07e6f-101">Get-AzureRmDataMigrationTask</span></span>

## <span data-ttu-id="07e6f-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="07e6f-102">SYNOPSIS</span></span>
<span data-ttu-id="07e6f-103">Hämtar det PSProjectTask-objekt som är kopplat till en migrering för Azure Database migration service.</span><span class="sxs-lookup"><span data-stu-id="07e6f-103">Retrieves the PSProjectTask object associated with an Azure Database Migration Service migration task.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="07e6f-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="07e6f-104">SYNTAX</span></span>

### <span data-ttu-id="07e6f-105">ListByComponent (standard)</span><span class="sxs-lookup"><span data-stu-id="07e6f-105">ListByComponent (Default)</span></span>
```
Get-AzureRmDataMigrationTask -ResourceGroupName <String> -ServiceName <String> -ProjectName <String>
 [-TaskType <TaskTypeEnum>] [-DefaultProfile <IAzureContextContainer>]
```

### <span data-ttu-id="07e6f-106">ListByInputObject</span><span class="sxs-lookup"><span data-stu-id="07e6f-106">ListByInputObject</span></span>
```
Get-AzureRmDataMigrationTask [-InputObject] <PSProject> [-TaskType <TaskTypeEnum>]
 [-DefaultProfile <IAzureContextContainer>]
```

### <span data-ttu-id="07e6f-107">GetByInputObject</span><span class="sxs-lookup"><span data-stu-id="07e6f-107">GetByInputObject</span></span>
```
Get-AzureRmDataMigrationTask [-InputObject] <PSProject> -Name <String> [-Expand]
 [-DefaultProfile <IAzureContextContainer>]
```

### <span data-ttu-id="07e6f-108">GetByInputObjectResultType</span><span class="sxs-lookup"><span data-stu-id="07e6f-108">GetByInputObjectResultType</span></span>
```
Get-AzureRmDataMigrationTask [-InputObject] <PSProject> -Name <String> [-Expand] -ResultType <ResultTypeEnum>
 [-DefaultProfile <IAzureContextContainer>]
```

### <span data-ttu-id="07e6f-109">ListByResourceId</span><span class="sxs-lookup"><span data-stu-id="07e6f-109">ListByResourceId</span></span>
```
Get-AzureRmDataMigrationTask [-ResourceId] <String> [-TaskType <TaskTypeEnum>]
 [-DefaultProfile <IAzureContextContainer>]
```

### <span data-ttu-id="07e6f-110">GetByResourceId</span><span class="sxs-lookup"><span data-stu-id="07e6f-110">GetByResourceId</span></span>
```
Get-AzureRmDataMigrationTask [-ResourceId] <String> -Name <String> [-Expand]
 [-DefaultProfile <IAzureContextContainer>]
```

### <span data-ttu-id="07e6f-111">GetByResourceIdResultType</span><span class="sxs-lookup"><span data-stu-id="07e6f-111">GetByResourceIdResultType</span></span>
```
Get-AzureRmDataMigrationTask [-ResourceId] <String> -Name <String> [-Expand] -ResultType <ResultTypeEnum>
 [-DefaultProfile <IAzureContextContainer>]
```

### <span data-ttu-id="07e6f-112">GetByComponent</span><span class="sxs-lookup"><span data-stu-id="07e6f-112">GetByComponent</span></span>
```
Get-AzureRmDataMigrationTask -ResourceGroupName <String> -ServiceName <String> -ProjectName <String>
 [-Name <String>] [-Expand] [-DefaultProfile <IAzureContextContainer>]
```

### <span data-ttu-id="07e6f-113">GetByComponentResultType</span><span class="sxs-lookup"><span data-stu-id="07e6f-113">GetByComponentResultType</span></span>
```
Get-AzureRmDataMigrationTask -ResourceGroupName <String> -ServiceName <String> -ProjectName <String>
 -Name <String> [-Expand] -ResultType <ResultTypeEnum> [-DefaultProfile <IAzureContextContainer>]
```

## <span data-ttu-id="07e6f-114">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="07e6f-114">DESCRIPTION</span></span>
<span data-ttu-id="07e6f-115">Get-AzureRmDataMigrationTask cmdlet hämtar egenskaperna som är kopplade till en migrerings aktivitet för Azure Database migration service.</span><span class="sxs-lookup"><span data-stu-id="07e6f-115">The Get-AzureRmDataMigrationTask cmdlet retrieves the properties associated with an Azure Database Migration Service migration task.</span></span>

## <span data-ttu-id="07e6f-116">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="07e6f-116">EXAMPLES</span></span>

### <span data-ttu-id="07e6f-117">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="07e6f-117">Example 1</span></span>
```
PS C:\> Get -AzureRmDataMigrationTask -TaskName myTestTask -ServiceName myTestService -ProjectName MyTestProject -ResourceGroupName MyResourceGroup -Expand
```

<span data-ttu-id="07e6f-118">Exemplet ovan visar hur du använder Get-AzureRmDataMigrationTask cmdlet för att hämta egenskaperna som är kopplade till en uppgraderings aktivitet för Azure Database migration baserat på aktivitets namnet som angavs som indataparameter</span><span class="sxs-lookup"><span data-stu-id="07e6f-118">The above example illustrates the use of Get-AzureRmDataMigrationTask cmdlet to retrieve the properties associated with an Azure Database Migration Service migration task based on task name passed in as input parameter</span></span>

### <span data-ttu-id="07e6f-119">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="07e6f-119">Example 2</span></span>
```
PS C:\> Get -AzureRmDataMigrationTask -Project $myProject
```

<span data-ttu-id="07e6f-120">I exemplet ovan visas hur du använder Get-AzureRmDataMigrationTask cmdlet för att hämta alla migreringsåtgärder som är associerade med PSProject-objekt som har överförts som indataparameter</span><span class="sxs-lookup"><span data-stu-id="07e6f-120">The above example illustrates the use of Get-AzureRmDataMigrationTask cmdlet to retrieve all of the migration tasks associated with PSProject object passed in as input parameter</span></span>

## <span data-ttu-id="07e6f-121">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="07e6f-121">PARAMETERS</span></span>

### <span data-ttu-id="07e6f-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="07e6f-122">-DefaultProfile</span></span>
<span data-ttu-id="07e6f-123">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="07e6f-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="07e6f-124">-Expandera</span><span class="sxs-lookup"><span data-stu-id="07e6f-124">-Expand</span></span>
<span data-ttu-id="07e6f-125">Visa utdata</span><span class="sxs-lookup"><span data-stu-id="07e6f-125">Expand output</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: GetByInputObject, GetByResourceId, GetByComponent
Aliases: 

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: SwitchParameter
Parameter Sets: GetByInputObjectResultType, GetByResourceIdResultType, GetByComponentResultType
Aliases: 

Required: True
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="07e6f-126">-InputObject</span><span class="sxs-lookup"><span data-stu-id="07e6f-126">-InputObject</span></span>
<span data-ttu-id="07e6f-127">PSProject-objekt.</span><span class="sxs-lookup"><span data-stu-id="07e6f-127">PSProject Object.</span></span>

```yaml
Type: PSProject
Parameter Sets: ListByInputObject
Aliases: Project

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

```yaml
Type: PSProject
Parameter Sets: GetByInputObject, GetByInputObjectResultType
Aliases: Project

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="07e6f-128">-Namn</span><span class="sxs-lookup"><span data-stu-id="07e6f-128">-Name</span></span>
<span data-ttu-id="07e6f-129">Uppgiftens namn.</span><span class="sxs-lookup"><span data-stu-id="07e6f-129">The name of the task.</span></span>

```yaml
Type: String
Parameter Sets: GetByInputObject, GetByInputObjectResultType, GetByResourceId, GetByResourceIdResultType, GetByComponentResultType
Aliases: TaskName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: GetByComponent
Aliases: TaskName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="07e6f-130">-Projektetsnamn</span><span class="sxs-lookup"><span data-stu-id="07e6f-130">-ProjectName</span></span>
<span data-ttu-id="07e6f-131">Namnet på projektet.</span><span class="sxs-lookup"><span data-stu-id="07e6f-131">The name of the project.</span></span>

```yaml
Type: String
Parameter Sets: ListByComponent, GetByComponent, GetByComponentResultType
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="07e6f-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="07e6f-132">-ResourceGroupName</span></span>
<span data-ttu-id="07e6f-133">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="07e6f-133">The name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: ListByComponent, GetByComponent, GetByComponentResultType
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="07e6f-134">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="07e6f-134">-ResourceId</span></span>
<span data-ttu-id="07e6f-135">Projekt resurs-ID.</span><span class="sxs-lookup"><span data-stu-id="07e6f-135">Project Resource Id.</span></span>

```yaml
Type: String
Parameter Sets: ListByResourceId
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: GetByResourceId, GetByResourceIdResultType
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="07e6f-136">-ResultType</span><span class="sxs-lookup"><span data-stu-id="07e6f-136">-ResultType</span></span>
<span data-ttu-id="07e6f-137">Expandera utdata från angiven resultat typ.</span><span class="sxs-lookup"><span data-stu-id="07e6f-137">Expand output of given result type.</span></span>

```yaml
Type: ResultTypeEnum
Parameter Sets: GetByInputObjectResultType, GetByResourceIdResultType, GetByComponentResultType
Aliases: 
Accepted values: MigrationLevelOutput, DatabaseLevelOutput, TableLevelOutput, MigrationValidationOutput, MigrationValidationDatabaseLevelOutput

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="07e6f-138">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="07e6f-138">-ServiceName</span></span>
<span data-ttu-id="07e6f-139">Tjänst namn för data migration.</span><span class="sxs-lookup"><span data-stu-id="07e6f-139">Data Migration Service Name.</span></span>

```yaml
Type: String
Parameter Sets: ListByComponent, GetByComponent, GetByComponentResultType
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="07e6f-140">-TaskType</span><span class="sxs-lookup"><span data-stu-id="07e6f-140">-TaskType</span></span>
<span data-ttu-id="07e6f-141">Filtrera efter TaskType.</span><span class="sxs-lookup"><span data-stu-id="07e6f-141">Filter by TaskType.</span></span>

```yaml
Type: TaskTypeEnum
Parameter Sets: ListByComponent, ListByInputObject, ListByResourceId
Aliases: 
Accepted values: MigrateSqlServerSqlDb, ConnectToSourceSqlServer, ConnectToTargetSqlDb, GetUserTablesSql

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

## <span data-ttu-id="07e6f-142">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="07e6f-142">INPUTS</span></span>

### <span data-ttu-id="07e6f-143">Microsoft. Azure. commands. DataMigration. Models. PSProject</span><span class="sxs-lookup"><span data-stu-id="07e6f-143">Microsoft.Azure.Commands.DataMigration.Models.PSProject</span></span>
<span data-ttu-id="07e6f-144">System. String</span><span class="sxs-lookup"><span data-stu-id="07e6f-144">System.String</span></span>

## <span data-ttu-id="07e6f-145">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="07e6f-145">OUTPUTS</span></span>

### <span data-ttu-id="07e6f-146">System. Collections. Generic. IList ' 1 [[Microsoft. Azure. commands. DataMigration. Models. PSProjectTask, Microsoft. Azure. commands. DataMigration, version = 0.1.0.0, Culture = neutralt, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="07e6f-146">System.Collections.Generic.IList\`1[[Microsoft.Azure.Commands.DataMigration.Models.PSProjectTask, Microsoft.Azure.Commands.DataMigration, Version=0.1.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="07e6f-147">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="07e6f-147">NOTES</span></span>

## <span data-ttu-id="07e6f-148">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="07e6f-148">RELATED LINKS</span></span>

