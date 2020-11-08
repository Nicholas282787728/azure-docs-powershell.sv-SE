---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: BFB57100-93F6-4FD2-8ECA-7F54BEB0D6B0
online version: ''
schema: 2.0.0
ms.openlocfilehash: 7114f39ee2b105c80429151df8347b5c17dcfea0
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94099736"
---
# <span data-ttu-id="c664d-101">Get-AzureWebsiteLog</span><span class="sxs-lookup"><span data-stu-id="c664d-101">Get-AzureWebsiteLog</span></span>

## <span data-ttu-id="c664d-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="c664d-102">SYNOPSIS</span></span>
<span data-ttu-id="c664d-103">Hämtar loggar för den angivna webbplatsen.</span><span class="sxs-lookup"><span data-stu-id="c664d-103">Gets logs for the specified website.</span></span>

## <span data-ttu-id="c664d-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="c664d-104">SYNTAX</span></span>

### <span data-ttu-id="c664d-105">Potatis</span><span class="sxs-lookup"><span data-stu-id="c664d-105">Tail</span></span>
```
Get-AzureWebsiteLog [-Path <String>] [-Message <String>] [-Tail] [-Name <String>] [-Slot <String>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="c664d-106">ListPath</span><span class="sxs-lookup"><span data-stu-id="c664d-106">ListPath</span></span>
```
Get-AzureWebsiteLog [-ListPath] [-Name <String>] [-Slot <String>] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="c664d-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="c664d-107">DESCRIPTION</span></span>
<span data-ttu-id="c664d-108">I det här avsnittet beskrivs cmdleten i 0.8.10-versionen av Microsoft Azure PowerShell-modulen.</span><span class="sxs-lookup"><span data-stu-id="c664d-108">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="c664d-109">För att få den version av modulen du använder, gå till Azure PowerShell-konsolen och skriv `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="c664d-109">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="c664d-110">Loggar in för den angivna webbplatsen.</span><span class="sxs-lookup"><span data-stu-id="c664d-110">Gets log for the specified website.</span></span>

## <span data-ttu-id="c664d-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="c664d-111">EXAMPLES</span></span>

### <span data-ttu-id="c664d-112">Exempel 1: starta logg direkt uppspelning</span><span class="sxs-lookup"><span data-stu-id="c664d-112">Example 1: Start log streaming</span></span>
```
PS C:\> Get-AzureWebsiteLog -Tail
```

<span data-ttu-id="c664d-113">I det här exemplet startas logg strömmar för alla program loggar.</span><span class="sxs-lookup"><span data-stu-id="c664d-113">This example starts log streaming for all application logs.</span></span>

### <span data-ttu-id="c664d-114">Exempel 2: starta logg direkt uppspelning för http-loggar</span><span class="sxs-lookup"><span data-stu-id="c664d-114">Example 2: Start log streaming for http logs</span></span>
```
PS C:\> Get-AzureWebsiteLog -Tail -Path http
```

<span data-ttu-id="c664d-115">I det här exemplet startas logg strömmar för http-loggar.</span><span class="sxs-lookup"><span data-stu-id="c664d-115">This example starts log streaming for http logs.</span></span>

### <span data-ttu-id="c664d-116">Exempel 3: starta logg direkt uppspelning för fel loggar</span><span class="sxs-lookup"><span data-stu-id="c664d-116">Example 3: Start log streaming for error logs</span></span>
```
PS C:\> Get-AzureWebsiteLog -Tail -Message Error
```

<span data-ttu-id="c664d-117">I det här exemplet startas logg strömmar och endast fel loggar visas.</span><span class="sxs-lookup"><span data-stu-id="c664d-117">This example starts log streaming and show error logs only.</span></span>

### <span data-ttu-id="c664d-118">Exempel 4: Visa avaiable-loggar</span><span class="sxs-lookup"><span data-stu-id="c664d-118">Example 4: Display avaiable logs</span></span>
```
PS C:\> Get-AzureWebsiteLog -Name MyWebsite -ListPath
```

<span data-ttu-id="c664d-119">Det här exemplet visar alla tillgängliga logg Sök vägar på webbplatsen.</span><span class="sxs-lookup"><span data-stu-id="c664d-119">This example lists all available log paths in the website.</span></span>

## <span data-ttu-id="c664d-120">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="c664d-120">PARAMETERS</span></span>

### <span data-ttu-id="c664d-121">-ListPath</span><span class="sxs-lookup"><span data-stu-id="c664d-121">-ListPath</span></span>
<span data-ttu-id="c664d-122">Anger om logg Sök vägar ska listas.</span><span class="sxs-lookup"><span data-stu-id="c664d-122">Indicates whether to list the log paths.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: ListPath
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c664d-123">– Meddelande</span><span class="sxs-lookup"><span data-stu-id="c664d-123">-Message</span></span>
<span data-ttu-id="c664d-124">Anger en sträng som ska användas för att filtrera logg meddelandet.</span><span class="sxs-lookup"><span data-stu-id="c664d-124">Specifies a string which will be used to filter the log message.</span></span>
<span data-ttu-id="c664d-125">Endast loggar som innehåller den här strängen hämtas.</span><span class="sxs-lookup"><span data-stu-id="c664d-125">Only logs which contains this string will be retrieved.</span></span>

```yaml
Type: String
Parameter Sets: Tail
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c664d-126">-Namn</span><span class="sxs-lookup"><span data-stu-id="c664d-126">-Name</span></span>
<span data-ttu-id="c664d-127">Webbplatsens namn.</span><span class="sxs-lookup"><span data-stu-id="c664d-127">The name of the website.</span></span>

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

