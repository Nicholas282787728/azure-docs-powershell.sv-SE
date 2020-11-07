---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: AF02FFF8-F00D-4446-968F-F3C9008C39F0
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermapplicationgatewaysslpolicy
schema: 2.0.0
ms.openlocfilehash: 237df37605581adeeb45fdfbb7bae6449128aa7b
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93931313"
---
# <span data-ttu-id="932f6-101">Get-AzureRmApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="932f6-101">Get-AzureRmApplicationGatewaySslPolicy</span></span>

## <span data-ttu-id="932f6-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="932f6-102">SYNOPSIS</span></span>
<span data-ttu-id="932f6-103">Hämtar SSL-principen för en Programgateway.</span><span class="sxs-lookup"><span data-stu-id="932f6-103">Gets the SSL policy of an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="932f6-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="932f6-104">SYNTAX</span></span>

```
Get-AzureRmApplicationGatewaySslPolicy -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="932f6-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="932f6-105">DESCRIPTION</span></span>
<span data-ttu-id="932f6-106">Cmdleten **Get-AzureRmApplicationGatewaySslPolicy** hämtar SSL-principen för en Programgateway.</span><span class="sxs-lookup"><span data-stu-id="932f6-106">The **Get-AzureRmApplicationGatewaySslPolicy** cmdlet gets the SSL policy of an application gateway.</span></span>

## <span data-ttu-id="932f6-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="932f6-107">EXAMPLES</span></span>

### <span data-ttu-id="932f6-108">9.1</span><span class="sxs-lookup"><span data-stu-id="932f6-108">1:</span></span>
```
PS C:\>$AppGW = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $sslpolicy = Get-AzureRmApplicationGatewaySslPolicy -ApplicationGateway $AppGW
```

<span data-ttu-id="932f6-109">Med det första kommandot får programgatewayen namnet ApplicationGateway01 och lagras resultatet i variabeln som heter $AppGW.</span><span class="sxs-lookup"><span data-stu-id="932f6-109">The first command gets the Application Gateway named ApplicationGateway01 and stores the result in the variable named $AppGW.</span></span>
<span data-ttu-id="932f6-110">Det andra kommandot hämtar SSL-principen från den Application Gateway som lagras i variabeln $AppGW.</span><span class="sxs-lookup"><span data-stu-id="932f6-110">The second command gets the ssl policy from the Application Gateway stored in the variable named $AppGW.</span></span>

## <span data-ttu-id="932f6-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="932f6-111">PARAMETERS</span></span>

### <span data-ttu-id="932f6-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="932f6-112">-ApplicationGateway</span></span>
<span data-ttu-id="932f6-113">Anger Application Gateway för SSL-policyn som denna cmdlet får.</span><span class="sxs-lookup"><span data-stu-id="932f6-113">Specifies the application gateway of the SSL policy that this cmdlet gets.</span></span>

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

### <span data-ttu-id="932f6-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="932f6-114">-DefaultProfile</span></span>
<span data-ttu-id="932f6-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="932f6-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="932f6-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="932f6-116">CommonParameters</span></span>
<span data-ttu-id="932f6-117">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="932f6-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="932f6-118">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="932f6-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="932f6-119">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="932f6-119">INPUTS</span></span>

### <span data-ttu-id="932f6-120">System. String</span><span class="sxs-lookup"><span data-stu-id="932f6-120">System.String</span></span>

## <span data-ttu-id="932f6-121">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="932f6-121">OUTPUTS</span></span>

### <span data-ttu-id="932f6-122">Microsoft. Azure. commands. Networks. Models. PSApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="932f6-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslPolicy</span></span>

## <span data-ttu-id="932f6-123">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="932f6-123">NOTES</span></span>
* <span data-ttu-id="932f6-124">Nyckelord: Azure, azurerm, arm, resurs, hantering, chef, nätverk, nätverk</span><span class="sxs-lookup"><span data-stu-id="932f6-124">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="932f6-125">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="932f6-125">RELATED LINKS</span></span>

[<span data-ttu-id="932f6-126">New-AzureRmApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="932f6-126">New-AzureRmApplicationGatewaySslPolicy</span></span>](./New-AzureRmApplicationGatewaySslPolicy.md)

[<span data-ttu-id="932f6-127">Set-AzureRmApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="932f6-127">Set-AzureRmApplicationGatewaySslPolicy</span></span>](./Set-AzureRmApplicationGatewaySslPolicy.md)


