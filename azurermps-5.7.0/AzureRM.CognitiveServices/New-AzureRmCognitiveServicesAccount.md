---
external help file: Microsoft.Azure.Commands.Management.CognitiveServices.dll-Help.xml
Module Name: AzureRM.CognitiveServices
ms.assetid: A2B4ACC1-6F53-47DE-A2D4-831E8AC89A5C
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.cognitiveservices/new-azurermcognitiveservicesaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/CognitiveServices/Commands.Management.CognitiveServices/help/New-AzureRmCognitiveServicesAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/CognitiveServices/Commands.Management.CognitiveServices/help/New-AzureRmCognitiveServicesAccount.md
ms.openlocfilehash: 1c1d4ad776ed3db2cb3b5adfb490902a7de12f42
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93755398"
---
# <span data-ttu-id="d2754-101">New-AzureRmCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="d2754-101">New-AzureRmCognitiveServicesAccount</span></span>

## <span data-ttu-id="d2754-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="d2754-102">SYNOPSIS</span></span>
<span data-ttu-id="d2754-103">Skapar ett konto för kognitiva tjänster.</span><span class="sxs-lookup"><span data-stu-id="d2754-103">Creates a Cognitive Services account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d2754-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="d2754-104">SYNTAX</span></span>

```
New-AzureRmCognitiveServicesAccount [-ResourceGroupName] <String> [-Name] <String> [-Type] <String>
 [-SkuName] <String> [-Location] <String> [-Tag <Hashtable[]>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d2754-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="d2754-105">DESCRIPTION</span></span>
<span data-ttu-id="d2754-106">Cmdleten **New-AzureRmCognitiveServicesAccount** skapar ett konto för kognitiva tjänster med den angivna typen och SKU.</span><span class="sxs-lookup"><span data-stu-id="d2754-106">The **New-AzureRmCognitiveServicesAccount** cmdlet creates a Cognitive Services account with the specified type and SKU.</span></span>

## <span data-ttu-id="d2754-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="d2754-107">EXAMPLES</span></span>

### <span data-ttu-id="d2754-108">9.1</span><span class="sxs-lookup"><span data-stu-id="d2754-108">1:</span></span>
```
New-AzureRmCognitiveServicesAccount -ResourceGroupName 'resourcegroup1' -name 'MyAccountName' -Type TextTranslation -SkuName F0 -Location 'usgovvirginia'
```

## <span data-ttu-id="d2754-109">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="d2754-109">PARAMETERS</span></span>

### <span data-ttu-id="d2754-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d2754-110">-DefaultProfile</span></span>
<span data-ttu-id="d2754-111">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="d2754-111">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d2754-112">-Force</span><span class="sxs-lookup"><span data-stu-id="d2754-112">-Force</span></span>
<span data-ttu-id="d2754-113">Tvingar kommandot att köras utan att fråga efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="d2754-113">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="d2754-114">-Plats</span><span class="sxs-lookup"><span data-stu-id="d2754-114">-Location</span></span>
<span data-ttu-id="d2754-115">Anger den plats där kontot ska skapas.</span><span class="sxs-lookup"><span data-stu-id="d2754-115">Specifies the location in which to create the account.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d2754-116">-Namn</span><span class="sxs-lookup"><span data-stu-id="d2754-116">-Name</span></span>
<span data-ttu-id="d2754-117">Anger namnet på kontot.</span><span class="sxs-lookup"><span data-stu-id="d2754-117">Specifies the name for the account.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: CognitiveServicesAccountName, AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d2754-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d2754-118">-ResourceGroupName</span></span>
<span data-ttu-id="d2754-119">Anger namnet på den resurs grupp som kontot ska tilldelas till.</span><span class="sxs-lookup"><span data-stu-id="d2754-119">Specifies the name of the resource group to which to assign the account.</span></span>
<span data-ttu-id="d2754-120">Resurs gruppen måste redan finnas.</span><span class="sxs-lookup"><span data-stu-id="d2754-120">The resource group must already exist.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d2754-121">-SkuName</span><span class="sxs-lookup"><span data-stu-id="d2754-121">-SkuName</span></span>
<span data-ttu-id="d2754-122">Anger SKU för kontot.</span><span class="sxs-lookup"><span data-stu-id="d2754-122">Specifies the SKU for the account.</span></span>
<span data-ttu-id="d2754-123">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="d2754-123">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="d2754-124">F0 (kostnads fri nivå)</span><span class="sxs-lookup"><span data-stu-id="d2754-124">F0 (free tier)</span></span>
- <span data-ttu-id="d2754-125">S0</span><span class="sxs-lookup"><span data-stu-id="d2754-125">S0</span></span>
- <span data-ttu-id="d2754-126">S</span><span class="sxs-lookup"><span data-stu-id="d2754-126">S1</span></span>
- <span data-ttu-id="d2754-127">S2</span><span class="sxs-lookup"><span data-stu-id="d2754-127">S2</span></span>
- <span data-ttu-id="d2754-128">S3</span><span class="sxs-lookup"><span data-stu-id="d2754-128">S3</span></span>
- <span data-ttu-id="d2754-129">S4</span><span class="sxs-lookup"><span data-stu-id="d2754-129">S4</span></span>

<span data-ttu-id="d2754-130">Mer information finns i [funktions tjänst-API: erna](https://www.microsoft.com/cognitive-services/en-us/apis).</span><span class="sxs-lookup"><span data-stu-id="d2754-130">For more information, see [Cognitive Service APIs](https://www.microsoft.com/cognitive-services/en-us/apis).</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d2754-131">-Tagg</span><span class="sxs-lookup"><span data-stu-id="d2754-131">-Tag</span></span>
<span data-ttu-id="d2754-132">Anger en tagg som ett namn/värde-par.</span><span class="sxs-lookup"><span data-stu-id="d2754-132">Specifies a tag as a name/value pair.</span></span>

```yaml
Type: Hashtable[]
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d2754-133">– Skriv</span><span class="sxs-lookup"><span data-stu-id="d2754-133">-Type</span></span>
<span data-ttu-id="d2754-134">Anger vilken typ av konto som ska skapas.</span><span class="sxs-lookup"><span data-stu-id="d2754-134">Specifies the type of account to create.</span></span> <span data-ttu-id="d2754-135">Aktuella acceptabla värden för denna parameter är:</span><span class="sxs-lookup"><span data-stu-id="d2754-135">Current acceptable values for this parameter are:</span></span>

