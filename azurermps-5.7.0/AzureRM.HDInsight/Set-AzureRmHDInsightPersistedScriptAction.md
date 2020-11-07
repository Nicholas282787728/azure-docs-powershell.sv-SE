---
external help file: Microsoft.Azure.Commands.HDInsight.dll-Help.xml
Module Name: AzureRM.HDInsight
ms.assetid: 92F21752-4FB6-4162-B542-DA25ACA3340B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.hdinsight/set-azurermhdinsightpersistedscriptaction
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Set-AzureRmHDInsightPersistedScriptAction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Set-AzureRmHDInsightPersistedScriptAction.md
ms.openlocfilehash: 28b95833e9221e5ecaa05ab33a6e2518c7cca1a2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93757947"
---
# <span data-ttu-id="a5319-101">Set-AzureRmHDInsightPersistedScriptAction</span><span class="sxs-lookup"><span data-stu-id="a5319-101">Set-AzureRmHDInsightPersistedScriptAction</span></span>

## <span data-ttu-id="a5319-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="a5319-102">SYNOPSIS</span></span>
<span data-ttu-id="a5319-103">Anger att en tidigare körd skript åtgärd ska vara en bestående skript åtgärd.</span><span class="sxs-lookup"><span data-stu-id="a5319-103">Sets a previously executed script action to be a persisted script action.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a5319-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="a5319-104">SYNTAX</span></span>

```
Set-AzureRmHDInsightPersistedScriptAction [-ClusterName] <String> [-ScriptExecutionId] <Int64>
 [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a5319-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="a5319-105">DESCRIPTION</span></span>
<span data-ttu-id="a5319-106">Cmdleten **set-AzureRmHDInsightPersistedScriptAction** anger en tidigare körd skript åtgärd som ska vara en bestående skript åtgärd.</span><span class="sxs-lookup"><span data-stu-id="a5319-106">The **Set-AzureRmHDInsightPersistedScriptAction** cmdlet sets a previously executed script action to be a persisted script action.</span></span>
<span data-ttu-id="a5319-107">Den angivna skript åtgärden måste ha lyckats.</span><span class="sxs-lookup"><span data-stu-id="a5319-107">The specified script action must have previously succeeded.</span></span>
<span data-ttu-id="a5319-108">Skript åtgärden körs varje gång Azure HDInsight-klustret skalas upp.</span><span class="sxs-lookup"><span data-stu-id="a5319-108">The script action will run each time the Azure HDInsight cluster is scaled up.</span></span>

## <span data-ttu-id="a5319-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="a5319-109">EXAMPLES</span></span>

### <span data-ttu-id="a5319-110">Exempel 1: ange att en tidigare lyckad skript åtgärd ska bevaras eller kör på klustrets skala</span><span class="sxs-lookup"><span data-stu-id="a5319-110">Example 1: Set a previously successful script action to be persisted, or run on cluster scale up</span></span>
```
PS C:\>Set-AzureRmHDInsightPersistedScriptAction `
            -ClusterName "your-hadoop-001" `
            -ScriptExecutionId "<id>"
```

<span data-ttu-id="a5319-111">Det här kommandot ställer in en åtgärd med skript som redan har lyckats.</span><span class="sxs-lookup"><span data-stu-id="a5319-111">This command sets a previously successful script action to be a persisted script action.</span></span>

## <span data-ttu-id="a5319-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="a5319-112">PARAMETERS</span></span>

### <span data-ttu-id="a5319-113">-Kluster namn</span><span class="sxs-lookup"><span data-stu-id="a5319-113">-ClusterName</span></span>
<span data-ttu-id="a5319-114">Anger namnet på klustret.</span><span class="sxs-lookup"><span data-stu-id="a5319-114">Specifies the name of the cluster.</span></span>

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

### <span data-ttu-id="a5319-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a5319-115">-DefaultProfile</span></span>
<span data-ttu-id="a5319-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="a5319-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a5319-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a5319-117">-ResourceGroupName</span></span>
<span data-ttu-id="a5319-118">Anger namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="a5319-118">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="a5319-119">-ScriptExecutionId</span><span class="sxs-lookup"><span data-stu-id="a5319-119">-ScriptExecutionId</span></span>
<span data-ttu-id="a5319-120">Anger kör-ID för skript åtgärden som ska behållas till bevarat.</span><span class="sxs-lookup"><span data-stu-id="a5319-120">Specifies the execution ID of the script action to promote to persisted.</span></span>
<span data-ttu-id="a5319-121">Skript åtgärden måste ha lyckats för att kunna höjas.</span><span class="sxs-lookup"><span data-stu-id="a5319-121">This script action must have succeeded in order to be promoted.</span></span>
<span data-ttu-id="a5319-122">Kör-ID för skript åtgärden kan hittas med Get-AzureRmHDInsightScriptActionHistory.</span><span class="sxs-lookup"><span data-stu-id="a5319-122">You can find the script action execution ID using Get-AzureRmHDInsightScriptActionHistory.</span></span>

```yaml
Type: Int64
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a5319-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a5319-123">CommonParameters</span></span>
<span data-ttu-id="a5319-124">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a5319-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a5319-125">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a5319-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a5319-126">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="a5319-126">INPUTS</span></span>

### <span data-ttu-id="a5319-127">Ingen</span><span class="sxs-lookup"><span data-stu-id="a5319-127">None</span></span>
<span data-ttu-id="a5319-128">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="a5319-128">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="a5319-129">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="a5319-129">OUTPUTS</span></span>

### <span data-ttu-id="a5319-130">System. Void</span><span class="sxs-lookup"><span data-stu-id="a5319-130">System.Void</span></span>

## <span data-ttu-id="a5319-131">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="a5319-131">NOTES</span></span>

## <span data-ttu-id="a5319-132">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="a5319-132">RELATED LINKS</span></span>

[<span data-ttu-id="a5319-133">Get-AzureRmHDInsightPersistedScriptAction</span><span class="sxs-lookup"><span data-stu-id="a5319-133">Get-AzureRmHDInsightPersistedScriptAction</span></span>](./Get-AzureRmHDInsightPersistedScriptAction.md)

[<span data-ttu-id="a5319-134">Remove-AzureRmHDInsightPersistedScriptAction</span><span class="sxs-lookup"><span data-stu-id="a5319-134">Remove-AzureRmHDInsightPersistedScriptAction</span></span>](./Remove-AzureRmHDInsightPersistedScriptAction.md)


