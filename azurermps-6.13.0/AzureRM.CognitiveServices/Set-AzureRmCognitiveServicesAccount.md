---
external help file: Microsoft.Azure.Commands.Management.CognitiveServices.dll-Help.xml
Module Name: AzureRM.CognitiveServices
ms.assetid: 11E2D82A-1DF1-4E19-8328-44674641D1BB
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.cognitiveservices/set-azurermcognitiveservicesaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/CognitiveServices/Commands.Management.CognitiveServices/help/Set-AzureRmCognitiveServicesAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/CognitiveServices/Commands.Management.CognitiveServices/help/Set-AzureRmCognitiveServicesAccount.md
ms.openlocfilehash: 74c066cd59497603da4f953f35ed16e454e67155
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93756032"
---
# <span data-ttu-id="dbeb5-101">Set-AzureRmCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="dbeb5-101">Set-AzureRmCognitiveServicesAccount</span></span>

## <span data-ttu-id="dbeb5-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="dbeb5-102">SYNOPSIS</span></span>
<span data-ttu-id="dbeb5-103">Ändrar ett konto.</span><span class="sxs-lookup"><span data-stu-id="dbeb5-103">Modifies an account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="dbeb5-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="dbeb5-104">SYNTAX</span></span>

```
Set-AzureRmCognitiveServicesAccount [-ResourceGroupName] <String> [-Name] <String> [-SkuName <String>]
 [-Tag <Hashtable[]>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="dbeb5-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="dbeb5-105">DESCRIPTION</span></span>
<span data-ttu-id="dbeb5-106">Cmdleten **set-AzureRmCognitiveServicesAccount** ändrar SKU eller taggar för det angivna kontot för kognitiva tjänster.</span><span class="sxs-lookup"><span data-stu-id="dbeb5-106">The **Set-AzureRmCognitiveServicesAccount** cmdlet modifies the SKU or tags of the specified Cognitive Services account.</span></span>

## <span data-ttu-id="dbeb5-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="dbeb5-107">EXAMPLES</span></span>

### <span data-ttu-id="dbeb5-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="dbeb5-108">Example 1</span></span>
```powershell
PS C:\> Set-AzureRmCognitiveServicesAccount -ResourceGroupName cognitive-services-resource-group -name myluis -SkuName S0


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

## <span data-ttu-id="dbeb5-109">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="dbeb5-109">PARAMETERS</span></span>

### <span data-ttu-id="dbeb5-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dbeb5-110">-DefaultProfile</span></span>
<span data-ttu-id="dbeb5-111">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="dbeb5-111">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="dbeb5-112">-Force</span><span class="sxs-lookup"><span data-stu-id="dbeb5-112">-Force</span></span>
<span data-ttu-id="dbeb5-113">Tvingar kommandot att köras utan att fråga efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="dbeb5-113">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="dbeb5-114">-Namn</span><span class="sxs-lookup"><span data-stu-id="dbeb5-114">-Name</span></span>
<span data-ttu-id="dbeb5-115">Anger namnet på kontot som ska ändras.</span><span class="sxs-lookup"><span data-stu-id="dbeb5-115">Specifies the name of the account to modify.</span></span>

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

### <span data-ttu-id="dbeb5-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dbeb5-116">-ResourceGroupName</span></span>
<span data-ttu-id="dbeb5-117">Anger namnet på resurs gruppen som kontot är tilldelat till.</span><span class="sxs-lookup"><span data-stu-id="dbeb5-117">Specifies the name of the resource group the account is assigned to.</span></span>

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

### <span data-ttu-id="dbeb5-118">-SkuName</span><span class="sxs-lookup"><span data-stu-id="dbeb5-118">-SkuName</span></span>
<span data-ttu-id="dbeb5-119">Anger SKU för kontot.</span><span class="sxs-lookup"><span data-stu-id="dbeb5-119">Specifies the SKU for the account.</span></span>
<span data-ttu-id="dbeb5-120">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="dbeb5-120">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="dbeb5-121">F0 (kostnads fri nivå)</span><span class="sxs-lookup"><span data-stu-id="dbeb5-121">F0 (free tier)</span></span>
- <span data-ttu-id="dbeb5-122">S0</span><span class="sxs-lookup"><span data-stu-id="dbeb5-122">S0</span></span>
- <span data-ttu-id="dbeb5-123">S</span><span class="sxs-lookup"><span data-stu-id="dbeb5-123">S1</span></span>
- <span data-ttu-id="dbeb5-124">S2</span><span class="sxs-lookup"><span data-stu-id="dbeb5-124">S2</span></span>
- <span data-ttu-id="dbeb5-125">S3</span><span class="sxs-lookup"><span data-stu-id="dbeb5-125">S3</span></span>
- <span data-ttu-id="dbeb5-126">S4</span><span class="sxs-lookup"><span data-stu-id="dbeb5-126">S4</span></span>

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

### <span data-ttu-id="dbeb5-127">-Tagg</span><span class="sxs-lookup"><span data-stu-id="dbeb5-127">-Tag</span></span>
<span data-ttu-id="dbeb5-128">Anger en tagg som ett namn/värde-par.</span><span class="sxs-lookup"><span data-stu-id="dbeb5-128">Specifies a tag as a name/value pair.</span></span>

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

### <span data-ttu-id="dbeb5-129">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="dbeb5-129">-Confirm</span></span>
<span data-ttu-id="dbeb5-130">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="dbeb5-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dbeb5-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dbeb5-131">-WhatIf</span></span>
<span data-ttu-id="dbeb5-132">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="dbeb5-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="dbeb5-133">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="dbeb5-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dbeb5-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dbeb5-134">CommonParameters</span></span>
<span data-ttu-id="dbeb5-135">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dbeb5-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dbeb5-136">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dbeb5-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dbeb5-137">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="dbeb5-137">INPUTS</span></span>

### <span data-ttu-id="dbeb5-138">System. String</span><span class="sxs-lookup"><span data-stu-id="dbeb5-138">System.String</span></span>

### <span data-ttu-id="dbeb5-139">System. Collections. hash-program []</span><span class="sxs-lookup"><span data-stu-id="dbeb5-139">System.Collections.Hashtable[]</span></span>

## <span data-ttu-id="dbeb5-140">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="dbeb5-140">OUTPUTS</span></span>

### <span data-ttu-id="dbeb5-141">Microsoft. Azure. commands. Management. CognitiveServices. Models. PSCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="dbeb5-141">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSCognitiveServicesAccount</span></span>

## <span data-ttu-id="dbeb5-142">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="dbeb5-142">NOTES</span></span>

## <span data-ttu-id="dbeb5-143">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="dbeb5-143">RELATED LINKS</span></span>

[<span data-ttu-id="dbeb5-144">Get-AzureRmCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="dbeb5-144">Get-AzureRmCognitiveServicesAccount</span></span>](./Get-AzureRmCognitiveServicesAccount.md)

[<span data-ttu-id="dbeb5-145">New-AzureRmCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="dbeb5-145">New-AzureRmCognitiveServicesAccount</span></span>](./New-AzureRmCognitiveServicesAccount.md)

[<span data-ttu-id="dbeb5-146">Remove-AzureRmCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="dbeb5-146">Remove-AzureRmCognitiveServicesAccount</span></span>](./Remove-AzureRmCognitiveServicesAccount.md)
