---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Kusto.dll-Help.xml
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/remove-azkustocluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/Kusto/help/Remove-AzKustoCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/Kusto/help/Remove-AzKustoCluster.md
ms.openlocfilehash: 3556ff99dafe804ab78899f8b0eefc64db4ca82b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93743834"
---
# <span data-ttu-id="4f603-101">Remove-AzKustoCluster</span><span class="sxs-lookup"><span data-stu-id="4f603-101">Remove-AzKustoCluster</span></span>

## <span data-ttu-id="4f603-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="4f603-102">SYNOPSIS</span></span>
<span data-ttu-id="4f603-103">Tar bort ett befintligt Kusto-kluster.</span><span class="sxs-lookup"><span data-stu-id="4f603-103">Deletes an existing Kusto cluster.</span></span>

## <span data-ttu-id="4f603-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="4f603-104">SYNTAX</span></span>

### <span data-ttu-id="4f603-105">ByNameAndResourceGroup (standard)</span><span class="sxs-lookup"><span data-stu-id="4f603-105">ByNameAndResourceGroup (Default)</span></span>
```
Remove-AzKustoCluster [-ResourceGroupName] <String> [-Name] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4f603-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="4f603-106">ByResourceId</span></span>
```
Remove-AzKustoCluster [-ResourceId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4f603-107">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="4f603-107">ByInputObject</span></span>
```
Remove-AzKustoCluster [-InputObject] <PSKustoCluster> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4f603-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="4f603-108">DESCRIPTION</span></span>
<span data-ttu-id="4f603-109">Tar bort ett befintligt Kusto-kluster.</span><span class="sxs-lookup"><span data-stu-id="4f603-109">Deletes an existing Kusto cluster.</span></span>

## <span data-ttu-id="4f603-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="4f603-110">EXAMPLES</span></span>

### <span data-ttu-id="4f603-111">Exempel 1 – ta bort ett befintligt Kusto-kluster med namn</span><span class="sxs-lookup"><span data-stu-id="4f603-111">Example 1 - Delete an existing Kusto cluster by name</span></span>

```
PS C:\> Remove-AzKustoCluster -ResourceGroupName testrg -Name mykustocluster
```

<span data-ttu-id="4f603-112">Kommandot ovan tar bort Kusto-klustret med namnet "mykustocluster" i resurs gruppen "testrg".</span><span class="sxs-lookup"><span data-stu-id="4f603-112">The above command deletes the Kusto cluster named "mykustocluster" in the resource group "testrg".</span></span>

### <span data-ttu-id="4f603-113">Exempel 2 – ta bort ett befintligt Kusto-kluster genom att rör</span><span class="sxs-lookup"><span data-stu-id="4f603-113">Example 2 - Delete an existing Kusto cluster by piping</span></span>

```
PS C:\> Get-AzKustoCluster -ResourceGroupName testrg -Name mykustocluster | Remove-AzKustoCluster
```

<span data-ttu-id="4f603-114">Kommandot ovan får till Kusto-klustret med namnet "mykustocluster" i resurs gruppen "testrg" med hjälp av `Get-AzKustoCluster` cmdleten och sedan flyttas resultatet till `Remove-AzKustoCluster` för att ta bort det.</span><span class="sxs-lookup"><span data-stu-id="4f603-114">The above command gets the Kusto cluster named "mykustocluster" in the resource group "testrg" using the `Get-AzKustoCluster` cmdlet, and then pipes the result to `Remove-AzKustoCluster` to delete it.</span></span>

## <span data-ttu-id="4f603-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="4f603-115">PARAMETERS</span></span>

### <span data-ttu-id="4f603-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4f603-116">-DefaultProfile</span></span>
<span data-ttu-id="4f603-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="4f603-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4f603-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4f603-118">-InputObject</span></span>
<span data-ttu-id="4f603-119">Kusto.</span><span class="sxs-lookup"><span data-stu-id="4f603-119">Kusto cluster object.</span></span>

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

### <span data-ttu-id="4f603-120">-Namn</span><span class="sxs-lookup"><span data-stu-id="4f603-120">-Name</span></span>
<span data-ttu-id="4f603-121">Namn på det kluster som ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="4f603-121">Name of cluster to be removed.</span></span>

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

### <span data-ttu-id="4f603-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="4f603-122">-PassThru</span></span>
<span data-ttu-id="4f603-123">Återvänd till det angivna klustret eller inte.</span><span class="sxs-lookup"><span data-stu-id="4f603-123">Return whether the specified cluster was successfully deleted or not.</span></span>

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

### <span data-ttu-id="4f603-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4f603-124">-ResourceGroupName</span></span>
<span data-ttu-id="4f603-125">Namnet på den resurs grupp som klustret finns under.</span><span class="sxs-lookup"><span data-stu-id="4f603-125">Name of resource group under which the cluster exists.</span></span>

```yaml
Type: System.String
Parameter Sets: ByNameAndResourceGroup
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4f603-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="4f603-126">-ResourceId</span></span>
<span data-ttu-id="4f603-127">Kusto-kluster-ResourceID.</span><span class="sxs-lookup"><span data-stu-id="4f603-127">Kusto cluster ResourceID.</span></span>

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

### <span data-ttu-id="4f603-128">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="4f603-128">-Confirm</span></span>
<span data-ttu-id="4f603-129">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="4f603-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4f603-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4f603-130">-WhatIf</span></span>
<span data-ttu-id="4f603-131">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="4f603-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4f603-132">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="4f603-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4f603-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4f603-133">CommonParameters</span></span>
<span data-ttu-id="4f603-134">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4f603-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4f603-135">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4f603-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4f603-136">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="4f603-136">INPUTS</span></span>

### <span data-ttu-id="4f603-137">System. String</span><span class="sxs-lookup"><span data-stu-id="4f603-137">System.String</span></span>

### <span data-ttu-id="4f603-138">Microsoft. Azure. commands. Kusto. Models. PSKustoCluster</span><span class="sxs-lookup"><span data-stu-id="4f603-138">Microsoft.Azure.Commands.Kusto.Models.PSKustoCluster</span></span>

## <span data-ttu-id="4f603-139">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="4f603-139">OUTPUTS</span></span>

### <span data-ttu-id="4f603-140">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="4f603-140">System.Boolean</span></span>

## <span data-ttu-id="4f603-141">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="4f603-141">NOTES</span></span>

## <span data-ttu-id="4f603-142">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="4f603-142">RELATED LINKS</span></span>
