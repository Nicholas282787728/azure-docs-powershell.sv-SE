---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 679452A6-A6CA-4DC8-8E00-09E369505319
online version: ''
schema: 2.0.0
ms.openlocfilehash: 933c6de8e7baa55b2093a7ffc4ac28fede13bb5b
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94099688"
---
# <span data-ttu-id="c66aa-101">Remove-AzureStorageAccount</span><span class="sxs-lookup"><span data-stu-id="c66aa-101">Remove-AzureStorageAccount</span></span>

## <span data-ttu-id="c66aa-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="c66aa-102">SYNOPSIS</span></span>
<span data-ttu-id="c66aa-103">Tar bort angivet lagrings konto från ett abonnemang.</span><span class="sxs-lookup"><span data-stu-id="c66aa-103">Deletes the specified storage account from a subscription.</span></span>

## <span data-ttu-id="c66aa-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="c66aa-104">SYNTAX</span></span>

```
Remove-AzureStorageAccount [-StorageAccountName] <String> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="c66aa-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="c66aa-105">DESCRIPTION</span></span>
<span data-ttu-id="c66aa-106">Cmdleten **Remove-AzureStorageAccount** tar bort ett konto från en Azure-prenumeration.</span><span class="sxs-lookup"><span data-stu-id="c66aa-106">The **Remove-AzureStorageAccount** cmdlet removes an account from an Azure subscription.</span></span>

## <span data-ttu-id="c66aa-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="c66aa-107">EXAMPLES</span></span>

### <span data-ttu-id="c66aa-108">Exempel 1: ta bort ett lagrings konto</span><span class="sxs-lookup"><span data-stu-id="c66aa-108">Example 1: Remove a storage account</span></span>
```
PS C:\> Remove-AzureStorageAccount -StorageAccountName "ContosoStore01"
```

<span data-ttu-id="c66aa-109">Det här kommandot tar bort ContosoStore01 lagrings konto från det angivna abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="c66aa-109">This command removes the ContosoStore01 storage account from the specified subscription.</span></span>

## <span data-ttu-id="c66aa-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="c66aa-110">PARAMETERS</span></span>

### <span data-ttu-id="c66aa-111">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="c66aa-111">-InformationAction</span></span>
<span data-ttu-id="c66aa-112">Anger hur den här cmdleten svarar på en informations händelse.</span><span class="sxs-lookup"><span data-stu-id="c66aa-112">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="c66aa-113">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="c66aa-113">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="c66aa-114">Vidare</span><span class="sxs-lookup"><span data-stu-id="c66aa-114">Continue</span></span>
- <span data-ttu-id="c66aa-115">Över</span><span class="sxs-lookup"><span data-stu-id="c66aa-115">Ignore</span></span>
- <span data-ttu-id="c66aa-116">Inquire</span><span class="sxs-lookup"><span data-stu-id="c66aa-116">Inquire</span></span>
- <span data-ttu-id="c66aa-117">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="c66aa-117">SilentlyContinue</span></span>
- <span data-ttu-id="c66aa-118">Stanna</span><span class="sxs-lookup"><span data-stu-id="c66aa-118">Stop</span></span>
- <span data-ttu-id="c66aa-119">Avbryt</span><span class="sxs-lookup"><span data-stu-id="c66aa-119">Suspend</span></span>

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

### <span data-ttu-id="c66aa-120">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="c66aa-120">-InformationVariable</span></span>
<span data-ttu-id="c66aa-121">Anger en informations variabel.</span><span class="sxs-lookup"><span data-stu-id="c66aa-121">Specifies an information variable.</span></span>

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

### <span data-ttu-id="c66aa-122">-Profil</span><span class="sxs-lookup"><span data-stu-id="c66aa-122">-Profile</span></span>
<span data-ttu-id="c66aa-123">Anger den Azure-profil från vilken denna cmdlet läser.</span><span class="sxs-lookup"><span data-stu-id="c66aa-123">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="c66aa-124">Om du inte anger en profil läser denna cmdlet från den lokala standard profilen.</span><span class="sxs-lookup"><span data-stu-id="c66aa-124">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="c66aa-125">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="c66aa-125">-StorageAccountName</span></span>
<span data-ttu-id="c66aa-126">Anger namnet på det lagrings konto som ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="c66aa-126">Specifies the name of the storage account to remove.</span></span>

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

### <span data-ttu-id="c66aa-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c66aa-127">CommonParameters</span></span>
<span data-ttu-id="c66aa-128">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c66aa-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c66aa-129">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c66aa-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c66aa-130">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="c66aa-130">INPUTS</span></span>

## <span data-ttu-id="c66aa-131">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="c66aa-131">OUTPUTS</span></span>

## <span data-ttu-id="c66aa-132">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="c66aa-132">NOTES</span></span>

## <span data-ttu-id="c66aa-133">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="c66aa-133">RELATED LINKS</span></span>

[<span data-ttu-id="c66aa-134">Get-AzureStorageAccount</span><span class="sxs-lookup"><span data-stu-id="c66aa-134">Get-AzureStorageAccount</span></span>](./Get-AzureStorageAccount.md)

[<span data-ttu-id="c66aa-135">New-AzureStorageAccount</span><span class="sxs-lookup"><span data-stu-id="c66aa-135">New-AzureStorageAccount</span></span>](./New-AzureStorageAccount.md)

[<span data-ttu-id="c66aa-136">Set-AzureStorageAccount</span><span class="sxs-lookup"><span data-stu-id="c66aa-136">Set-AzureStorageAccount</span></span>](./Set-AzureStorageAccount.md)


