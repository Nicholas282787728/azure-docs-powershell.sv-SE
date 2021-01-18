---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/set-azsynapsesqlpooltransparentdataencryption
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Set-AzSynapseSqlPoolTransparentDataEncryption.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Set-AzSynapseSqlPoolTransparentDataEncryption.md
ms.openlocfilehash: 5a8dbd1f21d640d5d1cb38fa403ee05dec9cfc20
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98523902"
---
# <span data-ttu-id="4599f-101">Set-AzSynapseSqlPoolTransparentDataEncryption</span><span class="sxs-lookup"><span data-stu-id="4599f-101">Set-AzSynapseSqlPoolTransparentDataEncryption</span></span>

## <span data-ttu-id="4599f-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="4599f-102">SYNOPSIS</span></span>
<span data-ttu-id="4599f-103">Ändrar egenskapen TDE för en SQL-pool.</span><span class="sxs-lookup"><span data-stu-id="4599f-103">Modifies TDE property for a SQL pool.</span></span>

## <span data-ttu-id="4599f-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="4599f-104">SYNTAX</span></span>

### <span data-ttu-id="4599f-105">SetByNameParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="4599f-105">SetByNameParameterSet (Default)</span></span>
```
Set-AzSynapseSqlPoolTransparentDataEncryption [-ResourceGroupName <String>] -WorkspaceName <String>
 -Name <String> -State <TransparentDataEncryptionStateType> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4599f-106">SetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="4599f-106">SetByParentObjectParameterSet</span></span>
```
Set-AzSynapseSqlPoolTransparentDataEncryption -Name <String> -WorkspaceObject <PSSynapseWorkspace>
 -State <TransparentDataEncryptionStateType> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4599f-107">SetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="4599f-107">SetByInputObjectParameterSet</span></span>
```
Set-AzSynapseSqlPoolTransparentDataEncryption -InputObject <PSSynapseSqlPool>
 -State <TransparentDataEncryptionStateType> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4599f-108">SetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="4599f-108">SetByResourceIdParameterSet</span></span>
```
Set-AzSynapseSqlPoolTransparentDataEncryption -ResourceId <String> -State <TransparentDataEncryptionStateType>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4599f-109">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="4599f-109">DESCRIPTION</span></span>
<span data-ttu-id="4599f-110">Cmdleten **set-AzSynapseSqlPoolTransparentDataEncryption** ändrar egenskapen transparent Data Encryption (TDE) för en Azure SYNAPSE Analytics SQL-pool.</span><span class="sxs-lookup"><span data-stu-id="4599f-110">The **Set-AzSynapseSqlPoolTransparentDataEncryption** cmdlet modifies the Transparent Data Encryption (TDE) property of an Azure Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="4599f-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="4599f-111">EXAMPLES</span></span>

### <span data-ttu-id="4599f-112">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="4599f-112">Example 1</span></span>
```powershell
PS C:\> Set-AzSynapseSqlPoolTransparentDataEncryption -WorkspaceName ContosoWorkspace -Name ContosoSqlPool -State Enabled
```

<span data-ttu-id="4599f-113">Det här kommandot aktiverar TDE för SQL-poolen med namnet ContosoSqlPool under arbets ytan med namnet ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="4599f-113">This command enables TDE for the SQL pool named ContosoSqlPool under the workspace named ContosoWorkspace.</span></span>

## <span data-ttu-id="4599f-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="4599f-114">PARAMETERS</span></span>

### <span data-ttu-id="4599f-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="4599f-115">-AsJob</span></span>
<span data-ttu-id="4599f-116">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="4599f-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="4599f-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4599f-117">-DefaultProfile</span></span>
<span data-ttu-id="4599f-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="4599f-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4599f-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4599f-119">-InputObject</span></span>
<span data-ttu-id="4599f-120">Objekt i SQL-pool, vanligt vis passerar genom pipeline.</span><span class="sxs-lookup"><span data-stu-id="4599f-120">SQL pool input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool
Parameter Sets: SetByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4599f-121">-Namn</span><span class="sxs-lookup"><span data-stu-id="4599f-121">-Name</span></span>
<span data-ttu-id="4599f-122">Namn på SQL-poolen Synapse.</span><span class="sxs-lookup"><span data-stu-id="4599f-122">Name of Synapse SQL pool.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByNameParameterSet, SetByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4599f-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4599f-123">-ResourceGroupName</span></span>
<span data-ttu-id="4599f-124">Resurs grupps namn.</span><span class="sxs-lookup"><span data-stu-id="4599f-124">Resource group name.</span></span>

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

### <span data-ttu-id="4599f-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="4599f-125">-ResourceId</span></span>
<span data-ttu-id="4599f-126">Resurs-ID för Synapse SQL-pool.</span><span class="sxs-lookup"><span data-stu-id="4599f-126">Resource identifier of Synapse SQL Pool.</span></span>

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

### <span data-ttu-id="4599f-127">-State</span><span class="sxs-lookup"><span data-stu-id="4599f-127">-State</span></span>
<span data-ttu-id="4599f-128">Läget för att öppna SQL-poolen för Azure Synapse.</span><span class="sxs-lookup"><span data-stu-id="4599f-128">The Azure Synapse Analytics Sql Pool Transparent Data Encryption state.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.TransparentDataEncryptionStateType
Parameter Sets: (All)
Aliases:
Accepted values: Enabled, Disabled

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4599f-129">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="4599f-129">-WorkspaceName</span></span>
<span data-ttu-id="4599f-130">Namn på Synapse-arbetsyta.</span><span class="sxs-lookup"><span data-stu-id="4599f-130">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4599f-131">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="4599f-131">-WorkspaceObject</span></span>
<span data-ttu-id="4599f-132">objekt för arbets yta, vanligt vis passerar genom pipeline.</span><span class="sxs-lookup"><span data-stu-id="4599f-132">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: SetByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4599f-133">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="4599f-133">-Confirm</span></span>
<span data-ttu-id="4599f-134">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="4599f-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4599f-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4599f-135">-WhatIf</span></span>
<span data-ttu-id="4599f-136">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="4599f-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4599f-137">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="4599f-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4599f-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4599f-138">CommonParameters</span></span>
<span data-ttu-id="4599f-139">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4599f-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4599f-140">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="4599f-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4599f-141">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="4599f-141">INPUTS</span></span>

### <span data-ttu-id="4599f-142">Microsoft. Azure. commands. Synapse. Models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="4599f-142">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="4599f-143">Microsoft. Azure. commands. Synapse. Models. PSSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="4599f-143">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span></span>

## <span data-ttu-id="4599f-144">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="4599f-144">OUTPUTS</span></span>

### <span data-ttu-id="4599f-145">Microsoft. Azure. commands. Synapse. Models. PSTransparentDataEncryption</span><span class="sxs-lookup"><span data-stu-id="4599f-145">Microsoft.Azure.Commands.Synapse.Models.PSTransparentDataEncryption</span></span>

## <span data-ttu-id="4599f-146">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="4599f-146">NOTES</span></span>

## <span data-ttu-id="4599f-147">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="4599f-147">RELATED LINKS</span></span>
