---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: 6AF7D392-8C8B-4695-95D0-E927093F654A
online version: ''
schema: 2.0.0
ms.openlocfilehash: c21eb1b7bcad200e67659f830bfb3bbef42fe0f8
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94099812"
---
# <span data-ttu-id="f6281-101">Get-AzureNetworkSecurityGroupAssociation</span><span class="sxs-lookup"><span data-stu-id="f6281-101">Get-AzureNetworkSecurityGroupAssociation</span></span>

## <span data-ttu-id="f6281-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="f6281-102">SYNOPSIS</span></span>
<span data-ttu-id="f6281-103">Hämtar en nätverks säkerhets grupp för en virtuell dator, nätverkskort eller PaaS-roll.</span><span class="sxs-lookup"><span data-stu-id="f6281-103">Gets a network security group for a virtual machine, network adapter, or PaaS role.</span></span>

## <span data-ttu-id="f6281-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="f6281-104">SYNTAX</span></span>

### <span data-ttu-id="f6281-105">GetNetworkSecurityGroupAssociationForSubnet</span><span class="sxs-lookup"><span data-stu-id="f6281-105">GetNetworkSecurityGroupAssociationForSubnet</span></span>
```
Get-AzureNetworkSecurityGroupAssociation -VirtualNetworkName <String> -SubnetName <String> [-Detailed]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="f6281-106">GetNetworkSecurityGroupAssociationForIaaSRole</span><span class="sxs-lookup"><span data-stu-id="f6281-106">GetNetworkSecurityGroupAssociationForIaaSRole</span></span>
```
Get-AzureNetworkSecurityGroupAssociation -VM <PersistentVMRoleContext> -ServiceName <String>
 [-NetworkInterfaceName <String>] [-Detailed] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="f6281-107">GetNetworkSecurityGroupAssociationForPaaSRole</span><span class="sxs-lookup"><span data-stu-id="f6281-107">GetNetworkSecurityGroupAssociationForPaaSRole</span></span>
```
Get-AzureNetworkSecurityGroupAssociation [-Slot <String>] -RoleName <String> -ServiceName <String>
 [-NetworkInterfaceName <String>] [-Detailed] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="f6281-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="f6281-108">DESCRIPTION</span></span>
<span data-ttu-id="f6281-109">Cmdleten **Get-AzureNetworkSecurityGroupAssociation** hämtar nätverks säkerhets gruppen för en virtuell dator, nätverkskort eller plattform som tjänst (PaaS).</span><span class="sxs-lookup"><span data-stu-id="f6281-109">The **Get-AzureNetworkSecurityGroupAssociation** cmdlet gets the network security group for a virtual machine, network adapter, or platform as a service (PaaS) role.</span></span>

## <span data-ttu-id="f6281-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="f6281-110">EXAMPLES</span></span>

### <span data-ttu-id="f6281-111">Exempel 1: Hämta nätverks säkerhets gruppen för en virtuell dator</span><span class="sxs-lookup"><span data-stu-id="f6281-111">Example 1: Get the network security group for a virtual machine</span></span>
```
PS C:\> Get-AzureVM -ServiceName "ContosoService" -Name "ContosoVM06" | Get-AzureNetworkSecurityGroupAssociation
```

<span data-ttu-id="f6281-112">Det här kommandot får en virtuell dator med namnet ContosoVM06 för tjänsten som heter ContosoService och skickar det virtuella datorobjektet till den aktuella cmdleten.</span><span class="sxs-lookup"><span data-stu-id="f6281-112">This command gets a virtual machine named ContosoVM06 for the service named ContosoService, and passes that virtual machine object to the current cmdlet.</span></span>
<span data-ttu-id="f6281-113">Den aktuella cmdleten hämtar nätverks säkerhets gruppen som är kopplad till den virtuella datorn.</span><span class="sxs-lookup"><span data-stu-id="f6281-113">The current cmdlet gets the network security group associated to that virtual machine.</span></span>

## <span data-ttu-id="f6281-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="f6281-114">PARAMETERS</span></span>

### <span data-ttu-id="f6281-115">-Detaljerad</span><span class="sxs-lookup"><span data-stu-id="f6281-115">-Detailed</span></span>
<span data-ttu-id="f6281-116">Anger att den här cmdleten returnerar information om nätverks säkerhets gruppen som är kopplad till den virtuella datorn.</span><span class="sxs-lookup"><span data-stu-id="f6281-116">Indicates that this cmdlet returns details of the network security group that is associated to the virtual machine.</span></span>
<span data-ttu-id="f6281-117">Dessa uppgifter inkluderar plats och regler.</span><span class="sxs-lookup"><span data-stu-id="f6281-117">These details include location and rules.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f6281-118">-NetworkInterfaceName</span><span class="sxs-lookup"><span data-stu-id="f6281-118">-NetworkInterfaceName</span></span>
<span data-ttu-id="f6281-119">Anger namnet på det nätverkskort som denna cmdlet får nätverks säkerhets gruppen för.</span><span class="sxs-lookup"><span data-stu-id="f6281-119">Specifies the name of the network adapter for which this cmdlet gets the network security group.</span></span>

```yaml
Type: String
Parameter Sets: GetNetworkSecurityGroupAssociationForIaaSRole, GetNetworkSecurityGroupAssociationForPaaSRole
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f6281-120">-Profil</span><span class="sxs-lookup"><span data-stu-id="f6281-120">-Profile</span></span>
<span data-ttu-id="f6281-121">Anger den Azure-profil från vilken denna cmdlet läser.</span><span class="sxs-lookup"><span data-stu-id="f6281-121">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="f6281-122">Om du inte anger en profil läser denna cmdlet från den lokala standard profilen.</span><span class="sxs-lookup"><span data-stu-id="f6281-122">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="f6281-123">-RoleName</span><span class="sxs-lookup"><span data-stu-id="f6281-123">-RoleName</span></span>
<span data-ttu-id="f6281-124">Anger namnet på en PaaS-roll för vilken denna cmdlet får nätverks säkerhets gruppen.</span><span class="sxs-lookup"><span data-stu-id="f6281-124">Specifies the name of a PaaS role for which this cmdlet gets the network security group.</span></span>

