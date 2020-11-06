---
external help file: Microsoft.Azure.Commands.HDInsight.dll-Help.xml
Module Name: AzureRM.HDInsight
ms.assetid: 8C6D9533-68FD-4AFF-91FB-8307A8C8EAEB
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Revoke-AzureRmHDInsightRdpServicesAccess.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Revoke-AzureRmHDInsightRdpServicesAccess.md
ms.openlocfilehash: f05cae3484067f227fde8f30cd7806307832b185
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93574662"
---
# <span data-ttu-id="9a865-101">Revoke-AzureRmHDInsightRdpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="9a865-101">Revoke-AzureRmHDInsightRdpServicesAccess</span></span>

## <span data-ttu-id="9a865-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="9a865-102">SYNOPSIS</span></span>
<span data-ttu-id="9a865-103">Inaktiverar RDP-åtkomst till ett Windows-kluster.</span><span class="sxs-lookup"><span data-stu-id="9a865-103">Disables RDP access to a Windows cluster.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9a865-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="9a865-104">SYNTAX</span></span>

```
Revoke-AzureRmHDInsightRdpServicesAccess [-ClusterName] <String> [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9a865-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="9a865-105">DESCRIPTION</span></span>
<span data-ttu-id="9a865-106">Med cmdleten **REVOKE-AzureRmHDInsightRdpServicesAccess** inaktive ras RDP-åtkomst (Remote Desktop Protocol) till ett Windows-baserat Azure HDInsight-kluster.</span><span class="sxs-lookup"><span data-stu-id="9a865-106">The **Revoke-AzureRmHDInsightRdpServicesAccess** cmdlet disables Remote Desktop Protocol (RDP) access to a Windows-based Azure HDInsight cluster.</span></span>

## <span data-ttu-id="9a865-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="9a865-107">EXAMPLES</span></span>

### <span data-ttu-id="9a865-108">Exempel 1: inaktivera RDP-åtkomst till ett angivet kluster</span><span class="sxs-lookup"><span data-stu-id="9a865-108">Example 1: Disable RDP access to a specified cluster</span></span>
```
PS C:\>Revoke-AzureRmHDInsightRdpServicesAccess -ClusterName "your-hadoop-001"
```

<span data-ttu-id="9a865-109">Det här kommandot återkallar RDP-åtkomst till det kluster som heter din-Hadoop-001.</span><span class="sxs-lookup"><span data-stu-id="9a865-109">This command revokes RDP access to the cluster named your-hadoop-001.</span></span>

## <span data-ttu-id="9a865-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="9a865-110">PARAMETERS</span></span>

### <span data-ttu-id="9a865-111">-Kluster namn</span><span class="sxs-lookup"><span data-stu-id="9a865-111">-ClusterName</span></span>
<span data-ttu-id="9a865-112">Anger namnet på klustret.</span><span class="sxs-lookup"><span data-stu-id="9a865-112">Specifies the name of the cluster.</span></span>

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

### <span data-ttu-id="9a865-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9a865-113">-ResourceGroupName</span></span>
<span data-ttu-id="9a865-114">Anger namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="9a865-114">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="9a865-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9a865-115">-DefaultProfile</span></span>
<span data-ttu-id="9a865-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="9a865-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9a865-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9a865-117">CommonParameters</span></span>
<span data-ttu-id="9a865-118">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9a865-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9a865-119">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9a865-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9a865-120">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="9a865-120">INPUTS</span></span>

## <span data-ttu-id="9a865-121">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="9a865-121">OUTPUTS</span></span>

### <span data-ttu-id="9a865-122">System. Void</span><span class="sxs-lookup"><span data-stu-id="9a865-122">System.Void</span></span>

## <span data-ttu-id="9a865-123">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="9a865-123">NOTES</span></span>

## <span data-ttu-id="9a865-124">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="9a865-124">RELATED LINKS</span></span>

[<span data-ttu-id="9a865-125">Grant-AzureRmHDInsightRdpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="9a865-125">Grant-AzureRmHDInsightRdpServicesAccess</span></span>](./Grant-AzureRmHDInsightRdpServicesAccess.md)


