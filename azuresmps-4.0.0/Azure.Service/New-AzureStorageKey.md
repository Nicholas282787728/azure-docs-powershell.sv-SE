---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 09ABE9E2-1080-4DEF-92DD-B8FF4C8B308C
online version: ''
schema: 2.0.0
ms.openlocfilehash: 9afdaafa57592239d0c24870e4459d650fac84c3
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94099433"
---
# <span data-ttu-id="6e21c-101">New-AzureStorageKey</span><span class="sxs-lookup"><span data-stu-id="6e21c-101">New-AzureStorageKey</span></span>

## <span data-ttu-id="6e21c-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="6e21c-102">SYNOPSIS</span></span>
<span data-ttu-id="6e21c-103">Återskapar lagrings nycklar för ett Azure Storage-konto.</span><span class="sxs-lookup"><span data-stu-id="6e21c-103">Regenerates storage keys for an Azure storage account.</span></span>

## <span data-ttu-id="6e21c-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="6e21c-104">SYNTAX</span></span>

```
New-AzureStorageKey [-KeyType] <String> [-StorageAccountName] <String> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="6e21c-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="6e21c-105">DESCRIPTION</span></span>
<span data-ttu-id="6e21c-106">**New-AzureStorageKey** cmdlet återskapar den primära eller sekundära nyckeln för ett Azure Storage-konto.</span><span class="sxs-lookup"><span data-stu-id="6e21c-106">The **New-AzureStorageKey** cmdlet regenerates the primary or secondary key for an Azure Storage account.</span></span>
<span data-ttu-id="6e21c-107">Det returnerar ett objekt som innehåller lagrings kontots namn, primär nycklar och sekundära nycklar som egenskaper.</span><span class="sxs-lookup"><span data-stu-id="6e21c-107">It returns an object that contains the storage account name, primary key, and secondary key as properties.</span></span>

## <span data-ttu-id="6e21c-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="6e21c-108">EXAMPLES</span></span>

### <span data-ttu-id="6e21c-109">Exempel 1: återskapa en primär lagrings nyckeln</span><span class="sxs-lookup"><span data-stu-id="6e21c-109">Example 1: Regenerate a primary storage key</span></span>
```
PS C:\> New-AzureStorageKey -KeyType "Primary" -StorageAccountName "ContosoStore01"
```

<span data-ttu-id="6e21c-110">Det här kommandot återskapar den primära lagrings nyckeln för ContosoStore01 lagrings konto.</span><span class="sxs-lookup"><span data-stu-id="6e21c-110">This command regenerates the primary storage key for the ContosoStore01 storage account.</span></span>

### <span data-ttu-id="6e21c-111">Exempel 2: återskapa en sekundär lagrings nyckeln och spara den i en variabel</span><span class="sxs-lookup"><span data-stu-id="6e21c-111">Example 2: Regenerate a secondary storage key and save it in a variable</span></span>
```
PS C:\> $ContosoStoreKey = New-AzureStorageKey -KeyType "Secondary" -StorageAccountName "ContosoStore01"
```

<span data-ttu-id="6e21c-112">Det här kommandot återskapa den sekundära lagrings nyckeln för ContosoStore01 lagrings konto och lagrar den uppdaterade informationen om lagrings konto nyckeln i $ContosoStoreKey.</span><span class="sxs-lookup"><span data-stu-id="6e21c-112">This command regenerate the secondary storage key for the ContosoStore01 storage account and stores the updated storage account key information in the $ContosoStoreKey.</span></span>

## <span data-ttu-id="6e21c-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="6e21c-113">PARAMETERS</span></span>

### <span data-ttu-id="6e21c-114">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="6e21c-114">-InformationAction</span></span>
<span data-ttu-id="6e21c-115">Anger hur den här cmdleten svarar på en informations händelse.</span><span class="sxs-lookup"><span data-stu-id="6e21c-115">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="6e21c-116">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="6e21c-116">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="6e21c-117">Vidare</span><span class="sxs-lookup"><span data-stu-id="6e21c-117">Continue</span></span>
- <span data-ttu-id="6e21c-118">Över</span><span class="sxs-lookup"><span data-stu-id="6e21c-118">Ignore</span></span>
- <span data-ttu-id="6e21c-119">Inquire</span><span class="sxs-lookup"><span data-stu-id="6e21c-119">Inquire</span></span>
- <span data-ttu-id="6e21c-120">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="6e21c-120">SilentlyContinue</span></span>
- <span data-ttu-id="6e21c-121">Stanna</span><span class="sxs-lookup"><span data-stu-id="6e21c-121">Stop</span></span>
- <span data-ttu-id="6e21c-122">Avbryt</span><span class="sxs-lookup"><span data-stu-id="6e21c-122">Suspend</span></span>

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

### <span data-ttu-id="6e21c-123">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="6e21c-123">-InformationVariable</span></span>
<span data-ttu-id="6e21c-124">Anger en informations variabel.</span><span class="sxs-lookup"><span data-stu-id="6e21c-124">Specifies an information variable.</span></span>

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

### <span data-ttu-id="6e21c-125">-Värdetyp</span><span class="sxs-lookup"><span data-stu-id="6e21c-125">-KeyType</span></span>
<span data-ttu-id="6e21c-126">Anger vilken nyckeln som ska skapas.</span><span class="sxs-lookup"><span data-stu-id="6e21c-126">Specifies which key to regenerate.</span></span>
<span data-ttu-id="6e21c-127">Giltiga värden är: primära och sekundära.</span><span class="sxs-lookup"><span data-stu-id="6e21c-127">Valid values are: Primary and Secondary.</span></span>

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

### <span data-ttu-id="6e21c-128">-Profil</span><span class="sxs-lookup"><span data-stu-id="6e21c-128">-Profile</span></span>
<span data-ttu-id="6e21c-129">Anger den Azure-profil från vilken denna cmdlet läser.</span><span class="sxs-lookup"><span data-stu-id="6e21c-129">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="6e21c-130">Om du inte anger en profil läser denna cmdlet från den lokala standard profilen.</span><span class="sxs-lookup"><span data-stu-id="6e21c-130">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="6e21c-131">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="6e21c-131">-StorageAccountName</span></span>
<span data-ttu-id="6e21c-132">Anger namnet på det Azure Storage-konto som du vill återskapa en nyckeln för.</span><span class="sxs-lookup"><span data-stu-id="6e21c-132">Specifies the name of the Azure Storage account for which to regenerate a key.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ServiceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6e21c-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6e21c-133">CommonParameters</span></span>
<span data-ttu-id="6e21c-134">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6e21c-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6e21c-135">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6e21c-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6e21c-136">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="6e21c-136">INPUTS</span></span>

## <span data-ttu-id="6e21c-137">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="6e21c-137">OUTPUTS</span></span>

### <span data-ttu-id="6e21c-138">StorageServiceKeys</span><span class="sxs-lookup"><span data-stu-id="6e21c-138">StorageServiceKeys</span></span>

## <span data-ttu-id="6e21c-139">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="6e21c-139">NOTES</span></span>

## <span data-ttu-id="6e21c-140">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="6e21c-140">RELATED LINKS</span></span>

[<span data-ttu-id="6e21c-141">Get-AzureStorageKey</span><span class="sxs-lookup"><span data-stu-id="6e21c-141">Get-AzureStorageKey</span></span>](./Get-AzureStorageKey.md)


