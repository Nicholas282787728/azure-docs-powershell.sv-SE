---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/get-azservicefabriccluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Get-AzServiceFabricCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Get-AzServiceFabricCluster.md
ms.openlocfilehash: f35cfcbfea4bdca0b75c2048fa403712c3262e02
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94092182"
---
# <span data-ttu-id="9c5ff-101">Get-AzServiceFabricCluster</span><span class="sxs-lookup"><span data-stu-id="9c5ff-101">Get-AzServiceFabricCluster</span></span>

## <span data-ttu-id="9c5ff-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="9c5ff-102">SYNOPSIS</span></span>
<span data-ttu-id="9c5ff-103">Hämta information om kluster resursen.</span><span class="sxs-lookup"><span data-stu-id="9c5ff-103">Get the cluster resource details.</span></span>

## <span data-ttu-id="9c5ff-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="9c5ff-104">SYNTAX</span></span>

### <span data-ttu-id="9c5ff-105">BySubscription (standard)</span><span class="sxs-lookup"><span data-stu-id="9c5ff-105">BySubscription (Default)</span></span>
```
Get-AzServiceFabricCluster [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9c5ff-106">ByResourceGroup</span><span class="sxs-lookup"><span data-stu-id="9c5ff-106">ByResourceGroup</span></span>
```
Get-AzServiceFabricCluster [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="9c5ff-107">ByName</span><span class="sxs-lookup"><span data-stu-id="9c5ff-107">ByName</span></span>
```
Get-AzServiceFabricCluster [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9c5ff-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="9c5ff-108">DESCRIPTION</span></span>
<span data-ttu-id="9c5ff-109">Med **Get-AzServiceFabricCluster** får du information om kluster resursen.</span><span class="sxs-lookup"><span data-stu-id="9c5ff-109">The **Get-AzServiceFabricCluster** will get the cluster resource details.</span></span>

## <span data-ttu-id="9c5ff-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="9c5ff-110">EXAMPLES</span></span>

### <span data-ttu-id="9c5ff-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="9c5ff-111">Example 1</span></span>
```powershell
PS C:\> Get-AzServiceFabricCluster -ResourceGroupName 'Group1' -ClusterName 'Contoso01SFCluster'
```

<span data-ttu-id="9c5ff-112">Det här kommandot hämtar kluster resurs informationen för klustrets kluster.</span><span class="sxs-lookup"><span data-stu-id="9c5ff-112">This command will get the cluster resource details for cluster 'myCluster'.</span></span>

## <span data-ttu-id="9c5ff-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="9c5ff-113">PARAMETERS</span></span>

### <span data-ttu-id="9c5ff-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9c5ff-114">-DefaultProfile</span></span>
<span data-ttu-id="9c5ff-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="9c5ff-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9c5ff-116">-Namn</span><span class="sxs-lookup"><span data-stu-id="9c5ff-116">-Name</span></span>
<span data-ttu-id="9c5ff-117">Ange namnet på klustret</span><span class="sxs-lookup"><span data-stu-id="9c5ff-117">Specify the name of the cluster</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases: ClusterName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9c5ff-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9c5ff-118">-ResourceGroupName</span></span>
<span data-ttu-id="9c5ff-119">Ange namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="9c5ff-119">Specify the name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroup, ByName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9c5ff-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9c5ff-120">CommonParameters</span></span>
<span data-ttu-id="9c5ff-121">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9c5ff-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9c5ff-122">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9c5ff-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9c5ff-123">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="9c5ff-123">INPUTS</span></span>

### <span data-ttu-id="9c5ff-124">System. String</span><span class="sxs-lookup"><span data-stu-id="9c5ff-124">System.String</span></span>

## <span data-ttu-id="9c5ff-125">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="9c5ff-125">OUTPUTS</span></span>

### <span data-ttu-id="9c5ff-126">Microsoft. Azure. commands. ServiceFabric. Models. PSCluster</span><span class="sxs-lookup"><span data-stu-id="9c5ff-126">Microsoft.Azure.Commands.ServiceFabric.Models.PSCluster</span></span>

## <span data-ttu-id="9c5ff-127">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="9c5ff-127">NOTES</span></span>

## <span data-ttu-id="9c5ff-128">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="9c5ff-128">RELATED LINKS</span></span>
