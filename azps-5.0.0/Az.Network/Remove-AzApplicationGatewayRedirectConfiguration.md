---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azapplicationgatewayredirectconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayRedirectConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayRedirectConfiguration.md
ms.openlocfilehash: fdd461ea2908e59ba824b09a49bed3b6b8f4d38f
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94269199"
---
# <span data-ttu-id="119f3-101">Remove-AzApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="119f3-101">Remove-AzApplicationGatewayRedirectConfiguration</span></span>

## <span data-ttu-id="119f3-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="119f3-102">SYNOPSIS</span></span>
<span data-ttu-id="119f3-103">Tar bort en omdirigeringsinställningar från en befintlig Programgateway.</span><span class="sxs-lookup"><span data-stu-id="119f3-103">Removes a redirect configuration from an existing Application Gateway.</span></span>

## <span data-ttu-id="119f3-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="119f3-104">SYNTAX</span></span>

```
Remove-AzApplicationGatewayRedirectConfiguration -Name <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="119f3-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="119f3-105">DESCRIPTION</span></span>
<span data-ttu-id="119f3-106">Cmdleten **Remove-AzApplicationGatewayRedirectConfiguration** tar bort en omdirigeringsinställningar från en befintlig Programgateway.</span><span class="sxs-lookup"><span data-stu-id="119f3-106">The **Remove-AzApplicationGatewayRedirectConfiguration** cmdlet removes a redirect configuration from an existing Application Gateway.</span></span>

## <span data-ttu-id="119f3-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="119f3-107">EXAMPLES</span></span>

### <span data-ttu-id="119f3-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="119f3-108">Example 1</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\>$AppGw = Remove-AzApplicationGatewayRedirectConfiguration -ApplicationGateway $AppGw -Name "Redirect01"
```

<span data-ttu-id="119f3-109">Det första kommandot får en Programgateway och lagrar den i $AppGw variabeln.</span><span class="sxs-lookup"><span data-stu-id="119f3-109">The first command gets an application gateway and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="119f3-110">Det andra kommandot tar bort den omdirigerings konfiguration som heter Redirect01 från Application Gateway som lagras i $AppGw.</span><span class="sxs-lookup"><span data-stu-id="119f3-110">The second command removes the redirect configuration named Redirect01 from the application gateway stored in $AppGw.</span></span>

## <span data-ttu-id="119f3-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="119f3-111">PARAMETERS</span></span>

### <span data-ttu-id="119f3-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="119f3-112">-ApplicationGateway</span></span>
<span data-ttu-id="119f3-113">ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="119f3-113">The applicationGateway</span></span>

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

### <span data-ttu-id="119f3-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="119f3-114">-DefaultProfile</span></span>
<span data-ttu-id="119f3-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="119f3-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="119f3-116">-Namn</span><span class="sxs-lookup"><span data-stu-id="119f3-116">-Name</span></span>
<span data-ttu-id="119f3-117">Namnet på omdirigerings konfigurationen</span><span class="sxs-lookup"><span data-stu-id="119f3-117">The name of the redirect configuration</span></span>

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

### <span data-ttu-id="119f3-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="119f3-118">CommonParameters</span></span>
<span data-ttu-id="119f3-119">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="119f3-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="119f3-120">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="119f3-120">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="119f3-121">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="119f3-121">INPUTS</span></span>

### <span data-ttu-id="119f3-122">Microsoft. Azure. commands. Networks. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="119f3-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="119f3-123">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="119f3-123">OUTPUTS</span></span>

### <span data-ttu-id="119f3-124">Microsoft. Azure. commands. Networks. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="119f3-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="119f3-125">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="119f3-125">NOTES</span></span>

## <span data-ttu-id="119f3-126">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="119f3-126">RELATED LINKS</span></span>

[<span data-ttu-id="119f3-127">Add-AzApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="119f3-127">Add-AzApplicationGatewayRedirectConfiguration</span></span>](./Add-AzApplicationGatewayRedirectConfiguration.md)

[<span data-ttu-id="119f3-128">Get-AzApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="119f3-128">Get-AzApplicationGatewayRedirectConfiguration</span></span>](./Get-AzApplicationGatewayRedirectConfiguration.md)

[<span data-ttu-id="119f3-129">New-AzApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="119f3-129">New-AzApplicationGatewayRedirectConfiguration</span></span>](./New-AzApplicationGatewayRedirectConfiguration.md)

[<span data-ttu-id="119f3-130">Set-AzApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="119f3-130">Set-AzApplicationGatewayRedirectConfiguration</span></span>](./Set-AzApplicationGatewayRedirectConfiguration.md)