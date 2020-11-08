---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 3422EFD0-88DC-4DF0-868C-5C63C9FA95EF
online version: ''
schema: 2.0.0
ms.openlocfilehash: d9aa78f34abf17c2aa5858697f492f76ee124d91
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94093416"
---
# <span data-ttu-id="ef4dd-101">Disable-AzureWebsiteApplicationDiagnostic</span><span class="sxs-lookup"><span data-stu-id="ef4dd-101">Disable-AzureWebsiteApplicationDiagnostic</span></span>

## <span data-ttu-id="ef4dd-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="ef4dd-102">SYNOPSIS</span></span>
<span data-ttu-id="ef4dd-103">Inaktiverar Application Diagnostics för en Azure-webbplats.</span><span class="sxs-lookup"><span data-stu-id="ef4dd-103">Disables application diagnostics for an Azure website.</span></span>

## <span data-ttu-id="ef4dd-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="ef4dd-104">SYNTAX</span></span>

```
Disable-AzureWebsiteApplicationDiagnostic [-PassThru] [-File] [-TableStorage] [-BlobStorage] [-Name <String>]
 [-Slot <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="ef4dd-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="ef4dd-105">DESCRIPTION</span></span>
<span data-ttu-id="ef4dd-106">I det här avsnittet beskrivs cmdleten i 0.8.10-versionen av Microsoft Azure PowerShell-modulen.</span><span class="sxs-lookup"><span data-stu-id="ef4dd-106">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="ef4dd-107">För att få den version av modulen du använder, gå till Azure PowerShell-konsolen och skriv `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="ef4dd-107">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="ef4dd-108">Inaktiverar Application Diagnostics för en Azure-webbplats.</span><span class="sxs-lookup"><span data-stu-id="ef4dd-108">Disables application diagnostics for an Azure website.</span></span>
<span data-ttu-id="ef4dd-109">Inaktiverar loggning som är konfigurerad för att lagras på ett fil system eller på Azure.</span><span class="sxs-lookup"><span data-stu-id="ef4dd-109">Disables logging configured to be stored on a file system or on Azure.</span></span>

## <span data-ttu-id="ef4dd-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="ef4dd-110">EXAMPLES</span></span>

### <span data-ttu-id="ef4dd-111">Exempel 1: inaktivera loggnings filen för program</span><span class="sxs-lookup"><span data-stu-id="ef4dd-111">Example 1:  Disable application logging file</span></span>
```
PS C:\> Disable-AzureWebsiteApplicationDiagnostic -Name MyWebsite -File
```

<span data-ttu-id="ef4dd-112">Följande exempel inaktiverar program loggning i fil systemet.</span><span class="sxs-lookup"><span data-stu-id="ef4dd-112">The following example disables application logging on the file system.</span></span>

### <span data-ttu-id="ef4dd-113">Exempel 2: inaktivera loggning med Azure Storage</span><span class="sxs-lookup"><span data-stu-id="ef4dd-113">Example 2:  Disable logging using Azure storage</span></span>
```
PS C:\> Disable-AzureWebsiteApplicationDiagnostic -Name MyWebsite -Storage
```

<span data-ttu-id="ef4dd-114">I följande exempel inaktive ras program loggning med lagring.</span><span class="sxs-lookup"><span data-stu-id="ef4dd-114">The following example disables application logging using storage.</span></span>

## <span data-ttu-id="ef4dd-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="ef4dd-115">PARAMETERS</span></span>

### <span data-ttu-id="ef4dd-116">-BlobStorage</span><span class="sxs-lookup"><span data-stu-id="ef4dd-116">-BlobStorage</span></span>
```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ef4dd-117">-Fil</span><span class="sxs-lookup"><span data-stu-id="ef4dd-117">-File</span></span>
<span data-ttu-id="ef4dd-118">Anger att du vill använda fil systemet för att lagra loggfilerna.</span><span class="sxs-lookup"><span data-stu-id="ef4dd-118">Specifies that you want to use the file system to store the log files.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ef4dd-119">-Namn</span><span class="sxs-lookup"><span data-stu-id="ef4dd-119">-Name</span></span>
<span data-ttu-id="ef4dd-120">Anger namnet på webbplatsen.</span><span class="sxs-lookup"><span data-stu-id="ef4dd-120">Specifies the name of the website.</span></span>

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

### <span data-ttu-id="ef4dd-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ef4dd-121">-PassThru</span></span>
<span data-ttu-id="ef4dd-122">Flagga för att returnera SANT om den lyckades.</span><span class="sxs-lookup"><span data-stu-id="ef4dd-122">Flag to return true if succeeded.</span></span>

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

### <span data-ttu-id="ef4dd-123">-Profil</span><span class="sxs-lookup"><span data-stu-id="ef4dd-123">-Profile</span></span>
<span data-ttu-id="ef4dd-124">Anger den Azure-profil från vilken denna cmdlet läser.</span><span class="sxs-lookup"><span data-stu-id="ef4dd-124">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="ef4dd-125">Om du inte anger en profil läser denna cmdlet från den lokala standard profilen.</span><span class="sxs-lookup"><span data-stu-id="ef4dd-125">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="ef4dd-126">-Plats</span><span class="sxs-lookup"><span data-stu-id="ef4dd-126">-Slot</span></span>
<span data-ttu-id="ef4dd-127">Anger namnet på platsen.</span><span class="sxs-lookup"><span data-stu-id="ef4dd-127">Specifies the name of slot.</span></span>

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

### <span data-ttu-id="ef4dd-128">-TableStorage</span><span class="sxs-lookup"><span data-stu-id="ef4dd-128">-TableStorage</span></span>
```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ef4dd-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ef4dd-129">CommonParameters</span></span>
<span data-ttu-id="ef4dd-130">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ef4dd-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ef4dd-131">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ef4dd-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ef4dd-132">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="ef4dd-132">INPUTS</span></span>

## <span data-ttu-id="ef4dd-133">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="ef4dd-133">OUTPUTS</span></span>

## <span data-ttu-id="ef4dd-134">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="ef4dd-134">NOTES</span></span>

## <span data-ttu-id="ef4dd-135">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="ef4dd-135">RELATED LINKS</span></span>

[<span data-ttu-id="ef4dd-136">Enable-AzureWebsiteApplicationDiagnostic</span><span class="sxs-lookup"><span data-stu-id="ef4dd-136">Enable-AzureWebsiteApplicationDiagnostic</span></span>](./Enable-AzureWebsiteApplicationDiagnostic.md)

[<span data-ttu-id="ef4dd-137">Get-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="ef4dd-137">Get-AzureWebsite</span></span>](./Get-AzureWebsite.md)

[<span data-ttu-id="ef4dd-138">New-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="ef4dd-138">New-AzureWebsite</span></span>](./New-AzureWebsite.md)

[<span data-ttu-id="ef4dd-139">Remove-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="ef4dd-139">Remove-AzureWebsite</span></span>](./Remove-AzureWebsite.md)

[<span data-ttu-id="ef4dd-140">Start-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="ef4dd-140">Start-AzureWebsite</span></span>](./Start-AzureWebsite.md)


