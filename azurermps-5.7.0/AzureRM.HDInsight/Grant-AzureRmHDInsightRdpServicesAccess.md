---
external help file: Microsoft.Azure.Commands.HDInsight.dll-Help.xml
Module Name: AzureRM.HDInsight
ms.assetid: 6288DD8A-FF23-4B12-A065-856DBAE200E8
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.hdinsight/grant-azurermhdinsightrdpservicesaccess
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Grant-AzureRmHDInsightRdpServicesAccess.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Grant-AzureRmHDInsightRdpServicesAccess.md
ms.openlocfilehash: 09b389763897f91a23f56f0a3383dd3f7f03ca1b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93755602"
---
# <span data-ttu-id="31b78-101">Grant-AzureRmHDInsightRdpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="31b78-101">Grant-AzureRmHDInsightRdpServicesAccess</span></span>

## <span data-ttu-id="31b78-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="31b78-102">SYNOPSIS</span></span>
<span data-ttu-id="31b78-103">Ger RDP-åtkomst till Windows-klustret.</span><span class="sxs-lookup"><span data-stu-id="31b78-103">Grants RDP access to the Windows cluster.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="31b78-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="31b78-104">SYNTAX</span></span>

```
Grant-AzureRmHDInsightRdpServicesAccess [-ClusterName] <String> [-RdpCredential] <PSCredential>
 [-RdpAccessExpiry] <DateTime> [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="31b78-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="31b78-105">DESCRIPTION</span></span>
<span data-ttu-id="31b78-106">Med cmdleten **Grant-AzureRmHDInsightRdpServicesAccess** kan du använda RDP (Remote Desktop Protocol) för åtkomst till ett Windows-baserat Azure HDInsight-kluster.</span><span class="sxs-lookup"><span data-stu-id="31b78-106">The **Grant-AzureRmHDInsightRdpServicesAccess** cmdlet enables Remote Desktop Protocol (RDP) to access to a Windows-based Azure HDInsight cluster.</span></span>

## <span data-ttu-id="31b78-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="31b78-107">EXAMPLES</span></span>

### <span data-ttu-id="31b78-108">Exempel 1: bevilja RDP-åtkomst till ett Azure HDInsight-kluster</span><span class="sxs-lookup"><span data-stu-id="31b78-108">Example 1: Grant RDP access to an Azure HDInsight cluster</span></span>
```
PS C:\># Cluster info
PS C:\> $clusterName = "your-hadoop-001"
PS C:\> $clusterCreds = Get-Credential

PS C:\> Grant-AzureRmHDInsightRdpServicesAccess `
            -ClusterName $clusterName `
            -RdpCredential $newRdpCreds `
            -RdpAccessExpiry $newRdpExpiry
```

<span data-ttu-id="31b78-109">Det här kommandot beviljar RDP-åtkomst till det kluster som heter din-Hadoop-001.</span><span class="sxs-lookup"><span data-stu-id="31b78-109">This command grants RDP access to the cluster named your-hadoop-001.</span></span>

## <span data-ttu-id="31b78-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="31b78-110">PARAMETERS</span></span>

### <span data-ttu-id="31b78-111">-Kluster namn</span><span class="sxs-lookup"><span data-stu-id="31b78-111">-ClusterName</span></span>
<span data-ttu-id="31b78-112">Anger namnet på klustret.</span><span class="sxs-lookup"><span data-stu-id="31b78-112">Specifies the name of the cluster.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="31b78-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="31b78-113">-DefaultProfile</span></span>
<span data-ttu-id="31b78-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="31b78-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="31b78-115">-RdpAccessExpiry</span><span class="sxs-lookup"><span data-stu-id="31b78-115">-RdpAccessExpiry</span></span>
<span data-ttu-id="31b78-116">Anger förfallo dag som ett **datetime** -objekt för RDP-åtkomst till ett kluster.</span><span class="sxs-lookup"><span data-stu-id="31b78-116">Specifies the expiration, as a **DateTime** object, for RDP access to a cluster.</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="31b78-117">-RdpCredential</span><span class="sxs-lookup"><span data-stu-id="31b78-117">-RdpCredential</span></span>
<span data-ttu-id="31b78-118">Anger RDP-autentiseringsuppgifter för klustret.</span><span class="sxs-lookup"><span data-stu-id="31b78-118">Specifies the RDP credentials for the cluster.</span></span>
<span data-ttu-id="31b78-119">Det här är endast för Windows-kluster.</span><span class="sxs-lookup"><span data-stu-id="31b78-119">This is only for Windows clusters.</span></span>

```yaml
Type: PSCredential
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="31b78-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="31b78-120">-ResourceGroupName</span></span>
<span data-ttu-id="31b78-121">Anger namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="31b78-121">Specifies the name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="31b78-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="31b78-122">CommonParameters</span></span>
<span data-ttu-id="31b78-123">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="31b78-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="31b78-124">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="31b78-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="31b78-125">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="31b78-125">INPUTS</span></span>

### <span data-ttu-id="31b78-126">Ingen</span><span class="sxs-lookup"><span data-stu-id="31b78-126">None</span></span>
<span data-ttu-id="31b78-127">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="31b78-127">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="31b78-128">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="31b78-128">OUTPUTS</span></span>

### <span data-ttu-id="31b78-129">System. Void</span><span class="sxs-lookup"><span data-stu-id="31b78-129">System.Void</span></span>

## <span data-ttu-id="31b78-130">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="31b78-130">NOTES</span></span>

## <span data-ttu-id="31b78-131">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="31b78-131">RELATED LINKS</span></span>

[<span data-ttu-id="31b78-132">Återkalla-AzureRmHDInsightRdpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="31b78-132">Revoke-AzureRmHDInsightRdpServicesAccess</span></span>](./Revoke-AzureRmHDInsightRdpServicesAccess.md)


