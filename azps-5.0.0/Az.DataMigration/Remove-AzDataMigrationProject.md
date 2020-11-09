---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataMigration.dll-Help.xml
Module Name: Az.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/az.datamigration/Remove-AzDataMigrationProject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/Remove-AzDataMigrationProject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/Remove-AzDataMigrationProject.md
ms.openlocfilehash: f45134cae9c77108aca4084470fd7f919fde02a4
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94320403"
---
# <span data-ttu-id="51089-101">Remove-AzDataMigrationProject</span><span class="sxs-lookup"><span data-stu-id="51089-101">Remove-AzDataMigrationProject</span></span>

## <span data-ttu-id="51089-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="51089-102">SYNOPSIS</span></span>
<span data-ttu-id="51089-103">Tar bort en Azure Database migration service-projekt från Azure.</span><span class="sxs-lookup"><span data-stu-id="51089-103">Removes an Azure Database Migration Service project from Azure.</span></span>

## <span data-ttu-id="51089-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="51089-104">SYNTAX</span></span>

### <span data-ttu-id="51089-105">ComponentNameParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="51089-105">ComponentNameParameterSet (Default)</span></span>
```
Remove-AzDataMigrationProject -ResourceGroupName <String> -ServiceName <String> -Name <String> [-Force]
 [-DeleteRunningTask] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="51089-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="51089-106">ComponentObjectParameterSet</span></span>
```
Remove-AzDataMigrationProject [-InputObject] <PSProject> [-Force] [-DeleteRunningTask] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="51089-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="51089-107">ResourceIdParameterSet</span></span>
```
Remove-AzDataMigrationProject [-ResourceId] <String> [-Force] [-DeleteRunningTask] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="51089-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="51089-108">DESCRIPTION</span></span>
<span data-ttu-id="51089-109">Remove-AzDataMigrationProject cmdlet tar bort en Azure Database migration service-projekt från Azure.</span><span class="sxs-lookup"><span data-stu-id="51089-109">The Remove-AzDataMigrationProject cmdlet removes an Azure Database Migration Service project from Azure.</span></span> <span data-ttu-id="51089-110">Om du anger parametern DeleteRunningTask tar du bort alla uppgifter i Azure Database migration service som är associerade med projektet som tas bort.</span><span class="sxs-lookup"><span data-stu-id="51089-110">Supplying the DeleteRunningTask parameter removes all of the Azure Database Migration Service tasks associated with the project that is being removed.</span></span> 

## <span data-ttu-id="51089-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="51089-111">EXAMPLES</span></span>

### <span data-ttu-id="51089-112">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="51089-112">Example 1</span></span>
```
PS C:\> Remove-AzDataMigrationProject -ResourceGroupName myResourceGroup -ServiceName myDMService -ProjectName myDMProject
```

<span data-ttu-id="51089-113">Exemplet ovan tar bort Azure Database migration service Project med namnet myDMProject från Azure baserat på namn som indataparameter</span><span class="sxs-lookup"><span data-stu-id="51089-113">The above example removes the Azure Database Migration Service project called myDMProject from Azure based on name as input parameter</span></span>

### <span data-ttu-id="51089-114">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="51089-114">Example 2</span></span>
```
PS C:\> Remove-AzDataMigrationProject -InputObject $myDMSProject
```

<span data-ttu-id="51089-115">I exemplet ovan tas Azure Database migration service Project bort baserat på PSProject-objekt som indataparameter.</span><span class="sxs-lookup"><span data-stu-id="51089-115">The above example removes the Azure Database Migration Service project based on PSProject object as input parameter.</span></span>

## <span data-ttu-id="51089-116">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="51089-116">PARAMETERS</span></span>

### <span data-ttu-id="51089-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="51089-117">-DefaultProfile</span></span>
<span data-ttu-id="51089-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="51089-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="51089-119">-DeleteRunningTask</span><span class="sxs-lookup"><span data-stu-id="51089-119">-DeleteRunningTask</span></span>
<span data-ttu-id="51089-120">Ta bort en pågående uppgift</span><span class="sxs-lookup"><span data-stu-id="51089-120">Delete any running task</span></span>

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

### <span data-ttu-id="51089-121">-Force</span><span class="sxs-lookup"><span data-stu-id="51089-121">-Force</span></span>
<span data-ttu-id="51089-122">Hoppa över bekräftelse meddelande för att utföra åtgärden</span><span class="sxs-lookup"><span data-stu-id="51089-122">Skip confirmation message for performing the action</span></span>

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

### <span data-ttu-id="51089-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="51089-123">-InputObject</span></span>
<span data-ttu-id="51089-124">PSProject-objekt.</span><span class="sxs-lookup"><span data-stu-id="51089-124">PSProject Object.</span></span>

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

### <span data-ttu-id="51089-125">-Namn</span><span class="sxs-lookup"><span data-stu-id="51089-125">-Name</span></span>
<span data-ttu-id="51089-126">Namnet på projektet.</span><span class="sxs-lookup"><span data-stu-id="51089-126">The name of the project.</span></span>

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

### <span data-ttu-id="51089-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="51089-127">-PassThru</span></span>
<span data-ttu-id="51089-128">Returnerar TRUE/FALSE.</span><span class="sxs-lookup"><span data-stu-id="51089-128">Returns an true/false.</span></span>
<span data-ttu-id="51089-129">Denna cmdlet genererar som standard inga utdata.</span><span class="sxs-lookup"><span data-stu-id="51089-129">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="51089-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="51089-130">-ResourceGroupName</span></span>
<span data-ttu-id="51089-131">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="51089-131">The name of the resource group.</span></span>

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

### <span data-ttu-id="51089-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="51089-132">-ResourceId</span></span>
<span data-ttu-id="51089-133">Projekt resurs-ID.</span><span class="sxs-lookup"><span data-stu-id="51089-133">Project Resource Id.</span></span>

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

### <span data-ttu-id="51089-134">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="51089-134">-ServiceName</span></span>
<span data-ttu-id="51089-135">Tjänst namn för databas migration.</span><span class="sxs-lookup"><span data-stu-id="51089-135">Database Migration Service Name.</span></span>

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

### <span data-ttu-id="51089-136">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="51089-136">-Confirm</span></span>
<span data-ttu-id="51089-137">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="51089-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="51089-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="51089-138">-WhatIf</span></span>
<span data-ttu-id="51089-139">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="51089-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="51089-140">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="51089-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="51089-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="51089-141">CommonParameters</span></span>
<span data-ttu-id="51089-142">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="51089-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="51089-143">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="51089-143">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="51089-144">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="51089-144">INPUTS</span></span>

### <span data-ttu-id="51089-145">Microsoft. Azure. commands. DataMigration. Models. PSProject</span><span class="sxs-lookup"><span data-stu-id="51089-145">Microsoft.Azure.Commands.DataMigration.Models.PSProject</span></span>

### <span data-ttu-id="51089-146">System. String</span><span class="sxs-lookup"><span data-stu-id="51089-146">System.String</span></span>

## <span data-ttu-id="51089-147">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="51089-147">OUTPUTS</span></span>

### <span data-ttu-id="51089-148">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="51089-148">System.Boolean</span></span>

## <span data-ttu-id="51089-149">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="51089-149">NOTES</span></span>

## <span data-ttu-id="51089-150">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="51089-150">RELATED LINKS</span></span>
