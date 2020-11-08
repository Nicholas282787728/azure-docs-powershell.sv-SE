---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azapplicationgatewayprivatelinkconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayPrivateLinkConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayPrivateLinkConfiguration.md
ms.openlocfilehash: 2083dd00c5163a67492ff9973fdf7399d67d7cb6
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94269803"
---
# <span data-ttu-id="49ab3-101">Add-AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="49ab3-101">Add-AzApplicationGatewayPrivateLinkConfiguration</span></span>

## <span data-ttu-id="49ab3-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="49ab3-102">SYNOPSIS</span></span>
<span data-ttu-id="49ab3-103">Lägger till en privat länk konfiguration till en Programgateway.</span><span class="sxs-lookup"><span data-stu-id="49ab3-103">Adds a private link configuration to an application gateway.</span></span>

## <span data-ttu-id="49ab3-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="49ab3-104">SYNTAX</span></span>

```
Add-AzApplicationGatewayPrivateLinkConfiguration -ApplicationGateway <PSApplicationGateway> -Name <String>
 -IpConfiguration <PSApplicationGatewayPrivateLinkIpConfiguration[]> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="49ab3-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="49ab3-105">DESCRIPTION</span></span>
<span data-ttu-id="49ab3-106">Cmdleten **Add-AzApplicationGatewayPrivateLinkConfiguration** lägger till en privat länk konfiguration till en Programgateway.</span><span class="sxs-lookup"><span data-stu-id="49ab3-106">The **Add-AzApplicationGatewayPrivateLinkConfiguration** cmdlet adds a private link configuration to an application gateway.</span></span>

## <span data-ttu-id="49ab3-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="49ab3-107">EXAMPLES</span></span>

### <span data-ttu-id="49ab3-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="49ab3-108">Example 1</span></span>
```powershell
PS C:\> $PrivateLinkIpConfiguration = New-AzApplicationGatewayPrivateLinkConfiguration -Name "ipConfig01" -Subnet $subnet -Primary
PS C:\> $AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Add-AzApplicationGatewayPrivateLinkConfiguration -ApplicationGateway $AppGw -Name "privateLinkConfig01" -IpConfiguration $PrivateLinkIpConfiguration
```

<span data-ttu-id="49ab3-109">Det första kommandot skapar en privateLinkIpConfiguration och lagrar den i variabeln $PrivateLinkIpConfiguration.</span><span class="sxs-lookup"><span data-stu-id="49ab3-109">The first command creates a privateLinkIpConfiguration and stores it in the $PrivateLinkIpConfiguration variable.</span></span>
<span data-ttu-id="49ab3-110">Det andra kommandot får den Programgateway som heter ApplicationGateway01 som tillhör resurs gruppen ResourceGroup01 och lagrar den i $AppGw variabeln.</span><span class="sxs-lookup"><span data-stu-id="49ab3-110">The second command gets the application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01, and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="49ab3-111">Det tredje kommandot lägger till den privata länk konfigurationen som heter privateLinkConfig01 för gatewayen i $AppGw</span><span class="sxs-lookup"><span data-stu-id="49ab3-111">The third command adds the private link configuration named privateLinkConfig01, for the gateway in $AppGw</span></span>

## <span data-ttu-id="49ab3-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="49ab3-112">PARAMETERS</span></span>

### <span data-ttu-id="49ab3-113">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="49ab3-113">-ApplicationGateway</span></span>
<span data-ttu-id="49ab3-114">ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="49ab3-114">The applicationGateway</span></span>

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

### <span data-ttu-id="49ab3-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="49ab3-115">-DefaultProfile</span></span>
<span data-ttu-id="49ab3-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="49ab3-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="49ab3-117">-IpConfiguration</span><span class="sxs-lookup"><span data-stu-id="49ab3-117">-IpConfiguration</span></span>
<span data-ttu-id="49ab3-118">Listan över ipConfiguration</span><span class="sxs-lookup"><span data-stu-id="49ab3-118">The list of ipConfiguration</span></span>

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

### <span data-ttu-id="49ab3-119">-Namn</span><span class="sxs-lookup"><span data-stu-id="49ab3-119">-Name</span></span>
<span data-ttu-id="49ab3-120">Namnet på privateLink-konfigurationen</span><span class="sxs-lookup"><span data-stu-id="49ab3-120">The name of the privateLink configuration</span></span>

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

### <span data-ttu-id="49ab3-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="49ab3-121">CommonParameters</span></span>
<span data-ttu-id="49ab3-122">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="49ab3-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="49ab3-123">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="49ab3-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="49ab3-124">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="49ab3-124">INPUTS</span></span>

### <span data-ttu-id="49ab3-125">Microsoft. Azure. commands. Networks. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="49ab3-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

### <span data-ttu-id="49ab3-126">Microsoft. Azure. commands. Network. Models. PSApplicationGatewayPrivateLinkIpConfiguration []</span><span class="sxs-lookup"><span data-stu-id="49ab3-126">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayPrivateLinkIpConfiguration[]</span></span>

## <span data-ttu-id="49ab3-127">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="49ab3-127">OUTPUTS</span></span>

### <span data-ttu-id="49ab3-128">Microsoft. Azure. commands. Networks. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="49ab3-128">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="49ab3-129">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="49ab3-129">NOTES</span></span>

## <span data-ttu-id="49ab3-130">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="49ab3-130">RELATED LINKS</span></span>

[<span data-ttu-id="49ab3-131">New-AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="49ab3-131">New-AzApplicationGatewayPrivateLinkConfiguration</span></span>](./New-AzApplicationGatewayPrivateLinkConfiguration.md)

[<span data-ttu-id="49ab3-132">Get-AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="49ab3-132">Get-AzApplicationGatewayPrivateLinkConfiguration</span></span>](./Get-AzApplicationGatewayPrivateLinkConfiguration.md)

[<span data-ttu-id="49ab3-133">Remove-AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="49ab3-133">Remove-AzApplicationGatewayPrivateLinkConfiguration</span></span>](./Remove-AzApplicationGatewayPrivateLinkConfiguration.md)

[<span data-ttu-id="49ab3-134">Set-AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="49ab3-134">Set-AzApplicationGatewayPrivateLinkConfiguration</span></span>](./Set-AzApplicationGatewayPrivateLinkConfiguration.md)