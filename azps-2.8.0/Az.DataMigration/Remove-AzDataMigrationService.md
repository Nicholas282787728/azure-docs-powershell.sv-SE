---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataMigration.dll-Help.xml
Module Name: Az.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/az.datamigration/Remove-AzDataMigrationService
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/Remove-AzDataMigrationService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/Remove-AzDataMigrationService.md
ms.openlocfilehash: 737f723fddd7b351a0f1e9189590a61d83454976
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93744484"
---
# <span data-ttu-id="80336-101">Remove-AzDataMigrationService</span><span class="sxs-lookup"><span data-stu-id="80336-101">Remove-AzDataMigrationService</span></span>

## <span data-ttu-id="80336-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="80336-102">SYNOPSIS</span></span>
<span data-ttu-id="80336-103">Tar bort en instans av Azure Database migration service från Azure.</span><span class="sxs-lookup"><span data-stu-id="80336-103">Removes an instance of the Azure Database Migration Service from Azure.</span></span>

## <span data-ttu-id="80336-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="80336-104">SYNTAX</span></span>

### <span data-ttu-id="80336-105">ComponentNameParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="80336-105">ComponentNameParameterSet (Default)</span></span>
```
Remove-AzDataMigrationService -ResourceGroupName <String> -Name <String> [-Force] [-DeleteRunningTask]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="80336-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="80336-106">ComponentObjectParameterSet</span></span>
```
Remove-AzDataMigrationService [-InputObject] <PSDataMigrationService> [-Force] [-DeleteRunningTask] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="80336-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="80336-107">ResourceIdParameterSet</span></span>
```
Remove-AzDataMigrationService [-ResourceId] <String> [-Force] [-DeleteRunningTask] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="80336-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="80336-108">DESCRIPTION</span></span>
<span data-ttu-id="80336-109">Remove-AzDataMigrationService-cmdleten tar bort en instans av Azure Database migration-tjänsten från Azure.</span><span class="sxs-lookup"><span data-stu-id="80336-109">The Remove-AzDataMigrationService cmdlet removes an instance of the Azure Database Migration Service from Azure.</span></span> <span data-ttu-id="80336-110">Om du anger parametern DeleteRunningTask tar du bort alla uppgifter för Azure Database migration som är associerade med tjänsten som tas bort.</span><span class="sxs-lookup"><span data-stu-id="80336-110">Supplying the DeleteRunningTask parameter removes all of the Azure Database Migration Service tasks associated with the service that is being removed.</span></span> 

## <span data-ttu-id="80336-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="80336-111">EXAMPLES</span></span>

### <span data-ttu-id="80336-112">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="80336-112">Example 1</span></span>
```
PS C:\> Remove-AzDataMigrationService -ResourceGroupName MyResourceGroup -ServiceName TestService
```

<span data-ttu-id="80336-113">I exemplet ovan tas en instans av Azure Database migration-tjänsten med namnet TestService som ingår i en Azure-resurs grupp med namnet MyResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="80336-113">The above example removes an instance of the Azure Database Migration Service named TestService that is contained in an Azure Resource Group named MyResourceGroup.</span></span>

## <span data-ttu-id="80336-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="80336-114">PARAMETERS</span></span>

### <span data-ttu-id="80336-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="80336-115">-DefaultProfile</span></span>
<span data-ttu-id="80336-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="80336-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="80336-117">-DeleteRunningTask</span><span class="sxs-lookup"><span data-stu-id="80336-117">-DeleteRunningTask</span></span>
<span data-ttu-id="80336-118">Ta bort en pågående uppgift</span><span class="sxs-lookup"><span data-stu-id="80336-118">Delete any running task</span></span>

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

### <span data-ttu-id="80336-119">-Force</span><span class="sxs-lookup"><span data-stu-id="80336-119">-Force</span></span>
<span data-ttu-id="80336-120">Hoppa över bekräftelse meddelande för att utföra åtgärden</span><span class="sxs-lookup"><span data-stu-id="80336-120">Skip confirmation message for performing the action</span></span>

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

### <span data-ttu-id="80336-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="80336-121">-InputObject</span></span>
<span data-ttu-id="80336-122">PSDataMigrationService-objekt.</span><span class="sxs-lookup"><span data-stu-id="80336-122">PSDataMigrationService Object.</span></span>

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

### <span data-ttu-id="80336-123">-Namn</span><span class="sxs-lookup"><span data-stu-id="80336-123">-Name</span></span>
<span data-ttu-id="80336-124">Namnet på databasens migreringstjänster.</span><span class="sxs-lookup"><span data-stu-id="80336-124">The name of the Database Migration Service.</span></span>

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

### <span data-ttu-id="80336-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="80336-125">-PassThru</span></span>
<span data-ttu-id="80336-126">Returnerar TRUE/FALSE.</span><span class="sxs-lookup"><span data-stu-id="80336-126">Returns an true/false.</span></span>
<span data-ttu-id="80336-127">Denna cmdlet genererar som standard inga utdata.</span><span class="sxs-lookup"><span data-stu-id="80336-127">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="80336-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="80336-128">-ResourceGroupName</span></span>
<span data-ttu-id="80336-129">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="80336-129">The name of the resource group.</span></span>

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

### <span data-ttu-id="80336-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="80336-130">-ResourceId</span></span>
<span data-ttu-id="80336-131">DataMigrationService resurs-ID.</span><span class="sxs-lookup"><span data-stu-id="80336-131">DataMigrationService Resource Id.</span></span>

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

### <span data-ttu-id="80336-132">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="80336-132">-Confirm</span></span>
<span data-ttu-id="80336-133">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="80336-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="80336-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="80336-134">-WhatIf</span></span>
<span data-ttu-id="80336-135">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="80336-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="80336-136">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="80336-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="80336-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="80336-137">CommonParameters</span></span>
<span data-ttu-id="80336-138">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="80336-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="80336-139">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="80336-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="80336-140">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="80336-140">INPUTS</span></span>

### <span data-ttu-id="80336-141">Microsoft.Azure.Commands.DataMigration.Models.PSDataMigrationService</span><span class="sxs-lookup"><span data-stu-id="80336-141">Microsoft.Azure.Commands.DataMigration.Models.PSDataMigrationService</span></span>

### <span data-ttu-id="80336-142">System. String</span><span class="sxs-lookup"><span data-stu-id="80336-142">System.String</span></span>

## <span data-ttu-id="80336-143">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="80336-143">OUTPUTS</span></span>

### <span data-ttu-id="80336-144">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="80336-144">System.Boolean</span></span>

## <span data-ttu-id="80336-145">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="80336-145">NOTES</span></span>

## <span data-ttu-id="80336-146">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="80336-146">RELATED LINKS</span></span>
