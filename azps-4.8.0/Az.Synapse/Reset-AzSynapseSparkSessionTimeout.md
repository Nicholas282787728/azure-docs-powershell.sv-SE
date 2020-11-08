---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/reset-azsynapsesparksessiontimeout
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Reset-AzSynapseSparkSessionTimeout.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Reset-AzSynapseSparkSessionTimeout.md
ms.openlocfilehash: cccc0d3cffd9eb313e2983d81a3492bdf89e9e44
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94261188"
---
# <span data-ttu-id="36b45-101">Reset-AzSynapseSparkSessionTimeout</span><span class="sxs-lookup"><span data-stu-id="36b45-101">Reset-AzSynapseSparkSessionTimeout</span></span>

## <span data-ttu-id="36b45-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="36b45-102">SYNOPSIS</span></span>
<span data-ttu-id="36b45-103">Återställer timeout för en Synapse Analytics Spark-session.</span><span class="sxs-lookup"><span data-stu-id="36b45-103">Resets timeout of a Synapse Analytics Spark session.</span></span>

## <span data-ttu-id="36b45-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="36b45-104">SYNTAX</span></span>

### <span data-ttu-id="36b45-105">ResetByNameParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="36b45-105">ResetByNameParameterSet (Default)</span></span>
```
Reset-AzSynapseSparkSessionTimeout -WorkspaceName <String> -SparkPoolName <String> -LivyId <Int32> [-PassThru]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="36b45-106">ResetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="36b45-106">ResetByParentObjectParameterSet</span></span>
```
Reset-AzSynapseSparkSessionTimeout -LivyId <Int32> -SparkPoolObject <PSSynapseSparkPool> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="36b45-107">ResetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="36b45-107">ResetByInputObjectParameterSet</span></span>
```
Reset-AzSynapseSparkSessionTimeout -InputObject <PSSynapseSparkSession> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="36b45-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="36b45-108">DESCRIPTION</span></span>
<span data-ttu-id="36b45-109">Cmdleten **Remove-AzSynapseSparkSessionTimeout** återställer timeout för en Synapse Analytics Spark-session.</span><span class="sxs-lookup"><span data-stu-id="36b45-109">The **Remove-AzSynapseSparkSessionTimeout** cmdlet resets timeout of a Synapse Analytics Spark session.</span></span>

## <span data-ttu-id="36b45-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="36b45-110">EXAMPLES</span></span>

### <span data-ttu-id="36b45-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="36b45-111">Example 1</span></span>
```powershell
PS C:\> Reset-AzSynapseSparkSessionTimeout -WorkspaceName ContosoWorkspace -SparkPoolName ContosoSparkPool -LivyId 125
```

<span data-ttu-id="36b45-112">Det här kommandot återställer timeout för Synapse Analytics Spark-session med angivet livy-ID.</span><span class="sxs-lookup"><span data-stu-id="36b45-112">This command resets timeout of the Synapse Analytics Spark session with the specified livy ID.</span></span>

### <span data-ttu-id="36b45-113">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="36b45-113">Example 2</span></span>
```powershell
PS C:\> $pool = Get-AzSynapseSparkPool -WorkspaceName ContosoWorkspace -SparkPoolName ContosoSparkPool
PS C:\> $pool | Reset-AzSynapseSparkSessionTimeout -LivyId 125
```

<span data-ttu-id="36b45-114">Det här kommandot återställer timeout för Synapse Analytics Spark-session med angivet livy-ID genom pipeline.</span><span class="sxs-lookup"><span data-stu-id="36b45-114">This command resets timeout of the Synapse Analytics Spark session with the specified livy ID through pipeline.</span></span>

### <span data-ttu-id="36b45-115">Exempel 3</span><span class="sxs-lookup"><span data-stu-id="36b45-115">Example 3</span></span>
```powershell
PS C:\> $session = Get-AzSynapseSparkSession -WorkspaceName ContosoWorkspace -SparkPoolName ContosoSparkPool -LivyId 125
PS C:\> $session | Reset-AzSynapseSparkSessionTimeout
```

<span data-ttu-id="36b45-116">Det här kommandot återställer timeout för Synapse Analytics Spark-session med angivet livy-ID genom pipeline.</span><span class="sxs-lookup"><span data-stu-id="36b45-116">This command resets timeout of the Synapse Analytics Spark session with the specified livy ID through pipeline.</span></span>

## <span data-ttu-id="36b45-117">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="36b45-117">PARAMETERS</span></span>

### <span data-ttu-id="36b45-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="36b45-118">-AsJob</span></span>
<span data-ttu-id="36b45-119">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="36b45-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="36b45-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="36b45-120">-DefaultProfile</span></span>
<span data-ttu-id="36b45-121">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="36b45-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="36b45-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="36b45-122">-InputObject</span></span>
<span data-ttu-id="36b45-123">Spark session-objekt som normalt passerar genom pipeline.</span><span class="sxs-lookup"><span data-stu-id="36b45-123">Spark session input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkSession
Parameter Sets: ResetByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="36b45-124">-LivyId</span><span class="sxs-lookup"><span data-stu-id="36b45-124">-LivyId</span></span>
<span data-ttu-id="36b45-125">Identifierare för Spark-session.</span><span class="sxs-lookup"><span data-stu-id="36b45-125">Identifier of Spark session.</span></span>

```yaml
Type: System.Int32
Parameter Sets: ResetByNameParameterSet, ResetByParentObjectParameterSet
Aliases: Id

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="36b45-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="36b45-126">-PassThru</span></span>
<span data-ttu-id="36b45-127">Denna cmdlet returnerar inte ett objekt som standard.</span><span class="sxs-lookup"><span data-stu-id="36b45-127">This Cmdlet does not return an object by default.</span></span> <span data-ttu-id="36b45-128">Om denna växel anges returnerar den sant om den är klar.</span><span class="sxs-lookup"><span data-stu-id="36b45-128">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="36b45-129">-SparkPoolName</span><span class="sxs-lookup"><span data-stu-id="36b45-129">-SparkPoolName</span></span>
<span data-ttu-id="36b45-130">Namn på Synapse Spark-pool.</span><span class="sxs-lookup"><span data-stu-id="36b45-130">Name of Synapse Spark pool.</span></span>

