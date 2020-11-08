---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: 125B6865-0022-4F88-BB0F-DDDDB2EDFF00
online version: ''
schema: 2.0.0
ms.openlocfilehash: 2a1f1d033c3e8bae708310d12a1c4cb2b581bf80
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94099030"
---
# <span data-ttu-id="0dc1c-101">Set-AzureNetworkSecurityRule</span><span class="sxs-lookup"><span data-stu-id="0dc1c-101">Set-AzureNetworkSecurityRule</span></span>

## <span data-ttu-id="0dc1c-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="0dc1c-102">SYNOPSIS</span></span>
<span data-ttu-id="0dc1c-103">Lägger till eller ändrar en nätverks säkerhets regel i en nätverks säkerhets grupp.</span><span class="sxs-lookup"><span data-stu-id="0dc1c-103">Adds or modifies a network security rule in a network security group.</span></span>

## <span data-ttu-id="0dc1c-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="0dc1c-104">SYNTAX</span></span>

```
Set-AzureNetworkSecurityRule -Name <String> -Type <String> -Priority <Int32> -Action <String>
 -SourceAddressPrefix <String> -SourcePortRange <String> -DestinationAddressPrefix <String>
 -DestinationPortRange <String> -Protocol <String> -NetworkSecurityGroup <INetworkSecurityGroup>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="0dc1c-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="0dc1c-105">DESCRIPTION</span></span>
<span data-ttu-id="0dc1c-106">Cmdleten **set-AzureNetworkSecurityRule** lägger till eller ändrar en Azure Network Security-regel i en nätverks säkerhets grupp.</span><span class="sxs-lookup"><span data-stu-id="0dc1c-106">The **Set-AzureNetworkSecurityRule** cmdlet adds or modifies an Azure network security rule in a network security group.</span></span>

## <span data-ttu-id="0dc1c-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="0dc1c-107">EXAMPLES</span></span>

## <span data-ttu-id="0dc1c-108">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="0dc1c-108">PARAMETERS</span></span>

### <span data-ttu-id="0dc1c-109">-Åtgärd</span><span class="sxs-lookup"><span data-stu-id="0dc1c-109">-Action</span></span>
<span data-ttu-id="0dc1c-110">Anger åtgärd för en nätverks säkerhets regel.</span><span class="sxs-lookup"><span data-stu-id="0dc1c-110">Specifies the action for a network security rule.</span></span>
<span data-ttu-id="0dc1c-111">Giltiga värden är: Allow och Deny.</span><span class="sxs-lookup"><span data-stu-id="0dc1c-111">Valid values are: Allow and Deny.</span></span>

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

### <span data-ttu-id="0dc1c-112">-DestinationAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="0dc1c-112">-DestinationAddressPrefix</span></span>
<span data-ttu-id="0dc1c-113">Anger CIDR-adressen (Classless Interdomain Routing) för mål-IP-adressintervallet för nätverks säkerhets regeln.</span><span class="sxs-lookup"><span data-stu-id="0dc1c-113">Specifies the Classless Interdomain Routing (CIDR) address of the destination IP range for the network security rule.</span></span>
<span data-ttu-id="0dc1c-114">En asterisk (\*) anger en IP-adress.</span><span class="sxs-lookup"><span data-stu-id="0dc1c-114">An asterisk (\*) specifies any IP address.</span></span>

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

### <span data-ttu-id="0dc1c-115">-DestinationPortRange</span><span class="sxs-lookup"><span data-stu-id="0dc1c-115">-DestinationPortRange</span></span>
<span data-ttu-id="0dc1c-116">Anger ett mål Port intervall för nätverks säkerhets regeln.</span><span class="sxs-lookup"><span data-stu-id="0dc1c-116">Specifies a destination port range for the network security rule.</span></span>
<span data-ttu-id="0dc1c-117">Giltiga värden är heltal från 0 till 65535.</span><span class="sxs-lookup"><span data-stu-id="0dc1c-117">Valid values consist of integers from 0 to 65535.</span></span>
<span data-ttu-id="0dc1c-118">Du kan ange ett enskilt värde eller ange ett område i formatet LowerNumber-HigherNumber.</span><span class="sxs-lookup"><span data-stu-id="0dc1c-118">You can specify an individual value, or specify a range in the format LowerNumber-HigherNumber.</span></span>
<span data-ttu-id="0dc1c-119">Ett bindestreck avgränsar de två värdena.</span><span class="sxs-lookup"><span data-stu-id="0dc1c-119">A hyphen separates the two values.</span></span>

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

### <span data-ttu-id="0dc1c-120">-Namn</span><span class="sxs-lookup"><span data-stu-id="0dc1c-120">-Name</span></span>
<span data-ttu-id="0dc1c-121">Anger namnet på nätverks säkerhets regeln som denna cmdlet lägger till eller ändrar.</span><span class="sxs-lookup"><span data-stu-id="0dc1c-121">Specifies the name for the network security rule that this cmdlet adds or modifies.</span></span>

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

### <span data-ttu-id="0dc1c-122">-NetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="0dc1c-122">-NetworkSecurityGroup</span></span>
<span data-ttu-id="0dc1c-123">Anger den nätverks säkerhets grupp som denna cmdlet ändrar.</span><span class="sxs-lookup"><span data-stu-id="0dc1c-123">Specifies the network security group that this cmdlet modifies.</span></span>
<span data-ttu-id="0dc1c-124">Använd Get-AzureNetworkSecurityGroup cmdlet för att få ett **INetworkSecurityGroup** -objekt.</span><span class="sxs-lookup"><span data-stu-id="0dc1c-124">To obtain an **INetworkSecurityGroup** object, use the Get-AzureNetworkSecurityGroup cmdlet.</span></span>

```yaml
Type: INetworkSecurityGroup
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0dc1c-125">-Prioritet</span><span class="sxs-lookup"><span data-stu-id="0dc1c-125">-Priority</span></span>
<span data-ttu-id="0dc1c-126">Anger prioriteten för nätverks säkerhets regeln.</span><span class="sxs-lookup"><span data-stu-id="0dc1c-126">Specifies the priority for the network security rule.</span></span>
<span data-ttu-id="0dc1c-127">Giltiga värden är: heltal från 100 till 4096.</span><span class="sxs-lookup"><span data-stu-id="0dc1c-127">Valid values are: integers from 100 to 4096.</span></span>

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

