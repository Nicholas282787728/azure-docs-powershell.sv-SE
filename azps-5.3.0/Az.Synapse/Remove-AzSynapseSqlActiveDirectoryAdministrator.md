---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/remove-azsynapsesqlactivedirectoryadministrator
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseSqlActiveDirectoryAdministrator.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseSqlActiveDirectoryAdministrator.md
ms.openlocfilehash: 21d7169f18a999f84adbc568da18c90cb2aa2424
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98424152"
---
# <span data-ttu-id="1b544-101">Remove-AzSynapseSqlActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="1b544-101">Remove-AzSynapseSqlActiveDirectoryAdministrator</span></span>

## <span data-ttu-id="1b544-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="1b544-102">SYNOPSIS</span></span>
<span data-ttu-id="1b544-103">Tar bort en Azure AD-administratör för Synapse Analytics-arbetsyta.</span><span class="sxs-lookup"><span data-stu-id="1b544-103">Removes an Azure AD administrator for Synapse Analytics Workspace.</span></span>

## <span data-ttu-id="1b544-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="1b544-104">SYNTAX</span></span>

### <span data-ttu-id="1b544-105">RemoveByNameParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="1b544-105">RemoveByNameParameterSet (Default)</span></span>
```
Remove-AzSynapseSqlActiveDirectoryAdministrator [-ResourceGroupName <String>] -WorkspaceName <String>
 [-PassThru] [-AsJob] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="1b544-106">RemoveByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="1b544-106">RemoveByInputObjectParameterSet</span></span>
```
Remove-AzSynapseSqlActiveDirectoryAdministrator -InputObject <PSSynapseWorkspace> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1b544-107">RemoveByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="1b544-107">RemoveByResourceIdParameterSet</span></span>
```
Remove-AzSynapseSqlActiveDirectoryAdministrator -ResourceId <String> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1b544-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="1b544-108">DESCRIPTION</span></span>
<span data-ttu-id="1b544-109">Cmdleten **Remove-AzSynapseSqlActiveDirectoryAdministrator** tar bort en Azure Active Directory-administratör (Azure AD) för Azure Synapse Analytics-arbetsyta.</span><span class="sxs-lookup"><span data-stu-id="1b544-109">The **Remove-AzSynapseSqlActiveDirectoryAdministrator** cmdlet removes an Azure Active Directory (Azure AD) administrator for Azure Synapse Analytics Workspace.</span></span>

## <span data-ttu-id="1b544-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="1b544-110">EXAMPLES</span></span>

### <span data-ttu-id="1b544-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="1b544-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzSynapseSqlActiveDirectoryAdministrator -WorkspaceName ContosoWorkspace
```

<span data-ttu-id="1b544-112">Det här kommandot tar bort Azure AD-administratören för arbets ytan med namnet ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="1b544-112">This command removes the Azure AD administrator for the workspace named ContosoWorkspace.</span></span>

## <span data-ttu-id="1b544-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="1b544-113">PARAMETERS</span></span>

### <span data-ttu-id="1b544-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="1b544-114">-AsJob</span></span>
<span data-ttu-id="1b544-115">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="1b544-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="1b544-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1b544-116">-DefaultProfile</span></span>
<span data-ttu-id="1b544-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="1b544-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1b544-118">-Force</span><span class="sxs-lookup"><span data-stu-id="1b544-118">-Force</span></span>
<span data-ttu-id="1b544-119">Fråga inte efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="1b544-119">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="1b544-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1b544-120">-InputObject</span></span>
<span data-ttu-id="1b544-121">objekt för arbets yta, vanligt vis passerar genom pipeline.</span><span class="sxs-lookup"><span data-stu-id="1b544-121">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="1b544-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="1b544-122">-PassThru</span></span>
<span data-ttu-id="1b544-123">Denna cmdlet returnerar inte ett objekt som standard.</span><span class="sxs-lookup"><span data-stu-id="1b544-123">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="1b544-124">Om denna växel anges returnerar den sant om den är klar.</span><span class="sxs-lookup"><span data-stu-id="1b544-124">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="1b544-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1b544-125">-ResourceGroupName</span></span>
<span data-ttu-id="1b544-126">Resurs grupps namn.</span><span class="sxs-lookup"><span data-stu-id="1b544-126">Resource group name.</span></span>

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

### <span data-ttu-id="1b544-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="1b544-127">-ResourceId</span></span>
<span data-ttu-id="1b544-128">Resurs-ID för Synapse-arbetsyta.</span><span class="sxs-lookup"><span data-stu-id="1b544-128">Resource identifier of Synapse workspace.</span></span>

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

### <span data-ttu-id="1b544-129">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="1b544-129">-WorkspaceName</span></span>
<span data-ttu-id="1b544-130">Namn på Synapse-arbetsyta.</span><span class="sxs-lookup"><span data-stu-id="1b544-130">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="1b544-131">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="1b544-131">-Confirm</span></span>
<span data-ttu-id="1b544-132">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="1b544-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1b544-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1b544-133">-WhatIf</span></span>
<span data-ttu-id="1b544-134">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="1b544-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1b544-135">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="1b544-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1b544-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1b544-136">CommonParameters</span></span>
<span data-ttu-id="1b544-137">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1b544-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1b544-138">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="1b544-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1b544-139">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="1b544-139">INPUTS</span></span>

### <span data-ttu-id="1b544-140">Microsoft. Azure. commands. Synapse. Models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="1b544-140">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="1b544-141">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="1b544-141">OUTPUTS</span></span>

### <span data-ttu-id="1b544-142">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="1b544-142">System.Boolean</span></span>

## <span data-ttu-id="1b544-143">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="1b544-143">NOTES</span></span>

## <span data-ttu-id="1b544-144">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="1b544-144">RELATED LINKS</span></span>
