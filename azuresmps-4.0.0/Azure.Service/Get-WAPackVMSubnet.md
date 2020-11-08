---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 0E358CEF-69E4-4639-918C-CE593E97B189
online version: ''
schema: 2.0.0
ms.openlocfilehash: d534a1734a49739db648558e8d7e62b22e43d561
ms.sourcegitcommit: 3d16496984a0b9fd7631aa043726060ddae3624d
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/08/2020
ms.locfileid: "94100585"
---
# <span data-ttu-id="4dc0a-101">Get-WAPackVMSubnet</span><span class="sxs-lookup"><span data-stu-id="4dc0a-101">Get-WAPackVMSubnet</span></span>

## <span data-ttu-id="4dc0a-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="4dc0a-102">SYNOPSIS</span></span>
<span data-ttu-id="4dc0a-103">Hämtar undernät för virtuella datorer.</span><span class="sxs-lookup"><span data-stu-id="4dc0a-103">Gets virtual machine subnet objects.</span></span>

## <span data-ttu-id="4dc0a-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="4dc0a-104">SYNTAX</span></span>

### <span data-ttu-id="4dc0a-105">FromVMNetworkObject (standard)</span><span class="sxs-lookup"><span data-stu-id="4dc0a-105">FromVMNetworkObject (Default)</span></span>
```
Get-WAPackVMSubnet -VNet <VMNetwork> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="4dc0a-106">FromName</span><span class="sxs-lookup"><span data-stu-id="4dc0a-106">FromName</span></span>
```
Get-WAPackVMSubnet -VNet <VMNetwork> -Name <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="4dc0a-107">FromId</span><span class="sxs-lookup"><span data-stu-id="4dc0a-107">FromId</span></span>
```
Get-WAPackVMSubnet -VNet <VMNetwork> -ID <Guid> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="4dc0a-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="4dc0a-108">DESCRIPTION</span></span>
<span data-ttu-id="4dc0a-109">De här ämnena är föråldrade och kommer att tas bort i framtiden.</span><span class="sxs-lookup"><span data-stu-id="4dc0a-109">These topics are deprecated and will be removed in the future.</span></span>
<span data-ttu-id="4dc0a-110">I det här avsnittet beskrivs cmdleten i 0.8.1-versionen av Microsoft Azure PowerShell-modulen.</span><span class="sxs-lookup"><span data-stu-id="4dc0a-110">This topic describes the cmdlet in the 0.8.1 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="4dc0a-111">För att ta reda på vilken version av modulen du använder, går du till Azure PowerShell-konsolen och skriver `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="4dc0a-111">To find out the version of the module you're using, from the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="4dc0a-112">Cmdleten **Get-WAPackVMSubnet** hämtar objekt för virtuella datorer.</span><span class="sxs-lookup"><span data-stu-id="4dc0a-112">The **Get-WAPackVMSubnet** cmdlet gets virtual machine subnet objects.</span></span>

## <span data-ttu-id="4dc0a-113">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="4dc0a-113">EXAMPLES</span></span>

### <span data-ttu-id="4dc0a-114">Exempel 1: Hämta ett virtuellt dator nät genom att använda ett namn</span><span class="sxs-lookup"><span data-stu-id="4dc0a-114">Example 1: Get a virtual machine subnet by using a name</span></span>
```
PS C:\> $VNet = Get-WAPackVNet -Name "ContosoVNet01"
PS C:\> Get-WAPackVMTemplate -VNet $VNet -Name "ContosoSubnet01"
```

<span data-ttu-id="4dc0a-115">Det här kommandot får det virtuella dator under nätet med namnet ContosoSubnet01.</span><span class="sxs-lookup"><span data-stu-id="4dc0a-115">This command gets the virtual machine subnet named ContosoSubnet01.</span></span>

### <span data-ttu-id="4dc0a-116">Exempel 2: Hämta ett undernät för virtuell dator med hjälp av ett ID</span><span class="sxs-lookup"><span data-stu-id="4dc0a-116">Example 2: Get a virtual machine subnet by using an ID</span></span>
```
PS C:\> $VNet = Get-WAPackVNet -Name "ContosoVNet01"
PS C:\> Get-WAPackVMSubnet -VNet $VNet -Id 66242D17-189F-480D-87CF-8E1D749998C8
```

