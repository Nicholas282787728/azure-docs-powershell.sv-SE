---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 35588231-CBAC-4411-9531-9A06BD298ACA
online version: ''
schema: 2.0.0
ms.openlocfilehash: 7fdcad4b3a0f41f0589e49d4b33a767b93267855
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94093274"
---
# <span data-ttu-id="87440-101">Get-AzureStorageKey</span><span class="sxs-lookup"><span data-stu-id="87440-101">Get-AzureStorageKey</span></span>

## <span data-ttu-id="87440-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="87440-102">SYNOPSIS</span></span>
<span data-ttu-id="87440-103">Returnerar primära och sekundära lagrings konto nycklar för ett Azure Storage-konto.</span><span class="sxs-lookup"><span data-stu-id="87440-103">Returns the primary and secondary storage account keys for an Azure storage account.</span></span>

## <span data-ttu-id="87440-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="87440-104">SYNTAX</span></span>

```
Get-AzureStorageKey [-StorageAccountName] <String> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="87440-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="87440-105">DESCRIPTION</span></span>
<span data-ttu-id="87440-106">Cmdleten **Get-AzureStorageKey** returnerar ett objekt med namnet på Azure Storage-kontot, den primära konto-och den sekundära konto-tangenten för det angivna Azure Storage-kontot som egenskaper.</span><span class="sxs-lookup"><span data-stu-id="87440-106">The **Get-AzureStorageKey** cmdlet returns an object with the Azure Storage account name, the primary account key, and the secondary account key of the specified Azure storage account as properties.</span></span>

## <span data-ttu-id="87440-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="87440-107">EXAMPLES</span></span>

### <span data-ttu-id="87440-108">Exempel 1: Hämta ett objekt som innehåller primära och sekundära lagrings nycklar</span><span class="sxs-lookup"><span data-stu-id="87440-108">Example 1: Get an object that contains primary and secondary storage keys</span></span>
```
PS C:\> Get-AzureStorageKey -StorageAccountName "ContosoStore01"
```

<span data-ttu-id="87440-109">Det här kommandot får ett objekt med de primära och sekundära lagrings nycklarna för ContosoStore01 lagrings konto.</span><span class="sxs-lookup"><span data-stu-id="87440-109">This command gets an object with the primary and secondary storage keys for the ContosoStore01 storage account.</span></span>

### <span data-ttu-id="87440-110">Exempel 2: Hämta primär lagrings konto och lagra den i en variabel</span><span class="sxs-lookup"><span data-stu-id="87440-110">Example 2: Get the primary storage account key and store it in a variable</span></span>
```
PS C:\> $ContosoStoreKey = (Get-AzureStorageKey -StorageAccountName "ContosoStore01").Primary
```

<span data-ttu-id="87440-111">Det här kommandot placerar den primära lagrings konto-tangenten för ContosoStore01 lagrings konto i variabeln $ContosoStoreKey.</span><span class="sxs-lookup"><span data-stu-id="87440-111">This command puts the primary storage account key for the ContosoStore01 storage account in the $ContosoStoreKey variable.</span></span>

## <span data-ttu-id="87440-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="87440-112">PARAMETERS</span></span>

### <span data-ttu-id="87440-113">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="87440-113">-InformationAction</span></span>
<span data-ttu-id="87440-114">Anger hur den här cmdleten svarar på en informations händelse.</span><span class="sxs-lookup"><span data-stu-id="87440-114">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="87440-115">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="87440-115">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="87440-116">Vidare</span><span class="sxs-lookup"><span data-stu-id="87440-116">Continue</span></span>
- <span data-ttu-id="87440-117">Över</span><span class="sxs-lookup"><span data-stu-id="87440-117">Ignore</span></span>
- <span data-ttu-id="87440-118">Inquire</span><span class="sxs-lookup"><span data-stu-id="87440-118">Inquire</span></span>
- <span data-ttu-id="87440-119">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="87440-119">SilentlyContinue</span></span>
- <span data-ttu-id="87440-120">Stanna</span><span class="sxs-lookup"><span data-stu-id="87440-120">Stop</span></span>
- <span data-ttu-id="87440-121">Avbryt</span><span class="sxs-lookup"><span data-stu-id="87440-121">Suspend</span></span>

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

### <span data-ttu-id="87440-122">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="87440-122">-InformationVariable</span></span>
<span data-ttu-id="87440-123">Anger en informations variabel.</span><span class="sxs-lookup"><span data-stu-id="87440-123">Specifies an information variable.</span></span>

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

### <span data-ttu-id="87440-124">-Profil</span><span class="sxs-lookup"><span data-stu-id="87440-124">-Profile</span></span>
<span data-ttu-id="87440-125">Anger den Azure-profil från vilken denna cmdlet läser.</span><span class="sxs-lookup"><span data-stu-id="87440-125">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="87440-126">Om du inte anger en profil läser denna cmdlet från den lokala standard profilen.</span><span class="sxs-lookup"><span data-stu-id="87440-126">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="87440-127">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="87440-127">-StorageAccountName</span></span>
<span data-ttu-id="87440-128">Anger namnet på lagrings kontot.</span><span class="sxs-lookup"><span data-stu-id="87440-128">Specifies the storage account name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ServiceName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="87440-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="87440-129">CommonParameters</span></span>
<span data-ttu-id="87440-130">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="87440-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="87440-131">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="87440-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="87440-132">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="87440-132">INPUTS</span></span>

## <span data-ttu-id="87440-133">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="87440-133">OUTPUTS</span></span>

## <span data-ttu-id="87440-134">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="87440-134">NOTES</span></span>
* <span data-ttu-id="87440-135">Använd kommandot för att få hjälp med Node.js `help node-dev` .</span><span class="sxs-lookup"><span data-stu-id="87440-135">To get help with Node.js, use the `help node-dev` command.</span></span> <span data-ttu-id="87440-136">Använd kommandot för hjälp med PHP-tillägg `help php-dev` .</span><span class="sxs-lookup"><span data-stu-id="87440-136">For help with PHP extensions, use the `help php-dev` command.</span></span>

## <span data-ttu-id="87440-137">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="87440-137">RELATED LINKS</span></span>

[<span data-ttu-id="87440-138">Get-AzureStorageAccount</span><span class="sxs-lookup"><span data-stu-id="87440-138">Get-AzureStorageAccount</span></span>](./Get-AzureStorageAccount.md)

[<span data-ttu-id="87440-139">New-AzureStorageAccount</span><span class="sxs-lookup"><span data-stu-id="87440-139">New-AzureStorageAccount</span></span>](./New-AzureStorageAccount.md)

[<span data-ttu-id="87440-140">New-AzureStorageKey</span><span class="sxs-lookup"><span data-stu-id="87440-140">New-AzureStorageKey</span></span>](./New-AzureStorageKey.md)

[<span data-ttu-id="87440-141">Remove-AzureStorageAccount</span><span class="sxs-lookup"><span data-stu-id="87440-141">Remove-AzureStorageAccount</span></span>](./Remove-AzureStorageAccount.md)

[<span data-ttu-id="87440-142">Set-AzureStorageAccount</span><span class="sxs-lookup"><span data-stu-id="87440-142">Set-AzureStorageAccount</span></span>](./Set-AzureStorageAccount.md)


