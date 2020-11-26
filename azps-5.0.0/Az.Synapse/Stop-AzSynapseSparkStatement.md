---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/stop-azsynapsesparkstatement
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Stop-AzSynapseSparkStatement.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Stop-AzSynapseSparkStatement.md
ms.openlocfilehash: 84d3f73735c3606813d769d9b0daf0f9716fc1a3
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94272512"
---
# <span data-ttu-id="d6dfc-101">Stop-AzSynapseSparkStatement</span><span class="sxs-lookup"><span data-stu-id="d6dfc-101">Stop-AzSynapseSparkStatement</span></span>

## <span data-ttu-id="d6dfc-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="d6dfc-102">SYNOPSIS</span></span>
<span data-ttu-id="d6dfc-103">Avbryter en Synapse Analytics Spark-programsats.</span><span class="sxs-lookup"><span data-stu-id="d6dfc-103">Cancels a Synapse Analytics Spark statement.</span></span>

## <span data-ttu-id="d6dfc-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="d6dfc-104">SYNTAX</span></span>

### <span data-ttu-id="d6dfc-105">StopSparkStatementByIdParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="d6dfc-105">StopSparkStatementByIdParameterSet (Default)</span></span>
```
Stop-AzSynapseSparkStatement -WorkspaceName <String> -SparkPoolName <String> -LivyId <Int32> -SessionId <Int32>
 [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d6dfc-106">StopSparkStatementByIdFromParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="d6dfc-106">StopSparkStatementByIdFromParentObjectParameterSet</span></span>
```
Stop-AzSynapseSparkStatement -SessionObject <PSSynapseSparkSession> -LivyId <Int32> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d6dfc-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="d6dfc-107">DESCRIPTION</span></span>
<span data-ttu-id="d6dfc-108">Cmdleten **Stop-AzSynapseSparkStatement** avbryter ett Synapse Analytics Spark-uttryck.</span><span class="sxs-lookup"><span data-stu-id="d6dfc-108">The **Stop-AzSynapseSparkStatement** cmdlet cancels a Synapse Analytics Spark statement.</span></span>

## <span data-ttu-id="d6dfc-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="d6dfc-109">EXAMPLES</span></span>

### <span data-ttu-id="d6dfc-110">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="d6dfc-110">Example 1</span></span>
```powershell
PS C:\> Stop-AzSynapseStatement -WorkspaceName ContosoWorkspace -SparkPoolName ContosoSparkPool -SessionId 130 -LivyId 1
```

<span data-ttu-id="d6dfc-111">Det här kommandot avbryter Spark-instruktionen med angivet livy-ID.</span><span class="sxs-lookup"><span data-stu-id="d6dfc-111">This command cancels the Spark statement with the specified livy ID.</span></span>

### <span data-ttu-id="d6dfc-112">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="d6dfc-112">Example 2</span></span>
```powershell
PS C:\> $session = Get-AzSynapseSparkSession -WorkspaceName ContosoWorkspace -SparkPoolName ContosoSparkPool -LivyId 130
PS C:\> $session | Stop-AzSynapseStatement -LivyId 3
```

<span data-ttu-id="d6dfc-113">Det här kommandot avbryter Spark-satsen med angivet livy-ID via pipeline.</span><span class="sxs-lookup"><span data-stu-id="d6dfc-113">This command cancels the Spark statement with the specified livy ID through pipeline.</span></span>

## <span data-ttu-id="d6dfc-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="d6dfc-114">PARAMETERS</span></span>

### <span data-ttu-id="d6dfc-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d6dfc-115">-DefaultProfile</span></span>
<span data-ttu-id="d6dfc-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="d6dfc-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d6dfc-117">-Force</span><span class="sxs-lookup"><span data-stu-id="d6dfc-117">-Force</span></span>
<span data-ttu-id="d6dfc-118">Fråga inte efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="d6dfc-118">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="d6dfc-119">-LivyId</span><span class="sxs-lookup"><span data-stu-id="d6dfc-119">-LivyId</span></span>
<span data-ttu-id="d6dfc-120">Identifierare för Spark-instruktionen.</span><span class="sxs-lookup"><span data-stu-id="d6dfc-120">Identifier of Spark statement.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: Id

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d6dfc-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d6dfc-121">-PassThru</span></span>
<span data-ttu-id="d6dfc-122">Denna cmdlet returnerar inte ett objekt som standard.</span><span class="sxs-lookup"><span data-stu-id="d6dfc-122">This Cmdlet does not return an object by default.</span></span> <span data-ttu-id="d6dfc-123">Om denna växel anges returnerar den sant om den är klar.</span><span class="sxs-lookup"><span data-stu-id="d6dfc-123">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="d6dfc-124">-SessionId</span><span class="sxs-lookup"><span data-stu-id="d6dfc-124">-SessionId</span></span>
<span data-ttu-id="d6dfc-125">Identifierare för Spark-session.</span><span class="sxs-lookup"><span data-stu-id="d6dfc-125">Identifier of Spark session.</span></span>

```yaml
Type: System.Int32
Parameter Sets: StopSparkStatementByIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d6dfc-126">-SessionObject</span><span class="sxs-lookup"><span data-stu-id="d6dfc-126">-SessionObject</span></span>
<span data-ttu-id="d6dfc-127">Spark session-objekt som normalt passerar genom pipeline.</span><span class="sxs-lookup"><span data-stu-id="d6dfc-127">Spark session input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkSession
Parameter Sets: StopSparkStatementByIdFromParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d6dfc-128">-SparkPoolName</span><span class="sxs-lookup"><span data-stu-id="d6dfc-128">-SparkPoolName</span></span>
<span data-ttu-id="d6dfc-129">Namn på Synapse Spark-pool.</span><span class="sxs-lookup"><span data-stu-id="d6dfc-129">Name of Synapse Spark pool.</span></span>

```yaml
Type: System.String
Parameter Sets: StopSparkStatementByIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d6dfc-130">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="d6dfc-130">-WorkspaceName</span></span>
<span data-ttu-id="d6dfc-131">Namn på Synapse-arbetsyta.</span><span class="sxs-lookup"><span data-stu-id="d6dfc-131">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: StopSparkStatementByIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d6dfc-132">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="d6dfc-132">-Confirm</span></span>
<span data-ttu-id="d6dfc-133">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="d6dfc-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d6dfc-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d6dfc-134">-WhatIf</span></span>
<span data-ttu-id="d6dfc-135">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="d6dfc-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d6dfc-136">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="d6dfc-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d6dfc-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d6dfc-137">CommonParameters</span></span>
<span data-ttu-id="d6dfc-138">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d6dfc-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d6dfc-139">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d6dfc-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d6dfc-140">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="d6dfc-140">INPUTS</span></span>

### <span data-ttu-id="d6dfc-141">Microsoft. Azure. commands. Synapse. Models. PSSynapseSparkSession</span><span class="sxs-lookup"><span data-stu-id="d6dfc-141">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkSession</span></span>

## <span data-ttu-id="d6dfc-142">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="d6dfc-142">OUTPUTS</span></span>

### <span data-ttu-id="d6dfc-143">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="d6dfc-143">System.Boolean</span></span>

## <span data-ttu-id="d6dfc-144">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="d6dfc-144">NOTES</span></span>

## <span data-ttu-id="d6dfc-145">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="d6dfc-145">RELATED LINKS</span></span>