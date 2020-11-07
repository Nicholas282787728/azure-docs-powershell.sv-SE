---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 312AA609-7362-42A5-A889-C0784D5A2943
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayipconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/New-AzApplicationGatewayIPConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/New-AzApplicationGatewayIPConfiguration.md
ms.openlocfilehash: 67cf5adb8d8cc0bef914f0623f66ee0e871302d8
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93922165"
---
# <span data-ttu-id="71c6c-101">New-AzApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="71c6c-101">New-AzApplicationGatewayIPConfiguration</span></span>

## <span data-ttu-id="71c6c-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="71c6c-102">SYNOPSIS</span></span>
<span data-ttu-id="71c6c-103">Skapar en IP-konfiguration för en Programgateway.</span><span class="sxs-lookup"><span data-stu-id="71c6c-103">Creates an IP configuration for an application gateway.</span></span>

## <span data-ttu-id="71c6c-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="71c6c-104">SYNTAX</span></span>

### <span data-ttu-id="71c6c-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="71c6c-105">SetByResourceId</span></span>
```
New-AzApplicationGatewayIPConfiguration -Name <String> [-SubnetId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="71c6c-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="71c6c-106">SetByResource</span></span>
```
New-AzApplicationGatewayIPConfiguration -Name <String> [-Subnet <PSSubnet>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="71c6c-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="71c6c-107">DESCRIPTION</span></span>
<span data-ttu-id="71c6c-108">Cmdleten **New-AzApplicationGatewayIPConfiguration** skapar en IP-konfiguration för en Programgateway.</span><span class="sxs-lookup"><span data-stu-id="71c6c-108">The **New-AzApplicationGatewayIPConfiguration** cmdlet creates an IP configuration for an application gateway.</span></span>
<span data-ttu-id="71c6c-109">IP-konfigurationen innehåller det undernät då Programgateway distribueras.</span><span class="sxs-lookup"><span data-stu-id="71c6c-109">The IP configuration contains the subnet in which application gateway is deployed.</span></span>

## <span data-ttu-id="71c6c-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="71c6c-110">EXAMPLES</span></span>

### <span data-ttu-id="71c6c-111">Exempel 1: skapa en IP-konfiguration för en Programgateway.</span><span class="sxs-lookup"><span data-stu-id="71c6c-111">Example 1: Create an IP configuration for an application gateway.</span></span>
```
PS C:\>$VNet = Get-AzvirtualNetwork -Name "VNet01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Subnet = Get-AzVirtualNetworkSubnetConfig -Name "Subnet01" -VirtualNetwork $VNet 
PS C:\ $GatewayIpConfig = New-AzApplicationGatewayIPConfiguration -Name "AppGwSubnet01" -Subnet $Subnet
```

<span data-ttu-id="71c6c-112">Det första kommandot får ett virtuellt nätverk som heter VNet01 som tillhör resurs gruppen "ResourceGroup01".</span><span class="sxs-lookup"><span data-stu-id="71c6c-112">The first command gets a virtual network named VNet01 that belongs to the resource group named ResourceGroup01.</span></span>

<span data-ttu-id="71c6c-113">Det andra kommandot får under nätets konfiguration för det undernät som det virtuella nätverket i föregående kommando tillhör och lagrar det i $Subnet variabeln.</span><span class="sxs-lookup"><span data-stu-id="71c6c-113">The second command gets the subnet configuration for the subnet that the virtual network in the previous command belongs to, and stores it in the $Subnet variable.</span></span>

<span data-ttu-id="71c6c-114">Det tredje kommandot skapar IP-konfigurationen med $Subnet.</span><span class="sxs-lookup"><span data-stu-id="71c6c-114">The third command creates the IP configuration using $Subnet.</span></span>

## <span data-ttu-id="71c6c-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="71c6c-115">PARAMETERS</span></span>

### <span data-ttu-id="71c6c-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="71c6c-116">-DefaultProfile</span></span>
<span data-ttu-id="71c6c-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="71c6c-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="71c6c-118">-Namn</span><span class="sxs-lookup"><span data-stu-id="71c6c-118">-Name</span></span>
<span data-ttu-id="71c6c-119">Anger namnet på den IP-konfiguration som ska skapas.</span><span class="sxs-lookup"><span data-stu-id="71c6c-119">Specifies the name of the IP configuration to create.</span></span>

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

### <span data-ttu-id="71c6c-120">-Undernät</span><span class="sxs-lookup"><span data-stu-id="71c6c-120">-Subnet</span></span>
<span data-ttu-id="71c6c-121">Anger ett under näts objekt.</span><span class="sxs-lookup"><span data-stu-id="71c6c-121">Specifies the subnet object.</span></span>
<span data-ttu-id="71c6c-122">Det här är det undernät där Application Gateway distribueras.</span><span class="sxs-lookup"><span data-stu-id="71c6c-122">This is the subnet in which the application gateway is deployed.</span></span>

```yaml
Type: PSSubnet
Parameter Sets: SetByResource
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="71c6c-123">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="71c6c-123">-SubnetId</span></span>
<span data-ttu-id="71c6c-124">Anger nät-ID.</span><span class="sxs-lookup"><span data-stu-id="71c6c-124">Specifies the subnet ID.</span></span>
<span data-ttu-id="71c6c-125">Det här är det undernät där programgatewayen distribueras.</span><span class="sxs-lookup"><span data-stu-id="71c6c-125">This is the subnet in which the application gateway would be deployed.</span></span>

```yaml
Type: String
Parameter Sets: SetByResourceId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="71c6c-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="71c6c-126">CommonParameters</span></span>
<span data-ttu-id="71c6c-127">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="71c6c-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="71c6c-128">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="71c6c-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="71c6c-129">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="71c6c-129">INPUTS</span></span>

### <span data-ttu-id="71c6c-130">System. String</span><span class="sxs-lookup"><span data-stu-id="71c6c-130">System.String</span></span>

## <span data-ttu-id="71c6c-131">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="71c6c-131">OUTPUTS</span></span>

### <span data-ttu-id="71c6c-132">Microsoft. Azure. commands. Networks. Models. PSApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="71c6c-132">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayIPConfiguration</span></span>

## <span data-ttu-id="71c6c-133">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="71c6c-133">NOTES</span></span>

## <span data-ttu-id="71c6c-134">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="71c6c-134">RELATED LINKS</span></span>

[<span data-ttu-id="71c6c-135">Add-AzApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="71c6c-135">Add-AzApplicationGatewayIPConfiguration</span></span>](./Add-AzApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="71c6c-136">Get-AzApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="71c6c-136">Get-AzApplicationGatewayIPConfiguration</span></span>](./Get-AzApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="71c6c-137">Remove-AzApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="71c6c-137">Remove-AzApplicationGatewayIPConfiguration</span></span>](./Remove-AzApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="71c6c-138">Set-AzApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="71c6c-138">Set-AzApplicationGatewayIPConfiguration</span></span>](./Set-AzApplicationGatewayIPConfiguration.md)