- <span data-ttu-id="d2754-136">Bing. föreslå v7</span><span class="sxs-lookup"><span data-stu-id="d2754-136">Bing.Autosuggest.v7</span></span>
- <span data-ttu-id="d2754-137">Bing. CustomSearch</span><span class="sxs-lookup"><span data-stu-id="d2754-137">Bing.CustomSearch</span></span>
- <span data-ttu-id="d2754-138">Bing. search. v7</span><span class="sxs-lookup"><span data-stu-id="d2754-138">Bing.Search.v7</span></span>
- <span data-ttu-id="d2754-139">Bing. Speech</span><span class="sxs-lookup"><span data-stu-id="d2754-139">Bing.Speech</span></span>
- <span data-ttu-id="d2754-140">Bing. stavnings kontroll. v7</span><span class="sxs-lookup"><span data-stu-id="d2754-140">Bing.SpellCheck.v7</span></span>
- <span data-ttu-id="d2754-141">ComputerVision</span><span class="sxs-lookup"><span data-stu-id="d2754-141">ComputerVision</span></span>
- <span data-ttu-id="d2754-142">ContentModerator</span><span class="sxs-lookup"><span data-stu-id="d2754-142">ContentModerator</span></span>
- <span data-ttu-id="d2754-143">CustomSpeech</span><span class="sxs-lookup"><span data-stu-id="d2754-143">CustomSpeech</span></span>
- <span data-ttu-id="d2754-144">CustomVision. förutsägelse</span><span class="sxs-lookup"><span data-stu-id="d2754-144">CustomVision.Prediction</span></span>
- <span data-ttu-id="d2754-145">CustomVision. utbildning</span><span class="sxs-lookup"><span data-stu-id="d2754-145">CustomVision.Training</span></span>
- <span data-ttu-id="d2754-146">Emotion</span><span class="sxs-lookup"><span data-stu-id="d2754-146">Emotion</span></span>
- <span data-ttu-id="d2754-147">Sidan</span><span class="sxs-lookup"><span data-stu-id="d2754-147">Face</span></span>
- <span data-ttu-id="d2754-148">LUIS</span><span class="sxs-lookup"><span data-stu-id="d2754-148">LUIS</span></span>
- <span data-ttu-id="d2754-149">QnAMaker</span><span class="sxs-lookup"><span data-stu-id="d2754-149">QnAMaker</span></span>
- <span data-ttu-id="d2754-150">SpeakerRecognition</span><span class="sxs-lookup"><span data-stu-id="d2754-150">SpeakerRecognition</span></span>
- <span data-ttu-id="d2754-151">SpeechTranslation</span><span class="sxs-lookup"><span data-stu-id="d2754-151">SpeechTranslation</span></span>
- <span data-ttu-id="d2754-152">TextAnalytics</span><span class="sxs-lookup"><span data-stu-id="d2754-152">TextAnalytics</span></span>
- <span data-ttu-id="d2754-153">TextTranslation</span><span class="sxs-lookup"><span data-stu-id="d2754-153">TextTranslation</span></span>
- <span data-ttu-id="d2754-154">WebLM</span><span class="sxs-lookup"><span data-stu-id="d2754-154">WebLM</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: CognitiveServicesAccountType, AccountType, Kind

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d2754-155">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="d2754-155">-Confirm</span></span>
<span data-ttu-id="d2754-156">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="d2754-156">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d2754-157">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d2754-157">-WhatIf</span></span>
<span data-ttu-id="d2754-158">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="d2754-158">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d2754-159">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="d2754-159">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d2754-160">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d2754-160">CommonParameters</span></span>
<span data-ttu-id="d2754-161">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d2754-161">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d2754-162">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d2754-162">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d2754-163">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="d2754-163">INPUTS</span></span>

### <span data-ttu-id="d2754-164">Ingen</span><span class="sxs-lookup"><span data-stu-id="d2754-164">None</span></span>
<span data-ttu-id="d2754-165">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="d2754-165">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="d2754-166">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="d2754-166">OUTPUTS</span></span>

### <span data-ttu-id="d2754-167">Microsoft. Azure. commands. Management. CognitiveServices. Models. PSCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="d2754-167">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSCognitiveServicesAccount</span></span>

## <span data-ttu-id="d2754-168">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="d2754-168">NOTES</span></span>

## <span data-ttu-id="d2754-169">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="d2754-169">RELATED LINKS</span></span>

[<span data-ttu-id="d2754-170">Get-AzureRmCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="d2754-170">Get-AzureRmCognitiveServicesAccount</span></span>](./Get-AzureRmCognitiveServicesAccount.md)

[<span data-ttu-id="d2754-171">Remove-AzureRmCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="d2754-171">Remove-AzureRmCognitiveServicesAccount</span></span>](./Remove-AzureRmCognitiveServicesAccount.md)

[<span data-ttu-id="d2754-172">Set-AzureRmCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="d2754-172">Set-AzureRmCognitiveServicesAccount</span></span>](./Set-AzureRmCognitiveServicesAccount.md)
