---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: 82CF6E71-FFE2-4B2C-8AAD-04C137AD5706
online version: ''
schema: 2.0.0
ms.openlocfilehash: 49f9cce74cb2621d6c9ff51485b7c4bce4a302bf
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94099583"
---
# <span data-ttu-id="3c396-101">Get-AzureEffectiveRouteTable</span><span class="sxs-lookup"><span data-stu-id="3c396-101">Get-AzureEffectiveRouteTable</span></span>

## <span data-ttu-id="3c396-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="3c396-102">SYNOPSIS</span></span>
<span data-ttu-id="3c396-103">Hämtar vägen som används på en virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="3c396-103">Gets the route applied in a virtual machine.</span></span>

## <span data-ttu-id="3c396-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="3c396-104">SYNTAX</span></span>

### <span data-ttu-id="3c396-105">IaaSGetEffectiveRouteTableParamSet</span><span class="sxs-lookup"><span data-stu-id="3c396-105">IaaSGetEffectiveRouteTableParamSet</span></span>
```
Get-AzureEffectiveRouteTable -VM <PersistentVMRoleContext> -ServiceName <String>
 [-NetworkInterfaceName <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="3c396-106">SlotGetEffectiveRouteTableParamSet</span><span class="sxs-lookup"><span data-stu-id="3c396-106">SlotGetEffectiveRouteTableParamSet</span></span>
```
Get-AzureEffectiveRouteTable -ServiceName <String> [-Slot <String>] -RoleInstanceName <String>
 [-NetworkInterfaceName <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="3c396-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="3c396-107">DESCRIPTION</span></span>
<span data-ttu-id="3c396-108">Cmdleten **Get-AzureEffectiveRouteTable** hämtar vägen på en virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="3c396-108">The **Get-AzureEffectiveRouteTable** cmdlet gets the route applied in a virtual machine.</span></span>
<span data-ttu-id="3c396-109">Det kan ta flera sekunder att slutföra den här åtgärden.</span><span class="sxs-lookup"><span data-stu-id="3c396-109">This operation could take several seconds to finish.</span></span>

## <span data-ttu-id="3c396-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="3c396-110">EXAMPLES</span></span>

### <span data-ttu-id="3c396-111">Exempel 1: hämta den effektiva vägen som tillämpas på en virtuell dator</span><span class="sxs-lookup"><span data-stu-id="3c396-111">Example 1: Get the effective route applied a virtual machine</span></span>
```
PS C:\> Get-AzureVM -ServiceName "ContosoService" -Name "ContosoVM06" | Get-AzureEffectiveRouteTable
```

<span data-ttu-id="3c396-112">Det här kommandot får en virtuell dator med namnet ContosoVM06 för tjänsten som heter ContosoService och skickar det virtuella datorobjektet till den aktuella cmdleten.</span><span class="sxs-lookup"><span data-stu-id="3c396-112">This command gets a virtual machine named ContosoVM06 for the service named ContosoService, and passes that virtual machine object to the current cmdlet.</span></span>
<span data-ttu-id="3c396-113">Den aktuella cmdleten får vägen att tillämpas på den virtuella datorn.</span><span class="sxs-lookup"><span data-stu-id="3c396-113">The current cmdlet gets the route applied to that virtual machine.</span></span>

## <span data-ttu-id="3c396-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="3c396-114">PARAMETERS</span></span>

### <span data-ttu-id="3c396-115">-NetworkInterfaceName</span><span class="sxs-lookup"><span data-stu-id="3c396-115">-NetworkInterfaceName</span></span>
<span data-ttu-id="3c396-116">Anger namnet på det nätverkskort som denna cmdlet får effektiva vägar för.</span><span class="sxs-lookup"><span data-stu-id="3c396-116">Specifies the name of the network adapter for which this cmdlet gets effective routes.</span></span>

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

### <span data-ttu-id="3c396-117">-Profil</span><span class="sxs-lookup"><span data-stu-id="3c396-117">-Profile</span></span>
<span data-ttu-id="3c396-118">Anger den Azure-profil från vilken denna cmdlet läser.</span><span class="sxs-lookup"><span data-stu-id="3c396-118">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="3c396-119">Om du inte anger en profil läser denna cmdlet från den lokala standard profilen.</span><span class="sxs-lookup"><span data-stu-id="3c396-119">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="3c396-120">-RoleInstanceName</span><span class="sxs-lookup"><span data-stu-id="3c396-120">-RoleInstanceName</span></span>
<span data-ttu-id="3c396-121">Anger namnet på en PaaS-roll för vilken denna cmdlet hämtar effektiva vägar.</span><span class="sxs-lookup"><span data-stu-id="3c396-121">Specifies the name of a PaaS role for which this cmdlet gets effective routes.</span></span>

```yaml
Type: String
Parameter Sets: SlotGetEffectiveRouteTableParamSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3c396-122">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="3c396-122">-ServiceName</span></span>
<span data-ttu-id="3c396-123">Anger namnet på en moln tjänst.</span><span class="sxs-lookup"><span data-stu-id="3c396-123">Specifies the name of a cloud service.</span></span>
<span data-ttu-id="3c396-124">PaaS-rollen för vilken denna cmdlet hämtar effektiva vägar tillhör den tjänst som anges av den här parametern.</span><span class="sxs-lookup"><span data-stu-id="3c396-124">The PaaS role for which this cmdlet gets effective routes belongs to the service that this parameter specifies.</span></span>

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

### <span data-ttu-id="3c396-125">-Plats</span><span class="sxs-lookup"><span data-stu-id="3c396-125">-Slot</span></span>
<span data-ttu-id="3c396-126">Anger en PaaS-kortplats.</span><span class="sxs-lookup"><span data-stu-id="3c396-126">Specifies a PaaS slot.</span></span>
<span data-ttu-id="3c396-127">PaaS-rollen för vilken denna cmdlet hämtar effektiva vägar har den plats som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="3c396-127">The PaaS role for which this cmdlet gets effective routes has the slot that this parameter specifies.</span></span>
<span data-ttu-id="3c396-128">Giltiga värden är:</span><span class="sxs-lookup"><span data-stu-id="3c396-128">Valid values are:</span></span> 

- <span data-ttu-id="3c396-129">Produktionsoperationsföljden</span><span class="sxs-lookup"><span data-stu-id="3c396-129">Production</span></span>
- <span data-ttu-id="3c396-130">Lagring</span><span class="sxs-lookup"><span data-stu-id="3c396-130">Staging</span></span> 

<span data-ttu-id="3c396-131">Standardvärdet är produktion.</span><span class="sxs-lookup"><span data-stu-id="3c396-131">The default value is Production.</span></span>

```yaml
Type: String
Parameter Sets: SlotGetEffectiveRouteTableParamSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3c396-132">-VM</span><span class="sxs-lookup"><span data-stu-id="3c396-132">-VM</span></span>
<span data-ttu-id="3c396-133">Anger det virtuella dator objekt för vilket denna cmdlet hämtar effektiva vägar.</span><span class="sxs-lookup"><span data-stu-id="3c396-133">Specifies the virtual machine object for which this cmdlet gets effective routes.</span></span>

```yaml
Type: PersistentVMRoleContext
Parameter Sets: IaaSGetEffectiveRouteTableParamSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3c396-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3c396-134">CommonParameters</span></span>
<span data-ttu-id="3c396-135">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3c396-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3c396-136">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3c396-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3c396-137">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="3c396-137">INPUTS</span></span>

## <span data-ttu-id="3c396-138">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="3c396-138">OUTPUTS</span></span>

### <span data-ttu-id="3c396-139">System. Collections. Generic. IEnumerable<Microsoft. WindowsAzure. Management. Network. Models. EffectiveRouteTable, Microsoft. WindowsAzure. Management. Network></span><span class="sxs-lookup"><span data-stu-id="3c396-139">System.Collections.Generic.IEnumerable<Microsoft.WindowsAzure.Management.Network.Models.EffectiveRouteTable, Microsoft.WindowsAzure.Management.Network></span></span>

## <span data-ttu-id="3c396-140">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="3c396-140">NOTES</span></span>

## <span data-ttu-id="3c396-141">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="3c396-141">RELATED LINKS</span></span>

[<span data-ttu-id="3c396-142">Get-AzureRouteTable</span><span class="sxs-lookup"><span data-stu-id="3c396-142">Get-AzureRouteTable</span></span>](./Get-AzureRouteTable.md)

[<span data-ttu-id="3c396-143">New-AzureRouteTable</span><span class="sxs-lookup"><span data-stu-id="3c396-143">New-AzureRouteTable</span></span>](./New-AzureRouteTable.md)

[<span data-ttu-id="3c396-144">Remove-AzureRouteTable</span><span class="sxs-lookup"><span data-stu-id="3c396-144">Remove-AzureRouteTable</span></span>](./Remove-AzureRouteTable.md)

[<span data-ttu-id="3c396-145">Remove-AzureSubnetRouteTable</span><span class="sxs-lookup"><span data-stu-id="3c396-145">Remove-AzureSubnetRouteTable</span></span>](./Remove-AzureSubnetRouteTable.md)

[<span data-ttu-id="3c396-146">Set-AzureSubnetRouteTable</span><span class="sxs-lookup"><span data-stu-id="3c396-146">Set-AzureSubnetRouteTable</span></span>](./Set-AzureSubnetRouteTable.md)


