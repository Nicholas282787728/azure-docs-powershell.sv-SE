---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 8C01AFE1-65E7-4C5F-B3ED-8FCD9C4D20FC
online version: ''
schema: 2.0.0
ms.openlocfilehash: a42ffe7ded2eb47638dd961ae79b10dd21cf08ad
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94099144"
---
# <span data-ttu-id="79f49-101">New-AzureInternalLoadBalancerConfig</span><span class="sxs-lookup"><span data-stu-id="79f49-101">New-AzureInternalLoadBalancerConfig</span></span>

## <span data-ttu-id="79f49-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="79f49-102">SYNOPSIS</span></span>
<span data-ttu-id="79f49-103">Skapar en intern belastnings Utjämnings konfiguration.</span><span class="sxs-lookup"><span data-stu-id="79f49-103">Creates an internal load balancer configuration.</span></span>

## <span data-ttu-id="79f49-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="79f49-104">SYNTAX</span></span>

### <span data-ttu-id="79f49-105">ServiceAndSlot (standard)</span><span class="sxs-lookup"><span data-stu-id="79f49-105">ServiceAndSlot (Default)</span></span>
```
New-AzureInternalLoadBalancerConfig [-InternalLoadBalancerName] <String> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="79f49-106">SubnetNameOnly</span><span class="sxs-lookup"><span data-stu-id="79f49-106">SubnetNameOnly</span></span>
```
New-AzureInternalLoadBalancerConfig [-InternalLoadBalancerName] <String> [-SubnetName] <String>
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

### <span data-ttu-id="79f49-107">SubnetNameAndIP</span><span class="sxs-lookup"><span data-stu-id="79f49-107">SubnetNameAndIP</span></span>
```
New-AzureInternalLoadBalancerConfig [-InternalLoadBalancerName] <String> [-SubnetName] <String>
 [-StaticVNetIPAddress] <IPAddress> [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="79f49-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="79f49-108">DESCRIPTION</span></span>
<span data-ttu-id="79f49-109">Cmdleten **New-AzureInternalLoadBalancerConfig** skapar ett **InternalLoadBalancerConfig** -objekt.</span><span class="sxs-lookup"><span data-stu-id="79f49-109">The **New-AzureInternalLoadBalancerConfig** cmdlet creates an **InternalLoadBalancerConfig** object.</span></span>
<span data-ttu-id="79f49-110">Du kan använda en intern belastnings Utjämnings konfiguration när du skapar en distribution av Azure Virtual Machine.</span><span class="sxs-lookup"><span data-stu-id="79f49-110">You can use an internal load balancer configuration when you create an Azure virtual machine deployment.</span></span>

## <span data-ttu-id="79f49-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="79f49-111">EXAMPLES</span></span>

### <span data-ttu-id="79f49-112">Exempel 1: skapa en intern belastnings Utjämnings konfiguration</span><span class="sxs-lookup"><span data-stu-id="79f49-112">Example 1: Create an internal load balancer configuration</span></span>
```
PS C:\> $IlbConfig = New-AzureInternalLoadBalancerConfig -InternalLoadBalancerName "Contoso" -SubnetName "FrontEndSubnet"
```

<span data-ttu-id="79f49-113">Det här kommandot skapar en intern belastningsutjämnare för under nätet som heter FrontEndSubnet.</span><span class="sxs-lookup"><span data-stu-id="79f49-113">This command creates an internal load balancer configuration for the subnet named FrontEndSubnet.</span></span>
<span data-ttu-id="79f49-114">Kommandot lagrar konfigurationen i $IlbConfig variabeln som du kan använda för en virtuell dator distribution.</span><span class="sxs-lookup"><span data-stu-id="79f49-114">The command stores the configuration in the $IlbConfig variable for you to use for a virtual machine deployment.</span></span>

## <span data-ttu-id="79f49-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="79f49-115">PARAMETERS</span></span>

### <span data-ttu-id="79f49-116">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="79f49-116">-InformationAction</span></span>
<span data-ttu-id="79f49-117">Anger hur den här cmdleten svarar på en informations händelse.</span><span class="sxs-lookup"><span data-stu-id="79f49-117">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="79f49-118">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="79f49-118">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="79f49-119">Vidare</span><span class="sxs-lookup"><span data-stu-id="79f49-119">Continue</span></span>
- <span data-ttu-id="79f49-120">Över</span><span class="sxs-lookup"><span data-stu-id="79f49-120">Ignore</span></span>
- <span data-ttu-id="79f49-121">Inquire</span><span class="sxs-lookup"><span data-stu-id="79f49-121">Inquire</span></span>
- <span data-ttu-id="79f49-122">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="79f49-122">SilentlyContinue</span></span>
- <span data-ttu-id="79f49-123">Stanna</span><span class="sxs-lookup"><span data-stu-id="79f49-123">Stop</span></span>
- <span data-ttu-id="79f49-124">Avbryt</span><span class="sxs-lookup"><span data-stu-id="79f49-124">Suspend</span></span>

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

### <span data-ttu-id="79f49-125">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="79f49-125">-InformationVariable</span></span>
<span data-ttu-id="79f49-126">Anger en informations variabel.</span><span class="sxs-lookup"><span data-stu-id="79f49-126">Specifies an information variable.</span></span>

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

### <span data-ttu-id="79f49-127">-InternalLoadBalancerName</span><span class="sxs-lookup"><span data-stu-id="79f49-127">-InternalLoadBalancerName</span></span>
<span data-ttu-id="79f49-128">Anger namnet på intern belastningsutjämnaren som denna cmdlet inkluderar i konfigurationen.</span><span class="sxs-lookup"><span data-stu-id="79f49-128">Specifies the name of the internal load balancer that this cmdlet includes in the configuration.</span></span>

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

### <span data-ttu-id="79f49-129">-Profil</span><span class="sxs-lookup"><span data-stu-id="79f49-129">-Profile</span></span>
<span data-ttu-id="79f49-130">Anger den Azure-profil från vilken denna cmdlet läser.</span><span class="sxs-lookup"><span data-stu-id="79f49-130">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="79f49-131">Om du inte anger en profil läser denna cmdlet från den lokala standard profilen.</span><span class="sxs-lookup"><span data-stu-id="79f49-131">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="79f49-132">-StaticVNetIPAddress</span><span class="sxs-lookup"><span data-stu-id="79f49-132">-StaticVNetIPAddress</span></span>
<span data-ttu-id="79f49-133">Anger den virtuella nätverks-IP-adressen för en intern belastningsutjämnare som denna cmdlet inkluderar i konfigurationen.</span><span class="sxs-lookup"><span data-stu-id="79f49-133">Specifies the virtual network IP address for an internal load balancer that this cmdlet includes in the configuration.</span></span>

```yaml
Type: IPAddress
Parameter Sets: SubnetNameAndIP
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="79f49-134">-SubnetName</span><span class="sxs-lookup"><span data-stu-id="79f49-134">-SubnetName</span></span>
<span data-ttu-id="79f49-135">Anger namnet på under nätet för en intern belastnings utjämning.</span><span class="sxs-lookup"><span data-stu-id="79f49-135">Specifies the name of the subnet for an internal load balancer.</span></span>

