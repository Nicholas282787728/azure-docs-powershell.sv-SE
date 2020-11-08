---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: BE661AC7-BA39-4D6A-8083-16CE9327DC08
online version: ''
schema: 2.0.0
ms.openlocfilehash: cf4c84155484435a9601af005393593040c9cfe4
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94099578"
---
# <span data-ttu-id="8252c-101">Get-AzureIPForwarding</span><span class="sxs-lookup"><span data-stu-id="8252c-101">Get-AzureIPForwarding</span></span>

## <span data-ttu-id="8252c-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="8252c-102">SYNOPSIS</span></span>
<span data-ttu-id="8252c-103">Hämtar statusen för IP-vidarekoppling.</span><span class="sxs-lookup"><span data-stu-id="8252c-103">Gets the status of IP forwarding.</span></span>

## <span data-ttu-id="8252c-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="8252c-104">SYNTAX</span></span>

### <span data-ttu-id="8252c-105">IaaSIPForwardingParamSet</span><span class="sxs-lookup"><span data-stu-id="8252c-105">IaaSIPForwardingParamSet</span></span>
```
Get-AzureIPForwarding -VM <PersistentVMRoleContext> -ServiceName <String> [-NetworkInterfaceName <String>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="8252c-106">SlotIPForwardingParamSet</span><span class="sxs-lookup"><span data-stu-id="8252c-106">SlotIPForwardingParamSet</span></span>
```
Get-AzureIPForwarding -ServiceName <String> [-Slot <String>] -RoleName <String>
 [-NetworkInterfaceName <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="8252c-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="8252c-107">DESCRIPTION</span></span>
<span data-ttu-id="8252c-108">Cmdleten **Get-AzureIPForwarding** får statusen IP-vidarebefordring.</span><span class="sxs-lookup"><span data-stu-id="8252c-108">The **Get-AzureIPForwarding** cmdlet gets the status of IP forwarding.</span></span>

## <span data-ttu-id="8252c-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="8252c-109">EXAMPLES</span></span>

### <span data-ttu-id="8252c-110">Exempel 1: Hämta status för IP-vidarekoppling för en virtuell dator</span><span class="sxs-lookup"><span data-stu-id="8252c-110">Example 1: Get IP forwarding status for a virtual machine</span></span>
```
PS C:\> Get-AzureVM -ServiceName "ContosoService" -Name "ContosoVM06" | Get-AzureIPForwarding
Disabled
```

<span data-ttu-id="8252c-111">Det här kommandot får en virtuell dator med namnet ContosoVM06 för tjänsten som heter ContosoService och skickar det virtuella datorobjektet till den aktuella cmdleten.</span><span class="sxs-lookup"><span data-stu-id="8252c-111">This command gets a virtual machine named ContosoVM06 for the service named ContosoService, and passes that virtual machine object to the current cmdlet.</span></span>
<span data-ttu-id="8252c-112">Den aktuella cmdleten får statusen för IP-vidarekoppling för den virtuella datorn.</span><span class="sxs-lookup"><span data-stu-id="8252c-112">The current cmdlet gets the status of IP forwarding for that virtual machine.</span></span>

## <span data-ttu-id="8252c-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="8252c-113">PARAMETERS</span></span>

### <span data-ttu-id="8252c-114">-NetworkInterfaceName</span><span class="sxs-lookup"><span data-stu-id="8252c-114">-NetworkInterfaceName</span></span>
<span data-ttu-id="8252c-115">Anger namnet på det nätverkskort som den här cmdleten får IP-vidarebefordringstabellen för.</span><span class="sxs-lookup"><span data-stu-id="8252c-115">Specifies the name of the network adapter for which this cmdlet gets IP forwarding status.</span></span>

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

### <span data-ttu-id="8252c-116">-Profil</span><span class="sxs-lookup"><span data-stu-id="8252c-116">-Profile</span></span>
<span data-ttu-id="8252c-117">Anger den Azure-profil från vilken denna cmdlet läser.</span><span class="sxs-lookup"><span data-stu-id="8252c-117">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="8252c-118">Om du inte anger en profil läser denna cmdlet från den lokala standard profilen.</span><span class="sxs-lookup"><span data-stu-id="8252c-118">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="8252c-119">-RoleName</span><span class="sxs-lookup"><span data-stu-id="8252c-119">-RoleName</span></span>
<span data-ttu-id="8252c-120">Anger namnet på en PaaS-roll för vilken denna cmdlet får IP Forwarding-status.</span><span class="sxs-lookup"><span data-stu-id="8252c-120">Specifies the name of a PaaS role for which this cmdlet gets IP forwarding status.</span></span>

```yaml
Type: String
Parameter Sets: SlotIPForwardingParamSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8252c-121">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="8252c-121">-ServiceName</span></span>
<span data-ttu-id="8252c-122">Anger namnet på en moln tjänst.</span><span class="sxs-lookup"><span data-stu-id="8252c-122">Specifies the name of a cloud service.</span></span>
<span data-ttu-id="8252c-123">PaaS-rollen tillhör den tjänst som anges av den här parametern.</span><span class="sxs-lookup"><span data-stu-id="8252c-123">The PaaS role belongs to the service that this parameter specifies.</span></span>

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

### <span data-ttu-id="8252c-124">-Plats</span><span class="sxs-lookup"><span data-stu-id="8252c-124">-Slot</span></span>
<span data-ttu-id="8252c-125">Anger en PaaS-kortplats.</span><span class="sxs-lookup"><span data-stu-id="8252c-125">Specifies a PaaS slot.</span></span>
<span data-ttu-id="8252c-126">PaaS-rollen för vilken den här cmdleten vidarebefordrar status är den plats som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="8252c-126">The PaaS role for which this cmdlet gets forwarding status has the slot that this parameter specifies.</span></span>
<span data-ttu-id="8252c-127">Giltiga värden är:</span><span class="sxs-lookup"><span data-stu-id="8252c-127">Valid values are:</span></span> 

- <span data-ttu-id="8252c-128">Produktionsoperationsföljden</span><span class="sxs-lookup"><span data-stu-id="8252c-128">Production</span></span>
- <span data-ttu-id="8252c-129">Lagring</span><span class="sxs-lookup"><span data-stu-id="8252c-129">Staging</span></span> 

<span data-ttu-id="8252c-130">Standardvärdet är produktion.</span><span class="sxs-lookup"><span data-stu-id="8252c-130">The default value is Production.</span></span>

```yaml
Type: String
Parameter Sets: SlotIPForwardingParamSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8252c-131">-VM</span><span class="sxs-lookup"><span data-stu-id="8252c-131">-VM</span></span>
<span data-ttu-id="8252c-132">Anger den virtuella datorobjektet för vilken denna cmdlet får IP Forwarding-status.</span><span class="sxs-lookup"><span data-stu-id="8252c-132">Specifies the virtual machine object for which this cmdlet gets IP forwarding status.</span></span>

```yaml
Type: PersistentVMRoleContext
Parameter Sets: IaaSIPForwardingParamSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8252c-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8252c-133">CommonParameters</span></span>
<span data-ttu-id="8252c-134">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8252c-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8252c-135">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8252c-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8252c-136">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="8252c-136">INPUTS</span></span>

## <span data-ttu-id="8252c-137">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="8252c-137">OUTPUTS</span></span>

### <span data-ttu-id="8252c-138">System. String</span><span class="sxs-lookup"><span data-stu-id="8252c-138">System.String</span></span>

## <span data-ttu-id="8252c-139">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="8252c-139">NOTES</span></span>

## <span data-ttu-id="8252c-140">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="8252c-140">RELATED LINKS</span></span>

[<span data-ttu-id="8252c-141">Set-AzureIPForwarding</span><span class="sxs-lookup"><span data-stu-id="8252c-141">Set-AzureIPForwarding</span></span>](./Set-AzureIPForwarding.md)


