---
external help file: Microsoft.Azure.Commands.HDInsight.dll-Help.xml
Module Name: AzureRM.HDInsight
ms.assetid: 2B7C1B83-EEEA-4BD1-9E9B-1F3070295995
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.hdinsight/get-azurermhdinsightpersistedscriptaction
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Get-AzureRmHDInsightPersistedScriptAction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Get-AzureRmHDInsightPersistedScriptAction.md
ms.openlocfilehash: c70b4fecc9be5937d24ca4bc84b8aa6554daf482
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93586099"
---
# <span data-ttu-id="36458-101">Get-AzureRmHDInsightPersistedScriptAction</span><span class="sxs-lookup"><span data-stu-id="36458-101">Get-AzureRmHDInsightPersistedScriptAction</span></span>

## <span data-ttu-id="36458-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="36458-102">SYNOPSIS</span></span>
<span data-ttu-id="36458-103">Hämtar de beständiga skript åtgärderna för ett kluster och visar dem i kronologisk ordning, eller hämtar information om en viss beständiga skript åtgärd.</span><span class="sxs-lookup"><span data-stu-id="36458-103">Gets the persisted script actions for a cluster and lists them in chronological order, or gets details for a specified persisted script action.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="36458-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="36458-104">SYNTAX</span></span>

```
Get-AzureRmHDInsightPersistedScriptAction [-ClusterName] <String> [[-Name] <String>]
 [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="36458-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="36458-105">DESCRIPTION</span></span>
<span data-ttu-id="36458-106">Cmdleten **Get-AzureRmHDInsightPersistedScriptAction** hämtar de beständiga skript åtgärderna för ett Azure HDInsight-kluster och visar dem i kronologisk ordning, eller hämtar information om en viss beständiga skript åtgärd.</span><span class="sxs-lookup"><span data-stu-id="36458-106">The **Get-AzureRmHDInsightPersistedScriptAction** cmdlet gets the persisted script actions for an Azure HDInsight cluster and lists them in chronological order, or gets details for a specified persisted script action.</span></span>

## <span data-ttu-id="36458-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="36458-107">EXAMPLES</span></span>

### <span data-ttu-id="36458-108">Exempel 1: Hämta de beständiga skript åtgärderna i ett kluster</span><span class="sxs-lookup"><span data-stu-id="36458-108">Example 1: Get the persisted script actions on a cluster</span></span>
```
PS C:\>Get-AzureRmHDInsightPersistedScriptAction -ClusterName "your-hadoop-001"
```

<span data-ttu-id="36458-109">Det här kommandot hämtar beständiga skript åtgärder i klustret som heter din-Hadoop-001.</span><span class="sxs-lookup"><span data-stu-id="36458-109">This command gets persisted script actions on the cluster named your-hadoop-001.</span></span>

## <span data-ttu-id="36458-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="36458-110">PARAMETERS</span></span>

### <span data-ttu-id="36458-111">-Kluster namn</span><span class="sxs-lookup"><span data-stu-id="36458-111">-ClusterName</span></span>
<span data-ttu-id="36458-112">Anger namnet på klustret.</span><span class="sxs-lookup"><span data-stu-id="36458-112">Specifies the name of the cluster.</span></span>

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

### <span data-ttu-id="36458-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="36458-113">-DefaultProfile</span></span>
<span data-ttu-id="36458-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="36458-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="36458-115">-Namn</span><span class="sxs-lookup"><span data-stu-id="36458-115">-Name</span></span>
<span data-ttu-id="36458-116">Anger namnet på den beständiga skript åtgärden.</span><span class="sxs-lookup"><span data-stu-id="36458-116">Specifies the name of the persisted script action.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="36458-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="36458-117">-ResourceGroupName</span></span>
<span data-ttu-id="36458-118">Anger namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="36458-118">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="36458-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="36458-119">CommonParameters</span></span>
<span data-ttu-id="36458-120">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="36458-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="36458-121">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="36458-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="36458-122">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="36458-122">INPUTS</span></span>

### <span data-ttu-id="36458-123">Ingen</span><span class="sxs-lookup"><span data-stu-id="36458-123">None</span></span>
<span data-ttu-id="36458-124">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="36458-124">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="36458-125">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="36458-125">OUTPUTS</span></span>

### <span data-ttu-id="36458-126">System. Collections. Generic. IList ' 1 [Microsoft. Azure. commands. HDInsight. Models. Management. AzureHDInsightRuntimeScriptAction]</span><span class="sxs-lookup"><span data-stu-id="36458-126">System.Collections.Generic.IList\`1[Microsoft.Azure.Commands.HDInsight.Models.Management.AzureHDInsightRuntimeScriptAction]</span></span>

## <span data-ttu-id="36458-127">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="36458-127">NOTES</span></span>

## <span data-ttu-id="36458-128">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="36458-128">RELATED LINKS</span></span>

[<span data-ttu-id="36458-129">Remove-AzureRmHDInsightPersistedScriptAction</span><span class="sxs-lookup"><span data-stu-id="36458-129">Remove-AzureRmHDInsightPersistedScriptAction</span></span>](./Remove-AzureRmHDInsightPersistedScriptAction.md)

[<span data-ttu-id="36458-130">Set-AzureRmHDInsightPersistedScriptAction</span><span class="sxs-lookup"><span data-stu-id="36458-130">Set-AzureRmHDInsightPersistedScriptAction</span></span>](./Set-AzureRmHDInsightPersistedScriptAction.md)

