---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataMigration.dll-Help.xml
Module Name: Az.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/az.datamigration/Remove-AzDataMigrationProject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/Remove-AzDataMigrationProject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/Remove-AzDataMigrationProject.md
ms.openlocfilehash: 53dc4841dbbdcb7f3d855630b69a94320b4dfeff
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93754254"
---
# <span data-ttu-id="b2077-101">Remove-AzDataMigrationProject</span><span class="sxs-lookup"><span data-stu-id="b2077-101">Remove-AzDataMigrationProject</span></span>

## <span data-ttu-id="b2077-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="b2077-102">SYNOPSIS</span></span>
<span data-ttu-id="b2077-103">Tar bort en Azure Database migration service-projekt från Azure.</span><span class="sxs-lookup"><span data-stu-id="b2077-103">Removes an Azure Database Migration Service project from Azure.</span></span>

## <span data-ttu-id="b2077-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="b2077-104">SYNTAX</span></span>

### <span data-ttu-id="b2077-105">ComponentNameParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="b2077-105">ComponentNameParameterSet (Default)</span></span>
```
Remove-AzDataMigrationProject -ResourceGroupName <String> -ServiceName <String> -Name <String> [-Force]
 [-DeleteRunningTask] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="b2077-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="b2077-106">ComponentObjectParameterSet</span></span>
```
Remove-AzDataMigrationProject [-InputObject] <PSProject> [-Force] [-DeleteRunningTask] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b2077-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="b2077-107">ResourceIdParameterSet</span></span>
```
Remove-AzDataMigrationProject [-ResourceId] <String> [-Force] [-DeleteRunningTask] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b2077-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="b2077-108">DESCRIPTION</span></span>
<span data-ttu-id="b2077-109">Remove-AzDataMigrationProject cmdlet tar bort en Azure Database migration service-projekt från Azure.</span><span class="sxs-lookup"><span data-stu-id="b2077-109">The Remove-AzDataMigrationProject cmdlet removes an Azure Database Migration Service project from Azure.</span></span> <span data-ttu-id="b2077-110">Om du anger parametern DeleteRunningTask tar du bort alla uppgifter i Azure Database migration service som är associerade med projektet som tas bort.</span><span class="sxs-lookup"><span data-stu-id="b2077-110">Supplying the DeleteRunningTask parameter removes all of the Azure Database Migration Service tasks associated with the project that is being removed.</span></span> 

## <span data-ttu-id="b2077-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="b2077-111">EXAMPLES</span></span>

### <span data-ttu-id="b2077-112">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="b2077-112">Example 1</span></span>
```
PS C:\> Remove-AzDataMigrationProject -ResourceGroupName myResourceGroup -ServiceName myDMService -ProjectName myDMProject
```

<span data-ttu-id="b2077-113">Exemplet ovan tar bort Azure Database migration service Project med namnet myDMProject från Azure baserat på namn som indataparameter</span><span class="sxs-lookup"><span data-stu-id="b2077-113">The above example removes the Azure Database Migration Service project called myDMProject from Azure based on name as input parameter</span></span>

### <span data-ttu-id="b2077-114">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="b2077-114">Example 2</span></span>
```
PS C:\> Remove-AzDataMigrationProject -InputObject $myDMSProject
```

<span data-ttu-id="b2077-115">I exemplet ovan tas Azure Database migration service Project bort baserat på PSProject-objekt som indataparameter.</span><span class="sxs-lookup"><span data-stu-id="b2077-115">The above example removes the Azure Database Migration Service project based on PSProject object as input parameter.</span></span>

## <span data-ttu-id="b2077-116">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="b2077-116">PARAMETERS</span></span>

### <span data-ttu-id="b2077-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b2077-117">-DefaultProfile</span></span>
<span data-ttu-id="b2077-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="b2077-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b2077-119">-DeleteRunningTask</span><span class="sxs-lookup"><span data-stu-id="b2077-119">-DeleteRunningTask</span></span>
<span data-ttu-id="b2077-120">Ta bort en pågående uppgift</span><span class="sxs-lookup"><span data-stu-id="b2077-120">Delete any running task</span></span>

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

### <span data-ttu-id="b2077-121">-Force</span><span class="sxs-lookup"><span data-stu-id="b2077-121">-Force</span></span>
<span data-ttu-id="b2077-122">Hoppa över bekräftelse meddelande för att utföra åtgärden</span><span class="sxs-lookup"><span data-stu-id="b2077-122">Skip confirmation message for performing the action</span></span>

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

### <span data-ttu-id="b2077-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b2077-123">-InputObject</span></span>
<span data-ttu-id="b2077-124">PSProject-objekt.</span><span class="sxs-lookup"><span data-stu-id="b2077-124">PSProject Object.</span></span>

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

### <span data-ttu-id="b2077-125">-Namn</span><span class="sxs-lookup"><span data-stu-id="b2077-125">-Name</span></span>
<span data-ttu-id="b2077-126">Namnet på projektet.</span><span class="sxs-lookup"><span data-stu-id="b2077-126">The name of the project.</span></span>

```yaml
Type: System.String
Parameter Sets: ComponentNameParameterSet
Aliases: ProjectName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b2077-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b2077-127">-PassThru</span></span>
<span data-ttu-id="b2077-128">Returnerar TRUE/FALSE.</span><span class="sxs-lookup"><span data-stu-id="b2077-128">Returns an true/false.</span></span>
<span data-ttu-id="b2077-129">Denna cmdlet genererar som standard inga utdata.</span><span class="sxs-lookup"><span data-stu-id="b2077-129">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="b2077-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b2077-130">-ResourceGroupName</span></span>
<span data-ttu-id="b2077-131">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="b2077-131">The name of the resource group.</span></span>

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

### <span data-ttu-id="b2077-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b2077-132">-ResourceId</span></span>
<span data-ttu-id="b2077-133">Projekt resurs-ID.</span><span class="sxs-lookup"><span data-stu-id="b2077-133">Project Resource Id.</span></span>

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

### <span data-ttu-id="b2077-134">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="b2077-134">-ServiceName</span></span>
<span data-ttu-id="b2077-135">Tjänst namn för databas migration.</span><span class="sxs-lookup"><span data-stu-id="b2077-135">Database Migration Service Name.</span></span>

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

### <span data-ttu-id="b2077-136">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="b2077-136">-Confirm</span></span>
<span data-ttu-id="b2077-137">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="b2077-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b2077-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b2077-138">-WhatIf</span></span>
<span data-ttu-id="b2077-139">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="b2077-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b2077-140">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="b2077-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b2077-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b2077-141">CommonParameters</span></span>
<span data-ttu-id="b2077-142">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b2077-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b2077-143">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b2077-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b2077-144">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="b2077-144">INPUTS</span></span>

### <span data-ttu-id="b2077-145">Microsoft. Azure. commands. DataMigration. Models. PSProject</span><span class="sxs-lookup"><span data-stu-id="b2077-145">Microsoft.Azure.Commands.DataMigration.Models.PSProject</span></span>

### <span data-ttu-id="b2077-146">System. String</span><span class="sxs-lookup"><span data-stu-id="b2077-146">System.String</span></span>

## <span data-ttu-id="b2077-147">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="b2077-147">OUTPUTS</span></span>

### <span data-ttu-id="b2077-148">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="b2077-148">System.Boolean</span></span>

## <span data-ttu-id="b2077-149">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="b2077-149">NOTES</span></span>

## <span data-ttu-id="b2077-150">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="b2077-150">RELATED LINKS</span></span>
