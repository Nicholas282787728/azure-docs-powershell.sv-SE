---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 9C22F5D7-1FD0-4699-83D7-1D72C5234DEF
online version: ''
schema: 2.0.0
ms.openlocfilehash: d09173c43de9c01056055f714217db5eb4c58225
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94099223"
---
# <span data-ttu-id="01cd6-101">New-AzureReservedIP</span><span class="sxs-lookup"><span data-stu-id="01cd6-101">New-AzureReservedIP</span></span>

## <span data-ttu-id="01cd6-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="01cd6-102">SYNOPSIS</span></span>
<span data-ttu-id="01cd6-103">Skapar en reserverad IP-adress.</span><span class="sxs-lookup"><span data-stu-id="01cd6-103">Creates a reserved IP address.</span></span>

## <span data-ttu-id="01cd6-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="01cd6-104">SYNTAX</span></span>

### <span data-ttu-id="01cd6-105">CreateNewReservedIP (standard)</span><span class="sxs-lookup"><span data-stu-id="01cd6-105">CreateNewReservedIP (Default)</span></span>
```
New-AzureReservedIP [-ReservedIPName] <String> [[-Label] <String>] [-Location] <String>
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

### <span data-ttu-id="01cd6-106">CreateInUseReservedIPUsingSlot</span><span class="sxs-lookup"><span data-stu-id="01cd6-106">CreateInUseReservedIPUsingSlot</span></span>
```
New-AzureReservedIP [-ReservedIPName] <String> [[-Label] <String>] [-Location] <String>
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

### <span data-ttu-id="01cd6-107">CreateInUseReservedIP</span><span class="sxs-lookup"><span data-stu-id="01cd6-107">CreateInUseReservedIP</span></span>
```
New-AzureReservedIP [-ReservedIPName] <String> [[-Label] <String>] [-Location] <String> [-ServiceName] <String>
 [[-VirtualIPName] <String>] [[-Slot] <String>] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="01cd6-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="01cd6-108">DESCRIPTION</span></span>
<span data-ttu-id="01cd6-109">Cmdleten **New-AzureReservedIP** skapar en reserverad IP-adress.</span><span class="sxs-lookup"><span data-stu-id="01cd6-109">The **New-AzureReservedIP** cmdlet creates a reserved IP address.</span></span>

## <span data-ttu-id="01cd6-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="01cd6-110">EXAMPLES</span></span>

### <span data-ttu-id="01cd6-111">Exempel 1: skapa en ny reserverad IP</span><span class="sxs-lookup"><span data-stu-id="01cd6-111">Example 1: Create a new reserved IP</span></span>
```
PS C:\> New-AzureReservedIP -ReservedIPName $Name -Label $Label -Location $Location
```

<span data-ttu-id="01cd6-112">Det här kommandot skapar en ny reserverad IP-adress i prenumerationen, som kan användas för att skapa moln tjänster som innehåller webben, arbetare och virtuella datorer.</span><span class="sxs-lookup"><span data-stu-id="01cd6-112">This command creates a new reserved IP address in the subscription, which can be used for creating cloud services that include Web, Worker, and Virtual Machines.</span></span>

### <span data-ttu-id="01cd6-113">Exempel 2: skapa en reserverad IP baserad på en befintlig IP-adress</span><span class="sxs-lookup"><span data-stu-id="01cd6-113">Example 2: Create a reserved IP based on an existing IP</span></span>
```
PS C:\> New-AzureReservedIP -ReservedIPName resip14 -Location "West Europe" -ServiceName piptestwesteurope
```

<span data-ttu-id="01cd6-114">Det här kommandot skapar en befintlig VIP (virtuell IP) för den angivna tjänsten.</span><span class="sxs-lookup"><span data-stu-id="01cd6-114">This command creates an existing VIP (Virtual IP) on the specified service.</span></span>

## <span data-ttu-id="01cd6-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="01cd6-115">PARAMETERS</span></span>

### <span data-ttu-id="01cd6-116">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="01cd6-116">-InformationAction</span></span>
<span data-ttu-id="01cd6-117">Anger hur den här cmdleten svarar på en informations händelse.</span><span class="sxs-lookup"><span data-stu-id="01cd6-117">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="01cd6-118">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="01cd6-118">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="01cd6-119">Vidare</span><span class="sxs-lookup"><span data-stu-id="01cd6-119">Continue</span></span>
- <span data-ttu-id="01cd6-120">Över</span><span class="sxs-lookup"><span data-stu-id="01cd6-120">Ignore</span></span>
- <span data-ttu-id="01cd6-121">Inquire</span><span class="sxs-lookup"><span data-stu-id="01cd6-121">Inquire</span></span>
- <span data-ttu-id="01cd6-122">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="01cd6-122">SilentlyContinue</span></span>
- <span data-ttu-id="01cd6-123">Stanna</span><span class="sxs-lookup"><span data-stu-id="01cd6-123">Stop</span></span>
- <span data-ttu-id="01cd6-124">Avbryt</span><span class="sxs-lookup"><span data-stu-id="01cd6-124">Suspend</span></span>

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

### <span data-ttu-id="01cd6-125">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="01cd6-125">-InformationVariable</span></span>
<span data-ttu-id="01cd6-126">Anger en informations variabel.</span><span class="sxs-lookup"><span data-stu-id="01cd6-126">Specifies an information variable.</span></span>

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

### <span data-ttu-id="01cd6-127">-Etikett</span><span class="sxs-lookup"><span data-stu-id="01cd6-127">-Label</span></span>
<span data-ttu-id="01cd6-128">Anger en etikett för den reserverade IP-adressen.</span><span class="sxs-lookup"><span data-stu-id="01cd6-128">Specifies a label for the reserved IP address.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="01cd6-129">-Plats</span><span class="sxs-lookup"><span data-stu-id="01cd6-129">-Location</span></span>
<span data-ttu-id="01cd6-130">Anger den plats där du vill skapa den reserverade IP-adressen.</span><span class="sxs-lookup"><span data-stu-id="01cd6-130">Specifies a location at which to create the reserved IP address.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="01cd6-131">-Profil</span><span class="sxs-lookup"><span data-stu-id="01cd6-131">-Profile</span></span>
<span data-ttu-id="01cd6-132">Anger den Azure-profil från vilken denna cmdlet läser.</span><span class="sxs-lookup"><span data-stu-id="01cd6-132">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="01cd6-133">Om du inte anger en profil läser denna cmdlet från den lokala standard profilen.</span><span class="sxs-lookup"><span data-stu-id="01cd6-133">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="01cd6-134">-ReservedIPName</span><span class="sxs-lookup"><span data-stu-id="01cd6-134">-ReservedIPName</span></span>
<span data-ttu-id="01cd6-135">Anger namnet på den reserverade IP-adressen.</span><span class="sxs-lookup"><span data-stu-id="01cd6-135">Specifies the reserved IP address name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="01cd6-136">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="01cd6-136">-ServiceName</span></span>
<span data-ttu-id="01cd6-137">Anger ett tjänst namn.</span><span class="sxs-lookup"><span data-stu-id="01cd6-137">Specifies a service name.</span></span>

```yaml
Type: String
Parameter Sets: CreateInUseReservedIP
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="01cd6-138">-Plats</span><span class="sxs-lookup"><span data-stu-id="01cd6-138">-Slot</span></span>
<span data-ttu-id="01cd6-139">Anger distributions platsen.</span><span class="sxs-lookup"><span data-stu-id="01cd6-139">Specifies the deployment slot.</span></span>
<span data-ttu-id="01cd6-140">De acceptabla värdena för den här parametern är: för produktion, produktion.</span><span class="sxs-lookup"><span data-stu-id="01cd6-140">The acceptable values for this parameter are: Staging, Production.</span></span>

