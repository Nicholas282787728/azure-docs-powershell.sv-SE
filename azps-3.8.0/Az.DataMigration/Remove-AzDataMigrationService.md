---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataMigration.dll-Help.xml
Module Name: Az.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/az.datamigration/Remove-AzDataMigrationService
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/Remove-AzDataMigrationService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/Remove-AzDataMigrationService.md
ms.openlocfilehash: 2ba182833fc1d4c59d9164b6db5d68bcd3c499f6
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93925881"
---
# <span data-ttu-id="91fc4-101">Remove-AzDataMigrationService</span><span class="sxs-lookup"><span data-stu-id="91fc4-101">Remove-AzDataMigrationService</span></span>

## <span data-ttu-id="91fc4-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="91fc4-102">SYNOPSIS</span></span>
<span data-ttu-id="91fc4-103">Tar bort en instans av Azure Database migration service från Azure.</span><span class="sxs-lookup"><span data-stu-id="91fc4-103">Removes an instance of the Azure Database Migration Service from Azure.</span></span>

## <span data-ttu-id="91fc4-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="91fc4-104">SYNTAX</span></span>

### <span data-ttu-id="91fc4-105">ComponentNameParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="91fc4-105">ComponentNameParameterSet (Default)</span></span>
```
Remove-AzDataMigrationService -ResourceGroupName <String> -Name <String> [-Force] [-DeleteRunningTask]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="91fc4-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="91fc4-106">ComponentObjectParameterSet</span></span>
```
Remove-AzDataMigrationService [-InputObject] <PSDataMigrationService> [-Force] [-DeleteRunningTask] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="91fc4-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="91fc4-107">ResourceIdParameterSet</span></span>
```
Remove-AzDataMigrationService [-ResourceId] <String> [-Force] [-DeleteRunningTask] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="91fc4-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="91fc4-108">DESCRIPTION</span></span>
<span data-ttu-id="91fc4-109">Remove-AzDataMigrationService-cmdleten tar bort en instans av Azure Database migration-tjänsten från Azure.</span><span class="sxs-lookup"><span data-stu-id="91fc4-109">The Remove-AzDataMigrationService cmdlet removes an instance of the Azure Database Migration Service from Azure.</span></span> <span data-ttu-id="91fc4-110">Om du anger parametern DeleteRunningTask tar du bort alla uppgifter för Azure Database migration som är associerade med tjänsten som tas bort.</span><span class="sxs-lookup"><span data-stu-id="91fc4-110">Supplying the DeleteRunningTask parameter removes all of the Azure Database Migration Service tasks associated with the service that is being removed.</span></span> 

## <span data-ttu-id="91fc4-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="91fc4-111">EXAMPLES</span></span>

### <span data-ttu-id="91fc4-112">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="91fc4-112">Example 1</span></span>
```
PS C:\> Remove-AzDataMigrationService -ResourceGroupName MyResourceGroup -ServiceName TestService
```

<span data-ttu-id="91fc4-113">I exemplet ovan tas en instans av Azure Database migration-tjänsten med namnet TestService som ingår i en Azure-resurs grupp med namnet MyResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="91fc4-113">The above example removes an instance of the Azure Database Migration Service named TestService that is contained in an Azure Resource Group named MyResourceGroup.</span></span>

## <span data-ttu-id="91fc4-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="91fc4-114">PARAMETERS</span></span>

### <span data-ttu-id="91fc4-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="91fc4-115">-DefaultProfile</span></span>
<span data-ttu-id="91fc4-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="91fc4-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="91fc4-117">-DeleteRunningTask</span><span class="sxs-lookup"><span data-stu-id="91fc4-117">-DeleteRunningTask</span></span>
<span data-ttu-id="91fc4-118">Ta bort en pågående uppgift</span><span class="sxs-lookup"><span data-stu-id="91fc4-118">Delete any running task</span></span>

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

### <span data-ttu-id="91fc4-119">-Force</span><span class="sxs-lookup"><span data-stu-id="91fc4-119">-Force</span></span>
<span data-ttu-id="91fc4-120">Hoppa över bekräftelse meddelande för att utföra åtgärden</span><span class="sxs-lookup"><span data-stu-id="91fc4-120">Skip confirmation message for performing the action</span></span>

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

### <span data-ttu-id="91fc4-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="91fc4-121">-InputObject</span></span>
<span data-ttu-id="91fc4-122">PSDataMigrationService-objekt.</span><span class="sxs-lookup"><span data-stu-id="91fc4-122">PSDataMigrationService Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataMigration.Models.PSDataMigrationService
Parameter Sets: ComponentObjectParameterSet
Aliases: DataMigrationService

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="91fc4-123">-Namn</span><span class="sxs-lookup"><span data-stu-id="91fc4-123">-Name</span></span>
<span data-ttu-id="91fc4-124">Namnet på databasens migreringstjänster.</span><span class="sxs-lookup"><span data-stu-id="91fc4-124">The name of the Database Migration Service.</span></span>

```yaml
Type: System.String
Parameter Sets: ComponentNameParameterSet
Aliases: ServiceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="91fc4-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="91fc4-125">-PassThru</span></span>
<span data-ttu-id="91fc4-126">Returnerar TRUE/FALSE.</span><span class="sxs-lookup"><span data-stu-id="91fc4-126">Returns an true/false.</span></span>
<span data-ttu-id="91fc4-127">Denna cmdlet genererar som standard inga utdata.</span><span class="sxs-lookup"><span data-stu-id="91fc4-127">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="91fc4-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="91fc4-128">-ResourceGroupName</span></span>
<span data-ttu-id="91fc4-129">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="91fc4-129">The name of the resource group.</span></span>

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

### <span data-ttu-id="91fc4-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="91fc4-130">-ResourceId</span></span>
<span data-ttu-id="91fc4-131">DataMigrationService resurs-ID.</span><span class="sxs-lookup"><span data-stu-id="91fc4-131">DataMigrationService Resource Id.</span></span>

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

### <span data-ttu-id="91fc4-132">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="91fc4-132">-Confirm</span></span>
<span data-ttu-id="91fc4-133">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="91fc4-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="91fc4-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="91fc4-134">-WhatIf</span></span>
<span data-ttu-id="91fc4-135">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="91fc4-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="91fc4-136">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="91fc4-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="91fc4-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="91fc4-137">CommonParameters</span></span>
<span data-ttu-id="91fc4-138">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="91fc4-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="91fc4-139">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="91fc4-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="91fc4-140">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="91fc4-140">INPUTS</span></span>

### <span data-ttu-id="91fc4-141">Microsoft.Azure.Commands.DataMigration.Models.PSDataMigrationService</span><span class="sxs-lookup"><span data-stu-id="91fc4-141">Microsoft.Azure.Commands.DataMigration.Models.PSDataMigrationService</span></span>

### <span data-ttu-id="91fc4-142">System. String</span><span class="sxs-lookup"><span data-stu-id="91fc4-142">System.String</span></span>

## <span data-ttu-id="91fc4-143">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="91fc4-143">OUTPUTS</span></span>

### <span data-ttu-id="91fc4-144">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="91fc4-144">System.Boolean</span></span>

## <span data-ttu-id="91fc4-145">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="91fc4-145">NOTES</span></span>

## <span data-ttu-id="91fc4-146">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="91fc4-146">RELATED LINKS</span></span>
