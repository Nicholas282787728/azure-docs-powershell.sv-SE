---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: C6D23ECB-C06E-4EB7-8096-33787E39694D
online version: ''
schema: 2.0.0
ms.openlocfilehash: 66f6bac80b219a2b3629b399bb568140a5cef217
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94099184"
---
# <span data-ttu-id="48b97-101">Set-AzureInternalLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="48b97-101">Set-AzureInternalLoadBalancer</span></span>

## <span data-ttu-id="48b97-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="48b97-102">SYNOPSIS</span></span>
<span data-ttu-id="48b97-103">Ändrar en intern belastnings Utjämnings konfiguration i en Azure-tjänst.</span><span class="sxs-lookup"><span data-stu-id="48b97-103">Modifies an internal load balancer configuration in an Azure service.</span></span>

## <span data-ttu-id="48b97-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="48b97-104">SYNTAX</span></span>

### <span data-ttu-id="48b97-105">ServiceAndSlot (standard)</span><span class="sxs-lookup"><span data-stu-id="48b97-105">ServiceAndSlot (Default)</span></span>
```
Set-AzureInternalLoadBalancer [-InternalLoadBalancerName] <String> [-ServiceName] <String>
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

### <span data-ttu-id="48b97-106">SubnetNameOnly</span><span class="sxs-lookup"><span data-stu-id="48b97-106">SubnetNameOnly</span></span>
```
Set-AzureInternalLoadBalancer [-InternalLoadBalancerName] <String> [-ServiceName] <String>
 [-SubnetName] <String> [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="48b97-107">SubnetNameAndIP</span><span class="sxs-lookup"><span data-stu-id="48b97-107">SubnetNameAndIP</span></span>
```
Set-AzureInternalLoadBalancer [-InternalLoadBalancerName] <String> [-ServiceName] <String>
 [-SubnetName] <String> [-StaticVNetIPAddress] <IPAddress> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="48b97-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="48b97-108">DESCRIPTION</span></span>
<span data-ttu-id="48b97-109">Cmdleten **set-AzureInternalLoadBalancer** ändrar en intern belastnings Utjämnings konfiguration i en Azure-tjänst.</span><span class="sxs-lookup"><span data-stu-id="48b97-109">The **Set-AzureInternalLoadBalancer** cmdlet modifies an internal load balancer configuration in an Azure service.</span></span>
<span data-ttu-id="48b97-110">För ett virtuellt nätverk kan du ange ett undernät eller IP-adressen för den interna belastningsutjämnaren.</span><span class="sxs-lookup"><span data-stu-id="48b97-110">For a virtual network, you can specify a subnet or the IP address of the internal load balancer.</span></span>

## <span data-ttu-id="48b97-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="48b97-111">EXAMPLES</span></span>

### <span data-ttu-id="48b97-112">9.1</span><span class="sxs-lookup"><span data-stu-id="48b97-112">1:</span></span>
```

```

## <span data-ttu-id="48b97-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="48b97-113">PARAMETERS</span></span>

### <span data-ttu-id="48b97-114">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="48b97-114">-InformationAction</span></span>
<span data-ttu-id="48b97-115">Anger hur den här cmdleten svarar på en informations händelse.</span><span class="sxs-lookup"><span data-stu-id="48b97-115">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="48b97-116">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="48b97-116">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="48b97-117">Vidare</span><span class="sxs-lookup"><span data-stu-id="48b97-117">Continue</span></span>
- <span data-ttu-id="48b97-118">Över</span><span class="sxs-lookup"><span data-stu-id="48b97-118">Ignore</span></span>
- <span data-ttu-id="48b97-119">Inquire</span><span class="sxs-lookup"><span data-stu-id="48b97-119">Inquire</span></span>
- <span data-ttu-id="48b97-120">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="48b97-120">SilentlyContinue</span></span>
- <span data-ttu-id="48b97-121">Stanna</span><span class="sxs-lookup"><span data-stu-id="48b97-121">Stop</span></span>
- <span data-ttu-id="48b97-122">Avbryt</span><span class="sxs-lookup"><span data-stu-id="48b97-122">Suspend</span></span>

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

### <span data-ttu-id="48b97-123">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="48b97-123">-InformationVariable</span></span>
<span data-ttu-id="48b97-124">Anger en informations variabel.</span><span class="sxs-lookup"><span data-stu-id="48b97-124">Specifies an information variable.</span></span>

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

### <span data-ttu-id="48b97-125">-InternalLoadBalancerName</span><span class="sxs-lookup"><span data-stu-id="48b97-125">-InternalLoadBalancerName</span></span>
<span data-ttu-id="48b97-126">Anger namnet på intern belastningsutjämnaren som denna cmdlet ändrar.</span><span class="sxs-lookup"><span data-stu-id="48b97-126">Specifies the name of the internal load balancer that this cmdlet modifies.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="48b97-127">-Profil</span><span class="sxs-lookup"><span data-stu-id="48b97-127">-Profile</span></span>
<span data-ttu-id="48b97-128">Anger den Azure-profil från vilken denna cmdlet läser.</span><span class="sxs-lookup"><span data-stu-id="48b97-128">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="48b97-129">Om du inte anger en profil läser denna cmdlet från den lokala standard profilen.</span><span class="sxs-lookup"><span data-stu-id="48b97-129">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="48b97-130">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="48b97-130">-ServiceName</span></span>
<span data-ttu-id="48b97-131">Anger namnet på den tjänst där denna cmdlet ändrar en intern belastningsutjämnare.</span><span class="sxs-lookup"><span data-stu-id="48b97-131">Specifies the name of the service in which this cmdlet modifies an internal load balancer.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="48b97-132">-StaticVNetIPAddress</span><span class="sxs-lookup"><span data-stu-id="48b97-132">-StaticVNetIPAddress</span></span>
<span data-ttu-id="48b97-133">Anger virtuell nätverks-IP-adress för en intern belastnings utjämning.</span><span class="sxs-lookup"><span data-stu-id="48b97-133">Specifies the virtual network IP address for an internal load balancer.</span></span>

```yaml
Type: IPAddress
Parameter Sets: SubnetNameAndIP
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="48b97-134">-SubnetName</span><span class="sxs-lookup"><span data-stu-id="48b97-134">-SubnetName</span></span>
<span data-ttu-id="48b97-135">Anger namnet på under nätet för en intern belastnings utjämning.</span><span class="sxs-lookup"><span data-stu-id="48b97-135">Specifies the name of the subnet for an internal load balancer.</span></span>

```yaml
Type: String
Parameter Sets: SubnetNameOnly, SubnetNameAndIP
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="48b97-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="48b97-136">CommonParameters</span></span>
<span data-ttu-id="48b97-137">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="48b97-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="48b97-138">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="48b97-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="48b97-139">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="48b97-139">INPUTS</span></span>

## <span data-ttu-id="48b97-140">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="48b97-140">OUTPUTS</span></span>

## <span data-ttu-id="48b97-141">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="48b97-141">NOTES</span></span>

## <span data-ttu-id="48b97-142">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="48b97-142">RELATED LINKS</span></span>

[<span data-ttu-id="48b97-143">Add-AzureInternalLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="48b97-143">Add-AzureInternalLoadBalancer</span></span>](./Add-AzureInternalLoadBalancer.md)

[<span data-ttu-id="48b97-144">Get-AzureInternalLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="48b97-144">Get-AzureInternalLoadBalancer</span></span>](./Get-AzureInternalLoadBalancer.md)

[<span data-ttu-id="48b97-145">New-AzureInternalLoadBalancerConfig</span><span class="sxs-lookup"><span data-stu-id="48b97-145">New-AzureInternalLoadBalancerConfig</span></span>](./New-AzureInternalLoadBalancerConfig.md)

[<span data-ttu-id="48b97-146">Remove-AzureInternalLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="48b97-146">Remove-AzureInternalLoadBalancer</span></span>](./Remove-AzureInternalLoadBalancer.md)


