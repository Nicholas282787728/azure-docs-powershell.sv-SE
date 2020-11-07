---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 6288DD8A-FF23-4B12-A065-856DBAE200E8
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/grant-azhdinsightrdpservicesaccess
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Grant-AzHDInsightRdpServicesAccess.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Grant-AzHDInsightRdpServicesAccess.md
ms.openlocfilehash: 6cbe18311f4a14b31bc50f7c0b95266bf99d4a40
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93744087"
---
# <span data-ttu-id="a5789-101">Grant-AzHDInsightRdpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="a5789-101">Grant-AzHDInsightRdpServicesAccess</span></span>

## <span data-ttu-id="a5789-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="a5789-102">SYNOPSIS</span></span>
<span data-ttu-id="a5789-103">Ger RDP-åtkomst till Windows-klustret.</span><span class="sxs-lookup"><span data-stu-id="a5789-103">Grants RDP access to the Windows cluster.</span></span>

## <span data-ttu-id="a5789-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="a5789-104">SYNTAX</span></span>

```
Grant-AzHDInsightRdpServicesAccess [-ClusterName] <String> [-RdpCredential] <PSCredential>
 [-RdpAccessExpiry] <DateTime> [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="a5789-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="a5789-105">DESCRIPTION</span></span>
<span data-ttu-id="a5789-106">Med cmdleten **Grant-AzHDInsightRdpServicesAccess** kan du använda RDP (Remote Desktop Protocol) för åtkomst till ett Windows-baserat Azure HDInsight-kluster.</span><span class="sxs-lookup"><span data-stu-id="a5789-106">The **Grant-AzHDInsightRdpServicesAccess** cmdlet enables Remote Desktop Protocol (RDP) to access to a Windows-based Azure HDInsight cluster.</span></span>

## <span data-ttu-id="a5789-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="a5789-107">EXAMPLES</span></span>

### <span data-ttu-id="a5789-108">Exempel 1: bevilja RDP-åtkomst till ett Azure HDInsight-kluster</span><span class="sxs-lookup"><span data-stu-id="a5789-108">Example 1: Grant RDP access to an Azure HDInsight cluster</span></span>
```
PS C:\># Cluster info
PS C:\> $clusterName = "your-hadoop-001"
PS C:\> $clusterCreds = Get-Credential

PS C:\> Grant-AzHDInsightRdpServicesAccess `
            -ClusterName $clusterName `
            -RdpCredential $newRdpCreds `
            -RdpAccessExpiry $newRdpExpiry
```

<span data-ttu-id="a5789-109">Det här kommandot beviljar RDP-åtkomst till det kluster som heter din-Hadoop-001.</span><span class="sxs-lookup"><span data-stu-id="a5789-109">This command grants RDP access to the cluster named your-hadoop-001.</span></span>

## <span data-ttu-id="a5789-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="a5789-110">PARAMETERS</span></span>

### <span data-ttu-id="a5789-111">-Kluster namn</span><span class="sxs-lookup"><span data-stu-id="a5789-111">-ClusterName</span></span>
<span data-ttu-id="a5789-112">Anger namnet på klustret.</span><span class="sxs-lookup"><span data-stu-id="a5789-112">Specifies the name of the cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a5789-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a5789-113">-DefaultProfile</span></span>
<span data-ttu-id="a5789-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="a5789-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a5789-115">-RdpAccessExpiry</span><span class="sxs-lookup"><span data-stu-id="a5789-115">-RdpAccessExpiry</span></span>
<span data-ttu-id="a5789-116">Anger förfallo dag som ett **datetime** -objekt för RDP-åtkomst till ett kluster.</span><span class="sxs-lookup"><span data-stu-id="a5789-116">Specifies the expiration, as a **DateTime** object, for RDP access to a cluster.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a5789-117">-RdpCredential</span><span class="sxs-lookup"><span data-stu-id="a5789-117">-RdpCredential</span></span>
<span data-ttu-id="a5789-118">Anger RDP-autentiseringsuppgifter för klustret.</span><span class="sxs-lookup"><span data-stu-id="a5789-118">Specifies the RDP credentials for the cluster.</span></span>
<span data-ttu-id="a5789-119">Det här är endast för Windows-kluster.</span><span class="sxs-lookup"><span data-stu-id="a5789-119">This is only for Windows clusters.</span></span>

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a5789-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a5789-120">-ResourceGroupName</span></span>
<span data-ttu-id="a5789-121">Anger namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="a5789-121">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="a5789-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a5789-122">CommonParameters</span></span>
<span data-ttu-id="a5789-123">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a5789-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a5789-124">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a5789-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a5789-125">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="a5789-125">INPUTS</span></span>

### <span data-ttu-id="a5789-126">Ingen</span><span class="sxs-lookup"><span data-stu-id="a5789-126">None</span></span>

## <span data-ttu-id="a5789-127">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="a5789-127">OUTPUTS</span></span>

### <span data-ttu-id="a5789-128">System. Void</span><span class="sxs-lookup"><span data-stu-id="a5789-128">System.Void</span></span>

## <span data-ttu-id="a5789-129">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="a5789-129">NOTES</span></span>

## <span data-ttu-id="a5789-130">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="a5789-130">RELATED LINKS</span></span>

[<span data-ttu-id="a5789-131">Återkalla-AzHDInsightRdpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="a5789-131">Revoke-AzHDInsightRdpServicesAccess</span></span>](./Revoke-AzHDInsightRdpServicesAccess.md)