```yaml
Type: System.String
Parameter Sets: ResetByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="36b45-131">-SparkPoolObject</span><span class="sxs-lookup"><span data-stu-id="36b45-131">-SparkPoolObject</span></span>
<span data-ttu-id="36b45-132">Indata från Spark-pool, vanligt vis passerar genom pipeline.</span><span class="sxs-lookup"><span data-stu-id="36b45-132">Spark pool input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkPool
Parameter Sets: ResetByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="36b45-133">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="36b45-133">-WorkspaceName</span></span>
<span data-ttu-id="36b45-134">Namn på Synapse-arbetsyta.</span><span class="sxs-lookup"><span data-stu-id="36b45-134">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: ResetByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="36b45-135">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="36b45-135">-Confirm</span></span>
<span data-ttu-id="36b45-136">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="36b45-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="36b45-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="36b45-137">-WhatIf</span></span>
<span data-ttu-id="36b45-138">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="36b45-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="36b45-139">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="36b45-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="36b45-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="36b45-140">CommonParameters</span></span>
<span data-ttu-id="36b45-141">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="36b45-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="36b45-142">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="36b45-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="36b45-143">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="36b45-143">INPUTS</span></span>

### <span data-ttu-id="36b45-144">Microsoft. Azure. commands. Synapse. Models. PSSynapseSparkPool</span><span class="sxs-lookup"><span data-stu-id="36b45-144">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkPool</span></span>

### <span data-ttu-id="36b45-145">Microsoft. Azure. commands. Synapse. Models. PSSynapseSparkSession</span><span class="sxs-lookup"><span data-stu-id="36b45-145">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkSession</span></span>

## <span data-ttu-id="36b45-146">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="36b45-146">OUTPUTS</span></span>

### <span data-ttu-id="36b45-147">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="36b45-147">System.Boolean</span></span>

## <span data-ttu-id="36b45-148">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="36b45-148">NOTES</span></span>

## <span data-ttu-id="36b45-149">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="36b45-149">RELATED LINKS</span></span>
