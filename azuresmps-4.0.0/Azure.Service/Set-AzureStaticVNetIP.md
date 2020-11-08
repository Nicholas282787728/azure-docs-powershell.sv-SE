---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: E54E4D16-DB2A-4626-B543-773C187B2E08
online version: ''
schema: 2.0.0
ms.openlocfilehash: d242418117b1bb576206f9ebb5fd568bd3e63cd1
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94099092"
---
# <span data-ttu-id="38bbc-101">Set-AzureStaticVNetIP</span><span class="sxs-lookup"><span data-stu-id="38bbc-101">Set-AzureStaticVNetIP</span></span>

## <span data-ttu-id="38bbc-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="38bbc-102">SYNOPSIS</span></span>
<span data-ttu-id="38bbc-103">Anger den statiska IP-adressen för ett virtuellt dator objekt.</span><span class="sxs-lookup"><span data-stu-id="38bbc-103">Sets the static VNet IP address information for a virtual machine object.</span></span>

## <span data-ttu-id="38bbc-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="38bbc-104">SYNTAX</span></span>

```
Set-AzureStaticVNetIP [-IPAddress] <String> -VM <IPersistentVM> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="38bbc-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="38bbc-105">DESCRIPTION</span></span>
<span data-ttu-id="38bbc-106">Cmdleten **set-AzureStaticVNetIP** anger den statiska virtuell nätverks informationen (VNet) för ett virtuellt dator objekt.</span><span class="sxs-lookup"><span data-stu-id="38bbc-106">The **Set-AzureStaticVNetIP** cmdlet sets the static virtual network (VNet) IP address information for a virtual machine object.</span></span>

## <span data-ttu-id="38bbc-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="38bbc-107">EXAMPLES</span></span>

### <span data-ttu-id="38bbc-108">Exempel 1: Ange virtuell nätverks-IP-adress kopplad till en virtuell dator</span><span class="sxs-lookup"><span data-stu-id="38bbc-108">Example 1: Set the virtual network IP address associated with a virtual machine</span></span>
```
PS C:\> # Prerequisite: VNet has been set up with SubNet
          # Set-AzureVNetConfig -ConfigurationPath $vnetConfigPath;

          $vm = New-AzureVMConfig -Name $vmname -ImageName $img -InstanceSize $sz | Add-AzureProvisioningConfig -Windows -Password $pwd -AdminUsername $usr;
          $vm = Set-AzureSubNet -VM $vm -SubNetNames $sn;
          Set-AzureStaticVNetIP -IPAddress $ip -VM $vm;
          New-AzureVM -ServiceName $svc -VMs $vm -VNetName $vnetName -Location $loc;
