---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmApplicationGatewayConnectionDraining.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmApplicationGatewayConnectionDraining.md
ms.openlocfilehash: 12667316df99e19fbc0535a2b5e3fca3082d4484
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93574572"
---
# <span data-ttu-id="f8564-101">Remove-AzureRmApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="f8564-101">Remove-AzureRmApplicationGatewayConnectionDraining</span></span>

## <span data-ttu-id="f8564-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="f8564-102">SYNOPSIS</span></span>
<span data-ttu-id="f8564-103">Tar bort anslutningen tömning av ett objekt för HTTP-inställningar för backend.</span><span class="sxs-lookup"><span data-stu-id="f8564-103">Removes the connection draining configuration of a back-end HTTP settings object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f8564-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="f8564-104">SYNTAX</span></span>

```
Remove-AzureRmApplicationGatewayConnectionDraining
 -BackendHttpSettings <PSApplicationGatewayBackendHttpSettings> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="f8564-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="f8564-105">DESCRIPTION</span></span>
<span data-ttu-id="f8564-106">Cmdleten **Remove-AzureRmApplicationGatewayConnectionDraining** tar bort anslutningen som tömmer konfigurationen för ett objekt med http-inställningar för backend.</span><span class="sxs-lookup"><span data-stu-id="f8564-106">The **Remove-AzureRmApplicationGatewayConnectionDraining** cmdlet removes the connection draining configuration of a back-end HTTP settings object.</span></span>

## <span data-ttu-id="f8564-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="f8564-107">EXAMPLES</span></span>

### <span data-ttu-id="f8564-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="f8564-108">Example 1</span></span>
```
PS C:\> $AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Settings  = Get-AzureRmApplicationGatewayBackendHttpSettings -Name "Settings01" -ApplicationGateway $AppGw
PS C:\> Remove-AzureRmApplicationGatewayConnectionDraining -BackendHttpSettings $Settings
```

<span data-ttu-id="f8564-109">Det första kommandot får den Programgateway som heter ApplicationGateway01 i resurs gruppen som heter ResourceGroup01 och lagrar den i $AppGw variabeln.</span><span class="sxs-lookup"><span data-stu-id="f8564-109">The first command gets the application gateway named ApplicationGateway01 in the resource group named ResourceGroup01 and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="f8564-110">Det andra kommandot får de backend-HTTP-inställningarna "Settings01" för $AppGw och lagrar inställningarna i $Settings-variabeln.</span><span class="sxs-lookup"><span data-stu-id="f8564-110">The second command gets the back-end HTTP settings named Settings01 for $AppGw and stores the settings in the $Settings variable.</span></span>
<span data-ttu-id="f8564-111">Med kommandot senaste tar du bort anslutningen tömning av backend HTTP-inställningar som lagras i $Settings.</span><span class="sxs-lookup"><span data-stu-id="f8564-111">The last command removes the connection draining configuration of the back-end HTTP settings stored in $Settings.</span></span>

## <span data-ttu-id="f8564-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="f8564-112">PARAMETERS</span></span>

### <span data-ttu-id="f8564-113">-BackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="f8564-113">-BackendHttpSettings</span></span>
<span data-ttu-id="f8564-114">Server delens http-inställningar</span><span class="sxs-lookup"><span data-stu-id="f8564-114">The backend http settings</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendHttpSettings
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f8564-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f8564-115">-DefaultProfile</span></span>
<span data-ttu-id="f8564-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="f8564-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f8564-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f8564-117">CommonParameters</span></span>
<span data-ttu-id="f8564-118">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f8564-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f8564-119">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f8564-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f8564-120">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="f8564-120">INPUTS</span></span>

### <span data-ttu-id="f8564-121">Microsoft. Azure. commands. Networks. Models. PSApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="f8564-121">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendHttpSettings</span></span>

## <span data-ttu-id="f8564-122">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="f8564-122">OUTPUTS</span></span>

### <span data-ttu-id="f8564-123">Microsoft. Azure. commands. Networks. Models. PSApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="f8564-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendHttpSettings</span></span>

## <span data-ttu-id="f8564-124">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="f8564-124">NOTES</span></span>

## <span data-ttu-id="f8564-125">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="f8564-125">RELATED LINKS</span></span>

[<span data-ttu-id="f8564-126">Get-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="f8564-126">Get-AzureRmApplicationGateway</span></span>](./Get-AzureRmApplicationGateway.md)

[<span data-ttu-id="f8564-127">Get-AzureRmApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="f8564-127">Get-AzureRmApplicationGatewayBackendHttpSettings</span></span>](./Get-AzureRmApplicationGatewayBackendHttpSettings.md)

[<span data-ttu-id="f8564-128">Get-AzureRmApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="f8564-128">Get-AzureRmApplicationGatewayConnectionDraining</span></span>](./Get-AzureRmApplicationGatewayConnectionDraining.md)

[<span data-ttu-id="f8564-129">New-AzureRmApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="f8564-129">New-AzureRmApplicationGatewayConnectionDraining</span></span>](./New-AzureRmApplicationGatewayConnectionDraining.md)

[<span data-ttu-id="f8564-130">Set-AzureRmApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="f8564-130">Set-AzureRmApplicationGatewayConnectionDraining</span></span>](./Set-AzureRmApplicationGatewayConnectionDraining.md)

