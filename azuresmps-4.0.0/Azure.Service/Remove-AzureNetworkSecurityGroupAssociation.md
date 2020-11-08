---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: 3E3E0237-8E2D-4B3A-AD0C-2121DDE1AAB6
online version: ''
schema: 2.0.0
ms.openlocfilehash: 28259b97f382092f5e6293048c040688011cfe92
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94099382"
---
# <span data-ttu-id="5810b-101">Remove-AzureNetworkSecurityGroupAssociation</span><span class="sxs-lookup"><span data-stu-id="5810b-101">Remove-AzureNetworkSecurityGroupAssociation</span></span>

## <span data-ttu-id="5810b-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="5810b-102">SYNOPSIS</span></span>
<span data-ttu-id="5810b-103">Tar bort en nätverks säkerhets grupp.</span><span class="sxs-lookup"><span data-stu-id="5810b-103">Removes a network security group.</span></span>

## <span data-ttu-id="5810b-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="5810b-104">SYNTAX</span></span>

### <span data-ttu-id="5810b-105">RemoveNetworkSecurityGroupAssociationFromSubnet</span><span class="sxs-lookup"><span data-stu-id="5810b-105">RemoveNetworkSecurityGroupAssociationFromSubnet</span></span>
```
Remove-AzureNetworkSecurityGroupAssociation -Name <String> -VirtualNetworkName <String> -SubnetName <String>
 [-Force] [-PassThru] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="5810b-106">RemoveNetworkSecurityGroupAssociationFromIaaSRole</span><span class="sxs-lookup"><span data-stu-id="5810b-106">RemoveNetworkSecurityGroupAssociationFromIaaSRole</span></span>
```
Remove-AzureNetworkSecurityGroupAssociation -Name <String> -VM <PersistentVMRoleContext> -ServiceName <String>
 [-NetworkInterfaceName <String>] [-Force] [-PassThru] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="5810b-107">RemoveNetworkSecurityGroupAssociationFromPaaSRole</span><span class="sxs-lookup"><span data-stu-id="5810b-107">RemoveNetworkSecurityGroupAssociationFromPaaSRole</span></span>
