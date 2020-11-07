---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermexpressrouteport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmExpressRoutePort.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmExpressRoutePort.md
ms.openlocfilehash: 36c15c9a0bfae9bbf3a14f59877d23c1c8778163
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93757854"
---
# <span data-ttu-id="ddf06-101">Get-AzureRmExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="ddf06-101">Get-AzureRmExpressRoutePort</span></span>

## <span data-ttu-id="ddf06-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="ddf06-102">SYNOPSIS</span></span>
<span data-ttu-id="ddf06-103">Får en Azure ExpressRoutePort-resurs.</span><span class="sxs-lookup"><span data-stu-id="ddf06-103">Gets an Azure ExpressRoutePort resource.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ddf06-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="ddf06-104">SYNTAX</span></span>

### <span data-ttu-id="ddf06-105">ResourceNameParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="ddf06-105">ResourceNameParameterSet (Default)</span></span>
```
Get-AzureRmExpressRoutePort [-ResourceGroupName <String>] [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ddf06-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="ddf06-106">ResourceIdParameterSet</span></span>
```
Get-AzureRmExpressRoutePort -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="ddf06-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="ddf06-107">DESCRIPTION</span></span>
<span data-ttu-id="ddf06-108">Cmdleten **Get-AzureRmExpressRoutePort** används för att hämta ett ExpressRoutePort-objekt från din prenumeration.</span><span class="sxs-lookup"><span data-stu-id="ddf06-108">The **Get-AzureRmExpressRoutePort** cmdlet is used to retrieve an ExpressRoutePort object from your subscription.</span></span> <span data-ttu-id="ddf06-109">Det expressrouteport-objekt som returneras kan användas som indata för andra cmdlets som körs på ExpressRoutePort.</span><span class="sxs-lookup"><span data-stu-id="ddf06-109">The expressrouteport object returned can be used as input to other cmdlets that operate on ExpressRoutePort.</span></span>

## <span data-ttu-id="ddf06-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="ddf06-110">EXAMPLES</span></span>

### <span data-ttu-id="ddf06-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="ddf06-111">Example 1</span></span>
```powershell
PS C:\> Get-AzureRmExpressRoutePort -Name $PortName -ResourceGroupName $rg
```

<span data-ttu-id="ddf06-112">Hämtar ExpressRoutePort-objektet med namnet $PortName i resurs gruppen $rg i ditt abonnemang.</span><span class="sxs-lookup"><span data-stu-id="ddf06-112">Gets the ExpressRoutePort object with name $PortName in resource group $rg in your subscription.</span></span>

### <span data-ttu-id="ddf06-113">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="ddf06-113">Example 2</span></span>
```powershell
PS C:\> Get-AzureRmExpressRoutePort -ResourceId $id
```

<span data-ttu-id="ddf06-114">Hämtar ExpressRoutePort-objektet med ResourceId $id.</span><span class="sxs-lookup"><span data-stu-id="ddf06-114">Gets the ExpressRoutePort object with ResourceId $id.</span></span> 

## <span data-ttu-id="ddf06-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="ddf06-115">PARAMETERS</span></span>

### <span data-ttu-id="ddf06-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ddf06-116">-DefaultProfile</span></span>
<span data-ttu-id="ddf06-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="ddf06-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ddf06-118">-Namn</span><span class="sxs-lookup"><span data-stu-id="ddf06-118">-Name</span></span>
<span data-ttu-id="ddf06-119">Namnet på ExpressRoutePort.</span><span class="sxs-lookup"><span data-stu-id="ddf06-119">The name of the ExpressRoutePort.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceNameParameterSet
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ddf06-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ddf06-120">-ResourceGroupName</span></span>
<span data-ttu-id="ddf06-121">Resurs grupps namnet för ExpressRoutePort.</span><span class="sxs-lookup"><span data-stu-id="ddf06-121">The resource group name of the ExpressRoutePort.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ddf06-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ddf06-122">-ResourceId</span></span>
<span data-ttu-id="ddf06-123">ResourceId för ExpressRoute-porten.</span><span class="sxs-lookup"><span data-stu-id="ddf06-123">ResourceId of the express route port.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ddf06-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ddf06-124">CommonParameters</span></span>
<span data-ttu-id="ddf06-125">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ddf06-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ddf06-126">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ddf06-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ddf06-127">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="ddf06-127">INPUTS</span></span>

### <span data-ttu-id="ddf06-128">System. String</span><span class="sxs-lookup"><span data-stu-id="ddf06-128">System.String</span></span>

## <span data-ttu-id="ddf06-129">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="ddf06-129">OUTPUTS</span></span>

### <span data-ttu-id="ddf06-130">Microsoft. Azure. commands. Networks. Models. PSExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="ddf06-130">Microsoft.Azure.Commands.Network.Models.PSExpressRoutePort</span></span>

## <span data-ttu-id="ddf06-131">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="ddf06-131">NOTES</span></span>

## <span data-ttu-id="ddf06-132">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="ddf06-132">RELATED LINKS</span></span>
