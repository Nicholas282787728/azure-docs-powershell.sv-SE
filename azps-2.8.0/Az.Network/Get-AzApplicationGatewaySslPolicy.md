---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: AF02FFF8-F00D-4446-968F-F3C9008C39F0
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewaysslpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewaySslPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewaySslPolicy.md
ms.openlocfilehash: 6f93a66739fe1943182726e6998267d1e406f0a0
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93918784"
---
# <span data-ttu-id="add9f-101">Get-AzApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="add9f-101">Get-AzApplicationGatewaySslPolicy</span></span>

## <span data-ttu-id="add9f-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="add9f-102">SYNOPSIS</span></span>
<span data-ttu-id="add9f-103">Hämtar SSL-principen för en Programgateway.</span><span class="sxs-lookup"><span data-stu-id="add9f-103">Gets the SSL policy of an application gateway.</span></span>

## <span data-ttu-id="add9f-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="add9f-104">SYNTAX</span></span>

```
Get-AzApplicationGatewaySslPolicy -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="add9f-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="add9f-105">DESCRIPTION</span></span>
<span data-ttu-id="add9f-106">Cmdleten **Get-AzApplicationGatewaySslPolicy** hämtar SSL-principen för en Programgateway.</span><span class="sxs-lookup"><span data-stu-id="add9f-106">The **Get-AzApplicationGatewaySslPolicy** cmdlet gets the SSL policy of an application gateway.</span></span>

## <span data-ttu-id="add9f-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="add9f-107">EXAMPLES</span></span>

### <span data-ttu-id="add9f-108">9.1</span><span class="sxs-lookup"><span data-stu-id="add9f-108">1:</span></span>
```
PS C:\>$AppGW = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $sslpolicy = Get-AzApplicationGatewaySslPolicy -ApplicationGateway $AppGW
```

<span data-ttu-id="add9f-109">Med det första kommandot får programgatewayen namnet ApplicationGateway01 och lagras resultatet i variabeln som heter $AppGW.</span><span class="sxs-lookup"><span data-stu-id="add9f-109">The first command gets the Application Gateway named ApplicationGateway01 and stores the result in the variable named $AppGW.</span></span>
<span data-ttu-id="add9f-110">Det andra kommandot hämtar SSL-principen från den Application Gateway som lagras i variabeln $AppGW.</span><span class="sxs-lookup"><span data-stu-id="add9f-110">The second command gets the ssl policy from the Application Gateway stored in the variable named $AppGW.</span></span>

## <span data-ttu-id="add9f-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="add9f-111">PARAMETERS</span></span>

### <span data-ttu-id="add9f-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="add9f-112">-ApplicationGateway</span></span>
<span data-ttu-id="add9f-113">Anger Application Gateway för SSL-policyn som denna cmdlet får.</span><span class="sxs-lookup"><span data-stu-id="add9f-113">Specifies the application gateway of the SSL policy that this cmdlet gets.</span></span>

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

### <span data-ttu-id="add9f-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="add9f-114">-DefaultProfile</span></span>
<span data-ttu-id="add9f-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="add9f-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="add9f-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="add9f-116">CommonParameters</span></span>
<span data-ttu-id="add9f-117">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="add9f-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="add9f-118">Mer information finns i [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="add9f-118">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="add9f-119">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="add9f-119">INPUTS</span></span>

### <span data-ttu-id="add9f-120">Microsoft. Azure. commands. Networks. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="add9f-120">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="add9f-121">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="add9f-121">OUTPUTS</span></span>

### <span data-ttu-id="add9f-122">Microsoft. Azure. commands. Networks. Models. PSApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="add9f-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslPolicy</span></span>

## <span data-ttu-id="add9f-123">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="add9f-123">NOTES</span></span>
* <span data-ttu-id="add9f-124">Nyckelord: Azure, azurerm, arm, resurs, hantering, chef, nätverk, nätverk</span><span class="sxs-lookup"><span data-stu-id="add9f-124">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="add9f-125">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="add9f-125">RELATED LINKS</span></span>

[<span data-ttu-id="add9f-126">New-AzApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="add9f-126">New-AzApplicationGatewaySslPolicy</span></span>](./New-AzApplicationGatewaySslPolicy.md)

[<span data-ttu-id="add9f-127">Set-AzApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="add9f-127">Set-AzApplicationGatewaySslPolicy</span></span>](./Set-AzApplicationGatewaySslPolicy.md)