```
Remove-AzureNetworkSecurityGroupAssociation -Name <String> [-Slot <String>] -RoleName <String>
 -ServiceName <String> [-NetworkInterfaceName <String>] [-Force] [-PassThru] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="5810b-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="5810b-108">DESCRIPTION</span></span>
<span data-ttu-id="5810b-109">Cmdleten **Remove-AzureNetworkSecurityGroupAssociation** tar bort en nätverks säkerhets grupp från en virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="5810b-109">The **Remove-AzureNetworkSecurityGroupAssociation** cmdlet removes a network security group from a virtual machine.</span></span>

## <span data-ttu-id="5810b-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="5810b-110">EXAMPLES</span></span>

### <span data-ttu-id="5810b-111">Exempel 1: ta bort en virtuell dator till en nätverks säkerhets grupp</span><span class="sxs-lookup"><span data-stu-id="5810b-111">Example 1: Remove a virtual machine to a network security group</span></span>
```
PS C:\> Get-AzureVM -ServiceName "ContosoService" -Name "ContosoVM06" | Remove-AzureNetworkSecurityGroupAssociation -Name "ContosoNetworkSecurityGroup"
```

<span data-ttu-id="5810b-112">Det här kommandot får en virtuell dator med namnet ContosoVM06 för tjänsten som heter ContosoService och skickar det virtuella datorobjektet till den aktuella cmdleten.</span><span class="sxs-lookup"><span data-stu-id="5810b-112">This command gets a virtual machine named ContosoVM06 for the service named ContosoService, and passes that virtual machine object to the current cmdlet.</span></span>
<span data-ttu-id="5810b-113">Den aktuella cmdleten tar bort nätverks säkerhets gruppen ' ContosoNetworkSecurityGroup ' från den virtuella datorn.</span><span class="sxs-lookup"><span data-stu-id="5810b-113">The current cmdlet removes the network security group named ContosoNetworkSecurityGroup from that virtual machine.</span></span>

## <span data-ttu-id="5810b-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="5810b-114">PARAMETERS</span></span>

### <span data-ttu-id="5810b-115">-Force</span><span class="sxs-lookup"><span data-stu-id="5810b-115">-Force</span></span>
<span data-ttu-id="5810b-116">Tvingar kommandot att köras utan att fråga efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="5810b-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="5810b-117">-Namn</span><span class="sxs-lookup"><span data-stu-id="5810b-117">-Name</span></span>
<span data-ttu-id="5810b-118">Anger namnet på den nätverks säkerhets grupp som denna cmdlet tar bort.</span><span class="sxs-lookup"><span data-stu-id="5810b-118">Specifies the name of the network security group that this cmdlet removes.</span></span>

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

### <span data-ttu-id="5810b-119">-NetworkInterfaceName</span><span class="sxs-lookup"><span data-stu-id="5810b-119">-NetworkInterfaceName</span></span>
<span data-ttu-id="5810b-120">Anger namnet på det nätverkskort som den här cmdleten tar bort nätverks säkerhets gruppen från.</span><span class="sxs-lookup"><span data-stu-id="5810b-120">Specifies the name of the network adapter from which this cmdlet removes the network security group.</span></span>

```yaml
Type: String
Parameter Sets: RemoveNetworkSecurityGroupAssociationFromIaaSRole, RemoveNetworkSecurityGroupAssociationFromPaaSRole
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5810b-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="5810b-121">-PassThru</span></span>
<span data-ttu-id="5810b-122">Returnerar ett objekt som representerar det objekt som du arbetar med.</span><span class="sxs-lookup"><span data-stu-id="5810b-122">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="5810b-123">Denna cmdlet genererar som standard inga utdata.</span><span class="sxs-lookup"><span data-stu-id="5810b-123">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="5810b-124">-Profil</span><span class="sxs-lookup"><span data-stu-id="5810b-124">-Profile</span></span>
<span data-ttu-id="5810b-125">Anger den Azure-profil från vilken denna cmdlet läser.</span><span class="sxs-lookup"><span data-stu-id="5810b-125">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="5810b-126">Om du inte anger en profil läser denna cmdlet från den lokala standard profilen.</span><span class="sxs-lookup"><span data-stu-id="5810b-126">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="5810b-127">-RoleName</span><span class="sxs-lookup"><span data-stu-id="5810b-127">-RoleName</span></span>
<span data-ttu-id="5810b-128">Anger namnet på en PaaS-roll från vilken denna cmdlet tar bort nätverks säkerhets gruppen.</span><span class="sxs-lookup"><span data-stu-id="5810b-128">Specifies the name of a PaaS role from which this cmdlet removes the network security group.</span></span>

