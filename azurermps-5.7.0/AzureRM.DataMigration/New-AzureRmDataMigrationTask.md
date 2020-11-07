---
external help file: Microsoft.Azure.Commands.DataMigration.dll-Help.xml
Module Name: AzureRM.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datamigration/new-azurermdatamigrationtask
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataMigration/Commands.DataMigration/help/New-AzureRmDataMigrationTask.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataMigration/Commands.DataMigration/help/New-AzureRmDataMigrationTask.md
ms.openlocfilehash: 1bdf66311acd1b8ff1de43b5ea199d5d0a17c394
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93755879"
---
# <span data-ttu-id="54b8e-101">New-AzureRmDataMigrationTask</span><span class="sxs-lookup"><span data-stu-id="54b8e-101">New-AzureRmDataMigrationTask</span></span>

## <span data-ttu-id="54b8e-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="54b8e-102">SYNOPSIS</span></span>
<span data-ttu-id="54b8e-103">Skapar och startar en datamigrering i Azure Database migration service.</span><span class="sxs-lookup"><span data-stu-id="54b8e-103">Creates and starts a data migration task in the Azure Database Migration Service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="54b8e-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="54b8e-104">SYNTAX</span></span>

### <span data-ttu-id="54b8e-105">ComponentNameParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="54b8e-105">ComponentNameParameterSet (Default)</span></span>
```
New-AzureRmDataMigrationTask -TaskType <TaskTypeEnum> -ResourceGroupName <String> -ServiceName <String>
 -ProjectName <String> -Name <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="54b8e-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="54b8e-106">ComponentObjectParameterSet</span></span>
```
New-AzureRmDataMigrationTask [-InputObject] <PSProject> -TaskType <TaskTypeEnum> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="54b8e-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="54b8e-107">ResourceIdParameterSet</span></span>
```
New-AzureRmDataMigrationTask [-ResourceId] <String> -TaskType <TaskTypeEnum> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
```

## <span data-ttu-id="54b8e-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="54b8e-108">DESCRIPTION</span></span>
<span data-ttu-id="54b8e-109">New-AzureRmDataMigrationTask cmdlet skapar datamigrering.</span><span class="sxs-lookup"><span data-stu-id="54b8e-109">The New-AzureRmDataMigrationTask cmdlet creates data migration task.</span></span> <span data-ttu-id="54b8e-110">Denna cmdlet tar upp parametrar för aktivitets typs uppräkna ren, Azure resurs grupp, namnet på associerade Azure Data Migration-tjänsten och Project som indata.</span><span class="sxs-lookup"><span data-stu-id="54b8e-110">This cmdlet takes in parameters for Task Type enumerator, Azure Resource Group, name of associated Azure Data Migration Service and Project as input.</span></span> 

## <span data-ttu-id="54b8e-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="54b8e-111">EXAMPLES</span></span>

### <span data-ttu-id="54b8e-112">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="54b8e-112">Example 1</span></span>
```
PS C:\> New-AzureRmDmsTask -TaskType MigrateSqlServerSqlDb -ResourceGroupName myResourceGroup -ServiceName TestService -ProjectName myDMSProject -TaskName MyMigrationTask -SourceConnection $sourceConnInfo -SourceCred $sourceCred -TargetConnection $targetConnInfo -TargetCred $targetCred -SelectedDatabase  $selectedDbs
```
<span data-ttu-id="54b8e-113">Det här exemplet visar hur du skapar en ny datamigrerings aktivitet med namnet MyMigrationTask i projektet med namnet myDMSProject och tjänsten som heter TestService.</span><span class="sxs-lookup"><span data-stu-id="54b8e-113">This example script shows how to create a new Data Migration Task named MyMigrationTask in the project named myDMSProject and service named TestService.</span></span> 

## <span data-ttu-id="54b8e-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="54b8e-114">PARAMETERS</span></span>

