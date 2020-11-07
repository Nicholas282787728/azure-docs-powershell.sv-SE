---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CognitiveServices.dll-Help.xml
Module Name: Az.CognitiveServices
ms.assetid: 87A79215-5688-474D-822A-6B84B3D10E3F
online version: https://docs.microsoft.com/en-us/powershell/module/az.cognitiveservices/remove-azcognitiveservicesaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/Remove-AzCognitiveServicesAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/Remove-AzCognitiveServicesAccount.md
ms.openlocfilehash: ad3c5359d80f3133e6bb48ea73c1d6a93501288a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93754616"
---
# <span data-ttu-id="40a88-101">Remove-AzCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="40a88-101">Remove-AzCognitiveServicesAccount</span></span>

## <span data-ttu-id="40a88-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="40a88-102">SYNOPSIS</span></span>
<span data-ttu-id="40a88-103">Tar bort ett konto för kognitiva tjänster.</span><span class="sxs-lookup"><span data-stu-id="40a88-103">Deletes a Cognitive Services account.</span></span>

## <span data-ttu-id="40a88-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="40a88-104">SYNTAX</span></span>

```
Remove-AzCognitiveServicesAccount [-ResourceGroupName] <String> [-Name] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="40a88-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="40a88-105">DESCRIPTION</span></span>
<span data-ttu-id="40a88-106">Cmdleten **Remove-AzCognitiveServicesAccount** tar bort det angivna kontot för kognitiva tjänster.</span><span class="sxs-lookup"><span data-stu-id="40a88-106">The **Remove-AzCognitiveServicesAccount** cmdlet deletes the specified Cognitive Services account.</span></span>

## <span data-ttu-id="40a88-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="40a88-107">EXAMPLES</span></span>

### <span data-ttu-id="40a88-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="40a88-108">Example 1</span></span>
<span data-ttu-id="40a88-109">Det här kommandot returnerar ingenting.</span><span class="sxs-lookup"><span data-stu-id="40a88-109">This command doesn't return anything.</span></span>

```powershell
PS C:\> Remove-AzCognitiveServicesAccount -ResourceGroupName cognitive-services-resource-group -name myluis
PS C:\>
```

## <span data-ttu-id="40a88-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="40a88-110">PARAMETERS</span></span>

### <span data-ttu-id="40a88-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="40a88-111">-DefaultProfile</span></span>
<span data-ttu-id="40a88-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="40a88-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="40a88-113">-Force</span><span class="sxs-lookup"><span data-stu-id="40a88-113">-Force</span></span>
<span data-ttu-id="40a88-114">Tvingar kommandot att köras utan att fråga efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="40a88-114">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="40a88-115">-Namn</span><span class="sxs-lookup"><span data-stu-id="40a88-115">-Name</span></span>
<span data-ttu-id="40a88-116">Anger namnet på kontot som ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="40a88-116">Specifies the name of the account to delete.</span></span>

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

### <span data-ttu-id="40a88-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="40a88-117">-ResourceGroupName</span></span>
<span data-ttu-id="40a88-118">Anger namnet på resurs gruppen som är kopplat till det här kontot.</span><span class="sxs-lookup"><span data-stu-id="40a88-118">Specifies the name of the resource group the Cognitive Services account is assigned to.</span></span>

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

### <span data-ttu-id="40a88-119">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="40a88-119">-Confirm</span></span>
<span data-ttu-id="40a88-120">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="40a88-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="40a88-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="40a88-121">-WhatIf</span></span>
<span data-ttu-id="40a88-122">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="40a88-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="40a88-123">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="40a88-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="40a88-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="40a88-124">CommonParameters</span></span>
<span data-ttu-id="40a88-125">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="40a88-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="40a88-126">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="40a88-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="40a88-127">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="40a88-127">INPUTS</span></span>

### <span data-ttu-id="40a88-128">System. String</span><span class="sxs-lookup"><span data-stu-id="40a88-128">System.String</span></span>

## <span data-ttu-id="40a88-129">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="40a88-129">OUTPUTS</span></span>

### <span data-ttu-id="40a88-130">System. Void</span><span class="sxs-lookup"><span data-stu-id="40a88-130">System.Void</span></span>

## <span data-ttu-id="40a88-131">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="40a88-131">NOTES</span></span>

## <span data-ttu-id="40a88-132">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="40a88-132">RELATED LINKS</span></span>

[<span data-ttu-id="40a88-133">Get-AzCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="40a88-133">Get-AzCognitiveServicesAccount</span></span>](./Get-AzCognitiveServicesAccount.md)

[<span data-ttu-id="40a88-134">New-AzCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="40a88-134">New-AzCognitiveServicesAccount</span></span>](./New-AzCognitiveServicesAccount.md)

[<span data-ttu-id="40a88-135">Set-AzCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="40a88-135">Set-AzCognitiveServicesAccount</span></span>](./Set-AzCognitiveServicesAccount.md)