```yaml
Type: String
Parameter Sets: GetNetworkSecurityGroupAssociationForPaaSRole
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f6281-125">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="f6281-125">-ServiceName</span></span>
<span data-ttu-id="f6281-126">Anger namnet på en moln tjänst.</span><span class="sxs-lookup"><span data-stu-id="f6281-126">Specifies the name of a cloud service.</span></span>
<span data-ttu-id="f6281-127">PaaS-rollen tillhör den tjänst som anges av den här parametern.</span><span class="sxs-lookup"><span data-stu-id="f6281-127">The PaaS role belongs to the service that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: GetNetworkSecurityGroupAssociationForIaaSRole, GetNetworkSecurityGroupAssociationForPaaSRole
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f6281-128">-Plats</span><span class="sxs-lookup"><span data-stu-id="f6281-128">-Slot</span></span>
<span data-ttu-id="f6281-129">Anger en PaaS-kortplats.</span><span class="sxs-lookup"><span data-stu-id="f6281-129">Specifies a PaaS slot.</span></span>
<span data-ttu-id="f6281-130">PaaS-rollen för vilken denna cmdlet får nätverks säkerhets gruppen är den plats som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="f6281-130">The PaaS role for which this cmdlet gets the network security group has the slot that this parameter specifies.</span></span>
<span data-ttu-id="f6281-131">Giltiga värden är:</span><span class="sxs-lookup"><span data-stu-id="f6281-131">Valid values are:</span></span> 

- <span data-ttu-id="f6281-132">Produktionsoperationsföljden</span><span class="sxs-lookup"><span data-stu-id="f6281-132">Production</span></span>
- <span data-ttu-id="f6281-133">Lagring</span><span class="sxs-lookup"><span data-stu-id="f6281-133">Staging</span></span> 

<span data-ttu-id="f6281-134">Standardvärdet är produktion.</span><span class="sxs-lookup"><span data-stu-id="f6281-134">The default value is Production.</span></span>

```yaml
Type: String
Parameter Sets: GetNetworkSecurityGroupAssociationForPaaSRole
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f6281-135">-SubnetName</span><span class="sxs-lookup"><span data-stu-id="f6281-135">-SubnetName</span></span>
<span data-ttu-id="f6281-136">Anger namnet på ett undernät som denna cmdlet får nätverks säkerhets gruppen för.</span><span class="sxs-lookup"><span data-stu-id="f6281-136">Specifies the name of a subnet for which this cmdlet gets the network security group.</span></span>

```yaml
Type: String
Parameter Sets: GetNetworkSecurityGroupAssociationForSubnet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f6281-137">-VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="f6281-137">-VirtualNetworkName</span></span>
<span data-ttu-id="f6281-138">Anger namnet på ett virtuellt nätverk som innehåller det undernät som denna cmdlet får nätverks säkerhets gruppen för.</span><span class="sxs-lookup"><span data-stu-id="f6281-138">Specifies the name of a virtual network that contains the subnet for which this cmdlet gets the network security group.</span></span>

```yaml
Type: String
Parameter Sets: GetNetworkSecurityGroupAssociationForSubnet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f6281-139">-VM</span><span class="sxs-lookup"><span data-stu-id="f6281-139">-VM</span></span>
<span data-ttu-id="f6281-140">Anger den virtuella dator där denna cmdlet ska använda nätverks säkerhets gruppen.</span><span class="sxs-lookup"><span data-stu-id="f6281-140">Specifies the virtual machine to which this cmdlet applies the network security group.</span></span>

```yaml
Type: PersistentVMRoleContext
Parameter Sets: GetNetworkSecurityGroupAssociationForIaaSRole
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f6281-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f6281-141">CommonParameters</span></span>
<span data-ttu-id="f6281-142">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f6281-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f6281-143">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f6281-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f6281-144">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="f6281-144">INPUTS</span></span>

## <span data-ttu-id="f6281-145">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="f6281-145">OUTPUTS</span></span>

### <span data-ttu-id="f6281-146">Microsoft. WindowsAzure. kommandon. ServiceManagement. Network. NetworkSecurityGroup. Model. INetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="f6281-146">Microsoft.WindowsAzure.Commands.ServiceManagement.Network.NetworkSecurityGroup.Model.INetworkSecurityGroup</span></span>

## <span data-ttu-id="f6281-147">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="f6281-147">NOTES</span></span>

## <span data-ttu-id="f6281-148">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="f6281-148">RELATED LINKS</span></span>

[<span data-ttu-id="f6281-149">Remove-AzureNetworkSecurityGroupAssociation</span><span class="sxs-lookup"><span data-stu-id="f6281-149">Remove-AzureNetworkSecurityGroupAssociation</span></span>](./Remove-AzureNetworkSecurityGroupAssociation.md)

[<span data-ttu-id="f6281-150">Set-AzureNetworkSecurityGroupAssociation</span><span class="sxs-lookup"><span data-stu-id="f6281-150">Set-AzureNetworkSecurityGroupAssociation</span></span>](./Set-AzureNetworkSecurityGroupAssociation.md)


