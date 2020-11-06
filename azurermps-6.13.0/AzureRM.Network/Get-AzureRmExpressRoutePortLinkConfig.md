---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermexpressrouteportlinkconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmExpressRoutePortLinkConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmExpressRoutePortLinkConfig.md
ms.openlocfilehash: c758131685787ec8627f6e0cd3760e2ee42107c2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93584939"
---
# <span data-ttu-id="2222a-101">Get-AzureRmExpressRoutePortLinkConfig</span><span class="sxs-lookup"><span data-stu-id="2222a-101">Get-AzureRmExpressRoutePortLinkConfig</span></span>

## <span data-ttu-id="2222a-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="2222a-102">SYNOPSIS</span></span>
<span data-ttu-id="2222a-103">Hämtar en ExpressRoutePort.</span><span class="sxs-lookup"><span data-stu-id="2222a-103">Gets an ExpressRoutePort link configuration.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2222a-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="2222a-104">SYNTAX</span></span>

### <span data-ttu-id="2222a-105">ResourceNameParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="2222a-105">ResourceNameParameterSet (Default)</span></span>
```
Get-AzureRmExpressRoutePortLinkConfig -ExpressRoutePort <PSExpressRoutePort> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2222a-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="2222a-106">ResourceIdParameterSet</span></span>
```
Get-AzureRmExpressRoutePortLinkConfig -ExpressRoutePort <PSExpressRoutePort> -ResourceId <String> 
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2222a-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="2222a-107">DESCRIPTION</span></span>
<span data-ttu-id="2222a-108">Cmdleten **Get-AzureRmExpressRoutePortLinkConfig** hämtar konfigurationen för en länk till en ExpressRoutePort.</span><span class="sxs-lookup"><span data-stu-id="2222a-108">The **Get-AzureRmExpressRoutePortLinkConfig** cmdlet retrieves the configuration of a link of an ExpressRoutePort.</span></span>

## <span data-ttu-id="2222a-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="2222a-109">EXAMPLES</span></span>

### <span data-ttu-id="2222a-110">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="2222a-110">Example 1</span></span>
```powershell
PS C:\> Get-AzureRmExpressRoutePortLinkConfig -ExpressRoutePort $erport -Name Link1
```

<span data-ttu-id="2222a-111">Hämtar link1-konfigurationen för ExpressRoutePort $erport</span><span class="sxs-lookup"><span data-stu-id="2222a-111">Gets the Link1 configuration of ExpressRoutePort $erport</span></span>

### <span data-ttu-id="2222a-112">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="2222a-112">Example 2</span></span>
```powershell
PS C:\> Get-AzureRmExpressRoutePortLinkConfig -ExpressRoutePort $erport -ResourceId $id
```

<span data-ttu-id="2222a-113">Hämtar konfigurationen för en länk med ResourceId-$id i ExpressRoutePort $erport</span><span class="sxs-lookup"><span data-stu-id="2222a-113">Gets the configuration of link with ResourceId $id in ExpressRoutePort $erport</span></span>

## <span data-ttu-id="2222a-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="2222a-114">PARAMETERS</span></span>

### <span data-ttu-id="2222a-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2222a-115">-DefaultProfile</span></span>
<span data-ttu-id="2222a-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="2222a-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2222a-117">-ExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="2222a-117">-ExpressRoutePort</span></span>
<span data-ttu-id="2222a-118">Referensen för ExpressRoutePort-resursen.</span><span class="sxs-lookup"><span data-stu-id="2222a-118">The reference of the ExpressRoutePort resource.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSExpressRoutePort
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2222a-119">-Namn</span><span class="sxs-lookup"><span data-stu-id="2222a-119">-Name</span></span>
<span data-ttu-id="2222a-120">Namnet på länken.</span><span class="sxs-lookup"><span data-stu-id="2222a-120">Name of the link.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2222a-121">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="2222a-121">-ResourceId</span></span>
<span data-ttu-id="2222a-122">ResourceId för länken.</span><span class="sxs-lookup"><span data-stu-id="2222a-122">ResourceId of the link.</span></span>

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

### <span data-ttu-id="2222a-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2222a-123">CommonParameters</span></span>
<span data-ttu-id="2222a-124">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2222a-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2222a-125">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2222a-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2222a-126">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="2222a-126">INPUTS</span></span>

### <span data-ttu-id="2222a-127">Microsoft. Azure. commands. Networks. Models. PSExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="2222a-127">Microsoft.Azure.Commands.Network.Models.PSExpressRoutePort</span></span>

## <span data-ttu-id="2222a-128">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="2222a-128">OUTPUTS</span></span>

### <span data-ttu-id="2222a-129">Microsoft. Azure. commands. Networks. Models. PSExpressRouteLink</span><span class="sxs-lookup"><span data-stu-id="2222a-129">Microsoft.Azure.Commands.Network.Models.PSExpressRouteLink</span></span>

## <span data-ttu-id="2222a-130">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="2222a-130">NOTES</span></span>

## <span data-ttu-id="2222a-131">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="2222a-131">RELATED LINKS</span></span>
