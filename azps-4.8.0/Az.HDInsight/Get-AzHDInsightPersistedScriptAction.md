---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 2B7C1B83-EEEA-4BD1-9E9B-1F3070295995
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/get-azhdinsightpersistedscriptaction
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Get-AzHDInsightPersistedScriptAction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Get-AzHDInsightPersistedScriptAction.md
ms.openlocfilehash: 56056e2933254401645a30e190a3a181b0c4514f
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94100972"
---
# <span data-ttu-id="c9cee-101">Get-AzHDInsightPersistedScriptAction</span><span class="sxs-lookup"><span data-stu-id="c9cee-101">Get-AzHDInsightPersistedScriptAction</span></span>

## <span data-ttu-id="c9cee-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="c9cee-102">SYNOPSIS</span></span>
<span data-ttu-id="c9cee-103">Hämtar de beständiga skript åtgärderna för ett kluster och visar dem i kronologisk ordning, eller hämtar information om en viss beständiga skript åtgärd.</span><span class="sxs-lookup"><span data-stu-id="c9cee-103">Gets the persisted script actions for a cluster and lists them in chronological order, or gets details for a specified persisted script action.</span></span>

## <span data-ttu-id="c9cee-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="c9cee-104">SYNTAX</span></span>

```
Get-AzHDInsightPersistedScriptAction [-ClusterName] <String> [[-Name] <String>] [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c9cee-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="c9cee-105">DESCRIPTION</span></span>
<span data-ttu-id="c9cee-106">Cmdleten **Get-AzHDInsightPersistedScriptAction** hämtar de beständiga skript åtgärderna för ett Azure HDInsight-kluster och visar dem i kronologisk ordning, eller hämtar information om en viss beständiga skript åtgärd.</span><span class="sxs-lookup"><span data-stu-id="c9cee-106">The **Get-AzHDInsightPersistedScriptAction** cmdlet gets the persisted script actions for an Azure HDInsight cluster and lists them in chronological order, or gets details for a specified persisted script action.</span></span>

## <span data-ttu-id="c9cee-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="c9cee-107">EXAMPLES</span></span>

### <span data-ttu-id="c9cee-108">Exempel 1: Hämta de beständiga skript åtgärderna i ett kluster</span><span class="sxs-lookup"><span data-stu-id="c9cee-108">Example 1: Get the persisted script actions on a cluster</span></span>
```
PS C:\>Get-AzHDInsightPersistedScriptAction -ClusterName "your-hadoop-001"
```

<span data-ttu-id="c9cee-109">Det här kommandot hämtar beständiga skript åtgärder i klustret som heter din-Hadoop-001.</span><span class="sxs-lookup"><span data-stu-id="c9cee-109">This command gets persisted script actions on the cluster named your-hadoop-001.</span></span>

## <span data-ttu-id="c9cee-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="c9cee-110">PARAMETERS</span></span>

### <span data-ttu-id="c9cee-111">-Kluster namn</span><span class="sxs-lookup"><span data-stu-id="c9cee-111">-ClusterName</span></span>
<span data-ttu-id="c9cee-112">Anger namnet på klustret.</span><span class="sxs-lookup"><span data-stu-id="c9cee-112">Specifies the name of the cluster.</span></span>

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

### <span data-ttu-id="c9cee-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c9cee-113">-DefaultProfile</span></span>
<span data-ttu-id="c9cee-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="c9cee-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c9cee-115">-Namn</span><span class="sxs-lookup"><span data-stu-id="c9cee-115">-Name</span></span>
<span data-ttu-id="c9cee-116">Anger namnet på den beständiga skript åtgärden.</span><span class="sxs-lookup"><span data-stu-id="c9cee-116">Specifies the name of the persisted script action.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c9cee-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c9cee-117">-ResourceGroupName</span></span>
<span data-ttu-id="c9cee-118">Anger namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="c9cee-118">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="c9cee-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c9cee-119">CommonParameters</span></span>
<span data-ttu-id="c9cee-120">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c9cee-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c9cee-121">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c9cee-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c9cee-122">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="c9cee-122">INPUTS</span></span>

### <span data-ttu-id="c9cee-123">Ingen</span><span class="sxs-lookup"><span data-stu-id="c9cee-123">None</span></span>

## <span data-ttu-id="c9cee-124">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="c9cee-124">OUTPUTS</span></span>

### <span data-ttu-id="c9cee-125">Microsoft. Azure. commands. HDInsight. Models. Management. AzureHDInsightRuntimeScriptAction</span><span class="sxs-lookup"><span data-stu-id="c9cee-125">Microsoft.Azure.Commands.HDInsight.Models.Management.AzureHDInsightRuntimeScriptAction</span></span>

## <span data-ttu-id="c9cee-126">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="c9cee-126">NOTES</span></span>

## <span data-ttu-id="c9cee-127">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="c9cee-127">RELATED LINKS</span></span>

[<span data-ttu-id="c9cee-128">Remove-AzHDInsightPersistedScriptAction</span><span class="sxs-lookup"><span data-stu-id="c9cee-128">Remove-AzHDInsightPersistedScriptAction</span></span>](./Remove-AzHDInsightPersistedScriptAction.md)

[<span data-ttu-id="c9cee-129">Set-AzHDInsightPersistedScriptAction</span><span class="sxs-lookup"><span data-stu-id="c9cee-129">Set-AzHDInsightPersistedScriptAction</span></span>](./Set-AzHDInsightPersistedScriptAction.md)