### <span data-ttu-id="c664d-128">-Path</span><span class="sxs-lookup"><span data-stu-id="c664d-128">-Path</span></span>
<span data-ttu-id="c664d-129">Sökvägen som loggen hämtas från.</span><span class="sxs-lookup"><span data-stu-id="c664d-129">The path from which the log will be retrieved.</span></span>
<span data-ttu-id="c664d-130">Den är som standard rot, vilket innebär inkludera alla sökvägar.</span><span class="sxs-lookup"><span data-stu-id="c664d-130">By default it is Root, which means include all the paths.</span></span>

```yaml
Type: String
Parameter Sets: Tail
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c664d-131">-Profil</span><span class="sxs-lookup"><span data-stu-id="c664d-131">-Profile</span></span>
<span data-ttu-id="c664d-132">Anger den Azure-profil från vilken denna cmdlet läser.</span><span class="sxs-lookup"><span data-stu-id="c664d-132">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="c664d-133">Om du inte anger en profil läser denna cmdlet från den lokala standard profilen.</span><span class="sxs-lookup"><span data-stu-id="c664d-133">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="c664d-134">-Plats</span><span class="sxs-lookup"><span data-stu-id="c664d-134">-Slot</span></span>
<span data-ttu-id="c664d-135">Anger plats namnet.</span><span class="sxs-lookup"><span data-stu-id="c664d-135">Specifies the slot name.</span></span>

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

### <span data-ttu-id="c664d-136">-Pilslut</span><span class="sxs-lookup"><span data-stu-id="c664d-136">-Tail</span></span>
<span data-ttu-id="c664d-137">Anger om loggarna ska strömmas.</span><span class="sxs-lookup"><span data-stu-id="c664d-137">Specifies whether to stream the logs.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: Tail
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c664d-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c664d-138">CommonParameters</span></span>
<span data-ttu-id="c664d-139">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c664d-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c664d-140">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c664d-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c664d-141">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="c664d-141">INPUTS</span></span>

## <span data-ttu-id="c664d-142">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="c664d-142">OUTPUTS</span></span>

## <span data-ttu-id="c664d-143">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="c664d-143">NOTES</span></span>

## <span data-ttu-id="c664d-144">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="c664d-144">RELATED LINKS</span></span>

[<span data-ttu-id="c664d-145">Get-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="c664d-145">Get-AzureWebsite</span></span>](./Get-AzureWebsite.md)

[<span data-ttu-id="c664d-146">New-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="c664d-146">New-AzureWebsite</span></span>](./New-AzureWebsite.md)

[<span data-ttu-id="c664d-147">Remove-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="c664d-147">Remove-AzureWebsite</span></span>](./Remove-AzureWebsite.md)

[<span data-ttu-id="c664d-148">Start-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="c664d-148">Start-AzureWebsite</span></span>](./Start-AzureWebsite.md)


