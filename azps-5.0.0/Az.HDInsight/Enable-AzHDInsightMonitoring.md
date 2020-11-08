---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/enable-azhdinsightmonitoring
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Enable-AzHDInsightMonitoring.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Enable-AzHDInsightMonitoring.md
ms.openlocfilehash: 7ec91d5ab23322185c2920655410b39e2d1a1dce
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94263105"
---
# <span data-ttu-id="64748-101">Enable-AzHDInsightMonitoring</span><span class="sxs-lookup"><span data-stu-id="64748-101">Enable-AzHDInsightMonitoring</span></span>

## <span data-ttu-id="64748-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="64748-102">SYNOPSIS</span></span>
<span data-ttu-id="64748-103">Aktiverar övervakning i ett HDInsight-kluster och relevanta loggar skickas till övervaknings arbets ytan som anges vid aktivering.</span><span class="sxs-lookup"><span data-stu-id="64748-103">Enables monitoring in a HDInsight cluster and relevant logs will be sent to the monitoring workspace specified during enable.</span></span>

## <span data-ttu-id="64748-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="64748-104">SYNTAX</span></span>

```
Enable-AzHDInsightMonitoring [-Name] <String> [-WorkspaceId] <String> [-PrimaryKey] <String>
 [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="64748-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="64748-105">DESCRIPTION</span></span>
<span data-ttu-id="64748-106">Cmdleten **Enable-AzHDInsightMonitoring** aktiverar övervakning i ett Azure HDInsight-kluster.</span><span class="sxs-lookup"><span data-stu-id="64748-106">The **Enable-AzHDInsightMonitoring** cmdlet enables monitoring in a Azure HDInsight cluster.</span></span>

## <span data-ttu-id="64748-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="64748-107">EXAMPLES</span></span>

### <span data-ttu-id="64748-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="64748-108">Example 1</span></span>
```
PS C:\> Enable-AzHDInsightMonitoring -Name testcluster -WorkspaceId 1d364e89-bb71-4503-aa3d-a23535aea7bd -PrimaryKey <key for workspace 1d364e89-bb71-4503-aa3d-a23535aea7bd>

True
```

<span data-ttu-id="64748-109">Övervakning aktive ras i HDInsight-klustret och relevanta loggar skickas till övervaknings arbets ytan med ID 1d364e89-bb71-4503-aa3d-a23535aea7bd</span><span class="sxs-lookup"><span data-stu-id="64748-109">Monitoring will be enabled on the HDInsight cluster and relevant logs will be sent to the monitoring workspace with id 1d364e89-bb71-4503-aa3d-a23535aea7bd</span></span>

### <span data-ttu-id="64748-110">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="64748-110">Example 2</span></span>
```
PS C:\> Enable-AzHDInsightMonitoring -Name testcluster -ResourceGroupName testrg -WorkspaceId 1d364e89-bb71-4503-aa3d-a23535aea7bd -PrimaryKey <key for workspace 1d364e89-bb71-4503-aa3d-a23535aea7bd>

True
```

<span data-ttu-id="64748-111">Övervakning aktive ras i HDInsight-klustret och relevanta loggar skickas till övervaknings arbets ytan med ID 1d364e89-bb71-4503-aa3d-a23535aea7bd</span><span class="sxs-lookup"><span data-stu-id="64748-111">Monitoring will be enabled on the HDInsight cluster and relevant logs will be sent to the monitoring workspace with id 1d364e89-bb71-4503-aa3d-a23535aea7bd</span></span>

## <span data-ttu-id="64748-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="64748-112">PARAMETERS</span></span>

### <span data-ttu-id="64748-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="64748-113">-DefaultProfile</span></span>
<span data-ttu-id="64748-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="64748-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="64748-115">-Namn</span><span class="sxs-lookup"><span data-stu-id="64748-115">-Name</span></span>
<span data-ttu-id="64748-116">Namnet på klustret för att aktivera övervakning.</span><span class="sxs-lookup"><span data-stu-id="64748-116">The name of the cluster to enable monitoring.</span></span>

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

### <span data-ttu-id="64748-117">-PrimaryKey</span><span class="sxs-lookup"><span data-stu-id="64748-117">-PrimaryKey</span></span>
<span data-ttu-id="64748-118">Primärt för arbets ytan övervakning.</span><span class="sxs-lookup"><span data-stu-id="64748-118">The primary key of the monitoring workspace.</span></span>

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

### <span data-ttu-id="64748-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="64748-119">-ResourceGroupName</span></span>
<span data-ttu-id="64748-120">Klustrets resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="64748-120">The resource group of the cluster.</span></span>

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

### <span data-ttu-id="64748-121">-WorkspaceId</span><span class="sxs-lookup"><span data-stu-id="64748-121">-WorkspaceId</span></span>
<span data-ttu-id="64748-122">ID för övervaknings arbets ytan.</span><span class="sxs-lookup"><span data-stu-id="64748-122">The id of the monitoring workspace.</span></span>

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

### <span data-ttu-id="64748-123">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="64748-123">-Confirm</span></span>
<span data-ttu-id="64748-124">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="64748-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="64748-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="64748-125">-WhatIf</span></span>
<span data-ttu-id="64748-126">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="64748-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="64748-127">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="64748-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="64748-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="64748-128">CommonParameters</span></span>
<span data-ttu-id="64748-129">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="64748-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="64748-130">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="64748-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="64748-131">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="64748-131">INPUTS</span></span>

### <span data-ttu-id="64748-132">System. String</span><span class="sxs-lookup"><span data-stu-id="64748-132">System.String</span></span>

## <span data-ttu-id="64748-133">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="64748-133">OUTPUTS</span></span>

### <span data-ttu-id="64748-134">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="64748-134">System.Boolean</span></span>

## <span data-ttu-id="64748-135">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="64748-135">NOTES</span></span>

## <span data-ttu-id="64748-136">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="64748-136">RELATED LINKS</span></span>