```

<span data-ttu-id="38bbc-109">Det första kommandot anger konfigurations Sök vägen för ett virtuellt nätverk.</span><span class="sxs-lookup"><span data-stu-id="38bbc-109">The first command sets the configuration path for a virtual network.</span></span>

<span data-ttu-id="38bbc-110">Det andra kommandot skapar en konfiguration för en virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="38bbc-110">The second command creates a virtual machine configuration.</span></span>

<span data-ttu-id="38bbc-111">Det tredje kommandot ställer in under nätet för den virtuella datorn.</span><span class="sxs-lookup"><span data-stu-id="38bbc-111">The third command sets the subnet for the virtual machine.</span></span>

<span data-ttu-id="38bbc-112">Det fjärde kommandot anger den virtuella datorns IP-adress.</span><span class="sxs-lookup"><span data-stu-id="38bbc-112">The fourth command sets the IP address for the virtual machine.</span></span>

<span data-ttu-id="38bbc-113">Det femte kommandot skapar en virtuell dator med den virtuella datorn.</span><span class="sxs-lookup"><span data-stu-id="38bbc-113">The fifth command creates a virtual machine using the virtual machine.</span></span>

## <span data-ttu-id="38bbc-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="38bbc-114">PARAMETERS</span></span>

### <span data-ttu-id="38bbc-115">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="38bbc-115">-InformationAction</span></span>
<span data-ttu-id="38bbc-116">Anger hur den här cmdleten svarar på en informations händelse.</span><span class="sxs-lookup"><span data-stu-id="38bbc-116">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="38bbc-117">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="38bbc-117">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="38bbc-118">Vidare</span><span class="sxs-lookup"><span data-stu-id="38bbc-118">Continue</span></span>
- <span data-ttu-id="38bbc-119">Över</span><span class="sxs-lookup"><span data-stu-id="38bbc-119">Ignore</span></span>
- <span data-ttu-id="38bbc-120">Inquire</span><span class="sxs-lookup"><span data-stu-id="38bbc-120">Inquire</span></span>
- <span data-ttu-id="38bbc-121">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="38bbc-121">SilentlyContinue</span></span>
- <span data-ttu-id="38bbc-122">Stanna</span><span class="sxs-lookup"><span data-stu-id="38bbc-122">Stop</span></span>
- <span data-ttu-id="38bbc-123">Avbryt</span><span class="sxs-lookup"><span data-stu-id="38bbc-123">Suspend</span></span>

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

### <span data-ttu-id="38bbc-124">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="38bbc-124">-InformationVariable</span></span>
<span data-ttu-id="38bbc-125">Anger en informations variabel.</span><span class="sxs-lookup"><span data-stu-id="38bbc-125">Specifies an information variable.</span></span>

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

### <span data-ttu-id="38bbc-126">-IPAddress</span><span class="sxs-lookup"><span data-stu-id="38bbc-126">-IPAddress</span></span>
<span data-ttu-id="38bbc-127">Anger den statiska IP-adressen för VNet</span><span class="sxs-lookup"><span data-stu-id="38bbc-127">Specifies the static VNet IP address</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="38bbc-128">-Profil</span><span class="sxs-lookup"><span data-stu-id="38bbc-128">-Profile</span></span>
<span data-ttu-id="38bbc-129">Anger den Azure-profil från vilken denna cmdlet läser.</span><span class="sxs-lookup"><span data-stu-id="38bbc-129">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="38bbc-130">Om du inte anger en profil läser denna cmdlet från den lokala standard profilen.</span><span class="sxs-lookup"><span data-stu-id="38bbc-130">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="38bbc-131">-VM</span><span class="sxs-lookup"><span data-stu-id="38bbc-131">-VM</span></span>
<span data-ttu-id="38bbc-132">Anger ett permanent virtuellt dator objekt för vilket du vill ange IP-adressen för det statiska VNet.</span><span class="sxs-lookup"><span data-stu-id="38bbc-132">Specifies a persistent virtual machine object for which to set the static VNet IP address.</span></span>

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

### <span data-ttu-id="38bbc-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="38bbc-133">CommonParameters</span></span>
<span data-ttu-id="38bbc-134">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="38bbc-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="38bbc-135">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="38bbc-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="38bbc-136">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="38bbc-136">INPUTS</span></span>

## <span data-ttu-id="38bbc-137">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="38bbc-137">OUTPUTS</span></span>

## <span data-ttu-id="38bbc-138">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="38bbc-138">NOTES</span></span>

## <span data-ttu-id="38bbc-139">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="38bbc-139">RELATED LINKS</span></span>

[<span data-ttu-id="38bbc-140">Get-AzureStaticVNetIP</span><span class="sxs-lookup"><span data-stu-id="38bbc-140">Get-AzureStaticVNetIP</span></span>](./Get-AzureStaticVNetIP.md)

[<span data-ttu-id="38bbc-141">Test-AzureStaticVNetIP</span><span class="sxs-lookup"><span data-stu-id="38bbc-141">Test-AzureStaticVNetIP</span></span>](./Test-AzureStaticVNetIP.md)