### <span data-ttu-id="0dc1c-128">-Profil</span><span class="sxs-lookup"><span data-stu-id="0dc1c-128">-Profile</span></span>
<span data-ttu-id="0dc1c-129">Anger den Azure-profil från vilken denna cmdlet läser.</span><span class="sxs-lookup"><span data-stu-id="0dc1c-129">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="0dc1c-130">Om du inte anger en profil läser denna cmdlet från den lokala standard profilen.</span><span class="sxs-lookup"><span data-stu-id="0dc1c-130">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="0dc1c-131">-Protokoll</span><span class="sxs-lookup"><span data-stu-id="0dc1c-131">-Protocol</span></span>
<span data-ttu-id="0dc1c-132">Anger protokollet för nätverks säkerhets regeln.</span><span class="sxs-lookup"><span data-stu-id="0dc1c-132">Specifies the protocol for the network security rule.</span></span>
<span data-ttu-id="0dc1c-133">Giltiga värden är:</span><span class="sxs-lookup"><span data-stu-id="0dc1c-133">Valid values are:</span></span> 

- <span data-ttu-id="0dc1c-134">TCP</span><span class="sxs-lookup"><span data-stu-id="0dc1c-134">TCP</span></span> 
- <span data-ttu-id="0dc1c-135">UDP</span><span class="sxs-lookup"><span data-stu-id="0dc1c-135">UDP</span></span> 
- *

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

### <span data-ttu-id="0dc1c-136">-SourceAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="0dc1c-136">-SourceAddressPrefix</span></span>
<span data-ttu-id="0dc1c-137">Anger CIDR-adressen för käll-IP-intervallet för nätverks säkerhets regeln.</span><span class="sxs-lookup"><span data-stu-id="0dc1c-137">Specifies the CIDR address of the source IP range for the network security rule.</span></span>
<span data-ttu-id="0dc1c-138">En asterisk (\*) anger en IP-adress.</span><span class="sxs-lookup"><span data-stu-id="0dc1c-138">An asterisk (\*) specifies any IP address.</span></span>

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

### <span data-ttu-id="0dc1c-139">-SourcePortRange</span><span class="sxs-lookup"><span data-stu-id="0dc1c-139">-SourcePortRange</span></span>
<span data-ttu-id="0dc1c-140">Anger ett käll port intervall för nätverks säkerhets regeln.</span><span class="sxs-lookup"><span data-stu-id="0dc1c-140">Specifies a source port range for the network security rule.</span></span>
<span data-ttu-id="0dc1c-141">Giltiga värden är heltal från 0 till 65535.</span><span class="sxs-lookup"><span data-stu-id="0dc1c-141">Valid values consist of integers from 0 to 65535.</span></span>
<span data-ttu-id="0dc1c-142">Du kan ange ett enskilt värde eller ange ett område i formatet LowerNumber-HigherNumber.</span><span class="sxs-lookup"><span data-stu-id="0dc1c-142">You can specify an individual value, or specify a range in the format LowerNumber-HigherNumber.</span></span>
<span data-ttu-id="0dc1c-143">Ett bindestreck avgränsar de två värdena.</span><span class="sxs-lookup"><span data-stu-id="0dc1c-143">A hyphen separates the two values.</span></span>

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

### <span data-ttu-id="0dc1c-144">– Skriv</span><span class="sxs-lookup"><span data-stu-id="0dc1c-144">-Type</span></span>
<span data-ttu-id="0dc1c-145">Anger typen av anslutning för nätverks säkerhets regeln.</span><span class="sxs-lookup"><span data-stu-id="0dc1c-145">Specifies the type of connection for the network security rule.</span></span>
<span data-ttu-id="0dc1c-146">Giltiga värden är: inkommande och utgående.</span><span class="sxs-lookup"><span data-stu-id="0dc1c-146">Valid values are: Inbound and Outbound.</span></span>

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

### <span data-ttu-id="0dc1c-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0dc1c-147">CommonParameters</span></span>
<span data-ttu-id="0dc1c-148">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0dc1c-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0dc1c-149">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0dc1c-149">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0dc1c-150">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="0dc1c-150">INPUTS</span></span>

## <span data-ttu-id="0dc1c-151">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="0dc1c-151">OUTPUTS</span></span>

## <span data-ttu-id="0dc1c-152">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="0dc1c-152">NOTES</span></span>

## <span data-ttu-id="0dc1c-153">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="0dc1c-153">RELATED LINKS</span></span>

[<span data-ttu-id="0dc1c-154">Remove-AzureNetworkSecurityRule</span><span class="sxs-lookup"><span data-stu-id="0dc1c-154">Remove-AzureNetworkSecurityRule</span></span>](./Remove-AzureNetworkSecurityRule.md)


