---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CognitiveServices.dll-Help.xml
Module Name: Az.CognitiveServices
ms.assetid: A2B4ACC1-6F53-47DE-A2D4-831E8AC89A5C
online version: https://docs.microsoft.com/en-us/powershell/module/az.cognitiveservices/new-azcognitiveservicesaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/New-AzCognitiveServicesAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/New-AzCognitiveServicesAccount.md
ms.openlocfilehash: 7e5253951ec3c74850584aaac9818a6a7c8f2737
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93754619"
---
# <span data-ttu-id="e378c-101">New-AzCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="e378c-101">New-AzCognitiveServicesAccount</span></span>

## <span data-ttu-id="e378c-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="e378c-102">SYNOPSIS</span></span>
<span data-ttu-id="e378c-103">Skapar ett konto för kognitiva tjänster.</span><span class="sxs-lookup"><span data-stu-id="e378c-103">Creates a Cognitive Services account.</span></span>

## <span data-ttu-id="e378c-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="e378c-104">SYNTAX</span></span>

```
New-AzCognitiveServicesAccount [-ResourceGroupName] <String> [-Name] <String> [-Type] <String>
 [-SkuName] <String> [-Location] <String> [-Tag <Hashtable[]>] [-CustomSubdomainName <String>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e378c-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="e378c-105">DESCRIPTION</span></span>
<span data-ttu-id="e378c-106">Cmdleten **New-AzCognitiveServicesAccount** skapar ett konto för kognitiva tjänster med den angivna typen och SKU.</span><span class="sxs-lookup"><span data-stu-id="e378c-106">The **New-AzCognitiveServicesAccount** cmdlet creates a Cognitive Services account with the specified type and SKU.</span></span>

## <span data-ttu-id="e378c-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="e378c-107">EXAMPLES</span></span>

### <span data-ttu-id="e378c-108">9.1</span><span class="sxs-lookup"><span data-stu-id="e378c-108">1:</span></span>
```
PS C:\> New-AzCognitiveServicesAccount -ResourceGroupName cognitive-services-resource-group -name myluis -Type LUIS -SkuName S0 -Locatio
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

## <span data-ttu-id="e378c-109">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="e378c-109">PARAMETERS</span></span>

### <span data-ttu-id="e378c-110">-CustomSubdomainName</span><span class="sxs-lookup"><span data-stu-id="e378c-110">-CustomSubdomainName</span></span>
<span data-ttu-id="e378c-111">Namn på domän för kognitiva tjänster.</span><span class="sxs-lookup"><span data-stu-id="e378c-111">Cognitive Services Account Subdomain Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e378c-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e378c-112">-DefaultProfile</span></span>
<span data-ttu-id="e378c-113">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="e378c-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e378c-114">-Force</span><span class="sxs-lookup"><span data-stu-id="e378c-114">-Force</span></span>
<span data-ttu-id="e378c-115">Tvingar kommandot att köras utan att fråga efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="e378c-115">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="e378c-116">-Plats</span><span class="sxs-lookup"><span data-stu-id="e378c-116">-Location</span></span>
<span data-ttu-id="e378c-117">Anger den plats där kontot ska skapas.</span><span class="sxs-lookup"><span data-stu-id="e378c-117">Specifies the location in which to create the account.</span></span>

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

### <span data-ttu-id="e378c-118">-Namn</span><span class="sxs-lookup"><span data-stu-id="e378c-118">-Name</span></span>
<span data-ttu-id="e378c-119">Anger namnet på kontot.</span><span class="sxs-lookup"><span data-stu-id="e378c-119">Specifies the name for the account.</span></span>

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

### <span data-ttu-id="e378c-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e378c-120">-ResourceGroupName</span></span>
<span data-ttu-id="e378c-121">Anger namnet på den resurs grupp som kontot ska tilldelas till.</span><span class="sxs-lookup"><span data-stu-id="e378c-121">Specifies the name of the resource group to which to assign the account.</span></span>
<span data-ttu-id="e378c-122">Resurs gruppen måste redan finnas.</span><span class="sxs-lookup"><span data-stu-id="e378c-122">The resource group must already exist.</span></span>

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

