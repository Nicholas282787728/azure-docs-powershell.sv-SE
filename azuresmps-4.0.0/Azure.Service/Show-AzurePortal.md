---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 7ABEC06E-1046-401E-B4A1-902FC3EED867
online version: ''
schema: 2.0.0
ms.openlocfilehash: b0f0ff81fc38916adeedbb495117a8b27a1f88fb
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94099178"
---
# <span data-ttu-id="46268-101">Show-AzurePortal</span><span class="sxs-lookup"><span data-stu-id="46268-101">Show-AzurePortal</span></span>

## <span data-ttu-id="46268-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="46268-102">SYNOPSIS</span></span>
<span data-ttu-id="46268-103">Visa Azure-hanteringskonsolen.</span><span class="sxs-lookup"><span data-stu-id="46268-103">Show the Azure Management Portal.</span></span>

## <span data-ttu-id="46268-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="46268-104">SYNTAX</span></span>

```
Show-AzurePortal [-Name <String>] [-Realm <String>] [-Environment <String>] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="46268-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="46268-105">DESCRIPTION</span></span>
<span data-ttu-id="46268-106">I det här avsnittet beskrivs cmdleten i 0.8.10-versionen av Microsoft Azure PowerShell-modulen.</span><span class="sxs-lookup"><span data-stu-id="46268-106">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="46268-107">För att få den version av modulen du använder, gå till Azure PowerShell-konsolen och skriv `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="46268-107">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="46268-108">Cmdleten **show-AzurePortal** visar Azure Management-portalen.</span><span class="sxs-lookup"><span data-stu-id="46268-108">The **Show-AzurePortal** cmdlet shows the Azure Management Portal.</span></span>

## <span data-ttu-id="46268-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="46268-109">EXAMPLES</span></span>

### <span data-ttu-id="46268-110">Exempel 1: Visa information om en webbplats</span><span class="sxs-lookup"><span data-stu-id="46268-110">Example 1: Show information about a web site</span></span>
```
PS C:\> Show-AzurePortal -Name mySite
```

<span data-ttu-id="46268-111">I det här exemplet öppnas en webbläsare på Azure-portalen med information om en webbplats som heter min webbplats.</span><span class="sxs-lookup"><span data-stu-id="46268-111">This example opens a browser on the Azure portal, showing information about a web site named mySite.</span></span>

## <span data-ttu-id="46268-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="46268-112">PARAMETERS</span></span>

### <span data-ttu-id="46268-113">-Miljö</span><span class="sxs-lookup"><span data-stu-id="46268-113">-Environment</span></span>
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

### <span data-ttu-id="46268-114">-Namn</span><span class="sxs-lookup"><span data-stu-id="46268-114">-Name</span></span>
<span data-ttu-id="46268-115">Anger namnet på den webbplats som ska visas i portalen.</span><span class="sxs-lookup"><span data-stu-id="46268-115">Specifies the name of the website to show in the portal.</span></span>

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

### <span data-ttu-id="46268-116">-Profil</span><span class="sxs-lookup"><span data-stu-id="46268-116">-Profile</span></span>
<span data-ttu-id="46268-117">Anger den Azure-profil från vilken denna cmdlet läser.</span><span class="sxs-lookup"><span data-stu-id="46268-117">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="46268-118">Om du inte anger en profil läser denna cmdlet från den lokala standard profilen.</span><span class="sxs-lookup"><span data-stu-id="46268-118">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="46268-119">-Realm</span><span class="sxs-lookup"><span data-stu-id="46268-119">-Realm</span></span>
<span data-ttu-id="46268-120">Anger det organisations-ID som ska användas för federerad inloggningsautentisering när Azure-portalen visas.</span><span class="sxs-lookup"><span data-stu-id="46268-120">Specifies the organization ID to use for federated authentication when displaying the Azure Portal.</span></span>

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

### <span data-ttu-id="46268-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="46268-121">CommonParameters</span></span>
<span data-ttu-id="46268-122">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="46268-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="46268-123">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="46268-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="46268-124">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="46268-124">INPUTS</span></span>

## <span data-ttu-id="46268-125">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="46268-125">OUTPUTS</span></span>

## <span data-ttu-id="46268-126">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="46268-126">NOTES</span></span>

## <span data-ttu-id="46268-127">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="46268-127">RELATED LINKS</span></span>

[<span data-ttu-id="46268-128">Show-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="46268-128">Show-AzureWebsite</span></span>](./Show-AzureWebsite.md)


