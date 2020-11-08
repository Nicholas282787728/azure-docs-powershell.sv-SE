---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/disable-azhdinsightmonitoring
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Disable-AzHDInsightMonitoring.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Disable-AzHDInsightMonitoring.md
ms.openlocfilehash: 9a65a82808c78fe878ba4a61f8be01f37fc11771
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94260486"
---
# <span data-ttu-id="24abf-101">Disable-AzHDInsightMonitoring</span><span class="sxs-lookup"><span data-stu-id="24abf-101">Disable-AzHDInsightMonitoring</span></span>

## <span data-ttu-id="24abf-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="24abf-102">SYNOPSIS</span></span>
<span data-ttu-id="24abf-103">Inaktiverar övervakning i ett HDInsight-kluster och relevanta loggar slutar att flöda till arbets ytan övervakning som anges under aktivera.</span><span class="sxs-lookup"><span data-stu-id="24abf-103">Disables monitoring in a HDInsight cluster and relevant logs will stop flowing to the monitoring workspace specified during enable.</span></span>

## <span data-ttu-id="24abf-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="24abf-104">SYNTAX</span></span>

```
Disable-AzHDInsightMonitoring [-Name] <String> [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="24abf-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="24abf-105">DESCRIPTION</span></span>
<span data-ttu-id="24abf-106">Cmdleten **disable-AzHDInsightMonitoring** inaktiverar övervakning i ett Azure HDInsight-kluster.</span><span class="sxs-lookup"><span data-stu-id="24abf-106">The **Disable-AzHDInsightMonitoring** cmdlet disables monitoring in a Azure HDInsight cluster.</span></span>

## <span data-ttu-id="24abf-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="24abf-107">EXAMPLES</span></span>

### <span data-ttu-id="24abf-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="24abf-108">Example 1</span></span>
```
PS C:\> Disable-AzHDInsightMonitoring -Name testcluster

True
```

<span data-ttu-id="24abf-109">Övervakning kommer att inaktive ras i HDInsight-klustret och relevanta loggar slutar flöda till övervaknings arbets ytan.</span><span class="sxs-lookup"><span data-stu-id="24abf-109">Monitoring will be disabled on the HDInsight cluster and relevant logs will stop flowing to the monitoring workspace.</span></span>

### <span data-ttu-id="24abf-110">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="24abf-110">Example 2</span></span>
```
PS C:\> Disable-AzHDInsightMonitoring -Name testcluster -ResourceGroupName testrg

True
```

<span data-ttu-id="24abf-111">Övervakning kommer att inaktive ras i HDInsight-klustret och relevanta loggar slutar flöda till övervaknings arbets ytan.</span><span class="sxs-lookup"><span data-stu-id="24abf-111">Monitoring will be disabled on the HDInsight cluster and relevant logs will stop flowing to the monitoring workspace.</span></span>

## <span data-ttu-id="24abf-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="24abf-112">PARAMETERS</span></span>

### <span data-ttu-id="24abf-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="24abf-113">-DefaultProfile</span></span>
<span data-ttu-id="24abf-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="24abf-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="24abf-115">-Namn</span><span class="sxs-lookup"><span data-stu-id="24abf-115">-Name</span></span>
<span data-ttu-id="24abf-116">Namnet på klustret för att inaktivera övervakning.</span><span class="sxs-lookup"><span data-stu-id="24abf-116">The name of the cluster to disable Monitoring.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ClusterName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="24abf-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="24abf-117">-ResourceGroupName</span></span>
<span data-ttu-id="24abf-118">Klustrets resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="24abf-118">The resource group of the cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="24abf-119">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="24abf-119">-Confirm</span></span>
<span data-ttu-id="24abf-120">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="24abf-120">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="24abf-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="24abf-121">-WhatIf</span></span>
<span data-ttu-id="24abf-122">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="24abf-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="24abf-123">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="24abf-123">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="24abf-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="24abf-124">CommonParameters</span></span>
<span data-ttu-id="24abf-125">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="24abf-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="24abf-126">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="24abf-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="24abf-127">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="24abf-127">INPUTS</span></span>

### <span data-ttu-id="24abf-128">System. String</span><span class="sxs-lookup"><span data-stu-id="24abf-128">System.String</span></span>

## <span data-ttu-id="24abf-129">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="24abf-129">OUTPUTS</span></span>

### <span data-ttu-id="24abf-130">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="24abf-130">System.Boolean</span></span>

## <span data-ttu-id="24abf-131">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="24abf-131">NOTES</span></span>

## <span data-ttu-id="24abf-132">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="24abf-132">RELATED LINKS</span></span>
