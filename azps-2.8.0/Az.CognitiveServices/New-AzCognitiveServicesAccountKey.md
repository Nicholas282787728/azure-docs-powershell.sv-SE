---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CognitiveServices.dll-Help.xml
Module Name: Az.CognitiveServices
ms.assetid: E0819A61-157A-4DFD-B492-09C8F1C38E18
online version: https://docs.microsoft.com/en-us/powershell/module/az.cognitiveservices/new-azcognitiveservicesaccountkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/New-AzCognitiveServicesAccountKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/New-AzCognitiveServicesAccountKey.md
ms.openlocfilehash: ac8bc0e8fd65a82f05108351a5b3140da8c1fb3c
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93745264"
---
# <span data-ttu-id="e7add-101">New-AzCognitiveServicesAccountKey</span><span class="sxs-lookup"><span data-stu-id="e7add-101">New-AzCognitiveServicesAccountKey</span></span>

## <span data-ttu-id="e7add-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="e7add-102">SYNOPSIS</span></span>
<span data-ttu-id="e7add-103">Återskapar en konto-nyckeln.</span><span class="sxs-lookup"><span data-stu-id="e7add-103">Regenerates an account key.</span></span>

## <span data-ttu-id="e7add-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="e7add-104">SYNTAX</span></span>

```
New-AzCognitiveServicesAccountKey [-ResourceGroupName] <String> [-Name] <String> [-KeyName] <KeyName> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e7add-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="e7add-105">DESCRIPTION</span></span>
<span data-ttu-id="e7add-106">**New-AzCognitiveServicesAccountKey** cmdlet återskapar en API-nyckeln för ett kognitivt-konto.</span><span class="sxs-lookup"><span data-stu-id="e7add-106">The **New-AzCognitiveServicesAccountKey** cmdlet regenerates an API key for a Cognitive Services account.</span></span>

## <span data-ttu-id="e7add-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="e7add-107">EXAMPLES</span></span>

### <span data-ttu-id="e7add-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="e7add-108">Example 1</span></span>
```powershell
PS C:\> New-AzCognitiveServicesAccountKey -ResourceGroupName cognitive-services-resource-group -name myluis -keyname Key1

Key1                             Key2
----                             ----
xxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxx xxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxx
```

## <span data-ttu-id="e7add-109">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="e7add-109">PARAMETERS</span></span>

### <span data-ttu-id="e7add-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e7add-110">-DefaultProfile</span></span>
<span data-ttu-id="e7add-111">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="e7add-111">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e7add-112">-Force</span><span class="sxs-lookup"><span data-stu-id="e7add-112">-Force</span></span>
<span data-ttu-id="e7add-113">Tvingar kommandot att köras utan att fråga efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="e7add-113">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="e7add-114">-Namn</span><span class="sxs-lookup"><span data-stu-id="e7add-114">-KeyName</span></span>
<span data-ttu-id="e7add-115">Anger namnet på den som ska återskapas.</span><span class="sxs-lookup"><span data-stu-id="e7add-115">Specifies the name of the key to regenerate.</span></span>
<span data-ttu-id="e7add-116">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="e7add-116">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="e7add-117">Key1</span><span class="sxs-lookup"><span data-stu-id="e7add-117">Key1</span></span>
- <span data-ttu-id="e7add-118">Key2</span><span class="sxs-lookup"><span data-stu-id="e7add-118">Key2</span></span>

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

### <span data-ttu-id="e7add-119">-Namn</span><span class="sxs-lookup"><span data-stu-id="e7add-119">-Name</span></span>
<span data-ttu-id="e7add-120">Anger namnet på kontot.</span><span class="sxs-lookup"><span data-stu-id="e7add-120">Specifies the name of the account.</span></span>

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

### <span data-ttu-id="e7add-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e7add-121">-ResourceGroupName</span></span>
<span data-ttu-id="e7add-122">Anger namnet på resurs gruppen som kontot är tilldelat till.</span><span class="sxs-lookup"><span data-stu-id="e7add-122">Specifies the name of the resource group the account is assigned to.</span></span>

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

### <span data-ttu-id="e7add-123">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="e7add-123">-Confirm</span></span>
<span data-ttu-id="e7add-124">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="e7add-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e7add-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e7add-125">-WhatIf</span></span>
<span data-ttu-id="e7add-126">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="e7add-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e7add-127">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="e7add-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e7add-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e7add-128">CommonParameters</span></span>
<span data-ttu-id="e7add-129">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e7add-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e7add-130">Mer information finns i [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e7add-130">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e7add-131">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="e7add-131">INPUTS</span></span>

### <span data-ttu-id="e7add-132">System. String</span><span class="sxs-lookup"><span data-stu-id="e7add-132">System.String</span></span>

### <span data-ttu-id="e7add-133">Microsoft. Azure. Management. CognitiveServices. Models. Name</span><span class="sxs-lookup"><span data-stu-id="e7add-133">Microsoft.Azure.Management.CognitiveServices.Models.KeyName</span></span>

## <span data-ttu-id="e7add-134">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="e7add-134">OUTPUTS</span></span>

### <span data-ttu-id="e7add-135">Microsoft. Azure. Management. CognitiveServices. Models. CognitiveServicesAccountKeys</span><span class="sxs-lookup"><span data-stu-id="e7add-135">Microsoft.Azure.Management.CognitiveServices.Models.CognitiveServicesAccountKeys</span></span>

## <span data-ttu-id="e7add-136">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="e7add-136">NOTES</span></span>

## <span data-ttu-id="e7add-137">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="e7add-137">RELATED LINKS</span></span>

[<span data-ttu-id="e7add-138">Get-AzCognitiveServicesAccountKey</span><span class="sxs-lookup"><span data-stu-id="e7add-138">Get-AzCognitiveServicesAccountKey</span></span>](./Get-AzCognitiveServicesAccountKey.md)


