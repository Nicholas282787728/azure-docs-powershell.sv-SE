---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: 706CBF65-C796-4525-BAEB-AAFAD44C0464
online version: ''
schema: 2.0.0
ms.openlocfilehash: d37c2ce3b32d23f7c5bb682d2116de84cc90f047
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94099249"
---
# <span data-ttu-id="65224-101">Stop-AzureVNetGatewayDiagnostics</span><span class="sxs-lookup"><span data-stu-id="65224-101">Stop-AzureVNetGatewayDiagnostics</span></span>

## <span data-ttu-id="65224-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="65224-102">SYNOPSIS</span></span>
<span data-ttu-id="65224-103">Stoppar en aktive tids session med en VPN-gateway.</span><span class="sxs-lookup"><span data-stu-id="65224-103">Stops a running VPN gateway diagnostics session.</span></span>

## <span data-ttu-id="65224-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="65224-104">SYNTAX</span></span>

```
Stop-AzureVNetGatewayDiagnostics -VNetName <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="65224-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="65224-105">DESCRIPTION</span></span>
<span data-ttu-id="65224-106">Cmdleten **Stop-AzureVNetGatewayDiagnostics** stoppar en aktiv session med Virtual Private Network (VPN) Gateway-diagnostik.</span><span class="sxs-lookup"><span data-stu-id="65224-106">The **Stop-AzureVNetGatewayDiagnostics** cmdlet stops a running virtual private network (VPN) gateway diagnostics session.</span></span>
<span data-ttu-id="65224-107">Det här kommandot sparar resultatet av diagnostikprogrammet för det lagrings konto som cmdleten **Start-AzureVNetGatewayDiagnostics** anger.</span><span class="sxs-lookup"><span data-stu-id="65224-107">This command saves the results of the diagnostics session to the storage account that the **Start-AzureVNetGatewayDiagnostics** cmdlet specifies.</span></span>

## <span data-ttu-id="65224-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="65224-108">EXAMPLES</span></span>

## <span data-ttu-id="65224-109">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="65224-109">PARAMETERS</span></span>

### <span data-ttu-id="65224-110">-Profil</span><span class="sxs-lookup"><span data-stu-id="65224-110">-Profile</span></span>
<span data-ttu-id="65224-111">Anger den Azure-profil från vilken denna cmdlet läser.</span><span class="sxs-lookup"><span data-stu-id="65224-111">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="65224-112">Om du inte anger en profil läser denna cmdlet från den lokala standard profilen.</span><span class="sxs-lookup"><span data-stu-id="65224-112">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="65224-113">-VNetName</span><span class="sxs-lookup"><span data-stu-id="65224-113">-VNetName</span></span>
<span data-ttu-id="65224-114">Anger det virtuella nätverk som innehåller en virtuell nätverksgateway för vilken denna cmdlet stoppar diagnostik.</span><span class="sxs-lookup"><span data-stu-id="65224-114">Specifies the virtual network that contains a virtual network gateway for which this cmdlet stops diagnostics.</span></span>

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

### <span data-ttu-id="65224-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="65224-115">CommonParameters</span></span>
<span data-ttu-id="65224-116">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="65224-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="65224-117">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="65224-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="65224-118">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="65224-118">INPUTS</span></span>

## <span data-ttu-id="65224-119">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="65224-119">OUTPUTS</span></span>

## <span data-ttu-id="65224-120">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="65224-120">NOTES</span></span>

## <span data-ttu-id="65224-121">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="65224-121">RELATED LINKS</span></span>

[<span data-ttu-id="65224-122">Get-AzureVNetGatewayDiagnostics</span><span class="sxs-lookup"><span data-stu-id="65224-122">Get-AzureVNetGatewayDiagnostics</span></span>](./Get-AzureVNetGatewayDiagnostics.md)

[<span data-ttu-id="65224-123">Start-AzureVNetGatewayDiagnostics</span><span class="sxs-lookup"><span data-stu-id="65224-123">Start-AzureVNetGatewayDiagnostics</span></span>](./Start-AzureVNetGatewayDiagnostics.md)


