---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 73CEA6A8-46C9-4772-9A67-03F532696CFD
online version: ''
schema: 2.0.0
ms.openlocfilehash: 6c1287b3a0bb1cc39dea78fb4e92d2dcc4508c6a
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94093269"
---
# <span data-ttu-id="c2c5b-101">Get-AzureSubnet</span><span class="sxs-lookup"><span data-stu-id="c2c5b-101">Get-AzureSubnet</span></span>

## <span data-ttu-id="c2c5b-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="c2c5b-102">SYNOPSIS</span></span>
<span data-ttu-id="c2c5b-103">Hämtar en lista med undernät som är associerade med den angivna virtuella Azure-datorn.</span><span class="sxs-lookup"><span data-stu-id="c2c5b-103">Gets a list of subnets associated with the specified Azure virtual machine.</span></span>

## <span data-ttu-id="c2c5b-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="c2c5b-104">SYNTAX</span></span>

```
Get-AzureSubnet -VM <IPersistentVM> [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="c2c5b-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="c2c5b-105">DESCRIPTION</span></span>
<span data-ttu-id="c2c5b-106">Cmdleten **Get-AzureSubnet** returnerar en lista över de undernät som är associerade med den angivna virtuella datorn.</span><span class="sxs-lookup"><span data-stu-id="c2c5b-106">The **Get-AzureSubnet** cmdlet returns a list the subnets associated with the specified virtual machine.</span></span>
<span data-ttu-id="c2c5b-107">Använd **Get-AzureVM** för att ange den virtuella datorn.</span><span class="sxs-lookup"><span data-stu-id="c2c5b-107">Use **Get-AzureVM** to specify the virtual machine.</span></span>

## <span data-ttu-id="c2c5b-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="c2c5b-108">EXAMPLES</span></span>

### <span data-ttu-id="c2c5b-109">Exempel 1: Hämta undernät för en virtuell dator</span><span class="sxs-lookup"><span data-stu-id="c2c5b-109">Example 1: Get subnets for a virtual machine</span></span>
```
PS C:\> $VM = Get-AzureVM -ServiceName "ContosoService03" -Name "VirtualMachine01"
C:\PS> Get-AzureSubnet -VM $VM
```

<span data-ttu-id="c2c5b-110">Det första kommandot får en virtuell dator som heter VirtualMachine01 i tjänsten ContosoService03 och lagrar den sedan i $VM variabel.</span><span class="sxs-lookup"><span data-stu-id="c2c5b-110">The first command gets a virtual machine named VirtualMachine01 in the service named ContosoService03, and then stores it in the $VM variable.</span></span>

<span data-ttu-id="c2c5b-111">Det andra kommandot får Azure-undernäten för den virtuella datorn i $VM.</span><span class="sxs-lookup"><span data-stu-id="c2c5b-111">The second command gets the Azure subnets for the virtual machine in $VM.</span></span>

## <span data-ttu-id="c2c5b-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="c2c5b-112">PARAMETERS</span></span>

### <span data-ttu-id="c2c5b-113">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="c2c5b-113">-InformationAction</span></span>
<span data-ttu-id="c2c5b-114">Anger hur den här cmdleten svarar på en informations händelse.</span><span class="sxs-lookup"><span data-stu-id="c2c5b-114">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="c2c5b-115">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="c2c5b-115">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="c2c5b-116">Vidare</span><span class="sxs-lookup"><span data-stu-id="c2c5b-116">Continue</span></span>
- <span data-ttu-id="c2c5b-117">Över</span><span class="sxs-lookup"><span data-stu-id="c2c5b-117">Ignore</span></span>
- <span data-ttu-id="c2c5b-118">Inquire</span><span class="sxs-lookup"><span data-stu-id="c2c5b-118">Inquire</span></span>
- <span data-ttu-id="c2c5b-119">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="c2c5b-119">SilentlyContinue</span></span>
- <span data-ttu-id="c2c5b-120">Stanna</span><span class="sxs-lookup"><span data-stu-id="c2c5b-120">Stop</span></span>
- <span data-ttu-id="c2c5b-121">Avbryt</span><span class="sxs-lookup"><span data-stu-id="c2c5b-121">Suspend</span></span>

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

### <span data-ttu-id="c2c5b-122">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="c2c5b-122">-InformationVariable</span></span>
<span data-ttu-id="c2c5b-123">Anger en informations variabel.</span><span class="sxs-lookup"><span data-stu-id="c2c5b-123">Specifies an information variable.</span></span>

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

### <span data-ttu-id="c2c5b-124">-Profil</span><span class="sxs-lookup"><span data-stu-id="c2c5b-124">-Profile</span></span>
<span data-ttu-id="c2c5b-125">Anger den Azure-profil från vilken denna cmdlet läser.</span><span class="sxs-lookup"><span data-stu-id="c2c5b-125">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="c2c5b-126">Om du inte anger en profil läser denna cmdlet från den lokala standard profilen.</span><span class="sxs-lookup"><span data-stu-id="c2c5b-126">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="c2c5b-127">-VM</span><span class="sxs-lookup"><span data-stu-id="c2c5b-127">-VM</span></span>
<span data-ttu-id="c2c5b-128">Anger det virtuella dator objekt som du vill hämta under näts listan från.</span><span class="sxs-lookup"><span data-stu-id="c2c5b-128">Specifies the virtual machine object from which to get the subnet list.</span></span>

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

### <span data-ttu-id="c2c5b-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c2c5b-129">CommonParameters</span></span>
<span data-ttu-id="c2c5b-130">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c2c5b-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c2c5b-131">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c2c5b-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c2c5b-132">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="c2c5b-132">INPUTS</span></span>

## <span data-ttu-id="c2c5b-133">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="c2c5b-133">OUTPUTS</span></span>

## <span data-ttu-id="c2c5b-134">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="c2c5b-134">NOTES</span></span>

## <span data-ttu-id="c2c5b-135">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="c2c5b-135">RELATED LINKS</span></span>

[<span data-ttu-id="c2c5b-136">Get-AzureVM</span><span class="sxs-lookup"><span data-stu-id="c2c5b-136">Get-AzureVM</span></span>](./Get-AzureVM.md)

[<span data-ttu-id="c2c5b-137">Set-AzureSubnet</span><span class="sxs-lookup"><span data-stu-id="c2c5b-137">Set-AzureSubnet</span></span>](./Set-AzureSubnet.md)


