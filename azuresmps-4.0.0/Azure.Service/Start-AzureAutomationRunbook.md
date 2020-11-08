---
external help file: Microsoft.Azure.Commands.Automation.dll-Help.xml
ms.assetid: B0AE1969-71FD-4B6E-B0C0-1B744814BD5E
online version: ''
schema: 2.0.0
ms.openlocfilehash: 93dc73193c300f0f10fd9dccaff1c1f3954b8306
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94099262"
---
# <span data-ttu-id="c0694-101">Start-AzureAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="c0694-101">Start-AzureAutomationRunbook</span></span>

## <span data-ttu-id="c0694-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="c0694-102">SYNOPSIS</span></span>

<span data-ttu-id="c0694-103">Startar ett Runbook-jobb.</span><span class="sxs-lookup"><span data-stu-id="c0694-103">Starts a runbook job.</span></span>

## <span data-ttu-id="c0694-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="c0694-104">SYNTAX</span></span>

```
Start-AzureAutomationRunbook -Name <String> [-Parameters <IDictionary>] [-RunOn <String>]
 -AutomationAccountName <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="c0694-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="c0694-105">DESCRIPTION</span></span>

[!INCLUDE [aa-deprecation](../include/aa-deprecation.md)]

<span data-ttu-id="c0694-106">Cmdleten **Start-AzureAutomationRunbook** startar ett Microsoft Azure Automation-synkroniseringsjobb.</span><span class="sxs-lookup"><span data-stu-id="c0694-106">The **Start-AzureAutomationRunbook** cmdlet starts a Microsoft Azure Automation runbook job.</span></span>
<span data-ttu-id="c0694-107">Ange ID eller namnet på en Runbook.</span><span class="sxs-lookup"><span data-stu-id="c0694-107">Specify the ID or name of a runbook.</span></span>

## <span data-ttu-id="c0694-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="c0694-108">EXAMPLES</span></span>

### <span data-ttu-id="c0694-109">Exempel 1: starta ett Runbook-jobb</span><span class="sxs-lookup"><span data-stu-id="c0694-109">Example 1: Start a runbook job</span></span>
```
PS C:\> Start-AzureAutomationRunbook -AutomationAccountName "Contoso17" -Name "Runbk01"
```

<span data-ttu-id="c0694-110">Det här kommandot startar ett Runbook-jobb för Runbook med namnet Runbk01 i Automation-kontot med namnet Contoso17.</span><span class="sxs-lookup"><span data-stu-id="c0694-110">This command starts a runbook job for the runbook named Runbk01 in the Automation account named Contoso17.</span></span>

## <span data-ttu-id="c0694-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="c0694-111">PARAMETERS</span></span>

### <span data-ttu-id="c0694-112">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="c0694-112">-AutomationAccountName</span></span>
<span data-ttu-id="c0694-113">Anger namnet på ett Automation-konto.</span><span class="sxs-lookup"><span data-stu-id="c0694-113">Specifies the name of an Automation account.</span></span>

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

### <span data-ttu-id="c0694-114">-Namn</span><span class="sxs-lookup"><span data-stu-id="c0694-114">-Name</span></span>
<span data-ttu-id="c0694-115">Anger namnet på en Runbook.</span><span class="sxs-lookup"><span data-stu-id="c0694-115">Specifies the name of a runbook.</span></span>

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

### <span data-ttu-id="c0694-116">-Parametrar</span><span class="sxs-lookup"><span data-stu-id="c0694-116">-Parameters</span></span>
```yaml
Type: IDictionary
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c0694-117">-Profil</span><span class="sxs-lookup"><span data-stu-id="c0694-117">-Profile</span></span>
<span data-ttu-id="c0694-118">Anger den Azure-profil från vilken denna cmdlet läser.</span><span class="sxs-lookup"><span data-stu-id="c0694-118">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="c0694-119">Om du inte anger en profil läser denna cmdlet från den lokala standard profilen.</span><span class="sxs-lookup"><span data-stu-id="c0694-119">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="c0694-120">-RunOn</span><span class="sxs-lookup"><span data-stu-id="c0694-120">-RunOn</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: HybridWorker

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c0694-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c0694-121">CommonParameters</span></span>
<span data-ttu-id="c0694-122">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c0694-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c0694-123">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c0694-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c0694-124">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="c0694-124">INPUTS</span></span>

## <span data-ttu-id="c0694-125">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="c0694-125">OUTPUTS</span></span>

### <span data-ttu-id="c0694-126">Microsoft. Azure. commands. Automation. Model. job</span><span class="sxs-lookup"><span data-stu-id="c0694-126">Microsoft.Azure.Commands.Automation.Model.Job</span></span>

## <span data-ttu-id="c0694-127">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="c0694-127">NOTES</span></span>

## <span data-ttu-id="c0694-128">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="c0694-128">RELATED LINKS</span></span>

[<span data-ttu-id="c0694-129">Get-AzureAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="c0694-129">Get-AzureAutomationRunbook</span></span>](./Get-AzureAutomationRunbook.md)

[<span data-ttu-id="c0694-130">New-AzureAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="c0694-130">New-AzureAutomationRunbook</span></span>](./New-AzureAutomationRunbook.md)

[<span data-ttu-id="c0694-131">Publicera – AzureAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="c0694-131">Publish-AzureAutomationRunbook</span></span>](./Publish-AzureAutomationRunbook.md)

[<span data-ttu-id="c0694-132">Remove-AzureAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="c0694-132">Remove-AzureAutomationRunbook</span></span>](./Remove-AzureAutomationRunbook.md)

[<span data-ttu-id="c0694-133">Set-AzureAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="c0694-133">Set-AzureAutomationRunbook</span></span>](./Set-AzureAutomationRunbook.md)


