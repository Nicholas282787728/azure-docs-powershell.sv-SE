---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 3249E908-B1D9-4707-844D-168274F1A466
online version: ''
schema: 2.0.0
ms.openlocfilehash: ae16609adf70b2e5a0edcd05c36b30860a3920cf
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94099055"
---
# <span data-ttu-id="8c4e7-101">Set-AzureReservedIPAssociation</span><span class="sxs-lookup"><span data-stu-id="8c4e7-101">Set-AzureReservedIPAssociation</span></span>

## <span data-ttu-id="8c4e7-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="8c4e7-102">SYNOPSIS</span></span>
<span data-ttu-id="8c4e7-103">Associerar en reserverad IP-adress med en befintlig virtuell dator eller moln tjänst.</span><span class="sxs-lookup"><span data-stu-id="8c4e7-103">Associates a reserved IP address with an existing virtual machine or cloud service.</span></span>

## <span data-ttu-id="8c4e7-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="8c4e7-104">SYNTAX</span></span>

```
Set-AzureReservedIPAssociation [-ReservedIPName] <String> [-ServiceName] <String> [[-VirtualIPName] <String>]
 [[-Slot] <String>] [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="8c4e7-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="8c4e7-105">DESCRIPTION</span></span>
<span data-ttu-id="8c4e7-106">Cmdleten **set-AzureReservedIPAssociation** associerar en reserverad IP-adress med den virtuella IP-adressen (VIP) för en virtuell dator eller moln tjänst som körs.</span><span class="sxs-lookup"><span data-stu-id="8c4e7-106">The **Set-AzureReservedIPAssociation** cmdlet associates a reserved IP address with the Virtual IP address (VIP) of a running virtual machine or cloud service.</span></span>
<span data-ttu-id="8c4e7-107">Den reserverade IP-adressen får inte användas när denna cmdlet anropas och måste finnas i samma område som den virtuella datorn eller moln tjänsten.</span><span class="sxs-lookup"><span data-stu-id="8c4e7-107">The reserved IP address must not be in use at the time of invocation of this cmdlet, and must be in the same region as the virtual machine or cloud service.</span></span>

<span data-ttu-id="8c4e7-108">Åtgärden tar ungefär 30 sekunder att slutföra och sedan kan den virtuella datorn eller tjänsten nås via den reserverade IP-adressen.</span><span class="sxs-lookup"><span data-stu-id="8c4e7-108">The operation takes about 30 seconds to complete, after which the virtual machine or service is accessible using the reserved IP address.</span></span>

## <span data-ttu-id="8c4e7-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="8c4e7-109">EXAMPLES</span></span>

### <span data-ttu-id="8c4e7-110">Exempel 1: Ange en reserverad IP-associering</span><span class="sxs-lookup"><span data-stu-id="8c4e7-110">Example 1: Set a reserved IP association</span></span>
```
PS C:\> Set-AzureReservedIPAssociation -ReservedIPName "ResIp14" -ServiceName "PipTestWestEurope"
```

<span data-ttu-id="8c4e7-111">Det här kommandot tilldelar den reserverade IP-adressen som heter ResIp14 till tjänsten PipTestWestEurope.</span><span class="sxs-lookup"><span data-stu-id="8c4e7-111">This command assigns the reserved IP address named ResIp14 to the service PipTestWestEurope.</span></span>
<span data-ttu-id="8c4e7-112">ResIp14 är en reserverad IP i regionen Västeuropa.</span><span class="sxs-lookup"><span data-stu-id="8c4e7-112">ResIp14 is a reserved IP in the West Europe region.</span></span>

## <span data-ttu-id="8c4e7-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="8c4e7-113">PARAMETERS</span></span>

### <span data-ttu-id="8c4e7-114">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="8c4e7-114">-InformationAction</span></span>
<span data-ttu-id="8c4e7-115">Anger hur den här cmdleten svarar på en informations händelse.</span><span class="sxs-lookup"><span data-stu-id="8c4e7-115">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="8c4e7-116">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="8c4e7-116">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="8c4e7-117">Vidare</span><span class="sxs-lookup"><span data-stu-id="8c4e7-117">Continue</span></span>
- <span data-ttu-id="8c4e7-118">Över</span><span class="sxs-lookup"><span data-stu-id="8c4e7-118">Ignore</span></span>
- <span data-ttu-id="8c4e7-119">Inquire</span><span class="sxs-lookup"><span data-stu-id="8c4e7-119">Inquire</span></span>
- <span data-ttu-id="8c4e7-120">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="8c4e7-120">SilentlyContinue</span></span>
- <span data-ttu-id="8c4e7-121">Stanna</span><span class="sxs-lookup"><span data-stu-id="8c4e7-121">Stop</span></span>
- <span data-ttu-id="8c4e7-122">Avbryt</span><span class="sxs-lookup"><span data-stu-id="8c4e7-122">Suspend</span></span>

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

### <span data-ttu-id="8c4e7-123">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="8c4e7-123">-InformationVariable</span></span>
<span data-ttu-id="8c4e7-124">Anger en informations variabel.</span><span class="sxs-lookup"><span data-stu-id="8c4e7-124">Specifies an information variable.</span></span>

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

### <span data-ttu-id="8c4e7-125">-Profil</span><span class="sxs-lookup"><span data-stu-id="8c4e7-125">-Profile</span></span>
<span data-ttu-id="8c4e7-126">Anger den Azure-profil från vilken denna cmdlet läser.</span><span class="sxs-lookup"><span data-stu-id="8c4e7-126">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="8c4e7-127">Om du inte anger en profil läser denna cmdlet från den lokala standard profilen.</span><span class="sxs-lookup"><span data-stu-id="8c4e7-127">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="8c4e7-128">-ReservedIPName</span><span class="sxs-lookup"><span data-stu-id="8c4e7-128">-ReservedIPName</span></span>
<span data-ttu-id="8c4e7-129">Anger namnet på den reserverade IP-adressen som ska kopplas till en virtuell dator eller tjänst.</span><span class="sxs-lookup"><span data-stu-id="8c4e7-129">Specifies the name of the reserved IP address to associate with a virtual machine or service.</span></span>

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

### <span data-ttu-id="8c4e7-130">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="8c4e7-130">-ServiceName</span></span>
<span data-ttu-id="8c4e7-131">Anger namnet på den tjänst som har den distribution som ska kopplas till den reserverade IP-adressen.</span><span class="sxs-lookup"><span data-stu-id="8c4e7-131">Specifies the name of the service that has the deployment with which to associate the reserved IP address.</span></span>

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

### <span data-ttu-id="8c4e7-132">-Plats</span><span class="sxs-lookup"><span data-stu-id="8c4e7-132">-Slot</span></span>
<span data-ttu-id="8c4e7-133">Anger distributions platsen.</span><span class="sxs-lookup"><span data-stu-id="8c4e7-133">Specifies the deployment slot.</span></span>
<span data-ttu-id="8c4e7-134">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="8c4e7-134">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="8c4e7-135">Lagring</span><span class="sxs-lookup"><span data-stu-id="8c4e7-135">Staging</span></span>
- <span data-ttu-id="8c4e7-136">Produktionsoperationsföljden</span><span class="sxs-lookup"><span data-stu-id="8c4e7-136">Production</span></span>

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

### <span data-ttu-id="8c4e7-137">-VirtualIPName</span><span class="sxs-lookup"><span data-stu-id="8c4e7-137">-VirtualIPName</span></span>
<span data-ttu-id="8c4e7-138">Anger namnet på en befintlig VIP-adress som ska kopplas till en reserverad IP.</span><span class="sxs-lookup"><span data-stu-id="8c4e7-138">Specifies the name of an existing VIP to associate with a reserved IP.</span></span>
<span data-ttu-id="8c4e7-139">Se Add-AzureVirtualIP för att lägga till VIP i din moln tjänst.</span><span class="sxs-lookup"><span data-stu-id="8c4e7-139">See Add-AzureVirtualIP to add VIPs to your cloud service.</span></span>

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

### <span data-ttu-id="8c4e7-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8c4e7-140">CommonParameters</span></span>
<span data-ttu-id="8c4e7-141">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8c4e7-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8c4e7-142">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8c4e7-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8c4e7-143">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="8c4e7-143">INPUTS</span></span>

## <span data-ttu-id="8c4e7-144">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="8c4e7-144">OUTPUTS</span></span>

### <span data-ttu-id="8c4e7-145">Microsoft. WindowsAzure. commands. Utilitiess. Common. ManagementOperationContext</span><span class="sxs-lookup"><span data-stu-id="8c4e7-145">Microsoft.WindowsAzure.Commands.Utilities.Common.ManagementOperationContext</span></span>

## <span data-ttu-id="8c4e7-146">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="8c4e7-146">NOTES</span></span>

## <span data-ttu-id="8c4e7-147">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="8c4e7-147">RELATED LINKS</span></span>

[<span data-ttu-id="8c4e7-148">Remove-AzureReservedIPAssociation</span><span class="sxs-lookup"><span data-stu-id="8c4e7-148">Remove-AzureReservedIPAssociation</span></span>](./Remove-AzureReservedIPAssociation.md)


