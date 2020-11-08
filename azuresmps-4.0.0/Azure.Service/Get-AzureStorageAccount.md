---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 7D7D1FAE-5360-428B-AAE9-9D1109A7B67F
online version: ''
schema: 2.0.0
ms.openlocfilehash: faccd241929beca1f2423fa9c23f35793233205b
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94093275"
---
# <span data-ttu-id="8e79a-101">Get-AzureStorageAccount</span><span class="sxs-lookup"><span data-stu-id="8e79a-101">Get-AzureStorageAccount</span></span>

## <span data-ttu-id="8e79a-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="8e79a-102">SYNOPSIS</span></span>
<span data-ttu-id="8e79a-103">Hämtar lagrings konton för det aktuella Azure-abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="8e79a-103">Gets the storage accounts for the current Azure subscription.</span></span>

## <span data-ttu-id="8e79a-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="8e79a-104">SYNTAX</span></span>

```
Get-AzureStorageAccount [[-StorageAccountName] <String>] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="8e79a-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="8e79a-105">DESCRIPTION</span></span>
<span data-ttu-id="8e79a-106">Cmdleten **Get-AzureStorageAccount** returnerar ett objekt som innehåller information om lagrings kontona för det aktuella abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="8e79a-106">The **Get-AzureStorageAccount** cmdlet returns an object containing information about the storage accounts for the current subscription.</span></span>
<span data-ttu-id="8e79a-107">Om parametern *StorageAccountName* anges returneras bara information om det angivna lagrings kontot.</span><span class="sxs-lookup"><span data-stu-id="8e79a-107">If the *StorageAccountName* parameter is specified, then only information about the specified storage account is returned.</span></span>

## <span data-ttu-id="8e79a-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="8e79a-108">EXAMPLES</span></span>

### <span data-ttu-id="8e79a-109">Exempel 1: returnera alla lagrings konton</span><span class="sxs-lookup"><span data-stu-id="8e79a-109">Example 1: Return all storage accounts</span></span>
```
PS C:\> Get-AzureStorageAccount
```

<span data-ttu-id="8e79a-110">Det här kommandot returnerar ett objekt med alla lagrings konton som är kopplade till det aktuella abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="8e79a-110">This command returns an object with all the storage accounts associated with the current subscription.</span></span>

### <span data-ttu-id="8e79a-111">Exempel 2: returnera konto information för ett angivet konto</span><span class="sxs-lookup"><span data-stu-id="8e79a-111">Example 2: Return account information for a specified account</span></span>
```
PS C:\> Get-AzureStorageAccount -StorageAccountName "ContosoStore01"
```

<span data-ttu-id="8e79a-112">Det här kommandot returnerar ett objekt med endast ContosoStore01-konto information.</span><span class="sxs-lookup"><span data-stu-id="8e79a-112">This command returns an object with only the ContosoStore01 account information.</span></span>

### <span data-ttu-id="8e79a-113">Exempel 3: Visa en tabell med lagrings konton</span><span class="sxs-lookup"><span data-stu-id="8e79a-113">Example 3: Display a table of storage accounts</span></span>
```
PS C:\> Get-AzureStorageAccount | Format-Table -AutoSize -Property @{Label="Name";Expression={$_.StorageAccountName}},"Label","Location"
```

<span data-ttu-id="8e79a-114">Det här kommandot returnerar ett objekt med alla lagrings konton som är kopplade till det aktuella abonnemanget och visar dem som en tabell med konto namnet, konto etiketten och lagrings platsen.</span><span class="sxs-lookup"><span data-stu-id="8e79a-114">This command returns an object with all the storage accounts associated with the current subscription, and outputs them as a table showing the account name, the account label, and the storage location.</span></span>

## <span data-ttu-id="8e79a-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="8e79a-115">PARAMETERS</span></span>

### <span data-ttu-id="8e79a-116">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="8e79a-116">-InformationAction</span></span>
<span data-ttu-id="8e79a-117">Anger hur den här cmdleten svarar på en informations händelse.</span><span class="sxs-lookup"><span data-stu-id="8e79a-117">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="8e79a-118">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="8e79a-118">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="8e79a-119">Vidare</span><span class="sxs-lookup"><span data-stu-id="8e79a-119">Continue</span></span>
- <span data-ttu-id="8e79a-120">Över</span><span class="sxs-lookup"><span data-stu-id="8e79a-120">Ignore</span></span>
- <span data-ttu-id="8e79a-121">Inquire</span><span class="sxs-lookup"><span data-stu-id="8e79a-121">Inquire</span></span>
- <span data-ttu-id="8e79a-122">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="8e79a-122">SilentlyContinue</span></span>
- <span data-ttu-id="8e79a-123">Stanna</span><span class="sxs-lookup"><span data-stu-id="8e79a-123">Stop</span></span>
- <span data-ttu-id="8e79a-124">Avbryt</span><span class="sxs-lookup"><span data-stu-id="8e79a-124">Suspend</span></span>

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

### <span data-ttu-id="8e79a-125">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="8e79a-125">-InformationVariable</span></span>
<span data-ttu-id="8e79a-126">Anger en informations variabel.</span><span class="sxs-lookup"><span data-stu-id="8e79a-126">Specifies an information variable.</span></span>

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

### <span data-ttu-id="8e79a-127">-Profil</span><span class="sxs-lookup"><span data-stu-id="8e79a-127">-Profile</span></span>
<span data-ttu-id="8e79a-128">Anger den Azure-profil från vilken denna cmdlet läser.</span><span class="sxs-lookup"><span data-stu-id="8e79a-128">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="8e79a-129">Om du inte anger en profil läser denna cmdlet från den lokala standard profilen.</span><span class="sxs-lookup"><span data-stu-id="8e79a-129">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="8e79a-130">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="8e79a-130">-StorageAccountName</span></span>
<span data-ttu-id="8e79a-131">Anger namnet på ett lagrings konto.</span><span class="sxs-lookup"><span data-stu-id="8e79a-131">Specifies the name of a storage account.</span></span>
<span data-ttu-id="8e79a-132">Om det här alternativet anges returnerar den här cmdleten bara det angivna lagrings konto objekt.</span><span class="sxs-lookup"><span data-stu-id="8e79a-132">If specified, this cmdlet returns only the specified storage account object.</span></span>

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

### <span data-ttu-id="8e79a-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8e79a-133">CommonParameters</span></span>
<span data-ttu-id="8e79a-134">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8e79a-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8e79a-135">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8e79a-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8e79a-136">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="8e79a-136">INPUTS</span></span>

## <span data-ttu-id="8e79a-137">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="8e79a-137">OUTPUTS</span></span>

### <span data-ttu-id="8e79a-138">ManagementOperationContext</span><span class="sxs-lookup"><span data-stu-id="8e79a-138">ManagementOperationContext</span></span>

## <span data-ttu-id="8e79a-139">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="8e79a-139">NOTES</span></span>
* <span data-ttu-id="8e79a-140">Skriv `help node-dev` för att få hjälp med Node.js utvecklingsbaserade cmdletar.</span><span class="sxs-lookup"><span data-stu-id="8e79a-140">Type `help node-dev` to get help on Node.js development-related cmdlets.</span></span> <span data-ttu-id="8e79a-141">Skriv `help php-dev` för att få hjälp med relevanta cmdlets för php-utveckling.</span><span class="sxs-lookup"><span data-stu-id="8e79a-141">Type `help php-dev` to get help on PHP development-related cmdlets.</span></span>

## <span data-ttu-id="8e79a-142">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="8e79a-142">RELATED LINKS</span></span>

[<span data-ttu-id="8e79a-143">New-AzureStorageAccount</span><span class="sxs-lookup"><span data-stu-id="8e79a-143">New-AzureStorageAccount</span></span>](./New-AzureStorageAccount.md)

[<span data-ttu-id="8e79a-144">Set-AzureStorageAccount</span><span class="sxs-lookup"><span data-stu-id="8e79a-144">Set-AzureStorageAccount</span></span>](./Set-AzureStorageAccount.md)


