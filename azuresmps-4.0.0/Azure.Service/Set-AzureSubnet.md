---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 69974370-4542-4417-BD9D-3928EB005C31
online version: ''
schema: 2.0.0
ms.openlocfilehash: 81d6e523978196a47b01d21aa8e857027b0b4f40
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94099181"
---
# <span data-ttu-id="df3f3-101">Set-AzureSubnet</span><span class="sxs-lookup"><span data-stu-id="df3f3-101">Set-AzureSubnet</span></span>

## <span data-ttu-id="df3f3-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="df3f3-102">SYNOPSIS</span></span>
<span data-ttu-id="df3f3-103">Definierar under nätets lista för en virtuell Azure-dator.</span><span class="sxs-lookup"><span data-stu-id="df3f3-103">Defines the subnet list for an Azure virtual machine.</span></span>

## <span data-ttu-id="df3f3-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="df3f3-104">SYNTAX</span></span>

```
Set-AzureSubnet [-SubnetNames] <String[]> -VM <IPersistentVM> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="df3f3-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="df3f3-105">DESCRIPTION</span></span>
<span data-ttu-id="df3f3-106">Cmdleten **set-AzureSubnet** anger under nätets lista för konfiguration av en virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="df3f3-106">The **Set-AzureSubnet** cmdlet sets the subnet list for a virtual machine configuration.</span></span>
<span data-ttu-id="df3f3-107">Använd med **New-AzureVM** för att ställa in under näten för en virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="df3f3-107">Use with **New-AzureVM** to set the subnets for a virtual machine.</span></span>

## <span data-ttu-id="df3f3-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="df3f3-108">EXAMPLES</span></span>

### <span data-ttu-id="df3f3-109">Exempel 1: lägga till ett undernät till en virtuell dator konfiguration</span><span class="sxs-lookup"><span data-stu-id="df3f3-109">Example 1: Add a subnet to a virtual machine configuration</span></span>
```
PS C:\> New-AzureVMConfig -Name "VirtualMachine04" -ImageName $image -InstanceSize "Small" | Add-AzureProvisioningConfig -Windows -Password "password" | Set-AzureSubnet "PubSubnet","PrivSubnet" | New-AzureVM -ServiceName "ContosoService03"
```

<span data-ttu-id="df3f3-110">Det här kommandot lägger till ett undernät till den virtuella dator konfigurationen och skapar sedan den virtuella datorn med namnet VirtualMachine04.</span><span class="sxs-lookup"><span data-stu-id="df3f3-110">This command adds a subnet to the virtual machine configuration, and then creates the virtual machine named VirtualMachine04.</span></span>

## <span data-ttu-id="df3f3-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="df3f3-111">PARAMETERS</span></span>

### <span data-ttu-id="df3f3-112">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="df3f3-112">-InformationAction</span></span>
<span data-ttu-id="df3f3-113">Anger hur den här cmdleten svarar på en informations händelse.</span><span class="sxs-lookup"><span data-stu-id="df3f3-113">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="df3f3-114">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="df3f3-114">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="df3f3-115">Vidare</span><span class="sxs-lookup"><span data-stu-id="df3f3-115">Continue</span></span>
- <span data-ttu-id="df3f3-116">Över</span><span class="sxs-lookup"><span data-stu-id="df3f3-116">Ignore</span></span>
- <span data-ttu-id="df3f3-117">Inquire</span><span class="sxs-lookup"><span data-stu-id="df3f3-117">Inquire</span></span>
- <span data-ttu-id="df3f3-118">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="df3f3-118">SilentlyContinue</span></span>
- <span data-ttu-id="df3f3-119">Stanna</span><span class="sxs-lookup"><span data-stu-id="df3f3-119">Stop</span></span>
- <span data-ttu-id="df3f3-120">Avbryt</span><span class="sxs-lookup"><span data-stu-id="df3f3-120">Suspend</span></span>

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

### <span data-ttu-id="df3f3-121">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="df3f3-121">-InformationVariable</span></span>
<span data-ttu-id="df3f3-122">Anger en informations variabel.</span><span class="sxs-lookup"><span data-stu-id="df3f3-122">Specifies an information variable.</span></span>

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

### <span data-ttu-id="df3f3-123">-Profil</span><span class="sxs-lookup"><span data-stu-id="df3f3-123">-Profile</span></span>
<span data-ttu-id="df3f3-124">Anger den Azure-profil från vilken denna cmdlet läser.</span><span class="sxs-lookup"><span data-stu-id="df3f3-124">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="df3f3-125">Om du inte anger en profil läser denna cmdlet från den lokala standard profilen.</span><span class="sxs-lookup"><span data-stu-id="df3f3-125">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="df3f3-126">-SubnetNames</span><span class="sxs-lookup"><span data-stu-id="df3f3-126">-SubnetNames</span></span>
<span data-ttu-id="df3f3-127">Anger en matris som innehåller listan med under näts namn.</span><span class="sxs-lookup"><span data-stu-id="df3f3-127">Specifies an array that contains the list of subnet names.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="df3f3-128">-VM</span><span class="sxs-lookup"><span data-stu-id="df3f3-128">-VM</span></span>
<span data-ttu-id="df3f3-129">Anger det virtuella datorobjektet.</span><span class="sxs-lookup"><span data-stu-id="df3f3-129">Specifies the virtual machine object.</span></span>

```yaml
Type: IPersistentVM
Parameter Sets: (All)
Aliases: InputObject

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="df3f3-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="df3f3-130">CommonParameters</span></span>
<span data-ttu-id="df3f3-131">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="df3f3-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="df3f3-132">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="df3f3-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="df3f3-133">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="df3f3-133">INPUTS</span></span>

## <span data-ttu-id="df3f3-134">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="df3f3-134">OUTPUTS</span></span>

## <span data-ttu-id="df3f3-135">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="df3f3-135">NOTES</span></span>

## <span data-ttu-id="df3f3-136">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="df3f3-136">RELATED LINKS</span></span>

[<span data-ttu-id="df3f3-137">Get-AzureVM</span><span class="sxs-lookup"><span data-stu-id="df3f3-137">Get-AzureVM</span></span>](./Get-AzureVM.md)

[<span data-ttu-id="df3f3-138">New-AzureVM</span><span class="sxs-lookup"><span data-stu-id="df3f3-138">New-AzureVM</span></span>](./New-AzureVM.md)

[<span data-ttu-id="df3f3-139">Update-AzureVM</span><span class="sxs-lookup"><span data-stu-id="df3f3-139">Update-AzureVM</span></span>](./Update-AzureVM.md)


