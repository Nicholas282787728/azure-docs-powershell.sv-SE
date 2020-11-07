---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: EC798838-1850-4E88-B17F-D2F00F2D4EE9
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermpublicipaddress
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmPublicIpAddress.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmPublicIpAddress.md
ms.openlocfilehash: df1c03551d520a833e8b974ae2a2b71fe442c4c4
ms.sourcegitcommit: e0947ba0606618a565d8a99fa0e4bef7d028d7e7
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/21/2020
ms.locfileid: "93758442"
---
# <span data-ttu-id="0cca6-101">Set-AzureRmPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="0cca6-101">Set-AzureRmPublicIpAddress</span></span>

## <span data-ttu-id="0cca6-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="0cca6-102">SYNOPSIS</span></span>
<span data-ttu-id="0cca6-103">Anger mål tillstånd för en offentlig IP-adress.</span><span class="sxs-lookup"><span data-stu-id="0cca6-103">Sets the goal state for a public IP address.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0cca6-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="0cca6-104">SYNTAX</span></span>

```
Set-AzureRmPublicIpAddress -PublicIpAddress <PSPublicIpAddress> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0cca6-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="0cca6-105">DESCRIPTION</span></span>
<span data-ttu-id="0cca6-106">Cmdleten **set-AzureRmPublicIpAddress** anger mål tillståndet för en offentlig IP-adress.</span><span class="sxs-lookup"><span data-stu-id="0cca6-106">The **Set-AzureRmPublicIpAddress** cmdlet sets the goal state for a public IP address.</span></span>

## <span data-ttu-id="0cca6-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="0cca6-107">EXAMPLES</span></span>

### <span data-ttu-id="0cca6-108">1: ändra tilldelnings metod för en offentlig IP-adress</span><span class="sxs-lookup"><span data-stu-id="0cca6-108">1: Change allocation method of a public IP address</span></span>
```
PS C:\> $publicIp = Get-AzureRmPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName

PS C:\> $publicIp.PublicIpAllocationMethod = "Dynamic"
    
PS C:\> Set-AzureRmPublicIpAddress -PublicIpAddress $publicIp

PS C:\> $publicIp = Get-AzureRmPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName
```

 <span data-ttu-id="0cca6-109">Första kommandot får den offentliga IP-adressresursen med namnet $publicIPName i resurs gruppen $rgName.</span><span class="sxs-lookup"><span data-stu-id="0cca6-109">First command gets the public IP address resource with name $publicIPName in the resource group $rgName.</span></span>
<span data-ttu-id="0cca6-110">Andra kommando anger tilldelnings metod för det offentliga IP-adress-objektet till "statisk".</span><span class="sxs-lookup"><span data-stu-id="0cca6-110">Second command sets the allocation method of the public IP address object to "Static".</span></span>
<span data-ttu-id="0cca6-111">Set-AzureRmPublicIPAddress kommando uppdaterar den offentliga IP-adressresursen med det uppdaterade objektet och ändrar tilldelnings metoden till "statisk".</span><span class="sxs-lookup"><span data-stu-id="0cca6-111">Set-AzureRmPublicIPAddress command updates the public IP address resource with the updated object, and modifies the allocation method to 'Static'.</span></span> <span data-ttu-id="0cca6-112">En offentlig IP-adress tilldelas omedelbart.</span><span class="sxs-lookup"><span data-stu-id="0cca6-112">A public IP address gets allocated immediately.</span></span>

### <span data-ttu-id="0cca6-113">2: ändra DNS-domännamn för en offentlig IP-adress</span><span class="sxs-lookup"><span data-stu-id="0cca6-113">2: Change DNS domain label of a public IP address</span></span>
```
PS C:\> $publicIp = Get-AzureRmPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName

PS C:\> $publicIp.DnsSettings.DomainNameLabel = "newdnsprefix"
    
PS C:\> Set-AzureRmPublicIpAddress -PublicIpAddress $publicIp

