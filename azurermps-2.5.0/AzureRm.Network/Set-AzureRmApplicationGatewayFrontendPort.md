---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 85C0A1C3-FC6D-496A-B6B5-8DC2A73B8032
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermapplicationgatewayfrontendport
schema: 2.0.0
ms.openlocfilehash: 83c29e3c059664d7848fe66bd8ad7bcc005a8d47
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93931153"
---
# <span data-ttu-id="b8144-101">Set-AzureRmApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="b8144-101">Set-AzureRmApplicationGatewayFrontendPort</span></span>

## <span data-ttu-id="b8144-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="b8144-102">SYNOPSIS</span></span>
<span data-ttu-id="b8144-103">Ändrar frontend-port för en Programgateway.</span><span class="sxs-lookup"><span data-stu-id="b8144-103">Modifies a front-end port for an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b8144-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="b8144-104">SYNTAX</span></span>

```
Set-AzureRmApplicationGatewayFrontendPort -ApplicationGateway <PSApplicationGateway> -Name <String>
 -Port <Int32> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b8144-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="b8144-105">DESCRIPTION</span></span>
<span data-ttu-id="b8144-106">Cmdleten **set-AzureRmApplicationGatewayFrontendPort** ändrar en front port för en Programgateway.</span><span class="sxs-lookup"><span data-stu-id="b8144-106">The **Set-AzureRmApplicationGatewayFrontendPort** cmdlet modifies a front-end port for an application gateway.</span></span>

## <span data-ttu-id="b8144-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="b8144-107">EXAMPLES</span></span>

### <span data-ttu-id="b8144-108">Exempel 1: Ange front-end-port för Application Gateway till 80</span><span class="sxs-lookup"><span data-stu-id="b8144-108">Example 1: Set an application gateway front-end port to 80</span></span>
```
PS C:\> $AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Set-AzureRmApplicationGatewayFrontendPort -ApplicationGateway $AppGw -Name "FrontEndPort01" -Port 80
```

<span data-ttu-id="b8144-109">Det första kommandot hämtar den Programgateway som heter ApplicationGateway01 som tillhör resurs gruppen med namnet ResourceGroup01 och lagrar den i $AppGw variabeln.</span><span class="sxs-lookup"><span data-stu-id="b8144-109">The first command gets the application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01 and stores it in the $AppGw variable.</span></span>

<span data-ttu-id="b8144-110">Det andra kommandot ändrar gatewayen i $AppGw så att port 80 används för front porten som heter FrontEndPort01.</span><span class="sxs-lookup"><span data-stu-id="b8144-110">The second command modifies the gateway in $AppGw to use port 80 for the front-end port named FrontEndPort01.</span></span>

## <span data-ttu-id="b8144-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="b8144-111">PARAMETERS</span></span>

### <span data-ttu-id="b8144-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="b8144-112">-ApplicationGateway</span></span>
<span data-ttu-id="b8144-113">Anger det Application Gateway-objekt som denna cmdlet associerar fram porten med.</span><span class="sxs-lookup"><span data-stu-id="b8144-113">Specifies the application gateway object with which this cmdlet associates the front-end port.</span></span>

```yaml
Type: PSApplicationGateway
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b8144-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b8144-114">-DefaultProfile</span></span>
<span data-ttu-id="b8144-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="b8144-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b8144-116">-Namn</span><span class="sxs-lookup"><span data-stu-id="b8144-116">-Name</span></span>
<span data-ttu-id="b8144-117">Anger namnet på den frontend-port som ska ändras.</span><span class="sxs-lookup"><span data-stu-id="b8144-117">Specifies the name of the front-end port to modify.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b8144-118">-Port</span><span class="sxs-lookup"><span data-stu-id="b8144-118">-Port</span></span>
<span data-ttu-id="b8144-119">Anger vilket port nummer som ska användas för front porten.</span><span class="sxs-lookup"><span data-stu-id="b8144-119">Specifies the port number to use for the front-end port.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b8144-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b8144-120">CommonParameters</span></span>
<span data-ttu-id="b8144-121">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b8144-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b8144-122">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b8144-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b8144-123">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="b8144-123">INPUTS</span></span>

### <span data-ttu-id="b8144-124">PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="b8144-124">PSApplicationGateway</span></span>
<span data-ttu-id="b8144-125">Parametern ' ApplicationGateway ' godkänner värdet av typen ' PSApplicationGateway ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="b8144-125">Parameter 'ApplicationGateway' accepts value of type 'PSApplicationGateway' from the pipeline</span></span>

## <span data-ttu-id="b8144-126">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="b8144-126">OUTPUTS</span></span>

### <span data-ttu-id="b8144-127">Microsoft. Azure. commands. Networks. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="b8144-127">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="b8144-128">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="b8144-128">NOTES</span></span>

## <span data-ttu-id="b8144-129">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="b8144-129">RELATED LINKS</span></span>

[<span data-ttu-id="b8144-130">Add-AzureRmApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="b8144-130">Add-AzureRmApplicationGatewayFrontendPort</span></span>](./Add-AzureRmApplicationGatewayFrontendPort.md)

[<span data-ttu-id="b8144-131">Get-AzureRmApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="b8144-131">Get-AzureRmApplicationGatewayFrontendPort</span></span>](./Get-AzureRmApplicationGatewayFrontendPort.md)

[<span data-ttu-id="b8144-132">New-AzureRmApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="b8144-132">New-AzureRmApplicationGatewayFrontendPort</span></span>](./New-AzureRmApplicationGatewayFrontendPort.md)

[<span data-ttu-id="b8144-133">Remove-AzureRmApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="b8144-133">Remove-AzureRmApplicationGatewayFrontendPort</span></span>](./Remove-AzureRmApplicationGatewayFrontendPort.md)
