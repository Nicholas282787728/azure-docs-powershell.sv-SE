---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MachineLearningCompute.dll-Help.xml
Module Name: Az.MachineLearning
online version: https://docs.microsoft.com/en-us/powershell/module/az.machinelearning/update-azmlopclustersystemservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Update-AzMlOpClusterSystemService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Update-AzMlOpClusterSystemService.md
ms.openlocfilehash: 0e673cd74d87cee990130c1fd58b9049eec9ff15
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93743677"
---
# <span data-ttu-id="2cd84-101">Update-AzMlOpClusterSystemService</span><span class="sxs-lookup"><span data-stu-id="2cd84-101">Update-AzMlOpClusterSystemService</span></span>

## <span data-ttu-id="2cd84-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="2cd84-102">SYNOPSIS</span></span>
<span data-ttu-id="2cd84-103">Startar en uppdatering av operationalization kluster system tjänster.</span><span class="sxs-lookup"><span data-stu-id="2cd84-103">Starts an update on the operationalization cluster's system services.</span></span>

## <span data-ttu-id="2cd84-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="2cd84-104">SYNTAX</span></span>

### <span data-ttu-id="2cd84-105">StartUpdateWithNameAndResourceGroup</span><span class="sxs-lookup"><span data-stu-id="2cd84-105">StartUpdateWithNameAndResourceGroup</span></span>
```
Update-AzMlOpClusterSystemService -ResourceGroupName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2cd84-106">StartUpdateWithInputObject</span><span class="sxs-lookup"><span data-stu-id="2cd84-106">StartUpdateWithInputObject</span></span>
```
Update-AzMlOpClusterSystemService -InputObject <PSOperationalizationCluster>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2cd84-107">StartUpdateWithResourceId</span><span class="sxs-lookup"><span data-stu-id="2cd84-107">StartUpdateWithResourceId</span></span>
```
Update-AzMlOpClusterSystemService -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2cd84-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="2cd84-108">DESCRIPTION</span></span>
<span data-ttu-id="2cd84-109">System tjänsterna kan uppdateras oberoende av operationalization-klustret.</span><span class="sxs-lookup"><span data-stu-id="2cd84-109">The system services can be updated independently from the operationalization cluster.</span></span> <span data-ttu-id="2cd84-110">Använd denna cmdlet för att starta en uppdatering av system tjänsterna.</span><span class="sxs-lookup"><span data-stu-id="2cd84-110">To start an update on the system services use this cmdlet.</span></span> <span data-ttu-id="2cd84-111">Om det inte finns någon uppdatering kommer en uppdatering att påbörjas och kommer att återföras.</span><span class="sxs-lookup"><span data-stu-id="2cd84-111">If no update is available an update will still be started and will return successfully.</span></span> <span data-ttu-id="2cd84-112">När uppdateringen är klar rapporteras den när den startas, är färdig och om den lyckades.</span><span class="sxs-lookup"><span data-stu-id="2cd84-112">Once the update is finished it reports when it started, finished, and if it was successful.</span></span>

## <span data-ttu-id="2cd84-113">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="2cd84-113">EXAMPLES</span></span>

### <span data-ttu-id="2cd84-114">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="2cd84-114">Example 1</span></span>
```
PS C:\> Update-AzMlOpClusterSystemService -ResourceGroupName my-group -Name my-cluster
```

<span data-ttu-id="2cd84-115">Startar en system tjänst uppdatering i angivet kluster.</span><span class="sxs-lookup"><span data-stu-id="2cd84-115">Starts a system services update on the specified cluster.</span></span> 

## <span data-ttu-id="2cd84-116">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="2cd84-116">PARAMETERS</span></span>

### <span data-ttu-id="2cd84-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2cd84-117">-DefaultProfile</span></span>
<span data-ttu-id="2cd84-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="2cd84-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2cd84-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2cd84-119">-InputObject</span></span>
<span data-ttu-id="2cd84-120">Operationalization.</span><span class="sxs-lookup"><span data-stu-id="2cd84-120">The operationalization cluster object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.MachineLearningCompute.Models.PSOperationalizationCluster
Parameter Sets: StartUpdateWithInputObject
Aliases: Cluster

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2cd84-121">-Namn</span><span class="sxs-lookup"><span data-stu-id="2cd84-121">-Name</span></span>
<span data-ttu-id="2cd84-122">Namnet på operationalization-klustret.</span><span class="sxs-lookup"><span data-stu-id="2cd84-122">The name of the operationalization cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: StartUpdateWithNameAndResourceGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2cd84-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2cd84-123">-ResourceGroupName</span></span>
<span data-ttu-id="2cd84-124">Namnet på resurs gruppen för operationalization-klustret.</span><span class="sxs-lookup"><span data-stu-id="2cd84-124">The name of the resource group for the operationalization cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: StartUpdateWithNameAndResourceGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2cd84-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="2cd84-125">-ResourceId</span></span>
<span data-ttu-id="2cd84-126">Azure Resource ID för operationalization-klustret.</span><span class="sxs-lookup"><span data-stu-id="2cd84-126">The Azure resource id for the operationalization cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: StartUpdateWithResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2cd84-127">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="2cd84-127">-Confirm</span></span>
<span data-ttu-id="2cd84-128">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="2cd84-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2cd84-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2cd84-129">-WhatIf</span></span>
<span data-ttu-id="2cd84-130">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="2cd84-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2cd84-131">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="2cd84-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2cd84-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2cd84-132">CommonParameters</span></span>
<span data-ttu-id="2cd84-133">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2cd84-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2cd84-134">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2cd84-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2cd84-135">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="2cd84-135">INPUTS</span></span>

### <span data-ttu-id="2cd84-136">Microsoft. Azure. commands. MachineLearningCompute. Models. PSOperationalizationCluster</span><span class="sxs-lookup"><span data-stu-id="2cd84-136">Microsoft.Azure.Commands.MachineLearningCompute.Models.PSOperationalizationCluster</span></span>

### <span data-ttu-id="2cd84-137">System. String</span><span class="sxs-lookup"><span data-stu-id="2cd84-137">System.String</span></span>

## <span data-ttu-id="2cd84-138">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="2cd84-138">OUTPUTS</span></span>

### <span data-ttu-id="2cd84-139">Microsoft. Azure. commands. MachineLearningCompute. Models. PSUpdateSystemServicesResponse</span><span class="sxs-lookup"><span data-stu-id="2cd84-139">Microsoft.Azure.Commands.MachineLearningCompute.Models.PSUpdateSystemServicesResponse</span></span>

## <span data-ttu-id="2cd84-140">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="2cd84-140">NOTES</span></span>

## <span data-ttu-id="2cd84-141">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="2cd84-141">RELATED LINKS</span></span>
