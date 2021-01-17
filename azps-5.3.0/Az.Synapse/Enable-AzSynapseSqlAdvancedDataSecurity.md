---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/enable-azsynapsesqladvanceddatasecurity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Enable-AzSynapseSqlAdvancedDataSecurity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Enable-AzSynapseSqlAdvancedDataSecurity.md
ms.openlocfilehash: dea0770af8cca14ebd523f67b69d7a12931183ec
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98424568"
---
# <span data-ttu-id="6bbd9-101">Enable-AzSynapseSqlAdvancedDataSecurity</span><span class="sxs-lookup"><span data-stu-id="6bbd9-101">Enable-AzSynapseSqlAdvancedDataSecurity</span></span>

## <span data-ttu-id="6bbd9-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="6bbd9-102">SYNOPSIS</span></span>
<span data-ttu-id="6bbd9-103">Aktiverar avancerad data säkerhet på en arbets yta.</span><span class="sxs-lookup"><span data-stu-id="6bbd9-103">Enables Advanced Data Security on a workspace.</span></span>

## <span data-ttu-id="6bbd9-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="6bbd9-104">SYNTAX</span></span>

### <span data-ttu-id="6bbd9-105">EnableByNameParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="6bbd9-105">EnableByNameParameterSet (Default)</span></span>
```
Enable-AzSynapseSqlAdvancedDataSecurity [-ResourceGroupName <String>] -WorkspaceName <String>
 [-DoNotConfigureVulnerabilityAssessment] [-DeploymentName <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6bbd9-106">EnableByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="6bbd9-106">EnableByInputObjectParameterSet</span></span>
```
Enable-AzSynapseSqlAdvancedDataSecurity -InputObject <PSSynapseWorkspace>
 [-DoNotConfigureVulnerabilityAssessment] [-DeploymentName <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6bbd9-107">EnableByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="6bbd9-107">EnableByResourceIdParameterSet</span></span>
```
Enable-AzSynapseSqlAdvancedDataSecurity -ResourceId <String> [-DoNotConfigureVulnerabilityAssessment]
 [-DeploymentName <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="6bbd9-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="6bbd9-108">DESCRIPTION</span></span>
<span data-ttu-id="6bbd9-109">Cmdleten **Enable-AzSynapseSqlAdvancedDataSecurity** aktiverar avancerad data säkerhet på en arbets yta.</span><span class="sxs-lookup"><span data-stu-id="6bbd9-109">The **Enable-AzSynapseSqlAdvancedDataSecurity** cmdlet enables Advanced Data Security on a workspace.</span></span> <span data-ttu-id="6bbd9-110">Avancerad data säkerhet är ett enhetligt säkerhets paket som innehåller data klassificering, sårbarhets utvärdering och Avancerat skydd för arbets ytan.</span><span class="sxs-lookup"><span data-stu-id="6bbd9-110">Advanced Data Security is a unified security package that includes Data Classification, Vulnerability Assessment and Advanced Threat Protection for your workspace.</span></span> <span data-ttu-id="6bbd9-111">(Ett nytt lagrings konto skapas automatiskt för att spara säkerhets utvärderingar.</span><span class="sxs-lookup"><span data-stu-id="6bbd9-111">(A new storage account will automatically be created for saving vulnerability assessments.</span></span> <span data-ttu-id="6bbd9-112">Om du har skapat ett lagrings konto för detta ändamål används det i stället.</span><span class="sxs-lookup"><span data-stu-id="6bbd9-112">If a storage account was previously created for this purpose, it will be used instead)</span></span>

## <span data-ttu-id="6bbd9-113">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="6bbd9-113">EXAMPLES</span></span>

### <span data-ttu-id="6bbd9-114">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="6bbd9-114">Example 1</span></span>
```powershell
PS C:\> Enable-AzSynapseSqlAdvancedDataSecurity -WorkspaceName ContosoWorkspace
```

<span data-ttu-id="6bbd9-115">Det här kommandot aktiverar avancerad data säkerhet för arbets ytan.</span><span class="sxs-lookup"><span data-stu-id="6bbd9-115">This command enables workspace Advanced Data Security.</span></span>

### <span data-ttu-id="6bbd9-116">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="6bbd9-116">Example 2</span></span>
```powershell
PS C:\> Get-AzSynapseWorkspace -Name ContosoWorkspace | Enable-AzSynapseSqlAdvancedDataSecurity
```

<span data-ttu-id="6bbd9-117">Det här kommandot möjliggör avancerad data säkerhet för arbets ytan.</span><span class="sxs-lookup"><span data-stu-id="6bbd9-117">This command enables workspace Advanced Data Security through pipeline.</span></span>

### <span data-ttu-id="6bbd9-118">Exempel 3</span><span class="sxs-lookup"><span data-stu-id="6bbd9-118">Example 3</span></span>
```powershell
PS C:\> Enable-AzSynapseSqlAdvancedDataSecurity -WorkspaceName ContosoWorkspace -DoNotConfigureVulnerabilityAssessment
```

<span data-ttu-id="6bbd9-119">Det här kommandot aktiverar avancerad data säkerhet via arbets yta och aktiverar inte automatisk säkerhets problem.</span><span class="sxs-lookup"><span data-stu-id="6bbd9-119">This command enables workspace Advanced Data Security through pipeline and does not auto enable Vulnerability Assessment.</span></span>

## <span data-ttu-id="6bbd9-120">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="6bbd9-120">PARAMETERS</span></span>

### <span data-ttu-id="6bbd9-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="6bbd9-121">-AsJob</span></span>
<span data-ttu-id="6bbd9-122">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="6bbd9-122">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="6bbd9-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6bbd9-123">-DefaultProfile</span></span>
<span data-ttu-id="6bbd9-124">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="6bbd9-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6bbd9-125">-DeploymentName</span><span class="sxs-lookup"><span data-stu-id="6bbd9-125">-DeploymentName</span></span>
<span data-ttu-id="6bbd9-126">Ange ett namn för avancerad data säkerhets distribution.</span><span class="sxs-lookup"><span data-stu-id="6bbd9-126">Supply a custom name for Advanced Data Security deployment.</span></span>

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

### <span data-ttu-id="6bbd9-127">-DoNotConfigureVulnerabilityAssessment</span><span class="sxs-lookup"><span data-stu-id="6bbd9-127">-DoNotConfigureVulnerabilityAssessment</span></span>
<span data-ttu-id="6bbd9-128">Tillåt inte automatisk sårbarhets utvärdering (Detta skapar inte ett lagrings konto).</span><span class="sxs-lookup"><span data-stu-id="6bbd9-128">Do not auto enable Vulnerability Assessment (This will not create a storage account).</span></span>

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

### <span data-ttu-id="6bbd9-129">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6bbd9-129">-InputObject</span></span>
<span data-ttu-id="6bbd9-130">objekt för arbets yta, vanligt vis passerar genom pipeline.</span><span class="sxs-lookup"><span data-stu-id="6bbd9-130">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: EnableByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6bbd9-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6bbd9-131">-ResourceGroupName</span></span>
<span data-ttu-id="6bbd9-132">Resurs grupps namn.</span><span class="sxs-lookup"><span data-stu-id="6bbd9-132">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: EnableByNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6bbd9-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="6bbd9-133">-ResourceId</span></span>
<span data-ttu-id="6bbd9-134">Resurs-ID för Synapse-arbetsyta.</span><span class="sxs-lookup"><span data-stu-id="6bbd9-134">Resource identifier of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: EnableByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6bbd9-135">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="6bbd9-135">-WorkspaceName</span></span>
<span data-ttu-id="6bbd9-136">Namn på Synapse-arbetsyta.</span><span class="sxs-lookup"><span data-stu-id="6bbd9-136">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: EnableByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6bbd9-137">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="6bbd9-137">-Confirm</span></span>
<span data-ttu-id="6bbd9-138">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="6bbd9-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6bbd9-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6bbd9-139">-WhatIf</span></span>
<span data-ttu-id="6bbd9-140">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="6bbd9-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6bbd9-141">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="6bbd9-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6bbd9-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6bbd9-142">CommonParameters</span></span>
<span data-ttu-id="6bbd9-143">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6bbd9-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6bbd9-144">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="6bbd9-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6bbd9-145">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="6bbd9-145">INPUTS</span></span>

### <span data-ttu-id="6bbd9-146">Microsoft. Azure. commands. Synapse. Models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="6bbd9-146">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="6bbd9-147">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="6bbd9-147">OUTPUTS</span></span>

### <span data-ttu-id="6bbd9-148">Microsoft. Azure. commands. Synapse. Models. WorkspaceAdvancedDataSecurityPolicy</span><span class="sxs-lookup"><span data-stu-id="6bbd9-148">Microsoft.Azure.Commands.Synapse.Models.WorkspaceAdvancedDataSecurityPolicy</span></span>

## <span data-ttu-id="6bbd9-149">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="6bbd9-149">NOTES</span></span>

## <span data-ttu-id="6bbd9-150">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="6bbd9-150">RELATED LINKS</span></span>
