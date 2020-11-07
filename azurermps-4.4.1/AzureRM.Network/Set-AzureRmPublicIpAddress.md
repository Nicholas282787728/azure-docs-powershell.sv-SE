---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: EC798838-1850-4E88-B17F-D2F00F2D4EE9
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmPublicIpAddress.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmPublicIpAddress.md
ms.openlocfilehash: 1460b4497909d56e2d10d03e33df71518c52b796
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93755660"
---
# <span data-ttu-id="36257-101">Set-AzureRmPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="36257-101">Set-AzureRmPublicIpAddress</span></span>

## <span data-ttu-id="36257-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="36257-102">SYNOPSIS</span></span>
<span data-ttu-id="36257-103">Anger mål tillstånd för en offentlig IP-adress.</span><span class="sxs-lookup"><span data-stu-id="36257-103">Sets the goal state for a public IP address.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="36257-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="36257-104">SYNTAX</span></span>

```
Set-AzureRmPublicIpAddress -PublicIpAddress <PSPublicIpAddress> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="36257-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="36257-105">DESCRIPTION</span></span>
<span data-ttu-id="36257-106">Cmdleten **set-AzureRmPublicIpAddress** anger mål tillståndet för en offentlig IP-adress.</span><span class="sxs-lookup"><span data-stu-id="36257-106">The **Set-AzureRmPublicIpAddress** cmdlet sets the goal state for a public IP address.</span></span>

## <span data-ttu-id="36257-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="36257-107">EXAMPLES</span></span>

### <span data-ttu-id="36257-108">1: ändra tilldelnings metod för en offentlig IP-adress</span><span class="sxs-lookup"><span data-stu-id="36257-108">1: Change allocation method of a public IP address</span></span>
```
PS C:\> $publicIp = Get-AzureRmPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName

PS C:\> $publicIp.PublicIpAllocationMethod = "Dynamic"
    
PS C:\> Set-AzureRmPublicIpAddress -PublicIpAddress $publicIp

PS C:\> $publicIp = Get-AzureRmPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName
```

 <span data-ttu-id="36257-109">Första kommandot får den offentliga IP-adressresursen med namnet $publicIPName i resurs gruppen $rgName.</span><span class="sxs-lookup"><span data-stu-id="36257-109">First command gets the public IP address resource with name $publicIPName in the resource group $rgName.</span></span>
<span data-ttu-id="36257-110">Andra kommando anger tilldelnings metod för det offentliga IP-adress-objektet till "statisk".</span><span class="sxs-lookup"><span data-stu-id="36257-110">Second command sets the allocation method of the public IP address object to "Static".</span></span>
<span data-ttu-id="36257-111">Set-AzureRmPublicIPAddress kommando uppdaterar den offentliga IP-adressresursen med det uppdaterade objektet och ändrar tilldelnings metoden till "statisk".</span><span class="sxs-lookup"><span data-stu-id="36257-111">Set-AzureRmPublicIPAddress command updates the public IP address resource with the updated object, and modifies the allocation method to 'Static'.</span></span> <span data-ttu-id="36257-112">En offentlig IP-adress tilldelas omedelbart.</span><span class="sxs-lookup"><span data-stu-id="36257-112">A public IP address gets allocated immediately.</span></span>

### <span data-ttu-id="36257-113">2: ändra DNS-domännamn för en offentlig IP-adress</span><span class="sxs-lookup"><span data-stu-id="36257-113">2: Change DNS domain label of a public IP address</span></span>
```
PS C:\> $publicIp = Get-AzureRmPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName

PS C:\> $publicIp.DnsSettings.DomainNameLabel = "newdnsprefix"
    
PS C:\> Set-AzureRmPublicIpAddress -PublicIpAddress $publicIp

PS C:\> $publicIp = Get-AzureRmPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName
```

<span data-ttu-id="36257-114">Första kommandot får den offentliga IP-adressresursen med namnet $publicIPName i resurs gruppen $rgName.</span><span class="sxs-lookup"><span data-stu-id="36257-114">First command gets the public IP address resource with name $publicIPName in the resource group $rgName.</span></span>
<span data-ttu-id="36257-115">Med det andra kommandot anges egenskapen DomainNameLabel till det obligatoriska DNS-prefixet.</span><span class="sxs-lookup"><span data-stu-id="36257-115">Second command sets the DomainNameLabel property to the required dns prefix.</span></span>
<span data-ttu-id="36257-116">Set-AzureRmPublicIPAddress kommando uppdaterar den offentliga IP-adressresursen med det uppdaterade objektet.</span><span class="sxs-lookup"><span data-stu-id="36257-116">Set-AzureRmPublicIPAddress command updates the public IP address resource with the updated object.</span></span> <span data-ttu-id="36257-117">DomainNameLabel & FQDN ändras som förväntat.</span><span class="sxs-lookup"><span data-stu-id="36257-117">DomainNameLabel & Fqdn are modified as expected.</span></span>

## <span data-ttu-id="36257-118">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="36257-118">PARAMETERS</span></span>

### <span data-ttu-id="36257-119">-PublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="36257-119">-PublicIpAddress</span></span>
<span data-ttu-id="36257-120">Anger ett **PublicIpAddress** -objekt som representerar mål tillståndet som den offentliga IP-adressen ska anges för.</span><span class="sxs-lookup"><span data-stu-id="36257-120">Specifies a **PublicIpAddress** object that represents the goal state to which the public IP address should be set.</span></span>

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

### <span data-ttu-id="36257-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="36257-121">-DefaultProfile</span></span>
<span data-ttu-id="36257-122">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="36257-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="36257-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="36257-123">CommonParameters</span></span>
<span data-ttu-id="36257-124">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="36257-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="36257-125">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="36257-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="36257-126">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="36257-126">INPUTS</span></span>

### <span data-ttu-id="36257-127">PSPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="36257-127">PSPublicIpAddress</span></span>
<span data-ttu-id="36257-128">Parametern ' PublicIpAddress ' godkänner värdet av typen ' PSPublicIpAddress ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="36257-128">Parameter 'PublicIpAddress' accepts value of type 'PSPublicIpAddress' from the pipeline</span></span>

## <span data-ttu-id="36257-129">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="36257-129">OUTPUTS</span></span>

### <span data-ttu-id="36257-130">Microsoft. Azure. commands. Networks. Models. PSPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="36257-130">Microsoft.Azure.Commands.Network.Models.PSPublicIpAddress</span></span>

## <span data-ttu-id="36257-131">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="36257-131">NOTES</span></span>

## <span data-ttu-id="36257-132">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="36257-132">RELATED LINKS</span></span>

[<span data-ttu-id="36257-133">Get-AzureRmPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="36257-133">Get-AzureRmPublicIpAddress</span></span>](./Get-AzureRmPublicIpAddress.md)

[<span data-ttu-id="36257-134">Get-AzureRmPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="36257-134">Get-AzureRmPublicIpAddress</span></span>](./Get-AzureRmPublicIpAddress.md)

[<span data-ttu-id="36257-135">New-AzureRmPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="36257-135">New-AzureRmPublicIpAddress</span></span>](./New-AzureRmPublicIpAddress.md)

[<span data-ttu-id="36257-136">Remove-AzureRmPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="36257-136">Remove-AzureRmPublicIpAddress</span></span>](./Remove-AzureRmPublicIpAddress.md)


