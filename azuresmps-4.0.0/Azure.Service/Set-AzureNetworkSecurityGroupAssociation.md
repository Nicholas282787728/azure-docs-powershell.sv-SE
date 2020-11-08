---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: 64639A35-0573-48C8-AB21-19FEB09537BA
online version: ''
schema: 2.0.0
ms.openlocfilehash: b1b251a5fef3ad91f830e18714796421d2abca7b
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94093484"
---
# <span data-ttu-id="7ee5e-101">Set-AzureNetworkSecurityGroupAssociation</span><span class="sxs-lookup"><span data-stu-id="7ee5e-101">Set-AzureNetworkSecurityGroupAssociation</span></span>

## <span data-ttu-id="7ee5e-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="7ee5e-102">SYNOPSIS</span></span>
<span data-ttu-id="7ee5e-103">Associerar en nätverks säkerhets grupp till en virtuell dator, PaaS-roll eller nätverkskort.</span><span class="sxs-lookup"><span data-stu-id="7ee5e-103">Associates a network security group to a virtual machine, PaaS role, or network adapter.</span></span>

## <span data-ttu-id="7ee5e-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="7ee5e-104">SYNTAX</span></span>

### <span data-ttu-id="7ee5e-105">AddNetworkSecurityGroupAssociationToSubnet</span><span class="sxs-lookup"><span data-stu-id="7ee5e-105">AddNetworkSecurityGroupAssociationToSubnet</span></span>
```
Set-AzureNetworkSecurityGroupAssociation -Name <String> [-Force] [-PassThru] -VirtualNetworkName <String>
 -SubnetName <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="7ee5e-106">AddNetworkSecurityGroupAssociationToIaaSRole</span><span class="sxs-lookup"><span data-stu-id="7ee5e-106">AddNetworkSecurityGroupAssociationToIaaSRole</span></span>
```
Set-AzureNetworkSecurityGroupAssociation -Name <String> [-Force] [-PassThru] -VM <PersistentVMRoleContext>
 -ServiceName <String> [-NetworkInterfaceName <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="7ee5e-107">AddNetworkSecurityGroupAssociationToPaaSRole</span><span class="sxs-lookup"><span data-stu-id="7ee5e-107">AddNetworkSecurityGroupAssociationToPaaSRole</span></span>
```
Set-AzureNetworkSecurityGroupAssociation -Name <String> [-Force] [-PassThru] [-Slot <String>]
 -RoleName <String> -ServiceName <String> [-NetworkInterfaceName <String>] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="7ee5e-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="7ee5e-108">DESCRIPTION</span></span>
<span data-ttu-id="7ee5e-109">Cmdleten **set-AzureNetworkSecurityGroupAssociation** associerar en nätverks säkerhets grupp till en virtuell dator, plattform som tjänst (PaaS) eller nätverkskort.</span><span class="sxs-lookup"><span data-stu-id="7ee5e-109">The **Set-AzureNetworkSecurityGroupAssociation** cmdlet associates a network security group to a virtual machine, platform as a service (PaaS) role, or network adapter.</span></span>

## <span data-ttu-id="7ee5e-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="7ee5e-110">EXAMPLES</span></span>

### <span data-ttu-id="7ee5e-111">Exempel 1: tilldela en virtuell dator till en nätverks säkerhets grupp</span><span class="sxs-lookup"><span data-stu-id="7ee5e-111">Example 1: Assign a virtual machine to a network security group</span></span>
```
PS C:\> Get-AzureVM -ServiceName "ContosoService" -Name "ContosoVM06" | Set-AzureNetworkSecurityGroupAssociation -Name "ContosoNetworkSecurityGroup"
```

<span data-ttu-id="7ee5e-112">Det här kommandot får en virtuell dator med namnet ContosoVM06 för tjänsten som heter ContosoService och skickar det virtuella datorobjektet till den aktuella cmdleten.</span><span class="sxs-lookup"><span data-stu-id="7ee5e-112">This command gets a virtual machine named ContosoVM06 for the service named ContosoService, and passes that virtual machine object to the current cmdlet.</span></span>
<span data-ttu-id="7ee5e-113">Den aktuella cmdleten tilldelar nätverks säkerhets gruppen som heter ContosoNetworkSecurityGroup till den virtuella datorn.</span><span class="sxs-lookup"><span data-stu-id="7ee5e-113">The current cmdlet assigns the network security group named ContosoNetworkSecurityGroup to that virtual machine.</span></span>

## <span data-ttu-id="7ee5e-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="7ee5e-114">PARAMETERS</span></span>

### <span data-ttu-id="7ee5e-115">-Force</span><span class="sxs-lookup"><span data-stu-id="7ee5e-115">-Force</span></span>
<span data-ttu-id="7ee5e-116">Tvingar kommandot att köras utan att fråga efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="7ee5e-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="7ee5e-117">-Namn</span><span class="sxs-lookup"><span data-stu-id="7ee5e-117">-Name</span></span>
<span data-ttu-id="7ee5e-118">Anger namnet på den nätverks säkerhets grupp som cmdleten ställer in.</span><span class="sxs-lookup"><span data-stu-id="7ee5e-118">Specifies the name of the network security group that this cmdlet sets.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7ee5e-119">-NetworkInterfaceName</span><span class="sxs-lookup"><span data-stu-id="7ee5e-119">-NetworkInterfaceName</span></span>
<span data-ttu-id="7ee5e-120">Anger namnet på det nätverkskort där denna cmdlet ska använda nätverks säkerhets gruppen.</span><span class="sxs-lookup"><span data-stu-id="7ee5e-120">Specifies the name of the network adapter to which this cmdlet applies the network security group.</span></span>

```yaml
Type: String
Parameter Sets: AddNetworkSecurityGroupAssociationToIaaSRole, AddNetworkSecurityGroupAssociationToPaaSRole
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7ee5e-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="7ee5e-121">-PassThru</span></span>
<span data-ttu-id="7ee5e-122">Returnerar ett objekt som representerar det objekt som du arbetar med.</span><span class="sxs-lookup"><span data-stu-id="7ee5e-122">Returns an object representing the item with which you are working.</span></span> <span data-ttu-id="7ee5e-123">Denna cmdlet genererar som standard inga utdata.</span><span class="sxs-lookup"><span data-stu-id="7ee5e-123">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="7ee5e-124">-Profil</span><span class="sxs-lookup"><span data-stu-id="7ee5e-124">-Profile</span></span>
<span data-ttu-id="7ee5e-125">Anger den Azure-profil från vilken denna cmdlet läser.</span><span class="sxs-lookup"><span data-stu-id="7ee5e-125">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="7ee5e-126">Om du inte anger en profil läser denna cmdlet från den lokala standard profilen.</span><span class="sxs-lookup"><span data-stu-id="7ee5e-126">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="7ee5e-127">-RoleName</span><span class="sxs-lookup"><span data-stu-id="7ee5e-127">-RoleName</span></span>
<span data-ttu-id="7ee5e-128">Anger namnet på en PaaS-roll som denna cmdlet ska använda nätverks säkerhets gruppen för.</span><span class="sxs-lookup"><span data-stu-id="7ee5e-128">Specifies the name of a PaaS role to which this cmdlet applies the network security group.</span></span>

```yaml
Type: String
Parameter Sets: AddNetworkSecurityGroupAssociationToPaaSRole
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7ee5e-129">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="7ee5e-129">-ServiceName</span></span>
<span data-ttu-id="7ee5e-130">Anger namnet på en moln tjänst.</span><span class="sxs-lookup"><span data-stu-id="7ee5e-130">Specifies the name of a cloud service.</span></span>
<span data-ttu-id="7ee5e-131">PaaS-rollen tillhör den tjänst som anges av den här parametern.</span><span class="sxs-lookup"><span data-stu-id="7ee5e-131">The PaaS role belongs to the service that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: AddNetworkSecurityGroupAssociationToIaaSRole, AddNetworkSecurityGroupAssociationToPaaSRole
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7ee5e-132">-Plats</span><span class="sxs-lookup"><span data-stu-id="7ee5e-132">-Slot</span></span>
<span data-ttu-id="7ee5e-133">Anger en PaaS-kortplats.</span><span class="sxs-lookup"><span data-stu-id="7ee5e-133">Specifies a PaaS slot.</span></span>
<span data-ttu-id="7ee5e-134">PaaS-rollen för vilken den här cmdleten ställer in nätverks säkerhets gruppen är den plats som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="7ee5e-134">The PaaS role for which this cmdlet sets the network security group has the slot that this parameter specifies.</span></span>
<span data-ttu-id="7ee5e-135">Giltiga värden är:</span><span class="sxs-lookup"><span data-stu-id="7ee5e-135">Valid values are:</span></span> 

- <span data-ttu-id="7ee5e-136">Produktionsoperationsföljden</span><span class="sxs-lookup"><span data-stu-id="7ee5e-136">Production</span></span>
- <span data-ttu-id="7ee5e-137">Lagring</span><span class="sxs-lookup"><span data-stu-id="7ee5e-137">Staging</span></span> 

<span data-ttu-id="7ee5e-138">Standardvärdet är produktion.</span><span class="sxs-lookup"><span data-stu-id="7ee5e-138">The default value is Production.</span></span>

```yaml
Type: String
Parameter Sets: AddNetworkSecurityGroupAssociationToPaaSRole
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7ee5e-139">-SubnetName</span><span class="sxs-lookup"><span data-stu-id="7ee5e-139">-SubnetName</span></span>
<span data-ttu-id="7ee5e-140">Anger namnet på ett undernät som denna cmdlet associerar nätverks säkerhets gruppen med.</span><span class="sxs-lookup"><span data-stu-id="7ee5e-140">Specifies the name of a subnet to which this cmdlet associates the network security group.</span></span>

```yaml
Type: String
Parameter Sets: AddNetworkSecurityGroupAssociationToSubnet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7ee5e-141">-VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="7ee5e-141">-VirtualNetworkName</span></span>
<span data-ttu-id="7ee5e-142">Anger namnet på ett virtuellt nätverk som innehåller det undernät som denna cmdlet associerar nätverks säkerhets gruppen med.</span><span class="sxs-lookup"><span data-stu-id="7ee5e-142">Specifies the name of a virtual network that contains the subnet to which this cmdlet associates the network security group.</span></span>

```yaml
Type: String
Parameter Sets: AddNetworkSecurityGroupAssociationToSubnet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7ee5e-143">-VM</span><span class="sxs-lookup"><span data-stu-id="7ee5e-143">-VM</span></span>
<span data-ttu-id="7ee5e-144">Anger den virtuella dator där denna cmdlet ska använda nätverks säkerhets gruppen.</span><span class="sxs-lookup"><span data-stu-id="7ee5e-144">Specifies the virtual machine to which this cmdlet applies the network security group.</span></span>

```yaml
Type: PersistentVMRoleContext
Parameter Sets: AddNetworkSecurityGroupAssociationToIaaSRole
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7ee5e-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7ee5e-145">CommonParameters</span></span>
<span data-ttu-id="7ee5e-146">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7ee5e-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7ee5e-147">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7ee5e-147">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7ee5e-148">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="7ee5e-148">INPUTS</span></span>

## <span data-ttu-id="7ee5e-149">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="7ee5e-149">OUTPUTS</span></span>

### <span data-ttu-id="7ee5e-150">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="7ee5e-150">System.Boolean</span></span>

## <span data-ttu-id="7ee5e-151">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="7ee5e-151">NOTES</span></span>

## <span data-ttu-id="7ee5e-152">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="7ee5e-152">RELATED LINKS</span></span>

[<span data-ttu-id="7ee5e-153">Get-AzureNetworkSecurityGroupAssociation</span><span class="sxs-lookup"><span data-stu-id="7ee5e-153">Get-AzureNetworkSecurityGroupAssociation</span></span>](./Get-AzureNetworkSecurityGroupAssociation.md)

[<span data-ttu-id="7ee5e-154">Remove-AzureNetworkSecurityGroupAssociation</span><span class="sxs-lookup"><span data-stu-id="7ee5e-154">Remove-AzureNetworkSecurityGroupAssociation</span></span>](./Remove-AzureNetworkSecurityGroupAssociation.md)


