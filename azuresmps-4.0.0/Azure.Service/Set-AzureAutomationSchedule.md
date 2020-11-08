---
external help file: Microsoft.Azure.Commands.Automation.dll-Help.xml
ms.assetid: E1141271-BA00-455C-AE80-DF5CD00348E6
online version: ''
schema: 2.0.0
ms.openlocfilehash: c0dff4cb86ca46826a1fc7355a9f2c241d8de405
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94099301"
---
# <span data-ttu-id="5bddf-101">Set-AzureAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="5bddf-101">Set-AzureAutomationSchedule</span></span>

## <span data-ttu-id="5bddf-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="5bddf-102">SYNOPSIS</span></span>

<span data-ttu-id="5bddf-103">Ändrar ett automations schema.</span><span class="sxs-lookup"><span data-stu-id="5bddf-103">Modifies an Automation schedule.</span></span>

## <span data-ttu-id="5bddf-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="5bddf-104">SYNTAX</span></span>

```
Set-AzureAutomationSchedule -Name <String> [-IsEnabled <Boolean>] [-Description <String>]
 -AutomationAccountName <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="5bddf-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="5bddf-105">DESCRIPTION</span></span>

[!INCLUDE [aa-deprecation](../include/aa-deprecation.md)]

<span data-ttu-id="5bddf-106">Cmdleten **set-AzureAutomationSchedule** ändrar ett schema i Microsoft Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="5bddf-106">The **Set-AzureAutomationSchedule** cmdlet modifies a schedule in Microsoft Azure Automation.</span></span>

## <span data-ttu-id="5bddf-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="5bddf-107">EXAMPLES</span></span>

### <span data-ttu-id="5bddf-108">Exempel 1: ändra ett schema</span><span class="sxs-lookup"><span data-stu-id="5bddf-108">Example 1: Modify a schedule</span></span>
```
PS C:\> Set-AzureAutomationSchedule -AutomationAccountName "Contoso17" -Name "Schedule01" -Description "Automation Schedule"
```

<span data-ttu-id="5bddf-109">Det här kommandot ändrar beskrivningen av schemat som heter Schedule01.</span><span class="sxs-lookup"><span data-stu-id="5bddf-109">This command modifies the description of the schedule named Schedule01.</span></span>

## <span data-ttu-id="5bddf-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="5bddf-110">PARAMETERS</span></span>

### <span data-ttu-id="5bddf-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="5bddf-111">-AutomationAccountName</span></span>
<span data-ttu-id="5bddf-112">Anger namnet på ett Automation-konto.</span><span class="sxs-lookup"><span data-stu-id="5bddf-112">Specifies the name of an Automation account.</span></span>

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

### <span data-ttu-id="5bddf-113">-Beskrivning</span><span class="sxs-lookup"><span data-stu-id="5bddf-113">-Description</span></span>
<span data-ttu-id="5bddf-114">Anger en beskrivning av schemat.</span><span class="sxs-lookup"><span data-stu-id="5bddf-114">Specifies a description for the schedule.</span></span>

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

### <span data-ttu-id="5bddf-115">-IsEnabled</span><span class="sxs-lookup"><span data-stu-id="5bddf-115">-IsEnabled</span></span>
<span data-ttu-id="5bddf-116">Anger om schemat är aktiverat.</span><span class="sxs-lookup"><span data-stu-id="5bddf-116">Indicates whether the schedule is enabled.</span></span>

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

### <span data-ttu-id="5bddf-117">-Namn</span><span class="sxs-lookup"><span data-stu-id="5bddf-117">-Name</span></span>
<span data-ttu-id="5bddf-118">Anger ett namn för schemat.</span><span class="sxs-lookup"><span data-stu-id="5bddf-118">Specifies a name for the schedule.</span></span>

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

### <span data-ttu-id="5bddf-119">-Profil</span><span class="sxs-lookup"><span data-stu-id="5bddf-119">-Profile</span></span>
<span data-ttu-id="5bddf-120">Anger den Azure-profil från vilken denna cmdlet läser.</span><span class="sxs-lookup"><span data-stu-id="5bddf-120">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="5bddf-121">Om du inte anger en profil läser denna cmdlet från den lokala standard profilen.</span><span class="sxs-lookup"><span data-stu-id="5bddf-121">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="5bddf-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5bddf-122">CommonParameters</span></span>
<span data-ttu-id="5bddf-123">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5bddf-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5bddf-124">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5bddf-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5bddf-125">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="5bddf-125">INPUTS</span></span>

## <span data-ttu-id="5bddf-126">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="5bddf-126">OUTPUTS</span></span>

### <span data-ttu-id="5bddf-127">Microsoft. Azure. commands. Automation. Model. Schedule</span><span class="sxs-lookup"><span data-stu-id="5bddf-127">Microsoft.Azure.Commands.Automation.Model.Schedule</span></span>

## <span data-ttu-id="5bddf-128">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="5bddf-128">NOTES</span></span>

## <span data-ttu-id="5bddf-129">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="5bddf-129">RELATED LINKS</span></span>

[<span data-ttu-id="5bddf-130">Get-AzureAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="5bddf-130">Get-AzureAutomationSchedule</span></span>](./Get-AzureAutomationSchedule.md)

[<span data-ttu-id="5bddf-131">New-AzureAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="5bddf-131">New-AzureAutomationSchedule</span></span>](./New-AzureAutomationSchedule.md)

[<span data-ttu-id="5bddf-132">Remove-AzureAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="5bddf-132">Remove-AzureAutomationSchedule</span></span>](./Remove-AzureAutomationSchedule.md)


