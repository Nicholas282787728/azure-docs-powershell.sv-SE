---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 761317FE-55FD-4DCC-B997-4F27D041470F
online version: ''
schema: 2.0.0
ms.openlocfilehash: 77f58c4f3ee1c440e35c43648f92d21793efddc2
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94099375"
---
# <span data-ttu-id="37dfe-101">Remove-AzureReservedIP</span><span class="sxs-lookup"><span data-stu-id="37dfe-101">Remove-AzureReservedIP</span></span>

## <span data-ttu-id="37dfe-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="37dfe-102">SYNOPSIS</span></span>
<span data-ttu-id="37dfe-103">Tar bort en reserverad IP-adress utifrån dess namn.</span><span class="sxs-lookup"><span data-stu-id="37dfe-103">Removes a reserved IP address by its name.</span></span>

## <span data-ttu-id="37dfe-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="37dfe-104">SYNTAX</span></span>

```
Remove-AzureReservedIP [-ReservedIPName] <String> [-Force] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="37dfe-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="37dfe-105">DESCRIPTION</span></span>
<span data-ttu-id="37dfe-106">Cmdleten **Remove-AzureReservedIP** tar bort en reserverad IP-adress utifrån dess namn.</span><span class="sxs-lookup"><span data-stu-id="37dfe-106">The **Remove-AzureReservedIP** cmdlet removes a reserved IP address by its name.</span></span>

## <span data-ttu-id="37dfe-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="37dfe-107">EXAMPLES</span></span>

### <span data-ttu-id="37dfe-108">Exempel 1: ta bort en reserverad IP-adress utifrån dess namn</span><span class="sxs-lookup"><span data-stu-id="37dfe-108">Example 1: Remove a reserved IP address by its name</span></span>
```
PS C:\> Remove-AzureReservedIP -ReservedIPName $name
```

<span data-ttu-id="37dfe-109">Det här kommandot tar bort en reserverad IP-adress utifrån dess namn.</span><span class="sxs-lookup"><span data-stu-id="37dfe-109">This command removes a reserved IP address by its name.</span></span>

## <span data-ttu-id="37dfe-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="37dfe-110">PARAMETERS</span></span>

### <span data-ttu-id="37dfe-111">-Force</span><span class="sxs-lookup"><span data-stu-id="37dfe-111">-Force</span></span>
<span data-ttu-id="37dfe-112">Tvingar kommandot att köras utan att fråga efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="37dfe-112">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="37dfe-113">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="37dfe-113">-InformationAction</span></span>
<span data-ttu-id="37dfe-114">Anger hur den här cmdleten svarar på en informations händelse.</span><span class="sxs-lookup"><span data-stu-id="37dfe-114">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="37dfe-115">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="37dfe-115">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="37dfe-116">Vidare</span><span class="sxs-lookup"><span data-stu-id="37dfe-116">Continue</span></span>
- <span data-ttu-id="37dfe-117">Över</span><span class="sxs-lookup"><span data-stu-id="37dfe-117">Ignore</span></span>
- <span data-ttu-id="37dfe-118">Inquire</span><span class="sxs-lookup"><span data-stu-id="37dfe-118">Inquire</span></span>
- <span data-ttu-id="37dfe-119">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="37dfe-119">SilentlyContinue</span></span>
- <span data-ttu-id="37dfe-120">Stanna</span><span class="sxs-lookup"><span data-stu-id="37dfe-120">Stop</span></span>
- <span data-ttu-id="37dfe-121">Avbryt</span><span class="sxs-lookup"><span data-stu-id="37dfe-121">Suspend</span></span>

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

### <span data-ttu-id="37dfe-122">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="37dfe-122">-InformationVariable</span></span>
<span data-ttu-id="37dfe-123">Anger en informations variabel.</span><span class="sxs-lookup"><span data-stu-id="37dfe-123">Specifies an information variable.</span></span>

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

### <span data-ttu-id="37dfe-124">-Profil</span><span class="sxs-lookup"><span data-stu-id="37dfe-124">-Profile</span></span>
<span data-ttu-id="37dfe-125">Anger den Azure-profil från vilken denna cmdlet läser.</span><span class="sxs-lookup"><span data-stu-id="37dfe-125">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="37dfe-126">Om du inte anger en profil läser denna cmdlet från den lokala standard profilen.</span><span class="sxs-lookup"><span data-stu-id="37dfe-126">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="37dfe-127">-ReservedIPName</span><span class="sxs-lookup"><span data-stu-id="37dfe-127">-ReservedIPName</span></span>
<span data-ttu-id="37dfe-128">Anger namnet på den reserverade IP-adressen.</span><span class="sxs-lookup"><span data-stu-id="37dfe-128">Specifies the name of the reserved IP address.</span></span>

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

### <span data-ttu-id="37dfe-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="37dfe-129">CommonParameters</span></span>
<span data-ttu-id="37dfe-130">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="37dfe-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="37dfe-131">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="37dfe-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="37dfe-132">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="37dfe-132">INPUTS</span></span>

## <span data-ttu-id="37dfe-133">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="37dfe-133">OUTPUTS</span></span>

## <span data-ttu-id="37dfe-134">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="37dfe-134">NOTES</span></span>

## <span data-ttu-id="37dfe-135">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="37dfe-135">RELATED LINKS</span></span>

[<span data-ttu-id="37dfe-136">Get-AzureReservedIP</span><span class="sxs-lookup"><span data-stu-id="37dfe-136">Get-AzureReservedIP</span></span>](./Get-AzureReservedIP.md)

[<span data-ttu-id="37dfe-137">New-AzureReservedIP</span><span class="sxs-lookup"><span data-stu-id="37dfe-137">New-AzureReservedIP</span></span>](./New-AzureReservedIP.md)

[<span data-ttu-id="37dfe-138">Set-AzureReservedIPAssociation</span><span class="sxs-lookup"><span data-stu-id="37dfe-138">Set-AzureReservedIPAssociation</span></span>](./Set-AzureReservedIPAssociation.md)


