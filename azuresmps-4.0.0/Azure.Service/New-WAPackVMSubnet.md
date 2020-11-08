---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 83D18A17-94A4-4FB8-9DA6-F652D5BB84C7
online version: ''
schema: 2.0.0
ms.openlocfilehash: bf06561ac5f8c9e0c19edb88b7a8ff5ef816c609
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94099116"
---
# <span data-ttu-id="13ec3-101">New-WAPackVMSubnet</span><span class="sxs-lookup"><span data-stu-id="13ec3-101">New-WAPackVMSubnet</span></span>

## <span data-ttu-id="13ec3-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="13ec3-102">SYNOPSIS</span></span>
<span data-ttu-id="13ec3-103">Skapar ett undernät för virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="13ec3-103">Creates a virtual machine subnet.</span></span>

## <span data-ttu-id="13ec3-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="13ec3-104">SYNTAX</span></span>

```
New-WAPackVMSubnet -VNet <VMNetwork> -Name <String> -Subnet <String> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="13ec3-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="13ec3-105">DESCRIPTION</span></span>
<span data-ttu-id="13ec3-106">Cmdleten **New-WAPackVMSubnet** skapar ett undernät för virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="13ec3-106">The **New-WAPackVMSubnet** cmdlet creates a virtual machine subnet.</span></span>

## <span data-ttu-id="13ec3-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="13ec3-107">EXAMPLES</span></span>

### <span data-ttu-id="13ec3-108">Exempel 1: skapa ett undernät för virtuell dator</span><span class="sxs-lookup"><span data-stu-id="13ec3-108">Example 1: Create a virtual machine subnet</span></span>
```
PS C:\> $VNet = Get-WAPackVNet -Name "ContosoVNet01"
PS C:\> New-WAPackVMSubnet -VNet $VNet -Name "ContosoVMSubnet01" -Subnet "192.168.1.0/24"
```

<span data-ttu-id="13ec3-109">Första kommandot hämtar först det virtuella dator nätverk som vi vill lägga till en ny virtuell dator under nät.</span><span class="sxs-lookup"><span data-stu-id="13ec3-109">The first command first retrieves the virtual machine network to which we want to add a new virtual machine subnet.</span></span>
<span data-ttu-id="13ec3-110">Det här virtuella dator nätverket heter ContosoVNet01.</span><span class="sxs-lookup"><span data-stu-id="13ec3-110">This virtual machine network is named ContosoVNet01.</span></span>

<span data-ttu-id="13ec3-111">Det andra kommandot skapar ett virtuellt dator nät med hjälp av det tidigare Hämta virtuella dator nätverket, ett namn ContosoVMSubnet01 och en under näts 192.168.1.0/24.</span><span class="sxs-lookup"><span data-stu-id="13ec3-111">The second command creates a virtual machine subnet using the previously retrieve virtual machine network, a name ContosoVMSubnet01 and a subnet 192.168.1.0/24.</span></span>

## <span data-ttu-id="13ec3-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="13ec3-112">PARAMETERS</span></span>

### <span data-ttu-id="13ec3-113">-Namn</span><span class="sxs-lookup"><span data-stu-id="13ec3-113">-Name</span></span>
<span data-ttu-id="13ec3-114">Anger ett namn för det virtuella dator nätet.</span><span class="sxs-lookup"><span data-stu-id="13ec3-114">Specifies a name for the virtual machine subnet.</span></span>

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

### <span data-ttu-id="13ec3-115">-Profil</span><span class="sxs-lookup"><span data-stu-id="13ec3-115">-Profile</span></span>
<span data-ttu-id="13ec3-116">Anger den Azure-profil från vilken denna cmdlet läser.</span><span class="sxs-lookup"><span data-stu-id="13ec3-116">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="13ec3-117">Om du inte anger en profil läser denna cmdlet från den lokala standard profilen.</span><span class="sxs-lookup"><span data-stu-id="13ec3-117">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="13ec3-118">-Undernät</span><span class="sxs-lookup"><span data-stu-id="13ec3-118">-Subnet</span></span>
<span data-ttu-id="13ec3-119">Anger ett undernät för det virtuella dator under nätet.</span><span class="sxs-lookup"><span data-stu-id="13ec3-119">Specifies a subnet for the virtual machine subnet.</span></span>

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

### <span data-ttu-id="13ec3-120">-VNet</span><span class="sxs-lookup"><span data-stu-id="13ec3-120">-VNet</span></span>
<span data-ttu-id="13ec3-121">Anger ett VNet som är kopplat till det virtuella dator nätet.</span><span class="sxs-lookup"><span data-stu-id="13ec3-121">Specifies a VNet associated with the virtual machine subnet.</span></span>

```yaml
Type: VMNetwork
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="13ec3-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="13ec3-122">CommonParameters</span></span>
<span data-ttu-id="13ec3-123">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="13ec3-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="13ec3-124">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="13ec3-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="13ec3-125">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="13ec3-125">INPUTS</span></span>

## <span data-ttu-id="13ec3-126">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="13ec3-126">OUTPUTS</span></span>

## <span data-ttu-id="13ec3-127">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="13ec3-127">NOTES</span></span>

## <span data-ttu-id="13ec3-128">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="13ec3-128">RELATED LINKS</span></span>

[<span data-ttu-id="13ec3-129">Get-WAPackVMSubnet</span><span class="sxs-lookup"><span data-stu-id="13ec3-129">Get-WAPackVMSubnet</span></span>](./Get-WAPackVMSubnet.md)

[<span data-ttu-id="13ec3-130">Get-WAPackVNet</span><span class="sxs-lookup"><span data-stu-id="13ec3-130">Get-WAPackVNet</span></span>](./Get-WAPackVNet.md)

[<span data-ttu-id="13ec3-131">Remove-WAPackVMSubnet</span><span class="sxs-lookup"><span data-stu-id="13ec3-131">Remove-WAPackVMSubnet</span></span>](./Remove-WAPackVMSubnet.md)


