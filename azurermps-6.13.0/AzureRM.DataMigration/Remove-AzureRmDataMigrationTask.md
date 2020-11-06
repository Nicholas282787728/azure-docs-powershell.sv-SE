---
external help file: Microsoft.Azure.Commands.DataMigration.dll-Help.xml
Module Name: AzureRM.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datamigration/Remove-AzureRmDataMigrationTask
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataMigration/Commands.DataMigration/help/Remove-AzureRmDataMigrationTask.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataMigration/Commands.DataMigration/help/Remove-AzureRmDataMigrationTask.md
ms.openlocfilehash: 295ac647bcbe04e26e761e4fdf8fe2bd30282218
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93585016"
---
# <span data-ttu-id="0b53c-101">Remove-AzureRmDataMigrationTask</span><span class="sxs-lookup"><span data-stu-id="0b53c-101">Remove-AzureRmDataMigrationTask</span></span>

## <span data-ttu-id="0b53c-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="0b53c-102">SYNOPSIS</span></span>
<span data-ttu-id="0b53c-103">Tar bort en uppgift för Azure Database migration från Azure.</span><span class="sxs-lookup"><span data-stu-id="0b53c-103">Removes an Azure Database Migration Service task from Azure.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0b53c-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="0b53c-104">SYNTAX</span></span>

### <span data-ttu-id="0b53c-105">ComponentNameParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="0b53c-105">ComponentNameParameterSet (Default)</span></span>
```
Remove-AzureRmDataMigrationTask -ResourceGroupName <String> -ServiceName <String> -ProjectName <String>
 -Name <String> [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="0b53c-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="0b53c-106">ComponentObjectParameterSet</span></span>
```
Remove-AzureRmDataMigrationTask [-InputObject] <PSProjectTask> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0b53c-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="0b53c-107">ResourceIdParameterSet</span></span>
```
Remove-AzureRmDataMigrationTask [-ResourceId] <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0b53c-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="0b53c-108">DESCRIPTION</span></span>
<span data-ttu-id="0b53c-109">Remove-AzureRmDataMigrationTask cmdlet tar bort en uppgift för Azure Database migration från Azure.</span><span class="sxs-lookup"><span data-stu-id="0b53c-109">The Remove-AzureRmDataMigrationTask cmdlet removes an Azure Database Migration Service task from Azure.</span></span>

## <span data-ttu-id="0b53c-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="0b53c-110">EXAMPLES</span></span>

### <span data-ttu-id="0b53c-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="0b53c-111">Example 1</span></span>
```
PS C:\> Remove-AzureRmDataMigrationTask -TaskName TestTask -ProjectName myTestProject -ServiceName MyTestService
 -ResourceGroupName MyResourceGroup
