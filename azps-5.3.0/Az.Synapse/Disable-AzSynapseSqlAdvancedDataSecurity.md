---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/disable-azsynapsesqladvanceddatasecurity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Disable-AzSynapseSqlAdvancedDataSecurity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Disable-AzSynapseSqlAdvancedDataSecurity.md
ms.openlocfilehash: 2cbc79314d9e5fc7dac524786b8ba0bfa349573b
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98424576"
---
# <span data-ttu-id="f5161-101">Disable-AzSynapseSqlAdvancedDataSecurity</span><span class="sxs-lookup"><span data-stu-id="f5161-101">Disable-AzSynapseSqlAdvancedDataSecurity</span></span>

## <span data-ttu-id="f5161-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="f5161-102">SYNOPSIS</span></span>
<span data-ttu-id="f5161-103">Inaktiverar avancerad data säkerhet på en arbets yta.</span><span class="sxs-lookup"><span data-stu-id="f5161-103">Disables Advanced Data Security on a workspace.</span></span>

## <span data-ttu-id="f5161-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="f5161-104">SYNTAX</span></span>

### <span data-ttu-id="f5161-105">DisableByNameParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="f5161-105">DisableByNameParameterSet (Default)</span></span>
```
Disable-AzSynapseSqlAdvancedDataSecurity [-ResourceGroupName <String>] -WorkspaceName <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f5161-106">DisableByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="f5161-106">DisableByInputObjectParameterSet</span></span>
```
Disable-AzSynapseSqlAdvancedDataSecurity -InputObject <PSSynapseWorkspace> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f5161-107">DisableByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="f5161-107">DisableByResourceIdParameterSet</span></span>
```
Disable-AzSynapseSqlAdvancedDataSecurity -ResourceId <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f5161-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="f5161-108">DESCRIPTION</span></span>
<span data-ttu-id="f5161-109">Cmdleten **disable-AzSynapseSqlAdvancedDataSecurity** inaktiverar avancerad data säkerhet på en arbets yta.</span><span class="sxs-lookup"><span data-stu-id="f5161-109">The **Disable-AzSynapseSqlAdvancedDataSecurity** cmdlet disables Advanced Data Security on a workspace.</span></span>

## <span data-ttu-id="f5161-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="f5161-110">EXAMPLES</span></span>

### <span data-ttu-id="f5161-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="f5161-111">Example 1</span></span>
```powershell
PS C:\> Disable-AzSynapseSqlAdvancedDataSecurity -WorkspaceName ContosoWorkspace
```

<span data-ttu-id="f5161-112">Det här kommandot inaktiverar avancerad data säkerhet på arbets ytan med namnet ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="f5161-112">This command disables Advanced Data Security on the workspace named ContosoWorkspace.</span></span>

### <span data-ttu-id="f5161-113">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="f5161-113">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapseWorkspace -Name ContosoWorkspace | Disable-AzSynapseSqlAdvancedDataSecurity
```

<span data-ttu-id="f5161-114">Det här kommandot inaktiverar avancerad data säkerhet på arbets ytan som heter ContosoWorkspace via pipeline.</span><span class="sxs-lookup"><span data-stu-id="f5161-114">This command disables Advanced Data Security on the workspace named ContosoWorkspace through pipeline.</span></span>

## <span data-ttu-id="f5161-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="f5161-115">PARAMETERS</span></span>

### <span data-ttu-id="f5161-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f5161-116">-AsJob</span></span>
<span data-ttu-id="f5161-117">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="f5161-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="f5161-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f5161-118">-DefaultProfile</span></span>
<span data-ttu-id="f5161-119">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="f5161-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f5161-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f5161-120">-InputObject</span></span>
<span data-ttu-id="f5161-121">objekt för arbets yta, vanligt vis passerar genom pipeline.</span><span class="sxs-lookup"><span data-stu-id="f5161-121">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: DisableByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f5161-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f5161-122">-ResourceGroupName</span></span>
<span data-ttu-id="f5161-123">Resurs grupps namn.</span><span class="sxs-lookup"><span data-stu-id="f5161-123">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: DisableByNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f5161-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f5161-124">-ResourceId</span></span>
<span data-ttu-id="f5161-125">Resurs-ID för Synapse-arbetsyta.</span><span class="sxs-lookup"><span data-stu-id="f5161-125">Resource identifier of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: DisableByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f5161-126">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="f5161-126">-WorkspaceName</span></span>
<span data-ttu-id="f5161-127">Namn på Synapse-arbetsyta.</span><span class="sxs-lookup"><span data-stu-id="f5161-127">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: DisableByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f5161-128">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="f5161-128">-Confirm</span></span>
<span data-ttu-id="f5161-129">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="f5161-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f5161-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f5161-130">-WhatIf</span></span>
<span data-ttu-id="f5161-131">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="f5161-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f5161-132">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="f5161-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f5161-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f5161-133">CommonParameters</span></span>
<span data-ttu-id="f5161-134">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f5161-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f5161-135">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f5161-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f5161-136">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="f5161-136">INPUTS</span></span>

### <span data-ttu-id="f5161-137">Microsoft. Azure. commands. Synapse. Models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="f5161-137">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="f5161-138">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="f5161-138">OUTPUTS</span></span>

### <span data-ttu-id="f5161-139">Microsoft. Azure. commands. Synapse. Models. WorkspaceAdvancedDataSecurityPolicy</span><span class="sxs-lookup"><span data-stu-id="f5161-139">Microsoft.Azure.Commands.Synapse.Models.WorkspaceAdvancedDataSecurityPolicy</span></span>

## <span data-ttu-id="f5161-140">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="f5161-140">NOTES</span></span>

## <span data-ttu-id="f5161-141">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="f5161-141">RELATED LINKS</span></span>
