---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CognitiveServices.dll-Help.xml
Module Name: Az.CognitiveServices
ms.assetid: 11E2D82A-1DF1-4E19-8328-44674641D1BB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cognitiveservices/set-azcognitiveservicesaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/Set-AzCognitiveServicesAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/Set-AzCognitiveServicesAccount.md
ms.openlocfilehash: 2544531d9a988daaea314fc2088609df77b719b7
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93754617"
---
# <span data-ttu-id="8d183-101">Set-AzCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="8d183-101">Set-AzCognitiveServicesAccount</span></span>

## <span data-ttu-id="8d183-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="8d183-102">SYNOPSIS</span></span>
<span data-ttu-id="8d183-103">Ändrar ett konto.</span><span class="sxs-lookup"><span data-stu-id="8d183-103">Modifies an account.</span></span>

## <span data-ttu-id="8d183-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="8d183-104">SYNTAX</span></span>

```
Set-AzCognitiveServicesAccount [-ResourceGroupName] <String> [-Name] <String> [-SkuName <String>]
 [-Tag <Hashtable[]>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="8d183-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="8d183-105">DESCRIPTION</span></span>
<span data-ttu-id="8d183-106">Cmdleten **set-AzCognitiveServicesAccount** ändrar SKU eller taggar för det angivna kontot för kognitiva tjänster.</span><span class="sxs-lookup"><span data-stu-id="8d183-106">The **Set-AzCognitiveServicesAccount** cmdlet modifies the SKU or tags of the specified Cognitive Services account.</span></span>

## <span data-ttu-id="8d183-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="8d183-107">EXAMPLES</span></span>

### <span data-ttu-id="8d183-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="8d183-108">Example 1</span></span>
```powershell
PS C:\> Set-AzCognitiveServicesAccount -ResourceGroupName cognitive-services-resource-group -name myluis -SkuName S0


ResourceGroupName : cognitive-services-resource-group
AccountName       : myluis
Id                : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/cognitive-services-resource-group/providers/Microsoft.Cog
                    nitiveServices/accounts/myluis
Endpoint          : https://westus.api.cognitive.microsoft.com/luis/v2.0
Location          : WESTUS
Sku               : Microsoft.Azure.Management.CognitiveServices.Models.Sku
AccountType       : LUIS
ResourceType      : Microsoft.CognitiveServices/accounts
Etag              : "xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx"
ProvisioningState : Succeeded
Tags              :
```

## <span data-ttu-id="8d183-109">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="8d183-109">PARAMETERS</span></span>

### <span data-ttu-id="8d183-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8d183-110">-DefaultProfile</span></span>
<span data-ttu-id="8d183-111">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="8d183-111">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="8d183-112">-Force</span><span class="sxs-lookup"><span data-stu-id="8d183-112">-Force</span></span>
<span data-ttu-id="8d183-113">Tvingar kommandot att köras utan att fråga efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="8d183-113">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="8d183-114">-Namn</span><span class="sxs-lookup"><span data-stu-id="8d183-114">-Name</span></span>
<span data-ttu-id="8d183-115">Anger namnet på kontot som ska ändras.</span><span class="sxs-lookup"><span data-stu-id="8d183-115">Specifies the name of the account to modify.</span></span>

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

### <span data-ttu-id="8d183-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8d183-116">-ResourceGroupName</span></span>
<span data-ttu-id="8d183-117">Anger namnet på resurs gruppen som kontot är tilldelat till.</span><span class="sxs-lookup"><span data-stu-id="8d183-117">Specifies the name of the resource group the account is assigned to.</span></span>

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

### <span data-ttu-id="8d183-118">-SkuName</span><span class="sxs-lookup"><span data-stu-id="8d183-118">-SkuName</span></span>
<span data-ttu-id="8d183-119">Anger SKU för kontot.</span><span class="sxs-lookup"><span data-stu-id="8d183-119">Specifies the SKU for the account.</span></span>
<span data-ttu-id="8d183-120">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="8d183-120">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="8d183-121">F0 (kostnads fri nivå)</span><span class="sxs-lookup"><span data-stu-id="8d183-121">F0 (free tier)</span></span>
- <span data-ttu-id="8d183-122">S0</span><span class="sxs-lookup"><span data-stu-id="8d183-122">S0</span></span>
- <span data-ttu-id="8d183-123">S</span><span class="sxs-lookup"><span data-stu-id="8d183-123">S1</span></span>
- <span data-ttu-id="8d183-124">S2</span><span class="sxs-lookup"><span data-stu-id="8d183-124">S2</span></span>
- <span data-ttu-id="8d183-125">S3</span><span class="sxs-lookup"><span data-stu-id="8d183-125">S3</span></span>
- <span data-ttu-id="8d183-126">S4</span><span class="sxs-lookup"><span data-stu-id="8d183-126">S4</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8d183-127">-Tagg</span><span class="sxs-lookup"><span data-stu-id="8d183-127">-Tag</span></span>
<span data-ttu-id="8d183-128">Anger en tagg som ett namn/värde-par.</span><span class="sxs-lookup"><span data-stu-id="8d183-128">Specifies a tag as a name/value pair.</span></span>

```yaml
Type: System.Collections.Hashtable[]
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8d183-129">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="8d183-129">-Confirm</span></span>
<span data-ttu-id="8d183-130">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="8d183-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8d183-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8d183-131">-WhatIf</span></span>
<span data-ttu-id="8d183-132">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="8d183-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8d183-133">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="8d183-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8d183-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8d183-134">CommonParameters</span></span>
<span data-ttu-id="8d183-135">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8d183-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8d183-136">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8d183-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8d183-137">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="8d183-137">INPUTS</span></span>

### <span data-ttu-id="8d183-138">System. String</span><span class="sxs-lookup"><span data-stu-id="8d183-138">System.String</span></span>

### <span data-ttu-id="8d183-139">System. Collections. hash-program []</span><span class="sxs-lookup"><span data-stu-id="8d183-139">System.Collections.Hashtable[]</span></span>

## <span data-ttu-id="8d183-140">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="8d183-140">OUTPUTS</span></span>

### <span data-ttu-id="8d183-141">Microsoft. Azure. commands. Management. CognitiveServices. Models. PSCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="8d183-141">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSCognitiveServicesAccount</span></span>

## <span data-ttu-id="8d183-142">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="8d183-142">NOTES</span></span>

## <span data-ttu-id="8d183-143">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="8d183-143">RELATED LINKS</span></span>

[<span data-ttu-id="8d183-144">Get-AzCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="8d183-144">Get-AzCognitiveServicesAccount</span></span>](./Get-AzCognitiveServicesAccount.md)

[<span data-ttu-id="8d183-145">New-AzCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="8d183-145">New-AzCognitiveServicesAccount</span></span>](./New-AzCognitiveServicesAccount.md)

[<span data-ttu-id="8d183-146">Remove-AzCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="8d183-146">Remove-AzCognitiveServicesAccount</span></span>](./Remove-AzCognitiveServicesAccount.md)