```yaml
Type: String
Parameter Sets: RemoveNetworkSecurityGroupAssociationFromPaaSRole
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5810b-129">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="5810b-129">-ServiceName</span></span>
<span data-ttu-id="5810b-130">Anger namnet på en moln tjänst.</span><span class="sxs-lookup"><span data-stu-id="5810b-130">Specifies the name of a cloud service.</span></span>
<span data-ttu-id="5810b-131">PaaS-rollen från vilken denna cmdlet tar bort en nätverks säkerhets grupp tillhör den tjänst som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="5810b-131">The PaaS role from which this cmdlet removes a network security group belongs to the service that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: RemoveNetworkSecurityGroupAssociationFromIaaSRole, RemoveNetworkSecurityGroupAssociationFromPaaSRole
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5810b-132">-Plats</span><span class="sxs-lookup"><span data-stu-id="5810b-132">-Slot</span></span>
<span data-ttu-id="5810b-133">Anger en PaaS-kortplats.</span><span class="sxs-lookup"><span data-stu-id="5810b-133">Specifies a PaaS slot.</span></span>
<span data-ttu-id="5810b-134">PaaS-rollen från vilken denna cmdlet tar bort en nätverks säkerhets grupp är den plats som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="5810b-134">The PaaS role from which this cmdlet removes a network security group has the slot that this parameter specifies.</span></span>
<span data-ttu-id="5810b-135">Giltiga värden är:</span><span class="sxs-lookup"><span data-stu-id="5810b-135">Valid values are:</span></span>

- <span data-ttu-id="5810b-136">Produktionsoperationsföljden</span><span class="sxs-lookup"><span data-stu-id="5810b-136">Production</span></span>
- <span data-ttu-id="5810b-137">Lagring</span><span class="sxs-lookup"><span data-stu-id="5810b-137">Staging</span></span>

<span data-ttu-id="5810b-138">Standardvärdet är produktion.</span><span class="sxs-lookup"><span data-stu-id="5810b-138">The default value is Production.</span></span>

```yaml
Type: String
Parameter Sets: RemoveNetworkSecurityGroupAssociationFromPaaSRole
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5810b-139">-SubnetName</span><span class="sxs-lookup"><span data-stu-id="5810b-139">-SubnetName</span></span>
<span data-ttu-id="5810b-140">Anger namnet på ett undernät som denna cmdlet tar bort nätverks säkerhets gruppen från.</span><span class="sxs-lookup"><span data-stu-id="5810b-140">Specifies the name of a subnet from which this cmdlet removes the network security group.</span></span>

```yaml
Type: String
Parameter Sets: RemoveNetworkSecurityGroupAssociationFromSubnet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5810b-141">-VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="5810b-141">-VirtualNetworkName</span></span>
<span data-ttu-id="5810b-142">Anger namnet på ett virtuellt nätverk som innehåller det undernät som denna cmdlet tar bort nätverks säkerhets gruppen från.</span><span class="sxs-lookup"><span data-stu-id="5810b-142">Specifies the name of a virtual network that contains the subnet from which this cmdlet removes the network security group.</span></span>

```yaml
Type: String
Parameter Sets: RemoveNetworkSecurityGroupAssociationFromSubnet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5810b-143">-VM</span><span class="sxs-lookup"><span data-stu-id="5810b-143">-VM</span></span>
<span data-ttu-id="5810b-144">Anger den virtuella dator där denna cmdlet ska använda nätverks säkerhets gruppen.</span><span class="sxs-lookup"><span data-stu-id="5810b-144">Specifies the virtual machine to which this cmdlet applies the network security group.</span></span>

```yaml
Type: PersistentVMRoleContext
Parameter Sets: RemoveNetworkSecurityGroupAssociationFromIaaSRole
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5810b-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5810b-145">CommonParameters</span></span>
<span data-ttu-id="5810b-146">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5810b-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5810b-147">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5810b-147">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5810b-148">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="5810b-148">INPUTS</span></span>

## <span data-ttu-id="5810b-149">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="5810b-149">OUTPUTS</span></span>

### <span data-ttu-id="5810b-150">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="5810b-150">System.Boolean</span></span>

## <span data-ttu-id="5810b-151">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="5810b-151">NOTES</span></span>

## <span data-ttu-id="5810b-152">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="5810b-152">RELATED LINKS</span></span>

[<span data-ttu-id="5810b-153">Get-AzureNetworkSecurityGroupAssociation</span><span class="sxs-lookup"><span data-stu-id="5810b-153">Get-AzureNetworkSecurityGroupAssociation</span></span>](./Get-AzureNetworkSecurityGroupAssociation.md)

[<span data-ttu-id="5810b-154">Set-AzureNetworkSecurityGroupAssociation</span><span class="sxs-lookup"><span data-stu-id="5810b-154">Set-AzureNetworkSecurityGroupAssociation</span></span>](./Set-AzureNetworkSecurityGroupAssociation.md)
