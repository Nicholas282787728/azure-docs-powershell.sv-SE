---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: CE690DB0-0CD4-4841-B219-C208173D4730
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/get-azhdinsightscriptactionhistory
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Get-AzHDInsightScriptActionHistory.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Get-AzHDInsightScriptActionHistory.md
ms.openlocfilehash: 0424578473aedb60071e3389e7aaff2b84848f8c
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98520612"
---
# <span data-ttu-id="e2b5a-101">Get-AzHDInsightScriptActionHistory</span><span class="sxs-lookup"><span data-stu-id="e2b5a-101">Get-AzHDInsightScriptActionHistory</span></span>

## <span data-ttu-id="e2b5a-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="e2b5a-102">SYNOPSIS</span></span>
<span data-ttu-id="e2b5a-103">Hämtar skript åtgärds historiken för ett kluster och visar den i omvänd kronologisk ordning, eller hämtar information om en tidigare körd skript åtgärd.</span><span class="sxs-lookup"><span data-stu-id="e2b5a-103">Gets the script action history for a cluster and lists it in reverse chronological order, or gets details of a previously executed script action.</span></span>

## <span data-ttu-id="e2b5a-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="e2b5a-104">SYNTAX</span></span>

```
Get-AzHDInsightScriptActionHistory [-ClusterName] <String> [[-ScriptExecutionId] <Int64>]
 [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e2b5a-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="e2b5a-105">DESCRIPTION</span></span>
<span data-ttu-id="e2b5a-106">Cmdleten **Get-AzHDInsightScriptActionHistory** hämtar skript åtgärds historiken för ett Azure HDInsight-kluster och visar den i omvänd kronologisk ordning, eller hämtar information om en tidigare körd skript åtgärd.</span><span class="sxs-lookup"><span data-stu-id="e2b5a-106">The **Get-AzHDInsightScriptActionHistory** cmdlet gets the script action history for an Azure HDInsight cluster and lists it in reverse chronological order, or gets details of a previously executed script action.</span></span>

## <span data-ttu-id="e2b5a-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="e2b5a-107">EXAMPLES</span></span>

### <span data-ttu-id="e2b5a-108">Exempel 1: Hämta historiken över körningar av skript åtgärder för ett kluster</span><span class="sxs-lookup"><span data-stu-id="e2b5a-108">Example 1: Get the history of script actions executions for a cluster</span></span>
```
PS C:\>Get-AzHDInsightScriptActionHistory -ClusterName "your-hadoop-001"
```

<span data-ttu-id="e2b5a-109">Det här kommandot hämtar skript åtgärderna för klustret din-Hadoop-001.</span><span class="sxs-lookup"><span data-stu-id="e2b5a-109">This command gets the history of script actions for the cluster your-hadoop-001.</span></span>

## <span data-ttu-id="e2b5a-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="e2b5a-110">PARAMETERS</span></span>

### <span data-ttu-id="e2b5a-111">-Kluster namn</span><span class="sxs-lookup"><span data-stu-id="e2b5a-111">-ClusterName</span></span>
<span data-ttu-id="e2b5a-112">Anger namnet på klustret.</span><span class="sxs-lookup"><span data-stu-id="e2b5a-112">Specifies the name of the cluster.</span></span>

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

### <span data-ttu-id="e2b5a-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e2b5a-113">-DefaultProfile</span></span>
<span data-ttu-id="e2b5a-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="e2b5a-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e2b5a-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e2b5a-115">-ResourceGroupName</span></span>
<span data-ttu-id="e2b5a-116">Anger namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="e2b5a-116">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="e2b5a-117">-ScriptExecutionId</span><span class="sxs-lookup"><span data-stu-id="e2b5a-117">-ScriptExecutionId</span></span>
<span data-ttu-id="e2b5a-118">Anger kör-ID för den skript åtgärd som körs.</span><span class="sxs-lookup"><span data-stu-id="e2b5a-118">Specifies the execution ID of the executed script action.</span></span>

```yaml
Type: System.Nullable`1[System.Int64]
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e2b5a-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e2b5a-119">CommonParameters</span></span>
<span data-ttu-id="e2b5a-120">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e2b5a-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e2b5a-121">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e2b5a-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e2b5a-122">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="e2b5a-122">INPUTS</span></span>

### <span data-ttu-id="e2b5a-123">Ingen</span><span class="sxs-lookup"><span data-stu-id="e2b5a-123">None</span></span>

## <span data-ttu-id="e2b5a-124">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="e2b5a-124">OUTPUTS</span></span>

### <span data-ttu-id="e2b5a-125">Microsoft. Azure. commands. HDInsight. Models. Management. AzureHDInsightRuntimeScriptActionDetail</span><span class="sxs-lookup"><span data-stu-id="e2b5a-125">Microsoft.Azure.Commands.HDInsight.Models.Management.AzureHDInsightRuntimeScriptActionDetail</span></span>

## <span data-ttu-id="e2b5a-126">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="e2b5a-126">NOTES</span></span>

## <span data-ttu-id="e2b5a-127">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="e2b5a-127">RELATED LINKS</span></span>
