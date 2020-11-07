---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Kusto.dll-Help.xml
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/resume-azkustocluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/Kusto/help/Resume-AzKustoCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/Kusto/help/Resume-AzKustoCluster.md
ms.openlocfilehash: ce2fbe2f598ca6d08033c397a988f140379fda96
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93743833"
---
# <span data-ttu-id="89ee3-101">Resume-AzKustoCluster</span><span class="sxs-lookup"><span data-stu-id="89ee3-101">Resume-AzKustoCluster</span></span>

## <span data-ttu-id="89ee3-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="89ee3-102">SYNOPSIS</span></span>
<span data-ttu-id="89ee3-103">Återuppta ett inaktiverat Kusto-kluster.</span><span class="sxs-lookup"><span data-stu-id="89ee3-103">Resume a suspended Kusto cluster.</span></span>

## <span data-ttu-id="89ee3-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="89ee3-104">SYNTAX</span></span>

### <span data-ttu-id="89ee3-105">ByNameAndResourceGroup (standard)</span><span class="sxs-lookup"><span data-stu-id="89ee3-105">ByNameAndResourceGroup (Default)</span></span>
```
Resume-AzKustoCluster [[-ResourceGroupName] <String>] [-Name] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="89ee3-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="89ee3-106">ByResourceId</span></span>
```
Resume-AzKustoCluster [-ResourceId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="89ee3-107">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="89ee3-107">ByInputObject</span></span>
```
Resume-AzKustoCluster [-InputObject] <PSKustoCluster> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="89ee3-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="89ee3-108">DESCRIPTION</span></span>
<span data-ttu-id="89ee3-109">Återuppta ett inaktiverat Kusto-kluster.</span><span class="sxs-lookup"><span data-stu-id="89ee3-109">Resume a suspended Kusto cluster.</span></span>

## <span data-ttu-id="89ee3-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="89ee3-110">EXAMPLES</span></span>

### <span data-ttu-id="89ee3-111">Exempel 1-Resume a Suspended Kusto Cluster efter namn</span><span class="sxs-lookup"><span data-stu-id="89ee3-111">Example 1 - Resume a suspended Kusto cluster by name</span></span>

```
PS C:\> Resume-AzKustoCluster -ResourceGroupName testrg -Name mykustocluster
```

<span data-ttu-id="89ee3-112">Kommandot ovan återupptar det upphävda Kusto-klustret med namnet "mykustocluster" i resurs gruppen "testrg".</span><span class="sxs-lookup"><span data-stu-id="89ee3-112">The above command resumes the suspended Kusto cluster named "mykustocluster" found in the resource group "testrg".</span></span>

### <span data-ttu-id="89ee3-113">Exempel 2 – återuppta ett suspenderat Kusto-kluster genom att koppla</span><span class="sxs-lookup"><span data-stu-id="89ee3-113">Example 2 - Resume a suspended Kusto cluster by piping</span></span>

```
PS C:\> Get-AzKustoCluster -ResourceGroupName testrg -Name mykustocluster | Resume-AzKustoCluster
```

<span data-ttu-id="89ee3-114">Kommandot ovan får till Kusto-klustret med namnet "mykustocluster" i resurs gruppen "testrg" med hjälp av `Get-AzKustoCluster` cmdleten, och sedan flyttas resultatet till `Resume-AzKustoCluster` för att återuppta det.</span><span class="sxs-lookup"><span data-stu-id="89ee3-114">The above command gets the Kusto cluster named "mykustocluster" found in the resource group "testrg" using the `Get-AzKustoCluster` cmdlet, and then pipes the result to `Resume-AzKustoCluster` to resume it.</span></span>

## <span data-ttu-id="89ee3-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="89ee3-115">PARAMETERS</span></span>

### <span data-ttu-id="89ee3-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="89ee3-116">-DefaultProfile</span></span>
<span data-ttu-id="89ee3-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="89ee3-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="89ee3-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="89ee3-118">-InputObject</span></span>
<span data-ttu-id="89ee3-119">Kusto.</span><span class="sxs-lookup"><span data-stu-id="89ee3-119">Kusto cluster object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Kusto.Models.PSKustoCluster
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="89ee3-120">-Namn</span><span class="sxs-lookup"><span data-stu-id="89ee3-120">-Name</span></span>
<span data-ttu-id="89ee3-121">Namn på klustret som ska återupptas.</span><span class="sxs-lookup"><span data-stu-id="89ee3-121">Name of cluster to be resume.</span></span>

```yaml
Type: System.String
Parameter Sets: ByNameAndResourceGroup
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="89ee3-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="89ee3-122">-PassThru</span></span>
<span data-ttu-id="89ee3-123">Återvänd till det angivna klustret eller inte.</span><span class="sxs-lookup"><span data-stu-id="89ee3-123">Return whether the specified cluster was successfully resumed or not.</span></span>

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

### <span data-ttu-id="89ee3-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="89ee3-124">-ResourceGroupName</span></span>
<span data-ttu-id="89ee3-125">Namnet på den resurs grupp som klustret finns under.</span><span class="sxs-lookup"><span data-stu-id="89ee3-125">Name of resource group under which the cluster exists.</span></span>

```yaml
Type: System.String
Parameter Sets: ByNameAndResourceGroup
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="89ee3-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="89ee3-126">-ResourceId</span></span>
<span data-ttu-id="89ee3-127">Kusto-kluster-ResourceID.</span><span class="sxs-lookup"><span data-stu-id="89ee3-127">Kusto cluster ResourceID.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="89ee3-128">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="89ee3-128">-Confirm</span></span>
<span data-ttu-id="89ee3-129">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="89ee3-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="89ee3-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="89ee3-130">-WhatIf</span></span>
<span data-ttu-id="89ee3-131">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="89ee3-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="89ee3-132">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="89ee3-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="89ee3-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="89ee3-133">CommonParameters</span></span>
<span data-ttu-id="89ee3-134">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="89ee3-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="89ee3-135">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="89ee3-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="89ee3-136">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="89ee3-136">INPUTS</span></span>

### <span data-ttu-id="89ee3-137">System. String</span><span class="sxs-lookup"><span data-stu-id="89ee3-137">System.String</span></span>

### <span data-ttu-id="89ee3-138">Microsoft. Azure. commands. Kusto. Models. PSKustoCluster</span><span class="sxs-lookup"><span data-stu-id="89ee3-138">Microsoft.Azure.Commands.Kusto.Models.PSKustoCluster</span></span>

## <span data-ttu-id="89ee3-139">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="89ee3-139">OUTPUTS</span></span>

### <span data-ttu-id="89ee3-140">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="89ee3-140">System.Boolean</span></span>

## <span data-ttu-id="89ee3-141">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="89ee3-141">NOTES</span></span>

## <span data-ttu-id="89ee3-142">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="89ee3-142">RELATED LINKS</span></span>