<span data-ttu-id="4dc0a-117">Det här kommandot får det virtuella dator under nätet med angivet ID.</span><span class="sxs-lookup"><span data-stu-id="4dc0a-117">This command gets the virtual machine subnet that has the specified ID.</span></span>

### <span data-ttu-id="4dc0a-118">Exempel 3: Hämta alla virtuella dator under nätverk från ett angivet virtualiserat nätverk</span><span class="sxs-lookup"><span data-stu-id="4dc0a-118">Example 3: Get all virtual machine subnets from a given virtualized network</span></span>
```
PS C:\> $VNet = Get-WAPackVNet -Name "ContosoVNet01"
PS C:\> Get-WAPackVMSubnet -VNet $VNet
```

<span data-ttu-id="4dc0a-119">Det här kommandot får alla virtuella dator nät från ett visst virtualiserat nätverk.</span><span class="sxs-lookup"><span data-stu-id="4dc0a-119">This command gets all the virtual machine subnets from a given virtualized network.</span></span>

## <span data-ttu-id="4dc0a-120">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="4dc0a-120">PARAMETERS</span></span>

### <span data-ttu-id="4dc0a-121">-ID</span><span class="sxs-lookup"><span data-stu-id="4dc0a-121">-ID</span></span>
<span data-ttu-id="4dc0a-122">Anger unikt ID för ett undernät för en virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="4dc0a-122">Specifies the unique ID of a virtual machine subnet.</span></span>

```yaml
Type: Guid
Parameter Sets: FromId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4dc0a-123">-Namn</span><span class="sxs-lookup"><span data-stu-id="4dc0a-123">-Name</span></span>
<span data-ttu-id="4dc0a-124">Anger namnet på en virtuell dator under nät.</span><span class="sxs-lookup"><span data-stu-id="4dc0a-124">Specifies the name of a virtual machine subnet.</span></span>

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

### <span data-ttu-id="4dc0a-125">-Profil</span><span class="sxs-lookup"><span data-stu-id="4dc0a-125">-Profile</span></span>
<span data-ttu-id="4dc0a-126">Anger den Azure-profil från vilken denna cmdlet läser.</span><span class="sxs-lookup"><span data-stu-id="4dc0a-126">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="4dc0a-127">Om du inte anger en profil läser denna cmdlet från den lokala standard profilen.</span><span class="sxs-lookup"><span data-stu-id="4dc0a-127">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="4dc0a-128">-VNet</span><span class="sxs-lookup"><span data-stu-id="4dc0a-128">-VNet</span></span>
<span data-ttu-id="4dc0a-129">Anger det VNet som är kopplat till ett virtuellt dator nät.</span><span class="sxs-lookup"><span data-stu-id="4dc0a-129">Specifies the VNet associated with a virtual machine subnet.</span></span>

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

### <span data-ttu-id="4dc0a-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4dc0a-130">CommonParameters</span></span>
<span data-ttu-id="4dc0a-131">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4dc0a-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4dc0a-132">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4dc0a-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4dc0a-133">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="4dc0a-133">INPUTS</span></span>

## <span data-ttu-id="4dc0a-134">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="4dc0a-134">OUTPUTS</span></span>

## <span data-ttu-id="4dc0a-135">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="4dc0a-135">NOTES</span></span>

## <span data-ttu-id="4dc0a-136">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="4dc0a-136">RELATED LINKS</span></span>

[<span data-ttu-id="4dc0a-137">Get-WAPackVNet</span><span class="sxs-lookup"><span data-stu-id="4dc0a-137">Get-WAPackVNet</span></span>](./Get-WAPackVNet.md)

[<span data-ttu-id="4dc0a-138">New-WAPackVMSubnet</span><span class="sxs-lookup"><span data-stu-id="4dc0a-138">New-WAPackVMSubnet</span></span>](./New-WAPackVMSubnet.md)

[<span data-ttu-id="4dc0a-139">Remove-WAPackVMSubnet</span><span class="sxs-lookup"><span data-stu-id="4dc0a-139">Remove-WAPackVMSubnet</span></span>](./Remove-WAPackVMSubnet.md)


