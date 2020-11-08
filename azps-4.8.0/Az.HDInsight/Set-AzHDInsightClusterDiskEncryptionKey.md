---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 5141D84C-3C58-42B9-890F-C3C9049BC1C5
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/set-azhdinsightclusterdiskencryptionkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Set-AzHDInsightClusterDiskEncryptionKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Set-AzHDInsightClusterDiskEncryptionKey.md
ms.openlocfilehash: b3421fa4382912d11a3e3a28b81acffb7be123a2
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94261112"
---
# <span data-ttu-id="c779c-101">Set-AzHDInsightClusterDiskEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="c779c-101">Set-AzHDInsightClusterDiskEncryptionKey</span></span>

## <span data-ttu-id="c779c-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="c779c-102">SYNOPSIS</span></span>
<span data-ttu-id="c779c-103">Roterar disk krypterings tangenten för det angivna HDInsight-klustret.</span><span class="sxs-lookup"><span data-stu-id="c779c-103">Rotates the disk encryption key of the specified HDInsight cluster.</span></span>

## <span data-ttu-id="c779c-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="c779c-104">SYNTAX</span></span>

### <span data-ttu-id="c779c-105">SetByNameParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="c779c-105">SetByNameParameterSet (Default)</span></span>
```
Set-AzHDInsightClusterDiskEncryptionKey [-ResourceGroupName] <String> [-Name] <String>
 -EncryptionKeyName <String> -EncryptionKeyVersion <String> -EncryptionVaultUri <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c779c-106">SetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="c779c-106">SetByResourceIdParameterSet</span></span>
```
Set-AzHDInsightClusterDiskEncryptionKey [-ResourceId] <String> -EncryptionKeyName <String>
 -EncryptionKeyVersion <String> -EncryptionVaultUri <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c779c-107">SetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="c779c-107">SetByInputObjectParameterSet</span></span>
```
Set-AzHDInsightClusterDiskEncryptionKey [-InputObject] <AzureHDInsightCluster> -EncryptionKeyName <String>
 -EncryptionKeyVersion <String> -EncryptionVaultUri <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c779c-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="c779c-108">DESCRIPTION</span></span>
<span data-ttu-id="c779c-109">Rotera disk krypterings tangenten för det angivna HDInsight-klustret.</span><span class="sxs-lookup"><span data-stu-id="c779c-109">Rotate the disk encryption key of the specified HDInsight cluster.</span></span> <span data-ttu-id="c779c-110">För den här åtgärden måste klustret ha åtkomst till både den aktuella tangenten och den tänkta nya knappen, annars går det inte att använda rotations knappen.</span><span class="sxs-lookup"><span data-stu-id="c779c-110">For this operation, the cluster must have access to both the current key and the intended new key, otherwise the rotate key operation will fail.</span></span>

## <span data-ttu-id="c779c-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="c779c-111">EXAMPLES</span></span>

### <span data-ttu-id="c779c-112">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="c779c-112">Example 1</span></span>
```powershell
PS C:\> # Cluster configuration info
        $clusterResourceGroupName = "Group"
        $clusterName = "your-cmk-cluster"

Set-AzHDInsightClusterDiskEncryptionKey `
        -ResourceGroupName $clusterResourceGroupName `
        -ClusterName $clusterName `
        -EncryptionKeyName new-key `
        -EncryptionVaultUri https://MyKeyVault.vault.azure.net `
        -EncryptionKeyVersion 00000000000000000000000000000000
```

### <span data-ttu-id="c779c-113">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="c779c-113">Example 2</span></span>
```powershell
PS C:\> # Cluster configuration info
        $clusterName = "your-cmk-cluster"

$cluster= Get-AzHDInsightCluster -ClusterName $clusterName 
$cluster |  Set-AzHDInsightClusterDiskEncryptionKey `
    -EncryptionKeyName new-key `
    -EncryptionVaultUri https://MyKeyVault.vault.azure.net `
    -EncryptionKeyVersion 00000000000000000000000000000000
