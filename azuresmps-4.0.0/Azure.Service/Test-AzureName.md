---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 0DF54C9D-7A19-4591-A1FC-33C6A4C9BF33
online version: ''
schema: 2.0.0
ms.openlocfilehash: 05a99e1a4965329c0eeb29fe0e014814fd1807b2
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94099167"
---
# <span data-ttu-id="bb0ae-101">Test-AzureName</span><span class="sxs-lookup"><span data-stu-id="bb0ae-101">Test-AzureName</span></span>

## <span data-ttu-id="bb0ae-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="bb0ae-102">SYNOPSIS</span></span>
<span data-ttu-id="bb0ae-103">Testar om ett namn på Microsoft Azure Cloud-tjänsten, lagrings tjänstens namn eller Service Bus-namnutrymmet finns eller inte.</span><span class="sxs-lookup"><span data-stu-id="bb0ae-103">Tests whether a Microsoft Azure cloud service name, storage service name or service bus namespace name exists or not.</span></span>

## <span data-ttu-id="bb0ae-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="bb0ae-104">SYNTAX</span></span>

### <span data-ttu-id="bb0ae-105">Serv</span><span class="sxs-lookup"><span data-stu-id="bb0ae-105">Service</span></span>
```
Test-AzureName [-Service] -Name <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="bb0ae-106">Lagringsrelaterade</span><span class="sxs-lookup"><span data-stu-id="bb0ae-106">Storage</span></span>
```
Test-AzureName [-Storage] -Name <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="bb0ae-107">ServiceBusNamespace</span><span class="sxs-lookup"><span data-stu-id="bb0ae-107">ServiceBusNamespace</span></span>
```
Test-AzureName [-ServiceBusNamespace] -Name <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="bb0ae-108">Webbplats</span><span class="sxs-lookup"><span data-stu-id="bb0ae-108">Website</span></span>
```
Test-AzureName [-Website] -Name <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="bb0ae-109">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="bb0ae-109">DESCRIPTION</span></span>
<span data-ttu-id="bb0ae-110">Om namnet finns returnerar cmdleten $True.</span><span class="sxs-lookup"><span data-stu-id="bb0ae-110">If the name exists, the cmdlet returns $True.</span></span>
<span data-ttu-id="bb0ae-111">Om namnet inte existerar returneras $False.</span><span class="sxs-lookup"><span data-stu-id="bb0ae-111">If the name does not exist, it returns $False.</span></span>

## <span data-ttu-id="bb0ae-112">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="bb0ae-112">EXAMPLES</span></span>

### <span data-ttu-id="bb0ae-113">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="bb0ae-113">Example 1</span></span>
```
PS C:\> Test-AzureName -Service "MyNameService1"
```

<span data-ttu-id="bb0ae-114">Det här kommandot testar för att se om "MyNameService1" är ett befintligt namn på Microsoft Azure Cloud-tjänsten.</span><span class="sxs-lookup"><span data-stu-id="bb0ae-114">This command tests to see if the "MyNameService1" is an existing Microsoft Azure cloud service name.</span></span>

### <span data-ttu-id="bb0ae-115">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="bb0ae-115">Example 2</span></span>
```
PS C:\> Test-AzureName -Storage "mystorename1"
```

<span data-ttu-id="bb0ae-116">Det här kommandot testar för att se om "mystorename1" är ett befintligt Microsoft Azure Storage Service-namn.</span><span class="sxs-lookup"><span data-stu-id="bb0ae-116">This command tests to see if the "mystorename1" is an existing Microsoft Azure storage service name.</span></span>

### <span data-ttu-id="bb0ae-117">Exempel 3</span><span class="sxs-lookup"><span data-stu-id="bb0ae-117">Example 3</span></span>
```
PS C:\> Test-AzureName -ServiceBusNamespace "mynamespace"
```

<span data-ttu-id="bb0ae-118">Det här kommandot testar för att se om "multinamespace" är en befintlig Microsoft Azure Service Bus-namnrymd.</span><span class="sxs-lookup"><span data-stu-id="bb0ae-118">This command tests to see if the "mynamespace" is an existing Microsoft Azure service bus namespace name.</span></span>

## <span data-ttu-id="bb0ae-119">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="bb0ae-119">PARAMETERS</span></span>

### <span data-ttu-id="bb0ae-120">-Namn</span><span class="sxs-lookup"><span data-stu-id="bb0ae-120">-Name</span></span>
<span data-ttu-id="bb0ae-121">Anger namnet på det tjänst-eller lagrings konto som ska testas.</span><span class="sxs-lookup"><span data-stu-id="bb0ae-121">Specifies the name of the service or storage account to test.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bb0ae-122">-Profil</span><span class="sxs-lookup"><span data-stu-id="bb0ae-122">-Profile</span></span>
<span data-ttu-id="bb0ae-123">Anger den Azure-profil från vilken denna cmdlet läser.</span><span class="sxs-lookup"><span data-stu-id="bb0ae-123">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="bb0ae-124">Om du inte anger en profil läser denna cmdlet från den lokala standard profilen.</span><span class="sxs-lookup"><span data-stu-id="bb0ae-124">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="bb0ae-125">-Service</span><span class="sxs-lookup"><span data-stu-id="bb0ae-125">-Service</span></span>
<span data-ttu-id="bb0ae-126">Anger att du vill testa ett befintligt tjänst konto.</span><span class="sxs-lookup"><span data-stu-id="bb0ae-126">Specifies to test for an existing service account.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: Service
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bb0ae-127">-ServiceBusNamespace</span><span class="sxs-lookup"><span data-stu-id="bb0ae-127">-ServiceBusNamespace</span></span>
<span data-ttu-id="bb0ae-128">Anger att du vill testa ett befintligt Service Bus-namnområde.</span><span class="sxs-lookup"><span data-stu-id="bb0ae-128">Specifies to test for an existing service bus namespace.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: ServiceBusNamespace
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bb0ae-129">-Lagring</span><span class="sxs-lookup"><span data-stu-id="bb0ae-129">-Storage</span></span>
<span data-ttu-id="bb0ae-130">Anger att du vill testa ett befintligt lagrings konto.</span><span class="sxs-lookup"><span data-stu-id="bb0ae-130">Specifies to test for an existing storage account.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: Storage
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bb0ae-131">-Webbplats</span><span class="sxs-lookup"><span data-stu-id="bb0ae-131">-Website</span></span>
<span data-ttu-id="bb0ae-132">Anger att du vill testa en befintlig webbplats.</span><span class="sxs-lookup"><span data-stu-id="bb0ae-132">Specifies to test for an existing website.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: Website
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bb0ae-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bb0ae-133">CommonParameters</span></span>
<span data-ttu-id="bb0ae-134">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bb0ae-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bb0ae-135">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bb0ae-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bb0ae-136">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="bb0ae-136">INPUTS</span></span>

## <span data-ttu-id="bb0ae-137">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="bb0ae-137">OUTPUTS</span></span>

## <span data-ttu-id="bb0ae-138">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="bb0ae-138">NOTES</span></span>
* <span data-ttu-id="bb0ae-139">nod-dev, php-dev, python-dev</span><span class="sxs-lookup"><span data-stu-id="bb0ae-139">node-dev, php-dev, python-dev</span></span>

## <span data-ttu-id="bb0ae-140">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="bb0ae-140">RELATED LINKS</span></span>

