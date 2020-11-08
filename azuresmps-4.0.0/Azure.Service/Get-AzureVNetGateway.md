---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: 4024D20D-46DF-4ED8-A091-E6E17F840E40
online version: ''
schema: 2.0.0
ms.openlocfilehash: 92c6ba8827906fbfc51b121e4500dea3ec4555d9
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94099509"
---
# <span data-ttu-id="07187-101">Get-AzureVNetGateway</span><span class="sxs-lookup"><span data-stu-id="07187-101">Get-AzureVNetGateway</span></span>

## <span data-ttu-id="07187-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="07187-102">SYNOPSIS</span></span>
<span data-ttu-id="07187-103">Hämtar statusen för en virtuell nätverksgateway.</span><span class="sxs-lookup"><span data-stu-id="07187-103">Gets the status of a virtual network gateway.</span></span>

## <span data-ttu-id="07187-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="07187-104">SYNTAX</span></span>

```
Get-AzureVNetGateway -VNetName <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="07187-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="07187-105">DESCRIPTION</span></span>
<span data-ttu-id="07187-106">Cmdleten **Get-AzureVNetGateway** får statusen för en befintlig virtuell nätverksgateway.</span><span class="sxs-lookup"><span data-stu-id="07187-106">The **Get-AzureVNetGateway** cmdlet gets the status of an existing virtual network gateway.</span></span>

## <span data-ttu-id="07187-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="07187-107">EXAMPLES</span></span>

### <span data-ttu-id="07187-108">Exempel 1: få statusen för en virtuell nätverksgateway</span><span class="sxs-lookup"><span data-stu-id="07187-108">Example 1: Get the status of a virtual network gateway</span></span>
```
PS C:\> Get-AzureVNetGateway -VNetName "ContosoVN07"
```

<span data-ttu-id="07187-109">Det här kommandot får statusen för den virtuella Nätverksgatewayen för det virtuella nätverket som heter ContosoVN07.</span><span class="sxs-lookup"><span data-stu-id="07187-109">This command gets that status of the virtual network gateway for the virtual network named ContosoVN07.</span></span>

## <span data-ttu-id="07187-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="07187-110">PARAMETERS</span></span>

### <span data-ttu-id="07187-111">-Profil</span><span class="sxs-lookup"><span data-stu-id="07187-111">-Profile</span></span>
<span data-ttu-id="07187-112">Anger den Azure-profil från vilken denna cmdlet läser.</span><span class="sxs-lookup"><span data-stu-id="07187-112">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="07187-113">Om du inte anger en profil läser denna cmdlet från den lokala standard profilen.</span><span class="sxs-lookup"><span data-stu-id="07187-113">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="07187-114">-VNetName</span><span class="sxs-lookup"><span data-stu-id="07187-114">-VNetName</span></span>
<span data-ttu-id="07187-115">Anger det virtuella nätverk som innehåller den virtuella Nätverksgatewayen som den här cmdleten får status för.</span><span class="sxs-lookup"><span data-stu-id="07187-115">Specifies the virtual network that contains the virtual network gateway for which this cmdlet gets status.</span></span>

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

### <span data-ttu-id="07187-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="07187-116">CommonParameters</span></span>
<span data-ttu-id="07187-117">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="07187-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="07187-118">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="07187-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="07187-119">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="07187-119">INPUTS</span></span>

## <span data-ttu-id="07187-120">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="07187-120">OUTPUTS</span></span>

## <span data-ttu-id="07187-121">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="07187-121">NOTES</span></span>

## <span data-ttu-id="07187-122">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="07187-122">RELATED LINKS</span></span>

[<span data-ttu-id="07187-123">New-AzureVNetGateway</span><span class="sxs-lookup"><span data-stu-id="07187-123">New-AzureVNetGateway</span></span>](./New-AzureVNetGateway.md)

[<span data-ttu-id="07187-124">Remove-AzureVNetGateway</span><span class="sxs-lookup"><span data-stu-id="07187-124">Remove-AzureVNetGateway</span></span>](./Remove-AzureVNetGateway.md)

[<span data-ttu-id="07187-125">Reset-AzureVNetGateway</span><span class="sxs-lookup"><span data-stu-id="07187-125">Reset-AzureVNetGateway</span></span>](./Reset-AzureVNetGateway.md)

[<span data-ttu-id="07187-126">Ändra storlek – AzureVNetGateway</span><span class="sxs-lookup"><span data-stu-id="07187-126">Resize-AzureVNetGateway</span></span>](./Resize-AzureVNetGateway.md)

[<span data-ttu-id="07187-127">Set-AzureVNetGatewayKey</span><span class="sxs-lookup"><span data-stu-id="07187-127">Set-AzureVNetGatewayKey</span></span>](./Set-AzureVNetGatewayKey.md)


