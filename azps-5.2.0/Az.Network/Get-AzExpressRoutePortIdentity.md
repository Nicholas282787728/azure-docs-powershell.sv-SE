---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azexpressrouteportidentity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRoutePortIdentity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRoutePortIdentity.md
ms.openlocfilehash: 246675a2473bb20e5040f3898b6931f1b3ee6933
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98416667"
---
# <span data-ttu-id="5e3a5-101">Get-AzExpressRoutePortIdentity</span><span class="sxs-lookup"><span data-stu-id="5e3a5-101">Get-AzExpressRoutePortIdentity</span></span>

## <span data-ttu-id="5e3a5-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="5e3a5-102">SYNOPSIS</span></span>
<span data-ttu-id="5e3a5-103">Få identitet tilldelad en ExpressRoutePort.</span><span class="sxs-lookup"><span data-stu-id="5e3a5-103">Get identity assigned to an ExpressRoutePort.</span></span>

## <span data-ttu-id="5e3a5-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="5e3a5-104">SYNTAX</span></span>

```
Get-AzExpressRoutePortIdentity -ExpressRoutePort <PSExpressRoutePort>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5e3a5-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="5e3a5-105">DESCRIPTION</span></span>
<span data-ttu-id="5e3a5-106">Cmdleten **Get-AzExpressRoutePortIdentity** får identiteten tilldelad ett lokalt Azure ExpressRoutePort-objekt.</span><span class="sxs-lookup"><span data-stu-id="5e3a5-106">The **Get-AzExpressRoutePortIdentity** cmdlet gets identity assigned to a local Azure ExpressRoutePort object.</span></span>

## <span data-ttu-id="5e3a5-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="5e3a5-107">EXAMPLES</span></span>

### <span data-ttu-id="5e3a5-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="5e3a5-108">Example 1</span></span>
```powershell
PS C:\> $exrPort = Get-AzExpressRoutePort -Name $exrPortName -ResourceGroupName $resgpName
PS C:\> $identity = Get-AzExpressRoutePortIdentity -ExpressRoutePort $exrPort
```

## <span data-ttu-id="5e3a5-109">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="5e3a5-109">PARAMETERS</span></span>

### <span data-ttu-id="5e3a5-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5e3a5-110">-DefaultProfile</span></span>
<span data-ttu-id="5e3a5-111">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="5e3a5-111">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5e3a5-112">-ExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="5e3a5-112">-ExpressRoutePort</span></span>
<span data-ttu-id="5e3a5-113">Porten ExpressRoute</span><span class="sxs-lookup"><span data-stu-id="5e3a5-113">The ExpressRoute Port</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSExpressRoutePort
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5e3a5-114">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5e3a5-114">CommonParameters</span></span>
<span data-ttu-id="5e3a5-115">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5e3a5-115">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5e3a5-116">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="5e3a5-116">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5e3a5-117">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="5e3a5-117">INPUTS</span></span>

### <span data-ttu-id="5e3a5-118">Microsoft. Azure. commands. Networks. Models. PSExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="5e3a5-118">Microsoft.Azure.Commands.Network.Models.PSExpressRoutePort</span></span>

## <span data-ttu-id="5e3a5-119">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="5e3a5-119">OUTPUTS</span></span>

### <span data-ttu-id="5e3a5-120">Microsoft. Azure. commands. Networks. Models. PSManagedServiceIdentity</span><span class="sxs-lookup"><span data-stu-id="5e3a5-120">Microsoft.Azure.Commands.Network.Models.PSManagedServiceIdentity</span></span>

## <span data-ttu-id="5e3a5-121">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="5e3a5-121">NOTES</span></span>

## <span data-ttu-id="5e3a5-122">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="5e3a5-122">RELATED LINKS</span></span>
[<span data-ttu-id="5e3a5-123">Set-AzExpressRoutePortIdentity</span><span class="sxs-lookup"><span data-stu-id="5e3a5-123">Set-AzExpressRoutePortIdentity</span></span>](./Set-AzExpressRoutePortIdentity.md)

[<span data-ttu-id="5e3a5-124">New-AzExpressRoutePortIdentity</span><span class="sxs-lookup"><span data-stu-id="5e3a5-124">New-AzExpressRoutePortIdentity</span></span>](./New-AzExpressRoutePortIdentity.md)

[<span data-ttu-id="5e3a5-125">Remove-AzExpressRoutePortIdentity</span><span class="sxs-lookup"><span data-stu-id="5e3a5-125">Remove-AzExpressRoutePortIdentity</span></span>](./Remove-AzExpressRoutePortIdentity.md)