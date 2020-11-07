---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: FA154E07-EA26-4688-986E-C53C3A9E4F06
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/get-azhdinsightcluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Get-AzHDInsightCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Get-AzHDInsightCluster.md
ms.openlocfilehash: 8b15a93ee576af683cb2ebfffa621937a2ebba78
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93744096"
---
# <span data-ttu-id="3dd34-101">Get-AzHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="3dd34-101">Get-AzHDInsightCluster</span></span>

## <span data-ttu-id="3dd34-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="3dd34-102">SYNOPSIS</span></span>
<span data-ttu-id="3dd34-103">Hämtar och visar alla Azure HDInsight-kluster som är kopplade till det aktuella abonnemanget eller en angiven resurs grupp, eller hämtar ett specifikt kluster.</span><span class="sxs-lookup"><span data-stu-id="3dd34-103">Gets and lists all of the Azure HDInsight clusters associated with the current subscription or a specified resource group, or retrieves a specific cluster.</span></span>

## <span data-ttu-id="3dd34-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="3dd34-104">SYNTAX</span></span>

```
Get-AzHDInsightCluster [[-ResourceGroupName] <String>] [[-ClusterName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3dd34-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="3dd34-105">DESCRIPTION</span></span>
<span data-ttu-id="3dd34-106">Cmdleten **Get-AzHDInsightCluster** visar Azure HDInsight-tjänstens kluster för det aktuella abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="3dd34-106">The **Get-AzHDInsightCluster** cmdlet lists the Azure HDInsight service clusters for the current subscription.</span></span>
<span data-ttu-id="3dd34-107">Använd parametern *ClusterName* Clustered för att få information om ett visst kluster.</span><span class="sxs-lookup"><span data-stu-id="3dd34-107">Use the *ClusterName* parameter to get details for a specific cluster.</span></span>

## <span data-ttu-id="3dd34-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="3dd34-108">EXAMPLES</span></span>

### <span data-ttu-id="3dd34-109">Exempel 1: lista alla Azure HDInsight-kluster</span><span class="sxs-lookup"><span data-stu-id="3dd34-109">Example 1: List all Azure HDInsight clusters</span></span>
```
PS C:\>Get-AzHDInsightCluster
```

<span data-ttu-id="3dd34-110">Det här kommandot visar alla Azure HDInsight-kluster.</span><span class="sxs-lookup"><span data-stu-id="3dd34-110">This command lists all the Azure HDInsight clusters.</span></span>

## <span data-ttu-id="3dd34-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="3dd34-111">PARAMETERS</span></span>

### <span data-ttu-id="3dd34-112">-Kluster namn</span><span class="sxs-lookup"><span data-stu-id="3dd34-112">-ClusterName</span></span>
<span data-ttu-id="3dd34-113">Anger namnet på klustret.</span><span class="sxs-lookup"><span data-stu-id="3dd34-113">Specifies the name of the cluster.</span></span>

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

### <span data-ttu-id="3dd34-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3dd34-114">-DefaultProfile</span></span>
<span data-ttu-id="3dd34-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="3dd34-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="3dd34-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3dd34-116">-ResourceGroupName</span></span>
<span data-ttu-id="3dd34-117">Anger namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="3dd34-117">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="3dd34-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3dd34-118">CommonParameters</span></span>
<span data-ttu-id="3dd34-119">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3dd34-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3dd34-120">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3dd34-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3dd34-121">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="3dd34-121">INPUTS</span></span>

### <span data-ttu-id="3dd34-122">Ingen</span><span class="sxs-lookup"><span data-stu-id="3dd34-122">None</span></span>

## <span data-ttu-id="3dd34-123">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="3dd34-123">OUTPUTS</span></span>

### <span data-ttu-id="3dd34-124">Microsoft. Azure. commands. HDInsight. Models. AzureHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="3dd34-124">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightCluster</span></span>

## <span data-ttu-id="3dd34-125">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="3dd34-125">NOTES</span></span>

## <span data-ttu-id="3dd34-126">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="3dd34-126">RELATED LINKS</span></span>

[<span data-ttu-id="3dd34-127">Remove-AzHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="3dd34-127">Remove-AzHDInsightCluster</span></span>](./Remove-AzHDInsightCluster.md)

[<span data-ttu-id="3dd34-128">Use-AzHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="3dd34-128">Use-AzHDInsightCluster</span></span>](./Use-AzHDInsightCluster.md)

