---
external help file: Microsoft.Azure.Commands.DataMigration.dll-Help.xml
Module Name: AzureRM.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datamigration/remove-azurermdatamigrationservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataMigration/Commands.DataMigration/help/Remove-AzureRmDataMigrationService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataMigration/Commands.DataMigration/help/Remove-AzureRmDataMigrationService.md
ms.openlocfilehash: dde0044642f81c098358cd86cabe8c066240a215
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93580447"
---
# <span data-ttu-id="662e9-101">Remove-AzureRmDataMigrationService</span><span class="sxs-lookup"><span data-stu-id="662e9-101">Remove-AzureRmDataMigrationService</span></span>

## <span data-ttu-id="662e9-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="662e9-102">SYNOPSIS</span></span>
<span data-ttu-id="662e9-103">Tar bort en instans av Azure Database migration service från Azure.</span><span class="sxs-lookup"><span data-stu-id="662e9-103">Removes an instance of the Azure Database Migration Service from Azure.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="662e9-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="662e9-104">SYNTAX</span></span>

### <span data-ttu-id="662e9-105">ComponentNameParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="662e9-105">ComponentNameParameterSet (Default)</span></span>
```
Remove-AzureRmDataMigrationService -ResourceGroupName <String> -Name <String> [-Force] [-DeleteRunningTask]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="662e9-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="662e9-106">ComponentObjectParameterSet</span></span>
```
Remove-AzureRmDataMigrationService [-InputObject] <PSDataMigrationService> [-Force] [-DeleteRunningTask]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="662e9-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="662e9-107">ResourceIdParameterSet</span></span>
```
Remove-AzureRmDataMigrationService [-ResourceId] <String> [-Force] [-DeleteRunningTask] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
```

## <span data-ttu-id="662e9-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="662e9-108">DESCRIPTION</span></span>
<span data-ttu-id="662e9-109">Remove-AzureRmDataMigrationService-cmdleten tar bort en instans av Azure Database migration-tjänsten från Azure.</span><span class="sxs-lookup"><span data-stu-id="662e9-109">The Remove-AzureRmDataMigrationService cmdlet removes an instance of the Azure Database Migration Service from Azure.</span></span> <span data-ttu-id="662e9-110">Om du anger parametern DeleteRunningTask tar du bort alla uppgifter för Azure Database migration som är associerade med tjänsten som tas bort.</span><span class="sxs-lookup"><span data-stu-id="662e9-110">Supplying the DeleteRunningTask parameter removes all of the Azure Database Migration Service tasks associated with the service that is being removed.</span></span> 

## <span data-ttu-id="662e9-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="662e9-111">EXAMPLES</span></span>

### <span data-ttu-id="662e9-112">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="662e9-112">Example 1</span></span>
```
PS C:\> Remove-AzureRmDataMigrationService -ResourceGroupName MyResourceGroup –ServiceName TestService
```

<span data-ttu-id="662e9-113">I exemplet ovan tas en instans av Azure Database migration-tjänsten med namnet TestService som ingår i en Azure-resurs grupp med namnet MyResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="662e9-113">The above example removes an instance of the Azure Database Migration Service named TestService that is contained in an Azure Resource Group named MyResourceGroup.</span></span>

## <span data-ttu-id="662e9-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="662e9-114">PARAMETERS</span></span>

### <span data-ttu-id="662e9-115">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="662e9-115">-Confirm</span></span>
<span data-ttu-id="662e9-116">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="662e9-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="662e9-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="662e9-117">-DefaultProfile</span></span>
<span data-ttu-id="662e9-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="662e9-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="662e9-119">-DeleteRunningTask</span><span class="sxs-lookup"><span data-stu-id="662e9-119">-DeleteRunningTask</span></span>
<span data-ttu-id="662e9-120">Ta bort en pågående uppgift</span><span class="sxs-lookup"><span data-stu-id="662e9-120">Delete any running task</span></span>

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

### <span data-ttu-id="662e9-121">-Force</span><span class="sxs-lookup"><span data-stu-id="662e9-121">-Force</span></span>
<span data-ttu-id="662e9-122">Hoppa över bekräftelse meddelande för att utföra åtgärden</span><span class="sxs-lookup"><span data-stu-id="662e9-122">Skip confirmation message for performing the action</span></span>

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

### <span data-ttu-id="662e9-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="662e9-123">-InputObject</span></span>
<span data-ttu-id="662e9-124">PSDataMigrationService-objekt.</span><span class="sxs-lookup"><span data-stu-id="662e9-124">PSDataMigrationService Object.</span></span>

```yaml
Type: PSDataMigrationService
Parameter Sets: ComponentObjectParameterSet
Aliases: DataMigrationService

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="662e9-125">-Namn</span><span class="sxs-lookup"><span data-stu-id="662e9-125">-Name</span></span>
<span data-ttu-id="662e9-126">Namnet på data migrations tjänsten.</span><span class="sxs-lookup"><span data-stu-id="662e9-126">The name of the Data Migration Service.</span></span>

```yaml
Type: String
Parameter Sets: ComponentNameParameterSet
Aliases: ServiceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="662e9-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="662e9-127">-PassThru</span></span>
<span data-ttu-id="662e9-128">Returnerar TRUE/FALSE.</span><span class="sxs-lookup"><span data-stu-id="662e9-128">Returns an true/false.</span></span>
<span data-ttu-id="662e9-129">Denna cmdlet genererar som standard inga utdata.</span><span class="sxs-lookup"><span data-stu-id="662e9-129">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="662e9-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="662e9-130">-ResourceGroupName</span></span>
<span data-ttu-id="662e9-131">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="662e9-131">The name of the resource group.</span></span>

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

### <span data-ttu-id="662e9-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="662e9-132">-ResourceId</span></span>
<span data-ttu-id="662e9-133">DataMigrationService resurs-ID.</span><span class="sxs-lookup"><span data-stu-id="662e9-133">DataMigrationService Resource Id.</span></span>

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

### <span data-ttu-id="662e9-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="662e9-134">-WhatIf</span></span>
<span data-ttu-id="662e9-135">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="662e9-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="662e9-136">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="662e9-136">The cmdlet is not run.</span></span>

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

## <span data-ttu-id="662e9-137">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="662e9-137">INPUTS</span></span>

### <span data-ttu-id="662e9-138">Microsoft.Azure.Commands.DataMigration.Models.PSDataMigrationService</span><span class="sxs-lookup"><span data-stu-id="662e9-138">Microsoft.Azure.Commands.DataMigration.Models.PSDataMigrationService</span></span>
<span data-ttu-id="662e9-139">System. String</span><span class="sxs-lookup"><span data-stu-id="662e9-139">System.String</span></span>


## <span data-ttu-id="662e9-140">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="662e9-140">OUTPUTS</span></span>

### <span data-ttu-id="662e9-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="662e9-141">System.Boolean</span></span>


## <span data-ttu-id="662e9-142">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="662e9-142">NOTES</span></span>

## <span data-ttu-id="662e9-143">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="662e9-143">RELATED LINKS</span></span>


