---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 22A9B83D-789D-4722-BDD1-D8C448CFB88A
online version: ''
schema: 2.0.0
ms.openlocfilehash: c809a49e2e8c1a534d6868c99bcc7cab1d20ccd1
ms.sourcegitcommit: 3d16496984a0b9fd7631aa043726060ddae3624d
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/08/2020
ms.locfileid: "94100611"
---
# <span data-ttu-id="66136-101">New-WAPackStaticIPAddressPool</span><span class="sxs-lookup"><span data-stu-id="66136-101">New-WAPackStaticIPAddressPool</span></span>

## <span data-ttu-id="66136-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="66136-102">SYNOPSIS</span></span>
<span data-ttu-id="66136-103">Skapar en statisk IP-adresspool.</span><span class="sxs-lookup"><span data-stu-id="66136-103">Creates a static IP address pool.</span></span>

## <span data-ttu-id="66136-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="66136-104">SYNTAX</span></span>

```
New-WAPackStaticIPAddressPool -VMSubnet <VMSubnet> -Name <String> -IPAddressRangeStart <String>
 -IPAddressRangeEnd <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="66136-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="66136-105">DESCRIPTION</span></span>
<span data-ttu-id="66136-106">De här ämnena är föråldrade och kommer att tas bort i framtiden.</span><span class="sxs-lookup"><span data-stu-id="66136-106">These topics are deprecated and will be removed in the future.</span></span>
<span data-ttu-id="66136-107">I det här avsnittet beskrivs cmdleten i 0.8.1-versionen av Microsoft Azure PowerShell-modulen.</span><span class="sxs-lookup"><span data-stu-id="66136-107">This topic describes the cmdlet in the 0.8.1 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="66136-108">För att ta reda på vilken version av modulen du använder, går du till Azure PowerShell-konsolen och skriver `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="66136-108">To find out the version of the module you're using, from the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="66136-109">Cmdleten **New-WAPackStaticIPAddressPool** skapar en statisk IP-adresspool.</span><span class="sxs-lookup"><span data-stu-id="66136-109">The **New-WAPackStaticIPAddressPool** cmdlet creates a static IP address pool.</span></span>

## <span data-ttu-id="66136-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="66136-110">EXAMPLES</span></span>

### <span data-ttu-id="66136-111">Exempel 1: skapa en statisk IP-adresspool</span><span class="sxs-lookup"><span data-stu-id="66136-111">Example 1: Create a static IP address pool</span></span>
```
PS C:\> $VNet = Get-WAPackVNet -Name "ContosoVNet01"
PS C:\> $VMSubnet = Get-WAPackVMSubnet -VNet $VNet -Name "ContosoVMSubnet01"
PS C:\> New-WAPackStaticIpAddressPool ?VMSubnet $VMSubnet -Name "ContosoStaticIpAddressPool01" -IPAddressRangeStart "192.168.1.0" -IPAddressRangeEnd "192.168.1.10"
```

<span data-ttu-id="66136-112">Första kommandot hämtar först det virtuella dator nätverk som vi vill lägga till en statisk IP-adresspool för.</span><span class="sxs-lookup"><span data-stu-id="66136-112">The first command first retrieves the virtual machine network to which we want to add the static IP address pool.</span></span>
<span data-ttu-id="66136-113">Det här virtuella dator nätverket heter ContosoVNet01.</span><span class="sxs-lookup"><span data-stu-id="66136-113">This virtual machine network is named ContosoVNet01.</span></span>

<span data-ttu-id="66136-114">Det andra kommandot använder det tidigare hämtade virtuella dator nätverket för att hämta det virtuella dator under nätet som heter ContosoVMSubnet01 som vi vill lägga till den statiska IP-adresspoolen för.</span><span class="sxs-lookup"><span data-stu-id="66136-114">The second command uses the previously retrieved virtual machine network to get the virtual machine subnet named ContosoVMSubnet01 to which we want to add the static IP address pool.</span></span>

<span data-ttu-id="66136-115">Det sista kommandot skapar en ny statisk IP-adresspool med ett namn ContosoStaticIpAddressPool01 och ett intervall start-192.168.1.0 och ett intervall-end 192.168.1.10.</span><span class="sxs-lookup"><span data-stu-id="66136-115">The last command creates a new static IP address pool with a name ContosoStaticIpAddressPool01 and a range start 192.168.1.0 and a range end 192.168.1.10.</span></span>

## <span data-ttu-id="66136-116">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="66136-116">PARAMETERS</span></span>

### <span data-ttu-id="66136-117">-IPAddressRangeEnd</span><span class="sxs-lookup"><span data-stu-id="66136-117">-IPAddressRangeEnd</span></span>
<span data-ttu-id="66136-118">Anger ett IP-adressintervall för den statiska IP-adresspoolen.</span><span class="sxs-lookup"><span data-stu-id="66136-118">Specifies an IP address range end for the static IP address pool.</span></span>

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

### <span data-ttu-id="66136-119">-IPAddressRangeStart</span><span class="sxs-lookup"><span data-stu-id="66136-119">-IPAddressRangeStart</span></span>
<span data-ttu-id="66136-120">Anger ett IP-adressintervall för den statiska IP-adresspoolen.</span><span class="sxs-lookup"><span data-stu-id="66136-120">Specifies an IP address range start for the static IP address pool.</span></span>

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

### <span data-ttu-id="66136-121">-Namn</span><span class="sxs-lookup"><span data-stu-id="66136-121">-Name</span></span>
<span data-ttu-id="66136-122">Anger ett namn för den statiska IP-adresspoolen.</span><span class="sxs-lookup"><span data-stu-id="66136-122">Specifies a name for the static IP address pool.</span></span>

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

### <span data-ttu-id="66136-123">-Profil</span><span class="sxs-lookup"><span data-stu-id="66136-123">-Profile</span></span>
<span data-ttu-id="66136-124">Anger den Azure-profil från vilken denna cmdlet läser.</span><span class="sxs-lookup"><span data-stu-id="66136-124">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="66136-125">Om du inte anger en profil läser denna cmdlet från den lokala standard profilen.</span><span class="sxs-lookup"><span data-stu-id="66136-125">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="66136-126">-VMSubnet</span><span class="sxs-lookup"><span data-stu-id="66136-126">-VMSubnet</span></span>
<span data-ttu-id="66136-127">Anger ett VMSubnet som är associerat med den statiska IP-adresspoolen.</span><span class="sxs-lookup"><span data-stu-id="66136-127">Specifies a VMSubnet associated with the static IP address pool.</span></span>

```yaml
Type: VMSubnet
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="66136-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="66136-128">CommonParameters</span></span>
<span data-ttu-id="66136-129">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="66136-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="66136-130">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="66136-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="66136-131">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="66136-131">INPUTS</span></span>

## <span data-ttu-id="66136-132">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="66136-132">OUTPUTS</span></span>

## <span data-ttu-id="66136-133">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="66136-133">NOTES</span></span>

## <span data-ttu-id="66136-134">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="66136-134">RELATED LINKS</span></span>

[<span data-ttu-id="66136-135">Get-WAPackStaticIPAddressPool</span><span class="sxs-lookup"><span data-stu-id="66136-135">Get-WAPackStaticIPAddressPool</span></span>](./Get-WAPackStaticIPAddressPool.md)

[<span data-ttu-id="66136-136">Remove-WAPackStaticIPAddressPool</span><span class="sxs-lookup"><span data-stu-id="66136-136">Remove-WAPackStaticIPAddressPool</span></span>](./Remove-WAPackStaticIPAddressPool.md)


