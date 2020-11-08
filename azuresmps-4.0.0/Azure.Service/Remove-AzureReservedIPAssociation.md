---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: A6964C80-1991-46FC-84C8-5B00616386BE
online version: ''
schema: 2.0.0
ms.openlocfilehash: 9e43f841fea77626c18edbda541fa011e95faceb
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94099366"
---
# <span data-ttu-id="6b2d3-101">Remove-AzureReservedIPAssociation</span><span class="sxs-lookup"><span data-stu-id="6b2d3-101">Remove-AzureReservedIPAssociation</span></span>

## <span data-ttu-id="6b2d3-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="6b2d3-102">SYNOPSIS</span></span>
<span data-ttu-id="6b2d3-103">Tar bort associationen från den reserverade IP-adressen till VM eller moln tjänsten.</span><span class="sxs-lookup"><span data-stu-id="6b2d3-103">Removes the association from the reserved IP address to the VM or cloud service.</span></span>

## <span data-ttu-id="6b2d3-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="6b2d3-104">SYNTAX</span></span>

```
Remove-AzureReservedIPAssociation [-ReservedIPName] <String> [-ServiceName] <String>
 [[-VirtualIPName] <String>] [[-Slot] <String>] [-Force] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="6b2d3-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="6b2d3-105">DESCRIPTION</span></span>
<span data-ttu-id="6b2d3-106">Cmdleten **Remove-AzureReservedIPAssociation** avassocierar en reserverad IP-adress från en virtuell dator eller moln tjänst.</span><span class="sxs-lookup"><span data-stu-id="6b2d3-106">The **Remove-AzureReservedIPAssociation** cmdlet disassociates a reserved IP address from a virtual machine (VM) or Cloud Service.</span></span>
<span data-ttu-id="6b2d3-107">När åtgärden är slutförd är den reserverade IP-adressen kostnads fri och virtuell dator/VIP får en dynamisk offentlig IP-adress från Azure Inventory.</span><span class="sxs-lookup"><span data-stu-id="6b2d3-107">When the operation completes, the reserved IP address is free and the VM/VIP gets a dynamic public IP Address from the Azure Inventory.</span></span>

## <span data-ttu-id="6b2d3-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="6b2d3-108">EXAMPLES</span></span>

### <span data-ttu-id="6b2d3-109">Exempel 1: ta bort en reserverad IP-associering</span><span class="sxs-lookup"><span data-stu-id="6b2d3-109">Example 1: Remove a reserved IP association</span></span>
```
PS C:\> Remove-AzureReservedIPAssociation -ReservedIPName "ResIp14" -ServiceName "PipTestWestEurope"
```

<span data-ttu-id="6b2d3-110">Det här kommandot avassocierar den reserverade IP-adressen som heter ResIp14 från tjänsten PipTestWestEurope.</span><span class="sxs-lookup"><span data-stu-id="6b2d3-110">This command disassociates the reserved IP address named ResIp14 from the service named PipTestWestEurope.</span></span>
<span data-ttu-id="6b2d3-111">PipTestWestEurope tilldelas en ny dynamisk VIP.</span><span class="sxs-lookup"><span data-stu-id="6b2d3-111">PipTestWestEurope will be assigned a new dynamic VIP.</span></span>

## <span data-ttu-id="6b2d3-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="6b2d3-112">PARAMETERS</span></span>

### <span data-ttu-id="6b2d3-113">-Force</span><span class="sxs-lookup"><span data-stu-id="6b2d3-113">-Force</span></span>
<span data-ttu-id="6b2d3-114">Tvingar kommandot att köras utan att fråga efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="6b2d3-114">Forces the command to run without asking for user confirmation.</span></span>

<span data-ttu-id="6b2d3-115">Använd den här flaggan för att förbigå varnings meddelanden när du tar bort den reserverade IP-associeringen.</span><span class="sxs-lookup"><span data-stu-id="6b2d3-115">Use this flag to bypass warning messages when removing the reserved IP association.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6b2d3-116">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="6b2d3-116">-InformationAction</span></span>
<span data-ttu-id="6b2d3-117">Anger hur den här cmdleten svarar på en informations händelse.</span><span class="sxs-lookup"><span data-stu-id="6b2d3-117">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="6b2d3-118">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="6b2d3-118">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="6b2d3-119">Vidare</span><span class="sxs-lookup"><span data-stu-id="6b2d3-119">Continue</span></span>
- <span data-ttu-id="6b2d3-120">Över</span><span class="sxs-lookup"><span data-stu-id="6b2d3-120">Ignore</span></span>
- <span data-ttu-id="6b2d3-121">Inquire</span><span class="sxs-lookup"><span data-stu-id="6b2d3-121">Inquire</span></span>
- <span data-ttu-id="6b2d3-122">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="6b2d3-122">SilentlyContinue</span></span>
- <span data-ttu-id="6b2d3-123">Stanna</span><span class="sxs-lookup"><span data-stu-id="6b2d3-123">Stop</span></span>
- <span data-ttu-id="6b2d3-124">Avbryt</span><span class="sxs-lookup"><span data-stu-id="6b2d3-124">Suspend</span></span>

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

### <span data-ttu-id="6b2d3-125">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="6b2d3-125">-InformationVariable</span></span>
<span data-ttu-id="6b2d3-126">Anger en informations variabel.</span><span class="sxs-lookup"><span data-stu-id="6b2d3-126">Specifies an information variable.</span></span>

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

### <span data-ttu-id="6b2d3-127">-Profil</span><span class="sxs-lookup"><span data-stu-id="6b2d3-127">-Profile</span></span>
<span data-ttu-id="6b2d3-128">Anger den Azure-profil från vilken denna cmdlet läser.</span><span class="sxs-lookup"><span data-stu-id="6b2d3-128">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="6b2d3-129">Om du inte anger en profil läser denna cmdlet från den lokala standard profilen.</span><span class="sxs-lookup"><span data-stu-id="6b2d3-129">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="6b2d3-130">-ReservedIPName</span><span class="sxs-lookup"><span data-stu-id="6b2d3-130">-ReservedIPName</span></span>
<span data-ttu-id="6b2d3-131">Anger namnet på den reserverade IP-adressen.</span><span class="sxs-lookup"><span data-stu-id="6b2d3-131">Specifies the name of the reserved IP address.</span></span>

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

### <span data-ttu-id="6b2d3-132">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="6b2d3-132">-ServiceName</span></span>
<span data-ttu-id="6b2d3-133">Anger namnet på tjänsten.</span><span class="sxs-lookup"><span data-stu-id="6b2d3-133">Specifies the  name of the service.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6b2d3-134">-Plats</span><span class="sxs-lookup"><span data-stu-id="6b2d3-134">-Slot</span></span>
<span data-ttu-id="6b2d3-135">Anger distributions miljön.</span><span class="sxs-lookup"><span data-stu-id="6b2d3-135">Specifies the deployment environment.</span></span>
<span data-ttu-id="6b2d3-136">De acceptabla värdena för den här parametern är: produktion, mellanlagring.</span><span class="sxs-lookup"><span data-stu-id="6b2d3-136">The acceptable values for this parameter are: Production, Staging.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6b2d3-137">-VirtualIPName</span><span class="sxs-lookup"><span data-stu-id="6b2d3-137">-VirtualIPName</span></span>
<span data-ttu-id="6b2d3-138">Anger en virtuell IP-adress som du vill ta bort associeringen från med en tjänst eller VM.</span><span class="sxs-lookup"><span data-stu-id="6b2d3-138">Specifies a virtual IP address from which to remove the association with a service or VM.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6b2d3-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6b2d3-139">CommonParameters</span></span>
<span data-ttu-id="6b2d3-140">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6b2d3-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6b2d3-141">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6b2d3-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6b2d3-142">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="6b2d3-142">INPUTS</span></span>

## <span data-ttu-id="6b2d3-143">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="6b2d3-143">OUTPUTS</span></span>

### <span data-ttu-id="6b2d3-144">Microsoft. WindowsAzure. commands. Utilitiess. Common. ManagementOperationContext</span><span class="sxs-lookup"><span data-stu-id="6b2d3-144">Microsoft.WindowsAzure.Commands.Utilities.Common.ManagementOperationContext</span></span>

## <span data-ttu-id="6b2d3-145">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="6b2d3-145">NOTES</span></span>

## <span data-ttu-id="6b2d3-146">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="6b2d3-146">RELATED LINKS</span></span>

[<span data-ttu-id="6b2d3-147">Set-AzureReservedIPAssociation</span><span class="sxs-lookup"><span data-stu-id="6b2d3-147">Set-AzureReservedIPAssociation</span></span>](./Set-AzureReservedIPAssociation.md)


