---
external help file: Microsoft.Azure.Commands.Management.CognitiveServices.dll-Help.xml
Module Name: AzureRM.CognitiveServices
ms.assetid: A2B4ACC1-6F53-47DE-A2D4-831E8AC89A5C
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.cognitiveservices/new-azurermcognitiveservicesaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/CognitiveServices/Commands.Management.CognitiveServices/help/New-AzureRmCognitiveServicesAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/CognitiveServices/Commands.Management.CognitiveServices/help/New-AzureRmCognitiveServicesAccount.md
ms.openlocfilehash: 41defe467244647f707bae16c653dfcbe99eaec3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93576321"
---
# <span data-ttu-id="a4f1d-101">New-AzureRmCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="a4f1d-101">New-AzureRmCognitiveServicesAccount</span></span>

## <span data-ttu-id="a4f1d-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="a4f1d-102">SYNOPSIS</span></span>
<span data-ttu-id="a4f1d-103">Skapar ett konto för kognitiva tjänster.</span><span class="sxs-lookup"><span data-stu-id="a4f1d-103">Creates a Cognitive Services account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a4f1d-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="a4f1d-104">SYNTAX</span></span>

```
New-AzureRmCognitiveServicesAccount [-ResourceGroupName] <String> [-Name] <String> [-Type] <String>
 [-SkuName] <String> [-Location] <String> [-Tag <Hashtable[]>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a4f1d-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="a4f1d-105">DESCRIPTION</span></span>
<span data-ttu-id="a4f1d-106">Cmdleten **New-AzureRmCognitiveServicesAccount** skapar ett konto för kognitiva tjänster med den angivna typen och SKU.</span><span class="sxs-lookup"><span data-stu-id="a4f1d-106">The **New-AzureRmCognitiveServicesAccount** cmdlet creates a Cognitive Services account with the specified type and SKU.</span></span>

## <span data-ttu-id="a4f1d-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="a4f1d-107">EXAMPLES</span></span>

### <span data-ttu-id="a4f1d-108">9.1</span><span class="sxs-lookup"><span data-stu-id="a4f1d-108">1:</span></span>
```
PS C:\> New-AzureRmCognitiveServicesAccount -ResourceGroupName cognitive-services-resource-group -name myluis -Type LUIS -SkuName S0 -Locatio
n 'WestUS'


ResourceGroupName : cognitive-services-resource-group
AccountName       : myluis
Id                : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/cognitive-services-resource-group/providers/Microsoft.Cog
                    nitiveServices/accounts/myluis
