---
external help file: Microsoft.Azure.Commands.Automation.dll-Help.xml
ms.assetid: C24CFC83-3151-452D-A7B9-E78466493474
online version: ''
schema: 2.0.0
ms.openlocfilehash: e193dba6f64553e5e52d7f900bdc5c54deac5112
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94099302"
---
# <span data-ttu-id="b4155-101">Set-AzureAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="b4155-101">Set-AzureAutomationRunbook</span></span>

## <span data-ttu-id="b4155-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="b4155-102">SYNOPSIS</span></span>

<span data-ttu-id="b4155-103">Ändrar konfigurationen för en Runbook.</span><span class="sxs-lookup"><span data-stu-id="b4155-103">Modifies the configuration of a runbook.</span></span>

## <span data-ttu-id="b4155-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="b4155-104">SYNTAX</span></span>

```
Set-AzureAutomationRunbook -Name <String> [-Description <String>] [-Tags <String[]>] [-LogProgress <Boolean>]
 [-LogVerbose <Boolean>] -AutomationAccountName <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="b4155-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="b4155-105">DESCRIPTION</span></span>

[!INCLUDE [aa-deprecation](../include/aa-deprecation.md)]

<span data-ttu-id="b4155-106">Cmdleten **set-AzureAutomationRunbook** ändrar konfigurationen för en Microsoft Azure Automation-Runbook.</span><span class="sxs-lookup"><span data-stu-id="b4155-106">The **Set-AzureAutomationRunbook** cmdlet modifies the configuration of a Microsoft Azure Automation runbook.</span></span>

## <span data-ttu-id="b4155-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="b4155-107">EXAMPLES</span></span>

### <span data-ttu-id="b4155-108">Exempel 1: Aktivera utförlig loggning för en Runbook</span><span class="sxs-lookup"><span data-stu-id="b4155-108">Example 1: Enable verbose logging for a runbook</span></span>
```
PS C:\> Set-AzureAutomationRunbook -AutomationAccountName "Contoso17" -Name "MyRunbook" -LogVerbose $True
```

<span data-ttu-id="b4155-109">Det här kommandot aktiverar utförlig loggning för jobben för angiven Runbook i Automation-kontot med namnet Contoso17.</span><span class="sxs-lookup"><span data-stu-id="b4155-109">This command enables verbose logging for the jobs of the specified runbook in the Automation account named Contoso17.</span></span>

## <span data-ttu-id="b4155-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="b4155-110">PARAMETERS</span></span>

### <span data-ttu-id="b4155-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="b4155-111">-AutomationAccountName</span></span>
<span data-ttu-id="b4155-112">Anger namnet på ett Automation-konto.</span><span class="sxs-lookup"><span data-stu-id="b4155-112">Specifies the name of an Automation account.</span></span>

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

### <span data-ttu-id="b4155-113">-Beskrivning</span><span class="sxs-lookup"><span data-stu-id="b4155-113">-Description</span></span>
<span data-ttu-id="b4155-114">Anger en beskrivning av Runbook-flödet.</span><span class="sxs-lookup"><span data-stu-id="b4155-114">Specifies a description for the runbook.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b4155-115">-LogProgress</span><span class="sxs-lookup"><span data-stu-id="b4155-115">-LogProgress</span></span>
```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b4155-116">-LogVerbose</span><span class="sxs-lookup"><span data-stu-id="b4155-116">-LogVerbose</span></span>
<span data-ttu-id="b4155-117">Anger om utförlig loggning ska användas.</span><span class="sxs-lookup"><span data-stu-id="b4155-117">Indicates whether to use verbose logging.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b4155-118">-Namn</span><span class="sxs-lookup"><span data-stu-id="b4155-118">-Name</span></span>
<span data-ttu-id="b4155-119">Anger ett namn.</span><span class="sxs-lookup"><span data-stu-id="b4155-119">Specifies a name.</span></span>

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

### <span data-ttu-id="b4155-120">-Profil</span><span class="sxs-lookup"><span data-stu-id="b4155-120">-Profile</span></span>
<span data-ttu-id="b4155-121">Anger den Azure-profil från vilken denna cmdlet läser.</span><span class="sxs-lookup"><span data-stu-id="b4155-121">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="b4155-122">Om du inte anger en profil läser denna cmdlet från den lokala standard profilen.</span><span class="sxs-lookup"><span data-stu-id="b4155-122">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="b4155-123">-Taggar</span><span class="sxs-lookup"><span data-stu-id="b4155-123">-Tags</span></span>
<span data-ttu-id="b4155-124">Anger en matris med taggar.</span><span class="sxs-lookup"><span data-stu-id="b4155-124">Specifies an array of tags.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b4155-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b4155-125">CommonParameters</span></span>
<span data-ttu-id="b4155-126">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b4155-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b4155-127">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b4155-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b4155-128">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="b4155-128">INPUTS</span></span>

## <span data-ttu-id="b4155-129">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="b4155-129">OUTPUTS</span></span>

### <span data-ttu-id="b4155-130">Microsoft. Azure. commands. Automation. Model. Runbook</span><span class="sxs-lookup"><span data-stu-id="b4155-130">Microsoft.Azure.Commands.Automation.Model.Runbook</span></span>

## <span data-ttu-id="b4155-131">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="b4155-131">NOTES</span></span>

## <span data-ttu-id="b4155-132">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="b4155-132">RELATED LINKS</span></span>

[<span data-ttu-id="b4155-133">Get-AzureAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="b4155-133">Get-AzureAutomationRunbook</span></span>](./Get-AzureAutomationRunbook.md)

[<span data-ttu-id="b4155-134">New-AzureAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="b4155-134">New-AzureAutomationRunbook</span></span>](./New-AzureAutomationRunbook.md)

[<span data-ttu-id="b4155-135">Publicera – AzureAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="b4155-135">Publish-AzureAutomationRunbook</span></span>](./Publish-AzureAutomationRunbook.md)

[<span data-ttu-id="b4155-136">Remove-AzureAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="b4155-136">Remove-AzureAutomationRunbook</span></span>](./Remove-AzureAutomationRunbook.md)

[<span data-ttu-id="b4155-137">Start-AzureAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="b4155-137">Start-AzureAutomationRunbook</span></span>](./Start-AzureAutomationRunbook.md)