```

## <span data-ttu-id="c779c-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="c779c-114">PARAMETERS</span></span>

### <span data-ttu-id="c779c-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c779c-115">-DefaultProfile</span></span>
<span data-ttu-id="c779c-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="c779c-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c779c-117">-EncryptionKeyName</span><span class="sxs-lookup"><span data-stu-id="c779c-117">-EncryptionKeyName</span></span>
<span data-ttu-id="c779c-118">Hämtar eller anger namnet på krypterings nycklar.</span><span class="sxs-lookup"><span data-stu-id="c779c-118">Gets or sets the encryption key name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c779c-119">-EncryptionKeyVersion</span><span class="sxs-lookup"><span data-stu-id="c779c-119">-EncryptionKeyVersion</span></span>
<span data-ttu-id="c779c-120">Hämtar eller anger krypterings huvud versionen.</span><span class="sxs-lookup"><span data-stu-id="c779c-120">Gets or sets the encryption key version.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c779c-121">-EncryptionVaultUri</span><span class="sxs-lookup"><span data-stu-id="c779c-121">-EncryptionVaultUri</span></span>
<span data-ttu-id="c779c-122">Hämtar eller anger krypterings valv-URI.</span><span class="sxs-lookup"><span data-stu-id="c779c-122">Gets or sets the encryption vault uri.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c779c-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c779c-123">-InputObject</span></span>
<span data-ttu-id="c779c-124">Hämtar eller anger indatavärdet.</span><span class="sxs-lookup"><span data-stu-id="c779c-124">Gets or sets the input object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightCluster
Parameter Sets: SetByInputObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c779c-125">-Namn</span><span class="sxs-lookup"><span data-stu-id="c779c-125">-Name</span></span>
<span data-ttu-id="c779c-126">Hämtar eller anger klustrets namn.</span><span class="sxs-lookup"><span data-stu-id="c779c-126">Gets or sets the name of the cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByNameParameterSet
Aliases: ClusterName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c779c-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c779c-127">-ResourceGroupName</span></span>
<span data-ttu-id="c779c-128">Hämtar eller anger namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="c779c-128">Gets or sets the name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c779c-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c779c-129">-ResourceId</span></span>
<span data-ttu-id="c779c-130">Hämtar eller anger resurs-ID.</span><span class="sxs-lookup"><span data-stu-id="c779c-130">Gets or sets the resource id.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c779c-131">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="c779c-131">-Confirm</span></span>
<span data-ttu-id="c779c-132">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="c779c-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c779c-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c779c-133">-WhatIf</span></span>
<span data-ttu-id="c779c-134">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="c779c-134">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="c779c-135">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="c779c-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c779c-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c779c-136">CommonParameters</span></span>
<span data-ttu-id="c779c-137">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c779c-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c779c-138">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c779c-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c779c-139">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="c779c-139">INPUTS</span></span>

### <span data-ttu-id="c779c-140">Ingen</span><span class="sxs-lookup"><span data-stu-id="c779c-140">None</span></span>

## <span data-ttu-id="c779c-141">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="c779c-141">OUTPUTS</span></span>

### <span data-ttu-id="c779c-142">Microsoft. Azure. Management. HDInsight. Models. Cluster</span><span class="sxs-lookup"><span data-stu-id="c779c-142">Microsoft.Azure.Management.HDInsight.Models.Cluster</span></span>

## <span data-ttu-id="c779c-143">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="c779c-143">NOTES</span></span>

## <span data-ttu-id="c779c-144">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="c779c-144">RELATED LINKS</span></span>

[<span data-ttu-id="c779c-145">Kundhanterad kryptering av nycklar</span><span class="sxs-lookup"><span data-stu-id="c779c-145">Customer-managed key disk encryption</span></span>](https://docs.microsoft.com/en-us/azure/hdinsight/disk-encryption)
