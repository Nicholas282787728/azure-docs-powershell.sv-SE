---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 77B26360-F22B-457F-BDE3-9920A5736947
online version: ''
schema: 2.0.0
ms.openlocfilehash: 323b04a57cffc71059dff3f91480d54684941695
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94093397"
---
# <span data-ttu-id="8fcc1-101">Get-AzureAffinityGroup</span><span class="sxs-lookup"><span data-stu-id="8fcc1-101">Get-AzureAffinityGroup</span></span>

## <span data-ttu-id="8fcc1-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="8fcc1-102">SYNOPSIS</span></span>
<span data-ttu-id="8fcc1-103">Får ett Azure tillhörighets grupp objekt.</span><span class="sxs-lookup"><span data-stu-id="8fcc1-103">Gets an Azure affinity group object.</span></span>

## <span data-ttu-id="8fcc1-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="8fcc1-104">SYNTAX</span></span>

```
Get-AzureAffinityGroup [[-Name] <String>] [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="8fcc1-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="8fcc1-105">DESCRIPTION</span></span>
<span data-ttu-id="8fcc1-106">Cmdleten **Get-AzureAffinityGroup** hämtar en Azure tillhörighets grupp.</span><span class="sxs-lookup"><span data-stu-id="8fcc1-106">The **Get-AzureAffinityGroup** cmdlet gets an Azure affinity group.</span></span>
<span data-ttu-id="8fcc1-107">Grupp objekt för tillhörighet inkluderar tillhörighets gruppens namn, plats, etikett, beskrivning samt lagrings-och värd tjänster som ingår i tillhörighets gruppen.</span><span class="sxs-lookup"><span data-stu-id="8fcc1-107">The affinity group object includes the affinity group name, location, label, description and the storage and hosted services that are part of the affinity group.</span></span>

## <span data-ttu-id="8fcc1-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="8fcc1-108">EXAMPLES</span></span>

### <span data-ttu-id="8fcc1-109">Exempel 1: Hämta egenskaper för en tillhörighets grupp</span><span class="sxs-lookup"><span data-stu-id="8fcc1-109">Example 1: Get properties of an affinity group</span></span>
```
PS C:\> Get-AzureAffinityGroup -Name "South01"
```

<span data-ttu-id="8fcc1-110">Det här kommandot får egenskaperna för tillhörighets gruppen South01.</span><span class="sxs-lookup"><span data-stu-id="8fcc1-110">This command gets the properties of the affinity group named South01.</span></span>

## <span data-ttu-id="8fcc1-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="8fcc1-111">PARAMETERS</span></span>

### <span data-ttu-id="8fcc1-112">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="8fcc1-112">-InformationAction</span></span>
<span data-ttu-id="8fcc1-113">Anger hur den här cmdleten svarar på en informations händelse.</span><span class="sxs-lookup"><span data-stu-id="8fcc1-113">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="8fcc1-114">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="8fcc1-114">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="8fcc1-115">Vidare</span><span class="sxs-lookup"><span data-stu-id="8fcc1-115">Continue</span></span>
- <span data-ttu-id="8fcc1-116">Över</span><span class="sxs-lookup"><span data-stu-id="8fcc1-116">Ignore</span></span>
- <span data-ttu-id="8fcc1-117">Inquire</span><span class="sxs-lookup"><span data-stu-id="8fcc1-117">Inquire</span></span>
- <span data-ttu-id="8fcc1-118">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="8fcc1-118">SilentlyContinue</span></span>
- <span data-ttu-id="8fcc1-119">Stanna</span><span class="sxs-lookup"><span data-stu-id="8fcc1-119">Stop</span></span>
- <span data-ttu-id="8fcc1-120">Avbryt</span><span class="sxs-lookup"><span data-stu-id="8fcc1-120">Suspend</span></span>

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

### <span data-ttu-id="8fcc1-121">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="8fcc1-121">-InformationVariable</span></span>
<span data-ttu-id="8fcc1-122">Anger en informations variabel.</span><span class="sxs-lookup"><span data-stu-id="8fcc1-122">Specifies an information variable.</span></span>

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

### <span data-ttu-id="8fcc1-123">-Namn</span><span class="sxs-lookup"><span data-stu-id="8fcc1-123">-Name</span></span>
<span data-ttu-id="8fcc1-124">Anger namnet på den tillhörighets grupp som cmdleten får.</span><span class="sxs-lookup"><span data-stu-id="8fcc1-124">Specifies the name of the affinity group that this cmdlet gets.</span></span>
<span data-ttu-id="8fcc1-125">Namn på tillhörighets grupper som skapas via hanterings portalen är vanligt vis GUID.</span><span class="sxs-lookup"><span data-stu-id="8fcc1-125">Names for affinity groups created through the Management Portal are typically GUIDs.</span></span>
<span data-ttu-id="8fcc1-126">Hanterings porten visar tillhörighets grupps etiketten.</span><span class="sxs-lookup"><span data-stu-id="8fcc1-126">The Management Port shows the affinity group label.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8fcc1-127">-Profil</span><span class="sxs-lookup"><span data-stu-id="8fcc1-127">-Profile</span></span>
<span data-ttu-id="8fcc1-128">Anger den Azure-profil från vilken denna cmdlet läser.</span><span class="sxs-lookup"><span data-stu-id="8fcc1-128">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="8fcc1-129">Om du inte anger en profil läser denna cmdlet från den lokala standard profilen.</span><span class="sxs-lookup"><span data-stu-id="8fcc1-129">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="8fcc1-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8fcc1-130">CommonParameters</span></span>
<span data-ttu-id="8fcc1-131">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8fcc1-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8fcc1-132">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8fcc1-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8fcc1-133">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="8fcc1-133">INPUTS</span></span>

## <span data-ttu-id="8fcc1-134">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="8fcc1-134">OUTPUTS</span></span>

### <span data-ttu-id="8fcc1-135">AffinityGroup</span><span class="sxs-lookup"><span data-stu-id="8fcc1-135">AffinityGroup</span></span>

## <span data-ttu-id="8fcc1-136">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="8fcc1-136">NOTES</span></span>

## <span data-ttu-id="8fcc1-137">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="8fcc1-137">RELATED LINKS</span></span>

[<span data-ttu-id="8fcc1-138">New-AzureAffinityGroup</span><span class="sxs-lookup"><span data-stu-id="8fcc1-138">New-AzureAffinityGroup</span></span>](./New-AzureAffinityGroup.md)

[<span data-ttu-id="8fcc1-139">Remove-AzureAffinityGroup</span><span class="sxs-lookup"><span data-stu-id="8fcc1-139">Remove-AzureAffinityGroup</span></span>](./Remove-AzureAffinityGroup.md)

[<span data-ttu-id="8fcc1-140">Set-AzureAffinityGroup</span><span class="sxs-lookup"><span data-stu-id="8fcc1-140">Set-AzureAffinityGroup</span></span>](./Set-AzureAffinityGroup.md)


