---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 92F21752-4FB6-4162-B542-DA25ACA3340B
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/set-azhdinsightpersistedscriptaction
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Set-AzHDInsightPersistedScriptAction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Set-AzHDInsightPersistedScriptAction.md
ms.openlocfilehash: bff21d969a88282f3ba3c1d79d1f717c3c169265
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94102848"
---
# <span data-ttu-id="5f4d4-101">Set-AzHDInsightPersistedScriptAction</span><span class="sxs-lookup"><span data-stu-id="5f4d4-101">Set-AzHDInsightPersistedScriptAction</span></span>

## <span data-ttu-id="5f4d4-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="5f4d4-102">SYNOPSIS</span></span>
<span data-ttu-id="5f4d4-103">Anger att en tidigare körd skript åtgärd ska vara en bestående skript åtgärd.</span><span class="sxs-lookup"><span data-stu-id="5f4d4-103">Sets a previously executed script action to be a persisted script action.</span></span>

## <span data-ttu-id="5f4d4-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="5f4d4-104">SYNTAX</span></span>

```
Set-AzHDInsightPersistedScriptAction [-ClusterName] <String> [-ScriptExecutionId] <Int64>
 [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5f4d4-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="5f4d4-105">DESCRIPTION</span></span>
<span data-ttu-id="5f4d4-106">Cmdleten **set-AzHDInsightPersistedScriptAction** anger en tidigare körd skript åtgärd som ska vara en bestående skript åtgärd.</span><span class="sxs-lookup"><span data-stu-id="5f4d4-106">The **Set-AzHDInsightPersistedScriptAction** cmdlet sets a previously executed script action to be a persisted script action.</span></span>
<span data-ttu-id="5f4d4-107">Den angivna skript åtgärden måste ha lyckats.</span><span class="sxs-lookup"><span data-stu-id="5f4d4-107">The specified script action must have previously succeeded.</span></span>
<span data-ttu-id="5f4d4-108">Skript åtgärden körs varje gång Azure HDInsight-klustret skalas upp.</span><span class="sxs-lookup"><span data-stu-id="5f4d4-108">The script action will run each time the Azure HDInsight cluster is scaled up.</span></span>

## <span data-ttu-id="5f4d4-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="5f4d4-109">EXAMPLES</span></span>

### <span data-ttu-id="5f4d4-110">Exempel 1: ange att en tidigare lyckad skript åtgärd ska bevaras eller kör på klustrets skala</span><span class="sxs-lookup"><span data-stu-id="5f4d4-110">Example 1: Set a previously successful script action to be persisted, or run on cluster scale up</span></span>
```
PS C:\>Set-AzHDInsightPersistedScriptAction `
            -ClusterName "your-hadoop-001" `
            -ScriptExecutionId "<id>"
```

<span data-ttu-id="5f4d4-111">Det här kommandot ställer in en åtgärd med skript som redan har lyckats.</span><span class="sxs-lookup"><span data-stu-id="5f4d4-111">This command sets a previously successful script action to be a persisted script action.</span></span>

## <span data-ttu-id="5f4d4-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="5f4d4-112">PARAMETERS</span></span>

### <span data-ttu-id="5f4d4-113">-Kluster namn</span><span class="sxs-lookup"><span data-stu-id="5f4d4-113">-ClusterName</span></span>
<span data-ttu-id="5f4d4-114">Anger namnet på klustret.</span><span class="sxs-lookup"><span data-stu-id="5f4d4-114">Specifies the name of the cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5f4d4-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5f4d4-115">-DefaultProfile</span></span>
<span data-ttu-id="5f4d4-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="5f4d4-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="5f4d4-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5f4d4-117">-ResourceGroupName</span></span>
<span data-ttu-id="5f4d4-118">Anger namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="5f4d4-118">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="5f4d4-119">-ScriptExecutionId</span><span class="sxs-lookup"><span data-stu-id="5f4d4-119">-ScriptExecutionId</span></span>
<span data-ttu-id="5f4d4-120">Anger kör-ID för skript åtgärden som ska behållas till bevarat.</span><span class="sxs-lookup"><span data-stu-id="5f4d4-120">Specifies the execution ID of the script action to promote to persisted.</span></span>
<span data-ttu-id="5f4d4-121">Skript åtgärden måste ha lyckats för att kunna höjas.</span><span class="sxs-lookup"><span data-stu-id="5f4d4-121">This script action must have succeeded in order to be promoted.</span></span>
<span data-ttu-id="5f4d4-122">Kör-ID för skript åtgärden kan hittas med Get-AzHDInsightScriptActionHistory.</span><span class="sxs-lookup"><span data-stu-id="5f4d4-122">You can find the script action execution ID using Get-AzHDInsightScriptActionHistory.</span></span>

```yaml
Type: System.Int64
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5f4d4-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5f4d4-123">CommonParameters</span></span>
<span data-ttu-id="5f4d4-124">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5f4d4-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5f4d4-125">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5f4d4-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5f4d4-126">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="5f4d4-126">INPUTS</span></span>

### <span data-ttu-id="5f4d4-127">Ingen</span><span class="sxs-lookup"><span data-stu-id="5f4d4-127">None</span></span>

## <span data-ttu-id="5f4d4-128">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="5f4d4-128">OUTPUTS</span></span>

### <span data-ttu-id="5f4d4-129">System. Void</span><span class="sxs-lookup"><span data-stu-id="5f4d4-129">System.Void</span></span>

## <span data-ttu-id="5f4d4-130">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="5f4d4-130">NOTES</span></span>

## <span data-ttu-id="5f4d4-131">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="5f4d4-131">RELATED LINKS</span></span>

[<span data-ttu-id="5f4d4-132">Get-AzHDInsightPersistedScriptAction</span><span class="sxs-lookup"><span data-stu-id="5f4d4-132">Get-AzHDInsightPersistedScriptAction</span></span>](./Get-AzHDInsightPersistedScriptAction.md)

[<span data-ttu-id="5f4d4-133">Remove-AzHDInsightPersistedScriptAction</span><span class="sxs-lookup"><span data-stu-id="5f4d4-133">Remove-AzHDInsightPersistedScriptAction</span></span>](./Remove-AzHDInsightPersistedScriptAction.md)

