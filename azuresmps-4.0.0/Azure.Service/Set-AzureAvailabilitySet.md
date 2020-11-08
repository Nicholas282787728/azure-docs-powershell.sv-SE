---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: E0590AD4-F67B-48EF-8657-8890A2204CB6
online version: ''
schema: 2.0.0
ms.openlocfilehash: 607cd288bcc9c86209a3ae0af569e964205f5cb4
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94099297"
---
# <span data-ttu-id="44d82-101">Set-AzureAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="44d82-101">Set-AzureAvailabilitySet</span></span>

## <span data-ttu-id="44d82-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="44d82-102">SYNOPSIS</span></span>
<span data-ttu-id="44d82-103">Anger namnet på tillgänglighets uppsättningen på en virtuell Azure-dator.</span><span class="sxs-lookup"><span data-stu-id="44d82-103">Sets the name of the availability set on an Azure virtual machine.</span></span>

## <span data-ttu-id="44d82-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="44d82-104">SYNTAX</span></span>

```
Set-AzureAvailabilitySet [-AvailabilitySetName] <String> -VM <IPersistentVM> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="44d82-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="44d82-105">DESCRIPTION</span></span>
<span data-ttu-id="44d82-106">Cmdleten **set-AzureAvailabilitySet** anger namnet på tillgänglighets uppsättningen på en virtuell Azure-dator efter distributionen.</span><span class="sxs-lookup"><span data-stu-id="44d82-106">The **Set-AzureAvailabilitySet** cmdlet sets the name of the availability set on an Azure virtual machine after deployment.</span></span>

## <span data-ttu-id="44d82-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="44d82-107">EXAMPLES</span></span>

### <span data-ttu-id="44d82-108">Exempel 1: ändra namnet på en tillgänglighets uppsättning</span><span class="sxs-lookup"><span data-stu-id="44d82-108">Example 1: Modify the name of an availability set</span></span>
```
PS C:\> Get-AzureVM -ServiceName "ContosoService" -Name "VirtualMachine24" | Set-AzureAvailabilitySet -AvailabilitySetName "AvailabilitySet14" | Update-AzureVM
```

<span data-ttu-id="44d82-109">Det första kommandot får den virtuella datorn som heter VirtualMachine07 i tjänsten ContosoService med hjälp av cmdleten **Get-AzureVM** .</span><span class="sxs-lookup"><span data-stu-id="44d82-109">The first command gets the virtual machine named VirtualMachine07 in the service named ContosoService by using the **Get-AzureVM** cmdlet.</span></span>
<span data-ttu-id="44d82-110">Kommandot skickar detta objekt till den aktuella cmdleten med hjälp av pipeline-operatorn.</span><span class="sxs-lookup"><span data-stu-id="44d82-110">The command passes that object to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="44d82-111">Denna cmdlet ändrar namnet på tillgänglighets uppsättningen för den virtuella datorn.</span><span class="sxs-lookup"><span data-stu-id="44d82-111">That cmdlet modifies the name of the availability set for that virtual machine.</span></span>
<span data-ttu-id="44d82-112">Kommandot uppdaterar den virtuella datorn.</span><span class="sxs-lookup"><span data-stu-id="44d82-112">The command updates the virtual machine.</span></span>

## <span data-ttu-id="44d82-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="44d82-113">PARAMETERS</span></span>

### <span data-ttu-id="44d82-114">-AvailabilitySetName</span><span class="sxs-lookup"><span data-stu-id="44d82-114">-AvailabilitySetName</span></span>
<span data-ttu-id="44d82-115">Anger namnet på den tillgänglighets uppsättning som den virtuella datorn tillhör.</span><span class="sxs-lookup"><span data-stu-id="44d82-115">Specifies the name of the availability set to which the virtual machine belongs.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="44d82-116">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="44d82-116">-InformationAction</span></span>
<span data-ttu-id="44d82-117">Anger hur den här cmdleten svarar på en informations händelse.</span><span class="sxs-lookup"><span data-stu-id="44d82-117">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="44d82-118">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="44d82-118">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="44d82-119">Vidare</span><span class="sxs-lookup"><span data-stu-id="44d82-119">Continue</span></span>
- <span data-ttu-id="44d82-120">Över</span><span class="sxs-lookup"><span data-stu-id="44d82-120">Ignore</span></span>
- <span data-ttu-id="44d82-121">Inquire</span><span class="sxs-lookup"><span data-stu-id="44d82-121">Inquire</span></span>
- <span data-ttu-id="44d82-122">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="44d82-122">SilentlyContinue</span></span>
- <span data-ttu-id="44d82-123">Stanna</span><span class="sxs-lookup"><span data-stu-id="44d82-123">Stop</span></span>
- <span data-ttu-id="44d82-124">Avbryt</span><span class="sxs-lookup"><span data-stu-id="44d82-124">Suspend</span></span>

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

### <span data-ttu-id="44d82-125">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="44d82-125">-InformationVariable</span></span>
<span data-ttu-id="44d82-126">Anger en informations variabel.</span><span class="sxs-lookup"><span data-stu-id="44d82-126">Specifies an information variable.</span></span>

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

### <span data-ttu-id="44d82-127">-Profil</span><span class="sxs-lookup"><span data-stu-id="44d82-127">-Profile</span></span>
<span data-ttu-id="44d82-128">Anger den Azure-profil från vilken denna cmdlet läser.</span><span class="sxs-lookup"><span data-stu-id="44d82-128">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="44d82-129">Om du inte anger en profil läser denna cmdlet från den lokala standard profilen.</span><span class="sxs-lookup"><span data-stu-id="44d82-129">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="44d82-130">-VM</span><span class="sxs-lookup"><span data-stu-id="44d82-130">-VM</span></span>
<span data-ttu-id="44d82-131">Anger den virtuella dator konfigurationen som denna cmdlet ändrar.</span><span class="sxs-lookup"><span data-stu-id="44d82-131">Specifies the virtual machine configuration that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="44d82-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="44d82-132">CommonParameters</span></span>
<span data-ttu-id="44d82-133">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="44d82-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="44d82-134">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="44d82-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="44d82-135">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="44d82-135">INPUTS</span></span>

## <span data-ttu-id="44d82-136">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="44d82-136">OUTPUTS</span></span>

## <span data-ttu-id="44d82-137">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="44d82-137">NOTES</span></span>

## <span data-ttu-id="44d82-138">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="44d82-138">RELATED LINKS</span></span>

[<span data-ttu-id="44d82-139">Get-AzureVM</span><span class="sxs-lookup"><span data-stu-id="44d82-139">Get-AzureVM</span></span>](./Get-AzureVM.md)

[<span data-ttu-id="44d82-140">Remove-AzureAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="44d82-140">Remove-AzureAvailabilitySet</span></span>](./Remove-AzureAvailabilitySet.md)


