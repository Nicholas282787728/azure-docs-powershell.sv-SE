---
external help file: Microsoft.WindowsAzure.Commands.RemoteApp.dll-Help.xml
ms.assetid: 0E5F05B3-F2B0-479C-8222-927C34140416
online version: ''
schema: 2.0.0
ms.openlocfilehash: 74892352afe02ae5eb2f19e05704c23c489d2d75
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94093358"
---
# <span data-ttu-id="840b0-101">Get-AzureRemoteAppCollectionUsageDetails</span><span class="sxs-lookup"><span data-stu-id="840b0-101">Get-AzureRemoteAppCollectionUsageDetails</span></span>

## <span data-ttu-id="840b0-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="840b0-102">SYNOPSIS</span></span>
<span data-ttu-id="840b0-103">Hämtar användnings information för en Azure RemoteApp-samling.</span><span class="sxs-lookup"><span data-stu-id="840b0-103">Retrieves usage details for an Azure RemoteApp collection.</span></span>

## <span data-ttu-id="840b0-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="840b0-104">SYNTAX</span></span>

```
Get-AzureRemoteAppCollectionUsageDetails [-CollectionName] <String> [[-UsageMonth] <String>]
 [[-UsageYear] <String>] [-AsJob] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="840b0-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="840b0-105">DESCRIPTION</span></span>
<span data-ttu-id="840b0-106">Cmdleten **Get-AzureRemoteAppCollectionUsageDetails** hämtar användnings information för en Azure RemoteApp-samling.</span><span class="sxs-lookup"><span data-stu-id="840b0-106">The **Get-AzureRemoteAppCollectionUsageDetails** cmdlet retrieves usage details for an Azure RemoteApp collection.</span></span>

## <span data-ttu-id="840b0-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="840b0-107">EXAMPLES</span></span>

### <span data-ttu-id="840b0-108">Exempel 1: Hämta användnings information för en samling</span><span class="sxs-lookup"><span data-stu-id="840b0-108">Example 1: Get usage details for a collection</span></span>
```
PS C:\> Get-AzureRemoteAppCollectionUsageDetails -CollectionName Contoso -UsageMonth 12 -UsageYear 2014
```

<span data-ttu-id="840b0-109">Det här kommandot får användnings information för december månad i Year 2014 för en Azure RemoteApp-samling med namnet contoso.</span><span class="sxs-lookup"><span data-stu-id="840b0-109">This command gets usage details for the month of December in the year 2014, for an Azure RemoteApp collection named Contoso.</span></span>

## <span data-ttu-id="840b0-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="840b0-110">PARAMETERS</span></span>

### <span data-ttu-id="840b0-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="840b0-111">-AsJob</span></span>
<span data-ttu-id="840b0-112">Anger att cmdleten körs i bakgrunden som ett Windows PowerShell-jobb.</span><span class="sxs-lookup"><span data-stu-id="840b0-112">Indicates that the cmdlet runs in the background as a Windows PowerShell job.</span></span>

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

### <span data-ttu-id="840b0-113">-Samlings namn</span><span class="sxs-lookup"><span data-stu-id="840b0-113">-CollectionName</span></span>
<span data-ttu-id="840b0-114">Anger namnet på Azure RemoteApp-samlingen.</span><span class="sxs-lookup"><span data-stu-id="840b0-114">Specifies the name of the Azure RemoteApp collection.</span></span>

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

### <span data-ttu-id="840b0-115">-Profil</span><span class="sxs-lookup"><span data-stu-id="840b0-115">-Profile</span></span>
<span data-ttu-id="840b0-116">Anger den Azure-profil från vilken denna cmdlet läser.</span><span class="sxs-lookup"><span data-stu-id="840b0-116">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="840b0-117">Om du inte anger en profil läser denna cmdlet från den lokala standard profilen.</span><span class="sxs-lookup"><span data-stu-id="840b0-117">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="840b0-118">-UsageMonth</span><span class="sxs-lookup"><span data-stu-id="840b0-118">-UsageMonth</span></span>
<span data-ttu-id="840b0-119">Anger ett tvåsiffrigt nummer för den månad som du vill få användnings information för.</span><span class="sxs-lookup"><span data-stu-id="840b0-119">Specifies a two-digit number for the month for which to get usage details.</span></span>

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

### <span data-ttu-id="840b0-120">-UsageYear</span><span class="sxs-lookup"><span data-stu-id="840b0-120">-UsageYear</span></span>
<span data-ttu-id="840b0-121">Anger det fyrsiffriga årtal som används för att få användnings information.</span><span class="sxs-lookup"><span data-stu-id="840b0-121">Specifies the four-digit year for which to get usage details.</span></span>

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

### <span data-ttu-id="840b0-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="840b0-122">CommonParameters</span></span>
<span data-ttu-id="840b0-123">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="840b0-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="840b0-124">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="840b0-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="840b0-125">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="840b0-125">INPUTS</span></span>

## <span data-ttu-id="840b0-126">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="840b0-126">OUTPUTS</span></span>

## <span data-ttu-id="840b0-127">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="840b0-127">NOTES</span></span>

## <span data-ttu-id="840b0-128">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="840b0-128">RELATED LINKS</span></span>

[<span data-ttu-id="840b0-129">Get-AzureRemoteAppCollection</span><span class="sxs-lookup"><span data-stu-id="840b0-129">Get-AzureRemoteAppCollection</span></span>](./Get-AzureRemoteAppCollection.md)

[<span data-ttu-id="840b0-130">Get-AzureRemoteAppCollectionUsageSummary</span><span class="sxs-lookup"><span data-stu-id="840b0-130">Get-AzureRemoteAppCollectionUsageSummary</span></span>](./Get-AzureRemoteAppCollectionUsageSummary.md)