### <span data-ttu-id="e378c-123">-SkuName</span><span class="sxs-lookup"><span data-stu-id="e378c-123">-SkuName</span></span>
<span data-ttu-id="e378c-124">Anger SKU för kontot.</span><span class="sxs-lookup"><span data-stu-id="e378c-124">Specifies the SKU for the account.</span></span>
<span data-ttu-id="e378c-125">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="e378c-125">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="e378c-126">F0 (kostnads fri nivå)</span><span class="sxs-lookup"><span data-stu-id="e378c-126">F0 (free tier)</span></span>
- <span data-ttu-id="e378c-127">S0</span><span class="sxs-lookup"><span data-stu-id="e378c-127">S0</span></span>
- <span data-ttu-id="e378c-128">S</span><span class="sxs-lookup"><span data-stu-id="e378c-128">S1</span></span>
- <span data-ttu-id="e378c-129">S2</span><span class="sxs-lookup"><span data-stu-id="e378c-129">S2</span></span>
- <span data-ttu-id="e378c-130">S3</span><span class="sxs-lookup"><span data-stu-id="e378c-130">S3</span></span>
- <span data-ttu-id="e378c-131">S4 mer information finns i [API för kognitiva tjänster](https://www.microsoft.com/cognitive-services/en-us/apis).</span><span class="sxs-lookup"><span data-stu-id="e378c-131">S4 For more information, see [Cognitive Service APIs](https://www.microsoft.com/cognitive-services/en-us/apis).</span></span>

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

### <span data-ttu-id="e378c-132">-Tagg</span><span class="sxs-lookup"><span data-stu-id="e378c-132">-Tag</span></span>
<span data-ttu-id="e378c-133">Anger en tagg som ett namn/värde-par.</span><span class="sxs-lookup"><span data-stu-id="e378c-133">Specifies a tag as a name/value pair.</span></span>

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

### <span data-ttu-id="e378c-134">– Skriv</span><span class="sxs-lookup"><span data-stu-id="e378c-134">-Type</span></span>
<span data-ttu-id="e378c-135">Anger vilken typ av konto som ska skapas.</span><span class="sxs-lookup"><span data-stu-id="e378c-135">Specifies the type of account to create.</span></span> <span data-ttu-id="e378c-136">Använd `Get-AzCognitiveServicesAccountType` cmdlet för att få aktuella acceptabla värden.</span><span class="sxs-lookup"><span data-stu-id="e378c-136">Use `Get-AzCognitiveServicesAccountType` cmdlet to get current acceptable values.</span></span>

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

### <span data-ttu-id="e378c-137">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="e378c-137">-Confirm</span></span>
<span data-ttu-id="e378c-138">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="e378c-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e378c-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e378c-139">-WhatIf</span></span>
<span data-ttu-id="e378c-140">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="e378c-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e378c-141">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="e378c-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e378c-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e378c-142">CommonParameters</span></span>
<span data-ttu-id="e378c-143">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e378c-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e378c-144">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e378c-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e378c-145">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="e378c-145">INPUTS</span></span>

### <span data-ttu-id="e378c-146">System. String</span><span class="sxs-lookup"><span data-stu-id="e378c-146">System.String</span></span>

## <span data-ttu-id="e378c-147">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="e378c-147">OUTPUTS</span></span>

### <span data-ttu-id="e378c-148">Microsoft. Azure. commands. Management. CognitiveServices. Models. PSCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="e378c-148">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSCognitiveServicesAccount</span></span>

## <span data-ttu-id="e378c-149">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="e378c-149">NOTES</span></span>

## <span data-ttu-id="e378c-150">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="e378c-150">RELATED LINKS</span></span>

[<span data-ttu-id="e378c-151">Get-AzCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="e378c-151">Get-AzCognitiveServicesAccount</span></span>](./Get-AzCognitiveServicesAccount.md)

[<span data-ttu-id="e378c-152">Remove-AzCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="e378c-152">Remove-AzCognitiveServicesAccount</span></span>](./Remove-AzCognitiveServicesAccount.md)

[<span data-ttu-id="e378c-153">Set-AzCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="e378c-153">Set-AzCognitiveServicesAccount</span></span>](./Set-AzCognitiveServicesAccount.md)
