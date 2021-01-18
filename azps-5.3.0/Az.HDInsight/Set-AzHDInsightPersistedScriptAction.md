---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 92F21752-4FB6-4162-B542-DA25ACA3340B
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/set-azhdinsightpersistedscriptaction
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Set-AzHDInsightPersistedScriptAction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Set-AzHDInsightPersistedScriptAction.md
ms.openlocfilehash: f593989125642d03a9dff1b48bbc7430498b2a36
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98522624"
---
# <span data-ttu-id="bea34-101">Set-AzHDInsightPersistedScriptAction</span><span class="sxs-lookup"><span data-stu-id="bea34-101">Set-AzHDInsightPersistedScriptAction</span></span>

## <span data-ttu-id="bea34-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="bea34-102">SYNOPSIS</span></span>
<span data-ttu-id="bea34-103">Anger att en tidigare körd skript åtgärd ska vara en bestående skript åtgärd.</span><span class="sxs-lookup"><span data-stu-id="bea34-103">Sets a previously executed script action to be a persisted script action.</span></span>

## <span data-ttu-id="bea34-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="bea34-104">SYNTAX</span></span>

```
Set-AzHDInsightPersistedScriptAction [-ClusterName] <String> [-ScriptExecutionId] <Int64>
 [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bea34-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="bea34-105">DESCRIPTION</span></span>
<span data-ttu-id="bea34-106">Cmdleten **set-AzHDInsightPersistedScriptAction** anger en tidigare körd skript åtgärd som ska vara en bestående skript åtgärd.</span><span class="sxs-lookup"><span data-stu-id="bea34-106">The **Set-AzHDInsightPersistedScriptAction** cmdlet sets a previously executed script action to be a persisted script action.</span></span>
<span data-ttu-id="bea34-107">Den angivna skript åtgärden måste ha lyckats.</span><span class="sxs-lookup"><span data-stu-id="bea34-107">The specified script action must have previously succeeded.</span></span>
<span data-ttu-id="bea34-108">Skript åtgärden körs varje gång Azure HDInsight-klustret skalas upp.</span><span class="sxs-lookup"><span data-stu-id="bea34-108">The script action will run each time the Azure HDInsight cluster is scaled up.</span></span>

## <span data-ttu-id="bea34-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="bea34-109">EXAMPLES</span></span>

### <span data-ttu-id="bea34-110">Exempel 1: ange att en tidigare lyckad skript åtgärd ska bevaras eller kör på klustrets skala</span><span class="sxs-lookup"><span data-stu-id="bea34-110">Example 1: Set a previously successful script action to be persisted, or run on cluster scale up</span></span>
```
PS C:\>Set-AzHDInsightPersistedScriptAction `
            -ClusterName "your-hadoop-001" `
            -ScriptExecutionId "<id>"
```

<span data-ttu-id="bea34-111">Det här kommandot ställer in en åtgärd med skript som redan har lyckats.</span><span class="sxs-lookup"><span data-stu-id="bea34-111">This command sets a previously successful script action to be a persisted script action.</span></span>

## <span data-ttu-id="bea34-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="bea34-112">PARAMETERS</span></span>

### <span data-ttu-id="bea34-113">-Kluster namn</span><span class="sxs-lookup"><span data-stu-id="bea34-113">-ClusterName</span></span>
<span data-ttu-id="bea34-114">Anger namnet på klustret.</span><span class="sxs-lookup"><span data-stu-id="bea34-114">Specifies the name of the cluster.</span></span>

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

### <span data-ttu-id="bea34-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bea34-115">-DefaultProfile</span></span>
<span data-ttu-id="bea34-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="bea34-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="bea34-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bea34-117">-ResourceGroupName</span></span>
<span data-ttu-id="bea34-118">Anger namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="bea34-118">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="bea34-119">-ScriptExecutionId</span><span class="sxs-lookup"><span data-stu-id="bea34-119">-ScriptExecutionId</span></span>
<span data-ttu-id="bea34-120">Anger kör-ID för skript åtgärden som ska behållas till bevarat.</span><span class="sxs-lookup"><span data-stu-id="bea34-120">Specifies the execution ID of the script action to promote to persisted.</span></span>
<span data-ttu-id="bea34-121">Skript åtgärden måste ha lyckats för att kunna höjas.</span><span class="sxs-lookup"><span data-stu-id="bea34-121">This script action must have succeeded in order to be promoted.</span></span>
<span data-ttu-id="bea34-122">Kör-ID för skript åtgärden kan hittas med Get-AzHDInsightScriptActionHistory.</span><span class="sxs-lookup"><span data-stu-id="bea34-122">You can find the script action execution ID using Get-AzHDInsightScriptActionHistory.</span></span>

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

### <span data-ttu-id="bea34-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bea34-123">CommonParameters</span></span>
<span data-ttu-id="bea34-124">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bea34-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bea34-125">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="bea34-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bea34-126">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="bea34-126">INPUTS</span></span>

### <span data-ttu-id="bea34-127">Ingen</span><span class="sxs-lookup"><span data-stu-id="bea34-127">None</span></span>

## <span data-ttu-id="bea34-128">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="bea34-128">OUTPUTS</span></span>

### <span data-ttu-id="bea34-129">System. Void</span><span class="sxs-lookup"><span data-stu-id="bea34-129">System.Void</span></span>

## <span data-ttu-id="bea34-130">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="bea34-130">NOTES</span></span>

## <span data-ttu-id="bea34-131">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="bea34-131">RELATED LINKS</span></span>

[<span data-ttu-id="bea34-132">Get-AzHDInsightPersistedScriptAction</span><span class="sxs-lookup"><span data-stu-id="bea34-132">Get-AzHDInsightPersistedScriptAction</span></span>](./Get-AzHDInsightPersistedScriptAction.md)

[<span data-ttu-id="bea34-133">Remove-AzHDInsightPersistedScriptAction</span><span class="sxs-lookup"><span data-stu-id="bea34-133">Remove-AzHDInsightPersistedScriptAction</span></span>](./Remove-AzHDInsightPersistedScriptAction.md)


