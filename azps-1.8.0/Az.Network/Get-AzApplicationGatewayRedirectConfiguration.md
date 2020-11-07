---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewayredirectconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayRedirectConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayRedirectConfiguration.md
ms.openlocfilehash: 79a4e76f4c9ece74c25c8f017fab6840aac63a9a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93748367"
---
# <span data-ttu-id="7ac79-101">Get-AzApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="7ac79-101">Get-AzApplicationGatewayRedirectConfiguration</span></span>

## <span data-ttu-id="7ac79-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="7ac79-102">SYNOPSIS</span></span>
<span data-ttu-id="7ac79-103">Hämtar en befintlig konfiguration för omdirigering från en Programgateway.</span><span class="sxs-lookup"><span data-stu-id="7ac79-103">Gets an existing redirect configuration from an Application Gateway.</span></span>

## <span data-ttu-id="7ac79-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="7ac79-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayRedirectConfiguration [-Name <String>] -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7ac79-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="7ac79-105">DESCRIPTION</span></span>
<span data-ttu-id="7ac79-106">Cmdleten **Get-AzApplicationGatewayRedirectConfiguration** hämtar en befintlig konfiguration för omdirigering från en Programgateway.</span><span class="sxs-lookup"><span data-stu-id="7ac79-106">The **Get-AzApplicationGatewayRedirectConfiguration** cmdlet gets an existing redirect configuration from an Application Gateway.</span></span>

## <span data-ttu-id="7ac79-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="7ac79-107">EXAMPLES</span></span>

### <span data-ttu-id="7ac79-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="7ac79-108">Example 1</span></span>
```
PS C:\>$AppGW = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $RedirectConfig = Get-AzApplicationGatewayRedirectConfiguration -Name "Redirect01" -ApplicationGateway $AppGW
```

<span data-ttu-id="7ac79-109">Med det första kommandot får programgatewayen namnet ApplicationGateway01 och lagras resultatet i variabeln som heter $AppGW.</span><span class="sxs-lookup"><span data-stu-id="7ac79-109">The first command gets the Application Gateway named ApplicationGateway01 and stores the result in the variable named $AppGW.</span></span>
<span data-ttu-id="7ac79-110">Det andra kommandot får till gång till omdirigeringsvariabler med namnet Redirect01 från Application Gateway som lagras i variabeln $AppGW.</span><span class="sxs-lookup"><span data-stu-id="7ac79-110">The second command gets the redirect configuration named Redirect01 from the Application Gateway stored in the variable named $AppGW.</span></span>

## <span data-ttu-id="7ac79-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="7ac79-111">PARAMETERS</span></span>

### <span data-ttu-id="7ac79-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="7ac79-112">-ApplicationGateway</span></span>
<span data-ttu-id="7ac79-113">ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="7ac79-113">The applicationGateway</span></span>

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

### <span data-ttu-id="7ac79-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7ac79-114">-DefaultProfile</span></span>
<span data-ttu-id="7ac79-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="7ac79-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7ac79-116">-Namn</span><span class="sxs-lookup"><span data-stu-id="7ac79-116">-Name</span></span>
<span data-ttu-id="7ac79-117">Namnet på regeln för anslutningsbegäran</span><span class="sxs-lookup"><span data-stu-id="7ac79-117">The name of the request routing rule</span></span>

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

### <span data-ttu-id="7ac79-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7ac79-118">CommonParameters</span></span>
<span data-ttu-id="7ac79-119">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7ac79-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7ac79-120">Mer information finns i [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="7ac79-120">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7ac79-121">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="7ac79-121">INPUTS</span></span>

### <span data-ttu-id="7ac79-122">Microsoft. Azure. commands. Networks. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="7ac79-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="7ac79-123">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="7ac79-123">OUTPUTS</span></span>

### <span data-ttu-id="7ac79-124">Microsoft. Azure. commands. Networks. Models. PSApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="7ac79-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRedirectConfiguration</span></span>

## <span data-ttu-id="7ac79-125">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="7ac79-125">NOTES</span></span>

## <span data-ttu-id="7ac79-126">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="7ac79-126">RELATED LINKS</span></span>

[<span data-ttu-id="7ac79-127">Add-AzApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="7ac79-127">Add-AzApplicationGatewayRedirectConfiguration</span></span>](./Add-AzApplicationGatewayRedirectConfiguration.md)

[<span data-ttu-id="7ac79-128">New-AzApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="7ac79-128">New-AzApplicationGatewayRedirectConfiguration</span></span>](./New-AzApplicationGatewayRedirectConfiguration.md)

[<span data-ttu-id="7ac79-129">Remove-AzApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="7ac79-129">Remove-AzApplicationGatewayRedirectConfiguration</span></span>](./Remove-AzApplicationGatewayRedirectConfiguration.md)

[<span data-ttu-id="7ac79-130">Set-AzApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="7ac79-130">Set-AzApplicationGatewayRedirectConfiguration</span></span>](./Set-AzApplicationGatewayRedirectConfiguration.md)
