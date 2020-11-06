---
external help file: Microsoft.Azure.Commands.DataMigration.dll-Help.xml
Module Name: AzureRM.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datamigration/remove-azurermdatamigrationproject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataMigration/Commands.DataMigration/help/Remove-AzureRmDataMigrationProject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataMigration/Commands.DataMigration/help/Remove-AzureRmDataMigrationProject.md
ms.openlocfilehash: 8ec046df13302ece90e57bcb722816f2019ff2e3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93584347"
---
# <span data-ttu-id="f3952-101">Remove-AzureRmDataMigrationProject</span><span class="sxs-lookup"><span data-stu-id="f3952-101">Remove-AzureRmDataMigrationProject</span></span>

## <span data-ttu-id="f3952-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="f3952-102">SYNOPSIS</span></span>
<span data-ttu-id="f3952-103">Tar bort en Azure Database migration service-projekt från Azure.</span><span class="sxs-lookup"><span data-stu-id="f3952-103">Removes an Azure Database Migration Service project from Azure.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f3952-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="f3952-104">SYNTAX</span></span>

### <span data-ttu-id="f3952-105">ComponentNameParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="f3952-105">ComponentNameParameterSet (Default)</span></span>
```
Remove-AzureRmDataMigrationProject -ResourceGroupName <String> -ServiceName <String> -Name <String> [-Force]
 [-DeleteRunningTask] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="f3952-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="f3952-106">ComponentObjectParameterSet</span></span>
```
Remove-AzureRmDataMigrationProject [-InputObject] <PSProject> [-Force] [-DeleteRunningTask] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="f3952-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="f3952-107">ResourceIdParameterSet</span></span>
```
Remove-AzureRmDataMigrationProject [-ResourceId] <String> [-Force] [-DeleteRunningTask] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
```

## <span data-ttu-id="f3952-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="f3952-108">DESCRIPTION</span></span>
<span data-ttu-id="f3952-109">Remove-AzureRmDataMigrationProject cmdlet tar bort en Azure Database migration service-projekt från Azure.</span><span class="sxs-lookup"><span data-stu-id="f3952-109">The Remove-AzureRmDataMigrationProject cmdlet removes an Azure Database Migration Service project from Azure.</span></span> <span data-ttu-id="f3952-110">Om du anger parametern DeleteRunningTask tar du bort alla uppgifter i Azure Database migration service som är associerade med projektet som tas bort.</span><span class="sxs-lookup"><span data-stu-id="f3952-110">Supplying the DeleteRunningTask parameter removes all of the Azure Database Migration Service tasks associated with the project that is being removed.</span></span> 

## <span data-ttu-id="f3952-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="f3952-111">EXAMPLES</span></span>

### <span data-ttu-id="f3952-112">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="f3952-112">Example 1</span></span>
```
PS C:\> Remove-AzureRmDataMigrationProject -ResourceGroupName myResourceGroup -ServiceName myDMService -ProjectName myDMProject
```

<span data-ttu-id="f3952-113">Exemplet ovan tar bort Azure Database migration service Project med namnet myDMProject från Azure baserat på namn som indataparameter</span><span class="sxs-lookup"><span data-stu-id="f3952-113">The above example removes the Azure Database Migration Service project called myDMProject from Azure based on name as input parameter</span></span>

### <span data-ttu-id="f3952-114">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="f3952-114">Example 2</span></span>
```
PS C:\> Remove-AzureRmDataMigrationProject -InputObject $myDMSProject
```

<span data-ttu-id="f3952-115">I exemplet ovan tas Azure Database migration service Project bort baserat på PSProject-objekt som indataparameter.</span><span class="sxs-lookup"><span data-stu-id="f3952-115">The above example removes the Azure Database Migration Service project based on PSProject object as input parameter.</span></span>

## <span data-ttu-id="f3952-116">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="f3952-116">PARAMETERS</span></span>

