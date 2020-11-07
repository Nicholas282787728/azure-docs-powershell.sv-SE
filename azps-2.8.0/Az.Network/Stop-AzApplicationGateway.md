---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 2C9609E8-0D8B-471B-9F0E-672BF55C3A0E
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/stop-azapplicationgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Stop-AzApplicationGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Stop-AzApplicationGateway.md
ms.openlocfilehash: 921c770cce5d1f597fa0af96dd30014f9dacb2fc
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93919445"
---
# <span data-ttu-id="983dc-101">Stop-AzApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="983dc-101">Stop-AzApplicationGateway</span></span>

## <span data-ttu-id="983dc-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="983dc-102">SYNOPSIS</span></span>
<span data-ttu-id="983dc-103">Stoppa en Programgateway</span><span class="sxs-lookup"><span data-stu-id="983dc-103">Stops an application gateway</span></span>

## <span data-ttu-id="983dc-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="983dc-104">SYNTAX</span></span>

```
Stop-AzApplicationGateway -ApplicationGateway <PSApplicationGateway> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="983dc-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="983dc-105">DESCRIPTION</span></span>
<span data-ttu-id="983dc-106">Cmdleten **Stop-AzApplicationGateway** stoppar en Programgateway.</span><span class="sxs-lookup"><span data-stu-id="983dc-106">The **Stop-AzApplicationGateway** cmdlet stops an application gateway.</span></span>

## <span data-ttu-id="983dc-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="983dc-107">EXAMPLES</span></span>

### <span data-ttu-id="983dc-108">Exempel 1: stoppa en Programgateway</span><span class="sxs-lookup"><span data-stu-id="983dc-108">Example 1: Stop an application gateway</span></span>
```
PS C:\>Stop-AzApplicationGateway -ApplicationGateway $AppGw
```

<span data-ttu-id="983dc-109">Det här kommandot stoppar programgatewayen som lagras i $AppGw variabel.</span><span class="sxs-lookup"><span data-stu-id="983dc-109">This command stops the application gateway stored in the $AppGw variable.</span></span>

## <span data-ttu-id="983dc-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="983dc-110">PARAMETERS</span></span>

### <span data-ttu-id="983dc-111">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="983dc-111">-ApplicationGateway</span></span>
<span data-ttu-id="983dc-112">Anger den Programgateway som denna cmdlet slutar.</span><span class="sxs-lookup"><span data-stu-id="983dc-112">Specifies the application gateway that this cmdlet stops.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGateway
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="983dc-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="983dc-113">-AsJob</span></span>
<span data-ttu-id="983dc-114">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="983dc-114">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="983dc-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="983dc-115">-DefaultProfile</span></span>
<span data-ttu-id="983dc-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="983dc-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="983dc-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="983dc-117">CommonParameters</span></span>
<span data-ttu-id="983dc-118">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="983dc-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="983dc-119">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="983dc-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="983dc-120">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="983dc-120">INPUTS</span></span>

### <span data-ttu-id="983dc-121">Microsoft. Azure. commands. Networks. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="983dc-121">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="983dc-122">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="983dc-122">OUTPUTS</span></span>

### <span data-ttu-id="983dc-123">Microsoft. Azure. commands. Networks. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="983dc-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="983dc-124">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="983dc-124">NOTES</span></span>

## <span data-ttu-id="983dc-125">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="983dc-125">RELATED LINKS</span></span>

[<span data-ttu-id="983dc-126">Get-AzApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="983dc-126">Get-AzApplicationGateway</span></span>](./Get-AzApplicationGateway.md)

[<span data-ttu-id="983dc-127">New-AzApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="983dc-127">New-AzApplicationGateway</span></span>](./New-AzApplicationGateway.md)

[<span data-ttu-id="983dc-128">Remove-AzApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="983dc-128">Remove-AzApplicationGateway</span></span>](./Remove-AzApplicationGateway.md)

[<span data-ttu-id="983dc-129">Set-AzApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="983dc-129">Set-AzApplicationGateway</span></span>](./Set-AzApplicationGateway.md)

[<span data-ttu-id="983dc-130">Start-AzApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="983dc-130">Start-AzApplicationGateway</span></span>](./Start-AzApplicationGateway.md)


