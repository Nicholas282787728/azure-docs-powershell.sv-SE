---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 85C0A1C3-FC6D-496A-B6B5-8DC2A73B8032
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmApplicationGatewayFrontendPort.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmApplicationGatewayFrontendPort.md
ms.openlocfilehash: 1c6a5ffee2f4a8b358f483fee2904fe1a7a970da
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93573617"
---
# <span data-ttu-id="39774-101">Set-AzureRmApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="39774-101">Set-AzureRmApplicationGatewayFrontendPort</span></span>

## <span data-ttu-id="39774-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="39774-102">SYNOPSIS</span></span>
<span data-ttu-id="39774-103">Ändrar frontend-port för en Programgateway.</span><span class="sxs-lookup"><span data-stu-id="39774-103">Modifies a front-end port for an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="39774-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="39774-104">SYNTAX</span></span>

```
Set-AzureRmApplicationGatewayFrontendPort -ApplicationGateway <PSApplicationGateway> -Name <String>
 -Port <Int32> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="39774-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="39774-105">DESCRIPTION</span></span>
<span data-ttu-id="39774-106">Cmdleten **set-AzureRmApplicationGatewayFrontendPort** ändrar en front port för en Programgateway.</span><span class="sxs-lookup"><span data-stu-id="39774-106">The **Set-AzureRmApplicationGatewayFrontendPort** cmdlet modifies a front-end port for an application gateway.</span></span>

## <span data-ttu-id="39774-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="39774-107">EXAMPLES</span></span>

### <span data-ttu-id="39774-108">Exempel 1: Ange front-end-port för Application Gateway till 80</span><span class="sxs-lookup"><span data-stu-id="39774-108">Example 1: Set an application gateway front-end port to 80</span></span>
```
PS C:\> $AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Set-AzureRmApplicationGatewayFrontendPort -ApplicationGateway $AppGw -Name "FrontEndPort01" -Port 80
```

<span data-ttu-id="39774-109">Det första kommandot hämtar den Programgateway som heter ApplicationGateway01 som tillhör resurs gruppen med namnet ResourceGroup01 och lagrar den i $AppGw variabeln.</span><span class="sxs-lookup"><span data-stu-id="39774-109">The first command gets the application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01 and stores it in the $AppGw variable.</span></span>

<span data-ttu-id="39774-110">Det andra kommandot ändrar gatewayen i $AppGw så att port 80 används för front porten som heter FrontEndPort01.</span><span class="sxs-lookup"><span data-stu-id="39774-110">The second command modifies the gateway in $AppGw to use port 80 for the front-end port named FrontEndPort01.</span></span>

## <span data-ttu-id="39774-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="39774-111">PARAMETERS</span></span>

### <span data-ttu-id="39774-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="39774-112">-ApplicationGateway</span></span>
<span data-ttu-id="39774-113">Anger det Application Gateway-objekt som denna cmdlet associerar fram porten med.</span><span class="sxs-lookup"><span data-stu-id="39774-113">Specifies the application gateway object with which this cmdlet associates the front-end port.</span></span>

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

### <span data-ttu-id="39774-114">-Namn</span><span class="sxs-lookup"><span data-stu-id="39774-114">-Name</span></span>
<span data-ttu-id="39774-115">Anger namnet på den frontend-port som ska ändras.</span><span class="sxs-lookup"><span data-stu-id="39774-115">Specifies the name of the front-end port to modify.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="39774-116">-Port</span><span class="sxs-lookup"><span data-stu-id="39774-116">-Port</span></span>
<span data-ttu-id="39774-117">Anger vilket port nummer som ska användas för front porten.</span><span class="sxs-lookup"><span data-stu-id="39774-117">Specifies the port number to use for the front-end port.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="39774-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="39774-118">-DefaultProfile</span></span>
<span data-ttu-id="39774-119">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="39774-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="39774-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="39774-120">CommonParameters</span></span>
<span data-ttu-id="39774-121">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="39774-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="39774-122">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="39774-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="39774-123">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="39774-123">INPUTS</span></span>

### <span data-ttu-id="39774-124">PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="39774-124">PSApplicationGateway</span></span>
<span data-ttu-id="39774-125">Parametern ' ApplicationGateway ' godkänner värdet av typen ' PSApplicationGateway ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="39774-125">Parameter 'ApplicationGateway' accepts value of type 'PSApplicationGateway' from the pipeline</span></span>

## <span data-ttu-id="39774-126">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="39774-126">OUTPUTS</span></span>

### <span data-ttu-id="39774-127">Microsoft. Azure. commands. Networks. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="39774-127">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="39774-128">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="39774-128">NOTES</span></span>

## <span data-ttu-id="39774-129">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="39774-129">RELATED LINKS</span></span>

[<span data-ttu-id="39774-130">Add-AzureRmApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="39774-130">Add-AzureRmApplicationGatewayFrontendPort</span></span>](./Add-AzureRmApplicationGatewayFrontendPort.md)

[<span data-ttu-id="39774-131">Get-AzureRmApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="39774-131">Get-AzureRmApplicationGatewayFrontendPort</span></span>](./Get-AzureRmApplicationGatewayFrontendPort.md)

[<span data-ttu-id="39774-132">New-AzureRmApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="39774-132">New-AzureRmApplicationGatewayFrontendPort</span></span>](./New-AzureRmApplicationGatewayFrontendPort.md)

[<span data-ttu-id="39774-133">Remove-AzureRmApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="39774-133">Remove-AzureRmApplicationGatewayFrontendPort</span></span>](./Remove-AzureRmApplicationGatewayFrontendPort.md)
