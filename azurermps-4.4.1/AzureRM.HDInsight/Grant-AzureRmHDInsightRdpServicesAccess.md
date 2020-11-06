---
external help file: Microsoft.Azure.Commands.HDInsight.dll-Help.xml
Module Name: AzureRM.HDInsight
ms.assetid: 6288DD8A-FF23-4B12-A065-856DBAE200E8
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Grant-AzureRmHDInsightRdpServicesAccess.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Grant-AzureRmHDInsightRdpServicesAccess.md
ms.openlocfilehash: 22d2f4617e5b8a268de8518695d5217191a211df
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93585567"
---
# <span data-ttu-id="9619e-101">Grant-AzureRmHDInsightRdpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="9619e-101">Grant-AzureRmHDInsightRdpServicesAccess</span></span>

## <span data-ttu-id="9619e-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="9619e-102">SYNOPSIS</span></span>
<span data-ttu-id="9619e-103">Ger RDP-åtkomst till Windows-klustret.</span><span class="sxs-lookup"><span data-stu-id="9619e-103">Grants RDP access to the Windows cluster.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9619e-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="9619e-104">SYNTAX</span></span>

```
Grant-AzureRmHDInsightRdpServicesAccess [-ClusterName] <String> [-RdpCredential] <PSCredential>
 [-RdpAccessExpiry] <DateTime> [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="9619e-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="9619e-105">DESCRIPTION</span></span>
<span data-ttu-id="9619e-106">Med cmdleten **Grant-AzureRmHDInsightRdpServicesAccess** kan du använda RDP (Remote Desktop Protocol) för åtkomst till ett Windows-baserat Azure HDInsight-kluster.</span><span class="sxs-lookup"><span data-stu-id="9619e-106">The **Grant-AzureRmHDInsightRdpServicesAccess** cmdlet enables Remote Desktop Protocol (RDP) to access to a Windows-based Azure HDInsight cluster.</span></span>

## <span data-ttu-id="9619e-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="9619e-107">EXAMPLES</span></span>

### <span data-ttu-id="9619e-108">Exempel 1: bevilja RDP-åtkomst till ett Azure HDInsight-kluster</span><span class="sxs-lookup"><span data-stu-id="9619e-108">Example 1: Grant RDP access to an Azure HDInsight cluster</span></span>
```
PS C:\># Cluster info
PS C:\> $clusterName = "your-hadoop-001"
PS C:\> $clusterCreds = Get-Credential

PS C:\> Grant-AzureRmHDInsightRdpServicesAccess `
            -ClusterName $clusterName `
            -RdpCredential $newRdpCreds `
            -RdpAccessExpiry $newRdpExpiry
```

<span data-ttu-id="9619e-109">Det här kommandot beviljar RDP-åtkomst till det kluster som heter din-Hadoop-001.</span><span class="sxs-lookup"><span data-stu-id="9619e-109">This command grants RDP access to the cluster named your-hadoop-001.</span></span>

## <span data-ttu-id="9619e-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="9619e-110">PARAMETERS</span></span>

### <span data-ttu-id="9619e-111">-Kluster namn</span><span class="sxs-lookup"><span data-stu-id="9619e-111">-ClusterName</span></span>
<span data-ttu-id="9619e-112">Anger namnet på klustret.</span><span class="sxs-lookup"><span data-stu-id="9619e-112">Specifies the name of the cluster.</span></span>

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

### <span data-ttu-id="9619e-113">-RdpAccessExpiry</span><span class="sxs-lookup"><span data-stu-id="9619e-113">-RdpAccessExpiry</span></span>
<span data-ttu-id="9619e-114">Anger förfallo dag som ett **datetime** -objekt för RDP-åtkomst till ett kluster.</span><span class="sxs-lookup"><span data-stu-id="9619e-114">Specifies the expiration, as a **DateTime** object, for RDP access to a cluster.</span></span>

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

### <span data-ttu-id="9619e-115">-RdpCredential</span><span class="sxs-lookup"><span data-stu-id="9619e-115">-RdpCredential</span></span>
<span data-ttu-id="9619e-116">Anger RDP-autentiseringsuppgifter för klustret.</span><span class="sxs-lookup"><span data-stu-id="9619e-116">Specifies the RDP credentials for the cluster.</span></span>
<span data-ttu-id="9619e-117">Det här är endast för Windows-kluster.</span><span class="sxs-lookup"><span data-stu-id="9619e-117">This is only for Windows clusters.</span></span>

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

### <span data-ttu-id="9619e-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9619e-118">-ResourceGroupName</span></span>
<span data-ttu-id="9619e-119">Anger namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="9619e-119">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="9619e-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9619e-120">-DefaultProfile</span></span>
<span data-ttu-id="9619e-121">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="9619e-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9619e-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9619e-122">CommonParameters</span></span>
<span data-ttu-id="9619e-123">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9619e-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9619e-124">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9619e-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9619e-125">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="9619e-125">INPUTS</span></span>

## <span data-ttu-id="9619e-126">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="9619e-126">OUTPUTS</span></span>

### <span data-ttu-id="9619e-127">System. Void</span><span class="sxs-lookup"><span data-stu-id="9619e-127">System.Void</span></span>

## <span data-ttu-id="9619e-128">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="9619e-128">NOTES</span></span>

## <span data-ttu-id="9619e-129">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="9619e-129">RELATED LINKS</span></span>

[<span data-ttu-id="9619e-130">Återkalla-AzureRmHDInsightRdpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="9619e-130">Revoke-AzureRmHDInsightRdpServicesAccess</span></span>](./Revoke-AzureRmHDInsightRdpServicesAccess.md)


