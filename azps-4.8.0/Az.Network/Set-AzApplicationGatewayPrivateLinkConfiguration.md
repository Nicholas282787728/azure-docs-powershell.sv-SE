---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azapplicationgatewayprivatelinkconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayPrivateLinkConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayPrivateLinkConfiguration.md
ms.openlocfilehash: 78af871cf476ee80c57e22e2469b48bb4d4337a1
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94102085"
---
# <span data-ttu-id="e8224-101">Set-AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="e8224-101">Set-AzApplicationGatewayPrivateLinkConfiguration</span></span>

## <span data-ttu-id="e8224-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="e8224-102">SYNOPSIS</span></span>
<span data-ttu-id="e8224-103">Ändrar en PrivateLink-konfiguration för en Programgateway.</span><span class="sxs-lookup"><span data-stu-id="e8224-103">Modifies an PrivateLink Configuration for an application gateway.</span></span>

## <span data-ttu-id="e8224-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="e8224-104">SYNTAX</span></span>

```
Set-AzApplicationGatewayPrivateLinkConfiguration -ApplicationGateway <PSApplicationGateway> -Name <String>
 -IpConfiguration <PSApplicationGatewayPrivateLinkIpConfiguration[]> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e8224-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="e8224-105">DESCRIPTION</span></span>
<span data-ttu-id="e8224-106">Cmdleten **set-AzApplicationGatewayPrivateLinkConfiguration** ändrar en privateLink-konfiguration för en Azure Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="e8224-106">The **Set-AzApplicationGatewayPrivateLinkConfiguration** cmdlet modifies an privateLink configuration for an Azure application gateway.</span></span>

## <span data-ttu-id="e8224-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="e8224-107">EXAMPLES</span></span>

### <span data-ttu-id="e8224-108">Exempel 1: Ange en PrivateLink-konfiguration</span><span class="sxs-lookup"><span data-stu-id="e8224-108">Example 1: Set a PrivateLink Configuration</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Set-AzApplicationGatewayPrivateLinkConfiguration -ApplicationGateway $AppGw -Name "privateLinkConfig01" -IpConfiguration $privateLinkIpConfiguration01
```

<span data-ttu-id="e8224-109">Det första kommandot hämtar den Programgateway som heter ApplicationGateway01 som tillhör resurs gruppen med namnet ResourceGroup01 och lagrar den i $AppGw variabeln.</span><span class="sxs-lookup"><span data-stu-id="e8224-109">The first command gets the application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01 and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="e8224-110">Det andra kommandot ställer in privateLink-konfigurationen med namnet privateLinkConfig01 att använda IP-konfigurationen som lagras i $privateLinkIpConfiguration 01</span><span class="sxs-lookup"><span data-stu-id="e8224-110">The second command sets the privateLink configuration with name privateLinkConfig01 to use the ip configuration stored in $privateLinkIpConfiguration01</span></span>

## <span data-ttu-id="e8224-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="e8224-111">PARAMETERS</span></span>

### <span data-ttu-id="e8224-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="e8224-112">-ApplicationGateway</span></span>
<span data-ttu-id="e8224-113">ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="e8224-113">The applicationGateway</span></span>

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

### <span data-ttu-id="e8224-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e8224-114">-DefaultProfile</span></span>
<span data-ttu-id="e8224-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="e8224-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e8224-116">-IpConfiguration</span><span class="sxs-lookup"><span data-stu-id="e8224-116">-IpConfiguration</span></span>
<span data-ttu-id="e8224-117">Listan över ipConfiguration</span><span class="sxs-lookup"><span data-stu-id="e8224-117">The list of ipConfiguration</span></span>

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

### <span data-ttu-id="e8224-118">-Namn</span><span class="sxs-lookup"><span data-stu-id="e8224-118">-Name</span></span>
<span data-ttu-id="e8224-119">Namnet på privateLink-konfigurationen</span><span class="sxs-lookup"><span data-stu-id="e8224-119">The name of the privateLink configuration</span></span>

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

### <span data-ttu-id="e8224-120">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="e8224-120">-Confirm</span></span>
<span data-ttu-id="e8224-121">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="e8224-121">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e8224-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e8224-122">-WhatIf</span></span>
<span data-ttu-id="e8224-123">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="e8224-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e8224-124">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="e8224-124">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e8224-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e8224-125">CommonParameters</span></span>
<span data-ttu-id="e8224-126">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e8224-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e8224-127">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e8224-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e8224-128">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="e8224-128">INPUTS</span></span>

### <span data-ttu-id="e8224-129">Microsoft. Azure. commands. Networks. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="e8224-129">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

### <span data-ttu-id="e8224-130">Microsoft. Azure. commands. Network. Models. PSApplicationGatewayPrivateLinkIpConfiguration []</span><span class="sxs-lookup"><span data-stu-id="e8224-130">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayPrivateLinkIpConfiguration[]</span></span>

## <span data-ttu-id="e8224-131">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="e8224-131">OUTPUTS</span></span>

### <span data-ttu-id="e8224-132">Microsoft. Azure. commands. Networks. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="e8224-132">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="e8224-133">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="e8224-133">NOTES</span></span>

## <span data-ttu-id="e8224-134">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="e8224-134">RELATED LINKS</span></span>

[<span data-ttu-id="e8224-135">New-AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="e8224-135">New-AzApplicationGatewayPrivateLinkConfiguration</span></span>](./New-AzApplicationGatewayPrivateLinkConfiguration.md)

[<span data-ttu-id="e8224-136">Add-AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="e8224-136">Add-AzApplicationGatewayPrivateLinkConfiguration</span></span>](./Add-AzApplicationGatewayPrivateLinkConfiguration.md)

[<span data-ttu-id="e8224-137">Get-AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="e8224-137">Get-AzApplicationGatewayPrivateLinkConfiguration</span></span>](./Get-AzApplicationGatewayPrivateLinkConfiguration.md)

[<span data-ttu-id="e8224-138">Remove-AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="e8224-138">Remove-AzApplicationGatewayPrivateLinkConfiguration</span></span>](./Remove-AzApplicationGatewayPrivateLinkConfiguration.md)