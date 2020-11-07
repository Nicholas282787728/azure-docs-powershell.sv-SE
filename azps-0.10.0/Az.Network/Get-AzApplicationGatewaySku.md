---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: F01CB88A-49E7-41D8-B4E7-F1A4DCDC6B84
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewaysku
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzApplicationGatewaySku.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzApplicationGatewaySku.md
ms.openlocfilehash: e8ad9974096f633cd829c4d933f092fd869a4103
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93922318"
---
# <span data-ttu-id="af2eb-101">Get-AzApplicationGatewaySku</span><span class="sxs-lookup"><span data-stu-id="af2eb-101">Get-AzApplicationGatewaySku</span></span>

## <span data-ttu-id="af2eb-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="af2eb-102">SYNOPSIS</span></span>
<span data-ttu-id="af2eb-103">Hämtar SKU för en Programgateway.</span><span class="sxs-lookup"><span data-stu-id="af2eb-103">Gets the SKU of an application gateway.</span></span>

## <span data-ttu-id="af2eb-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="af2eb-104">SYNTAX</span></span>

```
Get-AzApplicationGatewaySku -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="af2eb-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="af2eb-105">DESCRIPTION</span></span>
<span data-ttu-id="af2eb-106">Cmdleten **Get-AzApplicationGatewaySku** hämtar lager behållnings enheten (SKU) för en Programgateway.</span><span class="sxs-lookup"><span data-stu-id="af2eb-106">The **Get-AzApplicationGatewaySku** cmdlet gets the stock keeping unit (SKU) of an application gateway.</span></span>

## <span data-ttu-id="af2eb-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="af2eb-107">EXAMPLES</span></span>

### <span data-ttu-id="af2eb-108">Exempel 1: skaffa en Application Gateway SKU</span><span class="sxs-lookup"><span data-stu-id="af2eb-108">Example 1: Get an application gateway SKU</span></span>
```
PS C:\>$AppGW = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $SKU = Get-AzApplicationGatewaySku -ApplicationGateway $AppGW
```

<span data-ttu-id="af2eb-109">Med det första kommandot får programgatewayen namnet ApplicationGateway01 och lagras resultatet i variabeln som heter $AppGW.</span><span class="sxs-lookup"><span data-stu-id="af2eb-109">The first command gets the Application Gateway named ApplicationGateway01 and stores the result in the variable named $AppGW.</span></span>
<span data-ttu-id="af2eb-110">Det andra kommandot får SKU för en Programgateway som heter ApplicationGateway01 och lagrar resultatet i variabeln som heter $SKU.</span><span class="sxs-lookup"><span data-stu-id="af2eb-110">The second command gets the SKU of an application gateway named ApplicationGateway01 and stores the result in the variable named $SKU.</span></span>

## <span data-ttu-id="af2eb-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="af2eb-111">PARAMETERS</span></span>

### <span data-ttu-id="af2eb-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="af2eb-112">-ApplicationGateway</span></span>
<span data-ttu-id="af2eb-113">Anger Application Gateway-objekt.</span><span class="sxs-lookup"><span data-stu-id="af2eb-113">Specifies the application gateway object.</span></span>

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

### <span data-ttu-id="af2eb-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="af2eb-114">-DefaultProfile</span></span>
<span data-ttu-id="af2eb-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="af2eb-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="af2eb-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="af2eb-116">CommonParameters</span></span>
<span data-ttu-id="af2eb-117">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="af2eb-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="af2eb-118">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="af2eb-118">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="af2eb-119">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="af2eb-119">INPUTS</span></span>

### <span data-ttu-id="af2eb-120">System. String</span><span class="sxs-lookup"><span data-stu-id="af2eb-120">System.String</span></span>

## <span data-ttu-id="af2eb-121">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="af2eb-121">OUTPUTS</span></span>

### <span data-ttu-id="af2eb-122">Microsoft. Azure. commands. Networks. Models. PSApplicationGatewaySku</span><span class="sxs-lookup"><span data-stu-id="af2eb-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySku</span></span>

## <span data-ttu-id="af2eb-123">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="af2eb-123">NOTES</span></span>

## <span data-ttu-id="af2eb-124">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="af2eb-124">RELATED LINKS</span></span>

[<span data-ttu-id="af2eb-125">New-AzApplicationGatewaySku</span><span class="sxs-lookup"><span data-stu-id="af2eb-125">New-AzApplicationGatewaySku</span></span>](./New-AzApplicationGatewaySku.md)

[<span data-ttu-id="af2eb-126">Set-AzApplicationGatewaySku</span><span class="sxs-lookup"><span data-stu-id="af2eb-126">Set-AzApplicationGatewaySku</span></span>](./Set-AzApplicationGatewaySku.md)


