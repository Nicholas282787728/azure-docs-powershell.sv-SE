---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/reset-azsynapsesqlauditsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Reset-AzSynapseSqlAuditSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Reset-AzSynapseSqlAuditSetting.md
ms.openlocfilehash: b25ca2a026cf5d82aa25f69868ca8605fd75bced
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98393667"
---
# <span data-ttu-id="cd676-101">Reset-AzSynapseSqlAuditSetting</span><span class="sxs-lookup"><span data-stu-id="cd676-101">Reset-AzSynapseSqlAuditSetting</span></span>

## <span data-ttu-id="cd676-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="cd676-102">SYNOPSIS</span></span>
<span data-ttu-id="cd676-103">Tar bort gransknings inställningar för en Azure Synapse Analytics-arbetsyta.</span><span class="sxs-lookup"><span data-stu-id="cd676-103">Removes the auditing settings of an Azure Synapse Analytics Workspace.</span></span>

## <span data-ttu-id="cd676-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="cd676-104">SYNTAX</span></span>

### <span data-ttu-id="cd676-105">RemoveByNameParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="cd676-105">RemoveByNameParameterSet (Default)</span></span>
```
Reset-AzSynapseSqlAuditSetting [-ResourceGroupName <String>] -WorkspaceName <String> [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cd676-106">RemoveByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="cd676-106">RemoveByInputObjectParameterSet</span></span>
```
Reset-AzSynapseSqlAuditSetting -InputObject <PSSynapseWorkspace> [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cd676-107">RemoveByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="cd676-107">RemoveByResourceIdParameterSet</span></span>
```
Reset-AzSynapseSqlAuditSetting -ResourceId <String> [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cd676-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="cd676-108">DESCRIPTION</span></span>
<span data-ttu-id="cd676-109">Cmdleten **Reset-AzSynapseSqlAuditSetting** tar bort gransknings inställningarna för en Azure Synapse Analytics-arbetsyta.</span><span class="sxs-lookup"><span data-stu-id="cd676-109">The **Reset-AzSynapseSqlAuditSetting** cmdlet removes the auditing settings of an Azure Synapse Analytics Workspace.</span></span>

## <span data-ttu-id="cd676-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="cd676-110">EXAMPLES</span></span>

### <span data-ttu-id="cd676-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="cd676-111">Example 1</span></span>
```powershell
PS C:\> Reset-AzSynapseSqlAuditSetting -WorkspaceName ContosoWorkspace
```

<span data-ttu-id="cd676-112">Det här kommandot tar bort gransknings inställningarna för en Azure Synapse-arbetsyta med namnet ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="cd676-112">This command removes the auditing settings of an Azure Synapse Analytics Workspace named ContosoWorkspace.</span></span>

### <span data-ttu-id="cd676-113">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="cd676-113">Example 2</span></span>
```powershell
PS C:\> Get-AzSynapseWorkspace -Name ContosoWorkspace | Reset-AzSynapseSqlAuditSetting
```

<span data-ttu-id="cd676-114">Det här kommandot tar bort gransknings inställningarna för en Azure Synapse-arbetsyta med namnet ContosoWorkspace via pipeline.</span><span class="sxs-lookup"><span data-stu-id="cd676-114">This command removes the auditing settings of an Azure Synapse Analytics Workspace named ContosoWorkspace through pipeline.</span></span>

## <span data-ttu-id="cd676-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="cd676-115">PARAMETERS</span></span>

### <span data-ttu-id="cd676-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="cd676-116">-AsJob</span></span>
<span data-ttu-id="cd676-117">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="cd676-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="cd676-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cd676-118">-DefaultProfile</span></span>
<span data-ttu-id="cd676-119">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="cd676-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cd676-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="cd676-120">-InputObject</span></span>
<span data-ttu-id="cd676-121">objekt för arbets yta, vanligt vis passerar genom pipeline.</span><span class="sxs-lookup"><span data-stu-id="cd676-121">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: RemoveByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="cd676-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="cd676-122">-PassThru</span></span>
<span data-ttu-id="cd676-123">Denna cmdlet returnerar inte ett objekt som standard.</span><span class="sxs-lookup"><span data-stu-id="cd676-123">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="cd676-124">Om denna växel anges returnerar den sant om den är klar.</span><span class="sxs-lookup"><span data-stu-id="cd676-124">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="cd676-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cd676-125">-ResourceGroupName</span></span>
<span data-ttu-id="cd676-126">Resurs grupps namn.</span><span class="sxs-lookup"><span data-stu-id="cd676-126">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cd676-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="cd676-127">-ResourceId</span></span>
<span data-ttu-id="cd676-128">Resurs-ID för Synapse-arbetsyta.</span><span class="sxs-lookup"><span data-stu-id="cd676-128">Resource identifier of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cd676-129">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="cd676-129">-WorkspaceName</span></span>
<span data-ttu-id="cd676-130">Namn på Synapse-arbetsyta.</span><span class="sxs-lookup"><span data-stu-id="cd676-130">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cd676-131">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="cd676-131">-Confirm</span></span>
<span data-ttu-id="cd676-132">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="cd676-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cd676-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cd676-133">-WhatIf</span></span>
<span data-ttu-id="cd676-134">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="cd676-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cd676-135">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="cd676-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cd676-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cd676-136">CommonParameters</span></span>
<span data-ttu-id="cd676-137">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cd676-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cd676-138">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="cd676-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cd676-139">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="cd676-139">INPUTS</span></span>

### <span data-ttu-id="cd676-140">Microsoft. Azure. commands. Synapse. Models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="cd676-140">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="cd676-141">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="cd676-141">OUTPUTS</span></span>

### <span data-ttu-id="cd676-142">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="cd676-142">System.Boolean</span></span>

## <span data-ttu-id="cd676-143">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="cd676-143">NOTES</span></span>

## <span data-ttu-id="cd676-144">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="cd676-144">RELATED LINKS</span></span>
