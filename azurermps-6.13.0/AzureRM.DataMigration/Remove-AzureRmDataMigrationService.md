---
external help file: Microsoft.Azure.Commands.DataMigration.dll-Help.xml
Module Name: AzureRM.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datamigration/Remove-AzureRmDataMigrationService
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataMigration/Commands.DataMigration/help/Remove-AzureRmDataMigrationService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataMigration/Commands.DataMigration/help/Remove-AzureRmDataMigrationService.md
ms.openlocfilehash: 677e89dd0def314744e507c6e61c745f39a081bb
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93583524"
---
# <span data-ttu-id="279ca-101">Remove-AzureRmDataMigrationService</span><span class="sxs-lookup"><span data-stu-id="279ca-101">Remove-AzureRmDataMigrationService</span></span>

## <span data-ttu-id="279ca-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="279ca-102">SYNOPSIS</span></span>
<span data-ttu-id="279ca-103">Tar bort en instans av Azure Database migration service från Azure.</span><span class="sxs-lookup"><span data-stu-id="279ca-103">Removes an instance of the Azure Database Migration Service from Azure.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="279ca-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="279ca-104">SYNTAX</span></span>

### <span data-ttu-id="279ca-105">ComponentNameParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="279ca-105">ComponentNameParameterSet (Default)</span></span>
```
Remove-AzureRmDataMigrationService -ResourceGroupName <String> -Name <String> [-Force] [-DeleteRunningTask]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="279ca-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="279ca-106">ComponentObjectParameterSet</span></span>
```
Remove-AzureRmDataMigrationService [-InputObject] <PSDataMigrationService> [-Force] [-DeleteRunningTask]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="279ca-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="279ca-107">ResourceIdParameterSet</span></span>
```
Remove-AzureRmDataMigrationService [-ResourceId] <String> [-Force] [-DeleteRunningTask] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="279ca-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="279ca-108">DESCRIPTION</span></span>
<span data-ttu-id="279ca-109">Remove-AzureRmDataMigrationService-cmdleten tar bort en instans av Azure Database migration-tjänsten från Azure.</span><span class="sxs-lookup"><span data-stu-id="279ca-109">The Remove-AzureRmDataMigrationService cmdlet removes an instance of the Azure Database Migration Service from Azure.</span></span> <span data-ttu-id="279ca-110">Om du anger parametern DeleteRunningTask tar du bort alla uppgifter för Azure Database migration som är associerade med tjänsten som tas bort.</span><span class="sxs-lookup"><span data-stu-id="279ca-110">Supplying the DeleteRunningTask parameter removes all of the Azure Database Migration Service tasks associated with the service that is being removed.</span></span> 

## <span data-ttu-id="279ca-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="279ca-111">EXAMPLES</span></span>

### <span data-ttu-id="279ca-112">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="279ca-112">Example 1</span></span>
```
PS C:\> Remove-AzureRmDataMigrationService -ResourceGroupName MyResourceGroup -ServiceName TestService
```

<span data-ttu-id="279ca-113">I exemplet ovan tas en instans av Azure Database migration-tjänsten med namnet TestService som ingår i en Azure-resurs grupp med namnet MyResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="279ca-113">The above example removes an instance of the Azure Database Migration Service named TestService that is contained in an Azure Resource Group named MyResourceGroup.</span></span>

## <span data-ttu-id="279ca-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="279ca-114">PARAMETERS</span></span>

### <span data-ttu-id="279ca-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="279ca-115">-DefaultProfile</span></span>
<span data-ttu-id="279ca-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="279ca-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="279ca-117">-DeleteRunningTask</span><span class="sxs-lookup"><span data-stu-id="279ca-117">-DeleteRunningTask</span></span>
<span data-ttu-id="279ca-118">Ta bort en pågående uppgift</span><span class="sxs-lookup"><span data-stu-id="279ca-118">Delete any running task</span></span>

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

### <span data-ttu-id="279ca-119">-Force</span><span class="sxs-lookup"><span data-stu-id="279ca-119">-Force</span></span>
<span data-ttu-id="279ca-120">Hoppa över bekräftelse meddelande för att utföra åtgärden</span><span class="sxs-lookup"><span data-stu-id="279ca-120">Skip confirmation message for performing the action</span></span>

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

### <span data-ttu-id="279ca-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="279ca-121">-InputObject</span></span>
<span data-ttu-id="279ca-122">PSDataMigrationService-objekt.</span><span class="sxs-lookup"><span data-stu-id="279ca-122">PSDataMigrationService Object.</span></span>

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

### <span data-ttu-id="279ca-123">-Namn</span><span class="sxs-lookup"><span data-stu-id="279ca-123">-Name</span></span>
<span data-ttu-id="279ca-124">Namnet på databasens migreringstjänster.</span><span class="sxs-lookup"><span data-stu-id="279ca-124">The name of the Database Migration Service.</span></span>

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

### <span data-ttu-id="279ca-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="279ca-125">-PassThru</span></span>
<span data-ttu-id="279ca-126">Returnerar TRUE/FALSE.</span><span class="sxs-lookup"><span data-stu-id="279ca-126">Returns an true/false.</span></span>
<span data-ttu-id="279ca-127">Denna cmdlet genererar som standard inga utdata.</span><span class="sxs-lookup"><span data-stu-id="279ca-127">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="279ca-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="279ca-128">-ResourceGroupName</span></span>
<span data-ttu-id="279ca-129">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="279ca-129">The name of the resource group.</span></span>

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

### <span data-ttu-id="279ca-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="279ca-130">-ResourceId</span></span>
<span data-ttu-id="279ca-131">DataMigrationService resurs-ID.</span><span class="sxs-lookup"><span data-stu-id="279ca-131">DataMigrationService Resource Id.</span></span>

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

### <span data-ttu-id="279ca-132">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="279ca-132">-Confirm</span></span>
<span data-ttu-id="279ca-133">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="279ca-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="279ca-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="279ca-134">-WhatIf</span></span>
<span data-ttu-id="279ca-135">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="279ca-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="279ca-136">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="279ca-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="279ca-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="279ca-137">CommonParameters</span></span>
<span data-ttu-id="279ca-138">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="279ca-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="279ca-139">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="279ca-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="279ca-140">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="279ca-140">INPUTS</span></span>

### <span data-ttu-id="279ca-141">Microsoft.Azure.Commands.DataMigration.Models.PSDataMigrationService</span><span class="sxs-lookup"><span data-stu-id="279ca-141">Microsoft.Azure.Commands.DataMigration.Models.PSDataMigrationService</span></span>
<span data-ttu-id="279ca-142">Parametrar: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="279ca-142">Parameters: InputObject (ByValue)</span></span>

### <span data-ttu-id="279ca-143">System. String</span><span class="sxs-lookup"><span data-stu-id="279ca-143">System.String</span></span>

## <span data-ttu-id="279ca-144">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="279ca-144">OUTPUTS</span></span>

### <span data-ttu-id="279ca-145">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="279ca-145">System.Boolean</span></span>

## <span data-ttu-id="279ca-146">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="279ca-146">NOTES</span></span>

## <span data-ttu-id="279ca-147">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="279ca-147">RELATED LINKS</span></span>
