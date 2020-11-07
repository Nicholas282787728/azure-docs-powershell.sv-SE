---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/set-azhdinsightgatewaycredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Set-AzHDInsightGatewayCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Set-AzHDInsightGatewayCredential.md
ms.openlocfilehash: 045b0db296a9c3bde4332ce755c055d1e8616738
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93744057"
---
# <span data-ttu-id="49bb9-101">Set-AzHDInsightGatewayCredential</span><span class="sxs-lookup"><span data-stu-id="49bb9-101">Set-AzHDInsightGatewayCredential</span></span>

## <span data-ttu-id="49bb9-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="49bb9-102">SYNOPSIS</span></span>
<span data-ttu-id="49bb9-103">Anger HTTP-autentiseringsuppgifter för gateway för ett Azure HDInsight-kluster.</span><span class="sxs-lookup"><span data-stu-id="49bb9-103">Sets the gateway HTTP credentials of an Azure HDInsight cluster.</span></span>

## <span data-ttu-id="49bb9-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="49bb9-104">SYNTAX</span></span>

### <span data-ttu-id="49bb9-105">SetByNameParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="49bb9-105">SetByNameParameterSet (Default)</span></span>
```
Set-AzHDInsightGatewayCredential -Name <String> [-HttpCredential] <PSCredential> [-ResourceGroupName <String>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="49bb9-106">SetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="49bb9-106">SetByInputObjectParameterSet</span></span>
```
Set-AzHDInsightGatewayCredential [-HttpCredential] <PSCredential> [-ResourceGroupName <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] -InputObject <AzureHDInsightCluster> [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="49bb9-107">SetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="49bb9-107">SetByResourceIdParameterSet</span></span>
```
Set-AzHDInsightGatewayCredential [-HttpCredential] <PSCredential> [-ResourceGroupName <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] -ResourceId <String> [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="49bb9-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="49bb9-108">DESCRIPTION</span></span>
<span data-ttu-id="49bb9-109">Cmdleten **set-AzHDInsightGatewayCredential** anger Gateway-autentiseringsuppgifter för ett Azure HDInsight-kluster.</span><span class="sxs-lookup"><span data-stu-id="49bb9-109">The **Set-AzHDInsightGatewayCredential** cmdlet sets gateway credential of an Azure HDInsight cluster.</span></span>

## <span data-ttu-id="49bb9-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="49bb9-110">EXAMPLES</span></span>

### <span data-ttu-id="49bb9-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="49bb9-111">Example 1</span></span>
```powershell
PS C:\># Cluster info
PS C:\> $clusterName = "your-hadoop-001"
PS C:\> $clusterCreds = Get-Credential

PS C:\> Set-AzHDInsightGatewayCredential `
            -ClusterName $clusterName `
            -HttpCredential $clusterCreds
```

<span data-ttu-id="49bb9-112">Det här kommandot anger Gateway-autentiseringsuppgifter för klustret som heter ditt-Hadoop-001 efter namn.</span><span class="sxs-lookup"><span data-stu-id="49bb9-112">This command sets gateway credential of the cluster named your-hadoop-001 by name parameter set.</span></span>

### <span data-ttu-id="49bb9-113">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="49bb9-113">Example 2</span></span>
```powershell
PS C:\> Set-AzHDInsightGatewayCredential `
            -ResourceId "/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.HDInsight/clusters/your-hadoop-001" `
            -HttpCredential $clusterCreds
```

<span data-ttu-id="49bb9-114">Det här kommandot anger Gateway-autentiseringsuppgifter för klustret som heter din-Hadoop-001 enligt ResourceId-parameter uppsättning.</span><span class="sxs-lookup"><span data-stu-id="49bb9-114">This command sets gateway credential of the cluster named your-hadoop-001 by ResourceId parameter set.</span></span>

### <span data-ttu-id="49bb9-115">Exempel 3</span><span class="sxs-lookup"><span data-stu-id="49bb9-115">Example 3</span></span>
```powershell
PS C:\># Cluster info
PS C:\> $clusterName = "your-hadoop-001"
PS C:\> $clusterCreds = Get-Credential

PS C:\> Get-AzHDInsightCluster -ClusterName $clusterName | Set-AzHDInsightGatewayCredential `
            -HttpCredential $clusterCreds
```

<span data-ttu-id="49bb9-116">Det här kommandot anger Gateway-autentiseringsuppgifter för klustret som heter din-Hadoop-001 med InputObject parameter uppsättning.</span><span class="sxs-lookup"><span data-stu-id="49bb9-116">This command sets gateway credential of the cluster named your-hadoop-001 by InputObject parameter set.</span></span>

## <span data-ttu-id="49bb9-117">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="49bb9-117">PARAMETERS</span></span>

### <span data-ttu-id="49bb9-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="49bb9-118">-AsJob</span></span>
<span data-ttu-id="49bb9-119">Kör cmdleten i bakgrunden.</span><span class="sxs-lookup"><span data-stu-id="49bb9-119">Run cmdlet in the background.</span></span>

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

### <span data-ttu-id="49bb9-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="49bb9-120">-DefaultProfile</span></span>
<span data-ttu-id="49bb9-121">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="49bb9-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="49bb9-122">-HttpCredential</span><span class="sxs-lookup"><span data-stu-id="49bb9-122">-HttpCredential</span></span>
<span data-ttu-id="49bb9-123">Hämtar eller anger inloggningen för klustrets användare.</span><span class="sxs-lookup"><span data-stu-id="49bb9-123">Gets or sets the login for the cluster's user.</span></span>

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="49bb9-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="49bb9-124">-InputObject</span></span>
<span data-ttu-id="49bb9-125">Hämtar eller anger indatavärdet.</span><span class="sxs-lookup"><span data-stu-id="49bb9-125">Gets or sets the input object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightCluster
Parameter Sets: SetByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="49bb9-126">-Namn</span><span class="sxs-lookup"><span data-stu-id="49bb9-126">-Name</span></span>
<span data-ttu-id="49bb9-127">Hämtar eller anger klustrets namn.</span><span class="sxs-lookup"><span data-stu-id="49bb9-127">Gets or sets the name of the cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByNameParameterSet
Aliases: ClusterName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="49bb9-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="49bb9-128">-ResourceGroupName</span></span>
<span data-ttu-id="49bb9-129">Hämtar eller anger namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="49bb9-129">Gets or sets the name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="49bb9-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="49bb9-130">-ResourceId</span></span>
<span data-ttu-id="49bb9-131">Hämtar eller anger resurs-ID.</span><span class="sxs-lookup"><span data-stu-id="49bb9-131">Gets or sets the resource id.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="49bb9-132">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="49bb9-132">-Confirm</span></span>
<span data-ttu-id="49bb9-133">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="49bb9-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="49bb9-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="49bb9-134">-WhatIf</span></span>
<span data-ttu-id="49bb9-135">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="49bb9-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="49bb9-136">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="49bb9-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="49bb9-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="49bb9-137">CommonParameters</span></span>
<span data-ttu-id="49bb9-138">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="49bb9-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="49bb9-139">Mer information finns i [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="49bb9-139">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="49bb9-140">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="49bb9-140">INPUTS</span></span>

### <span data-ttu-id="49bb9-141">Ingen</span><span class="sxs-lookup"><span data-stu-id="49bb9-141">None</span></span>

## <span data-ttu-id="49bb9-142">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="49bb9-142">OUTPUTS</span></span>

### <span data-ttu-id="49bb9-143">Microsoft. Azure. Management. HDInsight. Models. HttpConnectivitySettings</span><span class="sxs-lookup"><span data-stu-id="49bb9-143">Microsoft.Azure.Management.HDInsight.Models.HttpConnectivitySettings</span></span>

## <span data-ttu-id="49bb9-144">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="49bb9-144">NOTES</span></span>

## <span data-ttu-id="49bb9-145">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="49bb9-145">RELATED LINKS</span></span>
