---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/new-azsynapsefirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/New-AzSynapseFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/New-AzSynapseFirewallRule.md
ms.openlocfilehash: b4579d01ed6dd5a7d742cbb82afb424151579772
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94324149"
---
# <span data-ttu-id="beb80-101">New-AzSynapseFirewallRule</span><span class="sxs-lookup"><span data-stu-id="beb80-101">New-AzSynapseFirewallRule</span></span>

## <span data-ttu-id="beb80-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="beb80-102">SYNOPSIS</span></span>
<span data-ttu-id="beb80-103">Skapar en Synapse för analys brand vägg.</span><span class="sxs-lookup"><span data-stu-id="beb80-103">Creates a Synapse Analytics Firewall Rule.</span></span>

## <span data-ttu-id="beb80-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="beb80-104">SYNTAX</span></span>

### <span data-ttu-id="beb80-105">CreateByNameParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="beb80-105">CreateByNameParameterSet (Default)</span></span>
```
New-AzSynapseFirewallRule [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String>
 -StartIpAddress <String> -EndIpAddress <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="beb80-106">CreateByNameAllowAllIpParameterSet</span><span class="sxs-lookup"><span data-stu-id="beb80-106">CreateByNameAllowAllIpParameterSet</span></span>
```
New-AzSynapseFirewallRule [-ResourceGroupName <String>] -WorkspaceName <String> [-AllowAllAzureIP] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="beb80-107">CreateByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="beb80-107">CreateByParentObjectParameterSet</span></span>
```
New-AzSynapseFirewallRule -WorkspaceObject <PSSynapseWorkspace> -Name <String> -StartIpAddress <String>
 -EndIpAddress <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="beb80-108">CreateByParentObjectAllowAllIpParameterSet</span><span class="sxs-lookup"><span data-stu-id="beb80-108">CreateByParentObjectAllowAllIpParameterSet</span></span>
```
New-AzSynapseFirewallRule -WorkspaceObject <PSSynapseWorkspace> [-AllowAllAzureIP] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="beb80-109">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="beb80-109">DESCRIPTION</span></span>
<span data-ttu-id="beb80-110">Cmdleten **New-AzSynapseFirewallRule** skapar en Azure Synapse Analytics-brandväggsregel.</span><span class="sxs-lookup"><span data-stu-id="beb80-110">The **New-AzSynapseFirewallRule** cmdlet creates an Azure Synapse Analytics Firewall Rule.</span></span>

## <span data-ttu-id="beb80-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="beb80-111">EXAMPLES</span></span>

### <span data-ttu-id="beb80-112">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="beb80-112">Example 1</span></span>
```powershell
PS C:\> New-AzSynapseFirewallRule -WorkspaceName ContosoWorkspace -Name ContosoFirewallRule -StartIpAddress "0.0.0.0" -EndIpAddress "255.255.255.255"
```

<span data-ttu-id="beb80-113">Det här kommandot skapar en brand Väggs regel med namnet ContosoFirewallRule under arbets ytan ContosoWorkspace med namnet ContosoFirewallRule.</span><span class="sxs-lookup"><span data-stu-id="beb80-113">This command creates firewall rule named ContosoFirewallRule under workspace ContosoWorkspace with name ContosoFirewallRule.</span></span>

