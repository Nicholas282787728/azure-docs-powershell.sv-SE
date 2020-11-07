---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 08D1D6AC-D064-4E2D-9C22-0B65E7BE4DA7
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/remove-azhdinsightpersistedscriptaction
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Remove-AzHDInsightPersistedScriptAction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Remove-AzHDInsightPersistedScriptAction.md
ms.openlocfilehash: cfa99107875940854b9ad9c74061ec717a16c51e
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93916562"
---
# <span data-ttu-id="10c8b-101">Remove-AzHDInsightPersistedScriptAction</span><span class="sxs-lookup"><span data-stu-id="10c8b-101">Remove-AzHDInsightPersistedScriptAction</span></span>

## <span data-ttu-id="10c8b-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="10c8b-102">SYNOPSIS</span></span>
<span data-ttu-id="10c8b-103">Tar bort en beständiga skript åtgärd från ett HDInsight-kluster.</span><span class="sxs-lookup"><span data-stu-id="10c8b-103">Removes an persisted script action from an HDInsight cluster.</span></span>

## <span data-ttu-id="10c8b-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="10c8b-104">SYNTAX</span></span>

```
Remove-AzHDInsightPersistedScriptAction [-ClusterName] <String> [-Name] <String> [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="10c8b-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="10c8b-105">DESCRIPTION</span></span>
<span data-ttu-id="10c8b-106">Cmdleten **Remove-AzHDInsightPersistedScriptAction** tar bort en beständiga skript åtgärd från det angivna Azure HDInsight-klustrets lista över beständiga skript åtgärder.</span><span class="sxs-lookup"><span data-stu-id="10c8b-106">The **Remove-AzHDInsightPersistedScriptAction** cmdlet removes a persisted script action from the specified Azure HDInsight cluster's list of persisted script actions.</span></span>
<span data-ttu-id="10c8b-107">Det borttagna skriptet körs inte längre när klustret skal för änd ras.</span><span class="sxs-lookup"><span data-stu-id="10c8b-107">The removed script will no longer be executed when the cluster is scaled up.</span></span>

## <span data-ttu-id="10c8b-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="10c8b-108">EXAMPLES</span></span>

### <span data-ttu-id="10c8b-109">Exempel 1: ta bort en skript åtgärd från listan med beständiga skript åtgärder i ett kluster</span><span class="sxs-lookup"><span data-stu-id="10c8b-109">Example 1: Remove a script action from the list of persisted script actions on a cluster</span></span>
```
PS C:\>Remove-AzHDInsightPersistedScriptAction `
            -ClusterName "your-hadoop-001" `
            -Name "Scriptaction"
```

<span data-ttu-id="10c8b-110">Det här kommandot tar bort skript åtgärden som heter Scriptaction från listan med beständiga skript åtgärder i det angivna klustret.</span><span class="sxs-lookup"><span data-stu-id="10c8b-110">This command removes the script action named Scriptaction from the list of persisted script actions on the specified cluster.</span></span>

## <span data-ttu-id="10c8b-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="10c8b-111">PARAMETERS</span></span>

### <span data-ttu-id="10c8b-112">-Kluster namn</span><span class="sxs-lookup"><span data-stu-id="10c8b-112">-ClusterName</span></span>
<span data-ttu-id="10c8b-113">Anger namnet på klustret.</span><span class="sxs-lookup"><span data-stu-id="10c8b-113">Specifies the name of the cluster.</span></span>

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

### <span data-ttu-id="10c8b-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="10c8b-114">-DefaultProfile</span></span>
<span data-ttu-id="10c8b-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="10c8b-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="10c8b-116">-Namn</span><span class="sxs-lookup"><span data-stu-id="10c8b-116">-Name</span></span>
<span data-ttu-id="10c8b-117">Anger namnet på den beständiga skript åtgärd som ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="10c8b-117">Specifies the name of the persisted script action to be removed.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="10c8b-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="10c8b-118">-ResourceGroupName</span></span>
<span data-ttu-id="10c8b-119">Anger namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="10c8b-119">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="10c8b-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="10c8b-120">CommonParameters</span></span>
<span data-ttu-id="10c8b-121">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="10c8b-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="10c8b-122">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="10c8b-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="10c8b-123">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="10c8b-123">INPUTS</span></span>

### <span data-ttu-id="10c8b-124">Ingen</span><span class="sxs-lookup"><span data-stu-id="10c8b-124">None</span></span>

## <span data-ttu-id="10c8b-125">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="10c8b-125">OUTPUTS</span></span>

### <span data-ttu-id="10c8b-126">System. Void</span><span class="sxs-lookup"><span data-stu-id="10c8b-126">System.Void</span></span>

## <span data-ttu-id="10c8b-127">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="10c8b-127">NOTES</span></span>

## <span data-ttu-id="10c8b-128">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="10c8b-128">RELATED LINKS</span></span>

[<span data-ttu-id="10c8b-129">Get-AzHDInsightPersistedScriptAction</span><span class="sxs-lookup"><span data-stu-id="10c8b-129">Get-AzHDInsightPersistedScriptAction</span></span>](./Get-AzHDInsightPersistedScriptAction.md)

[<span data-ttu-id="10c8b-130">Set-AzHDInsightPersistedScriptAction</span><span class="sxs-lookup"><span data-stu-id="10c8b-130">Set-AzHDInsightPersistedScriptAction</span></span>](./Set-AzHDInsightPersistedScriptAction.md)


