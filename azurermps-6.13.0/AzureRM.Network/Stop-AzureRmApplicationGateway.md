---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 2C9609E8-0D8B-471B-9F0E-672BF55C3A0E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/stop-azurermapplicationgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Stop-AzureRmApplicationGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Stop-AzureRmApplicationGateway.md
ms.openlocfilehash: a235ae8ad4467e135e85599300869bcb36805a30
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93756018"
---
# <span data-ttu-id="2fa79-101">Stop-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="2fa79-101">Stop-AzureRmApplicationGateway</span></span>

## <span data-ttu-id="2fa79-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="2fa79-102">SYNOPSIS</span></span>
<span data-ttu-id="2fa79-103">Stoppa en Programgateway</span><span class="sxs-lookup"><span data-stu-id="2fa79-103">Stops an application gateway</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2fa79-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="2fa79-104">SYNTAX</span></span>

```
Stop-AzureRmApplicationGateway -ApplicationGateway <PSApplicationGateway> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2fa79-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="2fa79-105">DESCRIPTION</span></span>
<span data-ttu-id="2fa79-106">Cmdleten **Stop-AzureRmApplicationGateway** stoppar en Programgateway.</span><span class="sxs-lookup"><span data-stu-id="2fa79-106">The **Stop-AzureRmApplicationGateway** cmdlet stops an application gateway.</span></span>

## <span data-ttu-id="2fa79-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="2fa79-107">EXAMPLES</span></span>

### <span data-ttu-id="2fa79-108">Exempel 1: stoppa en Programgateway</span><span class="sxs-lookup"><span data-stu-id="2fa79-108">Example 1: Stop an application gateway</span></span>
```
PS C:\>Stop-AzureRmApplicationGateway -ApplicationGateway $AppGw
```

<span data-ttu-id="2fa79-109">Det här kommandot stoppar programgatewayen som lagras i $AppGw variabel.</span><span class="sxs-lookup"><span data-stu-id="2fa79-109">This command stops the application gateway stored in the $AppGw variable.</span></span>

## <span data-ttu-id="2fa79-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="2fa79-110">PARAMETERS</span></span>

### <span data-ttu-id="2fa79-111">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="2fa79-111">-ApplicationGateway</span></span>
<span data-ttu-id="2fa79-112">Anger den Programgateway som denna cmdlet slutar.</span><span class="sxs-lookup"><span data-stu-id="2fa79-112">Specifies the application gateway that this cmdlet stops.</span></span>

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

### <span data-ttu-id="2fa79-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="2fa79-113">-AsJob</span></span>
<span data-ttu-id="2fa79-114">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="2fa79-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="2fa79-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2fa79-115">-DefaultProfile</span></span>
<span data-ttu-id="2fa79-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="2fa79-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2fa79-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2fa79-117">CommonParameters</span></span>
<span data-ttu-id="2fa79-118">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2fa79-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2fa79-119">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2fa79-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2fa79-120">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="2fa79-120">INPUTS</span></span>

### <span data-ttu-id="2fa79-121">Microsoft. Azure. commands. Networks. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="2fa79-121">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>
<span data-ttu-id="2fa79-122">Parametrar: ApplicationGateway (ByValue)</span><span class="sxs-lookup"><span data-stu-id="2fa79-122">Parameters: ApplicationGateway (ByValue)</span></span>

## <span data-ttu-id="2fa79-123">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="2fa79-123">OUTPUTS</span></span>

### <span data-ttu-id="2fa79-124">Microsoft. Azure. commands. Networks. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="2fa79-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="2fa79-125">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="2fa79-125">NOTES</span></span>

## <span data-ttu-id="2fa79-126">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="2fa79-126">RELATED LINKS</span></span>

[<span data-ttu-id="2fa79-127">Get-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="2fa79-127">Get-AzureRmApplicationGateway</span></span>](./Get-AzureRmApplicationGateway.md)

[<span data-ttu-id="2fa79-128">New-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="2fa79-128">New-AzureRmApplicationGateway</span></span>](./New-AzureRmApplicationGateway.md)

[<span data-ttu-id="2fa79-129">Remove-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="2fa79-129">Remove-AzureRmApplicationGateway</span></span>](./Remove-AzureRmApplicationGateway.md)

[<span data-ttu-id="2fa79-130">Set-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="2fa79-130">Set-AzureRmApplicationGateway</span></span>](./Set-AzureRmApplicationGateway.md)

[<span data-ttu-id="2fa79-131">Start-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="2fa79-131">Start-AzureRmApplicationGateway</span></span>](./Start-AzureRmApplicationGateway.md)


