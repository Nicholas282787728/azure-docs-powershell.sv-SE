---
external help file: Microsoft.Azure.Commands.Management.CognitiveServices.dll-Help.xml
Module Name: AzureRM.CognitiveServices
ms.assetid: 11E2D82A-1DF1-4E19-8328-44674641D1BB
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.cognitiveservices/set-azurermcognitiveservicesaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/CognitiveServices/Commands.Management.CognitiveServices/help/Set-AzureRmCognitiveServicesAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/CognitiveServices/Commands.Management.CognitiveServices/help/Set-AzureRmCognitiveServicesAccount.md
ms.openlocfilehash: a31ee6979a73e4637e683a5b388f4265bf53d2a2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93584444"
---
# <span data-ttu-id="0cfff-101">Set-AzureRmCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="0cfff-101">Set-AzureRmCognitiveServicesAccount</span></span>

## <span data-ttu-id="0cfff-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="0cfff-102">SYNOPSIS</span></span>
<span data-ttu-id="0cfff-103">Ändrar ett konto.</span><span class="sxs-lookup"><span data-stu-id="0cfff-103">Modifies an account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0cfff-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="0cfff-104">SYNTAX</span></span>

```
Set-AzureRmCognitiveServicesAccount [-ResourceGroupName] <String> [-Name] <String> [-SkuName <String>]
 [-Tag <Hashtable[]>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="0cfff-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="0cfff-105">DESCRIPTION</span></span>
<span data-ttu-id="0cfff-106">Cmdleten **set-AzureRmCognitiveServicesAccount** ändrar SKU eller taggar för det angivna kontot för kognitiva tjänster.</span><span class="sxs-lookup"><span data-stu-id="0cfff-106">The **Set-AzureRmCognitiveServicesAccount** cmdlet modifies the SKU or tags of the specified Cognitive Services account.</span></span>

## <span data-ttu-id="0cfff-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="0cfff-107">EXAMPLES</span></span>

## <span data-ttu-id="0cfff-108">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="0cfff-108">PARAMETERS</span></span>

### <span data-ttu-id="0cfff-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0cfff-109">-DefaultProfile</span></span>
<span data-ttu-id="0cfff-110">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="0cfff-110">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="0cfff-111">-Force</span><span class="sxs-lookup"><span data-stu-id="0cfff-111">-Force</span></span>
<span data-ttu-id="0cfff-112">Tvingar kommandot att köras utan att fråga efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="0cfff-112">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="0cfff-113">-Namn</span><span class="sxs-lookup"><span data-stu-id="0cfff-113">-Name</span></span>
<span data-ttu-id="0cfff-114">Anger namnet på kontot som ska ändras.</span><span class="sxs-lookup"><span data-stu-id="0cfff-114">Specifies the name of the account to modify.</span></span>

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

### <span data-ttu-id="0cfff-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0cfff-115">-ResourceGroupName</span></span>
<span data-ttu-id="0cfff-116">Anger namnet på resurs gruppen som kontot är tilldelat till.</span><span class="sxs-lookup"><span data-stu-id="0cfff-116">Specifies the name of the resource group the account is assigned to.</span></span>

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

### <span data-ttu-id="0cfff-117">-SkuName</span><span class="sxs-lookup"><span data-stu-id="0cfff-117">-SkuName</span></span>
<span data-ttu-id="0cfff-118">Anger SKU för kontot.</span><span class="sxs-lookup"><span data-stu-id="0cfff-118">Specifies the SKU for the account.</span></span>
<span data-ttu-id="0cfff-119">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="0cfff-119">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="0cfff-120">F0 (kostnads fri nivå)</span><span class="sxs-lookup"><span data-stu-id="0cfff-120">F0 (free tier)</span></span>
- <span data-ttu-id="0cfff-121">S0</span><span class="sxs-lookup"><span data-stu-id="0cfff-121">S0</span></span>
- <span data-ttu-id="0cfff-122">S</span><span class="sxs-lookup"><span data-stu-id="0cfff-122">S1</span></span>
- <span data-ttu-id="0cfff-123">S2</span><span class="sxs-lookup"><span data-stu-id="0cfff-123">S2</span></span>
- <span data-ttu-id="0cfff-124">S3</span><span class="sxs-lookup"><span data-stu-id="0cfff-124">S3</span></span>
- <span data-ttu-id="0cfff-125">S4</span><span class="sxs-lookup"><span data-stu-id="0cfff-125">S4</span></span>

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

### <span data-ttu-id="0cfff-126">-Tagg</span><span class="sxs-lookup"><span data-stu-id="0cfff-126">-Tag</span></span>
<span data-ttu-id="0cfff-127">Anger en tagg som ett namn/värde-par.</span><span class="sxs-lookup"><span data-stu-id="0cfff-127">Specifies a tag as a name/value pair.</span></span>

```yaml
Type: Hashtable[]
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0cfff-128">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="0cfff-128">-Confirm</span></span>
<span data-ttu-id="0cfff-129">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="0cfff-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0cfff-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0cfff-130">-WhatIf</span></span>
<span data-ttu-id="0cfff-131">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="0cfff-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0cfff-132">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="0cfff-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0cfff-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0cfff-133">CommonParameters</span></span>
<span data-ttu-id="0cfff-134">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0cfff-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0cfff-135">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0cfff-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0cfff-136">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="0cfff-136">INPUTS</span></span>

### <span data-ttu-id="0cfff-137">Ingen</span><span class="sxs-lookup"><span data-stu-id="0cfff-137">None</span></span>
<span data-ttu-id="0cfff-138">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="0cfff-138">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="0cfff-139">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="0cfff-139">OUTPUTS</span></span>

### <span data-ttu-id="0cfff-140">Microsoft. Azure. commands. Management. CognitiveServices. Models. PSCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="0cfff-140">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSCognitiveServicesAccount</span></span>

## <span data-ttu-id="0cfff-141">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="0cfff-141">NOTES</span></span>

## <span data-ttu-id="0cfff-142">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="0cfff-142">RELATED LINKS</span></span>

[<span data-ttu-id="0cfff-143">Get-AzureRmCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="0cfff-143">Get-AzureRmCognitiveServicesAccount</span></span>](./Get-AzureRmCognitiveServicesAccount.md)

[<span data-ttu-id="0cfff-144">New-AzureRmCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="0cfff-144">New-AzureRmCognitiveServicesAccount</span></span>](./New-AzureRmCognitiveServicesAccount.md)

[<span data-ttu-id="0cfff-145">Remove-AzureRmCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="0cfff-145">Remove-AzureRmCognitiveServicesAccount</span></span>](./Remove-AzureRmCognitiveServicesAccount.md)
