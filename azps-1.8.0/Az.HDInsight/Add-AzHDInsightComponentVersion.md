---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 774848C9-47A1-4C43-B6FA-B3C0C3C76470
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/add-azhdinsightcomponentversion
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Add-AzHDInsightComponentVersion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Add-AzHDInsightComponentVersion.md
ms.openlocfilehash: 792ca76f7259058991b8c181b383bdeffd7db290
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93916674"
---
# <span data-ttu-id="8bb24-101">Add-AzHDInsightComponentVersion</span><span class="sxs-lookup"><span data-stu-id="8bb24-101">Add-AzHDInsightComponentVersion</span></span>

## <span data-ttu-id="8bb24-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="8bb24-102">SYNOPSIS</span></span>
<span data-ttu-id="8bb24-103">Lägger till en version för en tjänst som körs i ett kluster till ett kluster konfigurations objekt.</span><span class="sxs-lookup"><span data-stu-id="8bb24-103">Adds a version for a service running in a cluster to a cluster configuration object.</span></span>

## <span data-ttu-id="8bb24-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="8bb24-104">SYNTAX</span></span>

```
Add-AzHDInsightComponentVersion [-Config] <AzureHDInsightConfig> [-ComponentName] <String>
 [-ComponentVersion] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="8bb24-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="8bb24-105">DESCRIPTION</span></span>
<span data-ttu-id="8bb24-106">Med Add-AzHDInsightComponentVersion-cmdleten läggs en version till för en tjänst som körs i ett kluster till Azure HDInsight-konfigurationsobjektet som skapas av New-AzHDInsightClusterConfig cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8bb24-106">The Add-AzHDInsightComponentVersion cmdlet adds a version for a service running in a cluster to the Azure HDInsight configuration object created by the New-AzHDInsightClusterConfig cmdlet.</span></span>

## <span data-ttu-id="8bb24-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="8bb24-107">EXAMPLES</span></span>

### <span data-ttu-id="8bb24-108">Exempel 1: lägga till en version för Spark i klustrets konfigurations objekt.</span><span class="sxs-lookup"><span data-stu-id="8bb24-108">Example 1: Add a version for Spark to the cluster configuration object.</span></span>
```
PS C:\> # Primary storage account info
        $storageAccountResourceGroupName = "Group"
        $storageAccountName = "yourstorageacct001"
        $storageAccountKey = Get-AzStorageAccountKey `
            -ResourceGroupName $storageAccountResourceGroupName `
            -Name $storageAccountName | %{ $_.Key1 }
        $storageContainer = "container001"

        # Cluster configuration info
        $location = "East US 2"
        $clusterResourceGroupName = "Group"
        $clusterName = "your-spark-001"
        $clusterCreds = Get-Credential
        $sshClusterCreds = Get-Credential

        # If the cluster's resource group doesn't exist yet, run:
        #   New-AzResourceGroup -Name $clusterResourceGroupName -Location $location

        # Create the cluster
        New-AzHDInsightClusterConfig `
            | Add-AzHDInsightComponentVersion `
                -ComponentName "Spark" `
                -ComponentVersion "2.0" `
            | New-AzHDInsightCluster `
                -ClusterType Spark `
                -OSType Linux `
                -ClusterSizeInNodes 4 `
                -ResourceGroupName $clusterResourceGroupName `
                -ClusterName $clusterName `
                -HttpCredential $clusterCreds `
                -Location $location `
                -DefaultStorageAccountName "$storageAccountName.blob.core.contoso.net" `
                -DefaultStorageAccountKey $storageAccountKey `
                -DefaultStorageContainer $storageContainer `
                -SshCredential $sshCredentials `
                -Version "3.5"
```

<span data-ttu-id="8bb24-109">Det här kommandot lägger till en version av Spark till HDInsight-klustret med namnet "din-spark-001".</span><span class="sxs-lookup"><span data-stu-id="8bb24-109">This command adds the version of Spark to the HDInsight cluster named 'your-spark-001'.</span></span>

## <span data-ttu-id="8bb24-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="8bb24-110">PARAMETERS</span></span>

### <span data-ttu-id="8bb24-111">-ComponentName</span><span class="sxs-lookup"><span data-stu-id="8bb24-111">-ComponentName</span></span>
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

### <span data-ttu-id="8bb24-112">-ComponentVersion</span><span class="sxs-lookup"><span data-stu-id="8bb24-112">-ComponentVersion</span></span>
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

### <span data-ttu-id="8bb24-113">-Config</span><span class="sxs-lookup"><span data-stu-id="8bb24-113">-Config</span></span>
```yaml
Type: Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8bb24-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8bb24-114">-DefaultProfile</span></span>
<span data-ttu-id="8bb24-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="8bb24-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="8bb24-116">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="8bb24-116">-Confirm</span></span>
<span data-ttu-id="8bb24-117">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="8bb24-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8bb24-118">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8bb24-118">-WhatIf</span></span>
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

### <span data-ttu-id="8bb24-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8bb24-119">CommonParameters</span></span>
<span data-ttu-id="8bb24-120">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8bb24-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8bb24-121">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8bb24-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8bb24-122">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="8bb24-122">INPUTS</span></span>

### <span data-ttu-id="8bb24-123">Microsoft. Azure. commands. HDInsight. Models. AzureHDInsightConfig</span><span class="sxs-lookup"><span data-stu-id="8bb24-123">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig</span></span>

## <span data-ttu-id="8bb24-124">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="8bb24-124">OUTPUTS</span></span>

### <span data-ttu-id="8bb24-125">Microsoft. Azure. commands. HDInsight. Models. AzureHDInsightConfig</span><span class="sxs-lookup"><span data-stu-id="8bb24-125">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig</span></span>

## <span data-ttu-id="8bb24-126">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="8bb24-126">NOTES</span></span>

## <span data-ttu-id="8bb24-127">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="8bb24-127">RELATED LINKS</span></span>