---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvirtualrouter
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualRouter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualRouter.md
ms.openlocfilehash: e99df2f29781281ee0293f4cf52715153ff0d0cc
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98422099"
---
# <span data-ttu-id="876d7-101">Get-AzVirtualRouter</span><span class="sxs-lookup"><span data-stu-id="876d7-101">Get-AzVirtualRouter</span></span>

## <span data-ttu-id="876d7-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="876d7-102">SYNOPSIS</span></span>
<span data-ttu-id="876d7-103">Skaffa en Azure-VirtualRouter</span><span class="sxs-lookup"><span data-stu-id="876d7-103">Get an Azure VirtualRouter</span></span>

## <span data-ttu-id="876d7-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="876d7-104">SYNTAX</span></span>

### <span data-ttu-id="876d7-105">VirtualRouterSubscriptionIdParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="876d7-105">VirtualRouterSubscriptionIdParameterSet (Default)</span></span>
```
Get-AzVirtualRouter [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="876d7-106">VirtualRouterNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="876d7-106">VirtualRouterNameParameterSet</span></span>
```
Get-AzVirtualRouter -ResourceGroupName <String> [-RouterName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="876d7-107">VirtualRouterResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="876d7-107">VirtualRouterResourceIdParameterSet</span></span>
```
Get-AzVirtualRouter -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="876d7-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="876d7-108">DESCRIPTION</span></span>
<span data-ttu-id="876d7-109">Cmdleten **Get-AzVirtualRouter** får ett Azure-VirtualRouter</span><span class="sxs-lookup"><span data-stu-id="876d7-109">The **Get-AzVirtualRouter** cmdlet gets an Azure VirtualRouter</span></span>

## <span data-ttu-id="876d7-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="876d7-110">EXAMPLES</span></span>

### <span data-ttu-id="876d7-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="876d7-111">Example 1</span></span>
```powershell
Get-AzVirtualRouter -ResourceGroupName virtualRouterRG -RouterName virtualRouter
```

### <span data-ttu-id="876d7-112">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="876d7-112">Example 2</span></span>
```powershell
$virtualRouterId = '/subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/virtualRouterRG/providers/Microsoft.Network/virtualRouters/virtualRouter'
Get-AzVirtualRouter -ResourceId $virtualRouterId
```

## <span data-ttu-id="876d7-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="876d7-113">PARAMETERS</span></span>

### <span data-ttu-id="876d7-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="876d7-114">-DefaultProfile</span></span>
<span data-ttu-id="876d7-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="876d7-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="876d7-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="876d7-116">-ResourceGroupName</span></span>
<span data-ttu-id="876d7-117">Namnet på den virtuella routern i resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="876d7-117">The resource group name of the virtual router.</span></span>

```yaml
Type: System.String
Parameter Sets: VirtualRouterNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="876d7-118">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="876d7-118">-ResourceId</span></span>
<span data-ttu-id="876d7-119">ResourceId för den virtuella routern.</span><span class="sxs-lookup"><span data-stu-id="876d7-119">ResourceId of the virtual router.</span></span>

```yaml
Type: System.String
Parameter Sets: VirtualRouterResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="876d7-120">-RouterName</span><span class="sxs-lookup"><span data-stu-id="876d7-120">-RouterName</span></span>
<span data-ttu-id="876d7-121">Namnet på den virtuella routern.</span><span class="sxs-lookup"><span data-stu-id="876d7-121">The name of the virtual router.</span></span>

```yaml
Type: System.String
Parameter Sets: VirtualRouterNameParameterSet
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="876d7-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="876d7-122">CommonParameters</span></span>
<span data-ttu-id="876d7-123">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="876d7-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="876d7-124">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="876d7-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="876d7-125">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="876d7-125">INPUTS</span></span>

### <span data-ttu-id="876d7-126">System. String</span><span class="sxs-lookup"><span data-stu-id="876d7-126">System.String</span></span>

## <span data-ttu-id="876d7-127">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="876d7-127">OUTPUTS</span></span>

### <span data-ttu-id="876d7-128">Microsoft. Azure. commands. Networks. Models. PSVirtualRouter</span><span class="sxs-lookup"><span data-stu-id="876d7-128">Microsoft.Azure.Commands.Network.Models.PSVirtualRouter</span></span>

## <span data-ttu-id="876d7-129">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="876d7-129">NOTES</span></span>

## <span data-ttu-id="876d7-130">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="876d7-130">RELATED LINKS</span></span>
