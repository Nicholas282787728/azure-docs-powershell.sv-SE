---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 54C89A5F-BF94-468C-92E7-224808FDD0EC
online version: ''
schema: 2.0.0
ms.openlocfilehash: be84995e4826b79befc6282133d70f3ee4a79b4f
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94099457"
---
# <span data-ttu-id="bb3b7-101">New-AzureAffinityGroup</span><span class="sxs-lookup"><span data-stu-id="bb3b7-101">New-AzureAffinityGroup</span></span>

## <span data-ttu-id="bb3b7-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="bb3b7-102">SYNOPSIS</span></span>
<span data-ttu-id="bb3b7-103">Skapar en tillhörighets grupp i det aktuella abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="bb3b7-103">Creates an affinity group in the current subscription.</span></span>

## <span data-ttu-id="bb3b7-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="bb3b7-104">SYNTAX</span></span>

```
New-AzureAffinityGroup [-Name] <String> [-Label <String>] [-Description <String>] -Location <String>
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

## <span data-ttu-id="bb3b7-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="bb3b7-105">DESCRIPTION</span></span>
<span data-ttu-id="bb3b7-106">Cmdleten **New-AzureAffinityGroup** skapar en Azure tillhörighets grupp i det aktuella Azure-abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="bb3b7-106">The **New-AzureAffinityGroup** cmdlet creates an Azure affinity group in the current Azure subscription.</span></span>

<span data-ttu-id="bb3b7-107">En tillhörighets grupp placerar dina tjänster och deras resurser tillsammans i ett Azure-datacenter.</span><span class="sxs-lookup"><span data-stu-id="bb3b7-107">An affinity group puts your services and their resources together in an Azure datacenter.</span></span>
<span data-ttu-id="bb3b7-108">Gruppens tillhörighet grupper är tillsammans för optimal prestanda.</span><span class="sxs-lookup"><span data-stu-id="bb3b7-108">The affinity group groups members together for optimal performance.</span></span>
<span data-ttu-id="bb3b7-109">Definiera tillhörighets grupper på abonnemangs nivån.</span><span class="sxs-lookup"><span data-stu-id="bb3b7-109">Define affinity groups at the subscription level.</span></span>
<span data-ttu-id="bb3b7-110">Dina tillhörighets grupper är tillgängliga för alla efterföljande moln tjänster eller lagrings konton som du skapar.</span><span class="sxs-lookup"><span data-stu-id="bb3b7-110">Your affinity groups are available to any subsequent cloud services or storage accounts that you create.</span></span>
<span data-ttu-id="bb3b7-111">Du kan bara lägga till tjänster i en tillhörighets grupp när du skapar den.</span><span class="sxs-lookup"><span data-stu-id="bb3b7-111">You can add services to an affinity group only when you create it.</span></span>

## <span data-ttu-id="bb3b7-112">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="bb3b7-112">EXAMPLES</span></span>

### <span data-ttu-id="bb3b7-113">Exempel 1: skapa en tillhörighets grupp</span><span class="sxs-lookup"><span data-stu-id="bb3b7-113">Example 1: Create an affinity group</span></span>
```
PS C:\> New-AzureAffinityGroup -Name "South01" -Location "South Central US" -Label "South Region" -Description "Affinity group for production applications in southern region."
```

<span data-ttu-id="bb3b7-114">Det här kommandot skapar en tillhörighets grupp med namnet South01 i området Central USA.</span><span class="sxs-lookup"><span data-stu-id="bb3b7-114">This command creates an affinity group named South01 in the South Central US region.</span></span>
<span data-ttu-id="bb3b7-115">Kommandot anger en etikett och en beskrivning.</span><span class="sxs-lookup"><span data-stu-id="bb3b7-115">The command specifies a label and a description.</span></span>

## <span data-ttu-id="bb3b7-116">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="bb3b7-116">PARAMETERS</span></span>

### <span data-ttu-id="bb3b7-117">-Beskrivning</span><span class="sxs-lookup"><span data-stu-id="bb3b7-117">-Description</span></span>
<span data-ttu-id="bb3b7-118">Anger en beskrivning av tillhörighets gruppen.</span><span class="sxs-lookup"><span data-stu-id="bb3b7-118">Specifies a description for the affinity group.</span></span>
<span data-ttu-id="bb3b7-119">Beskrivningen kan vara upp till 1024 tecken lång.</span><span class="sxs-lookup"><span data-stu-id="bb3b7-119">The description may be up to 1024 characters long.</span></span>

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

### <span data-ttu-id="bb3b7-120">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="bb3b7-120">-InformationAction</span></span>
<span data-ttu-id="bb3b7-121">Anger hur den här cmdleten svarar på en informations händelse.</span><span class="sxs-lookup"><span data-stu-id="bb3b7-121">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="bb3b7-122">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="bb3b7-122">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="bb3b7-123">Vidare</span><span class="sxs-lookup"><span data-stu-id="bb3b7-123">Continue</span></span>
- <span data-ttu-id="bb3b7-124">Över</span><span class="sxs-lookup"><span data-stu-id="bb3b7-124">Ignore</span></span>
- <span data-ttu-id="bb3b7-125">Inquire</span><span class="sxs-lookup"><span data-stu-id="bb3b7-125">Inquire</span></span>
- <span data-ttu-id="bb3b7-126">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="bb3b7-126">SilentlyContinue</span></span>
- <span data-ttu-id="bb3b7-127">Stanna</span><span class="sxs-lookup"><span data-stu-id="bb3b7-127">Stop</span></span>
- <span data-ttu-id="bb3b7-128">Avbryt</span><span class="sxs-lookup"><span data-stu-id="bb3b7-128">Suspend</span></span>

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

### <span data-ttu-id="bb3b7-129">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="bb3b7-129">-InformationVariable</span></span>
<span data-ttu-id="bb3b7-130">Anger en informations variabel.</span><span class="sxs-lookup"><span data-stu-id="bb3b7-130">Specifies an information variable.</span></span>

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

### <span data-ttu-id="bb3b7-131">-Etikett</span><span class="sxs-lookup"><span data-stu-id="bb3b7-131">-Label</span></span>
<span data-ttu-id="bb3b7-132">Anger en etikett för tillhörighets gruppen.</span><span class="sxs-lookup"><span data-stu-id="bb3b7-132">Specifies a label for the affinity group.</span></span>
<span data-ttu-id="bb3b7-133">Etiketten kan vara upp till 100 tecken lång.</span><span class="sxs-lookup"><span data-stu-id="bb3b7-133">The label may be up to 100 characters long.</span></span>

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

### <span data-ttu-id="bb3b7-134">-Plats</span><span class="sxs-lookup"><span data-stu-id="bb3b7-134">-Location</span></span>
<span data-ttu-id="bb3b7-135">Anger den geografiska platsen för Azure-datacenter där denna cmdlet skapar tillhörighets gruppen.</span><span class="sxs-lookup"><span data-stu-id="bb3b7-135">Specifies the geographical location of the Azure datacenter where this cmdlet creates the affinity group.</span></span>

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

### <span data-ttu-id="bb3b7-136">-Namn</span><span class="sxs-lookup"><span data-stu-id="bb3b7-136">-Name</span></span>
<span data-ttu-id="bb3b7-137">Anger ett namn för tillhörighets gruppen.</span><span class="sxs-lookup"><span data-stu-id="bb3b7-137">Specifies a name for the affinity group.</span></span>
<span data-ttu-id="bb3b7-138">Namnet måste vara unikt för abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="bb3b7-138">The name must be unique to the subscription.</span></span>

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

### <span data-ttu-id="bb3b7-139">-Profil</span><span class="sxs-lookup"><span data-stu-id="bb3b7-139">-Profile</span></span>
<span data-ttu-id="bb3b7-140">Anger den Azure-profil från vilken denna cmdlet läser.</span><span class="sxs-lookup"><span data-stu-id="bb3b7-140">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="bb3b7-141">Om du inte anger en profil läser denna cmdlet från den lokala standard profilen.</span><span class="sxs-lookup"><span data-stu-id="bb3b7-141">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="bb3b7-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bb3b7-142">CommonParameters</span></span>
<span data-ttu-id="bb3b7-143">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bb3b7-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bb3b7-144">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bb3b7-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bb3b7-145">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="bb3b7-145">INPUTS</span></span>

## <span data-ttu-id="bb3b7-146">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="bb3b7-146">OUTPUTS</span></span>

## <span data-ttu-id="bb3b7-147">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="bb3b7-147">NOTES</span></span>

## <span data-ttu-id="bb3b7-148">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="bb3b7-148">RELATED LINKS</span></span>

[<span data-ttu-id="bb3b7-149">Get-AzureAffinityGroup</span><span class="sxs-lookup"><span data-stu-id="bb3b7-149">Get-AzureAffinityGroup</span></span>](./Get-AzureAffinityGroup.md)

[<span data-ttu-id="bb3b7-150">Remove-AzureAffinityGroup</span><span class="sxs-lookup"><span data-stu-id="bb3b7-150">Remove-AzureAffinityGroup</span></span>](./Remove-AzureAffinityGroup.md)

[<span data-ttu-id="bb3b7-151">Set-AzureAffinityGroup</span><span class="sxs-lookup"><span data-stu-id="bb3b7-151">Set-AzureAffinityGroup</span></span>](./Set-AzureAffinityGroup.md)


