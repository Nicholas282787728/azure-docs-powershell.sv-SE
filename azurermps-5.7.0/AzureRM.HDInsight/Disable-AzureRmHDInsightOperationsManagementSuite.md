---
external help file: Microsoft.Azure.Commands.HDInsight.dll-Help.xml
Module Name: AzureRM.HDInsight
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.hdinsight/disable-azurermhdinsightoperationsmanagementsuite
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Disable-AzureRmHDInsightOperationsManagementSuite.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Disable-AzureRmHDInsightOperationsManagementSuite.md
ms.openlocfilehash: c29c27ab7b2212670abf7e100678cdfdd5beb6cb
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93579543"
---
# <span data-ttu-id="f083f-101">Disable-AzureRmHDInsightOperationsManagementSuite</span><span class="sxs-lookup"><span data-stu-id="f083f-101">Disable-AzureRmHDInsightOperationsManagementSuite</span></span>

## <span data-ttu-id="f083f-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="f083f-102">SYNOPSIS</span></span>
<span data-ttu-id="f083f-103">Inaktiverar Operations Management Suite (OMS) i ett HDInsight-kluster och relevanta loggar slutar flöda till den OMS-arbetsyta som anges vid aktivering.</span><span class="sxs-lookup"><span data-stu-id="f083f-103">Disables Operations Management Suite (OMS) in a HDInsight cluster and relevant logs will stop flowing to the OMS workspace specified during enable.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f083f-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="f083f-104">SYNTAX</span></span>

```
Disable-AzureRmHDInsightOperationsManagementSuite [-Name] <String> [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f083f-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="f083f-105">DESCRIPTION</span></span>
<span data-ttu-id="f083f-106">Cmdleten **disable-AzureRmHDInsightOperationsManagementSuite** inaktiverar Operations Management Suite (OMS) i ett Azure HDInsight-kluster.</span><span class="sxs-lookup"><span data-stu-id="f083f-106">The **Disable-AzureRmHDInsightOperationsManagementSuite** cmdlet disables Operations Management Suite (OMS) in a Azure HDInsight cluster.</span></span>

## <span data-ttu-id="f083f-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="f083f-107">EXAMPLES</span></span>

### <span data-ttu-id="f083f-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="f083f-108">Example 1</span></span>
```
PS C:\> Disable-AzureRmHDInsightOMS -Name testcluster

ErrorInfo  :

State      : Succeeded

RequestId  : 1417ad86-d055-48cd-9d68-a5c19a212a3a

StatusCode : OK
```

<span data-ttu-id="f083f-109">Operations Management Suite (OMS) inaktive ras i HDInsight-klustret och relevanta loggar slutar flöda till OMS-arbetsytan.</span><span class="sxs-lookup"><span data-stu-id="f083f-109">Operations Management Suite (OMS) will be disabled on the HDInsight cluster and relevant logs will stop flowing to the OMS workspace.</span></span>

### <span data-ttu-id="f083f-110">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="f083f-110">Example 2</span></span>
```
PS C:\> Disable-AzureRmHDInsightOMS -Name testcluster -ResourceGroupName testrg

ErrorInfo  :

State      : Succeeded

RequestId  : 1417ad86-d055-48cd-9d68-a5c19a212a3a

StatusCode : OK
```

<span data-ttu-id="f083f-111">Operations Management Suite (OMS) inaktive ras i HDInsight-klustret och relevanta loggar slutar flöda till OMS-arbetsytan.</span><span class="sxs-lookup"><span data-stu-id="f083f-111">Operations Management Suite (OMS) will be disabled on the HDInsight cluster and relevant logs will stop flowing to the OMS workspace.</span></span>

## <span data-ttu-id="f083f-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="f083f-112">PARAMETERS</span></span>

### <span data-ttu-id="f083f-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f083f-113">-DefaultProfile</span></span>
<span data-ttu-id="f083f-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="f083f-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f083f-115">-Namn</span><span class="sxs-lookup"><span data-stu-id="f083f-115">-Name</span></span>
<span data-ttu-id="f083f-116">Namnet på klustret för att avaktivera Operations Management Suite (OMS).</span><span class="sxs-lookup"><span data-stu-id="f083f-116">The name of the cluster to disable Operations Management Suite(OMS).</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ClusterName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f083f-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f083f-117">-ResourceGroupName</span></span>
<span data-ttu-id="f083f-118">Klustrets resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="f083f-118">The resource group of the cluster.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f083f-119">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="f083f-119">-Confirm</span></span>
<span data-ttu-id="f083f-120">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="f083f-120">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f083f-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f083f-121">-WhatIf</span></span>
<span data-ttu-id="f083f-122">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="f083f-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="f083f-123">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="f083f-123">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f083f-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f083f-124">CommonParameters</span></span>
<span data-ttu-id="f083f-125">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f083f-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f083f-126">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f083f-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f083f-127">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="f083f-127">INPUTS</span></span>

### <span data-ttu-id="f083f-128">System. String</span><span class="sxs-lookup"><span data-stu-id="f083f-128">System.String</span></span>

## <span data-ttu-id="f083f-129">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="f083f-129">OUTPUTS</span></span>

### <span data-ttu-id="f083f-130">Microsoft. Azure. Management. HDInsight. Models. OperationResource</span><span class="sxs-lookup"><span data-stu-id="f083f-130">Microsoft.Azure.Management.HDInsight.Models.OperationResource</span></span>

## <span data-ttu-id="f083f-131">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="f083f-131">NOTES</span></span>

## <span data-ttu-id="f083f-132">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="f083f-132">RELATED LINKS</span></span>

