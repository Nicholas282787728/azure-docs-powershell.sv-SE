---
external help file: Microsoft.Azure.Commands.Management.CognitiveServices.dll-Help.xml
Module Name: AzureRM.CognitiveServices
ms.assetid: E0819A61-157A-4DFD-B492-09C8F1C38E18
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/CognitiveServices/Commands.Management.CognitiveServices/help/New-AzureRmCognitiveServicesAccountKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/CognitiveServices/Commands.Management.CognitiveServices/help/New-AzureRmCognitiveServicesAccountKey.md
ms.openlocfilehash: 345e7c6365a66abde5f350f20f614d4d6c94b1b2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93585815"
---
# <span data-ttu-id="8fc0f-101">New-AzureRmCognitiveServicesAccountKey</span><span class="sxs-lookup"><span data-stu-id="8fc0f-101">New-AzureRmCognitiveServicesAccountKey</span></span>

## <span data-ttu-id="8fc0f-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="8fc0f-102">SYNOPSIS</span></span>
<span data-ttu-id="8fc0f-103">Återskapar en konto-nyckeln.</span><span class="sxs-lookup"><span data-stu-id="8fc0f-103">Regenerates an account key.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8fc0f-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="8fc0f-104">SYNTAX</span></span>

```
New-AzureRmCognitiveServicesAccountKey [-ResourceGroupName] <String> [-Name] <String> [-KeyName] <KeyName>
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8fc0f-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="8fc0f-105">DESCRIPTION</span></span>
<span data-ttu-id="8fc0f-106">**New-AzureRmCognitiveServicesAccountKey** cmdlet återskapar en API-nyckeln för ett kognitivt-konto.</span><span class="sxs-lookup"><span data-stu-id="8fc0f-106">The **New-AzureRmCognitiveServicesAccountKey** cmdlet regenerates an API key for a Cognitive Services account.</span></span>

## <span data-ttu-id="8fc0f-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="8fc0f-107">EXAMPLES</span></span>

## <span data-ttu-id="8fc0f-108">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="8fc0f-108">PARAMETERS</span></span>

### <span data-ttu-id="8fc0f-109">-Force</span><span class="sxs-lookup"><span data-stu-id="8fc0f-109">-Force</span></span>
<span data-ttu-id="8fc0f-110">Tvingar kommandot att köras utan att fråga efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="8fc0f-110">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="8fc0f-111">-Namn</span><span class="sxs-lookup"><span data-stu-id="8fc0f-111">-KeyName</span></span>
<span data-ttu-id="8fc0f-112">Anger namnet på den som ska återskapas.</span><span class="sxs-lookup"><span data-stu-id="8fc0f-112">Specifies the name of the key to regenerate.</span></span>
<span data-ttu-id="8fc0f-113">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="8fc0f-113">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="8fc0f-114">Key1</span><span class="sxs-lookup"><span data-stu-id="8fc0f-114">Key1</span></span>
- <span data-ttu-id="8fc0f-115">Key2</span><span class="sxs-lookup"><span data-stu-id="8fc0f-115">Key2</span></span>

```yaml
Type: Microsoft.Azure.Management.CognitiveServices.Models.KeyName
Parameter Sets: (All)
Aliases: 
Accepted values: Key1, Key2

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8fc0f-116">-Namn</span><span class="sxs-lookup"><span data-stu-id="8fc0f-116">-Name</span></span>
<span data-ttu-id="8fc0f-117">Anger namnet på kontot.</span><span class="sxs-lookup"><span data-stu-id="8fc0f-117">Specifies the name of the account.</span></span>

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

### <span data-ttu-id="8fc0f-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8fc0f-118">-ResourceGroupName</span></span>
<span data-ttu-id="8fc0f-119">Anger namnet på resurs gruppen som kontot är tilldelat till.</span><span class="sxs-lookup"><span data-stu-id="8fc0f-119">Specifies the name of the resource group the account is assigned to.</span></span>

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

### <span data-ttu-id="8fc0f-120">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="8fc0f-120">-Confirm</span></span>
<span data-ttu-id="8fc0f-121">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="8fc0f-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8fc0f-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8fc0f-122">-WhatIf</span></span>
<span data-ttu-id="8fc0f-123">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="8fc0f-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8fc0f-124">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="8fc0f-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8fc0f-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8fc0f-125">-DefaultProfile</span></span>
<span data-ttu-id="8fc0f-126">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="8fc0f-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8fc0f-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8fc0f-127">CommonParameters</span></span>
<span data-ttu-id="8fc0f-128">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8fc0f-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8fc0f-129">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8fc0f-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8fc0f-130">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="8fc0f-130">INPUTS</span></span>

## <span data-ttu-id="8fc0f-131">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="8fc0f-131">OUTPUTS</span></span>

### <span data-ttu-id="8fc0f-132">Microsoft. Azure. Management. CognitiveServices. Models. CognitiveServicesAccountKeys</span><span class="sxs-lookup"><span data-stu-id="8fc0f-132">Microsoft.Azure.Management.CognitiveServices.Models.CognitiveServicesAccountKeys</span></span>

## <span data-ttu-id="8fc0f-133">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="8fc0f-133">NOTES</span></span>

## <span data-ttu-id="8fc0f-134">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="8fc0f-134">RELATED LINKS</span></span>

[<span data-ttu-id="8fc0f-135">Get-AzureRmCognitiveServicesAccountKey</span><span class="sxs-lookup"><span data-stu-id="8fc0f-135">Get-AzureRmCognitiveServicesAccountKey</span></span>](./Get-AzureRmCognitiveServicesAccountKey.md)


