---
external help file: Microsoft.Azure.Commands.ServiceFabric.dll-Help.xml
Module Name: AzureRM.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicefabric/get-azurermservicefabriccluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceFabric/Commands.ServiceFabric/help/Get-AzureRmServiceFabricCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceFabric/Commands.ServiceFabric/help/Get-AzureRmServiceFabricCluster.md
ms.openlocfilehash: 5f034253326f551c5b1930f6cf90a80c83ed82f5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93574173"
---
# <span data-ttu-id="1b544-101">Get-AzureRmServiceFabricCluster</span><span class="sxs-lookup"><span data-stu-id="1b544-101">Get-AzureRmServiceFabricCluster</span></span>

## <span data-ttu-id="1b544-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="1b544-102">SYNOPSIS</span></span>
<span data-ttu-id="1b544-103">Hämta information om kluster resursen.</span><span class="sxs-lookup"><span data-stu-id="1b544-103">Get the cluster resource details.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1b544-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="1b544-104">SYNTAX</span></span>

### <span data-ttu-id="1b544-105">BySubscription (standard)</span><span class="sxs-lookup"><span data-stu-id="1b544-105">BySubscription (Default)</span></span>
```
Get-AzureRmServiceFabricCluster [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1b544-106">ByResourceGroup</span><span class="sxs-lookup"><span data-stu-id="1b544-106">ByResourceGroup</span></span>
```
Get-AzureRmServiceFabricCluster [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="1b544-107">ByName</span><span class="sxs-lookup"><span data-stu-id="1b544-107">ByName</span></span>
```
Get-AzureRmServiceFabricCluster [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1b544-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="1b544-108">DESCRIPTION</span></span>
<span data-ttu-id="1b544-109">**AzureRmServiceFabricCluster** får information om kluster resursen.</span><span class="sxs-lookup"><span data-stu-id="1b544-109">The **Add-AzureRmServiceFabricCluster** will get the cluster resource details.</span></span>

## <span data-ttu-id="1b544-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="1b544-110">EXAMPLES</span></span>

### <span data-ttu-id="1b544-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="1b544-111">Example 1</span></span>
```
PS C:\> Get-AzureRmServiceFabricCluster -ResourceGroupName 'Group1' -ClusterName 'Contoso01SFCluster'
```

<span data-ttu-id="1b544-112">Det här kommandot hämtar kluster resurs informationen för klustrets kluster.</span><span class="sxs-lookup"><span data-stu-id="1b544-112">This command will get the cluster resource details for cluster 'myCluster'.</span></span>

## <span data-ttu-id="1b544-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="1b544-113">PARAMETERS</span></span>

### <span data-ttu-id="1b544-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1b544-114">-DefaultProfile</span></span>
<span data-ttu-id="1b544-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="1b544-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1b544-116">-Namn</span><span class="sxs-lookup"><span data-stu-id="1b544-116">-Name</span></span>
<span data-ttu-id="1b544-117">Ange namnet på klustret.</span><span class="sxs-lookup"><span data-stu-id="1b544-117">Specify the name of the cluster.</span></span>

```yaml
Type: String
Parameter Sets: ByName
Aliases: ClusterName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1b544-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1b544-118">-ResourceGroupName</span></span>
<span data-ttu-id="1b544-119">Anger namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="1b544-119">Specifies the name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: ByResourceGroup, ByName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1b544-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1b544-120">CommonParameters</span></span>
<span data-ttu-id="1b544-121">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1b544-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1b544-122">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1b544-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1b544-123">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="1b544-123">INPUTS</span></span>

### <span data-ttu-id="1b544-124">System. String</span><span class="sxs-lookup"><span data-stu-id="1b544-124">System.String</span></span>

## <span data-ttu-id="1b544-125">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="1b544-125">OUTPUTS</span></span>

### <span data-ttu-id="1b544-126">System. Collections. Generic. IList ' 1 [[Microsoft. Azure. commands. ServiceFabric. Models. PsCluster, Microsoft. Azure. commands. ServiceFabric, version = 1.0.0.0, Culture = neutralt, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="1b544-126">System.Collections.Generic.IList\`1[[Microsoft.Azure.Commands.ServiceFabric.Models.PsCluster, Microsoft.Azure.Commands.ServiceFabric, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="1b544-127">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="1b544-127">NOTES</span></span>

## <span data-ttu-id="1b544-128">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="1b544-128">RELATED LINKS</span></span>

