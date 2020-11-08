---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: AA9686AF-2D03-43DB-A91B-50D06D674A3D
online version: ''
schema: 2.0.0
ms.openlocfilehash: fc8da83231a16f4c846f09d03374d6e35757e1ba
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94099186"
---
# <span data-ttu-id="92c9c-101">Set-AzureIPForwarding</span><span class="sxs-lookup"><span data-stu-id="92c9c-101">Set-AzureIPForwarding</span></span>

## <span data-ttu-id="92c9c-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="92c9c-102">SYNOPSIS</span></span>
<span data-ttu-id="92c9c-103">Aktiverar eller inaktiverar IP-vidarekoppling.</span><span class="sxs-lookup"><span data-stu-id="92c9c-103">Enables or disables IP forwarding.</span></span>

## <span data-ttu-id="92c9c-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="92c9c-104">SYNTAX</span></span>

### <span data-ttu-id="92c9c-105">EnableIaaSIPForwardingParamSet</span><span class="sxs-lookup"><span data-stu-id="92c9c-105">EnableIaaSIPForwardingParamSet</span></span>
```
Set-AzureIPForwarding -VM <PersistentVMRoleContext> -ServiceName <String> [-NetworkInterfaceName <String>]
 [-Enable] [-PassThru] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="92c9c-106">DisableIaaSIPForwardingParamSet</span><span class="sxs-lookup"><span data-stu-id="92c9c-106">DisableIaaSIPForwardingParamSet</span></span>
```
Set-AzureIPForwarding -VM <PersistentVMRoleContext> -ServiceName <String> [-NetworkInterfaceName <String>]
 [-Disable] [-PassThru] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="92c9c-107">EnableSlotIPForwardingParamSet</span><span class="sxs-lookup"><span data-stu-id="92c9c-107">EnableSlotIPForwardingParamSet</span></span>
```
Set-AzureIPForwarding -ServiceName <String> [-Slot <String>] -RoleName <String>
 [-NetworkInterfaceName <String>] [-Enable] [-PassThru] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="92c9c-108">DisableSlotIPForwardingParamSet</span><span class="sxs-lookup"><span data-stu-id="92c9c-108">DisableSlotIPForwardingParamSet</span></span>
```
Set-AzureIPForwarding -ServiceName <String> [-Slot <String>] -RoleName <String>
 [-NetworkInterfaceName <String>] [-Disable] [-PassThru] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="92c9c-109">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="92c9c-109">DESCRIPTION</span></span>
<span data-ttu-id="92c9c-110">Cmdleten **set-AzureIPForwarding** aktiverar eller inaktiverar IP-vidarekoppling för en virtuell dator, för en plattform som tjänst (PaaS) eller ett nätverkskort som tillhör en virtuell dator eller PaaS-roll.</span><span class="sxs-lookup"><span data-stu-id="92c9c-110">The **Set-AzureIPForwarding** cmdlet enables or disables IP forwarding for a virtual machine, for a platform as a service (PaaS) role, or a network adapter that belongs to a virtual machine or PaaS role.</span></span>

## <span data-ttu-id="92c9c-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="92c9c-111">EXAMPLES</span></span>

### <span data-ttu-id="92c9c-112">Exempel 1: aktivera IP-vidarekoppling för en virtuell dator</span><span class="sxs-lookup"><span data-stu-id="92c9c-112">Example 1: Enable IP forwarding for a virtual machine</span></span>
```
PS C:\> Get-AzureVM -ServiceName "ContosoService" -Name "ContosoVM06" | Set-AzureIPForwarding -Enable
```

