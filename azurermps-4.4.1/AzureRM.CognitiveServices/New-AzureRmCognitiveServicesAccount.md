---
external help file: Microsoft.Azure.Commands.Management.CognitiveServices.dll-Help.xml
Module Name: AzureRM.CognitiveServices
ms.assetid: A2B4ACC1-6F53-47DE-A2D4-831E8AC89A5C
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/CognitiveServices/Commands.Management.CognitiveServices/help/New-AzureRmCognitiveServicesAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/CognitiveServices/Commands.Management.CognitiveServices/help/New-AzureRmCognitiveServicesAccount.md
ms.openlocfilehash: 449b10f851dbd4e2f2e804bab0772543d512c0c0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93585816"
---
# <span data-ttu-id="0f037-101">New-AzureRmCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="0f037-101">New-AzureRmCognitiveServicesAccount</span></span>

## <span data-ttu-id="0f037-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="0f037-102">SYNOPSIS</span></span>
<span data-ttu-id="0f037-103">Skapar ett konto för kognitiva tjänster.</span><span class="sxs-lookup"><span data-stu-id="0f037-103">Creates a Cognitive Services account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0f037-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="0f037-104">SYNTAX</span></span>

```
New-AzureRmCognitiveServicesAccount [-ResourceGroupName] <String> [-Name] <String> [-Type] <String>
 [-SkuName] <String> [-Location] <String> [-Tag <Hashtable[]>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0f037-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="0f037-105">DESCRIPTION</span></span>
<span data-ttu-id="0f037-106">Cmdleten **New-AzureRmCognitiveServicesAccount** skapar ett konto för kognitiva tjänster med den angivna typen och SKU.</span><span class="sxs-lookup"><span data-stu-id="0f037-106">The **New-AzureRmCognitiveServicesAccount** cmdlet creates a Cognitive Services account with the specified type and SKU.</span></span>

## <span data-ttu-id="0f037-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="0f037-107">EXAMPLES</span></span>

### <span data-ttu-id="0f037-108">9.1</span><span class="sxs-lookup"><span data-stu-id="0f037-108">1:</span></span>
```
New-AzureRmCognitiveServicesAccount -ResourceGroupName 'resourcegroup1' -name 'MyAccountName' -Type TextTranslation -SkuName F0 -Location 'usgovvirginia'
```

## <span data-ttu-id="0f037-109">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="0f037-109">PARAMETERS</span></span>

### <span data-ttu-id="0f037-110">-Force</span><span class="sxs-lookup"><span data-stu-id="0f037-110">-Force</span></span>
<span data-ttu-id="0f037-111">Tvingar kommandot att köras utan att fråga efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="0f037-111">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0f037-112">-Plats</span><span class="sxs-lookup"><span data-stu-id="0f037-112">-Location</span></span>
<span data-ttu-id="0f037-113">Anger den plats där kontot ska skapas.</span><span class="sxs-lookup"><span data-stu-id="0f037-113">Specifies the location in which to create the account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0f037-114">-Namn</span><span class="sxs-lookup"><span data-stu-id="0f037-114">-Name</span></span>
<span data-ttu-id="0f037-115">Anger namnet på kontot.</span><span class="sxs-lookup"><span data-stu-id="0f037-115">Specifies the name for the account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: CognitiveServicesAccountName, AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0f037-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0f037-116">-ResourceGroupName</span></span>
<span data-ttu-id="0f037-117">Anger namnet på den resurs grupp som kontot ska tilldelas till.</span><span class="sxs-lookup"><span data-stu-id="0f037-117">Specifies the name of the resource group to which to assign the account.</span></span>
<span data-ttu-id="0f037-118">Resurs gruppen måste redan finnas.</span><span class="sxs-lookup"><span data-stu-id="0f037-118">The resource group must already exist.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0f037-119">-SkuName</span><span class="sxs-lookup"><span data-stu-id="0f037-119">-SkuName</span></span>
<span data-ttu-id="0f037-120">Anger SKU för kontot.</span><span class="sxs-lookup"><span data-stu-id="0f037-120">Specifies the SKU for the account.</span></span>
<span data-ttu-id="0f037-121">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="0f037-121">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="0f037-122">F0 (kostnads fri nivå)</span><span class="sxs-lookup"><span data-stu-id="0f037-122">F0 (free tier)</span></span>
- <span data-ttu-id="0f037-123">S0</span><span class="sxs-lookup"><span data-stu-id="0f037-123">S0</span></span>
- <span data-ttu-id="0f037-124">S</span><span class="sxs-lookup"><span data-stu-id="0f037-124">S1</span></span>
- <span data-ttu-id="0f037-125">S2</span><span class="sxs-lookup"><span data-stu-id="0f037-125">S2</span></span>
- <span data-ttu-id="0f037-126">S3</span><span class="sxs-lookup"><span data-stu-id="0f037-126">S3</span></span>
- <span data-ttu-id="0f037-127">S4</span><span class="sxs-lookup"><span data-stu-id="0f037-127">S4</span></span>

<span data-ttu-id="0f037-128">Mer information finns i [funktions tjänst-API: erna](https://www.microsoft.com/cognitive-services/en-us/apis).</span><span class="sxs-lookup"><span data-stu-id="0f037-128">For more information, see [Cognitive Service APIs](https://www.microsoft.com/cognitive-services/en-us/apis).</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0f037-129">-Tagg</span><span class="sxs-lookup"><span data-stu-id="0f037-129">-Tag</span></span>
<span data-ttu-id="0f037-130">Anger en tagg som ett namn/värde-par.</span><span class="sxs-lookup"><span data-stu-id="0f037-130">Specifies a tag as a name/value pair.</span></span>

```yaml
Type: System.Collections.Hashtable[]
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0f037-131">– Skriv</span><span class="sxs-lookup"><span data-stu-id="0f037-131">-Type</span></span>
<span data-ttu-id="0f037-132">Anger vilken typ av konto som ska skapas. De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="0f037-132">Specifies the type of account to create.The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="0f037-133">ComputerVision</span><span class="sxs-lookup"><span data-stu-id="0f037-133">ComputerVision</span></span>
- <span data-ttu-id="0f037-134">Emotion</span><span class="sxs-lookup"><span data-stu-id="0f037-134">Emotion</span></span>
- <span data-ttu-id="0f037-135">Sidan</span><span class="sxs-lookup"><span data-stu-id="0f037-135">Face</span></span>
- <span data-ttu-id="0f037-136">LUIS</span><span class="sxs-lookup"><span data-stu-id="0f037-136">LUIS</span></span>
- <span data-ttu-id="0f037-137">Anvisningar</span><span class="sxs-lookup"><span data-stu-id="0f037-137">Recommendations</span></span>
- <span data-ttu-id="0f037-138">Igenkänning</span><span class="sxs-lookup"><span data-stu-id="0f037-138">Speech</span></span>
- <span data-ttu-id="0f037-139">TextAnalytics</span><span class="sxs-lookup"><span data-stu-id="0f037-139">TextAnalytics</span></span>
- <span data-ttu-id="0f037-140">WebLM</span><span class="sxs-lookup"><span data-stu-id="0f037-140">WebLM</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: CognitiveServicesAccountType, AccountType, Kind

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0f037-141">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="0f037-141">-Confirm</span></span>
<span data-ttu-id="0f037-142">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="0f037-142">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0f037-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0f037-143">-WhatIf</span></span>
<span data-ttu-id="0f037-144">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="0f037-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0f037-145">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="0f037-145">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0f037-146">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0f037-146">-DefaultProfile</span></span>
<span data-ttu-id="0f037-147">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="0f037-147">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0f037-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0f037-148">CommonParameters</span></span>
<span data-ttu-id="0f037-149">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0f037-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0f037-150">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0f037-150">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0f037-151">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="0f037-151">INPUTS</span></span>

## <span data-ttu-id="0f037-152">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="0f037-152">OUTPUTS</span></span>

### <span data-ttu-id="0f037-153">Microsoft. Azure. commands. Management. CognitiveServices. Models. PSCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="0f037-153">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSCognitiveServicesAccount</span></span>

## <span data-ttu-id="0f037-154">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="0f037-154">NOTES</span></span>

## <span data-ttu-id="0f037-155">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="0f037-155">RELATED LINKS</span></span>

[<span data-ttu-id="0f037-156">Get-AzureRmCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="0f037-156">Get-AzureRmCognitiveServicesAccount</span></span>](./Get-AzureRmCognitiveServicesAccount.md)

[<span data-ttu-id="0f037-157">Remove-AzureRmCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="0f037-157">Remove-AzureRmCognitiveServicesAccount</span></span>](./Remove-AzureRmCognitiveServicesAccount.md)

[<span data-ttu-id="0f037-158">Set-AzureRmCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="0f037-158">Set-AzureRmCognitiveServicesAccount</span></span>](./Set-AzureRmCognitiveServicesAccount.md)