```

<span data-ttu-id="0b53c-112">I föregående exempel tas en Azure Database migration service-uppgift med namnet TestTask från Azure baserat på uppgifts namns parametern.</span><span class="sxs-lookup"><span data-stu-id="0b53c-112">The preceding example removes an Azure Database Migration Service task named TestTask from Azure based on task name parameter.</span></span>

### <span data-ttu-id="0b53c-113">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="0b53c-113">Example 2</span></span>
```
PS C:\> Remove-AzureRmDataMigrationTask -InputObject $TestTask
```

<span data-ttu-id="0b53c-114">Föregående exempel tar bort en Azure Database migration service-uppgift baserat på PSProjectTask-objekt som skickades.</span><span class="sxs-lookup"><span data-stu-id="0b53c-114">The preceding example removes an Azure Database Migration Service task based on PSProjectTask object passed in.</span></span>

## <span data-ttu-id="0b53c-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="0b53c-115">PARAMETERS</span></span>

### <span data-ttu-id="0b53c-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0b53c-116">-DefaultProfile</span></span>
<span data-ttu-id="0b53c-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="0b53c-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0b53c-118">-Force</span><span class="sxs-lookup"><span data-stu-id="0b53c-118">-Force</span></span>
<span data-ttu-id="0b53c-119">Hoppa över bekräftelse meddelande för att utföra åtgärden</span><span class="sxs-lookup"><span data-stu-id="0b53c-119">Skip confirmation message for performing the action</span></span>

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

### <span data-ttu-id="0b53c-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0b53c-120">-InputObject</span></span>
<span data-ttu-id="0b53c-121">PSProjectTask-objekt.</span><span class="sxs-lookup"><span data-stu-id="0b53c-121">PSProjectTask Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataMigration.Models.PSProjectTask
Parameter Sets: ComponentObjectParameterSet
Aliases: ProjectTask

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0b53c-122">-Namn</span><span class="sxs-lookup"><span data-stu-id="0b53c-122">-Name</span></span>
<span data-ttu-id="0b53c-123">Uppgiftens namn.</span><span class="sxs-lookup"><span data-stu-id="0b53c-123">The name of the task.</span></span>

```yaml
Type: System.String
Parameter Sets: ComponentNameParameterSet
Aliases: TaskName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0b53c-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="0b53c-124">-PassThru</span></span>
<span data-ttu-id="0b53c-125">Returnerar TRUE/FALSE.</span><span class="sxs-lookup"><span data-stu-id="0b53c-125">Returns an true/false.</span></span>
<span data-ttu-id="0b53c-126">Denna cmdlet genererar som standard inga utdata.</span><span class="sxs-lookup"><span data-stu-id="0b53c-126">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="0b53c-127">-Projektetsnamn</span><span class="sxs-lookup"><span data-stu-id="0b53c-127">-ProjectName</span></span>
<span data-ttu-id="0b53c-128">Namnet på projektet.</span><span class="sxs-lookup"><span data-stu-id="0b53c-128">The name of the project.</span></span>

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

### <span data-ttu-id="0b53c-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0b53c-129">-ResourceGroupName</span></span>
<span data-ttu-id="0b53c-130">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="0b53c-130">The name of the resource group.</span></span>

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

### <span data-ttu-id="0b53c-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="0b53c-131">-ResourceId</span></span>
<span data-ttu-id="0b53c-132">Projekt resurs-ID.</span><span class="sxs-lookup"><span data-stu-id="0b53c-132">Project Resource Id.</span></span>

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

### <span data-ttu-id="0b53c-133">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="0b53c-133">-ServiceName</span></span>
<span data-ttu-id="0b53c-134">Tjänst namn för databas migration.</span><span class="sxs-lookup"><span data-stu-id="0b53c-134">Database Migration Service Name.</span></span>

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

### <span data-ttu-id="0b53c-135">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="0b53c-135">-Confirm</span></span>
<span data-ttu-id="0b53c-136">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="0b53c-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0b53c-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0b53c-137">-WhatIf</span></span>
<span data-ttu-id="0b53c-138">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="0b53c-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0b53c-139">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="0b53c-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0b53c-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0b53c-140">CommonParameters</span></span>
<span data-ttu-id="0b53c-141">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0b53c-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0b53c-142">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0b53c-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0b53c-143">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="0b53c-143">INPUTS</span></span>

### <span data-ttu-id="0b53c-144">Microsoft. Azure. commands. DataMigration. Models. PSProjectTask</span><span class="sxs-lookup"><span data-stu-id="0b53c-144">Microsoft.Azure.Commands.DataMigration.Models.PSProjectTask</span></span>
<span data-ttu-id="0b53c-145">Parametrar: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="0b53c-145">Parameters: InputObject (ByValue)</span></span>

### <span data-ttu-id="0b53c-146">System. String</span><span class="sxs-lookup"><span data-stu-id="0b53c-146">System.String</span></span>

## <span data-ttu-id="0b53c-147">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="0b53c-147">OUTPUTS</span></span>

### <span data-ttu-id="0b53c-148">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="0b53c-148">System.Boolean</span></span>

## <span data-ttu-id="0b53c-149">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="0b53c-149">NOTES</span></span>

## <span data-ttu-id="0b53c-150">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="0b53c-150">RELATED LINKS</span></span>
