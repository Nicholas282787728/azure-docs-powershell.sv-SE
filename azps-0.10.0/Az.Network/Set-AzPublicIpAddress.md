---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: EC798838-1850-4E88-B17F-D2F00F2D4EE9
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azpublicipaddress
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Set-AzPublicIpAddress.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Set-AzPublicIpAddress.md
ms.openlocfilehash: 53d5e15e6354e359461e59728e0776b7d3ec99ea
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93924166"
---
# <span data-ttu-id="c07c5-101">Set-AzPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="c07c5-101">Set-AzPublicIpAddress</span></span>

## <span data-ttu-id="c07c5-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="c07c5-102">SYNOPSIS</span></span>
<span data-ttu-id="c07c5-103">Anger mål tillstånd för en offentlig IP-adress.</span><span class="sxs-lookup"><span data-stu-id="c07c5-103">Sets the goal state for a public IP address.</span></span>

## <span data-ttu-id="c07c5-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="c07c5-104">SYNTAX</span></span>

```
Set-AzPublicIpAddress -PublicIpAddress <PSPublicIpAddress> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c07c5-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="c07c5-105">DESCRIPTION</span></span>
<span data-ttu-id="c07c5-106">Cmdleten **set-AzPublicIpAddress** anger mål tillståndet för en offentlig IP-adress.</span><span class="sxs-lookup"><span data-stu-id="c07c5-106">The **Set-AzPublicIpAddress** cmdlet sets the goal state for a public IP address.</span></span>

## <span data-ttu-id="c07c5-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="c07c5-107">EXAMPLES</span></span>

### <span data-ttu-id="c07c5-108">1: ändra tilldelnings metod för en offentlig IP-adress</span><span class="sxs-lookup"><span data-stu-id="c07c5-108">1: Change allocation method of a public IP address</span></span>
```
PS C:\> $publicIp = Get-AzPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName

PS C:\> $publicIp.PublicIpAllocationMethod = "Dynamic"
    
PS C:\> Set-AzPublicIpAddress -PublicIpAddress $publicIp

PS C:\> $publicIp = Get-AzPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName
```

 <span data-ttu-id="c07c5-109">Första kommandot får den offentliga IP-adressresursen med namnet $publicIPName i resurs gruppen $rgName.</span><span class="sxs-lookup"><span data-stu-id="c07c5-109">First command gets the public IP address resource with name $publicIPName in the resource group $rgName.</span></span>
<span data-ttu-id="c07c5-110">Andra kommando anger tilldelnings metod för det offentliga IP-adress-objektet till "statisk".</span><span class="sxs-lookup"><span data-stu-id="c07c5-110">Second command sets the allocation method of the public IP address object to "Static".</span></span>
<span data-ttu-id="c07c5-111">Set-AzPublicIPAddress kommando uppdaterar den offentliga IP-adressresursen med det uppdaterade objektet och ändrar tilldelnings metoden till "statisk".</span><span class="sxs-lookup"><span data-stu-id="c07c5-111">Set-AzPublicIPAddress command updates the public IP address resource with the updated object, and modifies the allocation method to 'Static'.</span></span> <span data-ttu-id="c07c5-112">En offentlig IP-adress tilldelas omedelbart.</span><span class="sxs-lookup"><span data-stu-id="c07c5-112">A public IP address gets allocated immediately.</span></span>

### <span data-ttu-id="c07c5-113">2: ändra DNS-domännamn för en offentlig IP-adress</span><span class="sxs-lookup"><span data-stu-id="c07c5-113">2: Change DNS domain label of a public IP address</span></span>
```
PS C:\> $publicIp = Get-AzPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName

PS C:\> $publicIp.DnsSettings.DomainNameLabel = "newdnsprefix"
    
PS C:\> Set-AzPublicIpAddress -PublicIpAddress $publicIp

PS C:\> $publicIp = Get-AzPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName
```

<span data-ttu-id="c07c5-114">Första kommandot får den offentliga IP-adressresursen med namnet $publicIPName i resurs gruppen $rgName.</span><span class="sxs-lookup"><span data-stu-id="c07c5-114">First command gets the public IP address resource with name $publicIPName in the resource group $rgName.</span></span>
<span data-ttu-id="c07c5-115">Med det andra kommandot anges egenskapen DomainNameLabel till det obligatoriska DNS-prefixet.</span><span class="sxs-lookup"><span data-stu-id="c07c5-115">Second command sets the DomainNameLabel property to the required dns prefix.</span></span>
<span data-ttu-id="c07c5-116">Set-AzPublicIPAddress kommando uppdaterar den offentliga IP-adressresursen med det uppdaterade objektet.</span><span class="sxs-lookup"><span data-stu-id="c07c5-116">Set-AzPublicIPAddress command updates the public IP address resource with the updated object.</span></span> <span data-ttu-id="c07c5-117">DomainNameLabel & FQDN ändras som förväntat.</span><span class="sxs-lookup"><span data-stu-id="c07c5-117">DomainNameLabel & Fqdn are modified as expected.</span></span>

## <span data-ttu-id="c07c5-118">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="c07c5-118">PARAMETERS</span></span>

### <span data-ttu-id="c07c5-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c07c5-119">-AsJob</span></span>
<span data-ttu-id="c07c5-120">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="c07c5-120">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="c07c5-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c07c5-121">-DefaultProfile</span></span>
<span data-ttu-id="c07c5-122">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="c07c5-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c07c5-123">-PublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="c07c5-123">-PublicIpAddress</span></span>
<span data-ttu-id="c07c5-124">Anger ett **PublicIpAddress** -objekt som representerar mål tillståndet som den offentliga IP-adressen ska anges för.</span><span class="sxs-lookup"><span data-stu-id="c07c5-124">Specifies a **PublicIpAddress** object that represents the goal state to which the public IP address should be set.</span></span>

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

### <span data-ttu-id="c07c5-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c07c5-125">CommonParameters</span></span>
<span data-ttu-id="c07c5-126">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c07c5-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c07c5-127">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c07c5-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c07c5-128">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="c07c5-128">INPUTS</span></span>

### <span data-ttu-id="c07c5-129">PSPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="c07c5-129">PSPublicIpAddress</span></span>
<span data-ttu-id="c07c5-130">Parametern ' PublicIpAddress ' godkänner värdet av typen ' PSPublicIpAddress ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="c07c5-130">Parameter 'PublicIpAddress' accepts value of type 'PSPublicIpAddress' from the pipeline</span></span>

## <span data-ttu-id="c07c5-131">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="c07c5-131">OUTPUTS</span></span>

### <span data-ttu-id="c07c5-132">Microsoft. Azure. commands. Networks. Models. PSPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="c07c5-132">Microsoft.Azure.Commands.Network.Models.PSPublicIpAddress</span></span>

## <span data-ttu-id="c07c5-133">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="c07c5-133">NOTES</span></span>

## <span data-ttu-id="c07c5-134">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="c07c5-134">RELATED LINKS</span></span>

[<span data-ttu-id="c07c5-135">Get-AzPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="c07c5-135">Get-AzPublicIpAddress</span></span>](./Get-AzPublicIpAddress.md)

[<span data-ttu-id="c07c5-136">New-AzPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="c07c5-136">New-AzPublicIpAddress</span></span>](./New-AzPublicIpAddress.md)

[<span data-ttu-id="c07c5-137">Remove-AzPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="c07c5-137">Remove-AzPublicIpAddress</span></span>](./Remove-AzPublicIpAddress.md)


