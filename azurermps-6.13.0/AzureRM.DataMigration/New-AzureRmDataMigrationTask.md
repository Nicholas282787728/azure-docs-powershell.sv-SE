---
external help file: Microsoft.Azure.Commands.DataMigration.dll-Help.xml
Module Name: AzureRM.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datamigration/New-AzureRmDataMigrationTask
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataMigration/Commands.DataMigration/help/New-AzureRmDataMigrationTask.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataMigration/Commands.DataMigration/help/New-AzureRmDataMigrationTask.md
ms.openlocfilehash: 8352f7a63e40986e27c4b521dca58aaf003679bc
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93583528"
---
# <span data-ttu-id="b719c-101">New-AzureRmDataMigrationTask</span><span class="sxs-lookup"><span data-stu-id="b719c-101">New-AzureRmDataMigrationTask</span></span>

## <span data-ttu-id="b719c-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="b719c-102">SYNOPSIS</span></span>
<span data-ttu-id="b719c-103">Skapar och startar en datamigrering i Azure Database migration service.</span><span class="sxs-lookup"><span data-stu-id="b719c-103">Creates and starts a data migration task in the Azure Database Migration Service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b719c-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="b719c-104">SYNTAX</span></span>

### <span data-ttu-id="b719c-105">ComponentNameParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="b719c-105">ComponentNameParameterSet (Default)</span></span>
```
New-AzureRmDataMigrationTask -TaskType <TaskTypeEnum> -ResourceGroupName <String> -ServiceName <String>
 -ProjectName <String> -Name <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="b719c-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="b719c-106">ComponentObjectParameterSet</span></span>
```
New-AzureRmDataMigrationTask [-InputObject] <PSProject> -TaskType <TaskTypeEnum> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b719c-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="b719c-107">ResourceIdParameterSet</span></span>
```
New-AzureRmDataMigrationTask [-ResourceId] <String> -TaskType <TaskTypeEnum> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b719c-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="b719c-108">DESCRIPTION</span></span>
<span data-ttu-id="b719c-109">New-AzureRmDataMigrationTask cmdlet skapar datamigrering.</span><span class="sxs-lookup"><span data-stu-id="b719c-109">The New-AzureRmDataMigrationTask cmdlet creates data migration task.</span></span> <span data-ttu-id="b719c-110">Denna cmdlet tar upp parametrar för aktivitets typens uppräknare, Azure resurs grupp, namnet på den associerade tjänsten för Azure Database migration och Project som indata.</span><span class="sxs-lookup"><span data-stu-id="b719c-110">This cmdlet takes in parameters for Task Type enumerator, Azure Resource Group, name of associated Azure Database Migration Service and Project as input.</span></span> 

## <span data-ttu-id="b719c-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="b719c-111">EXAMPLES</span></span>

### <span data-ttu-id="b719c-112">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="b719c-112">Example 1</span></span>
```
PS C:\> New-AzureRmDmsTask -TaskType MigrateSqlServerSqlDb -ResourceGroupName myResourceGroup -ServiceName TestService -ProjectName myDMSProject -TaskName MyMigrationTask -SourceConnection $sourceConnInfo -SourceCred $sourceCred -TargetConnection $targetConnInfo -TargetCred $targetCred -SelectedDatabase  $selectedDbs
```

<span data-ttu-id="b719c-113">Det här exemplet visar hur du skapar en ny datamigrerings aktivitet med namnet MyMigrationTask i projektet med namnet myDMSProject och tjänsten som heter TestService.</span><span class="sxs-lookup"><span data-stu-id="b719c-113">This example script shows how to create a new Data Migration Task named MyMigrationTask in the project named myDMSProject and service named TestService.</span></span> 

## <span data-ttu-id="b719c-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="b719c-114">PARAMETERS</span></span>

### <span data-ttu-id="b719c-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b719c-115">-DefaultProfile</span></span>
<span data-ttu-id="b719c-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="b719c-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b719c-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b719c-117">-InputObject</span></span>
<span data-ttu-id="b719c-118">PSProject-objekt.</span><span class="sxs-lookup"><span data-stu-id="b719c-118">PSProject Object.</span></span>

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

### <span data-ttu-id="b719c-119">-Namn</span><span class="sxs-lookup"><span data-stu-id="b719c-119">-Name</span></span>
<span data-ttu-id="b719c-120">Uppgiftens namn.</span><span class="sxs-lookup"><span data-stu-id="b719c-120">The name of the task.</span></span>

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

### <span data-ttu-id="b719c-121">-Projektetsnamn</span><span class="sxs-lookup"><span data-stu-id="b719c-121">-ProjectName</span></span>
<span data-ttu-id="b719c-122">Namnet på projektet.</span><span class="sxs-lookup"><span data-stu-id="b719c-122">The name of the project.</span></span>

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

### <span data-ttu-id="b719c-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b719c-123">-ResourceGroupName</span></span>
<span data-ttu-id="b719c-124">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="b719c-124">The name of the resource group.</span></span>

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

### <span data-ttu-id="b719c-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b719c-125">-ResourceId</span></span>
<span data-ttu-id="b719c-126">Projekt resurs-ID.</span><span class="sxs-lookup"><span data-stu-id="b719c-126">Project Resource Id.</span></span>

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

### <span data-ttu-id="b719c-127">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="b719c-127">-ServiceName</span></span>
<span data-ttu-id="b719c-128">Tjänst namn för databas migration.</span><span class="sxs-lookup"><span data-stu-id="b719c-128">Database Migration Service Name.</span></span>

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

### <span data-ttu-id="b719c-129">-TaskType</span><span class="sxs-lookup"><span data-stu-id="b719c-129">-TaskType</span></span>
<span data-ttu-id="b719c-130">Aktivitets typ.</span><span class="sxs-lookup"><span data-stu-id="b719c-130">Task Type.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataMigration.Models.TaskTypeEnum
Parameter Sets: (All)
Aliases:
Accepted values: MigrateSqlServerSqlDb, ConnectToSourceSqlServer, ConnectToTargetSqlDb, GetUserTablesSql, ConnectToTargetSqlDbMi, MigrateSqlServerSqlDbMi, ValidateSqlServerSqlDbMi

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b719c-131">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="b719c-131">-Confirm</span></span>
<span data-ttu-id="b719c-132">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="b719c-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b719c-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b719c-133">-WhatIf</span></span>
<span data-ttu-id="b719c-134">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="b719c-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b719c-135">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="b719c-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b719c-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b719c-136">CommonParameters</span></span>
<span data-ttu-id="b719c-137">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b719c-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b719c-138">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b719c-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b719c-139">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="b719c-139">INPUTS</span></span>

### <span data-ttu-id="b719c-140">Microsoft. Azure. commands. DataMigration. Models. PSProject</span><span class="sxs-lookup"><span data-stu-id="b719c-140">Microsoft.Azure.Commands.DataMigration.Models.PSProject</span></span>
<span data-ttu-id="b719c-141">Parametrar: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="b719c-141">Parameters: InputObject (ByValue)</span></span>

### <span data-ttu-id="b719c-142">System. String</span><span class="sxs-lookup"><span data-stu-id="b719c-142">System.String</span></span>

## <span data-ttu-id="b719c-143">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="b719c-143">OUTPUTS</span></span>

### <span data-ttu-id="b719c-144">Microsoft. Azure. commands. DataMigration. Models. PSProjectTask</span><span class="sxs-lookup"><span data-stu-id="b719c-144">Microsoft.Azure.Commands.DataMigration.Models.PSProjectTask</span></span>

## <span data-ttu-id="b719c-145">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="b719c-145">NOTES</span></span>

## <span data-ttu-id="b719c-146">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="b719c-146">RELATED LINKS</span></span>
