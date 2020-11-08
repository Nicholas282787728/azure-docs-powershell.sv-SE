---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/invoke-azsynapsesparkstatement
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Invoke-AzSynapseSparkStatement.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Invoke-AzSynapseSparkStatement.md
ms.openlocfilehash: 64677ac73fecbaeaaaa327f21bc8e67e2a933d97
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94100705"
---
# <span data-ttu-id="9a440-101">Invoke-AzSynapseSparkStatement</span><span class="sxs-lookup"><span data-stu-id="9a440-101">Invoke-AzSynapseSparkStatement</span></span>

## <span data-ttu-id="9a440-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="9a440-102">SYNOPSIS</span></span>
<span data-ttu-id="9a440-103">Anropar en Synapse Analytics Spark-programsats.</span><span class="sxs-lookup"><span data-stu-id="9a440-103">Invokes a Synapse Analytics Spark statement.</span></span>

## <span data-ttu-id="9a440-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="9a440-104">SYNTAX</span></span>

### <span data-ttu-id="9a440-105">RunSparkStatementByCodePathParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="9a440-105">RunSparkStatementByCodePathParameterSet (Default)</span></span>
```
Invoke-AzSynapseSparkStatement -WorkspaceName <String> -SparkPoolName <String> -Language <String>
 -SessionId <Int32> -FilePath <String> [-Response] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9a440-106">RunSparkStatementByCodeParameterSet</span><span class="sxs-lookup"><span data-stu-id="9a440-106">RunSparkStatementByCodeParameterSet</span></span>
```
Invoke-AzSynapseSparkStatement -WorkspaceName <String> -SparkPoolName <String> -Language <String>
 -SessionId <Int32> -Code <String> [-Response] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9a440-107">RunSparkStatementByCodeAndInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="9a440-107">RunSparkStatementByCodeAndInputObjectParameterSet</span></span>
```
Invoke-AzSynapseSparkStatement -Language <String> -SessionObject <PSSynapseSparkSession> [-SessionId <Int32>]
 -Code <String> [-Response] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="9a440-108">RunSparkStatementByCodePathAndInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="9a440-108">RunSparkStatementByCodePathAndInputObjectParameterSet</span></span>
```
Invoke-AzSynapseSparkStatement -Language <String> -SessionObject <PSSynapseSparkSession> [-SessionId <Int32>]
 -FilePath <String> [-Response] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="9a440-109">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="9a440-109">DESCRIPTION</span></span>
<span data-ttu-id="9a440-110">Cmdleten **Invoke-AzSynapseSparkStatement** anropar en Synapse Analytics Spark-instruktion.</span><span class="sxs-lookup"><span data-stu-id="9a440-110">The **Invoke-AzSynapseSparkStatement** cmdlet invokes a Synapse Analytics Spark statement.</span></span>

## <span data-ttu-id="9a440-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="9a440-111">EXAMPLES</span></span>

### <span data-ttu-id="9a440-112">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="9a440-112">Example 1</span></span>
```powershell
PS C:\> $session = Start-AzSynapseSparkSession -WorkspaceName ContosoWorkspace -SparkPoolName ContosoSparkPool -Name ContosoSessionName -ExecutorCount 3 -ExecutorSize Small
PS C:\> $session.Language = 'Spark' 
PS C:\> $session | Invoke-AzSynapseSparkStatement -Code '
>> print("Hello world\n")
>> '
```

<span data-ttu-id="9a440-113">De här kommandona startar en spark-session och anropar sedan en inline Spark-programsats via pipeline.</span><span class="sxs-lookup"><span data-stu-id="9a440-113">These commands start a Spark session then invoke an inline Spark statement through pipeline.</span></span>

### <span data-ttu-id="9a440-114">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="9a440-114">Example 2</span></span>
```powershell
PS C:\> Invoke-AzSynapseSparkStatement -SessionId 324 -Language 'Spark' -Code '
>> print("Hello world\n")
>> '
```

<span data-ttu-id="9a440-115">De här kommandona startar en spark-session och anropar sedan en inline Spark-programsats.</span><span class="sxs-lookup"><span data-stu-id="9a440-115">These commands start a Spark session then invoke an inline Spark statement.</span></span>

### <span data-ttu-id="9a440-116">Exempel 3</span><span class="sxs-lookup"><span data-stu-id="9a440-116">Example 3</span></span>
```powershell
PS C:\> $session = Start-AzSynapseSparkSession -WorkspaceName ContosoWorkspace -SparkPoolName ContosoSparkPool -Name ContosoSessionName -ExecutorCount 3 -ExecutorSize Small
PS C:\> $session.Language = 'Spark' 
PS C:\> $session | Invoke-AzSynapseSparkStatement -FilePath C:\path\to\code.sc
```

<span data-ttu-id="9a440-117">Dessa kommandon startar en spark-session och anropar sedan Spark-uttryck i en fil.</span><span class="sxs-lookup"><span data-stu-id="9a440-117">These commands start a Spark session then invoke Spark statements in a file.</span></span>

## <span data-ttu-id="9a440-118">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="9a440-118">PARAMETERS</span></span>

### <span data-ttu-id="9a440-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="9a440-119">-AsJob</span></span>
<span data-ttu-id="9a440-120">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="9a440-120">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="9a440-121">-Kod</span><span class="sxs-lookup"><span data-stu-id="9a440-121">-Code</span></span>
<span data-ttu-id="9a440-122">Körnings koden.</span><span class="sxs-lookup"><span data-stu-id="9a440-122">The execution code.</span></span>

