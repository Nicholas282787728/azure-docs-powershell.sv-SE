---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 8CD55A33-5964-409A-BDA5-EDAE9A21E0C1
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/get-azhdinsightclusterautoscaleconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Get-AzHDInsightClusterAutoscaleConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Get-AzHDInsightClusterAutoscaleConfiguration.md
ms.openlocfilehash: 91e5a0fbb92ced1c79717aecb01d5896bb422280
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94263101"
---
# <span data-ttu-id="35e40-101">Get-AzHDInsightClusterAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="35e40-101">Get-AzHDInsightClusterAutoscaleConfiguration</span></span>

## <span data-ttu-id="35e40-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="35e40-102">SYNOPSIS</span></span>
<span data-ttu-id="35e40-103">Hämtar autoskalan för HDInsight-klustret.</span><span class="sxs-lookup"><span data-stu-id="35e40-103">Gets the autoscale configuration of HDInsight cluster.</span></span>

## <span data-ttu-id="35e40-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="35e40-104">SYNTAX</span></span>

### <span data-ttu-id="35e40-105">GetByNameParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="35e40-105">GetByNameParameterSet (Default)</span></span>
```
Get-AzHDInsightClusterAutoscaleConfiguration [[-ResourceGroupName] <String>] [-ClusterName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="35e40-106">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="35e40-106">GetByResourceIdParameterSet</span></span>
```
Get-AzHDInsightClusterAutoscaleConfiguration [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="35e40-107">GetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="35e40-107">GetByInputObjectParameterSet</span></span>
```
Get-AzHDInsightClusterAutoscaleConfiguration [-InputObject] <AzureHDInsightCluster>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="35e40-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="35e40-108">DESCRIPTION</span></span>
<span data-ttu-id="35e40-109">Cmdleten **Get-AzHDInsightClusterAutoscaleConfiguration** hämtar autoskalan för HDInsight-klustret.</span><span class="sxs-lookup"><span data-stu-id="35e40-109">The **Get-AzHDInsightClusterAutoscaleConfiguration** cmdlet gets the autoscale configuration of HDInsight cluster.</span></span>

## <span data-ttu-id="35e40-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="35e40-110">EXAMPLES</span></span>

### <span data-ttu-id="35e40-111">Exempel 1: Hämta autoskalan för HDInsight-klustret.</span><span class="sxs-lookup"><span data-stu-id="35e40-111">Example 1: Get the autoscale configuration of HDInsight cluster.</span></span>
```powershell
PS C:\> $clusterResourceGroup="group"
PS C:\> $clusterName="MyCluster"
PS C:\> Get-AzHDInsightClusterAutoscaleConfiguration -ResourceGroupName $clusterResourceGroup -ClusterName $clusterName
```

<span data-ttu-id="35e40-112">Det här kommandot hämtar autoskalans konfiguration för HDInsight-klustret.</span><span class="sxs-lookup"><span data-stu-id="35e40-112">This command gets the autoscale configuration of HDInsight cluster.</span></span>

## <span data-ttu-id="35e40-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="35e40-113">PARAMETERS</span></span>

### <span data-ttu-id="35e40-114">-Kluster namn</span><span class="sxs-lookup"><span data-stu-id="35e40-114">-ClusterName</span></span>
<span data-ttu-id="35e40-115">Hämtar eller anger klustrets namn.</span><span class="sxs-lookup"><span data-stu-id="35e40-115">Gets or sets the name of the cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="35e40-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="35e40-116">-DefaultProfile</span></span>
<span data-ttu-id="35e40-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="35e40-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="35e40-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="35e40-118">-InputObject</span></span>
<span data-ttu-id="35e40-119">Hämtar eller anger indatavärdet.</span><span class="sxs-lookup"><span data-stu-id="35e40-119">Gets or sets the input object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightCluster
Parameter Sets: GetByInputObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="35e40-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="35e40-120">-ResourceGroupName</span></span>
<span data-ttu-id="35e40-121">Hämtar eller anger namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="35e40-121">Gets or sets the name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="35e40-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="35e40-122">-ResourceId</span></span>
<span data-ttu-id="35e40-123">Hämtar eller anger resurs-ID.</span><span class="sxs-lookup"><span data-stu-id="35e40-123">Gets or sets the resource id.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="35e40-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="35e40-124">CommonParameters</span></span>
<span data-ttu-id="35e40-125">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="35e40-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="35e40-126">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="35e40-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="35e40-127">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="35e40-127">INPUTS</span></span>

### <span data-ttu-id="35e40-128">System. String</span><span class="sxs-lookup"><span data-stu-id="35e40-128">System.String</span></span>

### <span data-ttu-id="35e40-129">Microsoft. Azure. commands. HDInsight. Models. AzureHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="35e40-129">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightCluster</span></span>

## <span data-ttu-id="35e40-130">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="35e40-130">OUTPUTS</span></span>

### <span data-ttu-id="35e40-131">Microsoft. Azure. commands. HDInsight. Models. AzureHDInsightAutoscale</span><span class="sxs-lookup"><span data-stu-id="35e40-131">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightAutoscale</span></span>

## <span data-ttu-id="35e40-132">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="35e40-132">NOTES</span></span>

## <span data-ttu-id="35e40-133">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="35e40-133">RELATED LINKS</span></span>

<span data-ttu-id="35e40-134">[New-AzHDInsightClusterAutoscaleConfiguration](./New-AzHDInsightClusterAutoscaleConfiguration.md) 
 [Set-AzHDInsightClusterAutoscaleConfiguration](./Set-AzHDInsightClusterAutoscaleConfiguration.md) 
 [Remove-AzHDInsightClusterAutoscaleConfiguration](./Remove-AzHDInsightClusterAutoscaleConfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="35e40-134">[New-AzHDInsightClusterAutoscaleConfiguration](./New-AzHDInsightClusterAutoscaleConfiguration.md)
[Set-AzHDInsightClusterAutoscaleConfiguration](./Set-AzHDInsightClusterAutoscaleConfiguration.md)
[Remove-AzHDInsightClusterAutoscaleConfiguration](./Remove-AzHDInsightClusterAutoscaleConfiguration.md)</span></span>