```yaml
Type: String
Parameter Sets: SubnetNameOnly, SubnetNameAndIP
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="79f49-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="79f49-136">CommonParameters</span></span>
<span data-ttu-id="79f49-137">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="79f49-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="79f49-138">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="79f49-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="79f49-139">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="79f49-139">INPUTS</span></span>

## <span data-ttu-id="79f49-140">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="79f49-140">OUTPUTS</span></span>

### <span data-ttu-id="79f49-141">Microsoft. WindowsAzure. kommandon. ServiceManagement. Model. InternalLoadBalancerConfig</span><span class="sxs-lookup"><span data-stu-id="79f49-141">Microsoft.WindowsAzure.Commands.ServiceManagement.Model.InternalLoadBalancerConfig</span></span>

## <span data-ttu-id="79f49-142">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="79f49-142">NOTES</span></span>

## <span data-ttu-id="79f49-143">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="79f49-143">RELATED LINKS</span></span>

[<span data-ttu-id="79f49-144">Add-AzureInternalLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="79f49-144">Add-AzureInternalLoadBalancer</span></span>](./Add-AzureInternalLoadBalancer.md)

[<span data-ttu-id="79f49-145">Get-AzureInternalLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="79f49-145">Get-AzureInternalLoadBalancer</span></span>](./Get-AzureInternalLoadBalancer.md)

[<span data-ttu-id="79f49-146">Remove-AzureInternalLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="79f49-146">Remove-AzureInternalLoadBalancer</span></span>](./Remove-AzureInternalLoadBalancer.md)

[<span data-ttu-id="79f49-147">Set-AzureInternalLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="79f49-147">Set-AzureInternalLoadBalancer</span></span>](./Set-AzureInternalLoadBalancer.md)


