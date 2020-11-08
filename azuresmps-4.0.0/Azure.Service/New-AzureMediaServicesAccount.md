---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 6C4081EE-0BCD-4285-8ABB-778BD95BFE4F
online version: ''
schema: 2.0.0
ms.openlocfilehash: 37f6e5b1152af79b2fc199199bf2b872bfbfa4ec
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94099141"
---
# <span data-ttu-id="b5098-101">New-AzureMediaServicesAccount</span><span class="sxs-lookup"><span data-stu-id="b5098-101">New-AzureMediaServicesAccount</span></span>

## <span data-ttu-id="b5098-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="b5098-102">SYNOPSIS</span></span>
<span data-ttu-id="b5098-103">Skapar ett Azure Media Services-konto.</span><span class="sxs-lookup"><span data-stu-id="b5098-103">Creates an Azure Media Services account.</span></span>

<span data-ttu-id="b5098-104">**Obs!** Den här versionen är föråldrad, se den [senaste versionen](https://docs.microsoft.com/powershell/module/azurerm.media/?view=azurermps-5.4.0#media_services).</span><span class="sxs-lookup"><span data-stu-id="b5098-104">**Note:** This version is deprecated, please see the [newer version](https://docs.microsoft.com/powershell/module/azurerm.media/?view=azurermps-5.4.0#media_services).</span></span>

## <span data-ttu-id="b5098-105">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="b5098-105">SYNTAX</span></span>

```
New-AzureMediaServicesAccount -Name <String> -Location <String> -StorageAccountName <String>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="b5098-106">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="b5098-106">DESCRIPTION</span></span>
<span data-ttu-id="b5098-107">I det här avsnittet beskrivs cmdleten i 0.8.10-versionen av Microsoft Azure PowerShell-modulen.</span><span class="sxs-lookup"><span data-stu-id="b5098-107">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="b5098-108">För att få den version av modulen du använder, gå till Azure PowerShell-konsolen och skriv `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="b5098-108">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="b5098-109">Cmdleten **New-AzureMediaServicesAccount** skapar ett nytt Media tjänst konto med det angivna medie tjänst konto namnet, data Center platsen där du vill skapa kontot och ett befintligt lagrings konto namn.</span><span class="sxs-lookup"><span data-stu-id="b5098-109">The **New-AzureMediaServicesAccount** cmdlet creates a new Media Services account with the specified Media Services account name, datacenter location where you want to create the account, and an existing storage account name.</span></span>
<span data-ttu-id="b5098-110">Lagrings kontot måste finnas i samma data Center som det nya medie tjänst kontot.</span><span class="sxs-lookup"><span data-stu-id="b5098-110">The storage account has to be located in the same data center as the new Media Services account.</span></span>

## <span data-ttu-id="b5098-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="b5098-111">EXAMPLES</span></span>

### <span data-ttu-id="b5098-112">Exempel 1: skapa ett nytt Media tjänst konto</span><span class="sxs-lookup"><span data-stu-id="b5098-112">Example 1: Create a new Media Services account</span></span>
```
PS C:\> New-AzureMediaServicesAccount -Name "mediaserviceaccount" -StorageAccountName "storageaccount " -Location "West US"
```

## <span data-ttu-id="b5098-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="b5098-113">PARAMETERS</span></span>

### <span data-ttu-id="b5098-114">-Plats</span><span class="sxs-lookup"><span data-stu-id="b5098-114">-Location</span></span>
<span data-ttu-id="b5098-115">Anger platsen för medie tjänstens Data Center.</span><span class="sxs-lookup"><span data-stu-id="b5098-115">Specifies the Media Services datacenter location.</span></span>

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

### <span data-ttu-id="b5098-116">-Namn</span><span class="sxs-lookup"><span data-stu-id="b5098-116">-Name</span></span>
<span data-ttu-id="b5098-117">Anger namnet på medie tjänstens konto.</span><span class="sxs-lookup"><span data-stu-id="b5098-117">Specifies the Media Services account name.</span></span>

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

### <span data-ttu-id="b5098-118">-Profil</span><span class="sxs-lookup"><span data-stu-id="b5098-118">-Profile</span></span>
<span data-ttu-id="b5098-119">Anger den Azure-profil från vilken denna cmdlet läser.</span><span class="sxs-lookup"><span data-stu-id="b5098-119">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="b5098-120">Om du inte anger en profil läser denna cmdlet från den lokala standard profilen.</span><span class="sxs-lookup"><span data-stu-id="b5098-120">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="b5098-121">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="b5098-121">-StorageAccountName</span></span>
<span data-ttu-id="b5098-122">Anger namnet på lagrings kontot.</span><span class="sxs-lookup"><span data-stu-id="b5098-122">Specifies the storage account name.</span></span>
<span data-ttu-id="b5098-123">Lagrings kontot måste redan finnas i samma data Center som det nya medie tjänst kontot.</span><span class="sxs-lookup"><span data-stu-id="b5098-123">The storage account must already exist in the same datacenter as the new Media Services account.</span></span>

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

### <span data-ttu-id="b5098-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b5098-124">CommonParameters</span></span>
<span data-ttu-id="b5098-125">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b5098-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b5098-126">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b5098-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b5098-127">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="b5098-127">INPUTS</span></span>

## <span data-ttu-id="b5098-128">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="b5098-128">OUTPUTS</span></span>

## <span data-ttu-id="b5098-129">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="b5098-129">NOTES</span></span>

## <span data-ttu-id="b5098-130">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="b5098-130">RELATED LINKS</span></span>

[<span data-ttu-id="b5098-131">Använda Azure PowerShell för medie tjänster</span><span class="sxs-lookup"><span data-stu-id="b5098-131">How to use Azure PowerShell for Media Services</span></span>](https://go.microsoft.com/fwlink/?LinkId=324179)

[<span data-ttu-id="b5098-132">Get-AzureMediaServicesAccount</span><span class="sxs-lookup"><span data-stu-id="b5098-132">Get-AzureMediaServicesAccount</span></span>](./Get-AzureMediaServicesAccount.md)

[<span data-ttu-id="b5098-133">Remove-AzureMediaServicesAccount</span><span class="sxs-lookup"><span data-stu-id="b5098-133">Remove-AzureMediaServicesAccount</span></span>](./Remove-AzureMediaServicesAccount.md)


