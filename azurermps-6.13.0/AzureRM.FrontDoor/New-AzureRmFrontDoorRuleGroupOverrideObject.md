---
external help file: Microsoft.Azure.Commands.FrontDoor.dll-Help.xml
Module Name: AzureRM.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.frontdoor/new-azurermfrontdoorrulegroupoverrideobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/FrontDoor/Commands.FrontDoor/help/New-AzureRmFrontDoorRuleGroupOverrideObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/FrontDoor/Commands.FrontDoor/help/New-AzureRmFrontDoorRuleGroupOverrideObject.md
ms.openlocfilehash: 02253a59a7f05bfdecd8147325575605334f13ee
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93572755"
---
# <span data-ttu-id="3c9b2-101">New-AzureRmFrontDoorRuleGroupOverrideObject</span><span class="sxs-lookup"><span data-stu-id="3c9b2-101">New-AzureRmFrontDoorRuleGroupOverrideObject</span></span>

## <span data-ttu-id="3c9b2-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="3c9b2-102">SYNOPSIS</span></span>
<span data-ttu-id="3c9b2-103">Skapa RuleGroupOverride-objekt för WAF-princip</span><span class="sxs-lookup"><span data-stu-id="3c9b2-103">Create RuleGroupOverride Object for WAF policy creation</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3c9b2-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="3c9b2-104">SYNTAX</span></span>

```
New-AzureRmFrontDoorRuleGroupOverrideObject -Override <PSRuleGroupOverride> -Action <PSAction>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3c9b2-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="3c9b2-105">DESCRIPTION</span></span>
<span data-ttu-id="3c9b2-106">Skapa RuleGroupOverride-objekt för WAF-princip</span><span class="sxs-lookup"><span data-stu-id="3c9b2-106">Create RuleGroupOverride Object for WAF policy creation</span></span>

## <span data-ttu-id="3c9b2-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="3c9b2-107">EXAMPLES</span></span>

### <span data-ttu-id="3c9b2-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="3c9b2-108">Example 1</span></span>
```powershell
PS C:\>  New-AzureRmFrontDoorRuleGroupOverrideObject -Override SqlInjection -Action Block

Action RuleGroupOverride
------ -----------------
 Block      SqlInjection
```

<span data-ttu-id="3c9b2-109">Skapa ett RuleGroupOverride-objekt</span><span class="sxs-lookup"><span data-stu-id="3c9b2-109">Create a RuleGroupOverride Object</span></span>

## <span data-ttu-id="3c9b2-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="3c9b2-110">PARAMETERS</span></span>

### <span data-ttu-id="3c9b2-111">-Åtgärd</span><span class="sxs-lookup"><span data-stu-id="3c9b2-111">-Action</span></span>
<span data-ttu-id="3c9b2-112">Typ av åtgärder.</span><span class="sxs-lookup"><span data-stu-id="3c9b2-112">Type of Actions.</span></span>
<span data-ttu-id="3c9b2-113">Möjliga värden inkluderar: "Tillåt", "blockera", "log"</span><span class="sxs-lookup"><span data-stu-id="3c9b2-113">Possible values include: 'Allow', 'Block', 'Log'</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSAction
Parameter Sets: (All)
Aliases:
Accepted values: Allow, Block, Log

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3c9b2-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3c9b2-114">-DefaultProfile</span></span>
<span data-ttu-id="3c9b2-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="3c9b2-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3c9b2-116">-Åsidosätt</span><span class="sxs-lookup"><span data-stu-id="3c9b2-116">-Override</span></span>
<span data-ttu-id="3c9b2-117">Beskriver overrideruleGroup.</span><span class="sxs-lookup"><span data-stu-id="3c9b2-117">Describes overrideruleGroup.</span></span>
<span data-ttu-id="3c9b2-118">Möjliga värden är: ' SqlInjection ', ' XSS '</span><span class="sxs-lookup"><span data-stu-id="3c9b2-118">Possible values include: 'SqlInjection', 'XSS'</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSRuleGroupOverride
Parameter Sets: (All)
Aliases:
Accepted values: SqlInjection, XSS

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3c9b2-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3c9b2-119">CommonParameters</span></span>
<span data-ttu-id="3c9b2-120">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3c9b2-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3c9b2-121">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3c9b2-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3c9b2-122">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="3c9b2-122">INPUTS</span></span>

### <span data-ttu-id="3c9b2-123">Ingen</span><span class="sxs-lookup"><span data-stu-id="3c9b2-123">None</span></span>

## <span data-ttu-id="3c9b2-124">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="3c9b2-124">OUTPUTS</span></span>

### <span data-ttu-id="3c9b2-125">Microsoft. Azure. commands. FrontDoor. Models. PSAzureRuleGroupOverride</span><span class="sxs-lookup"><span data-stu-id="3c9b2-125">Microsoft.Azure.Commands.FrontDoor.Models.PSAzureRuleGroupOverride</span></span>

## <span data-ttu-id="3c9b2-126">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="3c9b2-126">NOTES</span></span>

## <span data-ttu-id="3c9b2-127">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="3c9b2-127">RELATED LINKS</span></span>

[<span data-ttu-id="3c9b2-128">New-AzureRmFrontDoorManagedRuleObject</span><span class="sxs-lookup"><span data-stu-id="3c9b2-128">New-AzureRmFrontDoorManagedRuleObject</span></span>](./New-AzureRmFrontDoorManagedRuleObject.md)