<span data-ttu-id="92c9c-113">Det här kommandot får en virtuell dator med namnet ContosoVM06 för tjänsten som heter ContosoService och skickar det virtuella datorobjektet till den aktuella cmdleten.</span><span class="sxs-lookup"><span data-stu-id="92c9c-113">This command gets a virtual machine named ContosoVM06 for the service named ContosoService, and passes that virtual machine object to the current cmdlet.</span></span>
<span data-ttu-id="92c9c-114">Den aktuella cmdleten aktiverar IP-vidarekoppling för den virtuella datorn.</span><span class="sxs-lookup"><span data-stu-id="92c9c-114">The current cmdlet enables IP forwarding for that virtual machine.</span></span>

### <span data-ttu-id="92c9c-115">Exempel 2: inaktivera IP-vidarekoppling för en virtuell dator</span><span class="sxs-lookup"><span data-stu-id="92c9c-115">Example 2: Disable IP forwarding for a virtual machine</span></span>
```
PS C:\> Get-AzureVM -ServiceName "ContosoService" -Name "ContosoVM06" | Set-AzureIPForwarding -Disable
```

<span data-ttu-id="92c9c-116">Det här kommandot får en virtuell dator med namnet ContosoVM06 för tjänsten som heter ContosoService och skickar det virtuella datorobjektet till den aktuella cmdleten.</span><span class="sxs-lookup"><span data-stu-id="92c9c-116">This command gets a virtual machine named ContosoVM06 for the service named ContosoService, and passes that virtual machine object to the current cmdlet.</span></span>
<span data-ttu-id="92c9c-117">Den aktuella cmdleten inaktiverar IP-vidarekoppling för den virtuella datorn.</span><span class="sxs-lookup"><span data-stu-id="92c9c-117">The current cmdlet disables IP forwarding for that virtual machine.</span></span>

## <span data-ttu-id="92c9c-118">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="92c9c-118">PARAMETERS</span></span>

### <span data-ttu-id="92c9c-119">-Inaktivera</span><span class="sxs-lookup"><span data-stu-id="92c9c-119">-Disable</span></span>
<span data-ttu-id="92c9c-120">Anger att denna cmdlet inaktiverar IP-vidarekoppling.</span><span class="sxs-lookup"><span data-stu-id="92c9c-120">Indicates that this cmdlet disables IP forwarding.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: DisableIaaSIPForwardingParamSet, DisableSlotIPForwardingParamSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="92c9c-121">-Aktivera</span><span class="sxs-lookup"><span data-stu-id="92c9c-121">-Enable</span></span>
<span data-ttu-id="92c9c-122">Anger att denna cmdlet aktiverar IP-vidarekoppling.</span><span class="sxs-lookup"><span data-stu-id="92c9c-122">Indicates that this cmdlet enables IP forwarding.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: EnableIaaSIPForwardingParamSet, EnableSlotIPForwardingParamSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="92c9c-123">-NetworkInterfaceName</span><span class="sxs-lookup"><span data-stu-id="92c9c-123">-NetworkInterfaceName</span></span>
<span data-ttu-id="92c9c-124">Anger namnet på det nätverkskort där denna cmdlet ställer in IP-vidarebefordring.</span><span class="sxs-lookup"><span data-stu-id="92c9c-124">Specifies the name of the network adapter on which this cmdlet sets IP forwarding.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="92c9c-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="92c9c-125">-PassThru</span></span>
<span data-ttu-id="92c9c-126">Returnerar ett objekt som representerar det objekt som du arbetar med.</span><span class="sxs-lookup"><span data-stu-id="92c9c-126">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="92c9c-127">Denna cmdlet genererar som standard inga utdata.</span><span class="sxs-lookup"><span data-stu-id="92c9c-127">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="92c9c-128">-Profil</span><span class="sxs-lookup"><span data-stu-id="92c9c-128">-Profile</span></span>
<span data-ttu-id="92c9c-129">Anger den Azure-profil från vilken denna cmdlet läser.</span><span class="sxs-lookup"><span data-stu-id="92c9c-129">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="92c9c-130">Om du inte anger en profil läser denna cmdlet från den lokala standard profilen.</span><span class="sxs-lookup"><span data-stu-id="92c9c-130">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="92c9c-131">-RoleName</span><span class="sxs-lookup"><span data-stu-id="92c9c-131">-RoleName</span></span>
<span data-ttu-id="92c9c-132">Anger namnet på en PaaS-roll där denna cmdlet ställer in IP-vidarebefordring.</span><span class="sxs-lookup"><span data-stu-id="92c9c-132">Specifies the name of a PaaS role on which this cmdlet sets IP forwarding.</span></span>

