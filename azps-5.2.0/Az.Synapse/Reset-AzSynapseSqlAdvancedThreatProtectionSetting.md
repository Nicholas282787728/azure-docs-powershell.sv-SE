---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/reset-azsynapsesqladvancedthreatprotectionsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Reset-AzSynapseSqlAdvancedThreatProtectionSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Reset-AzSynapseSqlAdvancedThreatProtectionSetting.md
ms.openlocfilehash: 420b95d8d20d21758e4f42db6c31e2d1ead557ac
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98394251"
---
# <span data-ttu-id="10ab9-101">Reset-AzSynapseSqlAdvancedThreatProtectionSetting</span><span class="sxs-lookup"><span data-stu-id="10ab9-101">Reset-AzSynapseSqlAdvancedThreatProtectionSetting</span></span>

## <span data-ttu-id="10ab9-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="10ab9-102">SYNOPSIS</span></span>
<span data-ttu-id="10ab9-103">Tar bort de avancerade skydds inställningarna från en arbets yta.</span><span class="sxs-lookup"><span data-stu-id="10ab9-103">Removes the advanced threat protection settings from a workspace.</span></span>

## <span data-ttu-id="10ab9-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="10ab9-104">SYNTAX</span></span>

### <span data-ttu-id="10ab9-105">ClearByNameParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="10ab9-105">ClearByNameParameterSet (Default)</span></span>
```
Reset-AzSynapseSqlAdvancedThreatProtectionSetting [-ResourceGroupName <String>] -WorkspaceName <String>
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="10ab9-106">ClearByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="10ab9-106">ClearByInputObjectParameterSet</span></span>
```
Reset-AzSynapseSqlAdvancedThreatProtectionSetting -InputObject <PSSynapseWorkspace> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="10ab9-107">ClearByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="10ab9-107">ClearByResourceIdParameterSet</span></span>
```
Reset-AzSynapseSqlAdvancedThreatProtectionSetting -ResourceId <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="10ab9-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="10ab9-108">DESCRIPTION</span></span>
<span data-ttu-id="10ab9-109">Cmdleten **Reset-AzSynapseSqlAdvancedThreatProtectionSetting** tar bort de avancerade skydds inställningarna från en Azure Synapse Analytics-arbetsyta.</span><span class="sxs-lookup"><span data-stu-id="10ab9-109">The **Reset-AzSynapseSqlAdvancedThreatProtectionSetting** cmdlet removes the advanced threat protection settings from an Azure Synapse Analytics Workspace.</span></span>

## <span data-ttu-id="10ab9-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="10ab9-110">EXAMPLES</span></span>

### <span data-ttu-id="10ab9-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="10ab9-111">Example 1</span></span>
```powershell
PS C:\> Reset-AzSynapseSqlAdvancedThreatProtectionSetting -WorkspaceName ContosoWorkspace
```

<span data-ttu-id="10ab9-112">Det här kommandot tar bort avancerade skydds inställningar från en arbets yta med namnet ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="10ab9-112">This command removes the advanced threat protection settings from a workspace named ContosoWorkspace.</span></span>

## <span data-ttu-id="10ab9-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="10ab9-113">PARAMETERS</span></span>

### <span data-ttu-id="10ab9-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="10ab9-114">-AsJob</span></span>
<span data-ttu-id="10ab9-115">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="10ab9-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="10ab9-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="10ab9-116">-DefaultProfile</span></span>
<span data-ttu-id="10ab9-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="10ab9-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="10ab9-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="10ab9-118">-InputObject</span></span>
<span data-ttu-id="10ab9-119">objekt för arbets yta, vanligt vis passerar genom pipeline.</span><span class="sxs-lookup"><span data-stu-id="10ab9-119">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: ClearByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="10ab9-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="10ab9-120">-PassThru</span></span>
<span data-ttu-id="10ab9-121">Denna cmdlet returnerar inte ett objekt som standard.</span><span class="sxs-lookup"><span data-stu-id="10ab9-121">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="10ab9-122">Om denna växel anges returnerar den sant om den är klar.</span><span class="sxs-lookup"><span data-stu-id="10ab9-122">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="10ab9-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="10ab9-123">-ResourceGroupName</span></span>
<span data-ttu-id="10ab9-124">Resurs grupps namn.</span><span class="sxs-lookup"><span data-stu-id="10ab9-124">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ClearByNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="10ab9-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="10ab9-125">-ResourceId</span></span>
<span data-ttu-id="10ab9-126">Resurs-ID för Synapse-arbetsyta.</span><span class="sxs-lookup"><span data-stu-id="10ab9-126">Resource identifier of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: ClearByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="10ab9-127">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="10ab9-127">-WorkspaceName</span></span>
<span data-ttu-id="10ab9-128">Namn på Synapse-arbetsyta.</span><span class="sxs-lookup"><span data-stu-id="10ab9-128">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: ClearByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="10ab9-129">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="10ab9-129">-Confirm</span></span>
<span data-ttu-id="10ab9-130">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="10ab9-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="10ab9-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="10ab9-131">-WhatIf</span></span>
<span data-ttu-id="10ab9-132">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="10ab9-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="10ab9-133">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="10ab9-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="10ab9-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="10ab9-134">CommonParameters</span></span>
<span data-ttu-id="10ab9-135">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="10ab9-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="10ab9-136">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="10ab9-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="10ab9-137">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="10ab9-137">INPUTS</span></span>

### <span data-ttu-id="10ab9-138">Microsoft. Azure. commands. Synapse. Models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="10ab9-138">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="10ab9-139">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="10ab9-139">OUTPUTS</span></span>

### <span data-ttu-id="10ab9-140">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="10ab9-140">System.Boolean</span></span>

## <span data-ttu-id="10ab9-141">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="10ab9-141">NOTES</span></span>

## <span data-ttu-id="10ab9-142">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="10ab9-142">RELATED LINKS</span></span>
