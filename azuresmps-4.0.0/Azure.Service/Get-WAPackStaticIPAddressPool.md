---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 4414EA89-8573-416E-A611-DA2135E350BD
online version: ''
schema: 2.0.0
ms.openlocfilehash: 75b216b512c364a3285df185a3365b1fc85a3d94
ms.sourcegitcommit: 3d16496984a0b9fd7631aa043726060ddae3624d
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/08/2020
ms.locfileid: "94100661"
---
# <span data-ttu-id="41880-101">Get-WAPackStaticIPAddressPool</span><span class="sxs-lookup"><span data-stu-id="41880-101">Get-WAPackStaticIPAddressPool</span></span>

## <span data-ttu-id="41880-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="41880-102">SYNOPSIS</span></span>
<span data-ttu-id="41880-103">Hämtar statiska IP-adresspooler.</span><span class="sxs-lookup"><span data-stu-id="41880-103">Gets static IP address pool objects.</span></span>

## <span data-ttu-id="41880-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="41880-104">SYNTAX</span></span>

### <span data-ttu-id="41880-105">FromVMSubnetObject (standard)</span><span class="sxs-lookup"><span data-stu-id="41880-105">FromVMSubnetObject (Default)</span></span>
```
Get-WAPackStaticIPAddressPool -VMSubnet <VMSubnet> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="41880-106">FromName</span><span class="sxs-lookup"><span data-stu-id="41880-106">FromName</span></span>
```
Get-WAPackStaticIPAddressPool -VMSubnet <VMSubnet> -Name <String> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="41880-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="41880-107">DESCRIPTION</span></span>
<span data-ttu-id="41880-108">De här ämnena är föråldrade och kommer att tas bort i framtiden.</span><span class="sxs-lookup"><span data-stu-id="41880-108">These topics are deprecated and will be removed in the future.</span></span>
<span data-ttu-id="41880-109">I det här avsnittet beskrivs cmdleten i 0.8.1-versionen av Microsoft Azure PowerShell-modulen.</span><span class="sxs-lookup"><span data-stu-id="41880-109">This topic describes the cmdlet in the 0.8.1 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="41880-110">För att ta reda på vilken version av modulen du använder, går du till Azure PowerShell-konsolen och skriver `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="41880-110">To find out the version of the module you're using, from the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="41880-111">Cmdleten **Get-WAPackStaticIPAddressPool** får statiska IP-adresspooler.</span><span class="sxs-lookup"><span data-stu-id="41880-111">The **Get-WAPackStaticIPAddressPool** cmdlet gets static IP address pool objects.</span></span>

## <span data-ttu-id="41880-112">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="41880-112">EXAMPLES</span></span>

### <span data-ttu-id="41880-113">Exempel 1: Hämta en statisk IP-adresspool från ett visst VMSubnet</span><span class="sxs-lookup"><span data-stu-id="41880-113">Example 1: Get a static IP address pool from a given VMSubnet</span></span>
```
PS C:\> $Subnet = Get-WAPackVMSubet -Name "ContosoVMSubnet01"
PS C:\> Get-WAPackStaticIPAddressPool -VMSubnet $Subnet -Name "ContosoStaticIPAddressPool01"
```

<span data-ttu-id="41880-114">Det här kommandot får den statiska IP-adresspoolen som heter ContosoStaticIPAddressPool01 från ett angivet VMSubnet.</span><span class="sxs-lookup"><span data-stu-id="41880-114">This command gets the static IP address pool named ContosoStaticIPAddressPool01 from a specified VMSubnet.</span></span>

### <span data-ttu-id="41880-115">Exempel 2: Hämta alla statiska IP-adresspooler från ett visst VMSubnet</span><span class="sxs-lookup"><span data-stu-id="41880-115">Example 2: Get all static IP address pools from a given VMSubnet</span></span>
```
PS C:\> $Subnet = Get-WAPackVMSubet -Name "ContosoVMSubnet01"
PS C:\> Get-WAPackStaticIPAddressPool -VMSubnet $Subnet
```

<span data-ttu-id="41880-116">Det här kommandot får alla statiska IP-pooler från ett angivet VMSubet.</span><span class="sxs-lookup"><span data-stu-id="41880-116">This command gets all the static IP pools from a specified VMSubet.</span></span>

## <span data-ttu-id="41880-117">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="41880-117">PARAMETERS</span></span>

### <span data-ttu-id="41880-118">-Namn</span><span class="sxs-lookup"><span data-stu-id="41880-118">-Name</span></span>
<span data-ttu-id="41880-119">Anger namnet på en statisk IP-adresspool.</span><span class="sxs-lookup"><span data-stu-id="41880-119">Specifies the name of a static IP address pool.</span></span>

```yaml
Type: String
Parameter Sets: FromName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="41880-120">-Profil</span><span class="sxs-lookup"><span data-stu-id="41880-120">-Profile</span></span>
<span data-ttu-id="41880-121">Anger den Azure-profil från vilken denna cmdlet läser.</span><span class="sxs-lookup"><span data-stu-id="41880-121">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="41880-122">Om du inte anger en profil läser denna cmdlet från den lokala standard profilen.</span><span class="sxs-lookup"><span data-stu-id="41880-122">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="41880-123">-VMSubnet</span><span class="sxs-lookup"><span data-stu-id="41880-123">-VMSubnet</span></span>
<span data-ttu-id="41880-124">Anger det **VMSubnet** -objekt som är associerat med den statiska IP-adresspoolen.</span><span class="sxs-lookup"><span data-stu-id="41880-124">Specifies the **VMSubnet** object associated to the static IP address pool.</span></span>

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

### <span data-ttu-id="41880-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="41880-125">CommonParameters</span></span>
<span data-ttu-id="41880-126">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="41880-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="41880-127">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="41880-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="41880-128">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="41880-128">INPUTS</span></span>

## <span data-ttu-id="41880-129">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="41880-129">OUTPUTS</span></span>

## <span data-ttu-id="41880-130">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="41880-130">NOTES</span></span>

## <span data-ttu-id="41880-131">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="41880-131">RELATED LINKS</span></span>

[<span data-ttu-id="41880-132">New-WAPackStaticIPAddressPool</span><span class="sxs-lookup"><span data-stu-id="41880-132">New-WAPackStaticIPAddressPool</span></span>](./New-WAPackStaticIPAddressPool.md)

[<span data-ttu-id="41880-133">Remove-WAPackStaticIPAddressPool</span><span class="sxs-lookup"><span data-stu-id="41880-133">Remove-WAPackStaticIPAddressPool</span></span>](./Remove-WAPackStaticIPAddressPool.md)