```yaml
Type: String
Parameter Sets: CreateInUseReservedIP
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="01cd6-141">-VirtualIPName</span><span class="sxs-lookup"><span data-stu-id="01cd6-141">-VirtualIPName</span></span>
<span data-ttu-id="01cd6-142">Anger att denna cmdlet använder parametern **VirtualIPName** för att reservera en befintlig virtuell IP-adress (VIP) i distributionen.</span><span class="sxs-lookup"><span data-stu-id="01cd6-142">Specifies that this cmdlet uses the **VirtualIPName** parameter to reserve an existing virtual IP address (VIP) in your deployment.</span></span>
<span data-ttu-id="01cd6-143">Om den här parametern inte anges reserverar denna cmdlet en ny VIP.</span><span class="sxs-lookup"><span data-stu-id="01cd6-143">If this parameter is not specified, this cmdlet reserves a new VIP.</span></span>

```yaml
Type: String
Parameter Sets: CreateInUseReservedIP
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="01cd6-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="01cd6-144">CommonParameters</span></span>
<span data-ttu-id="01cd6-145">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="01cd6-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="01cd6-146">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="01cd6-146">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="01cd6-147">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="01cd6-147">INPUTS</span></span>

## <span data-ttu-id="01cd6-148">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="01cd6-148">OUTPUTS</span></span>

## <span data-ttu-id="01cd6-149">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="01cd6-149">NOTES</span></span>

## <span data-ttu-id="01cd6-150">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="01cd6-150">RELATED LINKS</span></span>

[<span data-ttu-id="01cd6-151">Get-AzureReservedIP</span><span class="sxs-lookup"><span data-stu-id="01cd6-151">Get-AzureReservedIP</span></span>](./Get-AzureReservedIP.md)

[<span data-ttu-id="01cd6-152">Remove-AzureReservedIP</span><span class="sxs-lookup"><span data-stu-id="01cd6-152">Remove-AzureReservedIP</span></span>](./Remove-AzureReservedIP.md)


