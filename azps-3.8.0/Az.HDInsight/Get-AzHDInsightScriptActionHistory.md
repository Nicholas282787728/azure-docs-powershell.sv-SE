---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: CE690DB0-0CD4-4841-B219-C208173D4730
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/get-azhdinsightscriptactionhistory
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Get-AzHDInsightScriptActionHistory.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Get-AzHDInsightScriptActionHistory.md
ms.openlocfilehash: 4f73c58ee709e53e1337c161b698aa31cc38ca43
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93928138"
---
# <span data-ttu-id="187f5-101">Get-AzHDInsightScriptActionHistory</span><span class="sxs-lookup"><span data-stu-id="187f5-101">Get-AzHDInsightScriptActionHistory</span></span>

## <span data-ttu-id="187f5-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="187f5-102">SYNOPSIS</span></span>
<span data-ttu-id="187f5-103">Hämtar skript åtgärds historiken för ett kluster och visar den i omvänd kronologisk ordning, eller hämtar information om en tidigare körd skript åtgärd.</span><span class="sxs-lookup"><span data-stu-id="187f5-103">Gets the script action history for a cluster and lists it in reverse chronological order, or gets details of a previously executed script action.</span></span>

## <span data-ttu-id="187f5-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="187f5-104">SYNTAX</span></span>

```
Get-AzHDInsightScriptActionHistory [-ClusterName] <String> [[-ScriptExecutionId] <Int64>]
 [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="187f5-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="187f5-105">DESCRIPTION</span></span>
<span data-ttu-id="187f5-106">Cmdleten **Get-AzHDInsightScriptActionHistory** hämtar skript åtgärds historiken för ett Azure HDInsight-kluster och visar den i omvänd kronologisk ordning, eller hämtar information om en tidigare körd skript åtgärd.</span><span class="sxs-lookup"><span data-stu-id="187f5-106">The **Get-AzHDInsightScriptActionHistory** cmdlet gets the script action history for an Azure HDInsight cluster and lists it in reverse chronological order, or gets details of a previously executed script action.</span></span>

## <span data-ttu-id="187f5-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="187f5-107">EXAMPLES</span></span>

### <span data-ttu-id="187f5-108">Exempel 1: Hämta historiken över körningar av skript åtgärder för ett kluster</span><span class="sxs-lookup"><span data-stu-id="187f5-108">Example 1: Get the history of script actions executions for a cluster</span></span>
```
PS C:\>Get-AzHDInsightScriptActionHistory -ClusterName "your-hadoop-001"
```

<span data-ttu-id="187f5-109">Det här kommandot hämtar skript åtgärderna för klustret din-Hadoop-001.</span><span class="sxs-lookup"><span data-stu-id="187f5-109">This command gets the history of script actions for the cluster your-hadoop-001.</span></span>

## <span data-ttu-id="187f5-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="187f5-110">PARAMETERS</span></span>

### <span data-ttu-id="187f5-111">-Kluster namn</span><span class="sxs-lookup"><span data-stu-id="187f5-111">-ClusterName</span></span>
<span data-ttu-id="187f5-112">Anger namnet på klustret.</span><span class="sxs-lookup"><span data-stu-id="187f5-112">Specifies the name of the cluster.</span></span>

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

### <span data-ttu-id="187f5-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="187f5-113">-DefaultProfile</span></span>
<span data-ttu-id="187f5-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="187f5-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="187f5-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="187f5-115">-ResourceGroupName</span></span>
<span data-ttu-id="187f5-116">Anger namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="187f5-116">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="187f5-117">-ScriptExecutionId</span><span class="sxs-lookup"><span data-stu-id="187f5-117">-ScriptExecutionId</span></span>
<span data-ttu-id="187f5-118">Anger kör-ID för den skript åtgärd som körs.</span><span class="sxs-lookup"><span data-stu-id="187f5-118">Specifies the execution ID of the executed script action.</span></span>

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

### <span data-ttu-id="187f5-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="187f5-119">CommonParameters</span></span>
<span data-ttu-id="187f5-120">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="187f5-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="187f5-121">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="187f5-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="187f5-122">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="187f5-122">INPUTS</span></span>

### <span data-ttu-id="187f5-123">Ingen</span><span class="sxs-lookup"><span data-stu-id="187f5-123">None</span></span>

## <span data-ttu-id="187f5-124">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="187f5-124">OUTPUTS</span></span>

### <span data-ttu-id="187f5-125">Microsoft. Azure. commands. HDInsight. Models. Management. AzureHDInsightRuntimeScriptActionDetail</span><span class="sxs-lookup"><span data-stu-id="187f5-125">Microsoft.Azure.Commands.HDInsight.Models.Management.AzureHDInsightRuntimeScriptActionDetail</span></span>

## <span data-ttu-id="187f5-126">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="187f5-126">NOTES</span></span>

## <span data-ttu-id="187f5-127">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="187f5-127">RELATED LINKS</span></span>
