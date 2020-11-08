---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: BB216903-B2BB-4948-AC28-408ED6C768F2
online version: ''
schema: 2.0.0
ms.openlocfilehash: 6cae249f99282006ff8636e8d727485a223e2a1d
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94099129"
---
# <span data-ttu-id="c6dfa-101">New-AzureService</span><span class="sxs-lookup"><span data-stu-id="c6dfa-101">New-AzureService</span></span>

## <span data-ttu-id="c6dfa-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="c6dfa-102">SYNOPSIS</span></span>
<span data-ttu-id="c6dfa-103">Skapar en Azure-tjänst.</span><span class="sxs-lookup"><span data-stu-id="c6dfa-103">Creates an Azure service.</span></span>

## <span data-ttu-id="c6dfa-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="c6dfa-104">SYNTAX</span></span>

### <span data-ttu-id="c6dfa-105">ParameterSetAffinityGroup (standard)</span><span class="sxs-lookup"><span data-stu-id="c6dfa-105">ParameterSetAffinityGroup (Default)</span></span>
```
New-AzureService [-ServiceName] <String> [-AffinityGroup] <String> [[-Label] <String>]
 [[-Description] <String>] [[-ReverseDnsFqdn] <String>] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="c6dfa-106">ParameterSetLocation</span><span class="sxs-lookup"><span data-stu-id="c6dfa-106">ParameterSetLocation</span></span>
```
New-AzureService [-ServiceName] <String> [-Location] <String> [[-Label] <String>] [[-Description] <String>]
 [[-ReverseDnsFqdn] <String>] [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="c6dfa-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="c6dfa-107">DESCRIPTION</span></span>
<span data-ttu-id="c6dfa-108">Cmdleten **New-AzureService** skapar en ny Azure-tjänst i den aktuella prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="c6dfa-108">The **New-AzureService** cmdlet creates a new Azure service in the current subscription.</span></span>

## <span data-ttu-id="c6dfa-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="c6dfa-109">EXAMPLES</span></span>

### <span data-ttu-id="c6dfa-110">Exempel 1: skapa en tjänst</span><span class="sxs-lookup"><span data-stu-id="c6dfa-110">Example 1: Create a service</span></span>
```
PS C:\> New-AzureService -ServiceName "MySvc01" -Label "MyTestService" -Location "South Central US"
```

<span data-ttu-id="c6dfa-111">Det här kommandot skapar en ny tjänst som heter MySvc01 på platsen Central amerikanska.</span><span class="sxs-lookup"><span data-stu-id="c6dfa-111">This command creates a new service named MySvc01 in the South Central US location.</span></span>

### <span data-ttu-id="c6dfa-112">Exempel 2: skapa en tjänst i en tillhörighets grupp</span><span class="sxs-lookup"><span data-stu-id="c6dfa-112">Example 2: Create a service in an affinity group</span></span>
```
PS C:\> New-AzureService -ServiceName "MySvc01" -AffinityGroup NorthRegion
```

<span data-ttu-id="c6dfa-113">Det här kommandot skapar en ny tjänst som heter MySvc01 med hjälp av NorthRegion-tillhörighets gruppen.</span><span class="sxs-lookup"><span data-stu-id="c6dfa-113">This command creates a new service named MySvc01 using the NorthRegion affinity group.</span></span>

## <span data-ttu-id="c6dfa-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="c6dfa-114">PARAMETERS</span></span>

### <span data-ttu-id="c6dfa-115">-AffinityGroup</span><span class="sxs-lookup"><span data-stu-id="c6dfa-115">-AffinityGroup</span></span>
<span data-ttu-id="c6dfa-116">Anger den tillhörighets grupp som är kopplad till prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="c6dfa-116">Specifies the affinity group associated with the subscription.</span></span>
<span data-ttu-id="c6dfa-117">Om du inte anger *plats* parametern krävs en tillhörighets grupp.</span><span class="sxs-lookup"><span data-stu-id="c6dfa-117">If you do not specify the *Location* parameter, an affinity group is required.</span></span>

```yaml
Type: String
Parameter Sets: ParameterSetAffinityGroup
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c6dfa-118">-Beskrivning</span><span class="sxs-lookup"><span data-stu-id="c6dfa-118">-Description</span></span>
<span data-ttu-id="c6dfa-119">Anger en beskrivning av tjänsten.</span><span class="sxs-lookup"><span data-stu-id="c6dfa-119">Specifies a description for the service.</span></span>
<span data-ttu-id="c6dfa-120">Beskrivningen kan vara upp till 1024 tecken lång.</span><span class="sxs-lookup"><span data-stu-id="c6dfa-120">The description may be up to 1024 characters in length.</span></span>

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

### <span data-ttu-id="c6dfa-121">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="c6dfa-121">-InformationAction</span></span>
<span data-ttu-id="c6dfa-122">Anger hur den här cmdleten svarar på en informations händelse.</span><span class="sxs-lookup"><span data-stu-id="c6dfa-122">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="c6dfa-123">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="c6dfa-123">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="c6dfa-124">Vidare</span><span class="sxs-lookup"><span data-stu-id="c6dfa-124">Continue</span></span>
- <span data-ttu-id="c6dfa-125">Över</span><span class="sxs-lookup"><span data-stu-id="c6dfa-125">Ignore</span></span>
- <span data-ttu-id="c6dfa-126">Inquire</span><span class="sxs-lookup"><span data-stu-id="c6dfa-126">Inquire</span></span>
- <span data-ttu-id="c6dfa-127">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="c6dfa-127">SilentlyContinue</span></span>
- <span data-ttu-id="c6dfa-128">Stanna</span><span class="sxs-lookup"><span data-stu-id="c6dfa-128">Stop</span></span>
- <span data-ttu-id="c6dfa-129">Avbryt</span><span class="sxs-lookup"><span data-stu-id="c6dfa-129">Suspend</span></span>

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

### <span data-ttu-id="c6dfa-130">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="c6dfa-130">-InformationVariable</span></span>
<span data-ttu-id="c6dfa-131">Anger en informations variabel.</span><span class="sxs-lookup"><span data-stu-id="c6dfa-131">Specifies an information variable.</span></span>

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

### <span data-ttu-id="c6dfa-132">-Etikett</span><span class="sxs-lookup"><span data-stu-id="c6dfa-132">-Label</span></span>
<span data-ttu-id="c6dfa-133">Anger en etikett för tjänsten.</span><span class="sxs-lookup"><span data-stu-id="c6dfa-133">Specifies a label for the service.</span></span>
<span data-ttu-id="c6dfa-134">Etiketten kan vara upp till 100 tecken lång.</span><span class="sxs-lookup"><span data-stu-id="c6dfa-134">The label may be up to 100 characters in length.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c6dfa-135">-Plats</span><span class="sxs-lookup"><span data-stu-id="c6dfa-135">-Location</span></span>
<span data-ttu-id="c6dfa-136">Anger platsen för tjänsten.</span><span class="sxs-lookup"><span data-stu-id="c6dfa-136">Specifies the location for the service.</span></span>
<span data-ttu-id="c6dfa-137">En plats krävs om det inte finns någon angiven tillhörighets grupp.</span><span class="sxs-lookup"><span data-stu-id="c6dfa-137">A location is required if there isn't a specified Affinity Group.</span></span>

```yaml
Type: String
Parameter Sets: ParameterSetLocation
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c6dfa-138">-Profil</span><span class="sxs-lookup"><span data-stu-id="c6dfa-138">-Profile</span></span>
<span data-ttu-id="c6dfa-139">Anger den Azure-profil från vilken denna cmdlet läser.</span><span class="sxs-lookup"><span data-stu-id="c6dfa-139">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="c6dfa-140">Om du inte anger en profil läser denna cmdlet från den lokala standard profilen.</span><span class="sxs-lookup"><span data-stu-id="c6dfa-140">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="c6dfa-141">-ReverseDnsFqdn</span><span class="sxs-lookup"><span data-stu-id="c6dfa-141">-ReverseDnsFqdn</span></span>
<span data-ttu-id="c6dfa-142">Anger det fullständigt kvalificerade domän namnet för omvänd DNS.</span><span class="sxs-lookup"><span data-stu-id="c6dfa-142">Specifies the fully qualified domain name for reverse DNS.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c6dfa-143">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="c6dfa-143">-ServiceName</span></span>
<span data-ttu-id="c6dfa-144">Anger namnet på den nya tjänsten.</span><span class="sxs-lookup"><span data-stu-id="c6dfa-144">Specifies the name of the new service.</span></span>
<span data-ttu-id="c6dfa-145">Namnet måste vara unikt för abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="c6dfa-145">The name must be unique to the subscription.</span></span>

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

### <span data-ttu-id="c6dfa-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c6dfa-146">CommonParameters</span></span>
<span data-ttu-id="c6dfa-147">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c6dfa-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c6dfa-148">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c6dfa-148">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c6dfa-149">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="c6dfa-149">INPUTS</span></span>

## <span data-ttu-id="c6dfa-150">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="c6dfa-150">OUTPUTS</span></span>

## <span data-ttu-id="c6dfa-151">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="c6dfa-151">NOTES</span></span>

## <span data-ttu-id="c6dfa-152">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="c6dfa-152">RELATED LINKS</span></span>

[<span data-ttu-id="c6dfa-153">Get-AzureService</span><span class="sxs-lookup"><span data-stu-id="c6dfa-153">Get-AzureService</span></span>](./Get-AzureService.md)

[<span data-ttu-id="c6dfa-154">Set-AzureService</span><span class="sxs-lookup"><span data-stu-id="c6dfa-154">Set-AzureService</span></span>](./Set-AzureService.md)


