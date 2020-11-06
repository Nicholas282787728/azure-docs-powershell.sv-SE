---
external help file: Microsoft.Azure.Commands.HDInsight.dll-Help.xml
Module Name: AzureRM.HDInsight
ms.assetid: 8C6D9533-68FD-4AFF-91FB-8307A8C8EAEB
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.hdinsight/revoke-azurermhdinsightrdpservicesaccess
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Revoke-AzureRmHDInsightRdpServicesAccess.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Revoke-AzureRmHDInsightRdpServicesAccess.md
ms.openlocfilehash: 32664beb1ffe7600756953294b1ec33f7d1d54ea
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93581184"
---
# <span data-ttu-id="2c3d5-101">Revoke-AzureRmHDInsightRdpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="2c3d5-101">Revoke-AzureRmHDInsightRdpServicesAccess</span></span>

## <span data-ttu-id="2c3d5-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="2c3d5-102">SYNOPSIS</span></span>
<span data-ttu-id="2c3d5-103">Inaktiverar RDP-åtkomst till ett Windows-kluster.</span><span class="sxs-lookup"><span data-stu-id="2c3d5-103">Disables RDP access to a Windows cluster.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2c3d5-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="2c3d5-104">SYNTAX</span></span>

```
Revoke-AzureRmHDInsightRdpServicesAccess [-ClusterName] <String> [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2c3d5-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="2c3d5-105">DESCRIPTION</span></span>
<span data-ttu-id="2c3d5-106">Med cmdleten **REVOKE-AzureRmHDInsightRdpServicesAccess** inaktive ras RDP-åtkomst (Remote Desktop Protocol) till ett Windows-baserat Azure HDInsight-kluster.</span><span class="sxs-lookup"><span data-stu-id="2c3d5-106">The **Revoke-AzureRmHDInsightRdpServicesAccess** cmdlet disables Remote Desktop Protocol (RDP) access to a Windows-based Azure HDInsight cluster.</span></span>

## <span data-ttu-id="2c3d5-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="2c3d5-107">EXAMPLES</span></span>

### <span data-ttu-id="2c3d5-108">Exempel 1: inaktivera RDP-åtkomst till ett angivet kluster</span><span class="sxs-lookup"><span data-stu-id="2c3d5-108">Example 1: Disable RDP access to a specified cluster</span></span>
```
PS C:\>Revoke-AzureRmHDInsightRdpServicesAccess -ClusterName "your-hadoop-001"
```

<span data-ttu-id="2c3d5-109">Det här kommandot återkallar RDP-åtkomst till det kluster som heter din-Hadoop-001.</span><span class="sxs-lookup"><span data-stu-id="2c3d5-109">This command revokes RDP access to the cluster named your-hadoop-001.</span></span>

## <span data-ttu-id="2c3d5-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="2c3d5-110">PARAMETERS</span></span>

### <span data-ttu-id="2c3d5-111">-Kluster namn</span><span class="sxs-lookup"><span data-stu-id="2c3d5-111">-ClusterName</span></span>
<span data-ttu-id="2c3d5-112">Anger namnet på klustret.</span><span class="sxs-lookup"><span data-stu-id="2c3d5-112">Specifies the name of the cluster.</span></span>

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

### <span data-ttu-id="2c3d5-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2c3d5-113">-DefaultProfile</span></span>
<span data-ttu-id="2c3d5-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="2c3d5-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="2c3d5-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2c3d5-115">-ResourceGroupName</span></span>
<span data-ttu-id="2c3d5-116">Anger namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="2c3d5-116">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="2c3d5-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2c3d5-117">CommonParameters</span></span>
<span data-ttu-id="2c3d5-118">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2c3d5-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2c3d5-119">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2c3d5-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2c3d5-120">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="2c3d5-120">INPUTS</span></span>

### <span data-ttu-id="2c3d5-121">Ingen</span><span class="sxs-lookup"><span data-stu-id="2c3d5-121">None</span></span>
<span data-ttu-id="2c3d5-122">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="2c3d5-122">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="2c3d5-123">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="2c3d5-123">OUTPUTS</span></span>

### <span data-ttu-id="2c3d5-124">System. Void</span><span class="sxs-lookup"><span data-stu-id="2c3d5-124">System.Void</span></span>

## <span data-ttu-id="2c3d5-125">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="2c3d5-125">NOTES</span></span>

## <span data-ttu-id="2c3d5-126">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="2c3d5-126">RELATED LINKS</span></span>

[<span data-ttu-id="2c3d5-127">Grant-AzureRmHDInsightRdpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="2c3d5-127">Grant-AzureRmHDInsightRdpServicesAccess</span></span>](./Grant-AzureRmHDInsightRdpServicesAccess.md)


