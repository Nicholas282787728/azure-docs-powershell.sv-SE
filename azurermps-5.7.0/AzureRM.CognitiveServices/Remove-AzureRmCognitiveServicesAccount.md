---
external help file: Microsoft.Azure.Commands.Management.CognitiveServices.dll-Help.xml
Module Name: AzureRM.CognitiveServices
ms.assetid: 87A79215-5688-474D-822A-6B84B3D10E3F
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.cognitiveservices/remove-azurermcognitiveservicesaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/CognitiveServices/Commands.Management.CognitiveServices/help/Remove-AzureRmCognitiveServicesAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/CognitiveServices/Commands.Management.CognitiveServices/help/Remove-AzureRmCognitiveServicesAccount.md
ms.openlocfilehash: 7c77f11842c224a0a023215175f52bf451867296
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93584447"
---
# <span data-ttu-id="72e72-101">Remove-AzureRmCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="72e72-101">Remove-AzureRmCognitiveServicesAccount</span></span>

## <span data-ttu-id="72e72-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="72e72-102">SYNOPSIS</span></span>
<span data-ttu-id="72e72-103">Tar bort ett konto för kognitiva tjänster.</span><span class="sxs-lookup"><span data-stu-id="72e72-103">Deletes a Cognitive Services account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="72e72-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="72e72-104">SYNTAX</span></span>

```
Remove-AzureRmCognitiveServicesAccount [-ResourceGroupName] <String> [-Name] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="72e72-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="72e72-105">DESCRIPTION</span></span>
<span data-ttu-id="72e72-106">Cmdleten **Remove-AzureRmCognitiveServicesAccount** tar bort det angivna kontot för kognitiva tjänster.</span><span class="sxs-lookup"><span data-stu-id="72e72-106">The **Remove-AzureRmCognitiveServicesAccount** cmdlet deletes the specified Cognitive Services account.</span></span>

## <span data-ttu-id="72e72-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="72e72-107">EXAMPLES</span></span>

## <span data-ttu-id="72e72-108">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="72e72-108">PARAMETERS</span></span>

### <span data-ttu-id="72e72-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="72e72-109">-DefaultProfile</span></span>
<span data-ttu-id="72e72-110">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="72e72-110">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="72e72-111">-Force</span><span class="sxs-lookup"><span data-stu-id="72e72-111">-Force</span></span>
<span data-ttu-id="72e72-112">Tvingar kommandot att köras utan att fråga efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="72e72-112">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="72e72-113">-Namn</span><span class="sxs-lookup"><span data-stu-id="72e72-113">-Name</span></span>
<span data-ttu-id="72e72-114">Anger namnet på kontot som ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="72e72-114">Specifies the name of the account to delete.</span></span>

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

### <span data-ttu-id="72e72-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="72e72-115">-ResourceGroupName</span></span>
<span data-ttu-id="72e72-116">Anger namnet på resurs gruppen som är kopplat till det här kontot.</span><span class="sxs-lookup"><span data-stu-id="72e72-116">Specifies the name of the resource group the Cognitive Services account is assigned to.</span></span>

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

### <span data-ttu-id="72e72-117">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="72e72-117">-Confirm</span></span>
<span data-ttu-id="72e72-118">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="72e72-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="72e72-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="72e72-119">-WhatIf</span></span>
<span data-ttu-id="72e72-120">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="72e72-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="72e72-121">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="72e72-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="72e72-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="72e72-122">CommonParameters</span></span>
<span data-ttu-id="72e72-123">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="72e72-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="72e72-124">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="72e72-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="72e72-125">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="72e72-125">INPUTS</span></span>

### <span data-ttu-id="72e72-126">Ingen</span><span class="sxs-lookup"><span data-stu-id="72e72-126">None</span></span>
<span data-ttu-id="72e72-127">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="72e72-127">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="72e72-128">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="72e72-128">OUTPUTS</span></span>

## <span data-ttu-id="72e72-129">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="72e72-129">NOTES</span></span>

## <span data-ttu-id="72e72-130">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="72e72-130">RELATED LINKS</span></span>

[<span data-ttu-id="72e72-131">Get-AzureRmCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="72e72-131">Get-AzureRmCognitiveServicesAccount</span></span>](./Get-AzureRmCognitiveServicesAccount.md)

[<span data-ttu-id="72e72-132">New-AzureRmCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="72e72-132">New-AzureRmCognitiveServicesAccount</span></span>](./New-AzureRmCognitiveServicesAccount.md)

[<span data-ttu-id="72e72-133">Set-AzureRmCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="72e72-133">Set-AzureRmCognitiveServicesAccount</span></span>](./Set-AzureRmCognitiveServicesAccount.md)


