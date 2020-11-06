---
external help file: Microsoft.Azure.Commands.HDInsight.dll-Help.xml
Module Name: AzureRM.HDInsight
ms.assetid: FA154E07-EA26-4688-986E-C53C3A9E4F06
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Get-AzureRmHDInsightCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Get-AzureRmHDInsightCluster.md
ms.openlocfilehash: 81f25eeb8d0e6b704c4ee6ef71cd2aebcf3624ae
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93580612"
---
# <span data-ttu-id="88aa4-101">Get-AzureRmHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="88aa4-101">Get-AzureRmHDInsightCluster</span></span>

## <span data-ttu-id="88aa4-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="88aa4-102">SYNOPSIS</span></span>
<span data-ttu-id="88aa4-103">Hämtar och visar alla Azure HDInsight-kluster som är kopplade till det aktuella abonnemanget eller en angiven resurs grupp, eller hämtar ett specifikt kluster.</span><span class="sxs-lookup"><span data-stu-id="88aa4-103">Gets and lists all of the Azure HDInsight clusters associated with the current subscription or a specified resource group, or retrieves a specific cluster.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="88aa4-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="88aa4-104">SYNTAX</span></span>

```
Get-AzureRmHDInsightCluster [[-ResourceGroupName] <String>] [[-ClusterName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="88aa4-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="88aa4-105">DESCRIPTION</span></span>
<span data-ttu-id="88aa4-106">Cmdleten **Get-AzureRmHDInsightCluster** visar Azure HDInsight-tjänstens kluster för det aktuella abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="88aa4-106">The **Get-AzureRmHDInsightCluster** cmdlet lists the Azure HDInsight service clusters for the current subscription.</span></span>
<span data-ttu-id="88aa4-107">Använd parametern *ClusterName* Clustered för att få information om ett visst kluster.</span><span class="sxs-lookup"><span data-stu-id="88aa4-107">Use the *ClusterName* parameter to get details for a specific cluster.</span></span>

## <span data-ttu-id="88aa4-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="88aa4-108">EXAMPLES</span></span>

### <span data-ttu-id="88aa4-109">Exempel 1: lista alla Azure HDInsight-kluster</span><span class="sxs-lookup"><span data-stu-id="88aa4-109">Example 1: List all Azure HDInsight clusters</span></span>
```
PS C:\>Get-AzureRmHDInsightCluster
```

<span data-ttu-id="88aa4-110">Det här kommandot visar alla Azure HDInsight-kluster.</span><span class="sxs-lookup"><span data-stu-id="88aa4-110">This command lists all the Azure HDInsight clusters.</span></span>

## <span data-ttu-id="88aa4-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="88aa4-111">PARAMETERS</span></span>

### <span data-ttu-id="88aa4-112">-Kluster namn</span><span class="sxs-lookup"><span data-stu-id="88aa4-112">-ClusterName</span></span>
<span data-ttu-id="88aa4-113">Anger namnet på klustret.</span><span class="sxs-lookup"><span data-stu-id="88aa4-113">Specifies the name of the cluster.</span></span>

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

### <span data-ttu-id="88aa4-114">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="88aa4-114">-ResourceGroupName</span></span>
<span data-ttu-id="88aa4-115">Anger namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="88aa4-115">Specifies the name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="88aa4-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="88aa4-116">-DefaultProfile</span></span>
<span data-ttu-id="88aa4-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="88aa4-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="88aa4-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="88aa4-118">CommonParameters</span></span>
<span data-ttu-id="88aa4-119">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="88aa4-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="88aa4-120">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="88aa4-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="88aa4-121">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="88aa4-121">INPUTS</span></span>

## <span data-ttu-id="88aa4-122">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="88aa4-122">OUTPUTS</span></span>

### <span data-ttu-id="88aa4-123">System. Collections. Generic. list ' 1 [Microsoft. Azure. commands. HDInsight. Models. AzureHDInsightCluster]</span><span class="sxs-lookup"><span data-stu-id="88aa4-123">System.Collections.Generic.List\`1[Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightCluster]</span></span>

## <span data-ttu-id="88aa4-124">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="88aa4-124">NOTES</span></span>

## <span data-ttu-id="88aa4-125">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="88aa4-125">RELATED LINKS</span></span>

[<span data-ttu-id="88aa4-126">Remove-AzureRmHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="88aa4-126">Remove-AzureRmHDInsightCluster</span></span>](./Remove-AzureRmHDInsightCluster.md)

[<span data-ttu-id="88aa4-127">Use-AzureRmHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="88aa4-127">Use-AzureRmHDInsightCluster</span></span>](./Use-AzureRmHDInsightCluster.md)


