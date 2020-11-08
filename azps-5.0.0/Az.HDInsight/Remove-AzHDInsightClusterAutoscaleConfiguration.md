---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 5B1D72ED-7A1C-4360-B256-0066CC366E28
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/remove-azhdinsightclusterautoscaleconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Remove-AzHDInsightClusterAutoscaleConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Remove-AzHDInsightClusterAutoscaleConfiguration.md
ms.openlocfilehash: 1dbfc382b935a9cc14dc42f85653a337f82ece38
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94271061"
---
# <span data-ttu-id="f55af-101">Remove-AzHDInsightClusterAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="f55af-101">Remove-AzHDInsightClusterAutoscaleConfiguration</span></span>

## <span data-ttu-id="f55af-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="f55af-102">SYNOPSIS</span></span>
<span data-ttu-id="f55af-103">Tar bort autoskalan för HDInsight-klustret.</span><span class="sxs-lookup"><span data-stu-id="f55af-103">Removes the autoscale configuration of the HDInsight cluster.</span></span>

## <span data-ttu-id="f55af-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="f55af-104">SYNTAX</span></span>

### <span data-ttu-id="f55af-105">RemoveByNameParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="f55af-105">RemoveByNameParameterSet (Default)</span></span>
```
Remove-AzHDInsightClusterAutoscaleConfiguration [[-ResourceGroupName] <String>] [-ClusterName] <String>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f55af-106">RemoveByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="f55af-106">RemoveByResourceIdParameterSet</span></span>
```
Remove-AzHDInsightClusterAutoscaleConfiguration [-ResourceId] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f55af-107">RemoveByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="f55af-107">RemoveByInputObjectParameterSet</span></span>
```
Remove-AzHDInsightClusterAutoscaleConfiguration [-InputObject] <AzureHDInsightCluster> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f55af-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="f55af-108">DESCRIPTION</span></span>
<span data-ttu-id="f55af-109">Cmdleten **Remove-AzHDInsightClusterAutoscaleConfiguration** tar bort autoskalan för HDInsight-klustret.</span><span class="sxs-lookup"><span data-stu-id="f55af-109">The **Remove-AzHDInsightClusterAutoscaleConfiguration** cmdlet removes the autoscale configuration of the HDInsight cluster.</span></span>

## <span data-ttu-id="f55af-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="f55af-110">EXAMPLES</span></span>

### <span data-ttu-id="f55af-111">Exempel 1: ta bort autoskalan för HDInsight-klustret.</span><span class="sxs-lookup"><span data-stu-id="f55af-111">Example 1: Remove the autoscale configuration of the HDInsight cluster.</span></span>
```powershell
PS C:\> $clusterResourceGroup="group"
PS C:\> $clusterName="MyCluster"
PS C:\> Remove-AzHDInsightClusterAutoscaleConfiguration -ResourceGroupName $clusterResourceGroup -ClusterName $clusterName
```

<span data-ttu-id="f55af-112">Det här kommandot tar bort autoskalans konfiguration för HDInsight-klustret.</span><span class="sxs-lookup"><span data-stu-id="f55af-112">This command removes the autoscale configuration of the HDInsight cluster.</span></span>

## <span data-ttu-id="f55af-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="f55af-113">PARAMETERS</span></span>

### <span data-ttu-id="f55af-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f55af-114">-AsJob</span></span>
<span data-ttu-id="f55af-115">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="f55af-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="f55af-116">-Kluster namn</span><span class="sxs-lookup"><span data-stu-id="f55af-116">-ClusterName</span></span>
<span data-ttu-id="f55af-117">Hämtar eller anger klustrets namn.</span><span class="sxs-lookup"><span data-stu-id="f55af-117">Gets or sets the name of the cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f55af-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f55af-118">-DefaultProfile</span></span>
<span data-ttu-id="f55af-119">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="f55af-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f55af-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f55af-120">-InputObject</span></span>
<span data-ttu-id="f55af-121">Hämtar eller anger indatavärdet.</span><span class="sxs-lookup"><span data-stu-id="f55af-121">Gets or sets the input object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightCluster
Parameter Sets: RemoveByInputObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f55af-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f55af-122">-ResourceGroupName</span></span>
<span data-ttu-id="f55af-123">Hämtar eller anger namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="f55af-123">Gets or sets the name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByNameParameterSet
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f55af-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f55af-124">-ResourceId</span></span>
<span data-ttu-id="f55af-125">Hämtar eller anger resurs-ID.</span><span class="sxs-lookup"><span data-stu-id="f55af-125">Gets or sets the resource id.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f55af-126">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="f55af-126">-Confirm</span></span>
<span data-ttu-id="f55af-127">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="f55af-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f55af-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f55af-128">-WhatIf</span></span>
<span data-ttu-id="f55af-129">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="f55af-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f55af-130">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="f55af-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f55af-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f55af-131">CommonParameters</span></span>
<span data-ttu-id="f55af-132">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f55af-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f55af-133">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f55af-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f55af-134">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="f55af-134">INPUTS</span></span>

### <span data-ttu-id="f55af-135">System. String</span><span class="sxs-lookup"><span data-stu-id="f55af-135">System.String</span></span>

### <span data-ttu-id="f55af-136">Microsoft. Azure. commands. HDInsight. Models. AzureHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="f55af-136">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightCluster</span></span>

## <span data-ttu-id="f55af-137">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="f55af-137">OUTPUTS</span></span>

### <span data-ttu-id="f55af-138">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="f55af-138">System.Boolean</span></span>

## <span data-ttu-id="f55af-139">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="f55af-139">NOTES</span></span>

## <span data-ttu-id="f55af-140">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="f55af-140">RELATED LINKS</span></span>

<span data-ttu-id="f55af-141">[New-AzHDInsightClusterAutoscaleConfiguration](./New-AzHDInsightClusterAutoscaleConfiguration.md) 
 [Set-AzHDInsightClusterAutoscaleConfiguration](./Set-AzHDInsightClusterAutoscaleConfiguration.md) 
 [Get-AzHDInsightClusterAutoscaleConfiguration](./Get-AzHDInsightClusterAutoscaleConfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="f55af-141">[New-AzHDInsightClusterAutoscaleConfiguration](./New-AzHDInsightClusterAutoscaleConfiguration.md)
[Set-AzHDInsightClusterAutoscaleConfiguration](./Set-AzHDInsightClusterAutoscaleConfiguration.md)
[Get-AzHDInsightClusterAutoscaleConfiguration](./Get-AzHDInsightClusterAutoscaleConfiguration.md)</span></span>