### <span data-ttu-id="f3952-117">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="f3952-117">-Confirm</span></span>
<span data-ttu-id="f3952-118">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="f3952-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f3952-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f3952-119">-DefaultProfile</span></span>
<span data-ttu-id="f3952-120">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="f3952-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f3952-121">-DeleteRunningTask</span><span class="sxs-lookup"><span data-stu-id="f3952-121">-DeleteRunningTask</span></span>
<span data-ttu-id="f3952-122">Ta bort en pågående uppgift</span><span class="sxs-lookup"><span data-stu-id="f3952-122">Delete any running task</span></span>

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

### <span data-ttu-id="f3952-123">-Force</span><span class="sxs-lookup"><span data-stu-id="f3952-123">-Force</span></span>
<span data-ttu-id="f3952-124">Hoppa över bekräftelse meddelande för att utföra åtgärden</span><span class="sxs-lookup"><span data-stu-id="f3952-124">Skip confirmation message for performing the action</span></span>

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

### <span data-ttu-id="f3952-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f3952-125">-InputObject</span></span>
<span data-ttu-id="f3952-126">PSProject-objekt.</span><span class="sxs-lookup"><span data-stu-id="f3952-126">PSProject Object.</span></span>

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

### <span data-ttu-id="f3952-127">-Namn</span><span class="sxs-lookup"><span data-stu-id="f3952-127">-Name</span></span>
<span data-ttu-id="f3952-128">Namnet på projektet.</span><span class="sxs-lookup"><span data-stu-id="f3952-128">The name of the project.</span></span>

```yaml
Type: String
Parameter Sets: ComponentNameParameterSet
Aliases: ProjectName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f3952-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f3952-129">-PassThru</span></span>
<span data-ttu-id="f3952-130">Returnerar TRUE/FALSE.</span><span class="sxs-lookup"><span data-stu-id="f3952-130">Returns an true/false.</span></span>
<span data-ttu-id="f3952-131">Denna cmdlet genererar som standard inga utdata.</span><span class="sxs-lookup"><span data-stu-id="f3952-131">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="f3952-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f3952-132">-ResourceGroupName</span></span>
<span data-ttu-id="f3952-133">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="f3952-133">The name of the resource group.</span></span>

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

### <span data-ttu-id="f3952-134">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f3952-134">-ResourceId</span></span>
<span data-ttu-id="f3952-135">Projekt resurs-ID.</span><span class="sxs-lookup"><span data-stu-id="f3952-135">Project Resource Id.</span></span>

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

### <span data-ttu-id="f3952-136">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="f3952-136">-ServiceName</span></span>
<span data-ttu-id="f3952-137">Tjänst namn för data migration.</span><span class="sxs-lookup"><span data-stu-id="f3952-137">Data Migration Service Name.</span></span>

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

### <span data-ttu-id="f3952-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f3952-138">-WhatIf</span></span>
<span data-ttu-id="f3952-139">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="f3952-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f3952-140">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="f3952-140">The cmdlet is not run.</span></span>

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

## <span data-ttu-id="f3952-141">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="f3952-141">INPUTS</span></span>

### <span data-ttu-id="f3952-142">Microsoft. Azure. commands. DataMigration. Models. PSProject</span><span class="sxs-lookup"><span data-stu-id="f3952-142">Microsoft.Azure.Commands.DataMigration.Models.PSProject</span></span>
<span data-ttu-id="f3952-143">System. String</span><span class="sxs-lookup"><span data-stu-id="f3952-143">System.String</span></span>


## <span data-ttu-id="f3952-144">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="f3952-144">OUTPUTS</span></span>

### <span data-ttu-id="f3952-145">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="f3952-145">System.Boolean</span></span>


## <span data-ttu-id="f3952-146">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="f3952-146">NOTES</span></span>

## <span data-ttu-id="f3952-147">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="f3952-147">RELATED LINKS</span></span>

