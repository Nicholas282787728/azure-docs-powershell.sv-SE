---
external help file: Microsoft.Azure.Commands.Management.CognitiveServices.dll-Help.xml
Module Name: AzureRM.CognitiveServices
ms.assetid: E0819A61-157A-4DFD-B492-09C8F1C38E18
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.cognitiveservices/new-azurermcognitiveservicesaccountkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/CognitiveServices/Commands.Management.CognitiveServices/help/New-AzureRmCognitiveServicesAccountKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/CognitiveServices/Commands.Management.CognitiveServices/help/New-AzureRmCognitiveServicesAccountKey.md
ms.openlocfilehash: 4701ae347f5a6ea8cd294a0ff75efa51f4d1370d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93756400"
---
# <span data-ttu-id="365fb-101">New-AzureRmCognitiveServicesAccountKey</span><span class="sxs-lookup"><span data-stu-id="365fb-101">New-AzureRmCognitiveServicesAccountKey</span></span>

## <span data-ttu-id="365fb-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="365fb-102">SYNOPSIS</span></span>
<span data-ttu-id="365fb-103">Återskapar en konto-nyckeln.</span><span class="sxs-lookup"><span data-stu-id="365fb-103">Regenerates an account key.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="365fb-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="365fb-104">SYNTAX</span></span>

```
New-AzureRmCognitiveServicesAccountKey [-ResourceGroupName] <String> [-Name] <String> [-KeyName] <KeyName>
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="365fb-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="365fb-105">DESCRIPTION</span></span>
<span data-ttu-id="365fb-106">**New-AzureRmCognitiveServicesAccountKey** cmdlet återskapar en API-nyckeln för ett kognitivt-konto.</span><span class="sxs-lookup"><span data-stu-id="365fb-106">The **New-AzureRmCognitiveServicesAccountKey** cmdlet regenerates an API key for a Cognitive Services account.</span></span>

## <span data-ttu-id="365fb-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="365fb-107">EXAMPLES</span></span>

### <span data-ttu-id="365fb-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="365fb-108">Example 1</span></span>
```powershell
PS C:\> New-AzureRmCognitiveServicesAccountKey -ResourceGroupName cognitive-services-resource-group -name myluis -keyname Key1

Key1                             Key2
----                             ----
xxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxx xxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxx
```

## <span data-ttu-id="365fb-109">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="365fb-109">PARAMETERS</span></span>

### <span data-ttu-id="365fb-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="365fb-110">-DefaultProfile</span></span>
<span data-ttu-id="365fb-111">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="365fb-111">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="365fb-112">-Force</span><span class="sxs-lookup"><span data-stu-id="365fb-112">-Force</span></span>
<span data-ttu-id="365fb-113">Tvingar kommandot att köras utan att fråga efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="365fb-113">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="365fb-114">-Namn</span><span class="sxs-lookup"><span data-stu-id="365fb-114">-KeyName</span></span>
<span data-ttu-id="365fb-115">Anger namnet på den som ska återskapas.</span><span class="sxs-lookup"><span data-stu-id="365fb-115">Specifies the name of the key to regenerate.</span></span>
<span data-ttu-id="365fb-116">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="365fb-116">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="365fb-117">Key1</span><span class="sxs-lookup"><span data-stu-id="365fb-117">Key1</span></span>
- <span data-ttu-id="365fb-118">Key2</span><span class="sxs-lookup"><span data-stu-id="365fb-118">Key2</span></span>

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

### <span data-ttu-id="365fb-119">-Namn</span><span class="sxs-lookup"><span data-stu-id="365fb-119">-Name</span></span>
<span data-ttu-id="365fb-120">Anger namnet på kontot.</span><span class="sxs-lookup"><span data-stu-id="365fb-120">Specifies the name of the account.</span></span>

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

### <span data-ttu-id="365fb-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="365fb-121">-ResourceGroupName</span></span>
<span data-ttu-id="365fb-122">Anger namnet på resurs gruppen som kontot är tilldelat till.</span><span class="sxs-lookup"><span data-stu-id="365fb-122">Specifies the name of the resource group the account is assigned to.</span></span>

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

### <span data-ttu-id="365fb-123">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="365fb-123">-Confirm</span></span>
<span data-ttu-id="365fb-124">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="365fb-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="365fb-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="365fb-125">-WhatIf</span></span>
<span data-ttu-id="365fb-126">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="365fb-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="365fb-127">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="365fb-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="365fb-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="365fb-128">CommonParameters</span></span>
<span data-ttu-id="365fb-129">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="365fb-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="365fb-130">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="365fb-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="365fb-131">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="365fb-131">INPUTS</span></span>

### <span data-ttu-id="365fb-132">System. String</span><span class="sxs-lookup"><span data-stu-id="365fb-132">System.String</span></span>

### <span data-ttu-id="365fb-133">Microsoft. Azure. Management. CognitiveServices. Models. Name</span><span class="sxs-lookup"><span data-stu-id="365fb-133">Microsoft.Azure.Management.CognitiveServices.Models.KeyName</span></span>

## <span data-ttu-id="365fb-134">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="365fb-134">OUTPUTS</span></span>

### <span data-ttu-id="365fb-135">Microsoft. Azure. Management. CognitiveServices. Models. CognitiveServicesAccountKeys</span><span class="sxs-lookup"><span data-stu-id="365fb-135">Microsoft.Azure.Management.CognitiveServices.Models.CognitiveServicesAccountKeys</span></span>

## <span data-ttu-id="365fb-136">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="365fb-136">NOTES</span></span>

## <span data-ttu-id="365fb-137">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="365fb-137">RELATED LINKS</span></span>

[<span data-ttu-id="365fb-138">Get-AzureRmCognitiveServicesAccountKey</span><span class="sxs-lookup"><span data-stu-id="365fb-138">Get-AzureRmCognitiveServicesAccountKey</span></span>](./Get-AzureRmCognitiveServicesAccountKey.md)