```yaml
Type: System.String
Parameter Sets: RunSparkStatementByCodeParameterSet, RunSparkStatementByCodeAndInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9a440-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9a440-123">-DefaultProfile</span></span>
<span data-ttu-id="9a440-124">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="9a440-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9a440-125">-Sökväg</span><span class="sxs-lookup"><span data-stu-id="9a440-125">-FilePath</span></span>
<span data-ttu-id="9a440-126">Anger en lokal fil Sök väg som innehåller körnings koden.</span><span class="sxs-lookup"><span data-stu-id="9a440-126">Specifies a local file path that contains the execution code.</span></span>

```yaml
Type: System.String
Parameter Sets: RunSparkStatementByCodePathParameterSet, RunSparkStatementByCodePathAndInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9a440-127">-Språk</span><span class="sxs-lookup"><span data-stu-id="9a440-127">-Language</span></span>
<span data-ttu-id="9a440-128">Språk för körnings koden.</span><span class="sxs-lookup"><span data-stu-id="9a440-128">Language of the execution code.</span></span>

```yaml
Type: System.String
Parameter Sets: RunSparkStatementByCodePathParameterSet, RunSparkStatementByCodeParameterSet
Aliases:
Accepted values: Spark, Scala, PySpark, Python, SparkDotNet, CSharp, SQL

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: RunSparkStatementByCodeAndInputObjectParameterSet, RunSparkStatementByCodePathAndInputObjectParameterSet
Aliases:
Accepted values: Spark, Scala, PySpark, Python, SparkDotNet, CSharp, SQL

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9a440-129">-Svar</span><span class="sxs-lookup"><span data-stu-id="9a440-129">-Response</span></span>
<span data-ttu-id="9a440-130">Anger att fullständigt svar ska returneras.</span><span class="sxs-lookup"><span data-stu-id="9a440-130">Indicates full response should be return.</span></span>

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

### <span data-ttu-id="9a440-131">-SessionId</span><span class="sxs-lookup"><span data-stu-id="9a440-131">-SessionId</span></span>
<span data-ttu-id="9a440-132">Identifierare för Spark-session.</span><span class="sxs-lookup"><span data-stu-id="9a440-132">Identifier of Spark session.</span></span>

```yaml
Type: System.Int32
Parameter Sets: RunSparkStatementByCodePathParameterSet, RunSparkStatementByCodeParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.Int32
Parameter Sets: RunSparkStatementByCodeAndInputObjectParameterSet, RunSparkStatementByCodePathAndInputObjectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9a440-133">-SessionObject</span><span class="sxs-lookup"><span data-stu-id="9a440-133">-SessionObject</span></span>
<span data-ttu-id="9a440-134">Spark session-objekt som normalt passerar genom pipeline.</span><span class="sxs-lookup"><span data-stu-id="9a440-134">Spark session input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkSession
Parameter Sets: RunSparkStatementByCodeAndInputObjectParameterSet, RunSparkStatementByCodePathAndInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9a440-135">-SparkPoolName</span><span class="sxs-lookup"><span data-stu-id="9a440-135">-SparkPoolName</span></span>
<span data-ttu-id="9a440-136">Namn på Synapse Spark-pool.</span><span class="sxs-lookup"><span data-stu-id="9a440-136">Name of Synapse Spark pool.</span></span>

```yaml
Type: System.String
Parameter Sets: RunSparkStatementByCodePathParameterSet, RunSparkStatementByCodeParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9a440-137">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="9a440-137">-WorkspaceName</span></span>
<span data-ttu-id="9a440-138">Namn på Synapse-arbetsyta.</span><span class="sxs-lookup"><span data-stu-id="9a440-138">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: RunSparkStatementByCodePathParameterSet, RunSparkStatementByCodeParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9a440-139">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="9a440-139">-Confirm</span></span>
<span data-ttu-id="9a440-140">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="9a440-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9a440-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9a440-141">-WhatIf</span></span>
<span data-ttu-id="9a440-142">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="9a440-142">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="9a440-143">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="9a440-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9a440-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9a440-144">CommonParameters</span></span>
<span data-ttu-id="9a440-145">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9a440-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9a440-146">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="9a440-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9a440-147">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="9a440-147">INPUTS</span></span>

### <span data-ttu-id="9a440-148">System. String</span><span class="sxs-lookup"><span data-stu-id="9a440-148">System.String</span></span>

### <span data-ttu-id="9a440-149">Microsoft. Azure. commands. Synapse. Models. PSSynapseSparkSession</span><span class="sxs-lookup"><span data-stu-id="9a440-149">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkSession</span></span>

## <span data-ttu-id="9a440-150">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="9a440-150">OUTPUTS</span></span>

### <span data-ttu-id="9a440-151">Microsoft. Azure. commands. Synapse. Models. PSSynapseExtendedSparkStatement</span><span class="sxs-lookup"><span data-stu-id="9a440-151">Microsoft.Azure.Commands.Synapse.Models.PSSynapseExtendedSparkStatement</span></span>

## <span data-ttu-id="9a440-152">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="9a440-152">NOTES</span></span>

## <span data-ttu-id="9a440-153">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="9a440-153">RELATED LINKS</span></span>