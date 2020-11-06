---
external help file: Microsoft.Azure.Commands.ServiceFabric.dll-Help.xml
Module Name: AzureRM.ServiceFabric
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceFabric/Commands.ServiceFabric/help/Get-AzureRmServiceFabricCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceFabric/Commands.ServiceFabric/help/Get-AzureRmServiceFabricCluster.md
ms.openlocfilehash: 645981bb7b2cb02a4bb54a03ccbb570ec31925dc
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93585308"
---
# <span data-ttu-id="998c4-101">Get-AzureRmServiceFabricCluster</span><span class="sxs-lookup"><span data-stu-id="998c4-101">Get-AzureRmServiceFabricCluster</span></span>

## <span data-ttu-id="998c4-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="998c4-102">SYNOPSIS</span></span>
<span data-ttu-id="998c4-103">Hämta information om kluster resursen.</span><span class="sxs-lookup"><span data-stu-id="998c4-103">Get the cluster resource details.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="998c4-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="998c4-104">SYNTAX</span></span>

```
Get-AzureRmServiceFabricCluster [[-ResourceGroupName] <String>] [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="998c4-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="998c4-105">DESCRIPTION</span></span>
<span data-ttu-id="998c4-106">**AzureRmServiceFabricCluster** får information om kluster resursen.</span><span class="sxs-lookup"><span data-stu-id="998c4-106">The **Add-AzureRmServiceFabricCluster** will get the cluster resource details.</span></span>

## <span data-ttu-id="998c4-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="998c4-107">EXAMPLES</span></span>

### <span data-ttu-id="998c4-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="998c4-108">Example 1</span></span>
```
PS C:\> Get-AzureRmServiceFabricCluster -ResourceGroupName 'Group1' -ClusterName 'Contoso01SFCluster'
```

<span data-ttu-id="998c4-109">Det här kommandot hämtar kluster resurs informationen för klustrets kluster.</span><span class="sxs-lookup"><span data-stu-id="998c4-109">This command will get the cluster resource details for cluster 'myCluster'.</span></span>

## <span data-ttu-id="998c4-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="998c4-110">PARAMETERS</span></span>

### <span data-ttu-id="998c4-111">-Namn</span><span class="sxs-lookup"><span data-stu-id="998c4-111">-Name</span></span>
<span data-ttu-id="998c4-112">Ange namnet på klustret.</span><span class="sxs-lookup"><span data-stu-id="998c4-112">Specify the name of the cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ClusterName

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="998c4-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="998c4-113">-ResourceGroupName</span></span>
<span data-ttu-id="998c4-114">Anger namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="998c4-114">Specifies the name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="998c4-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="998c4-115">-DefaultProfile</span></span>
<span data-ttu-id="998c4-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="998c4-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="998c4-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="998c4-117">CommonParameters</span></span>
<span data-ttu-id="998c4-118">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="998c4-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="998c4-119">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="998c4-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="998c4-120">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="998c4-120">INPUTS</span></span>

### <span data-ttu-id="998c4-121">System. String</span><span class="sxs-lookup"><span data-stu-id="998c4-121">System.String</span></span>

## <span data-ttu-id="998c4-122">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="998c4-122">OUTPUTS</span></span>

### <span data-ttu-id="998c4-123">System. Collections. Generic. IList ' 1 [[Microsoft. Azure. commands. ServiceFabric. Models. PsCluster, Microsoft. Azure. commands. ServiceFabric, version = 1.0.0.0, Culture = neutralt, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="998c4-123">System.Collections.Generic.IList\`1[[Microsoft.Azure.Commands.ServiceFabric.Models.PsCluster, Microsoft.Azure.Commands.ServiceFabric, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="998c4-124">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="998c4-124">NOTES</span></span>

## <span data-ttu-id="998c4-125">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="998c4-125">RELATED LINKS</span></span>

