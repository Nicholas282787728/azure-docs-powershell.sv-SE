---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/enable-azhdinsightmonitoring
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Enable-AzHDInsightMonitoring.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Enable-AzHDInsightMonitoring.md
ms.openlocfilehash: 7ec91d5ab23322185c2920655410b39e2d1a1dce
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94260487"
---
# <span data-ttu-id="fc136-101">Enable-AzHDInsightMonitoring</span><span class="sxs-lookup"><span data-stu-id="fc136-101">Enable-AzHDInsightMonitoring</span></span>

## <span data-ttu-id="fc136-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="fc136-102">SYNOPSIS</span></span>
<span data-ttu-id="fc136-103">Aktiverar övervakning i ett HDInsight-kluster och relevanta loggar skickas till övervaknings arbets ytan som anges vid aktivering.</span><span class="sxs-lookup"><span data-stu-id="fc136-103">Enables monitoring in a HDInsight cluster and relevant logs will be sent to the monitoring workspace specified during enable.</span></span>

## <span data-ttu-id="fc136-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="fc136-104">SYNTAX</span></span>

```
Enable-AzHDInsightMonitoring [-Name] <String> [-WorkspaceId] <String> [-PrimaryKey] <String>
 [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="fc136-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="fc136-105">DESCRIPTION</span></span>
<span data-ttu-id="fc136-106">Cmdleten **Enable-AzHDInsightMonitoring** aktiverar övervakning i ett Azure HDInsight-kluster.</span><span class="sxs-lookup"><span data-stu-id="fc136-106">The **Enable-AzHDInsightMonitoring** cmdlet enables monitoring in a Azure HDInsight cluster.</span></span>

## <span data-ttu-id="fc136-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="fc136-107">EXAMPLES</span></span>

### <span data-ttu-id="fc136-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="fc136-108">Example 1</span></span>
```
PS C:\> Enable-AzHDInsightMonitoring -Name testcluster -WorkspaceId 1d364e89-bb71-4503-aa3d-a23535aea7bd -PrimaryKey <key for workspace 1d364e89-bb71-4503-aa3d-a23535aea7bd>

True
```

<span data-ttu-id="fc136-109">Övervakning aktive ras i HDInsight-klustret och relevanta loggar skickas till övervaknings arbets ytan med ID 1d364e89-bb71-4503-aa3d-a23535aea7bd</span><span class="sxs-lookup"><span data-stu-id="fc136-109">Monitoring will be enabled on the HDInsight cluster and relevant logs will be sent to the monitoring workspace with id 1d364e89-bb71-4503-aa3d-a23535aea7bd</span></span>

### <span data-ttu-id="fc136-110">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="fc136-110">Example 2</span></span>
```
PS C:\> Enable-AzHDInsightMonitoring -Name testcluster -ResourceGroupName testrg -WorkspaceId 1d364e89-bb71-4503-aa3d-a23535aea7bd -PrimaryKey <key for workspace 1d364e89-bb71-4503-aa3d-a23535aea7bd>

True
```

<span data-ttu-id="fc136-111">Övervakning aktive ras i HDInsight-klustret och relevanta loggar skickas till övervaknings arbets ytan med ID 1d364e89-bb71-4503-aa3d-a23535aea7bd</span><span class="sxs-lookup"><span data-stu-id="fc136-111">Monitoring will be enabled on the HDInsight cluster and relevant logs will be sent to the monitoring workspace with id 1d364e89-bb71-4503-aa3d-a23535aea7bd</span></span>

## <span data-ttu-id="fc136-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="fc136-112">PARAMETERS</span></span>

### <span data-ttu-id="fc136-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fc136-113">-DefaultProfile</span></span>
<span data-ttu-id="fc136-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="fc136-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="fc136-115">-Namn</span><span class="sxs-lookup"><span data-stu-id="fc136-115">-Name</span></span>
<span data-ttu-id="fc136-116">Namnet på klustret för att aktivera övervakning.</span><span class="sxs-lookup"><span data-stu-id="fc136-116">The name of the cluster to enable monitoring.</span></span>

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

### <span data-ttu-id="fc136-117">-PrimaryKey</span><span class="sxs-lookup"><span data-stu-id="fc136-117">-PrimaryKey</span></span>
<span data-ttu-id="fc136-118">Primärt för arbets ytan övervakning.</span><span class="sxs-lookup"><span data-stu-id="fc136-118">The primary key of the monitoring workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fc136-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fc136-119">-ResourceGroupName</span></span>
<span data-ttu-id="fc136-120">Klustrets resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="fc136-120">The resource group of the cluster.</span></span>

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

### <span data-ttu-id="fc136-121">-WorkspaceId</span><span class="sxs-lookup"><span data-stu-id="fc136-121">-WorkspaceId</span></span>
<span data-ttu-id="fc136-122">ID för övervaknings arbets ytan.</span><span class="sxs-lookup"><span data-stu-id="fc136-122">The id of the monitoring workspace.</span></span>

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

### <span data-ttu-id="fc136-123">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="fc136-123">-Confirm</span></span>
<span data-ttu-id="fc136-124">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="fc136-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fc136-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fc136-125">-WhatIf</span></span>
<span data-ttu-id="fc136-126">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="fc136-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="fc136-127">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="fc136-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fc136-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fc136-128">CommonParameters</span></span>
<span data-ttu-id="fc136-129">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fc136-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fc136-130">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="fc136-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fc136-131">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="fc136-131">INPUTS</span></span>

### <span data-ttu-id="fc136-132">System. String</span><span class="sxs-lookup"><span data-stu-id="fc136-132">System.String</span></span>

## <span data-ttu-id="fc136-133">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="fc136-133">OUTPUTS</span></span>

### <span data-ttu-id="fc136-134">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="fc136-134">System.Boolean</span></span>

## <span data-ttu-id="fc136-135">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="fc136-135">NOTES</span></span>

## <span data-ttu-id="fc136-136">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="fc136-136">RELATED LINKS</span></span>