```yaml
Type: String
Parameter Sets: EnableSlotIPForwardingParamSet, DisableSlotIPForwardingParamSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="92c9c-133">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="92c9c-133">-ServiceName</span></span>
<span data-ttu-id="92c9c-134">Anger namnet på en moln tjänst.</span><span class="sxs-lookup"><span data-stu-id="92c9c-134">Specifies the name of a cloud service.</span></span>
<span data-ttu-id="92c9c-135">PaaS-rollen tillhör den tjänst som anges av den här parametern.</span><span class="sxs-lookup"><span data-stu-id="92c9c-135">The PaaS role belongs to the service that this parameter specifies.</span></span>

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

### <span data-ttu-id="92c9c-136">-Plats</span><span class="sxs-lookup"><span data-stu-id="92c9c-136">-Slot</span></span>
<span data-ttu-id="92c9c-137">Anger en PaaS-kortplats.</span><span class="sxs-lookup"><span data-stu-id="92c9c-137">Specifies a PaaS slot.</span></span>
<span data-ttu-id="92c9c-138">PaaS-rollen för vilken denna cmdlet ställer in att den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="92c9c-138">The PaaS role for which this cmdlet sets forwarding has the slot that this parameter specifies.</span></span>
<span data-ttu-id="92c9c-139">Giltiga värden är:</span><span class="sxs-lookup"><span data-stu-id="92c9c-139">Valid values are:</span></span>

- <span data-ttu-id="92c9c-140">Produktionsoperationsföljden</span><span class="sxs-lookup"><span data-stu-id="92c9c-140">Production</span></span>
- <span data-ttu-id="92c9c-141">Lagring</span><span class="sxs-lookup"><span data-stu-id="92c9c-141">Staging</span></span>

<span data-ttu-id="92c9c-142">Standardvärdet är produktion.</span><span class="sxs-lookup"><span data-stu-id="92c9c-142">The default value is Production.</span></span>

```yaml
Type: String
Parameter Sets: EnableSlotIPForwardingParamSet, DisableSlotIPForwardingParamSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="92c9c-143">-VM</span><span class="sxs-lookup"><span data-stu-id="92c9c-143">-VM</span></span>
<span data-ttu-id="92c9c-144">Anger det virtuella dator objekt där denna cmdlet anger IP-vidarebefordring.</span><span class="sxs-lookup"><span data-stu-id="92c9c-144">Specifies the virtual machine object on which this cmdlet sets IP forwarding.</span></span>

```yaml
Type: PersistentVMRoleContext
Parameter Sets: EnableIaaSIPForwardingParamSet, DisableIaaSIPForwardingParamSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="92c9c-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="92c9c-145">CommonParameters</span></span>
<span data-ttu-id="92c9c-146">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="92c9c-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="92c9c-147">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="92c9c-147">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="92c9c-148">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="92c9c-148">INPUTS</span></span>

## <span data-ttu-id="92c9c-149">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="92c9c-149">OUTPUTS</span></span>

### <span data-ttu-id="92c9c-150">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="92c9c-150">System.Boolean</span></span>

## <span data-ttu-id="92c9c-151">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="92c9c-151">NOTES</span></span>

## <span data-ttu-id="92c9c-152">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="92c9c-152">RELATED LINKS</span></span>

[<span data-ttu-id="92c9c-153">Get-AzureIPForwarding</span><span class="sxs-lookup"><span data-stu-id="92c9c-153">Get-AzureIPForwarding</span></span>](./Get-AzureIPForwarding.md)