Endpoint          : https://westus.api.cognitive.microsoft.com/luis/v2.0
Location          : WestUS
Sku               : Microsoft.Azure.Management.CognitiveServices.Models.Sku
AccountType       : LUIS
ResourceType      : Microsoft.CognitiveServices/accounts
Etag              : "xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx"
ProvisioningState : Succeeded
Tags              :
```

## <span data-ttu-id="a4f1d-109">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="a4f1d-109">PARAMETERS</span></span>

### <span data-ttu-id="a4f1d-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a4f1d-110">-DefaultProfile</span></span>
<span data-ttu-id="a4f1d-111">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="a4f1d-111">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a4f1d-112">-Force</span><span class="sxs-lookup"><span data-stu-id="a4f1d-112">-Force</span></span>
<span data-ttu-id="a4f1d-113">Tvingar kommandot att köras utan att fråga efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="a4f1d-113">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="a4f1d-114">-Plats</span><span class="sxs-lookup"><span data-stu-id="a4f1d-114">-Location</span></span>
<span data-ttu-id="a4f1d-115">Anger den plats där kontot ska skapas.</span><span class="sxs-lookup"><span data-stu-id="a4f1d-115">Specifies the location in which to create the account.</span></span>

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

### <span data-ttu-id="a4f1d-116">-Namn</span><span class="sxs-lookup"><span data-stu-id="a4f1d-116">-Name</span></span>
<span data-ttu-id="a4f1d-117">Anger namnet på kontot.</span><span class="sxs-lookup"><span data-stu-id="a4f1d-117">Specifies the name for the account.</span></span>

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

### <span data-ttu-id="a4f1d-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a4f1d-118">-ResourceGroupName</span></span>
<span data-ttu-id="a4f1d-119">Anger namnet på den resurs grupp som kontot ska tilldelas till.</span><span class="sxs-lookup"><span data-stu-id="a4f1d-119">Specifies the name of the resource group to which to assign the account.</span></span>
<span data-ttu-id="a4f1d-120">Resurs gruppen måste redan finnas.</span><span class="sxs-lookup"><span data-stu-id="a4f1d-120">The resource group must already exist.</span></span>

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

### <span data-ttu-id="a4f1d-121">-SkuName</span><span class="sxs-lookup"><span data-stu-id="a4f1d-121">-SkuName</span></span>
<span data-ttu-id="a4f1d-122">Anger SKU för kontot.</span><span class="sxs-lookup"><span data-stu-id="a4f1d-122">Specifies the SKU for the account.</span></span>
<span data-ttu-id="a4f1d-123">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="a4f1d-123">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="a4f1d-124">F0 (kostnads fri nivå)</span><span class="sxs-lookup"><span data-stu-id="a4f1d-124">F0 (free tier)</span></span>
- <span data-ttu-id="a4f1d-125">S0</span><span class="sxs-lookup"><span data-stu-id="a4f1d-125">S0</span></span>
- <span data-ttu-id="a4f1d-126">S</span><span class="sxs-lookup"><span data-stu-id="a4f1d-126">S1</span></span>
- <span data-ttu-id="a4f1d-127">S2</span><span class="sxs-lookup"><span data-stu-id="a4f1d-127">S2</span></span>
- <span data-ttu-id="a4f1d-128">S3</span><span class="sxs-lookup"><span data-stu-id="a4f1d-128">S3</span></span>
- <span data-ttu-id="a4f1d-129">S4 mer information finns i [API för kognitiva tjänster](https://www.microsoft.com/cognitive-services/en-us/apis).</span><span class="sxs-lookup"><span data-stu-id="a4f1d-129">S4 For more information, see [Cognitive Service APIs](https://www.microsoft.com/cognitive-services/en-us/apis).</span></span>

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

### <span data-ttu-id="a4f1d-130">-Tagg</span><span class="sxs-lookup"><span data-stu-id="a4f1d-130">-Tag</span></span>
<span data-ttu-id="a4f1d-131">Anger en tagg som ett namn/värde-par.</span><span class="sxs-lookup"><span data-stu-id="a4f1d-131">Specifies a tag as a name/value pair.</span></span>

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

### <span data-ttu-id="a4f1d-132">– Skriv</span><span class="sxs-lookup"><span data-stu-id="a4f1d-132">-Type</span></span>
<span data-ttu-id="a4f1d-133">Anger vilken typ av konto som ska skapas.</span><span class="sxs-lookup"><span data-stu-id="a4f1d-133">Specifies the type of account to create.</span></span> <span data-ttu-id="a4f1d-134">Använd `Get-AzureRmCognitiveServicesAccountType` cmdlet för att få aktuella acceptabla värden.</span><span class="sxs-lookup"><span data-stu-id="a4f1d-134">Use `Get-AzureRmCognitiveServicesAccountType` cmdlet to get current acceptable values.</span></span>

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

### <span data-ttu-id="a4f1d-135">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="a4f1d-135">-Confirm</span></span>
<span data-ttu-id="a4f1d-136">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="a4f1d-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a4f1d-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a4f1d-137">-WhatIf</span></span>
<span data-ttu-id="a4f1d-138">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="a4f1d-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a4f1d-139">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="a4f1d-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a4f1d-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a4f1d-140">CommonParameters</span></span>
<span data-ttu-id="a4f1d-141">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a4f1d-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a4f1d-142">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a4f1d-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a4f1d-143">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="a4f1d-143">INPUTS</span></span>

### <span data-ttu-id="a4f1d-144">System. String</span><span class="sxs-lookup"><span data-stu-id="a4f1d-144">System.String</span></span>

## <span data-ttu-id="a4f1d-145">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="a4f1d-145">OUTPUTS</span></span>

### <span data-ttu-id="a4f1d-146">Microsoft. Azure. commands. Management. CognitiveServices. Models. PSCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="a4f1d-146">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSCognitiveServicesAccount</span></span>

## <span data-ttu-id="a4f1d-147">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="a4f1d-147">NOTES</span></span>

## <span data-ttu-id="a4f1d-148">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="a4f1d-148">RELATED LINKS</span></span>

[<span data-ttu-id="a4f1d-149">Get-AzureRmCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="a4f1d-149">Get-AzureRmCognitiveServicesAccount</span></span>](./Get-AzureRmCognitiveServicesAccount.md)

[<span data-ttu-id="a4f1d-150">Remove-AzureRmCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="a4f1d-150">Remove-AzureRmCognitiveServicesAccount</span></span>](./Remove-AzureRmCognitiveServicesAccount.md)

[<span data-ttu-id="a4f1d-151">Set-AzureRmCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="a4f1d-151">Set-AzureRmCognitiveServicesAccount</span></span>](./Set-AzureRmCognitiveServicesAccount.md)
