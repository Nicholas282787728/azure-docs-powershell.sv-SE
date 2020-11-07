---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 8C6D9533-68FD-4AFF-91FB-8307A8C8EAEB
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/revoke-azhdinsightrdpservicesaccess
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Revoke-AzHDInsightRdpServicesAccess.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Revoke-AzHDInsightRdpServicesAccess.md
ms.openlocfilehash: 7f5fcb8dcfbb325b8bc0381b3c943e550fe27e62
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93744058"
---
# <span data-ttu-id="6d484-101">Revoke-AzHDInsightRdpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="6d484-101">Revoke-AzHDInsightRdpServicesAccess</span></span>

## <span data-ttu-id="6d484-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="6d484-102">SYNOPSIS</span></span>
<span data-ttu-id="6d484-103">Inaktiverar RDP-åtkomst till ett Windows-kluster.</span><span class="sxs-lookup"><span data-stu-id="6d484-103">Disables RDP access to a Windows cluster.</span></span>

## <span data-ttu-id="6d484-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="6d484-104">SYNTAX</span></span>

```
Revoke-AzHDInsightRdpServicesAccess [-ClusterName] <String> [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6d484-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="6d484-105">DESCRIPTION</span></span>
<span data-ttu-id="6d484-106">Med cmdleten **REVOKE-AzHDInsightRdpServicesAccess** inaktive ras RDP-åtkomst (Remote Desktop Protocol) till ett Windows-baserat Azure HDInsight-kluster.</span><span class="sxs-lookup"><span data-stu-id="6d484-106">The **Revoke-AzHDInsightRdpServicesAccess** cmdlet disables Remote Desktop Protocol (RDP) access to a Windows-based Azure HDInsight cluster.</span></span>

## <span data-ttu-id="6d484-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="6d484-107">EXAMPLES</span></span>

### <span data-ttu-id="6d484-108">Exempel 1: inaktivera RDP-åtkomst till ett angivet kluster</span><span class="sxs-lookup"><span data-stu-id="6d484-108">Example 1: Disable RDP access to a specified cluster</span></span>
```
PS C:\>Revoke-AzHDInsightRdpServicesAccess -ClusterName "your-hadoop-001"
```

<span data-ttu-id="6d484-109">Det här kommandot återkallar RDP-åtkomst till det kluster som heter din-Hadoop-001.</span><span class="sxs-lookup"><span data-stu-id="6d484-109">This command revokes RDP access to the cluster named your-hadoop-001.</span></span>

## <span data-ttu-id="6d484-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="6d484-110">PARAMETERS</span></span>

### <span data-ttu-id="6d484-111">-Kluster namn</span><span class="sxs-lookup"><span data-stu-id="6d484-111">-ClusterName</span></span>
<span data-ttu-id="6d484-112">Anger namnet på klustret.</span><span class="sxs-lookup"><span data-stu-id="6d484-112">Specifies the name of the cluster.</span></span>

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

### <span data-ttu-id="6d484-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6d484-113">-DefaultProfile</span></span>
<span data-ttu-id="6d484-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="6d484-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="6d484-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6d484-115">-ResourceGroupName</span></span>
<span data-ttu-id="6d484-116">Anger namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="6d484-116">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="6d484-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6d484-117">CommonParameters</span></span>
<span data-ttu-id="6d484-118">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6d484-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6d484-119">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6d484-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6d484-120">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="6d484-120">INPUTS</span></span>

### <span data-ttu-id="6d484-121">Ingen</span><span class="sxs-lookup"><span data-stu-id="6d484-121">None</span></span>

## <span data-ttu-id="6d484-122">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="6d484-122">OUTPUTS</span></span>

### <span data-ttu-id="6d484-123">System. Void</span><span class="sxs-lookup"><span data-stu-id="6d484-123">System.Void</span></span>

## <span data-ttu-id="6d484-124">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="6d484-124">NOTES</span></span>

## <span data-ttu-id="6d484-125">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="6d484-125">RELATED LINKS</span></span>

[<span data-ttu-id="6d484-126">Grant-AzHDInsightRdpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="6d484-126">Grant-AzHDInsightRdpServicesAccess</span></span>](./Grant-AzHDInsightRdpServicesAccess.md)


