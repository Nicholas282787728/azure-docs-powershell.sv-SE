---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/restart-azhdinsighthost
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Restart-AzHDInsightHost.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Restart-AzHDInsightHost.md
ms.openlocfilehash: 4e0b5fda29696fb45515c3b478b9dc29ff67263e
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98387999"
---
# <span data-ttu-id="024d8-101">Restart-AzHDInsightHost</span><span class="sxs-lookup"><span data-stu-id="024d8-101">Restart-AzHDInsightHost</span></span>

## <span data-ttu-id="024d8-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="024d8-102">SYNOPSIS</span></span>
<span data-ttu-id="024d8-103">Startar om de specifika värderna för HDInsight-klustret.</span><span class="sxs-lookup"><span data-stu-id="024d8-103">Restarts the specific hosts of HDInsight cluster.</span></span>

## <span data-ttu-id="024d8-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="024d8-104">SYNTAX</span></span>

### <span data-ttu-id="024d8-105">SetByNameParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="024d8-105">SetByNameParameterSet (Default)</span></span>
```
Restart-AzHDInsightHost [[-ResourceGroupName] <String>] [-ClusterName] <String> [-Name] <String[]> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="024d8-106">SetByAzureHDInsightHostInfoParameterSet</span><span class="sxs-lookup"><span data-stu-id="024d8-106">SetByAzureHDInsightHostInfoParameterSet</span></span>
```
Restart-AzHDInsightHost [[-ResourceGroupName] <String>] [-ClusterName] <String>
 [-AzureHDInsightHostInfo] <AzureHDInsightHostInfo[]> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="024d8-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="024d8-107">DESCRIPTION</span></span>
<span data-ttu-id="024d8-108">Denna **omstart – AzHDInsightHost** cmdlet starta om de specifika värdarna för HDInsight-klustret.</span><span class="sxs-lookup"><span data-stu-id="024d8-108">This **Restart-AzHDInsightHost** cmdlet restart the specific hosts of HDInsight cluster.</span></span>

## <span data-ttu-id="024d8-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="024d8-109">EXAMPLES</span></span>

### <span data-ttu-id="024d8-110">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="024d8-110">Example 1</span></span>
```powershell
PS C:\># Cluster info
PS C:\> $clusterName = "your-hadoop-001"
PS C:\> Restart-AzHDInsightHost -ClusterName $clusterName -Name wn0, wn1
```

<span data-ttu-id="024d8-111">Det här kommandot startar om två värdar i klustret: worknode1, worknode2.</span><span class="sxs-lookup"><span data-stu-id="024d8-111">This command restarts two hosts of the cluster: worknode1, worknode2.</span></span>

### <span data-ttu-id="024d8-112">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="024d8-112">Example 2</span></span>
```powershell
PS C:\># Cluster info
PS C:\> $clusterName = "your-hadoop-001"
PS C:\> $worknode1= Get-AzHDInsightHost -ClusterName $clusterName | Where-Object {$_.Name -like "wn1*"}
PS C:\> $worknode1 | Restart-AzHDInsightHost -ClusterName $clusterName
```

<span data-ttu-id="024d8-113">Det här kommandot visar hur du samarbetar med cmdlet "Get-AzHDInsightHost".</span><span class="sxs-lookup"><span data-stu-id="024d8-113">This command shows how to cooperate with the cmdlet 'Get-AzHDInsightHost'.</span></span>

## <span data-ttu-id="024d8-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="024d8-114">PARAMETERS</span></span>

### <span data-ttu-id="024d8-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="024d8-115">-AsJob</span></span>
<span data-ttu-id="024d8-116">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="024d8-116">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="024d8-117">-AzureHDInsightHostInfo</span><span class="sxs-lookup"><span data-stu-id="024d8-117">-AzureHDInsightHostInfo</span></span>
<span data-ttu-id="024d8-118">Hämtar eller anger namnet på värden.</span><span class="sxs-lookup"><span data-stu-id="024d8-118">Gets or sets the name of the host.</span></span>

```yaml
Type: Microsoft.Azure.Commands.HDInsight.Models.Management.AzureHDInsightHostInfo[]
Parameter Sets: SetByAzureHDInsightHostInfoParameterSet
Aliases: Host

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="024d8-119">-Kluster namn</span><span class="sxs-lookup"><span data-stu-id="024d8-119">-ClusterName</span></span>
<span data-ttu-id="024d8-120">Hämtar eller anger klustrets namn.</span><span class="sxs-lookup"><span data-stu-id="024d8-120">Gets or sets the name of the cluster.</span></span>

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

### <span data-ttu-id="024d8-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="024d8-121">-DefaultProfile</span></span>
<span data-ttu-id="024d8-122">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="024d8-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="024d8-123">-Namn</span><span class="sxs-lookup"><span data-stu-id="024d8-123">-Name</span></span>
<span data-ttu-id="024d8-124">Hämtar eller anger namnet på värden.</span><span class="sxs-lookup"><span data-stu-id="024d8-124">Gets or sets the name of the host.</span></span>

```yaml
Type: System.String[]
Parameter Sets: SetByNameParameterSet
Aliases: HostName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="024d8-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="024d8-125">-PassThru</span></span>
<span data-ttu-id="024d8-126">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="024d8-126">{{ Fill PassThru Description }}</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="024d8-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="024d8-127">-ResourceGroupName</span></span>
<span data-ttu-id="024d8-128">Hämtar eller anger namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="024d8-128">Gets or sets the name of the resource group.</span></span>

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

### <span data-ttu-id="024d8-129">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="024d8-129">-Confirm</span></span>
<span data-ttu-id="024d8-130">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="024d8-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="024d8-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="024d8-131">-WhatIf</span></span>
<span data-ttu-id="024d8-132">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="024d8-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="024d8-133">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="024d8-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="024d8-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="024d8-134">CommonParameters</span></span>
<span data-ttu-id="024d8-135">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="024d8-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="024d8-136">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="024d8-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="024d8-137">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="024d8-137">INPUTS</span></span>

### <span data-ttu-id="024d8-138">System. string []</span><span class="sxs-lookup"><span data-stu-id="024d8-138">System.String[]</span></span>

### <span data-ttu-id="024d8-139">Microsoft. Azure. commands. HDInsight. Models. Management. AzureHDInsightHostInfo []</span><span class="sxs-lookup"><span data-stu-id="024d8-139">Microsoft.Azure.Commands.HDInsight.Models.Management.AzureHDInsightHostInfo[]</span></span>

## <span data-ttu-id="024d8-140">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="024d8-140">OUTPUTS</span></span>

### <span data-ttu-id="024d8-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="024d8-141">System.Boolean</span></span>

## <span data-ttu-id="024d8-142">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="024d8-142">NOTES</span></span>

## <span data-ttu-id="024d8-143">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="024d8-143">RELATED LINKS</span></span>