PS C:\> $publicIp = Get-AzureRmPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName
```

<span data-ttu-id="0cca6-114">Första kommandot får den offentliga IP-adressresursen med namnet $publicIPName i resurs gruppen $rgName.</span><span class="sxs-lookup"><span data-stu-id="0cca6-114">First command gets the public IP address resource with name $publicIPName in the resource group $rgName.</span></span>
<span data-ttu-id="0cca6-115">Med det andra kommandot anges egenskapen DomainNameLabel till det obligatoriska DNS-prefixet.</span><span class="sxs-lookup"><span data-stu-id="0cca6-115">Second command sets the DomainNameLabel property to the required dns prefix.</span></span>
<span data-ttu-id="0cca6-116">Set-AzureRmPublicIPAddress kommando uppdaterar den offentliga IP-adressresursen med det uppdaterade objektet.</span><span class="sxs-lookup"><span data-stu-id="0cca6-116">Set-AzureRmPublicIPAddress command updates the public IP address resource with the updated object.</span></span> <span data-ttu-id="0cca6-117">DomainNameLabel & FQDN ändras som förväntat.</span><span class="sxs-lookup"><span data-stu-id="0cca6-117">DomainNameLabel & Fqdn are modified as expected.</span></span>

## <span data-ttu-id="0cca6-118">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="0cca6-118">PARAMETERS</span></span>

### <span data-ttu-id="0cca6-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="0cca6-119">-AsJob</span></span>
<span data-ttu-id="0cca6-120">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="0cca6-120">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0cca6-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0cca6-121">-DefaultProfile</span></span>
<span data-ttu-id="0cca6-122">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="0cca6-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0cca6-123">-PublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="0cca6-123">-PublicIpAddress</span></span>
<span data-ttu-id="0cca6-124">Anger ett **PublicIpAddress** -objekt som representerar mål tillståndet som den offentliga IP-adressen ska anges för.</span><span class="sxs-lookup"><span data-stu-id="0cca6-124">Specifies a **PublicIpAddress** object that represents the goal state to which the public IP address should be set.</span></span>

```yaml
Type: PSPublicIpAddress
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0cca6-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0cca6-125">CommonParameters</span></span>
<span data-ttu-id="0cca6-126">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0cca6-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0cca6-127">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0cca6-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0cca6-128">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="0cca6-128">INPUTS</span></span>

### <span data-ttu-id="0cca6-129">PSPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="0cca6-129">PSPublicIpAddress</span></span>
<span data-ttu-id="0cca6-130">Parametern ' PublicIpAddress ' godkänner värdet av typen ' PSPublicIpAddress ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="0cca6-130">Parameter 'PublicIpAddress' accepts value of type 'PSPublicIpAddress' from the pipeline</span></span>

## <span data-ttu-id="0cca6-131">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="0cca6-131">OUTPUTS</span></span>

### <span data-ttu-id="0cca6-132">Microsoft. Azure. commands. Networks. Models. PSPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="0cca6-132">Microsoft.Azure.Commands.Network.Models.PSPublicIpAddress</span></span>

## <span data-ttu-id="0cca6-133">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="0cca6-133">NOTES</span></span>

## <span data-ttu-id="0cca6-134">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="0cca6-134">RELATED LINKS</span></span>

[<span data-ttu-id="0cca6-135">Get-AzureRmPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="0cca6-135">Get-AzureRmPublicIpAddress</span></span>](./Get-AzureRmPublicIpAddress.md)

[<span data-ttu-id="0cca6-136">New-AzureRmPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="0cca6-136">New-AzureRmPublicIpAddress</span></span>](./New-AzureRmPublicIpAddress.md)

[<span data-ttu-id="0cca6-137">Remove-AzureRmPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="0cca6-137">Remove-AzureRmPublicIpAddress</span></span>](./Remove-AzureRmPublicIpAddress.md)