### <span data-ttu-id="beb80-114">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="beb80-114">Example 2</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | New-AzSynapseFirewallRule -Name ContosoFirewallRule -StartIpAddress "0.0.0.0" -EndIpAddress "255.255.255.255"
```

<span data-ttu-id="beb80-115">Det här kommandot skapar en brand Väggs regel med namnet ContosoFirewallRule under en arbets yta via pipeline.</span><span class="sxs-lookup"><span data-stu-id="beb80-115">This command creates firewall rule named ContosoFirewallRule under a workspace through pipeline.</span></span>

### <span data-ttu-id="beb80-116">Exempel 3</span><span class="sxs-lookup"><span data-stu-id="beb80-116">Example 3</span></span>
```powershell
PS C:\> New-AzSynapseFirewallRule -WorkspaceName ContosoWorkspace -AllowAllAzureIP
```

<span data-ttu-id="beb80-117">Det här kommandot skapar en brand Väggs regel som tillåter alla Azure IP-adresser under en arbets yta.</span><span class="sxs-lookup"><span data-stu-id="beb80-117">This command creates firewall rule that allow all azure ips under a workspace.</span></span>

## <span data-ttu-id="beb80-118">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="beb80-118">PARAMETERS</span></span>

### <span data-ttu-id="beb80-119">-AllowAllAzureIP</span><span class="sxs-lookup"><span data-stu-id="beb80-119">-AllowAllAzureIP</span></span>
<span data-ttu-id="beb80-120">Skapar en brand Väggs regel som gör att alla Azure IP-adresser får åtkomst.</span><span class="sxs-lookup"><span data-stu-id="beb80-120">Creates a special firewall rule that permits all Azure IPs to have access.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: CreateByNameAllowAllIpParameterSet, CreateByParentObjectAllowAllIpParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="beb80-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="beb80-121">-AsJob</span></span>
<span data-ttu-id="beb80-122">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="beb80-122">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="beb80-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="beb80-123">-DefaultProfile</span></span>
<span data-ttu-id="beb80-124">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="beb80-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="beb80-125">-EndIpAddress</span><span class="sxs-lookup"><span data-stu-id="beb80-125">-EndIpAddress</span></span>
<span data-ttu-id="beb80-126">Sista IP-adressen för brand Väggs regeln.</span><span class="sxs-lookup"><span data-stu-id="beb80-126">The end IP address of the firewall rule.</span></span>
<span data-ttu-id="beb80-127">Måste vara IPv4-format.</span><span class="sxs-lookup"><span data-stu-id="beb80-127">Must be IPv4 format.</span></span>
<span data-ttu-id="beb80-128">Måste vara större än eller lika med startIpAddress.</span><span class="sxs-lookup"><span data-stu-id="beb80-128">Must be greater than or equal to startIpAddress.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateByNameParameterSet, CreateByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="beb80-129">-Namn</span><span class="sxs-lookup"><span data-stu-id="beb80-129">-Name</span></span>
<span data-ttu-id="beb80-130">Firerwall regel namn för arbets ytan.</span><span class="sxs-lookup"><span data-stu-id="beb80-130">The firerwall rule name for the workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateByNameParameterSet, CreateByParentObjectParameterSet
Aliases: FirewallRuleName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="beb80-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="beb80-131">-ResourceGroupName</span></span>
<span data-ttu-id="beb80-132">Resurs grupps namn.</span><span class="sxs-lookup"><span data-stu-id="beb80-132">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateByNameParameterSet, CreateByNameAllowAllIpParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="beb80-133">-StartIpAddress</span><span class="sxs-lookup"><span data-stu-id="beb80-133">-StartIpAddress</span></span>
<span data-ttu-id="beb80-134">Start-IP-adressen för brand Väggs regeln.</span><span class="sxs-lookup"><span data-stu-id="beb80-134">The start IP address of the firewall rule.</span></span>
<span data-ttu-id="beb80-135">Måste vara IPv4-format.</span><span class="sxs-lookup"><span data-stu-id="beb80-135">Must be IPv4 format.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateByNameParameterSet, CreateByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="beb80-136">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="beb80-136">-WorkspaceName</span></span>
<span data-ttu-id="beb80-137">Namn på Synapse-arbetsyta.</span><span class="sxs-lookup"><span data-stu-id="beb80-137">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateByNameParameterSet, CreateByNameAllowAllIpParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="beb80-138">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="beb80-138">-WorkspaceObject</span></span>
<span data-ttu-id="beb80-139">objekt för arbets yta, vanligt vis passerar genom pipeline.</span><span class="sxs-lookup"><span data-stu-id="beb80-139">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: CreateByParentObjectParameterSet, CreateByParentObjectAllowAllIpParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="beb80-140">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="beb80-140">-Confirm</span></span>
<span data-ttu-id="beb80-141">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="beb80-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="beb80-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="beb80-142">-WhatIf</span></span>
<span data-ttu-id="beb80-143">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="beb80-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="beb80-144">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="beb80-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="beb80-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="beb80-145">CommonParameters</span></span>
<span data-ttu-id="beb80-146">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="beb80-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="beb80-147">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="beb80-147">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="beb80-148">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="beb80-148">INPUTS</span></span>

### <span data-ttu-id="beb80-149">Microsoft. Azure. commands. Synapse. Models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="beb80-149">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="beb80-150">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="beb80-150">OUTPUTS</span></span>

### <span data-ttu-id="beb80-151">Microsoft. Azure. commands. Synapse. Models. PSSynapseIpFirewallRule</span><span class="sxs-lookup"><span data-stu-id="beb80-151">Microsoft.Azure.Commands.Synapse.Models.PSSynapseIpFirewallRule</span></span>

## <span data-ttu-id="beb80-152">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="beb80-152">NOTES</span></span>

## <span data-ttu-id="beb80-153">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="beb80-153">RELATED LINKS</span></span>
