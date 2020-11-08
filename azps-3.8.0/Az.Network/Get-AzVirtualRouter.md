---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvirtualrouter
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualRouter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualRouter.md
ms.openlocfilehash: dc568657feb5f86cf7cfaa21042e03f8470a9caa
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94089090"
---
# <span data-ttu-id="cf667-101">Get-AzVirtualRouter</span><span class="sxs-lookup"><span data-stu-id="cf667-101">Get-AzVirtualRouter</span></span>

## <span data-ttu-id="cf667-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="cf667-102">SYNOPSIS</span></span>
<span data-ttu-id="cf667-103">Skaffa en Azure-VirtualRouter</span><span class="sxs-lookup"><span data-stu-id="cf667-103">Get an Azure VirtualRouter</span></span>

## <span data-ttu-id="cf667-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="cf667-104">SYNTAX</span></span>

### <span data-ttu-id="cf667-105">VirtualRouterNameParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="cf667-105">VirtualRouterNameParameterSet (Default)</span></span>
```
Get-AzVirtualRouter -ResourceGroupName <String> [-RouterName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="cf667-106">VirtualRouterResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="cf667-106">VirtualRouterResourceIdParameterSet</span></span>
```
Get-AzVirtualRouter -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cf667-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="cf667-107">DESCRIPTION</span></span>
<span data-ttu-id="cf667-108">Cmdleten **Get-AzVirtualRouter** får ett Azure-VirtualRouter</span><span class="sxs-lookup"><span data-stu-id="cf667-108">The **Get-AzVirtualRouter** cmdlet gets an Azure VirtualRouter</span></span>

## <span data-ttu-id="cf667-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="cf667-109">EXAMPLES</span></span>

### <span data-ttu-id="cf667-110">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="cf667-110">Example 1</span></span>
```powershell
Get-AzVirtualRouter -ResourceGroupName virtualRouterRG -RouterName virtualRouter 
```

### <span data-ttu-id="cf667-111">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="cf667-111">Example 2</span></span>
```powershell
$virtualRouterId = '/subscriptions/8c992d64-fce9-426d-b278-85642dfeab03/resourceGroups/virtualRouterRG/providers/Microsoft.Network/virtualRouters/virtualRouter'
Get-AzVirtualRouter -ResourceId $virtualRouterId
```

## <span data-ttu-id="cf667-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="cf667-112">PARAMETERS</span></span>

### <span data-ttu-id="cf667-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cf667-113">-DefaultProfile</span></span>
<span data-ttu-id="cf667-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="cf667-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cf667-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cf667-115">-ResourceGroupName</span></span>
<span data-ttu-id="cf667-116">Namnet på den virtuella routern i resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="cf667-116">The resource group name of the virtual router.</span></span>

```yaml
Type: String
Parameter Sets: VirtualRouterNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cf667-117">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="cf667-117">-ResourceId</span></span>
<span data-ttu-id="cf667-118">ResourceId för den virtuella routern.</span><span class="sxs-lookup"><span data-stu-id="cf667-118">ResourceId of the virtual router.</span></span>

```yaml
Type: String
Parameter Sets: VirtualRouterResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cf667-119">-RouterName</span><span class="sxs-lookup"><span data-stu-id="cf667-119">-RouterName</span></span>
<span data-ttu-id="cf667-120">Namnet på den virtuella routern.</span><span class="sxs-lookup"><span data-stu-id="cf667-120">The name of the virtual router.</span></span>

```yaml
Type: String
Parameter Sets: VirtualRouterNameParameterSet
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cf667-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cf667-121">CommonParameters</span></span>
<span data-ttu-id="cf667-122">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cf667-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cf667-123">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cf667-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cf667-124">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="cf667-124">INPUTS</span></span>

### <span data-ttu-id="cf667-125">System. String</span><span class="sxs-lookup"><span data-stu-id="cf667-125">System.String</span></span>

## <span data-ttu-id="cf667-126">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="cf667-126">OUTPUTS</span></span>

### <span data-ttu-id="cf667-127">Microsoft. Azure. commands. Networks. Models. PSVirtualRouter</span><span class="sxs-lookup"><span data-stu-id="cf667-127">Microsoft.Azure.Commands.Network.Models.PSVirtualRouter</span></span>

## <span data-ttu-id="cf667-128">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="cf667-128">NOTES</span></span>

## <span data-ttu-id="cf667-129">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="cf667-129">RELATED LINKS</span></span>
