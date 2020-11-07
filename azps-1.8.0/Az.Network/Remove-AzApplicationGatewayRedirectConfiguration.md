---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azapplicationgatewayredirectconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayRedirectConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayRedirectConfiguration.md
ms.openlocfilehash: d75cbcbf89fde83419b9a1f97c0f66805258c82d
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93747931"
---
# <span data-ttu-id="7b4dd-101">Remove-AzApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="7b4dd-101">Remove-AzApplicationGatewayRedirectConfiguration</span></span>

## <span data-ttu-id="7b4dd-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="7b4dd-102">SYNOPSIS</span></span>
<span data-ttu-id="7b4dd-103">Tar bort en omdirigeringsinställningar från en befintlig Programgateway.</span><span class="sxs-lookup"><span data-stu-id="7b4dd-103">Removes a redirect configuration from an existing Application Gateway.</span></span>

## <span data-ttu-id="7b4dd-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="7b4dd-104">SYNTAX</span></span>

```
Remove-AzApplicationGatewayRedirectConfiguration -Name <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7b4dd-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="7b4dd-105">DESCRIPTION</span></span>
<span data-ttu-id="7b4dd-106">Cmdleten **Remove-AzApplicationGatewayRedirectConfiguration** tar bort en omdirigeringsinställningar från en befintlig Programgateway.</span><span class="sxs-lookup"><span data-stu-id="7b4dd-106">The **Remove-AzApplicationGatewayRedirectConfiguration** cmdlet removes a redirect configuration from an existing Application Gateway.</span></span>

## <span data-ttu-id="7b4dd-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="7b4dd-107">EXAMPLES</span></span>

### <span data-ttu-id="7b4dd-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="7b4dd-108">Example 1</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\>$AppGw = Remove-AzApplicationGatewayRedirectConfiguration -ApplicationGateway $AppGw -Name "Redirect01"
```

<span data-ttu-id="7b4dd-109">Det första kommandot får en Programgateway och lagrar den i $AppGw variabeln.</span><span class="sxs-lookup"><span data-stu-id="7b4dd-109">The first command gets an application gateway and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="7b4dd-110">Det andra kommandot tar bort den omdirigerings konfiguration som heter Redirect01 från Application Gateway som lagras i $AppGw.</span><span class="sxs-lookup"><span data-stu-id="7b4dd-110">The second command removes the redirect configuration named Redirect01 from the application gateway stored in $AppGw.</span></span>

## <span data-ttu-id="7b4dd-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="7b4dd-111">PARAMETERS</span></span>

### <span data-ttu-id="7b4dd-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="7b4dd-112">-ApplicationGateway</span></span>
<span data-ttu-id="7b4dd-113">ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="7b4dd-113">The applicationGateway</span></span>

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

### <span data-ttu-id="7b4dd-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7b4dd-114">-DefaultProfile</span></span>
<span data-ttu-id="7b4dd-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="7b4dd-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7b4dd-116">-Namn</span><span class="sxs-lookup"><span data-stu-id="7b4dd-116">-Name</span></span>
<span data-ttu-id="7b4dd-117">Namnet på omdirigerings konfigurationen</span><span class="sxs-lookup"><span data-stu-id="7b4dd-117">The name of the redirect configuration</span></span>

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

### <span data-ttu-id="7b4dd-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7b4dd-118">CommonParameters</span></span>
<span data-ttu-id="7b4dd-119">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7b4dd-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7b4dd-120">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7b4dd-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7b4dd-121">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="7b4dd-121">INPUTS</span></span>

### <span data-ttu-id="7b4dd-122">Microsoft. Azure. commands. Networks. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="7b4dd-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="7b4dd-123">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="7b4dd-123">OUTPUTS</span></span>

### <span data-ttu-id="7b4dd-124">Microsoft. Azure. commands. Networks. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="7b4dd-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="7b4dd-125">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="7b4dd-125">NOTES</span></span>

## <span data-ttu-id="7b4dd-126">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="7b4dd-126">RELATED LINKS</span></span>

[<span data-ttu-id="7b4dd-127">Add-AzApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="7b4dd-127">Add-AzApplicationGatewayRedirectConfiguration</span></span>](./Add-AzApplicationGatewayRedirectConfiguration.md)

[<span data-ttu-id="7b4dd-128">Get-AzApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="7b4dd-128">Get-AzApplicationGatewayRedirectConfiguration</span></span>](./Get-AzApplicationGatewayRedirectConfiguration.md)

[<span data-ttu-id="7b4dd-129">New-AzApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="7b4dd-129">New-AzApplicationGatewayRedirectConfiguration</span></span>](./New-AzApplicationGatewayRedirectConfiguration.md)

[<span data-ttu-id="7b4dd-130">Set-AzApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="7b4dd-130">Set-AzApplicationGatewayRedirectConfiguration</span></span>](./Set-AzApplicationGatewayRedirectConfiguration.md)
