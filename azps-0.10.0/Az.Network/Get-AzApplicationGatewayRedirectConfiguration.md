---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewayredirectconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzApplicationGatewayRedirectConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzApplicationGatewayRedirectConfiguration.md
ms.openlocfilehash: c9443c93745c1f6db9372b8f845f3ac399e51398
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93922316"
---
# <span data-ttu-id="c605d-101">Get-AzApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="c605d-101">Get-AzApplicationGatewayRedirectConfiguration</span></span>

## <span data-ttu-id="c605d-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="c605d-102">SYNOPSIS</span></span>
<span data-ttu-id="c605d-103">Hämtar en befintlig konfiguration för omdirigering från en Programgateway.</span><span class="sxs-lookup"><span data-stu-id="c605d-103">Gets an existing redirect configuration from an Application Gateway.</span></span>

## <span data-ttu-id="c605d-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="c605d-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayRedirectConfiguration [-Name <String>] -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c605d-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="c605d-105">DESCRIPTION</span></span>
<span data-ttu-id="c605d-106">Cmdleten **Get-AzApplicationGatewayRedirectConfiguration** hämtar en befintlig konfiguration för omdirigering från en Programgateway.</span><span class="sxs-lookup"><span data-stu-id="c605d-106">The **Get-AzApplicationGatewayRedirectConfiguration** cmdlet gets an existing redirect configuration from an Application Gateway.</span></span>

## <span data-ttu-id="c605d-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="c605d-107">EXAMPLES</span></span>

### <span data-ttu-id="c605d-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="c605d-108">Example 1</span></span>
```
PS C:\>$AppGW = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $RedirectConfig = Get-AzApplicationGatewayRedirectConfiguration -Name "Redirect01" -ApplicationGateway $AppGW
```

<span data-ttu-id="c605d-109">Med det första kommandot får programgatewayen namnet ApplicationGateway01 och lagras resultatet i variabeln som heter $AppGW.</span><span class="sxs-lookup"><span data-stu-id="c605d-109">The first command gets the Application Gateway named ApplicationGateway01 and stores the result in the variable named $AppGW.</span></span>
<span data-ttu-id="c605d-110">Det andra kommandot får till gång till omdirigeringsvariabler med namnet Redirect01 från Application Gateway som lagras i variabeln $AppGW.</span><span class="sxs-lookup"><span data-stu-id="c605d-110">The second command gets the redirect configuration named Redirect01 from the Application Gateway stored in the variable named $AppGW.</span></span>

## <span data-ttu-id="c605d-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="c605d-111">PARAMETERS</span></span>

### <span data-ttu-id="c605d-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="c605d-112">-ApplicationGateway</span></span>
<span data-ttu-id="c605d-113">ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="c605d-113">The applicationGateway</span></span>

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

### <span data-ttu-id="c605d-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c605d-114">-DefaultProfile</span></span>
<span data-ttu-id="c605d-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="c605d-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c605d-116">-Namn</span><span class="sxs-lookup"><span data-stu-id="c605d-116">-Name</span></span>
<span data-ttu-id="c605d-117">Namnet på regeln för anslutningsbegäran</span><span class="sxs-lookup"><span data-stu-id="c605d-117">The name of the request routing rule</span></span>

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

### <span data-ttu-id="c605d-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c605d-118">CommonParameters</span></span>
<span data-ttu-id="c605d-119">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c605d-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c605d-120">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c605d-120">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c605d-121">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="c605d-121">INPUTS</span></span>

### <span data-ttu-id="c605d-122">Microsoft. Azure. commands. Networks. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="c605d-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="c605d-123">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="c605d-123">OUTPUTS</span></span>

### <span data-ttu-id="c605d-124">Microsoft. Azure. commands. Networks. Models. PSApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="c605d-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRedirectConfiguration</span></span>
<span data-ttu-id="c605d-125">System. Collections. Generic. IEnumerable ' 1 [[Microsoft. Azure. commands. Network. Models. PSApplicationGatewayRedirectConfiguration, Microsoft. Azure. commands. Network, version = 4.1.0.0, Culture = neutralt, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="c605d-125">System.Collections.Generic.IEnumerable\`1[[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRedirectConfiguration, Microsoft.Azure.Commands.Network, Version=4.1.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="c605d-126">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="c605d-126">NOTES</span></span>

## <span data-ttu-id="c605d-127">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="c605d-127">RELATED LINKS</span></span>

