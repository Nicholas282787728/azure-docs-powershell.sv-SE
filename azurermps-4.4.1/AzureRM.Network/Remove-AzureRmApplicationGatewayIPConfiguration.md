---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 6943BB5C-D709-4A80-AF5E-DC9501C20680
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmApplicationGatewayIPConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmApplicationGatewayIPConfiguration.md
ms.openlocfilehash: 4ef644fb92bf3f872a9e80aef2674a3ffb56747b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93577651"
---
# <span data-ttu-id="b499b-101">Remove-AzureRmApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="b499b-101">Remove-AzureRmApplicationGatewayIPConfiguration</span></span>

## <span data-ttu-id="b499b-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="b499b-102">SYNOPSIS</span></span>
<span data-ttu-id="b499b-103">Tar bort en IP-konfiguration från en Programgateway.</span><span class="sxs-lookup"><span data-stu-id="b499b-103">Removes an IP configuration from an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b499b-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="b499b-104">SYNTAX</span></span>

```
Remove-AzureRmApplicationGatewayIPConfiguration -Name <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b499b-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="b499b-105">DESCRIPTION</span></span>
<span data-ttu-id="b499b-106">Cmdleten **Remove-AzureRmApplicationGatewayIPConfiguration** tar bort en IP-konfiguration från en Azure Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="b499b-106">The **Remove-AzureRmApplicationGatewayIPConfiguration** cmdlet removes an IP configuration from an Azure application gateway.</span></span>

## <span data-ttu-id="b499b-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="b499b-107">EXAMPLES</span></span>

### <span data-ttu-id="b499b-108">Exempel 1: ta bort en IP-konfiguration från en Azure Application Gateway</span><span class="sxs-lookup"><span data-stu-id="b499b-108">Example 1: Remove an IP configuration from an Azure application gateway</span></span>
```
PS C:\>$AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> Remove-AzureRmApplicationGatewayIPConfiguration -ApplicationGateway $AppGw -Name "Subnet02"
```

<span data-ttu-id="b499b-109">Det första kommandot får en Programgateway och lagrar den i $AppGw variabeln.</span><span class="sxs-lookup"><span data-stu-id="b499b-109">The first command gets an application gateway and stores it in the $AppGw variable.</span></span>

<span data-ttu-id="b499b-110">Det andra kommandot tar bort IP-konfigurationen som heter Subnet02 från Application Gateway som lagras i $AppGw.</span><span class="sxs-lookup"><span data-stu-id="b499b-110">The second command removes the IP configuration named Subnet02 from the application gateway stored in $AppGw.</span></span>

## <span data-ttu-id="b499b-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="b499b-111">PARAMETERS</span></span>

### <span data-ttu-id="b499b-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="b499b-112">-ApplicationGateway</span></span>
<span data-ttu-id="b499b-113">Anger den Programgateway från vilken du vill ta bort en IP-konfiguration.</span><span class="sxs-lookup"><span data-stu-id="b499b-113">Specifies the application gateway from which to remove an IP configuration.</span></span>

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

### <span data-ttu-id="b499b-114">-Namn</span><span class="sxs-lookup"><span data-stu-id="b499b-114">-Name</span></span>
<span data-ttu-id="b499b-115">Anger namnet på den IP-konfiguration som ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="b499b-115">Specifies the name of the IP configuration to remove.</span></span>

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

### <span data-ttu-id="b499b-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b499b-116">-DefaultProfile</span></span>
<span data-ttu-id="b499b-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="b499b-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b499b-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b499b-118">CommonParameters</span></span>
<span data-ttu-id="b499b-119">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b499b-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b499b-120">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b499b-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b499b-121">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="b499b-121">INPUTS</span></span>

### <span data-ttu-id="b499b-122">System. String</span><span class="sxs-lookup"><span data-stu-id="b499b-122">System.String</span></span>

## <span data-ttu-id="b499b-123">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="b499b-123">OUTPUTS</span></span>

### <span data-ttu-id="b499b-124">Microsoft. Azure. commands. Networks. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="b499b-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="b499b-125">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="b499b-125">NOTES</span></span>

## <span data-ttu-id="b499b-126">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="b499b-126">RELATED LINKS</span></span>

[<span data-ttu-id="b499b-127">Add-AzureRmApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="b499b-127">Add-AzureRmApplicationGatewayIPConfiguration</span></span>](./Add-AzureRmApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="b499b-128">Get-AzureRmApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="b499b-128">Get-AzureRmApplicationGatewayIPConfiguration</span></span>](./Get-AzureRmApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="b499b-129">New-AzureRmApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="b499b-129">New-AzureRmApplicationGatewayIPConfiguration</span></span>](./New-AzureRmApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="b499b-130">Set-AzureRmApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="b499b-130">Set-AzureRmApplicationGatewayIPConfiguration</span></span>](./Set-AzureRmApplicationGatewayIPConfiguration.md)


