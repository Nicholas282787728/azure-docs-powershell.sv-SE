---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 6943BB5C-D709-4A80-AF5E-DC9501C20680
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azapplicationgatewayipconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayIPConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayIPConfiguration.md
ms.openlocfilehash: 87f6f441220f1f8ab47fee5356bddca8d02b96c0
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94088076"
---
# <span data-ttu-id="bfbc7-101">Remove-AzApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="bfbc7-101">Remove-AzApplicationGatewayIPConfiguration</span></span>

## <span data-ttu-id="bfbc7-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="bfbc7-102">SYNOPSIS</span></span>
<span data-ttu-id="bfbc7-103">Tar bort en IP-konfiguration från en Programgateway.</span><span class="sxs-lookup"><span data-stu-id="bfbc7-103">Removes an IP configuration from an application gateway.</span></span>

## <span data-ttu-id="bfbc7-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="bfbc7-104">SYNTAX</span></span>

```
Remove-AzApplicationGatewayIPConfiguration -Name <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bfbc7-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="bfbc7-105">DESCRIPTION</span></span>
<span data-ttu-id="bfbc7-106">Cmdleten **Remove-AzApplicationGatewayIPConfiguration** tar bort en IP-konfiguration från en Azure Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="bfbc7-106">The **Remove-AzApplicationGatewayIPConfiguration** cmdlet removes an IP configuration from an Azure application gateway.</span></span>

## <span data-ttu-id="bfbc7-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="bfbc7-107">EXAMPLES</span></span>

### <span data-ttu-id="bfbc7-108">Exempel 1: ta bort en IP-konfiguration från en Azure Application Gateway</span><span class="sxs-lookup"><span data-stu-id="bfbc7-108">Example 1: Remove an IP configuration from an Azure application gateway</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> Remove-AzApplicationGatewayIPConfiguration -ApplicationGateway $AppGw -Name "Subnet02"
```

<span data-ttu-id="bfbc7-109">Det första kommandot får en Programgateway och lagrar den i $AppGw variabeln.</span><span class="sxs-lookup"><span data-stu-id="bfbc7-109">The first command gets an application gateway and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="bfbc7-110">Det andra kommandot tar bort IP-konfigurationen som heter Subnet02 från Application Gateway som lagras i $AppGw.</span><span class="sxs-lookup"><span data-stu-id="bfbc7-110">The second command removes the IP configuration named Subnet02 from the application gateway stored in $AppGw.</span></span>

## <span data-ttu-id="bfbc7-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="bfbc7-111">PARAMETERS</span></span>

### <span data-ttu-id="bfbc7-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="bfbc7-112">-ApplicationGateway</span></span>
<span data-ttu-id="bfbc7-113">Anger den Programgateway från vilken du vill ta bort en IP-konfiguration.</span><span class="sxs-lookup"><span data-stu-id="bfbc7-113">Specifies the application gateway from which to remove an IP configuration.</span></span>

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

### <span data-ttu-id="bfbc7-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bfbc7-114">-DefaultProfile</span></span>
<span data-ttu-id="bfbc7-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="bfbc7-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bfbc7-116">-Namn</span><span class="sxs-lookup"><span data-stu-id="bfbc7-116">-Name</span></span>
<span data-ttu-id="bfbc7-117">Anger namnet på den IP-konfiguration som ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="bfbc7-117">Specifies the name of the IP configuration to remove.</span></span>

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

### <span data-ttu-id="bfbc7-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bfbc7-118">CommonParameters</span></span>
<span data-ttu-id="bfbc7-119">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bfbc7-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bfbc7-120">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bfbc7-120">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bfbc7-121">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="bfbc7-121">INPUTS</span></span>

### <span data-ttu-id="bfbc7-122">Microsoft. Azure. commands. Networks. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="bfbc7-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="bfbc7-123">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="bfbc7-123">OUTPUTS</span></span>

### <span data-ttu-id="bfbc7-124">Microsoft. Azure. commands. Networks. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="bfbc7-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="bfbc7-125">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="bfbc7-125">NOTES</span></span>

## <span data-ttu-id="bfbc7-126">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="bfbc7-126">RELATED LINKS</span></span>

[<span data-ttu-id="bfbc7-127">Add-AzApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="bfbc7-127">Add-AzApplicationGatewayIPConfiguration</span></span>](./Add-AzApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="bfbc7-128">Get-AzApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="bfbc7-128">Get-AzApplicationGatewayIPConfiguration</span></span>](./Get-AzApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="bfbc7-129">New-AzApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="bfbc7-129">New-AzApplicationGatewayIPConfiguration</span></span>](./New-AzApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="bfbc7-130">Set-AzApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="bfbc7-130">Set-AzApplicationGatewayIPConfiguration</span></span>](./Set-AzApplicationGatewayIPConfiguration.md)

