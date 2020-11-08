---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: 9FCECA04-9855-461C-9470-85312993C4B1
online version: ''
schema: 2.0.0
ms.openlocfilehash: 5bb7bb3e708720b481edc4489d858c70736eac95
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94099256"
---
# <span data-ttu-id="ad4f7-101">Start-AzureVNetGatewayDiagnostics</span><span class="sxs-lookup"><span data-stu-id="ad4f7-101">Start-AzureVNetGatewayDiagnostics</span></span>

## <span data-ttu-id="ad4f7-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="ad4f7-102">SYNOPSIS</span></span>
<span data-ttu-id="ad4f7-103">Startar Gateway Diagnostics för en VPN-gateway.</span><span class="sxs-lookup"><span data-stu-id="ad4f7-103">Starts gateway diagnostics for a VPN gateway.</span></span>

## <span data-ttu-id="ad4f7-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="ad4f7-104">SYNTAX</span></span>

```
Start-AzureVNetGatewayDiagnostics -VNetName <String> -CaptureDurationInSeconds <Int32>
 [-ContainerName <String>] -StorageContext <AzureStorageContext> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="ad4f7-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="ad4f7-105">DESCRIPTION</span></span>
<span data-ttu-id="ad4f7-106">Cmdleten **Start-AzureVNetGatewayDiagnostics** startar en ny Gateway-felsökningssession för en VPN-gateway (virtuellt privat nätverk).</span><span class="sxs-lookup"><span data-stu-id="ad4f7-106">The **Start-AzureVNetGatewayDiagnostics** cmdlet starts a new gateway diagnostics session for a virtual private network (VPN) gateway.</span></span>
<span data-ttu-id="ad4f7-107">Endast en gateway-diagnostiksessionen kan köras åt gången.</span><span class="sxs-lookup"><span data-stu-id="ad4f7-107">Only one gateway diagnostics session can run at a time.</span></span>
<span data-ttu-id="ad4f7-108">Om du kör denna cmdlet när en gateway-session körs, returnerar denna cmdlet ett fel.</span><span class="sxs-lookup"><span data-stu-id="ad4f7-108">If you run this cmdlet while a gateway diagnostics session is running, this cmdlet returns an error.</span></span>

## <span data-ttu-id="ad4f7-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="ad4f7-109">EXAMPLES</span></span>

## <span data-ttu-id="ad4f7-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="ad4f7-110">PARAMETERS</span></span>

### <span data-ttu-id="ad4f7-111">-CaptureDurationInSeconds</span><span class="sxs-lookup"><span data-stu-id="ad4f7-111">-CaptureDurationInSeconds</span></span>
<span data-ttu-id="ad4f7-112">Anger fångst längden i sekunder.</span><span class="sxs-lookup"><span data-stu-id="ad4f7-112">Specifies the capture duration in seconds.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ad4f7-113">-ContainerName</span><span class="sxs-lookup"><span data-stu-id="ad4f7-113">-ContainerName</span></span>
<span data-ttu-id="ad4f7-114">Anger namnet på en Azure-behållare.</span><span class="sxs-lookup"><span data-stu-id="ad4f7-114">Specifies the name of an Azure container.</span></span>
<span data-ttu-id="ad4f7-115">Denna cmdlet lagrar resultat i behållaren som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="ad4f7-115">This cmdlet stores results in the container that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ad4f7-116">-Profil</span><span class="sxs-lookup"><span data-stu-id="ad4f7-116">-Profile</span></span>
<span data-ttu-id="ad4f7-117">Anger den Azure-profil från vilken denna cmdlet läser.</span><span class="sxs-lookup"><span data-stu-id="ad4f7-117">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="ad4f7-118">Om du inte anger en profil läser denna cmdlet från den lokala standard profilen.</span><span class="sxs-lookup"><span data-stu-id="ad4f7-118">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="ad4f7-119">-StorageContext</span><span class="sxs-lookup"><span data-stu-id="ad4f7-119">-StorageContext</span></span>
<span data-ttu-id="ad4f7-120">Anger en Azure Storage-kontext.</span><span class="sxs-lookup"><span data-stu-id="ad4f7-120">Specifies an Azure storage context.</span></span>
<span data-ttu-id="ad4f7-121">Denna cmdlet lagrar resultat genom att använda den lagrings kontext som anges i den här parametern.</span><span class="sxs-lookup"><span data-stu-id="ad4f7-121">This cmdlet stores results by using the storage context that this parameter specifies.</span></span>

```yaml
Type: AzureStorageContext
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ad4f7-122">-VNetName</span><span class="sxs-lookup"><span data-stu-id="ad4f7-122">-VNetName</span></span>
<span data-ttu-id="ad4f7-123">Anger det virtuella nätverk som innehåller en virtuell nätverksgateway för vilken den här cmdleten kör diagnostik.</span><span class="sxs-lookup"><span data-stu-id="ad4f7-123">Specifies the virtual network that contains a virtual network gateway for which this cmdlet runs diagnostics.</span></span>

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

### <span data-ttu-id="ad4f7-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ad4f7-124">CommonParameters</span></span>
<span data-ttu-id="ad4f7-125">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ad4f7-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ad4f7-126">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ad4f7-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ad4f7-127">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="ad4f7-127">INPUTS</span></span>

## <span data-ttu-id="ad4f7-128">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="ad4f7-128">OUTPUTS</span></span>

## <span data-ttu-id="ad4f7-129">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="ad4f7-129">NOTES</span></span>

## <span data-ttu-id="ad4f7-130">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="ad4f7-130">RELATED LINKS</span></span>

[<span data-ttu-id="ad4f7-131">Get-AzureVNetGatewayDiagnostics</span><span class="sxs-lookup"><span data-stu-id="ad4f7-131">Get-AzureVNetGatewayDiagnostics</span></span>](./Get-AzureVNetGatewayDiagnostics.md)

[<span data-ttu-id="ad4f7-132">Stopp-AzureVNetGatewayDiagnostics</span><span class="sxs-lookup"><span data-stu-id="ad4f7-132">Stop-AzureVNetGatewayDiagnostics</span></span>](./Stop-AzureVNetGatewayDiagnostics.md)


