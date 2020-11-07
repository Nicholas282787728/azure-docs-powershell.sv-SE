---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 364C41D0-A5DB-4AEF-853A-FE5A11AD9155
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermapplicationgatewayfrontendipconfig
schema: 2.0.0
ms.openlocfilehash: c138ced515932d158bb2a4a067ed405d8084db4e
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93929806"
---
# <span data-ttu-id="32ffd-101">Get-AzureRmApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="32ffd-101">Get-AzureRmApplicationGatewayFrontendIPConfig</span></span>

## <span data-ttu-id="32ffd-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="32ffd-102">SYNOPSIS</span></span>
<span data-ttu-id="32ffd-103">Hämtar klientens front-IP-konfiguration för en Programgateway.</span><span class="sxs-lookup"><span data-stu-id="32ffd-103">Gets the front-end IP configuration of an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="32ffd-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="32ffd-104">SYNTAX</span></span>

```
Get-AzureRmApplicationGatewayFrontendIPConfig [-Name <String>] -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="32ffd-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="32ffd-105">DESCRIPTION</span></span>
<span data-ttu-id="32ffd-106">Cmdleten **Get-AzureRmApplicationGatewayFrontendIPConfig** hämtar klientens front-IP-konfiguration för en Programgateway.</span><span class="sxs-lookup"><span data-stu-id="32ffd-106">The **Get-AzureRmApplicationGatewayFrontendIPConfig** cmdlet gets the front-end IP configuration of an application gateway.</span></span>

## <span data-ttu-id="32ffd-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="32ffd-107">EXAMPLES</span></span>

### <span data-ttu-id="32ffd-108">Exempel 1: Hämta en viss front-IP-konfiguration</span><span class="sxs-lookup"><span data-stu-id="32ffd-108">Example 1: Get a specified front-end IP configuration</span></span>
```
PS C:\>$AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $FrontEndIP= Get-AzureRmApplicationGatewayFrontendIPConfig -Name "FrontEndIP01" -ApplicationGateway $AppGw
```

<span data-ttu-id="32ffd-109">Det första kommandot får en Programgateway som heter ApplicationGateway01 från resurs gruppen med namnet ResourceGroup01 och lagrar den i $AppGw variabel. Det andra kommandot får klient konfigurationen front-end som heter FrontEndIP01 från $AppGw och lagrar den i $FrontEndIP-variabeln.</span><span class="sxs-lookup"><span data-stu-id="32ffd-109">The first command gets an application gateway named ApplicationGateway01 from the resource group named ResourceGroup01, and stores it in the $AppGw variable.The second command gets the front-end IP configuration named FrontEndIP01 from $AppGw and stores it in the $FrontEndIP variable.</span></span>

### <span data-ttu-id="32ffd-110">Exempel 2: Hämta en lista över front-IP-konfigurationer</span><span class="sxs-lookup"><span data-stu-id="32ffd-110">Example 2: Get a list of front-end IP configurations</span></span>
```
PS C:\>$AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $FrontEndIPs= Get-AzureRmApplicationGatewayFrontendIPConfig  -ApplicationGateway $AppGw
```

<span data-ttu-id="32ffd-111">Det första kommandot får en Programgateway som heter ApplicationGateway01 från resurs gruppen med namnet ResourceGroup01 och lagrar den i $AppGw variabel. Det andra kommandot får en lista med front-IP-konfigurationer från $AppGw och lagrar dem i $FrontEndIPs-variabeln.</span><span class="sxs-lookup"><span data-stu-id="32ffd-111">The first command gets an application gateway named ApplicationGateway01 from the resource group named ResourceGroup01, and stores it in the $AppGw variable.The second command gets a list of the front-end IP configurations from $AppGw and stores it in the $FrontEndIPs variable.</span></span>

## <span data-ttu-id="32ffd-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="32ffd-112">PARAMETERS</span></span>

### <span data-ttu-id="32ffd-113">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="32ffd-113">-ApplicationGateway</span></span>
<span data-ttu-id="32ffd-114">Anger det Application Gateway-objekt som innehåller front-IP-konfigurationen.</span><span class="sxs-lookup"><span data-stu-id="32ffd-114">Specifies the application gateway object that contains the front-end IP configuration.</span></span>

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

### <span data-ttu-id="32ffd-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="32ffd-115">-DefaultProfile</span></span>
<span data-ttu-id="32ffd-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="32ffd-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="32ffd-117">-Namn</span><span class="sxs-lookup"><span data-stu-id="32ffd-117">-Name</span></span>
<span data-ttu-id="32ffd-118">Anger namnet på den front-end IP-konfiguration som den här cmdleten får.</span><span class="sxs-lookup"><span data-stu-id="32ffd-118">Specifies the name of the front-end IP configuration that this cmdlet gets.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="32ffd-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="32ffd-119">CommonParameters</span></span>
<span data-ttu-id="32ffd-120">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="32ffd-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="32ffd-121">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="32ffd-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="32ffd-122">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="32ffd-122">INPUTS</span></span>

### <span data-ttu-id="32ffd-123">System. String</span><span class="sxs-lookup"><span data-stu-id="32ffd-123">System.String</span></span>

## <span data-ttu-id="32ffd-124">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="32ffd-124">OUTPUTS</span></span>

### <span data-ttu-id="32ffd-125">Microsoft. Azure. commands. Networks. Models. PSApplicationGatewayFrontendIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="32ffd-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFrontendIPConfiguration</span></span>

## <span data-ttu-id="32ffd-126">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="32ffd-126">NOTES</span></span>

## <span data-ttu-id="32ffd-127">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="32ffd-127">RELATED LINKS</span></span>

[<span data-ttu-id="32ffd-128">Add-AzureRmApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="32ffd-128">Add-AzureRmApplicationGatewayFrontendIPConfig</span></span>](./Add-AzureRmApplicationGatewayFrontendIPConfig.md)

[<span data-ttu-id="32ffd-129">New-AzureRmApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="32ffd-129">New-AzureRmApplicationGatewayFrontendIPConfig</span></span>](./New-AzureRmApplicationGatewayFrontendIPConfig.md)

[<span data-ttu-id="32ffd-130">Remove-AzureRmApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="32ffd-130">Remove-AzureRmApplicationGatewayFrontendIPConfig</span></span>](./Remove-AzureRmApplicationGatewayFrontendIPConfig.md)

[<span data-ttu-id="32ffd-131">Set-AzureRmApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="32ffd-131">Set-AzureRmApplicationGatewayFrontendIPConfig</span></span>](./Set-AzureRmApplicationGatewayFrontendIPConfig.md)


