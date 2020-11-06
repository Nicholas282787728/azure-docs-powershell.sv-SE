---
external help file: Microsoft.Azure.Commands.Management.CognitiveServices.dll-Help.xml
Module Name: AzureRM.CognitiveServices
ms.assetid: E0819A61-157A-4DFD-B492-09C8F1C38E18
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.cognitiveservices/new-azurermcognitiveservicesaccountkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/CognitiveServices/Commands.Management.CognitiveServices/help/New-AzureRmCognitiveServicesAccountKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/CognitiveServices/Commands.Management.CognitiveServices/help/New-AzureRmCognitiveServicesAccountKey.md
ms.openlocfilehash: 1c3ebaf3e95c1094b02b73505e471d13015721d7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93574374"
---
# <span data-ttu-id="954a6-101">New-AzureRmCognitiveServicesAccountKey</span><span class="sxs-lookup"><span data-stu-id="954a6-101">New-AzureRmCognitiveServicesAccountKey</span></span>

## <span data-ttu-id="954a6-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="954a6-102">SYNOPSIS</span></span>
<span data-ttu-id="954a6-103">Återskapar en konto-nyckeln.</span><span class="sxs-lookup"><span data-stu-id="954a6-103">Regenerates an account key.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="954a6-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="954a6-104">SYNTAX</span></span>

```
New-AzureRmCognitiveServicesAccountKey [-ResourceGroupName] <String> [-Name] <String> [-KeyName] <KeyName>
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="954a6-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="954a6-105">DESCRIPTION</span></span>
<span data-ttu-id="954a6-106">**New-AzureRmCognitiveServicesAccountKey** cmdlet återskapar en API-nyckeln för ett kognitivt-konto.</span><span class="sxs-lookup"><span data-stu-id="954a6-106">The **New-AzureRmCognitiveServicesAccountKey** cmdlet regenerates an API key for a Cognitive Services account.</span></span>

## <span data-ttu-id="954a6-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="954a6-107">EXAMPLES</span></span>

## <span data-ttu-id="954a6-108">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="954a6-108">PARAMETERS</span></span>

### <span data-ttu-id="954a6-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="954a6-109">-DefaultProfile</span></span>
<span data-ttu-id="954a6-110">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="954a6-110">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="954a6-111">-Force</span><span class="sxs-lookup"><span data-stu-id="954a6-111">-Force</span></span>
<span data-ttu-id="954a6-112">Tvingar kommandot att köras utan att fråga efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="954a6-112">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="954a6-113">-Namn</span><span class="sxs-lookup"><span data-stu-id="954a6-113">-KeyName</span></span>
<span data-ttu-id="954a6-114">Anger namnet på den som ska återskapas.</span><span class="sxs-lookup"><span data-stu-id="954a6-114">Specifies the name of the key to regenerate.</span></span>
<span data-ttu-id="954a6-115">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="954a6-115">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="954a6-116">Key1</span><span class="sxs-lookup"><span data-stu-id="954a6-116">Key1</span></span>
- <span data-ttu-id="954a6-117">Key2</span><span class="sxs-lookup"><span data-stu-id="954a6-117">Key2</span></span>

```yaml
Type: KeyName
Parameter Sets: (All)
Aliases: 
Accepted values: Key1, Key2

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="954a6-118">-Namn</span><span class="sxs-lookup"><span data-stu-id="954a6-118">-Name</span></span>
<span data-ttu-id="954a6-119">Anger namnet på kontot.</span><span class="sxs-lookup"><span data-stu-id="954a6-119">Specifies the name of the account.</span></span>

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

### <span data-ttu-id="954a6-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="954a6-120">-ResourceGroupName</span></span>
<span data-ttu-id="954a6-121">Anger namnet på resurs gruppen som kontot är tilldelat till.</span><span class="sxs-lookup"><span data-stu-id="954a6-121">Specifies the name of the resource group the account is assigned to.</span></span>

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

### <span data-ttu-id="954a6-122">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="954a6-122">-Confirm</span></span>
<span data-ttu-id="954a6-123">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="954a6-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="954a6-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="954a6-124">-WhatIf</span></span>
<span data-ttu-id="954a6-125">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="954a6-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="954a6-126">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="954a6-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="954a6-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="954a6-127">CommonParameters</span></span>
<span data-ttu-id="954a6-128">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="954a6-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="954a6-129">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="954a6-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="954a6-130">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="954a6-130">INPUTS</span></span>

### <span data-ttu-id="954a6-131">Ingen</span><span class="sxs-lookup"><span data-stu-id="954a6-131">None</span></span>
<span data-ttu-id="954a6-132">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="954a6-132">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="954a6-133">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="954a6-133">OUTPUTS</span></span>

### <span data-ttu-id="954a6-134">Microsoft. Azure. Management. CognitiveServices. Models. CognitiveServicesAccountKeys</span><span class="sxs-lookup"><span data-stu-id="954a6-134">Microsoft.Azure.Management.CognitiveServices.Models.CognitiveServicesAccountKeys</span></span>

## <span data-ttu-id="954a6-135">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="954a6-135">NOTES</span></span>

## <span data-ttu-id="954a6-136">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="954a6-136">RELATED LINKS</span></span>

[<span data-ttu-id="954a6-137">Get-AzureRmCognitiveServicesAccountKey</span><span class="sxs-lookup"><span data-stu-id="954a6-137">Get-AzureRmCognitiveServicesAccountKey</span></span>](./Get-AzureRmCognitiveServicesAccountKey.md)


