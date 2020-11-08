---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: B2C7E454-F38F-4139-ADA2-D1C59C03CC50
online version: ''
schema: 2.0.0
ms.openlocfilehash: efa519c380ffa78f44e8ac6edebda284a4ce3cd0
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94099661"
---
# <span data-ttu-id="d8646-101">Set-AzureAffinityGroup</span><span class="sxs-lookup"><span data-stu-id="d8646-101">Set-AzureAffinityGroup</span></span>

## <span data-ttu-id="d8646-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="d8646-102">SYNOPSIS</span></span>
<span data-ttu-id="d8646-103">Ändrar egenskaper för en tillhörighets grupp.</span><span class="sxs-lookup"><span data-stu-id="d8646-103">Modifies properties of an affinity group.</span></span>

## <span data-ttu-id="d8646-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="d8646-104">SYNTAX</span></span>

```
Set-AzureAffinityGroup [-Name] <String> -Label <String> [-Description <String>] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="d8646-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="d8646-105">DESCRIPTION</span></span>
<span data-ttu-id="d8646-106">Cmdleten **set-AzureAffinityGroup** ändrar egenskaper för en Azure tillhörighets grupp.</span><span class="sxs-lookup"><span data-stu-id="d8646-106">The **Set-AzureAffinityGroup** cmdlet modifies properties of an Azure affinity group.</span></span>
<span data-ttu-id="d8646-107">Du kan ändra etiketten och beskrivningen.</span><span class="sxs-lookup"><span data-stu-id="d8646-107">You can change the label and the description.</span></span>

## <span data-ttu-id="d8646-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="d8646-108">EXAMPLES</span></span>

### <span data-ttu-id="d8646-109">Exempel 1: ändra en tillhörighets grupp</span><span class="sxs-lookup"><span data-stu-id="d8646-109">Example 1: Modify an affinity group</span></span>
```
PS C:\> Set-AzureAffinityGroup -Name "South01" -Label "SouthUSProduction" -Description "Production applications for Southern US locations"
```

<span data-ttu-id="d8646-110">Det här kommandot ändrar etiketten för den tillhörighets grupp som heter South01 ska vara SouthUSProduction kommandot ändrar också beskrivningen.</span><span class="sxs-lookup"><span data-stu-id="d8646-110">This command modifies the label of the affinity group named South01 to be SouthUSProduction The command also modifies the description.</span></span>

## <span data-ttu-id="d8646-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="d8646-111">PARAMETERS</span></span>

### <span data-ttu-id="d8646-112">-Beskrivning</span><span class="sxs-lookup"><span data-stu-id="d8646-112">-Description</span></span>
<span data-ttu-id="d8646-113">Anger beskrivningen av tillhörighets gruppen.</span><span class="sxs-lookup"><span data-stu-id="d8646-113">Specifies the description of the affinity group.</span></span>
<span data-ttu-id="d8646-114">Beskrivningen kan vara upp till 1024 tecken lång.</span><span class="sxs-lookup"><span data-stu-id="d8646-114">The description can be up to 1024 characters long.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d8646-115">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="d8646-115">-InformationAction</span></span>
<span data-ttu-id="d8646-116">Anger hur den här cmdleten svarar på en informations händelse.</span><span class="sxs-lookup"><span data-stu-id="d8646-116">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="d8646-117">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="d8646-117">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="d8646-118">Vidare</span><span class="sxs-lookup"><span data-stu-id="d8646-118">Continue</span></span>
- <span data-ttu-id="d8646-119">Över</span><span class="sxs-lookup"><span data-stu-id="d8646-119">Ignore</span></span>
- <span data-ttu-id="d8646-120">Inquire</span><span class="sxs-lookup"><span data-stu-id="d8646-120">Inquire</span></span>
- <span data-ttu-id="d8646-121">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="d8646-121">SilentlyContinue</span></span>
- <span data-ttu-id="d8646-122">Stanna</span><span class="sxs-lookup"><span data-stu-id="d8646-122">Stop</span></span>
- <span data-ttu-id="d8646-123">Avbryt</span><span class="sxs-lookup"><span data-stu-id="d8646-123">Suspend</span></span>

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

### <span data-ttu-id="d8646-124">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="d8646-124">-InformationVariable</span></span>
<span data-ttu-id="d8646-125">Anger en informations variabel.</span><span class="sxs-lookup"><span data-stu-id="d8646-125">Specifies an information variable.</span></span>

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

### <span data-ttu-id="d8646-126">-Etikett</span><span class="sxs-lookup"><span data-stu-id="d8646-126">-Label</span></span>
<span data-ttu-id="d8646-127">Anger en etikett för tillhörighets gruppen.</span><span class="sxs-lookup"><span data-stu-id="d8646-127">Specifies a label for the affinity group.</span></span>
<span data-ttu-id="d8646-128">Etiketten kan vara upp till 100 tecken lång.</span><span class="sxs-lookup"><span data-stu-id="d8646-128">The label can be up to 100 characters long.</span></span>

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

### <span data-ttu-id="d8646-129">-Namn</span><span class="sxs-lookup"><span data-stu-id="d8646-129">-Name</span></span>
<span data-ttu-id="d8646-130">Anger namnet på den tillhörighets grupp som denna cmdlet ändrar.</span><span class="sxs-lookup"><span data-stu-id="d8646-130">Specifies the name of the affinity group that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="d8646-131">-Profil</span><span class="sxs-lookup"><span data-stu-id="d8646-131">-Profile</span></span>
<span data-ttu-id="d8646-132">Anger den Azure-profil från vilken denna cmdlet läser.</span><span class="sxs-lookup"><span data-stu-id="d8646-132">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="d8646-133">Om du inte anger en profil läser denna cmdlet från den lokala standard profilen.</span><span class="sxs-lookup"><span data-stu-id="d8646-133">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="d8646-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d8646-134">CommonParameters</span></span>
<span data-ttu-id="d8646-135">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d8646-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d8646-136">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d8646-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d8646-137">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="d8646-137">INPUTS</span></span>

## <span data-ttu-id="d8646-138">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="d8646-138">OUTPUTS</span></span>

## <span data-ttu-id="d8646-139">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="d8646-139">NOTES</span></span>

## <span data-ttu-id="d8646-140">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="d8646-140">RELATED LINKS</span></span>

[<span data-ttu-id="d8646-141">Get-AzureAffinityGroup</span><span class="sxs-lookup"><span data-stu-id="d8646-141">Get-AzureAffinityGroup</span></span>](./Get-AzureAffinityGroup.md)

[<span data-ttu-id="d8646-142">New-AzureAffinityGroup</span><span class="sxs-lookup"><span data-stu-id="d8646-142">New-AzureAffinityGroup</span></span>](./New-AzureAffinityGroup.md)

[<span data-ttu-id="d8646-143">Remove-AzureAffinityGroup</span><span class="sxs-lookup"><span data-stu-id="d8646-143">Remove-AzureAffinityGroup</span></span>](./Remove-AzureAffinityGroup.md)


