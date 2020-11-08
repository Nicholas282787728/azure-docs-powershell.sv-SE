---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/remove-azsynapsefirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseFirewallRule.md
ms.openlocfilehash: 6094c8d7e75136c9a9abf220ccfcb8775bda5dd7
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94269833"
---
# <span data-ttu-id="01c66-101">Remove-AzSynapseFirewallRule</span><span class="sxs-lookup"><span data-stu-id="01c66-101">Remove-AzSynapseFirewallRule</span></span>

## <span data-ttu-id="01c66-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="01c66-102">SYNOPSIS</span></span>
<span data-ttu-id="01c66-103">Tar bort en Synapse analys brand Väggs regel.</span><span class="sxs-lookup"><span data-stu-id="01c66-103">Deletes a Synapse Analytics Firewall Rule.</span></span>

## <span data-ttu-id="01c66-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="01c66-104">SYNTAX</span></span>

### <span data-ttu-id="01c66-105">DeleteByNameParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="01c66-105">DeleteByNameParameterSet (Default)</span></span>
```
Remove-AzSynapseFirewallRule [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String> [-PassThru]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="01c66-106">DeleteByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="01c66-106">DeleteByParentObjectParameterSet</span></span>
```
Remove-AzSynapseFirewallRule -Name <String> -WorkspaceObject <PSSynapseWorkspace> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="01c66-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="01c66-107">DESCRIPTION</span></span>
<span data-ttu-id="01c66-108">Cmdleten **Remove-AzSynapseFirewallRule** tar bort en Azure Synapse Analytics-brandväggsregel.</span><span class="sxs-lookup"><span data-stu-id="01c66-108">The **Remove-AzSynapseFirewallRule** cmdlet permanently deletes an Azure Synapse Analytics Firewall Rule.</span></span>

## <span data-ttu-id="01c66-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="01c66-109">EXAMPLES</span></span>

### <span data-ttu-id="01c66-110">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="01c66-110">Example 1</span></span>
```powershell
PS C:\> Remove-AzSynapseFirewallRule -ResourceGroupName ContosoResourceGroup -WorkspaceName ContosoWorkspace -Name ContosoFirewallRule
```

<span data-ttu-id="01c66-111">Det här kommandot tar bort brand Väggs regeln med namnet ContosoFirewallRule under arbets ytan ContosoWorkspace med namnet ContosoFirewallRule.</span><span class="sxs-lookup"><span data-stu-id="01c66-111">This command deletes firewall rule named ContosoFirewallRule under workspace ContosoWorkspace with name ContosoFirewallRule.</span></span>

### <span data-ttu-id="01c66-112">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="01c66-112">Example 2</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Remove-AzSynapseFirewallRule -Name ContosoFirewallRule
```

<span data-ttu-id="01c66-113">Det här kommandot tar bort brand Väggs regeln med namnet ContosoFirewallRule under en arbets yta via pipeline.</span><span class="sxs-lookup"><span data-stu-id="01c66-113">This command deletes firewall rule named ContosoFirewallRule under a workspace through pipeline.</span></span>

## <span data-ttu-id="01c66-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="01c66-114">PARAMETERS</span></span>

### <span data-ttu-id="01c66-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="01c66-115">-AsJob</span></span>
<span data-ttu-id="01c66-116">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="01c66-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="01c66-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="01c66-117">-DefaultProfile</span></span>
<span data-ttu-id="01c66-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="01c66-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="01c66-119">-Namn</span><span class="sxs-lookup"><span data-stu-id="01c66-119">-Name</span></span>
<span data-ttu-id="01c66-120">Firerwall regel namn för arbets ytan.</span><span class="sxs-lookup"><span data-stu-id="01c66-120">The firerwall rule name for the workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: FirewallRuleName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="01c66-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="01c66-121">-PassThru</span></span>
<span data-ttu-id="01c66-122">Denna cmdlet returnerar inte ett objekt som standard.</span><span class="sxs-lookup"><span data-stu-id="01c66-122">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="01c66-123">Om denna växel anges returnerar den sant om den är klar.</span><span class="sxs-lookup"><span data-stu-id="01c66-123">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="01c66-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="01c66-124">-ResourceGroupName</span></span>
<span data-ttu-id="01c66-125">Resurs grupps namn.</span><span class="sxs-lookup"><span data-stu-id="01c66-125">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="01c66-126">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="01c66-126">-WorkspaceName</span></span>
<span data-ttu-id="01c66-127">Namn på Synapse-arbetsyta.</span><span class="sxs-lookup"><span data-stu-id="01c66-127">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="01c66-128">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="01c66-128">-WorkspaceObject</span></span>
<span data-ttu-id="01c66-129">objekt för arbets yta, vanligt vis passerar genom pipeline.</span><span class="sxs-lookup"><span data-stu-id="01c66-129">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: DeleteByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="01c66-130">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="01c66-130">-Confirm</span></span>
<span data-ttu-id="01c66-131">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="01c66-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="01c66-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="01c66-132">-WhatIf</span></span>
<span data-ttu-id="01c66-133">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="01c66-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="01c66-134">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="01c66-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="01c66-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="01c66-135">CommonParameters</span></span>
<span data-ttu-id="01c66-136">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="01c66-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="01c66-137">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="01c66-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="01c66-138">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="01c66-138">INPUTS</span></span>

### <span data-ttu-id="01c66-139">Microsoft. Azure. commands. Synapse. Models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="01c66-139">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="01c66-140">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="01c66-140">OUTPUTS</span></span>

### <span data-ttu-id="01c66-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="01c66-141">System.Boolean</span></span>

## <span data-ttu-id="01c66-142">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="01c66-142">NOTES</span></span>

## <span data-ttu-id="01c66-143">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="01c66-143">RELATED LINKS</span></span>
