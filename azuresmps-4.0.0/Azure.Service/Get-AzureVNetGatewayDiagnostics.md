---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: 22E8CB18-8CDD-4992-AB81-E1BB400E6BC7
online version: ''
schema: 2.0.0
ms.openlocfilehash: 294e931529b7de939a6a5c20181d48b18da1e892
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94099507"
---
# <span data-ttu-id="9c0c5-101">Get-AzureVNetGatewayDiagnostics</span><span class="sxs-lookup"><span data-stu-id="9c0c5-101">Get-AzureVNetGatewayDiagnostics</span></span>

## <span data-ttu-id="9c0c5-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="9c0c5-102">SYNOPSIS</span></span>
<span data-ttu-id="9c0c5-103">Hämtar diagnostikens aktuella status för en virtuell nätverksgateway.</span><span class="sxs-lookup"><span data-stu-id="9c0c5-103">Gets the current state of diagnostics for a virtual network gateway.</span></span>

## <span data-ttu-id="9c0c5-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="9c0c5-104">SYNTAX</span></span>

```
Get-AzureVNetGatewayDiagnostics -VNetName <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="9c0c5-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="9c0c5-105">DESCRIPTION</span></span>
<span data-ttu-id="9c0c5-106">Cmdleten **Get-AzureVNetGatewayDiagnostics** hämtar det aktuella tillståndet för diagnostik för en virtuell nätverksgateway.</span><span class="sxs-lookup"><span data-stu-id="9c0c5-106">The **Get-AzureVNetGatewayDiagnostics** cmdlet gets the current state of diagnostics for a virtual network gateway.</span></span>
<span data-ttu-id="9c0c5-107">Om det finns ett binärt objekt (BLOB) där **Start-AzureVNetGatewayDiagnostics** har sparat en tidigare diagnostisk session, returnerar denna cmdlet också URL-adressen till blobben där cmdleten sparade den diagnostiksessionen.</span><span class="sxs-lookup"><span data-stu-id="9c0c5-107">If a binary large object (blob) exists where the **Start-AzureVNetGatewayDiagnostics** saved a previous diagnostics session, this cmdlet also returns the URL of the blob where that cmdlet saved that diagnostics session.</span></span>

## <span data-ttu-id="9c0c5-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="9c0c5-108">EXAMPLES</span></span>

## <span data-ttu-id="9c0c5-109">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="9c0c5-109">PARAMETERS</span></span>

### <span data-ttu-id="9c0c5-110">-Profil</span><span class="sxs-lookup"><span data-stu-id="9c0c5-110">-Profile</span></span>
<span data-ttu-id="9c0c5-111">Anger den Azure-profil från vilken denna cmdlet läser.</span><span class="sxs-lookup"><span data-stu-id="9c0c5-111">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="9c0c5-112">Om du inte anger en profil läser denna cmdlet från den lokala standard profilen.</span><span class="sxs-lookup"><span data-stu-id="9c0c5-112">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="9c0c5-113">-VNetName</span><span class="sxs-lookup"><span data-stu-id="9c0c5-113">-VNetName</span></span>
<span data-ttu-id="9c0c5-114">Anger det virtuella nätverk som innehåller en virtuell nätverksgateway för vilken denna cmdlet får diagnostik.</span><span class="sxs-lookup"><span data-stu-id="9c0c5-114">Specifies the virtual network that contains a virtual network gateway for which this cmdlet gets diagnostics.</span></span>

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

### <span data-ttu-id="9c0c5-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9c0c5-115">CommonParameters</span></span>
<span data-ttu-id="9c0c5-116">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9c0c5-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9c0c5-117">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9c0c5-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9c0c5-118">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="9c0c5-118">INPUTS</span></span>

## <span data-ttu-id="9c0c5-119">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="9c0c5-119">OUTPUTS</span></span>

## <span data-ttu-id="9c0c5-120">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="9c0c5-120">NOTES</span></span>

## <span data-ttu-id="9c0c5-121">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="9c0c5-121">RELATED LINKS</span></span>

[<span data-ttu-id="9c0c5-122">Start-AzureVNetGatewayDiagnostics</span><span class="sxs-lookup"><span data-stu-id="9c0c5-122">Start-AzureVNetGatewayDiagnostics</span></span>](./Start-AzureVNetGatewayDiagnostics.md)

[<span data-ttu-id="9c0c5-123">Stopp-AzureVNetGatewayDiagnostics</span><span class="sxs-lookup"><span data-stu-id="9c0c5-123">Stop-AzureVNetGatewayDiagnostics</span></span>](./Stop-AzureVNetGatewayDiagnostics.md)


