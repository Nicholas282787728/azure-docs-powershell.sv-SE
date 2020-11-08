---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: DA5689DF-AA4A-4161-89B0-8055BF384274
online version: ''
schema: 2.0.0
ms.openlocfilehash: 7b71367ac18a753fad5425d0073b55cacb413e4b
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94099002"
---
# <span data-ttu-id="33247-101">Start-AzureVirtualNetworkGatewayDiagnostics</span><span class="sxs-lookup"><span data-stu-id="33247-101">Start-AzureVirtualNetworkGatewayDiagnostics</span></span>

## <span data-ttu-id="33247-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="33247-102">SYNOPSIS</span></span>
<span data-ttu-id="33247-103">Startar diagnostik för en virtuell nätverksgateway.</span><span class="sxs-lookup"><span data-stu-id="33247-103">Starts diagnostics for a virtual network gateway.</span></span>

## <span data-ttu-id="33247-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="33247-104">SYNTAX</span></span>

```
Start-AzureVirtualNetworkGatewayDiagnostics -GatewayId <String> [-CaptureDurationInSeconds <Int32>]
 [-ContainerName <String>] [-StorageContext <AzureStorageContext>] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="33247-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="33247-105">DESCRIPTION</span></span>
<span data-ttu-id="33247-106">Cmdleten **Start-AzureVirtualNetworkGatewayDiagnostics** startar en ny Gateway Diagnostics-session för en virtuell nätverksgateway.</span><span class="sxs-lookup"><span data-stu-id="33247-106">The **Start-AzureVirtualNetworkGatewayDiagnostics** cmdlet starts a new gateway diagnostics session for a virtual network gateway.</span></span>
<span data-ttu-id="33247-107">Endast en gateway-diagnostiksessionen kan köras åt gången.</span><span class="sxs-lookup"><span data-stu-id="33247-107">Only one gateway diagnostics session can run at a time.</span></span>
<span data-ttu-id="33247-108">Om du kör denna cmdlet när en gateway-session körs, returnerar denna cmdlet ett fel.</span><span class="sxs-lookup"><span data-stu-id="33247-108">If you run this cmdlet while a gateway diagnostics session is running, this cmdlet returns an error.</span></span>

## <span data-ttu-id="33247-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="33247-109">EXAMPLES</span></span>

## <span data-ttu-id="33247-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="33247-110">PARAMETERS</span></span>

### <span data-ttu-id="33247-111">-CaptureDurationInSeconds</span><span class="sxs-lookup"><span data-stu-id="33247-111">-CaptureDurationInSeconds</span></span>
<span data-ttu-id="33247-112">Anger fångst längden i sekunder.</span><span class="sxs-lookup"><span data-stu-id="33247-112">Specifies the capture duration in seconds.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="33247-113">-ContainerName</span><span class="sxs-lookup"><span data-stu-id="33247-113">-ContainerName</span></span>
<span data-ttu-id="33247-114">Anger namnet på en Azure-behållare.</span><span class="sxs-lookup"><span data-stu-id="33247-114">Specifies the name of an Azure container.</span></span>
<span data-ttu-id="33247-115">Denna cmdlet lagrar resultat i behållaren som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="33247-115">This cmdlet stores results in the container that this parameter specifies.</span></span>

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

### <span data-ttu-id="33247-116">-GatewayId</span><span class="sxs-lookup"><span data-stu-id="33247-116">-GatewayId</span></span>
<span data-ttu-id="33247-117">Anger ID för en gateway.</span><span class="sxs-lookup"><span data-stu-id="33247-117">Specifies the ID of a gateway.</span></span>

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

### <span data-ttu-id="33247-118">-Profil</span><span class="sxs-lookup"><span data-stu-id="33247-118">-Profile</span></span>
<span data-ttu-id="33247-119">Anger den Azure-profil från vilken denna cmdlet läser.</span><span class="sxs-lookup"><span data-stu-id="33247-119">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="33247-120">Om du inte anger en profil läser denna cmdlet från den lokala standard profilen.</span><span class="sxs-lookup"><span data-stu-id="33247-120">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="33247-121">-StorageContext</span><span class="sxs-lookup"><span data-stu-id="33247-121">-StorageContext</span></span>
<span data-ttu-id="33247-122">Anger en Azure Storage-kontext.</span><span class="sxs-lookup"><span data-stu-id="33247-122">Specifies an Azure storage context.</span></span>
<span data-ttu-id="33247-123">Denna cmdlet lagrar resultat genom att använda den lagrings kontext som anges i den här parametern.</span><span class="sxs-lookup"><span data-stu-id="33247-123">This cmdlet stores results by using the storage context that this parameter specifies.</span></span>

```yaml
Type: AzureStorageContext
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="33247-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="33247-124">CommonParameters</span></span>
<span data-ttu-id="33247-125">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="33247-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="33247-126">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="33247-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="33247-127">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="33247-127">INPUTS</span></span>

## <span data-ttu-id="33247-128">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="33247-128">OUTPUTS</span></span>

## <span data-ttu-id="33247-129">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="33247-129">NOTES</span></span>

## <span data-ttu-id="33247-130">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="33247-130">RELATED LINKS</span></span>

[<span data-ttu-id="33247-131">Get-AzureVirtualNetworkGatewayDiagnostics</span><span class="sxs-lookup"><span data-stu-id="33247-131">Get-AzureVirtualNetworkGatewayDiagnostics</span></span>](./Get-AzureVirtualNetworkGatewayDiagnostics.md)

[<span data-ttu-id="33247-132">Stopp-AzureVirtualNetworkGatewayDiagnostics</span><span class="sxs-lookup"><span data-stu-id="33247-132">Stop-AzureVirtualNetworkGatewayDiagnostics</span></span>](./Stop-AzureVirtualNetworkGatewayDiagnostics.md)