### <span data-ttu-id="54b8e-115">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="54b8e-115">-Confirm</span></span>
<span data-ttu-id="54b8e-116">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="54b8e-116">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="54b8e-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="54b8e-117">-DefaultProfile</span></span>
<span data-ttu-id="54b8e-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="54b8e-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="54b8e-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="54b8e-119">-InputObject</span></span>
<span data-ttu-id="54b8e-120">PSProject-objekt.</span><span class="sxs-lookup"><span data-stu-id="54b8e-120">PSProject Object.</span></span>

```yaml
Type: PSProject
Parameter Sets: ComponentObjectParameterSet
Aliases: Project

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="54b8e-121">-Namn</span><span class="sxs-lookup"><span data-stu-id="54b8e-121">-Name</span></span>
<span data-ttu-id="54b8e-122">Uppgiftens namn.</span><span class="sxs-lookup"><span data-stu-id="54b8e-122">The name of the task.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: TaskName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="54b8e-123">-Projektetsnamn</span><span class="sxs-lookup"><span data-stu-id="54b8e-123">-ProjectName</span></span>
<span data-ttu-id="54b8e-124">Namnet på projektet.</span><span class="sxs-lookup"><span data-stu-id="54b8e-124">The name of the project.</span></span>

```yaml
Type: String
Parameter Sets: ComponentNameParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="54b8e-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="54b8e-125">-ResourceGroupName</span></span>
<span data-ttu-id="54b8e-126">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="54b8e-126">The name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: ComponentNameParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="54b8e-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="54b8e-127">-ResourceId</span></span>
<span data-ttu-id="54b8e-128">Projekt resurs-ID.</span><span class="sxs-lookup"><span data-stu-id="54b8e-128">Project Resource Id.</span></span>

```yaml
Type: String
Parameter Sets: ResourceIdParameterSet
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="54b8e-129">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="54b8e-129">-ServiceName</span></span>
<span data-ttu-id="54b8e-130">Tjänst namn för data migration.</span><span class="sxs-lookup"><span data-stu-id="54b8e-130">Data Migration Service Name.</span></span>

```yaml
Type: String
Parameter Sets: ComponentNameParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="54b8e-131">-TaskType</span><span class="sxs-lookup"><span data-stu-id="54b8e-131">-TaskType</span></span>
<span data-ttu-id="54b8e-132">Aktivitets typ.</span><span class="sxs-lookup"><span data-stu-id="54b8e-132">Task Type.</span></span>

```yaml
Type: TaskTypeEnum
Parameter Sets: (All)
Aliases: 
Accepted values: MigrateSqlServerSqlDb, ConnectToSourceSqlServer, ConnectToTargetSqlDb, GetUserTablesSql

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="54b8e-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="54b8e-133">-WhatIf</span></span>
<span data-ttu-id="54b8e-134">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="54b8e-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="54b8e-135">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="54b8e-135">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

## <span data-ttu-id="54b8e-136">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="54b8e-136">INPUTS</span></span>

### <span data-ttu-id="54b8e-137">Microsoft. Azure. commands. DataMigration. Models. PSProject</span><span class="sxs-lookup"><span data-stu-id="54b8e-137">Microsoft.Azure.Commands.DataMigration.Models.PSProject</span></span>
<span data-ttu-id="54b8e-138">System. String</span><span class="sxs-lookup"><span data-stu-id="54b8e-138">System.String</span></span>


## <span data-ttu-id="54b8e-139">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="54b8e-139">OUTPUTS</span></span>

### <span data-ttu-id="54b8e-140">Microsoft. Azure. commands. DataMigration. Models. PSProjectTask</span><span class="sxs-lookup"><span data-stu-id="54b8e-140">Microsoft.Azure.Commands.DataMigration.Models.PSProjectTask</span></span>


## <span data-ttu-id="54b8e-141">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="54b8e-141">NOTES</span></span>

## <span data-ttu-id="54b8e-142">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="54b8e-142">RELATED LINKS</span></span>


