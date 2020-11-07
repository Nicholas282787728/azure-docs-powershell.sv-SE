---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmApplicationGatewayRedirectConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmApplicationGatewayRedirectConfiguration.md
ms.openlocfilehash: 66da90ea590c4d2359dbe7e703667f9fe7189fba
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93755437"
---
# <span data-ttu-id="bbca8-101">Get-AzureRmApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="bbca8-101">Get-AzureRmApplicationGatewayRedirectConfiguration</span></span>

## <span data-ttu-id="bbca8-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="bbca8-102">SYNOPSIS</span></span>
<span data-ttu-id="bbca8-103">Hämtar en befintlig konfiguration för omdirigering från en Programgateway.</span><span class="sxs-lookup"><span data-stu-id="bbca8-103">Gets an existing redirect configuration from an Application Gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bbca8-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="bbca8-104">SYNTAX</span></span>

```
Get-AzureRmApplicationGatewayRedirectConfiguration [-Name <String>] -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bbca8-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="bbca8-105">DESCRIPTION</span></span>
<span data-ttu-id="bbca8-106">Cmdleten **Get-AzureRmApplicationGatewayRedirectConfiguration** hämtar en befintlig konfiguration för omdirigering från en Programgateway.</span><span class="sxs-lookup"><span data-stu-id="bbca8-106">The **Get-AzureRmApplicationGatewayRedirectConfiguration** cmdlet gets an existing redirect configuration from an Application Gateway.</span></span>

## <span data-ttu-id="bbca8-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="bbca8-107">EXAMPLES</span></span>

### <span data-ttu-id="bbca8-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="bbca8-108">Example 1</span></span>
```
PS C:\>$AppGW = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $RedirectConfig = Get-AzureRmApplicationGatewayRedirectConfiguration -Name "Redirect01" -ApplicationGateway $AppGW
```

<span data-ttu-id="bbca8-109">Med det första kommandot får programgatewayen namnet ApplicationGateway01 och lagras resultatet i variabeln som heter $AppGW.</span><span class="sxs-lookup"><span data-stu-id="bbca8-109">The first command gets the Application Gateway named ApplicationGateway01 and stores the result in the variable named $AppGW.</span></span>
<span data-ttu-id="bbca8-110">Det andra kommandot får till gång till omdirigeringsvariabler med namnet Redirect01 från Application Gateway som lagras i variabeln $AppGW.</span><span class="sxs-lookup"><span data-stu-id="bbca8-110">The second command gets the redirect configuration named Redirect01 from the Application Gateway stored in the variable named $AppGW.</span></span>

## <span data-ttu-id="bbca8-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="bbca8-111">PARAMETERS</span></span>

### <span data-ttu-id="bbca8-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="bbca8-112">-ApplicationGateway</span></span>
<span data-ttu-id="bbca8-113">ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="bbca8-113">The applicationGateway</span></span>

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

### <span data-ttu-id="bbca8-114">-Namn</span><span class="sxs-lookup"><span data-stu-id="bbca8-114">-Name</span></span>
<span data-ttu-id="bbca8-115">Namnet på regeln för anslutningsbegäran</span><span class="sxs-lookup"><span data-stu-id="bbca8-115">The name of the request routing rule</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bbca8-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bbca8-116">-DefaultProfile</span></span>
<span data-ttu-id="bbca8-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="bbca8-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bbca8-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bbca8-118">CommonParameters</span></span>
<span data-ttu-id="bbca8-119">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bbca8-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bbca8-120">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bbca8-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bbca8-121">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="bbca8-121">INPUTS</span></span>

### <span data-ttu-id="bbca8-122">Microsoft. Azure. commands. Networks. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="bbca8-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="bbca8-123">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="bbca8-123">OUTPUTS</span></span>

### <span data-ttu-id="bbca8-124">Microsoft. Azure. commands. Networks. Models. PSApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="bbca8-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRedirectConfiguration</span></span>
<span data-ttu-id="bbca8-125">System. Collections. Generic. IEnumerable ' 1 [[Microsoft. Azure. commands. Network. Models. PSApplicationGatewayRedirectConfiguration, Microsoft. Azure. commands. Network, version = 4.1.0.0, Culture = neutralt, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="bbca8-125">System.Collections.Generic.IEnumerable\`1[[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRedirectConfiguration, Microsoft.Azure.Commands.Network, Version=4.1.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="bbca8-126">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="bbca8-126">NOTES</span></span>

## <span data-ttu-id="bbca8-127">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="bbca8-127">RELATED LINKS</span></span>

