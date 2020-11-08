---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: D0A2B454-7BFF-4D4D-8A85-FDB47249758F
online version: ''
schema: 2.0.0
ms.openlocfilehash: 5f4d1598f17629d178e1feff1b5549631be48c60
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94099049"
---
# <span data-ttu-id="23394-101">Set-AzureServiceProject</span><span class="sxs-lookup"><span data-stu-id="23394-101">Set-AzureServiceProject</span></span>

## <span data-ttu-id="23394-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="23394-102">SYNOPSIS</span></span>
<span data-ttu-id="23394-103">Anger standard plats, prenumeration, plats och lagrings konto för den aktuella tjänsten.</span><span class="sxs-lookup"><span data-stu-id="23394-103">Sets default location, subscription, slot, and storage account for the current service.</span></span>

## <span data-ttu-id="23394-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="23394-104">SYNTAX</span></span>

```
Set-AzureServiceProject [-Location <String>] [-Slot <String>] [-Storage <String>] [-PassThru]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="23394-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="23394-105">DESCRIPTION</span></span>
<span data-ttu-id="23394-106">Cmdleten **set-AzureServiceProject** anger distributions plats, plats, lagrings konto och abonnemang för den aktuella tjänsten.</span><span class="sxs-lookup"><span data-stu-id="23394-106">The **Set-AzureServiceProject** cmdlet sets the deployment location, slot, storage account, and subscription for the current service.</span></span>
<span data-ttu-id="23394-107">Dessa värden används när tjänsten publiceras till molnet.</span><span class="sxs-lookup"><span data-stu-id="23394-107">These values are used whenever the service is published to the cloud.</span></span>

## <span data-ttu-id="23394-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="23394-108">EXAMPLES</span></span>

### <span data-ttu-id="23394-109">Exempel 1: grundläggande inställningar</span><span class="sxs-lookup"><span data-stu-id="23394-109">Example 1: Basic settings</span></span>
```
PS C:\> Set-AzureServiceProject -Location "North Central US" -Slot Production -Storage myStorageAccount -Subscription myAzureSubscription
```

<span data-ttu-id="23394-110">Anger distributions platsen för tjänsten till Nord Central USA-regionen.</span><span class="sxs-lookup"><span data-stu-id="23394-110">Sets the deployment location for the service to the North Central US region.</span></span>
<span data-ttu-id="23394-111">Ställer in distributions platsen för produktion.</span><span class="sxs-lookup"><span data-stu-id="23394-111">Sets the deployment slot to Production.</span></span> <span data-ttu-id="23394-112">Anger det lagrings konto som ska användas för att mellanlagra tjänst definitionen på myStorageAccount.</span><span class="sxs-lookup"><span data-stu-id="23394-112">Sets the storage account that will be used to stage the service definition to myStorageAccount.</span></span>
<span data-ttu-id="23394-113">Anger den prenumeration som ska vara värd för tjänsten för prenumeration.</span><span class="sxs-lookup"><span data-stu-id="23394-113">Sets the subscription that will host the service to mySubscription.</span></span>
<span data-ttu-id="23394-114">När tjänsten publiceras i molnet kommer den att finnas i ett Data Center i Nord Central USA-regionen, den uppdaterar distributions platsen och använder det angivna abonnemangs-och lagrings konto.</span><span class="sxs-lookup"><span data-stu-id="23394-114">Whenever the service is published to the cloud, it will be hosted in a data center in the North Central US region, it will update the deployment slot, and it will use the specified subscription and storage account.</span></span>

## <span data-ttu-id="23394-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="23394-115">PARAMETERS</span></span>

### <span data-ttu-id="23394-116">-Plats</span><span class="sxs-lookup"><span data-stu-id="23394-116">-Location</span></span>
<span data-ttu-id="23394-117">Den region där tjänsten hanteras.</span><span class="sxs-lookup"><span data-stu-id="23394-117">The region in which the service will be hosted.</span></span>
<span data-ttu-id="23394-118">Det här värdet används när tjänsten publiceras till molnet.</span><span class="sxs-lookup"><span data-stu-id="23394-118">This value is used whenever the service is published to the cloud.</span></span>
<span data-ttu-id="23394-119">Möjliga värden är: överallt, överallt, världen, USA, Östasien, öst, Nord Central USA, Nord Europa, södra Central USA, Sydostasien, Västeuropa, västra USA.</span><span class="sxs-lookup"><span data-stu-id="23394-119">Possible values are: Anywhere Asia, Anywhere Europe, Anywhere US, East Asia, East US, North Central US, North Europe, South Central US, Southeast Asia, West Europe, West US.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="23394-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="23394-120">-PassThru</span></span>
<span data-ttu-id="23394-121">Anger att den här cmdleten returnerar ett objekt som representerar det objekt som den körs på.</span><span class="sxs-lookup"><span data-stu-id="23394-121">Indicates that this cmdlet returns an object representing the item on which it operates.</span></span>
<span data-ttu-id="23394-122">Denna cmdlet genererar som standard inga utdata.</span><span class="sxs-lookup"><span data-stu-id="23394-122">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="23394-123">-Profil</span><span class="sxs-lookup"><span data-stu-id="23394-123">-Profile</span></span>
<span data-ttu-id="23394-124">Anger den Azure-profil från vilken denna cmdlet läser.</span><span class="sxs-lookup"><span data-stu-id="23394-124">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="23394-125">Om du inte anger en profil läser denna cmdlet från den lokala standard profilen.</span><span class="sxs-lookup"><span data-stu-id="23394-125">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="23394-126">-Plats</span><span class="sxs-lookup"><span data-stu-id="23394-126">-Slot</span></span>
<span data-ttu-id="23394-127">Den plats (produktion eller mellanlagring) som tjänsten finns i.</span><span class="sxs-lookup"><span data-stu-id="23394-127">The slot (production or staging) in which the service will be hosted.</span></span>
<span data-ttu-id="23394-128">Det här värdet används när tjänsten publiceras till molnet.</span><span class="sxs-lookup"><span data-stu-id="23394-128">This value is used whenever the service is published to the cloud.</span></span>
<span data-ttu-id="23394-129">Möjliga värden är: produktion, mellanlagring.</span><span class="sxs-lookup"><span data-stu-id="23394-129">Possible values are: Production, Staging.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="23394-130">-Lagring</span><span class="sxs-lookup"><span data-stu-id="23394-130">-Storage</span></span>
<span data-ttu-id="23394-131">Det lagrings konto som ska användas när tjänste paketet laddas upp till molnet.</span><span class="sxs-lookup"><span data-stu-id="23394-131">The storage account to be used when uploading the service package to the cloud.</span></span>
<span data-ttu-id="23394-132">Om lagrings kontot inte finns skapas det när tjänsten publiceras till molnet.</span><span class="sxs-lookup"><span data-stu-id="23394-132">If the storage account doesn't exist, it will be created when the service is published to the cloud.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="23394-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="23394-133">CommonParameters</span></span>
<span data-ttu-id="23394-134">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="23394-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="23394-135">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="23394-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="23394-136">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="23394-136">INPUTS</span></span>

## <span data-ttu-id="23394-137">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="23394-137">OUTPUTS</span></span>

## <span data-ttu-id="23394-138">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="23394-138">NOTES</span></span>
* <span data-ttu-id="23394-139">nod-dev, php-dev, python-dev</span><span class="sxs-lookup"><span data-stu-id="23394-139">node-dev, php-dev, python-dev</span></span>

## <span data-ttu-id="23394-140">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="23394-140">RELATED LINKS</span></span>

[<span data-ttu-id="23394-141">New-AzureServiceProject</span><span class="sxs-lookup"><span data-stu-id="23394-141">New-AzureServiceProject</span></span>](./New-AzureServiceProject.md)

[<span data-ttu-id="23394-142">Publicera – AzureServiceProject</span><span class="sxs-lookup"><span data-stu-id="23394-142">Publish-AzureServiceProject</span></span>](./Publish-AzureServiceProject.md)

[<span data-ttu-id="23394-143">Set-AzureServiceProjectRole</span><span class="sxs-lookup"><span data-stu-id="23394-143">Set-AzureServiceProjectRole</span></span>](./Set-AzureServiceProjectRole.md)


