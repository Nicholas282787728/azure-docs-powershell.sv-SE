---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azexpressrouteportlinkconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRoutePortLinkConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRoutePortLinkConfig.md
ms.openlocfilehash: 197d18f5d7585f6ae7e865b1c2b0449d032b4238
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94325289"
---
# <span data-ttu-id="66a4a-101">Get-AzExpressRoutePortLinkConfig</span><span class="sxs-lookup"><span data-stu-id="66a4a-101">Get-AzExpressRoutePortLinkConfig</span></span>

## <span data-ttu-id="66a4a-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="66a4a-102">SYNOPSIS</span></span>
<span data-ttu-id="66a4a-103">Hämtar en ExpressRoutePort.</span><span class="sxs-lookup"><span data-stu-id="66a4a-103">Gets an ExpressRoutePort link configuration.</span></span>

## <span data-ttu-id="66a4a-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="66a4a-104">SYNTAX</span></span>

### <span data-ttu-id="66a4a-105">ResourceNameParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="66a4a-105">ResourceNameParameterSet (Default)</span></span>
```
Get-AzExpressRoutePortLinkConfig -ExpressRoutePort <PSExpressRoutePort> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="66a4a-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="66a4a-106">ResourceIdParameterSet</span></span>
```
Get-AzExpressRoutePortLinkConfig -ResourceId <String> -ExpressRoutePort <PSExpressRoutePort>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="66a4a-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="66a4a-107">DESCRIPTION</span></span>
<span data-ttu-id="66a4a-108">Cmdleten **Get-AzExpressRoutePortLinkConfig** hämtar konfigurationen för en länk till en ExpressRoutePort.</span><span class="sxs-lookup"><span data-stu-id="66a4a-108">The **Get-AzExpressRoutePortLinkConfig** cmdlet retrieves the configuration of a link of an ExpressRoutePort.</span></span>

## <span data-ttu-id="66a4a-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="66a4a-109">EXAMPLES</span></span>

### <span data-ttu-id="66a4a-110">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="66a4a-110">Example 1</span></span>
```powershell
PS C:\> Get-AzExpressRoutePortLinkConfig -ExpressRoutePort $erport -Name Link1
```

<span data-ttu-id="66a4a-111">Hämtar link1-konfigurationen för ExpressRoutePort $erport</span><span class="sxs-lookup"><span data-stu-id="66a4a-111">Gets the Link1 configuration of ExpressRoutePort $erport</span></span>

### <span data-ttu-id="66a4a-112">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="66a4a-112">Example 2</span></span>
```powershell
PS C:\> Get-AzExpressRoutePortLinkConfig -ExpressRoutePort $erport -ResourceId $id
```

<span data-ttu-id="66a4a-113">Hämtar konfigurationen för en länk med ResourceId-$id i ExpressRoutePort $erport</span><span class="sxs-lookup"><span data-stu-id="66a4a-113">Gets the configuration of link with ResourceId $id in ExpressRoutePort $erport</span></span>

## <span data-ttu-id="66a4a-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="66a4a-114">PARAMETERS</span></span>

### <span data-ttu-id="66a4a-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="66a4a-115">-DefaultProfile</span></span>
<span data-ttu-id="66a4a-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="66a4a-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="66a4a-117">-ExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="66a4a-117">-ExpressRoutePort</span></span>
<span data-ttu-id="66a4a-118">Referensen för ExpressRoutePort-resursen.</span><span class="sxs-lookup"><span data-stu-id="66a4a-118">The reference of the ExpressRoutePort resource.</span></span>

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

### <span data-ttu-id="66a4a-119">-Namn</span><span class="sxs-lookup"><span data-stu-id="66a4a-119">-Name</span></span>
<span data-ttu-id="66a4a-120">Namnet på länken.</span><span class="sxs-lookup"><span data-stu-id="66a4a-120">Name of the link.</span></span>

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

### <span data-ttu-id="66a4a-121">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="66a4a-121">-ResourceId</span></span>
<span data-ttu-id="66a4a-122">ResourceId för länken.</span><span class="sxs-lookup"><span data-stu-id="66a4a-122">ResourceId of the link.</span></span>

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

### <span data-ttu-id="66a4a-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="66a4a-123">CommonParameters</span></span>
<span data-ttu-id="66a4a-124">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="66a4a-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="66a4a-125">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="66a4a-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="66a4a-126">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="66a4a-126">INPUTS</span></span>

### <span data-ttu-id="66a4a-127">System. String</span><span class="sxs-lookup"><span data-stu-id="66a4a-127">System.String</span></span>

### <span data-ttu-id="66a4a-128">Microsoft. Azure. commands. Networks. Models. PSExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="66a4a-128">Microsoft.Azure.Commands.Network.Models.PSExpressRoutePort</span></span>

## <span data-ttu-id="66a4a-129">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="66a4a-129">OUTPUTS</span></span>

### <span data-ttu-id="66a4a-130">Microsoft. Azure. commands. Networks. Models. PSExpressRouteLink</span><span class="sxs-lookup"><span data-stu-id="66a4a-130">Microsoft.Azure.Commands.Network.Models.PSExpressRouteLink</span></span>

## <span data-ttu-id="66a4a-131">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="66a4a-131">NOTES</span></span>

## <span data-ttu-id="66a4a-132">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="66a4a-132">RELATED LINKS</span></span>