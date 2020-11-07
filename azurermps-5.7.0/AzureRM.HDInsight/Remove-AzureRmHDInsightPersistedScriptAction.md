---
external help file: Microsoft.Azure.Commands.HDInsight.dll-Help.xml
Module Name: AzureRM.HDInsight
ms.assetid: 08D1D6AC-D064-4E2D-9C22-0B65E7BE4DA7
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.hdinsight/remove-azurermhdinsightpersistedscriptaction
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Remove-AzureRmHDInsightPersistedScriptAction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Remove-AzureRmHDInsightPersistedScriptAction.md
ms.openlocfilehash: 48b0fab43e104a5cae68ef26698735e89c603a78
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93756284"
---
# <span data-ttu-id="e42b1-101">Remove-AzureRmHDInsightPersistedScriptAction</span><span class="sxs-lookup"><span data-stu-id="e42b1-101">Remove-AzureRmHDInsightPersistedScriptAction</span></span>

## <span data-ttu-id="e42b1-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="e42b1-102">SYNOPSIS</span></span>
<span data-ttu-id="e42b1-103">Tar bort en beständiga skript åtgärd från ett HDInsight-kluster.</span><span class="sxs-lookup"><span data-stu-id="e42b1-103">Removes an persisted script action from an HDInsight cluster.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e42b1-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="e42b1-104">SYNTAX</span></span>

```
Remove-AzureRmHDInsightPersistedScriptAction [-ClusterName] <String> [-Name] <String>
 [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e42b1-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="e42b1-105">DESCRIPTION</span></span>
<span data-ttu-id="e42b1-106">Cmdleten **Remove-AzureRmHDInsightPersistedScriptAction** tar bort en beständiga skript åtgärd från det angivna Azure HDInsight-klustrets lista över beständiga skript åtgärder.</span><span class="sxs-lookup"><span data-stu-id="e42b1-106">The **Remove-AzureRmHDInsightPersistedScriptAction** cmdlet removes a persisted script action from the specified Azure HDInsight cluster's list of persisted script actions.</span></span>
<span data-ttu-id="e42b1-107">Det borttagna skriptet körs inte längre när klustret skal för änd ras.</span><span class="sxs-lookup"><span data-stu-id="e42b1-107">The removed script will no longer be executed when the cluster is scaled up.</span></span>

## <span data-ttu-id="e42b1-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="e42b1-108">EXAMPLES</span></span>

### <span data-ttu-id="e42b1-109">Exempel 1: ta bort en skript åtgärd från listan med beständiga skript åtgärder i ett kluster</span><span class="sxs-lookup"><span data-stu-id="e42b1-109">Example 1: Remove a script action from the list of persisted script actions on a cluster</span></span>
```
PS C:\>Remove-AzureRmHDInsightPersistedScriptAction `
            -ClusterName "your-hadoop-001" `
            -Name "Scriptaction"
```

<span data-ttu-id="e42b1-110">Det här kommandot tar bort skript åtgärden som heter Scriptaction från listan med beständiga skript åtgärder i det angivna klustret.</span><span class="sxs-lookup"><span data-stu-id="e42b1-110">This command removes the script action named Scriptaction from the list of persisted script actions on the specified cluster.</span></span>

## <span data-ttu-id="e42b1-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="e42b1-111">PARAMETERS</span></span>

### <span data-ttu-id="e42b1-112">-Kluster namn</span><span class="sxs-lookup"><span data-stu-id="e42b1-112">-ClusterName</span></span>
<span data-ttu-id="e42b1-113">Anger namnet på klustret.</span><span class="sxs-lookup"><span data-stu-id="e42b1-113">Specifies the name of the cluster.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e42b1-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e42b1-114">-DefaultProfile</span></span>
<span data-ttu-id="e42b1-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="e42b1-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e42b1-116">-Namn</span><span class="sxs-lookup"><span data-stu-id="e42b1-116">-Name</span></span>
<span data-ttu-id="e42b1-117">Anger namnet på den beständiga skript åtgärd som ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="e42b1-117">Specifies the name of the persisted script action to be removed.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e42b1-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e42b1-118">-ResourceGroupName</span></span>
<span data-ttu-id="e42b1-119">Anger namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="e42b1-119">Specifies the name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e42b1-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e42b1-120">CommonParameters</span></span>
<span data-ttu-id="e42b1-121">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e42b1-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e42b1-122">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e42b1-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e42b1-123">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="e42b1-123">INPUTS</span></span>

### <span data-ttu-id="e42b1-124">Ingen</span><span class="sxs-lookup"><span data-stu-id="e42b1-124">None</span></span>
<span data-ttu-id="e42b1-125">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="e42b1-125">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="e42b1-126">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="e42b1-126">OUTPUTS</span></span>

### <span data-ttu-id="e42b1-127">System. Void</span><span class="sxs-lookup"><span data-stu-id="e42b1-127">System.Void</span></span>

## <span data-ttu-id="e42b1-128">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="e42b1-128">NOTES</span></span>

## <span data-ttu-id="e42b1-129">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="e42b1-129">RELATED LINKS</span></span>

[<span data-ttu-id="e42b1-130">Get-AzureRmHDInsightPersistedScriptAction</span><span class="sxs-lookup"><span data-stu-id="e42b1-130">Get-AzureRmHDInsightPersistedScriptAction</span></span>](./Get-AzureRmHDInsightPersistedScriptAction.md)

[<span data-ttu-id="e42b1-131">Set-AzureRmHDInsightPersistedScriptAction</span><span class="sxs-lookup"><span data-stu-id="e42b1-131">Set-AzureRmHDInsightPersistedScriptAction</span></span>](./Set-AzureRmHDInsightPersistedScriptAction.md)


