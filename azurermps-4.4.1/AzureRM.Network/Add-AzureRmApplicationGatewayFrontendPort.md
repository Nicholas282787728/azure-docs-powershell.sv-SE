---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 40198C86-A4EB-494A-86D5-DF632518EB95
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmApplicationGatewayFrontendPort.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmApplicationGatewayFrontendPort.md
ms.openlocfilehash: 06b7c1fdbd83d90e595683612555c1dca67f23ea
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93584652"
---
# <span data-ttu-id="3ddc6-101">Add-AzureRmApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="3ddc6-101">Add-AzureRmApplicationGatewayFrontendPort</span></span>

## <span data-ttu-id="3ddc6-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="3ddc6-102">SYNOPSIS</span></span>
<span data-ttu-id="3ddc6-103">Lägger till en frontend-port till en programport.</span><span class="sxs-lookup"><span data-stu-id="3ddc6-103">Adds a front-end port to an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3ddc6-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="3ddc6-104">SYNTAX</span></span>

```
Add-AzureRmApplicationGatewayFrontendPort -ApplicationGateway <PSApplicationGateway> -Name <String>
 -Port <Int32> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3ddc6-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="3ddc6-105">DESCRIPTION</span></span>
<span data-ttu-id="3ddc6-106">Cmdleten **Add-AzureRmApplicationGatewayFrontendPort** lägger till en frontend-port till en Programgateway.</span><span class="sxs-lookup"><span data-stu-id="3ddc6-106">The **Add-AzureRmApplicationGatewayFrontendPort** cmdlet adds a front-end port to an application gateway.</span></span>

## <span data-ttu-id="3ddc6-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="3ddc6-107">EXAMPLES</span></span>

### <span data-ttu-id="3ddc6-108">Exempel 1: lägga till en front port i en Programgateway</span><span class="sxs-lookup"><span data-stu-id="3ddc6-108">Example 1: Add a front-end port to an application gateway</span></span>
```
PS C:\>$AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $ AppGw = Add-AzureRmApplicationGatewayFrontendPort -ApplicationGateway $AppGw -Name "FrontEndPort01" -Port 80
```

<span data-ttu-id="3ddc6-109">Det första kommandot hämtar den Programgateway som heter ApplicationGateway01 som tillhör resurs gruppen med namnet ResourceGroup01 och lagrar den i $AppGw variabeln.</span><span class="sxs-lookup"><span data-stu-id="3ddc6-109">The first command gets the application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01 and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="3ddc6-110">Det andra kommandot lägger till port 80 som front port för programgatewayen som lagras i $AppGw och namnger porten FrontEndPort01.</span><span class="sxs-lookup"><span data-stu-id="3ddc6-110">The second command adds port 80 as a front-end port for the application gateway stored in $AppGw and names the port FrontEndPort01.</span></span>

## <span data-ttu-id="3ddc6-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="3ddc6-111">PARAMETERS</span></span>

### <span data-ttu-id="3ddc6-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="3ddc6-112">-ApplicationGateway</span></span>
<span data-ttu-id="3ddc6-113">Anger den Programgateway till vilken denna cmdlet lägger till en front port.</span><span class="sxs-lookup"><span data-stu-id="3ddc6-113">Specifies the application gateway to which this cmdlet adds a front-end port.</span></span>

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

### <span data-ttu-id="3ddc6-114">-Namn</span><span class="sxs-lookup"><span data-stu-id="3ddc6-114">-Name</span></span>
<span data-ttu-id="3ddc6-115">Anger namnet på front porten.</span><span class="sxs-lookup"><span data-stu-id="3ddc6-115">Specifies the name of the front-end port.</span></span>

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

### <span data-ttu-id="3ddc6-116">-Port</span><span class="sxs-lookup"><span data-stu-id="3ddc6-116">-Port</span></span>
<span data-ttu-id="3ddc6-117">Anger port numret.</span><span class="sxs-lookup"><span data-stu-id="3ddc6-117">Specifies the port number.</span></span>

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

### <span data-ttu-id="3ddc6-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3ddc6-118">-DefaultProfile</span></span>
<span data-ttu-id="3ddc6-119">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="3ddc6-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3ddc6-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3ddc6-120">CommonParameters</span></span>
<span data-ttu-id="3ddc6-121">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3ddc6-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3ddc6-122">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3ddc6-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3ddc6-123">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="3ddc6-123">INPUTS</span></span>

### <span data-ttu-id="3ddc6-124">System. String</span><span class="sxs-lookup"><span data-stu-id="3ddc6-124">System.String</span></span>

## <span data-ttu-id="3ddc6-125">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="3ddc6-125">OUTPUTS</span></span>

### <span data-ttu-id="3ddc6-126">Microsoft. Azure. commands. Networks. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="3ddc6-126">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="3ddc6-127">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="3ddc6-127">NOTES</span></span>

## <span data-ttu-id="3ddc6-128">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="3ddc6-128">RELATED LINKS</span></span>

[<span data-ttu-id="3ddc6-129">Get-AzureRmApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="3ddc6-129">Get-AzureRmApplicationGatewayFrontendPort</span></span>](./Get-AzureRmApplicationGatewayFrontendPort.md)

[<span data-ttu-id="3ddc6-130">New-AzureRmApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="3ddc6-130">New-AzureRmApplicationGatewayFrontendPort</span></span>](./New-AzureRmApplicationGatewayFrontendPort.md)

[<span data-ttu-id="3ddc6-131">Remove-AzureRmApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="3ddc6-131">Remove-AzureRmApplicationGatewayFrontendPort</span></span>](./Remove-AzureRmApplicationGatewayFrontendPort.md)

[<span data-ttu-id="3ddc6-132">Set-AzureRmApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="3ddc6-132">Set-AzureRmApplicationGatewayFrontendPort</span></span>](./Set-AzureRmApplicationGatewayFrontendPort.md)


