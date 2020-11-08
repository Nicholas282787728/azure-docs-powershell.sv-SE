---
external help file: Microsoft.Azure.Commands.Automation.dll-Help.xml
ms.assetid: 454948A7-CE50-4C5A-AEBF-789B1A94F27E
online version: ''
schema: 2.0.0
ms.openlocfilehash: 62507f18e21c1e528f93f5de512e8ffc1fa2dfa3
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94099115"
---
# <span data-ttu-id="14e2b-101">Publish-AzureAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="14e2b-101">Publish-AzureAutomationRunbook</span></span>

## <span data-ttu-id="14e2b-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="14e2b-102">SYNOPSIS</span></span>

<span data-ttu-id="14e2b-103">Publicerar en Runbook.</span><span class="sxs-lookup"><span data-stu-id="14e2b-103">Publishes a runbook.</span></span>

## <span data-ttu-id="14e2b-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="14e2b-104">SYNTAX</span></span>

```
Publish-AzureAutomationRunbook -Name <String> -AutomationAccountName <String> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="14e2b-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="14e2b-105">DESCRIPTION</span></span>

[!INCLUDE [aa-deprecation](../include/aa-deprecation.md)]

<span data-ttu-id="14e2b-106">Cmdleten **Publishing-AzureAutomationRunbook** publicerar en Runbook för användning i produktions miljön för Microsoft Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="14e2b-106">The **Publish-AzureAutomationRunbook** cmdlet publishes a runbook for use in the production environment of Microsoft Azure Automation.</span></span>

## <span data-ttu-id="14e2b-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="14e2b-107">EXAMPLES</span></span>

### <span data-ttu-id="14e2b-108">Exempel 1: publicera en Runbook</span><span class="sxs-lookup"><span data-stu-id="14e2b-108">Example 1: Publish a runbook</span></span>
```
PS C:\> Publish-AzureAutomationRunbook -AutomationAccountName "Contoso17" -Name "Runbk01"
```

<span data-ttu-id="14e2b-109">Det här kommandot publicerar Runbook-flödet som heter Runbk01 i Automation-kontot med namnet Contoso17.</span><span class="sxs-lookup"><span data-stu-id="14e2b-109">This command publishes the runbook named Runbk01 in the Automation account named Contoso17.</span></span>

## <span data-ttu-id="14e2b-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="14e2b-110">PARAMETERS</span></span>

### <span data-ttu-id="14e2b-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="14e2b-111">-AutomationAccountName</span></span>
<span data-ttu-id="14e2b-112">Anger namnet på Automation-kontot.</span><span class="sxs-lookup"><span data-stu-id="14e2b-112">Specifies the name of the Automation account.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="14e2b-113">-Namn</span><span class="sxs-lookup"><span data-stu-id="14e2b-113">-Name</span></span>
<span data-ttu-id="14e2b-114">Anger namnet på Runbook-flödet.</span><span class="sxs-lookup"><span data-stu-id="14e2b-114">Specifies the name of the runbook.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: RunbookName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="14e2b-115">-Profil</span><span class="sxs-lookup"><span data-stu-id="14e2b-115">-Profile</span></span>
<span data-ttu-id="14e2b-116">Anger den Azure-profil från vilken denna cmdlet läser.</span><span class="sxs-lookup"><span data-stu-id="14e2b-116">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="14e2b-117">Om du inte anger en profil läser denna cmdlet från den lokala standard profilen.</span><span class="sxs-lookup"><span data-stu-id="14e2b-117">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="14e2b-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="14e2b-118">CommonParameters</span></span>
<span data-ttu-id="14e2b-119">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="14e2b-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="14e2b-120">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="14e2b-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="14e2b-121">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="14e2b-121">INPUTS</span></span>

## <span data-ttu-id="14e2b-122">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="14e2b-122">OUTPUTS</span></span>

## <span data-ttu-id="14e2b-123">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="14e2b-123">NOTES</span></span>

## <span data-ttu-id="14e2b-124">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="14e2b-124">RELATED LINKS</span></span>

[<span data-ttu-id="14e2b-125">Get-AzureAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="14e2b-125">Get-AzureAutomationRunbook</span></span>](./Get-AzureAutomationRunbook.md)

[<span data-ttu-id="14e2b-126">New-AzureAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="14e2b-126">New-AzureAutomationRunbook</span></span>](./New-AzureAutomationRunbook.md)

[<span data-ttu-id="14e2b-127">Remove-AzureAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="14e2b-127">Remove-AzureAutomationRunbook</span></span>](./Remove-AzureAutomationRunbook.md)

[<span data-ttu-id="14e2b-128">Set-AzureAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="14e2b-128">Set-AzureAutomationRunbook</span></span>](./Set-AzureAutomationRunbook.md)

[<span data-ttu-id="14e2b-129">Start-AzureAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="14e2b-129">Start-AzureAutomationRunbook</span></span>](./Start-AzureAutomationRunbook.md)


