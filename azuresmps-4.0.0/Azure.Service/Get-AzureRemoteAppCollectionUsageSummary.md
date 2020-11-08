---
external help file: Microsoft.WindowsAzure.Commands.RemoteApp.dll-Help.xml
ms.assetid: 8EF86C66-498F-4183-9070-F178628483F1
online version: ''
schema: 2.0.0
ms.openlocfilehash: 91c32ca5207efdff7fa65fbba599f44d276dab6d
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94099560"
---
# <span data-ttu-id="3e704-101">Get-AzureRemoteAppCollectionUsageSummary</span><span class="sxs-lookup"><span data-stu-id="3e704-101">Get-AzureRemoteAppCollectionUsageSummary</span></span>

## <span data-ttu-id="3e704-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="3e704-102">SYNOPSIS</span></span>
<span data-ttu-id="3e704-103">Hämtar en användnings översikt för en Azure RemoteApp-samling.</span><span class="sxs-lookup"><span data-stu-id="3e704-103">Retrieves a usage summary for an Azure RemoteApp collection.</span></span>

## <span data-ttu-id="3e704-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="3e704-104">SYNTAX</span></span>

```
Get-AzureRemoteAppCollectionUsageSummary [-CollectionName] <String> [[-UsageMonth] <String>]
 [[-UsageYear] <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="3e704-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="3e704-105">DESCRIPTION</span></span>
<span data-ttu-id="3e704-106">Cmdleten **Get-AzureRemoteAppCollectionUsageSummary** returnerar en användnings översikt för en Azure RemoteApp-samling.</span><span class="sxs-lookup"><span data-stu-id="3e704-106">The **Get-AzureRemoteAppCollectionUsageSummary** cmdlet retrieves a usage summary for an Azure RemoteApp collection.</span></span>

## <span data-ttu-id="3e704-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="3e704-107">EXAMPLES</span></span>

### <span data-ttu-id="3e704-108">Exempel 1: få en översikt över användning</span><span class="sxs-lookup"><span data-stu-id="3e704-108">Example 1: Get a usage summary</span></span>
```
PS C:\> Get-AzureRemoteAppCollectionUsageSummary -CollectionName Contoso -UsageMonth 12 -UsageYear 2014
```

<span data-ttu-id="3e704-109">Det här kommandot får en användnings översikt för december månad under året 2014 för en samling med namnet contoso.</span><span class="sxs-lookup"><span data-stu-id="3e704-109">This command gets a usage summary for the month of December in the year 2014, for a collection named Contoso.</span></span>

## <span data-ttu-id="3e704-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="3e704-110">PARAMETERS</span></span>

### <span data-ttu-id="3e704-111">-Samlings namn</span><span class="sxs-lookup"><span data-stu-id="3e704-111">-CollectionName</span></span>
<span data-ttu-id="3e704-112">Anger namnet på Azure RemoteApp-samlingen.</span><span class="sxs-lookup"><span data-stu-id="3e704-112">Specifies the name of the Azure RemoteApp collection.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3e704-113">-Profil</span><span class="sxs-lookup"><span data-stu-id="3e704-113">-Profile</span></span>
<span data-ttu-id="3e704-114">Anger den Azure-profil från vilken denna cmdlet läser.</span><span class="sxs-lookup"><span data-stu-id="3e704-114">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="3e704-115">Om du inte anger en profil läser denna cmdlet från den lokala standard profilen.</span><span class="sxs-lookup"><span data-stu-id="3e704-115">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="3e704-116">-UsageMonth</span><span class="sxs-lookup"><span data-stu-id="3e704-116">-UsageMonth</span></span>
<span data-ttu-id="3e704-117">Anger ett tvåsiffrigt nummer för den månad för vilken en användnings översikt ska visas.</span><span class="sxs-lookup"><span data-stu-id="3e704-117">Specifies a two digit number for the month for which to get a usage summary.</span></span>
<span data-ttu-id="3e704-118">Om den här parametern inte anges används den här cmdleten för den aktuella månaden.</span><span class="sxs-lookup"><span data-stu-id="3e704-118">If this parameter is not specified, this cmdlet provides usage for the current month.</span></span>

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

### <span data-ttu-id="3e704-119">-UsageYear</span><span class="sxs-lookup"><span data-stu-id="3e704-119">-UsageYear</span></span>
<span data-ttu-id="3e704-120">Anger det fyrsiffriga årtal som en användnings översikt ska få.</span><span class="sxs-lookup"><span data-stu-id="3e704-120">Specifies the four-digit year for which to get a usage summary.</span></span>
<span data-ttu-id="3e704-121">Om den här parametern inte anges innehåller denna cmdlet en användnings översikt för det aktuella året.</span><span class="sxs-lookup"><span data-stu-id="3e704-121">If this parameter is not specified, this cmdlet provides a usage summary for the current year will be used.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3e704-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3e704-122">CommonParameters</span></span>
<span data-ttu-id="3e704-123">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3e704-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3e704-124">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3e704-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3e704-125">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="3e704-125">INPUTS</span></span>

## <span data-ttu-id="3e704-126">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="3e704-126">OUTPUTS</span></span>

## <span data-ttu-id="3e704-127">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="3e704-127">NOTES</span></span>

## <span data-ttu-id="3e704-128">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="3e704-128">RELATED LINKS</span></span>

[<span data-ttu-id="3e704-129">Get-AzureRemoteAppCollection</span><span class="sxs-lookup"><span data-stu-id="3e704-129">Get-AzureRemoteAppCollection</span></span>](./Get-AzureRemoteAppCollection.md)

[<span data-ttu-id="3e704-130">Get-AzureRemoteAppCollectionUsageDetails</span><span class="sxs-lookup"><span data-stu-id="3e704-130">Get-AzureRemoteAppCollectionUsageDetails</span></span>](./Get-AzureRemoteAppCollectionUsageDetails.md)


