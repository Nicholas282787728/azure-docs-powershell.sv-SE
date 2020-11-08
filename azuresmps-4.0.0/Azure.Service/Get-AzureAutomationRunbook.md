---
external help file: Microsoft.Azure.Commands.Automation.dll-Help.xml
ms.assetid: 304F71E0-9E89-46E6-BD25-7584601CC845
online version: ''
schema: 2.0.0
ms.openlocfilehash: e507b1b35bf8739c80bbdf92f02f29099ceb3284
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94093383"
---
# <span data-ttu-id="4208d-101">Get-AzureAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="4208d-101">Get-AzureAutomationRunbook</span></span>

## <span data-ttu-id="4208d-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="4208d-102">SYNOPSIS</span></span>

<span data-ttu-id="4208d-103">Hämtar en Runbook.</span><span class="sxs-lookup"><span data-stu-id="4208d-103">Gets a runbook.</span></span>

## <span data-ttu-id="4208d-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="4208d-104">SYNTAX</span></span>

### <span data-ttu-id="4208d-105">ByAll (standard)</span><span class="sxs-lookup"><span data-stu-id="4208d-105">ByAll (Default)</span></span>
```
Get-AzureAutomationRunbook -AutomationAccountName <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="4208d-106">ByRunbookName</span><span class="sxs-lookup"><span data-stu-id="4208d-106">ByRunbookName</span></span>
```
Get-AzureAutomationRunbook -Name <String> -AutomationAccountName <String> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="4208d-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="4208d-107">DESCRIPTION</span></span>

[!INCLUDE [aa-deprecation](../include/aa-deprecation.md)]

<span data-ttu-id="4208d-108">Cmdleten **Get-AzureAutomationRunbook** hämtar en eller flera Microsoft Azure Automation-runbooks.</span><span class="sxs-lookup"><span data-stu-id="4208d-108">The **Get-AzureAutomationRunbook** cmdlet gets one or more Microsoft Azure Automation runbooks.</span></span>
<span data-ttu-id="4208d-109">Alla Runbooks returneras som standard.</span><span class="sxs-lookup"><span data-stu-id="4208d-109">By default, all runbooks are returned.</span></span>
<span data-ttu-id="4208d-110">Om du vill hämta en specifik Runbook anger du dess namn eller ID.</span><span class="sxs-lookup"><span data-stu-id="4208d-110">To get a specific runbook, specify its name or ID.</span></span>
<span data-ttu-id="4208d-111">Om du vill hämta alla Runbooks som är kopplade till ett visst schema anger du schema namnet.</span><span class="sxs-lookup"><span data-stu-id="4208d-111">To get all runbooks linked to a specific schedule, specify the schedule name.</span></span>

## <span data-ttu-id="4208d-112">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="4208d-112">EXAMPLES</span></span>

### <span data-ttu-id="4208d-113">Exempel 1: Hämta alla Runbooks</span><span class="sxs-lookup"><span data-stu-id="4208d-113">Example 1: Get all runbooks</span></span>
```
PS C:\> Get-AzureAutomationRunbook -AutomationAccountName "Contoso17"
```

<span data-ttu-id="4208d-114">Det här kommandot får alla Runbooks i Azure Automation-kontot som heter Contoso17.</span><span class="sxs-lookup"><span data-stu-id="4208d-114">This command gets all runbooks in the Azure Automation account named Contoso17.</span></span>

## <span data-ttu-id="4208d-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="4208d-115">PARAMETERS</span></span>

### <span data-ttu-id="4208d-116">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="4208d-116">-AutomationAccountName</span></span>
<span data-ttu-id="4208d-117">Anger namnet på ett Azure Automation-konto.</span><span class="sxs-lookup"><span data-stu-id="4208d-117">Specifies the name of an Azure Automation account.</span></span>

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

### <span data-ttu-id="4208d-118">-Namn</span><span class="sxs-lookup"><span data-stu-id="4208d-118">-Name</span></span>
<span data-ttu-id="4208d-119">Anger namnet på en Runbook.</span><span class="sxs-lookup"><span data-stu-id="4208d-119">Specifies the name of a runbook.</span></span>

```yaml
Type: String
Parameter Sets: ByRunbookName
Aliases: RunbookName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4208d-120">-Profil</span><span class="sxs-lookup"><span data-stu-id="4208d-120">-Profile</span></span>
<span data-ttu-id="4208d-121">Anger den Azure-profil från vilken denna cmdlet läser.</span><span class="sxs-lookup"><span data-stu-id="4208d-121">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="4208d-122">Om du inte anger en profil läser denna cmdlet från den lokala standard profilen.</span><span class="sxs-lookup"><span data-stu-id="4208d-122">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="4208d-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4208d-123">CommonParameters</span></span>
<span data-ttu-id="4208d-124">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4208d-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4208d-125">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4208d-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4208d-126">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="4208d-126">INPUTS</span></span>

## <span data-ttu-id="4208d-127">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="4208d-127">OUTPUTS</span></span>

### <span data-ttu-id="4208d-128">Microsoft. Azure. commands. Automation. Model. Runbook</span><span class="sxs-lookup"><span data-stu-id="4208d-128">Microsoft.Azure.Commands.Automation.Model.Runbook</span></span>

## <span data-ttu-id="4208d-129">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="4208d-129">NOTES</span></span>

## <span data-ttu-id="4208d-130">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="4208d-130">RELATED LINKS</span></span>

[<span data-ttu-id="4208d-131">New-AzureAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="4208d-131">New-AzureAutomationRunbook</span></span>](./New-AzureAutomationRunbook.md)

[<span data-ttu-id="4208d-132">Publicera – AzureAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="4208d-132">Publish-AzureAutomationRunbook</span></span>](./Publish-AzureAutomationRunbook.md)

[<span data-ttu-id="4208d-133">Remove-AzureAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="4208d-133">Remove-AzureAutomationRunbook</span></span>](./Remove-AzureAutomationRunbook.md)

[<span data-ttu-id="4208d-134">Set-AzureAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="4208d-134">Set-AzureAutomationRunbook</span></span>](./Set-AzureAutomationRunbook.md)

[<span data-ttu-id="4208d-135">Start-AzureAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="4208d-135">Start-AzureAutomationRunbook</span></span>](./Start-AzureAutomationRunbook.md)


