---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: A1327796-0CDC-43E0-97A6-FD1BF570066F
online version: ''
schema: 2.0.0
ms.openlocfilehash: c8676fbf957ebe96f0e849eedd3f64aca19a7741
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94099565"
---
# <span data-ttu-id="f1e3f-101">Get-AzureMediaServicesAccount</span><span class="sxs-lookup"><span data-stu-id="f1e3f-101">Get-AzureMediaServicesAccount</span></span>

## <span data-ttu-id="f1e3f-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="f1e3f-102">SYNOPSIS</span></span>
<span data-ttu-id="f1e3f-103">Får tillgängliga Azure Media Services-konton.</span><span class="sxs-lookup"><span data-stu-id="f1e3f-103">Gets the available Azure Media Services accounts.</span></span>

<span data-ttu-id="f1e3f-104">**Obs!** Den här versionen är föråldrad, se den [senaste versionen](https://docs.microsoft.com/powershell/module/azurerm.media/?view=azurermps-5.4.0#media_services).</span><span class="sxs-lookup"><span data-stu-id="f1e3f-104">**Note:** This version is deprecated, please see the [newer version](https://docs.microsoft.com/powershell/module/azurerm.media/?view=azurermps-5.4.0#media_services).</span></span>

## <span data-ttu-id="f1e3f-105">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="f1e3f-105">SYNTAX</span></span>

```
Get-AzureMediaServicesAccount [-Name <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="f1e3f-106">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="f1e3f-106">DESCRIPTION</span></span>
<span data-ttu-id="f1e3f-107">I det här avsnittet beskrivs cmdleten i 0.8.10-versionen av Microsoft Azure PowerShell-modulen.</span><span class="sxs-lookup"><span data-stu-id="f1e3f-107">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="f1e3f-108">För att få den version av modulen du använder, gå till Azure PowerShell-konsolen och skriv `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="f1e3f-108">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="f1e3f-109">Om du vill visa alla konton använder du `Get-AzureMediaServicesAccount` cmdleten.</span><span class="sxs-lookup"><span data-stu-id="f1e3f-109">To list all the accounts, use the `Get-AzureMediaServicesAccount` cmdlet.</span></span>
<span data-ttu-id="f1e3f-110">Om du vill ha mer detaljerad information om ett visst konto använder du `Get-AzureMediaServicesAccount -Name YourAccountName` cmdleten.</span><span class="sxs-lookup"><span data-stu-id="f1e3f-110">To get more detailed information about a specific account, use the `Get-AzureMediaServicesAccount -Name YourAccountName` cmdlet.</span></span>

## <span data-ttu-id="f1e3f-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="f1e3f-111">EXAMPLES</span></span>

### <span data-ttu-id="f1e3f-112">Exempel 1: lista alla medie tjänst konton</span><span class="sxs-lookup"><span data-stu-id="f1e3f-112">Example 1: List all Media Services accounts</span></span>
```
PS C:\> Get-AzureMediaServicesAccount
```

<span data-ttu-id="f1e3f-113">Det här kommandot visar alla tillgängliga medie tjänst konton.</span><span class="sxs-lookup"><span data-stu-id="f1e3f-113">This command lists all available Media Services accounts.</span></span>

### <span data-ttu-id="f1e3f-114">Exempel 2: få detaljerad information om ett media tjänst konto</span><span class="sxs-lookup"><span data-stu-id="f1e3f-114">Example 2: Get detailed information about a Media Services account</span></span>
```
PS C:\> Get-AzureMediaServicesAccount -Name accountname
```

<span data-ttu-id="f1e3f-115">Det här kommandot visar egenskaper för ett Media Services-konto.</span><span class="sxs-lookup"><span data-stu-id="f1e3f-115">This command displays properties of a Media Services account.</span></span>

## <span data-ttu-id="f1e3f-116">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="f1e3f-116">PARAMETERS</span></span>

### <span data-ttu-id="f1e3f-117">-Namn</span><span class="sxs-lookup"><span data-stu-id="f1e3f-117">-Name</span></span>
<span data-ttu-id="f1e3f-118">Medie tjänstens konto namn.</span><span class="sxs-lookup"><span data-stu-id="f1e3f-118">The Media Services account name.</span></span>

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

### <span data-ttu-id="f1e3f-119">-Profil</span><span class="sxs-lookup"><span data-stu-id="f1e3f-119">-Profile</span></span>
<span data-ttu-id="f1e3f-120">Anger den Azure-profil från vilken denna cmdlet läser.</span><span class="sxs-lookup"><span data-stu-id="f1e3f-120">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="f1e3f-121">Om du inte anger en profil läser denna cmdlet från den lokala standard profilen.</span><span class="sxs-lookup"><span data-stu-id="f1e3f-121">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="f1e3f-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f1e3f-122">CommonParameters</span></span>
<span data-ttu-id="f1e3f-123">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f1e3f-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f1e3f-124">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f1e3f-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f1e3f-125">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="f1e3f-125">INPUTS</span></span>

## <span data-ttu-id="f1e3f-126">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="f1e3f-126">OUTPUTS</span></span>

## <span data-ttu-id="f1e3f-127">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="f1e3f-127">NOTES</span></span>

## <span data-ttu-id="f1e3f-128">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="f1e3f-128">RELATED LINKS</span></span>

[<span data-ttu-id="f1e3f-129">Använda Azure PowerShell för medie tjänster</span><span class="sxs-lookup"><span data-stu-id="f1e3f-129">How to use Azure PowerShell for Media Services</span></span>](https://go.microsoft.com/fwlink/?LinkId=324179)


