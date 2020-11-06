---
external help file: Microsoft.Azure.Commands.Management.CognitiveServices.dll-Help.xml
Module Name: AzureRM.CognitiveServices
ms.assetid: 87A79215-5688-474D-822A-6B84B3D10E3F
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/CognitiveServices/Commands.Management.CognitiveServices/help/Remove-AzureRmCognitiveServicesAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/CognitiveServices/Commands.Management.CognitiveServices/help/Remove-AzureRmCognitiveServicesAccount.md
ms.openlocfilehash: a182bed0e93492521e3ac46d5f0ed3e2d705394c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93585808"
---
# <span data-ttu-id="3da3c-101">Remove-AzureRmCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="3da3c-101">Remove-AzureRmCognitiveServicesAccount</span></span>

## <span data-ttu-id="3da3c-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="3da3c-102">SYNOPSIS</span></span>
<span data-ttu-id="3da3c-103">Tar bort ett konto för kognitiva tjänster.</span><span class="sxs-lookup"><span data-stu-id="3da3c-103">Deletes a Cognitive Services account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3da3c-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="3da3c-104">SYNTAX</span></span>

```
Remove-AzureRmCognitiveServicesAccount [-ResourceGroupName] <String> [-Name] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3da3c-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="3da3c-105">DESCRIPTION</span></span>
<span data-ttu-id="3da3c-106">Cmdleten **Remove-AzureRmCognitiveServicesAccount** tar bort det angivna kontot för kognitiva tjänster.</span><span class="sxs-lookup"><span data-stu-id="3da3c-106">The **Remove-AzureRmCognitiveServicesAccount** cmdlet deletes the specified Cognitive Services account.</span></span>

## <span data-ttu-id="3da3c-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="3da3c-107">EXAMPLES</span></span>

## <span data-ttu-id="3da3c-108">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="3da3c-108">PARAMETERS</span></span>

### <span data-ttu-id="3da3c-109">-Force</span><span class="sxs-lookup"><span data-stu-id="3da3c-109">-Force</span></span>
<span data-ttu-id="3da3c-110">Tvingar kommandot att köras utan att fråga efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="3da3c-110">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="3da3c-111">-Namn</span><span class="sxs-lookup"><span data-stu-id="3da3c-111">-Name</span></span>
<span data-ttu-id="3da3c-112">Anger namnet på kontot som ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="3da3c-112">Specifies the name of the account to delete.</span></span>

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

### <span data-ttu-id="3da3c-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3da3c-113">-ResourceGroupName</span></span>
<span data-ttu-id="3da3c-114">Anger namnet på resurs gruppen som är kopplat till det här kontot.</span><span class="sxs-lookup"><span data-stu-id="3da3c-114">Specifies the name of the resource group the Cognitive Services account is assigned to.</span></span>

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

### <span data-ttu-id="3da3c-115">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="3da3c-115">-Confirm</span></span>
<span data-ttu-id="3da3c-116">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="3da3c-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3da3c-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3da3c-117">-WhatIf</span></span>
<span data-ttu-id="3da3c-118">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="3da3c-118">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3da3c-119">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="3da3c-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3da3c-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3da3c-120">-DefaultProfile</span></span>
<span data-ttu-id="3da3c-121">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="3da3c-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3da3c-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3da3c-122">CommonParameters</span></span>
<span data-ttu-id="3da3c-123">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3da3c-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3da3c-124">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3da3c-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3da3c-125">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="3da3c-125">INPUTS</span></span>

## <span data-ttu-id="3da3c-126">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="3da3c-126">OUTPUTS</span></span>

## <span data-ttu-id="3da3c-127">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="3da3c-127">NOTES</span></span>

## <span data-ttu-id="3da3c-128">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="3da3c-128">RELATED LINKS</span></span>

[<span data-ttu-id="3da3c-129">Get-AzureRmCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="3da3c-129">Get-AzureRmCognitiveServicesAccount</span></span>](./Get-AzureRmCognitiveServicesAccount.md)

[<span data-ttu-id="3da3c-130">New-AzureRmCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="3da3c-130">New-AzureRmCognitiveServicesAccount</span></span>](./New-AzureRmCognitiveServicesAccount.md)

[<span data-ttu-id="3da3c-131">Set-AzureRmCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="3da3c-131">Set-AzureRmCognitiveServicesAccount</span></span>](./Set-AzureRmCognitiveServicesAccount.md)


