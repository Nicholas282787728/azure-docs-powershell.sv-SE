---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azapplicationgatewayprivatelinkconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayPrivateLinkConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayPrivateLinkConfiguration.md
ms.openlocfilehash: 2083dd00c5163a67492ff9973fdf7399d67d7cb6
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98422355"
---
# <span data-ttu-id="deab0-101">Add-AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="deab0-101">Add-AzApplicationGatewayPrivateLinkConfiguration</span></span>

## <span data-ttu-id="deab0-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="deab0-102">SYNOPSIS</span></span>
<span data-ttu-id="deab0-103">Lägger till en privat länk konfiguration till en Programgateway.</span><span class="sxs-lookup"><span data-stu-id="deab0-103">Adds a private link configuration to an application gateway.</span></span>

## <span data-ttu-id="deab0-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="deab0-104">SYNTAX</span></span>

```
Add-AzApplicationGatewayPrivateLinkConfiguration -ApplicationGateway <PSApplicationGateway> -Name <String>
 -IpConfiguration <PSApplicationGatewayPrivateLinkIpConfiguration[]> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="deab0-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="deab0-105">DESCRIPTION</span></span>
<span data-ttu-id="deab0-106">Cmdleten **Add-AzApplicationGatewayPrivateLinkConfiguration** lägger till en privat länk konfiguration till en Programgateway.</span><span class="sxs-lookup"><span data-stu-id="deab0-106">The **Add-AzApplicationGatewayPrivateLinkConfiguration** cmdlet adds a private link configuration to an application gateway.</span></span>

## <span data-ttu-id="deab0-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="deab0-107">EXAMPLES</span></span>

### <span data-ttu-id="deab0-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="deab0-108">Example 1</span></span>
```powershell
PS C:\> $PrivateLinkIpConfiguration = New-AzApplicationGatewayPrivateLinkConfiguration -Name "ipConfig01" -Subnet $subnet -Primary
PS C:\> $AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Add-AzApplicationGatewayPrivateLinkConfiguration -ApplicationGateway $AppGw -Name "privateLinkConfig01" -IpConfiguration $PrivateLinkIpConfiguration
```

<span data-ttu-id="deab0-109">Det första kommandot skapar en privateLinkIpConfiguration och lagrar den i variabeln $PrivateLinkIpConfiguration.</span><span class="sxs-lookup"><span data-stu-id="deab0-109">The first command creates a privateLinkIpConfiguration and stores it in the $PrivateLinkIpConfiguration variable.</span></span>
<span data-ttu-id="deab0-110">Det andra kommandot får den Programgateway som heter ApplicationGateway01 som tillhör resurs gruppen ResourceGroup01 och lagrar den i $AppGw variabeln.</span><span class="sxs-lookup"><span data-stu-id="deab0-110">The second command gets the application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01, and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="deab0-111">Det tredje kommandot lägger till den privata länk konfigurationen som heter privateLinkConfig01 för gatewayen i $AppGw</span><span class="sxs-lookup"><span data-stu-id="deab0-111">The third command adds the private link configuration named privateLinkConfig01, for the gateway in $AppGw</span></span>

## <span data-ttu-id="deab0-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="deab0-112">PARAMETERS</span></span>

### <span data-ttu-id="deab0-113">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="deab0-113">-ApplicationGateway</span></span>
<span data-ttu-id="deab0-114">ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="deab0-114">The applicationGateway</span></span>

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

### <span data-ttu-id="deab0-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="deab0-115">-DefaultProfile</span></span>
<span data-ttu-id="deab0-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="deab0-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="deab0-117">-IpConfiguration</span><span class="sxs-lookup"><span data-stu-id="deab0-117">-IpConfiguration</span></span>
<span data-ttu-id="deab0-118">Listan över ipConfiguration</span><span class="sxs-lookup"><span data-stu-id="deab0-118">The list of ipConfiguration</span></span>

```yaml
Type: PSApplicationGatewayPrivateLinkIpConfiguration[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="deab0-119">-Namn</span><span class="sxs-lookup"><span data-stu-id="deab0-119">-Name</span></span>
<span data-ttu-id="deab0-120">Namnet på privateLink-konfigurationen</span><span class="sxs-lookup"><span data-stu-id="deab0-120">The name of the privateLink configuration</span></span>

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

### <span data-ttu-id="deab0-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="deab0-121">CommonParameters</span></span>
<span data-ttu-id="deab0-122">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="deab0-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="deab0-123">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="deab0-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="deab0-124">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="deab0-124">INPUTS</span></span>

### <span data-ttu-id="deab0-125">Microsoft. Azure. commands. Networks. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="deab0-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

### <span data-ttu-id="deab0-126">Microsoft. Azure. commands. Network. Models. PSApplicationGatewayPrivateLinkIpConfiguration []</span><span class="sxs-lookup"><span data-stu-id="deab0-126">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayPrivateLinkIpConfiguration[]</span></span>

## <span data-ttu-id="deab0-127">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="deab0-127">OUTPUTS</span></span>

### <span data-ttu-id="deab0-128">Microsoft. Azure. commands. Networks. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="deab0-128">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="deab0-129">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="deab0-129">NOTES</span></span>

## <span data-ttu-id="deab0-130">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="deab0-130">RELATED LINKS</span></span>

[<span data-ttu-id="deab0-131">New-AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="deab0-131">New-AzApplicationGatewayPrivateLinkConfiguration</span></span>](./New-AzApplicationGatewayPrivateLinkConfiguration.md)

[<span data-ttu-id="deab0-132">Get-AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="deab0-132">Get-AzApplicationGatewayPrivateLinkConfiguration</span></span>](./Get-AzApplicationGatewayPrivateLinkConfiguration.md)

[<span data-ttu-id="deab0-133">Remove-AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="deab0-133">Remove-AzApplicationGatewayPrivateLinkConfiguration</span></span>](./Remove-AzApplicationGatewayPrivateLinkConfiguration.md)

[<span data-ttu-id="deab0-134">Set-AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="deab0-134">Set-AzApplicationGatewayPrivateLinkConfiguration</span></span>](./Set-AzApplicationGatewayPrivateLinkConfiguration.md)