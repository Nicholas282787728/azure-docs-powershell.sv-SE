---
external help file: Microsoft.Azure.Commands.DataMigration.dll-Help.xml
Module Name: AzureRM.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datamigration/remove-azurermdatamigrationtask
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataMigration/Commands.DataMigration/help/Remove-AzureRmDataMigrationTask.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataMigration/Commands.DataMigration/help/Remove-AzureRmDataMigrationTask.md
ms.openlocfilehash: d192b7f422557b4d4373f794e98cdb2556db3c63
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93579547"
---
# <span data-ttu-id="4f099-101">Remove-AzureRmDataMigrationTask</span><span class="sxs-lookup"><span data-stu-id="4f099-101">Remove-AzureRmDataMigrationTask</span></span>

## <span data-ttu-id="4f099-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="4f099-102">SYNOPSIS</span></span>
<span data-ttu-id="4f099-103">Tar bort en uppgift för Azure Database migration från Azure.</span><span class="sxs-lookup"><span data-stu-id="4f099-103">Removes an Azure Database Migration Service task from Azure.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4f099-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="4f099-104">SYNTAX</span></span>

### <span data-ttu-id="4f099-105">ComponentNameParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="4f099-105">ComponentNameParameterSet (Default)</span></span>
```
Remove-AzureRmDataMigrationTask -ResourceGroupName <String> -ServiceName <String> -ProjectName <String>
 -Name <String> [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="4f099-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="4f099-106">ComponentObjectParameterSet</span></span>
```
Remove-AzureRmDataMigrationTask [-InputObject] <PSProjectTask> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="4f099-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="4f099-107">ResourceIdParameterSet</span></span>
```
Remove-AzureRmDataMigrationTask [-ResourceId] <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
```

## <span data-ttu-id="4f099-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="4f099-108">DESCRIPTION</span></span>
<span data-ttu-id="4f099-109">Remove-AzureRmDataMigrationTask cmdlet tar bort en uppgift för Azure Database migration från Azure.</span><span class="sxs-lookup"><span data-stu-id="4f099-109">The Remove-AzureRmDataMigrationTask cmdlet removes an Azure Database Migration Service task from Azure.</span></span>

## <span data-ttu-id="4f099-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="4f099-110">EXAMPLES</span></span>

### <span data-ttu-id="4f099-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="4f099-111">Example 1</span></span>
```
PS C:\> Remove-AzureRmDataMigrationTask –TaskName TestTask -ProjectName myTestProject -ServiceName MyTestService
 -ResourceGroupName MyResourceGroup

```

<span data-ttu-id="4f099-112">I föregående exempel tas en Azure Database migration service-uppgift med namnet TestTask från Azure baserat på uppgifts namns parametern.</span><span class="sxs-lookup"><span data-stu-id="4f099-112">The preceding example removes an Azure Database Migration Service task named TestTask from Azure based on task name parameter.</span></span>

### <span data-ttu-id="4f099-113">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="4f099-113">Example 2</span></span>
```
PS C:\> Remove-AzureRmDataMigrationTask –InputObject $TestTask

```

<span data-ttu-id="4f099-114">Föregående exempel tar bort en Azure Database migration service-uppgift baserat på PSProjectTask-objekt som skickades.</span><span class="sxs-lookup"><span data-stu-id="4f099-114">The preceding example removes an Azure Database Migration Service task based on PSProjectTask object passed in.</span></span>

## <span data-ttu-id="4f099-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="4f099-115">PARAMETERS</span></span>

### <span data-ttu-id="4f099-116">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="4f099-116">-Confirm</span></span>
<span data-ttu-id="4f099-117">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="4f099-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4f099-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4f099-118">-DefaultProfile</span></span>
<span data-ttu-id="4f099-119">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="4f099-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4f099-120">-Force</span><span class="sxs-lookup"><span data-stu-id="4f099-120">-Force</span></span>
<span data-ttu-id="4f099-121">Hoppa över bekräftelse meddelande för att utföra åtgärden</span><span class="sxs-lookup"><span data-stu-id="4f099-121">Skip confirmation message for performing the action</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4f099-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4f099-122">-InputObject</span></span>
<span data-ttu-id="4f099-123">PSProjectTask-objekt.</span><span class="sxs-lookup"><span data-stu-id="4f099-123">PSProjectTask Object.</span></span>

```yaml
Type: PSProjectTask
Parameter Sets: ComponentObjectParameterSet
Aliases: ProjectTask

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4f099-124">-Namn</span><span class="sxs-lookup"><span data-stu-id="4f099-124">-Name</span></span>
<span data-ttu-id="4f099-125">Uppgiftens namn.</span><span class="sxs-lookup"><span data-stu-id="4f099-125">The name of the task.</span></span>

```yaml
Type: String
Parameter Sets: ComponentNameParameterSet
Aliases: TaskName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4f099-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="4f099-126">-PassThru</span></span>
<span data-ttu-id="4f099-127">Returnerar TRUE/FALSE.</span><span class="sxs-lookup"><span data-stu-id="4f099-127">Returns an true/false.</span></span>
<span data-ttu-id="4f099-128">Denna cmdlet genererar som standard inga utdata.</span><span class="sxs-lookup"><span data-stu-id="4f099-128">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4f099-129">-Projektetsnamn</span><span class="sxs-lookup"><span data-stu-id="4f099-129">-ProjectName</span></span>
<span data-ttu-id="4f099-130">Namnet på projektet.</span><span class="sxs-lookup"><span data-stu-id="4f099-130">The name of the project.</span></span>

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

### <span data-ttu-id="4f099-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4f099-131">-ResourceGroupName</span></span>
<span data-ttu-id="4f099-132">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="4f099-132">The name of the resource group.</span></span>

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

### <span data-ttu-id="4f099-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="4f099-133">-ResourceId</span></span>
<span data-ttu-id="4f099-134">Projekt resurs-ID.</span><span class="sxs-lookup"><span data-stu-id="4f099-134">Project Resource Id.</span></span>

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

### <span data-ttu-id="4f099-135">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="4f099-135">-ServiceName</span></span>
<span data-ttu-id="4f099-136">Tjänst namn för data migration.</span><span class="sxs-lookup"><span data-stu-id="4f099-136">Data Migration Service Name.</span></span>

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

### <span data-ttu-id="4f099-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4f099-137">-WhatIf</span></span>
<span data-ttu-id="4f099-138">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="4f099-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4f099-139">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="4f099-139">The cmdlet is not run.</span></span>

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

## <span data-ttu-id="4f099-140">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="4f099-140">INPUTS</span></span>

### <span data-ttu-id="4f099-141">Microsoft. Azure. commands. DataMigration. Models. PSProjectTask</span><span class="sxs-lookup"><span data-stu-id="4f099-141">Microsoft.Azure.Commands.DataMigration.Models.PSProjectTask</span></span>
<span data-ttu-id="4f099-142">System. String</span><span class="sxs-lookup"><span data-stu-id="4f099-142">System.String</span></span>


## <span data-ttu-id="4f099-143">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="4f099-143">OUTPUTS</span></span>

### <span data-ttu-id="4f099-144">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="4f099-144">System.Boolean</span></span>


## <span data-ttu-id="4f099-145">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="4f099-145">NOTES</span></span>

## <span data-ttu-id="4f099-146">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="4f099-146">RELATED LINKS</span></span>


