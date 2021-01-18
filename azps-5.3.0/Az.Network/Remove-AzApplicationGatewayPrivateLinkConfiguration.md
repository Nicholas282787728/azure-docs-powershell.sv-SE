---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azapplicationgatewayprivatelinkconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayPrivateLinkConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayPrivateLinkConfiguration.md
ms.openlocfilehash: 8d222f4eaaa9d37a4f87f5f19604bdef9cff9e39
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98525834"
---
# <span data-ttu-id="e5d39-101">Remove-AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="e5d39-101">Remove-AzApplicationGatewayPrivateLinkConfiguration</span></span>

## <span data-ttu-id="e5d39-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="e5d39-102">SYNOPSIS</span></span>
<span data-ttu-id="e5d39-103">Tar bort en privateLink-konfiguration från en Programgateway.</span><span class="sxs-lookup"><span data-stu-id="e5d39-103">Removes a privateLink configuration from an application gateway.</span></span>

## <span data-ttu-id="e5d39-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="e5d39-104">SYNTAX</span></span>

```
Remove-AzApplicationGatewayPrivateLinkConfiguration -Name <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e5d39-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="e5d39-105">DESCRIPTION</span></span>
<span data-ttu-id="e5d39-106">Cmdleten **Remove-AzApplicationGatewayPrivateLinkConfiguration** tar bort en privateLink-konfiguration från en Azure Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="e5d39-106">The **Remove-AzApplicationGatewayPrivateLinkConfiguration** cmdlet removes an privateLink configuration from an Azure application gateway.</span></span>

## <span data-ttu-id="e5d39-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="e5d39-107">EXAMPLES</span></span>

### <span data-ttu-id="e5d39-108">Exempel 1: ta bort en Programgateway PrivateLink konfiguration</span><span class="sxs-lookup"><span data-stu-id="e5d39-108">Example 1: Remove an application gateway PrivateLink Configuration</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> Remove-AzApplicationGatewayPrivateLinkConfiguration -ApplicationGateway $AppGw -Name "privateLinkConfig01"
```

<span data-ttu-id="e5d39-109">Det första kommandot får en Programgateway och lagrar den i $AppGw variabeln.</span><span class="sxs-lookup"><span data-stu-id="e5d39-109">The first command gets an application gateway and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="e5d39-110">Det andra kommandot tar bort privateLink-konfigurationen som heter privateLinkConfig01 från Application Gateway som lagras i $AppGw.</span><span class="sxs-lookup"><span data-stu-id="e5d39-110">The second command removes the privateLink configuration named privateLinkConfig01 from the application gateway stored in $AppGw.</span></span>

## <span data-ttu-id="e5d39-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="e5d39-111">PARAMETERS</span></span>

### <span data-ttu-id="e5d39-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="e5d39-112">-ApplicationGateway</span></span>
<span data-ttu-id="e5d39-113">ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="e5d39-113">The applicationGateway</span></span>

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

### <span data-ttu-id="e5d39-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e5d39-114">-DefaultProfile</span></span>
<span data-ttu-id="e5d39-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="e5d39-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e5d39-116">-Namn</span><span class="sxs-lookup"><span data-stu-id="e5d39-116">-Name</span></span>
<span data-ttu-id="e5d39-117">Namnet på privateLink-konfigurationen för Application Gateway</span><span class="sxs-lookup"><span data-stu-id="e5d39-117">The name of the application gateway privateLink configuration</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e5d39-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e5d39-118">CommonParameters</span></span>
<span data-ttu-id="e5d39-119">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e5d39-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e5d39-120">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e5d39-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e5d39-121">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="e5d39-121">INPUTS</span></span>

### <span data-ttu-id="e5d39-122">Microsoft. Azure. commands. Networks. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="e5d39-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="e5d39-123">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="e5d39-123">OUTPUTS</span></span>

### <span data-ttu-id="e5d39-124">Microsoft. Azure. commands. Networks. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="e5d39-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="e5d39-125">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="e5d39-125">NOTES</span></span>

## <span data-ttu-id="e5d39-126">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="e5d39-126">RELATED LINKS</span></span>

[<span data-ttu-id="e5d39-127">New-AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="e5d39-127">New-AzApplicationGatewayPrivateLinkConfiguration</span></span>](./New-AzApplicationGatewayPrivateLinkConfiguration.md)

[<span data-ttu-id="e5d39-128">Add-AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="e5d39-128">Add-AzApplicationGatewayPrivateLinkConfiguration</span></span>](./Add-AzApplicationGatewayPrivateLinkConfiguration.md)

[<span data-ttu-id="e5d39-129">Get-AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="e5d39-129">Get-AzApplicationGatewayPrivateLinkConfiguration</span></span>](./Get-AzApplicationGatewayPrivateLinkConfiguration.md)

[<span data-ttu-id="e5d39-130">Set-AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="e5d39-130">Set-AzApplicationGatewayPrivateLinkConfiguration</span></span>](./Set-AzApplicationGatewayPrivateLinkConfiguration.md)