---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: EC798838-1850-4E88-B17F-D2F00F2D4EE9
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azpublicipaddress
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzPublicIpAddress.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzPublicIpAddress.md
ms.openlocfilehash: 4cb7d3a48d1783e834b9ecdd53d86969b4e1e6cb
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98525761"
---
# <span data-ttu-id="12a64-101">Set-AzPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="12a64-101">Set-AzPublicIpAddress</span></span>

## <span data-ttu-id="12a64-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="12a64-102">SYNOPSIS</span></span>
<span data-ttu-id="12a64-103">Uppdaterar en offentlig IP-adress.</span><span class="sxs-lookup"><span data-stu-id="12a64-103">Updates a public IP address.</span></span>

## <span data-ttu-id="12a64-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="12a64-104">SYNTAX</span></span>

```
Set-AzPublicIpAddress -PublicIpAddress <PSPublicIpAddress> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="12a64-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="12a64-105">DESCRIPTION</span></span>
<span data-ttu-id="12a64-106">Cmdleten **set-AzPublicIpAddress** uppdaterar en offentlig IP-adress.</span><span class="sxs-lookup"><span data-stu-id="12a64-106">The **Set-AzPublicIpAddress** cmdlet updates a public IP address.</span></span>

## <span data-ttu-id="12a64-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="12a64-107">EXAMPLES</span></span>

### <span data-ttu-id="12a64-108">1: ändra tilldelnings metod för en offentlig IP-adress</span><span class="sxs-lookup"><span data-stu-id="12a64-108">1: Change allocation method of a public IP address</span></span>
```
PS C:\> $publicIp = Get-AzPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName

PS C:\> $publicIp.PublicIpAllocationMethod = "Static"
    
PS C:\> Set-AzPublicIpAddress -PublicIpAddress $publicIp

PS C:\> Get-AzPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName
```

 <span data-ttu-id="12a64-109">Första kommandot får den offentliga IP-adressresursen med namnet $publicIPName i resurs gruppen $rgName.</span><span class="sxs-lookup"><span data-stu-id="12a64-109">First command gets the public IP address resource with name $publicIPName in the resource group $rgName.</span></span>
<span data-ttu-id="12a64-110">Andra kommando anger tilldelnings metod för det offentliga IP-adress-objektet till "statisk".</span><span class="sxs-lookup"><span data-stu-id="12a64-110">Second command sets the allocation method of the public IP address object to "Static".</span></span>
<span data-ttu-id="12a64-111">Set-AzPublicIPAddress kommando uppdaterar den offentliga IP-adressresursen med det uppdaterade objektet och ändrar tilldelnings metoden till "statisk".</span><span class="sxs-lookup"><span data-stu-id="12a64-111">Set-AzPublicIPAddress command updates the public IP address resource with the updated object, and modifies the allocation method to 'Static'.</span></span> <span data-ttu-id="12a64-112">En offentlig IP-adress tilldelas omedelbart.</span><span class="sxs-lookup"><span data-stu-id="12a64-112">A public IP address gets allocated immediately.</span></span>

### <span data-ttu-id="12a64-113">2: lägga till DNS-domännamn för en offentlig IP-adress</span><span class="sxs-lookup"><span data-stu-id="12a64-113">2: Add DNS domain label of a public IP address</span></span>
```
PS C:\> $publicIp = Get-AzPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName

PS C:\> $publicIp.DnsSettings = @{"DomainNameLabel" = "newdnsprefix"}
    
PS C:\> Set-AzPublicIpAddress -PublicIpAddress $publicIp

PS C:\> $publicIp = Get-AzPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName
```

<span data-ttu-id="12a64-114">Första kommandot får den offentliga IP-adressresursen med namnet $publicIPName i resurs gruppen $rgName.</span><span class="sxs-lookup"><span data-stu-id="12a64-114">First command gets the public IP address resource with name $publicIPName in the resource group $rgName.</span></span>
<span data-ttu-id="12a64-115">Med det andra kommandot anges egenskapen DomainNameLabel till det obligatoriska DNS-prefixet.</span><span class="sxs-lookup"><span data-stu-id="12a64-115">Second command sets the DomainNameLabel property to the required dns prefix.</span></span>
<span data-ttu-id="12a64-116">Set-AzPublicIPAddress kommando uppdaterar den offentliga IP-adressresursen med det uppdaterade objektet.</span><span class="sxs-lookup"><span data-stu-id="12a64-116">Set-AzPublicIPAddress command updates the public IP address resource with the updated object.</span></span> <span data-ttu-id="12a64-117">DomainNameLabel & FQDN ändras som förväntat.</span><span class="sxs-lookup"><span data-stu-id="12a64-117">DomainNameLabel & Fqdn are modified as expected.</span></span>
    
### <span data-ttu-id="12a64-118">3: ändra DNS-domännamn för en offentlig IP-adress</span><span class="sxs-lookup"><span data-stu-id="12a64-118">3: Change DNS domain label of a public IP address</span></span>
```
PS C:\> $publicIp = Get-AzPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName

PS C:\> $publicIp.DnsSettings.DomainNameLabel = "newdnsprefix"
    
PS C:\> Set-AzPublicIpAddress -PublicIpAddress $publicIp

PS C:\> $publicIp = Get-AzPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName
```

<span data-ttu-id="12a64-119">Första kommandot får den offentliga IP-adressresursen med namnet $publicIPName i resurs gruppen $rgName.</span><span class="sxs-lookup"><span data-stu-id="12a64-119">First command gets the public IP address resource with name $publicIPName in the resource group $rgName.</span></span>
<span data-ttu-id="12a64-120">Med det andra kommandot anges egenskapen DomainNameLabel till det obligatoriska DNS-prefixet.</span><span class="sxs-lookup"><span data-stu-id="12a64-120">Second command sets the DomainNameLabel property to the required dns prefix.</span></span>
<span data-ttu-id="12a64-121">Set-AzPublicIPAddress kommando uppdaterar den offentliga IP-adressresursen med det uppdaterade objektet.</span><span class="sxs-lookup"><span data-stu-id="12a64-121">Set-AzPublicIPAddress command updates the public IP address resource with the updated object.</span></span> <span data-ttu-id="12a64-122">DomainNameLabel & FQDN ändras som förväntat.</span><span class="sxs-lookup"><span data-stu-id="12a64-122">DomainNameLabel & Fqdn are modified as expected.</span></span>

## <span data-ttu-id="12a64-123">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="12a64-123">PARAMETERS</span></span>

### <span data-ttu-id="12a64-124">-AsJob</span><span class="sxs-lookup"><span data-stu-id="12a64-124">-AsJob</span></span>
<span data-ttu-id="12a64-125">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="12a64-125">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="12a64-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="12a64-126">-DefaultProfile</span></span>
<span data-ttu-id="12a64-127">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="12a64-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="12a64-128">-PublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="12a64-128">-PublicIpAddress</span></span>
<span data-ttu-id="12a64-129">Anger ett offentlig IP-adress-objekt som representerar tillståndet som den offentliga IP-adressen ska anges för.</span><span class="sxs-lookup"><span data-stu-id="12a64-129">Specifies a public IP address object representing the state to which the public IP address should be set.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSPublicIpAddress
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="12a64-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="12a64-130">CommonParameters</span></span>
<span data-ttu-id="12a64-131">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="12a64-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="12a64-132">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="12a64-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="12a64-133">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="12a64-133">INPUTS</span></span>

### <span data-ttu-id="12a64-134">Microsoft. Azure. commands. Networks. Models. PSPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="12a64-134">Microsoft.Azure.Commands.Network.Models.PSPublicIpAddress</span></span>

## <span data-ttu-id="12a64-135">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="12a64-135">OUTPUTS</span></span>

### <span data-ttu-id="12a64-136">Microsoft. Azure. commands. Networks. Models. PSPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="12a64-136">Microsoft.Azure.Commands.Network.Models.PSPublicIpAddress</span></span>

## <span data-ttu-id="12a64-137">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="12a64-137">NOTES</span></span>

## <span data-ttu-id="12a64-138">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="12a64-138">RELATED LINKS</span></span>

[<span data-ttu-id="12a64-139">Get-AzPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="12a64-139">Get-AzPublicIpAddress</span></span>](./Get-AzPublicIpAddress.md)

[<span data-ttu-id="12a64-140">New-AzPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="12a64-140">New-AzPublicIpAddress</span></span>](./New-AzPublicIpAddress.md)

[<span data-ttu-id="12a64-141">Remove-AzPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="12a64-141">Remove-AzPublicIpAddress</span></span>](./Remove-AzPublicIpAddress.md)


