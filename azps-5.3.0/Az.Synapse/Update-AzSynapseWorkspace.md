---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/update-azsynapseworkspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Update-AzSynapseWorkspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Update-AzSynapseWorkspace.md
ms.openlocfilehash: 84180165e835678dc74a7ed08f6a06c51cec8134
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98422736"
---
# <span data-ttu-id="b5bf8-101">Update-AzSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="b5bf8-101">Update-AzSynapseWorkspace</span></span>

## <span data-ttu-id="b5bf8-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="b5bf8-102">SYNOPSIS</span></span>
<span data-ttu-id="b5bf8-103">Uppdaterar en Synapse Analytics-arbetsyta.</span><span class="sxs-lookup"><span data-stu-id="b5bf8-103">Updates a Synapse Analytics workspace.</span></span>

## <span data-ttu-id="b5bf8-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="b5bf8-104">SYNTAX</span></span>

### <span data-ttu-id="b5bf8-105">SetByNameParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="b5bf8-105">SetByNameParameterSet (Default)</span></span>
```
Update-AzSynapseWorkspace [-ResourceGroupName <String>] [-Name <String>] [-Tag <Hashtable>]
 [-SqlAdministratorLoginPassword <SecureString>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b5bf8-106">SetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="b5bf8-106">SetByInputObjectParameterSet</span></span>
```
Update-AzSynapseWorkspace -InputObject <PSSynapseWorkspace> [-Tag <Hashtable>]
 [-SqlAdministratorLoginPassword <SecureString>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b5bf8-107">SetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="b5bf8-107">SetByResourceIdParameterSet</span></span>
```
Update-AzSynapseWorkspace -ResourceId <String> [-Tag <Hashtable>]
 [-SqlAdministratorLoginPassword <SecureString>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b5bf8-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="b5bf8-108">DESCRIPTION</span></span>
<span data-ttu-id="b5bf8-109">Cmdleten **Update-AzSynapseWorkspace** uppdaterar en Azure Synapse Analytics-arbetsyta.</span><span class="sxs-lookup"><span data-stu-id="b5bf8-109">The **Update-AzSynapseWorkspace** cmdlet updates an Azure Synapse Analytics workspace.</span></span>

## <span data-ttu-id="b5bf8-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="b5bf8-110">EXAMPLES</span></span>

### <span data-ttu-id="b5bf8-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="b5bf8-111">Example 1</span></span>
```powershell
PS C:\> Update-AzSynapseWorkspace -Name ContosoWorkspace -Tag @{'key'='value'}
```

<span data-ttu-id="b5bf8-112">Det här kommandot uppdaterar taggar för specififed Azure Synapse Analytics-arbets ytan.</span><span class="sxs-lookup"><span data-stu-id="b5bf8-112">This commands updates tags for the specififed Azure Synapse Analytics workspace.</span></span>

### <span data-ttu-id="b5bf8-113">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="b5bf8-113">Example 2</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Update-AzSynapseWorkspace -Tag @{'key'='value1'}
```

<span data-ttu-id="b5bf8-114">Det här kommandot uppdaterar taggar för specififed Azure Synapse Analytics-arbets ytan via pipeline.</span><span class="sxs-lookup"><span data-stu-id="b5bf8-114">This commands updates tags for the specififed Azure Synapse Analytics workspace through pipeline.</span></span>

### <span data-ttu-id="b5bf8-115">Exempel 3</span><span class="sxs-lookup"><span data-stu-id="b5bf8-115">Example 3</span></span>
```powershell
PS C:\> Update-AzSynapseWorkspace -ResourceId /subscriptions/21686af7-58ec-4f4d-9c68-f431f4db4edd/resourceGroups/ContosoResourceGroup/providers/Microsoft.Synapse/workspaces/ContosoWorkspace -Tag @{'key'='value2'}
```

<span data-ttu-id="b5bf8-116">Det här kommandot uppdaterar taggar för specififed Azure Synapse Analytics-arbetsyta via pipeline med resurs-ID.</span><span class="sxs-lookup"><span data-stu-id="b5bf8-116">This commands updates tags for the specififed Azure Synapse Analytics workspace through pipeline with resource ID.</span></span>

## <span data-ttu-id="b5bf8-117">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="b5bf8-117">PARAMETERS</span></span>

### <span data-ttu-id="b5bf8-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b5bf8-118">-AsJob</span></span>
<span data-ttu-id="b5bf8-119">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="b5bf8-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="b5bf8-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b5bf8-120">-DefaultProfile</span></span>
<span data-ttu-id="b5bf8-121">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="b5bf8-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b5bf8-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b5bf8-122">-InputObject</span></span>
<span data-ttu-id="b5bf8-123">objekt för arbets yta, vanligt vis passerar genom pipeline.</span><span class="sxs-lookup"><span data-stu-id="b5bf8-123">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: SetByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b5bf8-124">-Namn</span><span class="sxs-lookup"><span data-stu-id="b5bf8-124">-Name</span></span>
<span data-ttu-id="b5bf8-125">Namn på Synapse-arbetsyta.</span><span class="sxs-lookup"><span data-stu-id="b5bf8-125">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByNameParameterSet
Aliases: WorkspaceName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b5bf8-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b5bf8-126">-ResourceGroupName</span></span>
<span data-ttu-id="b5bf8-127">Resurs grupps namn.</span><span class="sxs-lookup"><span data-stu-id="b5bf8-127">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b5bf8-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b5bf8-128">-ResourceId</span></span>
<span data-ttu-id="b5bf8-129">Resurs-ID för Synapse-arbetsyta.</span><span class="sxs-lookup"><span data-stu-id="b5bf8-129">Resource identifier of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b5bf8-130">-SqlAdministratorLoginPassword</span><span class="sxs-lookup"><span data-stu-id="b5bf8-130">-SqlAdministratorLoginPassword</span></span>
<span data-ttu-id="b5bf8-131">Det nya administratörs lösen ordet för arbets ytan.</span><span class="sxs-lookup"><span data-stu-id="b5bf8-131">The new SQL administrator password for the workspace.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b5bf8-132">-Tagg</span><span class="sxs-lookup"><span data-stu-id="b5bf8-132">-Tag</span></span>
<span data-ttu-id="b5bf8-133">En sträng, en sträng ord lista med flaggor associerade med resursen.</span><span class="sxs-lookup"><span data-stu-id="b5bf8-133">A string,string dictionary of tags associated with the resource.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b5bf8-134">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="b5bf8-134">-Confirm</span></span>
<span data-ttu-id="b5bf8-135">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="b5bf8-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b5bf8-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b5bf8-136">-WhatIf</span></span>
<span data-ttu-id="b5bf8-137">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="b5bf8-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b5bf8-138">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="b5bf8-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b5bf8-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b5bf8-139">CommonParameters</span></span>
<span data-ttu-id="b5bf8-140">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b5bf8-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b5bf8-141">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b5bf8-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b5bf8-142">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="b5bf8-142">INPUTS</span></span>

### <span data-ttu-id="b5bf8-143">Microsoft. Azure. commands. Synapse. Models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="b5bf8-143">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="b5bf8-144">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="b5bf8-144">OUTPUTS</span></span>

### <span data-ttu-id="b5bf8-145">Microsoft. Azure. commands. Synapse. Models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="b5bf8-145">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="b5bf8-146">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="b5bf8-146">NOTES</span></span>

## <span data-ttu-id="b5bf8-147">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="b5bf8-147">RELATED LINKS</span></span>
