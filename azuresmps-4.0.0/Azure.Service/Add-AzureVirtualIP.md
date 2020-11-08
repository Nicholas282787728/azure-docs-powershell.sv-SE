---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: FBED8515-4216-4AB6-B34E-D14A6063A3A7
online version: ''
schema: 2.0.0
ms.openlocfilehash: c2f145ec51bc6744d877661554e3d8e475d722fb
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94093439"
---
# <span data-ttu-id="e5360-101">Add-AzureVirtualIP</span><span class="sxs-lookup"><span data-stu-id="e5360-101">Add-AzureVirtualIP</span></span>

## <span data-ttu-id="e5360-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="e5360-102">SYNOPSIS</span></span>
<span data-ttu-id="e5360-103">Lägger till en virtuell IP-adress i en moln tjänst.</span><span class="sxs-lookup"><span data-stu-id="e5360-103">Adds a virtual IP to a cloud service.</span></span>

## <span data-ttu-id="e5360-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="e5360-104">SYNTAX</span></span>

```
Add-AzureVirtualIP [-ServiceName] <String> [-VirtualIPName] <String> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="e5360-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="e5360-105">DESCRIPTION</span></span>
<span data-ttu-id="e5360-106">Cmdleten **Add-AzureVirtualIP** lägger till en ny virtuell IP-adress (VIP) i din Azure-tjänst.</span><span class="sxs-lookup"><span data-stu-id="e5360-106">The **Add-AzureVirtualIP** cmdlet adds a new virtual IP (VIP) to your Azure service.</span></span>
<span data-ttu-id="e5360-107">Den nya virtuella IP-adressen har ett namn men tilldelas inte en IP-adress.</span><span class="sxs-lookup"><span data-stu-id="e5360-107">The new virtual IP has a name but is not allocated an IP address.</span></span>

<span data-ttu-id="e5360-108">IP-adressen tilldelas bara när du associerar en slut punkt till VIP.</span><span class="sxs-lookup"><span data-stu-id="e5360-108">The IP address is allocated only when you associate an endpoint to the VIP.</span></span>
<span data-ttu-id="e5360-109">Mer information finns i Add-AzureEndpoint.</span><span class="sxs-lookup"><span data-stu-id="e5360-109">See Add-AzureEndpoint for more details.</span></span>

<span data-ttu-id="e5360-110">Ditt abonnemang debiteras endast för extra VIP när de är kopplade till en slut punkt.</span><span class="sxs-lookup"><span data-stu-id="e5360-110">Your subscription is charged for extra VIPs only once they are associated with an endpoint.</span></span>

## <span data-ttu-id="e5360-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="e5360-111">EXAMPLES</span></span>

### <span data-ttu-id="e5360-112">Exempel 1: lägga till en virtuell IP-adress till en tjänst</span><span class="sxs-lookup"><span data-stu-id="e5360-112">Example 1: Add a virtual IP to a service</span></span>
```
PS C:\> Add-AzureVirtualIP -VirtualIPName "Vip01" -ServiceName "ContosoService03"
OperationDescription OperationId                          OperationStatus
-------------------- -----------                          ---------------
Add-AzureVirtualIP   4bd7b638-d2e7-216f-ba38-5221233d70ce Succeeded
```

<span data-ttu-id="e5360-113">Det här kommandot lägger till en virtuell IP-adress till en tjänst.</span><span class="sxs-lookup"><span data-stu-id="e5360-113">This command adds a virtual IP address to a service.</span></span>

## <span data-ttu-id="e5360-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="e5360-114">PARAMETERS</span></span>

### <span data-ttu-id="e5360-115">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="e5360-115">-InformationAction</span></span>
<span data-ttu-id="e5360-116">Anger hur den här cmdleten svarar på en informations händelse.</span><span class="sxs-lookup"><span data-stu-id="e5360-116">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="e5360-117">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="e5360-117">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="e5360-118">Vidare</span><span class="sxs-lookup"><span data-stu-id="e5360-118">Continue</span></span>
- <span data-ttu-id="e5360-119">Över</span><span class="sxs-lookup"><span data-stu-id="e5360-119">Ignore</span></span>
- <span data-ttu-id="e5360-120">Inquire</span><span class="sxs-lookup"><span data-stu-id="e5360-120">Inquire</span></span>
- <span data-ttu-id="e5360-121">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="e5360-121">SilentlyContinue</span></span>
- <span data-ttu-id="e5360-122">Stanna</span><span class="sxs-lookup"><span data-stu-id="e5360-122">Stop</span></span>
- <span data-ttu-id="e5360-123">Avbryt</span><span class="sxs-lookup"><span data-stu-id="e5360-123">Suspend</span></span>

```yaml
Type: ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e5360-124">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="e5360-124">-InformationVariable</span></span>
<span data-ttu-id="e5360-125">Anger en informations variabel.</span><span class="sxs-lookup"><span data-stu-id="e5360-125">Specifies an information variable.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e5360-126">-Profil</span><span class="sxs-lookup"><span data-stu-id="e5360-126">-Profile</span></span>
<span data-ttu-id="e5360-127">Anger den Azure-profil från vilken denna cmdlet läser.</span><span class="sxs-lookup"><span data-stu-id="e5360-127">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="e5360-128">Om du inte anger en profil läser denna cmdlet från den lokala standard profilen.</span><span class="sxs-lookup"><span data-stu-id="e5360-128">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="e5360-129">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="e5360-129">-ServiceName</span></span>
<span data-ttu-id="e5360-130">Anger namnet på tjänsten.</span><span class="sxs-lookup"><span data-stu-id="e5360-130">Specifies the name of the service.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e5360-131">-VirtualIPName</span><span class="sxs-lookup"><span data-stu-id="e5360-131">-VirtualIPName</span></span>
<span data-ttu-id="e5360-132">Anger namnet på den virtuella IP-adressen.</span><span class="sxs-lookup"><span data-stu-id="e5360-132">Specifies the name of the virtual IP address.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e5360-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e5360-133">CommonParameters</span></span>
<span data-ttu-id="e5360-134">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e5360-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e5360-135">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e5360-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e5360-136">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="e5360-136">INPUTS</span></span>

## <span data-ttu-id="e5360-137">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="e5360-137">OUTPUTS</span></span>

### <span data-ttu-id="e5360-138">Microsoft. WindowsAzure. commands. Utilitiess. Common. ManagementOperationContext</span><span class="sxs-lookup"><span data-stu-id="e5360-138">Microsoft.WindowsAzure.Commands.Utilities.Common.ManagementOperationContext</span></span>

## <span data-ttu-id="e5360-139">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="e5360-139">NOTES</span></span>

## <span data-ttu-id="e5360-140">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="e5360-140">RELATED LINKS</span></span>

[<span data-ttu-id="e5360-141">Add-AzureEndpoint</span><span class="sxs-lookup"><span data-stu-id="e5360-141">Add-AzureEndpoint</span></span>](./Add-AzureEndpoint.md)

[<span data-ttu-id="e5360-142">Remove-AzureVirtualIP</span><span class="sxs-lookup"><span data-stu-id="e5360-142">Remove-AzureVirtualIP</span></span>](./Remove-AzureVirtualIP.md)


