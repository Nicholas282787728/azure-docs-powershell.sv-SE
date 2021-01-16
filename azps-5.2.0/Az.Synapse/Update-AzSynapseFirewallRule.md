---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/update-azsynapsefirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Update-AzSynapseFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Update-AzSynapseFirewallRule.md
ms.openlocfilehash: 9188a1cc8dde39db4d755fb2059f3633fc85ead8
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98394011"
---
# <span data-ttu-id="5321a-101">Update-AzSynapseFirewallRule</span><span class="sxs-lookup"><span data-stu-id="5321a-101">Update-AzSynapseFirewallRule</span></span>

## <span data-ttu-id="5321a-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="5321a-102">SYNOPSIS</span></span>
<span data-ttu-id="5321a-103">Uppdaterar en Synapse för analys brand vägg.</span><span class="sxs-lookup"><span data-stu-id="5321a-103">Updates a Synapse Analytics Firewall Rule.</span></span>

## <span data-ttu-id="5321a-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="5321a-104">SYNTAX</span></span>

### <span data-ttu-id="5321a-105">UpdateByNameParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="5321a-105">UpdateByNameParameterSet (Default)</span></span>
```
Update-AzSynapseFirewallRule [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String>
 [-StartIpAddress <String>] [-EndIpAddress <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5321a-106">UpdateByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="5321a-106">UpdateByParentObjectParameterSet</span></span>
```
Update-AzSynapseFirewallRule -WorkspaceObject <PSSynapseWorkspace> -Name <String> [-StartIpAddress <String>]
 [-EndIpAddress <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="5321a-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="5321a-107">DESCRIPTION</span></span>
<span data-ttu-id="5321a-108">Cmdleten **Update-AzSynapseFirewallRule** ändrar en Azure Synapse Analytics-brandväggsregel.</span><span class="sxs-lookup"><span data-stu-id="5321a-108">The **Update-AzSynapseFirewallRule** cmdlet modifys an Azure Synapse Analytics Firewall Rule.</span></span>

## <span data-ttu-id="5321a-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="5321a-109">EXAMPLES</span></span>

### <span data-ttu-id="5321a-110">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="5321a-110">Example 1</span></span>
```powershell
PS C:\> Update-AzSynapseFirewallRule -ResourceGroupName ContosoResourceGroup -WorkspaceName ContosoWorkspace -Name ContosoFirewallRule -StartIpAddress "0.0.0.0" -EndIpAssdress "255.255.255.255"
```

<span data-ttu-id="5321a-111">Det här kommandot uppdaterar brand Väggs regeln med namnet ContosoFirewallRule under arbets ytan ContosoWorkspace med namnet ContosoFirewallRule.</span><span class="sxs-lookup"><span data-stu-id="5321a-111">This command updates firewall rule named ContosoFirewallRule under workspace ContosoWorkspace with name ContosoFirewallRule.</span></span>

### <span data-ttu-id="5321a-112">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="5321a-112">Example 2</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Update-AzSynapseFirewallRule -Name ContosoFirewallRule -StartIpAddress "0.0.0.0" -EndIpAssdress "255.255.255.255"
```

<span data-ttu-id="5321a-113">Det här kommandot uppdaterar brand Väggs regeln med namnet ContosoFirewallRule under en arbets yta via pipeline.</span><span class="sxs-lookup"><span data-stu-id="5321a-113">This command updates firewall rule named ContosoFirewallRule under a workspace through pipeline.</span></span>

## <span data-ttu-id="5321a-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="5321a-114">PARAMETERS</span></span>

### <span data-ttu-id="5321a-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="5321a-115">-AsJob</span></span>
<span data-ttu-id="5321a-116">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="5321a-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="5321a-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5321a-117">-DefaultProfile</span></span>
<span data-ttu-id="5321a-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="5321a-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5321a-119">-EndIpAddress</span><span class="sxs-lookup"><span data-stu-id="5321a-119">-EndIpAddress</span></span>
<span data-ttu-id="5321a-120">Sista IP-adressen för brand Väggs regeln.</span><span class="sxs-lookup"><span data-stu-id="5321a-120">The end IP address of the firewall rule.</span></span>
<span data-ttu-id="5321a-121">Måste vara IPv4-format.</span><span class="sxs-lookup"><span data-stu-id="5321a-121">Must be IPv4 format.</span></span>
<span data-ttu-id="5321a-122">Måste vara större än eller lika med startIpAddress.</span><span class="sxs-lookup"><span data-stu-id="5321a-122">Must be greater than or equal to startIpAddress.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5321a-123">-Namn</span><span class="sxs-lookup"><span data-stu-id="5321a-123">-Name</span></span>
<span data-ttu-id="5321a-124">Firerwall regel namn för arbets ytan.</span><span class="sxs-lookup"><span data-stu-id="5321a-124">The firerwall rule name for the workspace.</span></span>

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

### <span data-ttu-id="5321a-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5321a-125">-ResourceGroupName</span></span>
<span data-ttu-id="5321a-126">Resurs grupps namn.</span><span class="sxs-lookup"><span data-stu-id="5321a-126">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateByNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5321a-127">-StartIpAddress</span><span class="sxs-lookup"><span data-stu-id="5321a-127">-StartIpAddress</span></span>
<span data-ttu-id="5321a-128">Start-IP-adressen för brand Väggs regeln.</span><span class="sxs-lookup"><span data-stu-id="5321a-128">The start IP address of the firewall rule.</span></span>
<span data-ttu-id="5321a-129">Måste vara IPv4-format.</span><span class="sxs-lookup"><span data-stu-id="5321a-129">Must be IPv4 format.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5321a-130">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="5321a-130">-WorkspaceName</span></span>
<span data-ttu-id="5321a-131">Namn på Synapse-arbetsyta.</span><span class="sxs-lookup"><span data-stu-id="5321a-131">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5321a-132">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="5321a-132">-WorkspaceObject</span></span>
<span data-ttu-id="5321a-133">objekt för arbets yta, vanligt vis passerar genom pipeline.</span><span class="sxs-lookup"><span data-stu-id="5321a-133">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: UpdateByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5321a-134">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="5321a-134">-Confirm</span></span>
<span data-ttu-id="5321a-135">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="5321a-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5321a-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5321a-136">-WhatIf</span></span>
<span data-ttu-id="5321a-137">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="5321a-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5321a-138">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="5321a-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5321a-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5321a-139">CommonParameters</span></span>
<span data-ttu-id="5321a-140">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5321a-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5321a-141">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="5321a-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5321a-142">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="5321a-142">INPUTS</span></span>

### <span data-ttu-id="5321a-143">Microsoft. Azure. commands. Synapse. Models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="5321a-143">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="5321a-144">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="5321a-144">OUTPUTS</span></span>

### <span data-ttu-id="5321a-145">Microsoft. Azure. commands. Synapse. Models. PSSynapseIpFirewallRule</span><span class="sxs-lookup"><span data-stu-id="5321a-145">Microsoft.Azure.Commands.Synapse.Models.PSSynapseIpFirewallRule</span></span>

## <span data-ttu-id="5321a-146">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="5321a-146">NOTES</span></span>

## <span data-ttu-id="5321a-147">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="5321a-147">RELATED LINKS</span></span>
