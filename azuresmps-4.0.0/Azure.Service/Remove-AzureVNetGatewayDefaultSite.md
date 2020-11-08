---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: 67260128-D57B-4587-BB61-2475703ABA66
online version: ''
schema: 2.0.0
ms.openlocfilehash: 38aca36799c57dd5a135af99e4b99ab713d2b1ca
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94093215"
---
# <span data-ttu-id="45576-101">Remove-AzureVNetGatewayDefaultSite</span><span class="sxs-lookup"><span data-stu-id="45576-101">Remove-AzureVNetGatewayDefaultSite</span></span>

## <span data-ttu-id="45576-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="45576-102">SYNOPSIS</span></span>
<span data-ttu-id="45576-103">Tar bort standard vägen för tvingande tunnel trafik.</span><span class="sxs-lookup"><span data-stu-id="45576-103">Removes the default route for forced tunneling traffic.</span></span>

## <span data-ttu-id="45576-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="45576-104">SYNTAX</span></span>

```
Remove-AzureVNetGatewayDefaultSite -VNetName <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="45576-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="45576-105">DESCRIPTION</span></span>
<span data-ttu-id="45576-106">Cmdleten **Remove-AzureVNetGatewayDefaultSite** tar bort standard vägen till den lokala webbplatsen för tvingande tunnel trafik.</span><span class="sxs-lookup"><span data-stu-id="45576-106">The **Remove-AzureVNetGatewayDefaultSite** cmdlet removes the default route to the on-premises site for forced tunneling traffic.</span></span>
<span data-ttu-id="45576-107">Denna cmdlet tar bort vägen från en Azure Virtual Private Network (VPN) Gateway för ett virtuellt nätverk.</span><span class="sxs-lookup"><span data-stu-id="45576-107">This cmdlet removes the route from an Azure virtual private network (VPN) gateway for a virtual network.</span></span>

## <span data-ttu-id="45576-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="45576-108">EXAMPLES</span></span>

### <span data-ttu-id="45576-109">Exempel 1: ta bort en väg till standard webbplatsen</span><span class="sxs-lookup"><span data-stu-id="45576-109">Example 1: Remove a route to the default site</span></span>
```
PS C:\> Remove-AzureVNetGatewayDefaultSite -VnetName "ContosoVNet01"
```

<span data-ttu-id="45576-110">Det här kommandot tar bort vägen till standard webbplatsen från VPN för det virtuella nätverket med namnet ContosoVNet01.</span><span class="sxs-lookup"><span data-stu-id="45576-110">This command removes the route to the default site from the VPN of the virtual network named ContosoVNet01.</span></span>

## <span data-ttu-id="45576-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="45576-111">PARAMETERS</span></span>

### <span data-ttu-id="45576-112">-Profil</span><span class="sxs-lookup"><span data-stu-id="45576-112">-Profile</span></span>
<span data-ttu-id="45576-113">Anger den Azure-profil från vilken denna cmdlet läser.</span><span class="sxs-lookup"><span data-stu-id="45576-113">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="45576-114">Om du inte anger en profil läser denna cmdlet från den lokala standard profilen.</span><span class="sxs-lookup"><span data-stu-id="45576-114">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="45576-115">-VNetName</span><span class="sxs-lookup"><span data-stu-id="45576-115">-VNetName</span></span>
<span data-ttu-id="45576-116">Anger ett virtuellt nätverk.</span><span class="sxs-lookup"><span data-stu-id="45576-116">Specifies a virtual network.</span></span>
<span data-ttu-id="45576-117">Denna cmdlet tar bort standard vägen från VPN gateway för det virtuella nätverk som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="45576-117">This cmdlet removes the default route from the VPN gateway for the virtual network that this parameter specifies.</span></span>

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

### <span data-ttu-id="45576-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="45576-118">CommonParameters</span></span>
<span data-ttu-id="45576-119">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="45576-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="45576-120">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="45576-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="45576-121">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="45576-121">INPUTS</span></span>

## <span data-ttu-id="45576-122">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="45576-122">OUTPUTS</span></span>

## <span data-ttu-id="45576-123">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="45576-123">NOTES</span></span>

## <span data-ttu-id="45576-124">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="45576-124">RELATED LINKS</span></span>

[<span data-ttu-id="45576-125">Set-AzureVNetGatewayDefaultSite</span><span class="sxs-lookup"><span data-stu-id="45576-125">Set-AzureVNetGatewayDefaultSite</span></span>](./Set-AzureVNetGatewayDefaultSite.md)
