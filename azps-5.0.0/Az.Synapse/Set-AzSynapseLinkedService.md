---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/set-azsynapselinkedservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Set-AzSynapseLinkedService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Set-AzSynapseLinkedService.md
ms.openlocfilehash: 635c1e064dbc081a5207f5c912c14166b2b01e17
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94269390"
---
# <span data-ttu-id="743cc-101">Set-AzSynapseLinkedService</span><span class="sxs-lookup"><span data-stu-id="743cc-101">Set-AzSynapseLinkedService</span></span>

## <span data-ttu-id="743cc-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="743cc-102">SYNOPSIS</span></span>
<span data-ttu-id="743cc-103">Länkar ett data lager eller en moln tjänst till arbets ytan.</span><span class="sxs-lookup"><span data-stu-id="743cc-103">Links a data store or a cloud service to workspace.</span></span>

## <span data-ttu-id="743cc-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="743cc-104">SYNTAX</span></span>

### <span data-ttu-id="743cc-105">SetByName (standard)</span><span class="sxs-lookup"><span data-stu-id="743cc-105">SetByName (Default)</span></span>
```
Set-AzSynapseLinkedService -WorkspaceName <String> -Name <String> -DefinitionFile <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="743cc-106">SetByObject</span><span class="sxs-lookup"><span data-stu-id="743cc-106">SetByObject</span></span>
```
Set-AzSynapseLinkedService -WorkspaceObject <PSSynapseWorkspace> -Name <String> -DefinitionFile <String>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="743cc-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="743cc-107">DESCRIPTION</span></span>
<span data-ttu-id="743cc-108">Cmdleten **set-AzSynapseLinkedService** länkar ett data lager eller en moln tjänst till arbets ytan.</span><span class="sxs-lookup"><span data-stu-id="743cc-108">The **Set-AzSynapseLinkedService** cmdlet links a data store or a cloud service to workspace.</span></span>

## <span data-ttu-id="743cc-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="743cc-109">EXAMPLES</span></span>

### <span data-ttu-id="743cc-110">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="743cc-110">Example 1</span></span>
```powershell
PS C:\> Set-AzSynapseLinkedService -WorkspaceName ContosoWorkspace -Name ContosoLinkedService -DefinitionFile "C:\\samples\\LinkedService.json"
```

<span data-ttu-id="743cc-111">Det här kommandot skapar en länkad tjänst som heter ContosoLinkedService i arbets ytan med namnet ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="743cc-111">This command creates a linked service named ContosoLinkedService in the workspace named ContosoWorkspace.</span></span>

### <span data-ttu-id="743cc-112">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="743cc-112">Example 2</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Set-AzSynapseLinkedService -Name ContosoLinkedService -DefinitionFile "C:\\samples\\LinkedService.json"
```

<span data-ttu-id="743cc-113">Det här kommandot skapar en länkad tjänst som heter ContosoLinkedService i arbets ytan ContosoWorkspace via pipeline.</span><span class="sxs-lookup"><span data-stu-id="743cc-113">This command creates a linked service named ContosoLinkedService in the workspace named ContosoWorkspace through pipeline.</span></span>

## <span data-ttu-id="743cc-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="743cc-114">PARAMETERS</span></span>

### <span data-ttu-id="743cc-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="743cc-115">-AsJob</span></span>
<span data-ttu-id="743cc-116">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="743cc-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="743cc-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="743cc-117">-DefaultProfile</span></span>
<span data-ttu-id="743cc-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="743cc-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="743cc-119">-DefinitionFile</span><span class="sxs-lookup"><span data-stu-id="743cc-119">-DefinitionFile</span></span>
<span data-ttu-id="743cc-120">Sökvägen till JSON-filen.</span><span class="sxs-lookup"><span data-stu-id="743cc-120">The JSON file path.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: File

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="743cc-121">-Namn</span><span class="sxs-lookup"><span data-stu-id="743cc-121">-Name</span></span>
<span data-ttu-id="743cc-122">Namnet på den länkade tjänsten.</span><span class="sxs-lookup"><span data-stu-id="743cc-122">The linked service name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: LinkedServiceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="743cc-123">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="743cc-123">-WorkspaceName</span></span>
<span data-ttu-id="743cc-124">Namn på Synapse-arbetsyta.</span><span class="sxs-lookup"><span data-stu-id="743cc-124">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="743cc-125">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="743cc-125">-WorkspaceObject</span></span>
<span data-ttu-id="743cc-126">objekt för arbets yta, vanligt vis passerar genom pipeline.</span><span class="sxs-lookup"><span data-stu-id="743cc-126">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: SetByObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="743cc-127">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="743cc-127">-Confirm</span></span>
<span data-ttu-id="743cc-128">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="743cc-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="743cc-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="743cc-129">-WhatIf</span></span>
<span data-ttu-id="743cc-130">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="743cc-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="743cc-131">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="743cc-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="743cc-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="743cc-132">CommonParameters</span></span>
<span data-ttu-id="743cc-133">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="743cc-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="743cc-134">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="743cc-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="743cc-135">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="743cc-135">INPUTS</span></span>

### <span data-ttu-id="743cc-136">Microsoft. Azure. commands. Synapse. Models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="743cc-136">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="743cc-137">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="743cc-137">OUTPUTS</span></span>

### <span data-ttu-id="743cc-138">Microsoft. Azure. commands. Synapse. Models. PSLinkedServiceResource</span><span class="sxs-lookup"><span data-stu-id="743cc-138">Microsoft.Azure.Commands.Synapse.Models.PSLinkedServiceResource</span></span>

## <span data-ttu-id="743cc-139">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="743cc-139">NOTES</span></span>

## <span data-ttu-id="743cc-140">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="743cc-140">RELATED LINKS</span></span>
