---
external help file: Microsoft.Azure.Commands.Automation.dll-Help.xml
ms.assetid: 436A6D6E-2280-475C-A1F5-6A6D72DAD9E7
online version: ''
schema: 2.0.0
ms.openlocfilehash: 4895c9aa12ad56b8e3ddffb88a19439777d5b54a
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94093381"
---
# <span data-ttu-id="ee1c8-101">Get-AzureAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="ee1c8-101">Get-AzureAutomationSchedule</span></span>

## <span data-ttu-id="ee1c8-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="ee1c8-102">SYNOPSIS</span></span>

<span data-ttu-id="ee1c8-103">Får ett Azure Automation-schema.</span><span class="sxs-lookup"><span data-stu-id="ee1c8-103">Gets an Azure Automation schedule.</span></span>

## <span data-ttu-id="ee1c8-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="ee1c8-104">SYNTAX</span></span>

### <span data-ttu-id="ee1c8-105">ByAll (standard)</span><span class="sxs-lookup"><span data-stu-id="ee1c8-105">ByAll (Default)</span></span>
```
Get-AzureAutomationSchedule -AutomationAccountName <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="ee1c8-106">ByName</span><span class="sxs-lookup"><span data-stu-id="ee1c8-106">ByName</span></span>
```
Get-AzureAutomationSchedule -Name <String> -AutomationAccountName <String> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="ee1c8-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="ee1c8-107">DESCRIPTION</span></span>

[!INCLUDE [aa-deprecation](../include/aa-deprecation.md)]

<span data-ttu-id="ee1c8-108">Cmdleten **Get-AzureAutomationSchedule** får ett Microsoft Azure Automation-schema.</span><span class="sxs-lookup"><span data-stu-id="ee1c8-108">The **Get-AzureAutomationSchedule** cmdlet gets a Microsoft Azure Automation schedule.</span></span>

## <span data-ttu-id="ee1c8-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="ee1c8-109">EXAMPLES</span></span>

### <span data-ttu-id="ee1c8-110">Exempel 1: få ett schema</span><span class="sxs-lookup"><span data-stu-id="ee1c8-110">Example 1: Get a schedule</span></span>
```
PS C:\> Get-AzureAutomationSchedule -AutomationAccountName "Contoso17" -Name "DailySchedule08"
```

<span data-ttu-id="ee1c8-111">Det här kommandot får schemat med namnet DailySchedule08.</span><span class="sxs-lookup"><span data-stu-id="ee1c8-111">This command gets the schedule named DailySchedule08.</span></span>

## <span data-ttu-id="ee1c8-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="ee1c8-112">PARAMETERS</span></span>

### <span data-ttu-id="ee1c8-113">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="ee1c8-113">-AutomationAccountName</span></span>
<span data-ttu-id="ee1c8-114">Anger namnet på ett Azure Automation-konto.</span><span class="sxs-lookup"><span data-stu-id="ee1c8-114">Specifies the name of an Azure Automation account.</span></span>

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

### <span data-ttu-id="ee1c8-115">-Namn</span><span class="sxs-lookup"><span data-stu-id="ee1c8-115">-Name</span></span>
<span data-ttu-id="ee1c8-116">Anger namnet på ett schema.</span><span class="sxs-lookup"><span data-stu-id="ee1c8-116">Specifies the name of a schedule.</span></span>

```yaml
Type: String
Parameter Sets: ByName
Aliases: ScheduleName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ee1c8-117">-Profil</span><span class="sxs-lookup"><span data-stu-id="ee1c8-117">-Profile</span></span>
<span data-ttu-id="ee1c8-118">Anger den Azure-profil från vilken denna cmdlet läser.</span><span class="sxs-lookup"><span data-stu-id="ee1c8-118">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="ee1c8-119">Om du inte anger en profil läser denna cmdlet från den lokala standard profilen.</span><span class="sxs-lookup"><span data-stu-id="ee1c8-119">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="ee1c8-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ee1c8-120">CommonParameters</span></span>
<span data-ttu-id="ee1c8-121">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ee1c8-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ee1c8-122">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ee1c8-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ee1c8-123">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="ee1c8-123">INPUTS</span></span>

## <span data-ttu-id="ee1c8-124">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="ee1c8-124">OUTPUTS</span></span>

### <span data-ttu-id="ee1c8-125">Microsoft. Azure. commands. Automation. Model. Schedule</span><span class="sxs-lookup"><span data-stu-id="ee1c8-125">Microsoft.Azure.Commands.Automation.Model.Schedule</span></span>

## <span data-ttu-id="ee1c8-126">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="ee1c8-126">NOTES</span></span>

## <span data-ttu-id="ee1c8-127">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="ee1c8-127">RELATED LINKS</span></span>

[<span data-ttu-id="ee1c8-128">New-AzureAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="ee1c8-128">New-AzureAutomationSchedule</span></span>](./New-AzureAutomationSchedule.md)

[<span data-ttu-id="ee1c8-129">Remove-AzureAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="ee1c8-129">Remove-AzureAutomationSchedule</span></span>](./Remove-AzureAutomationSchedule.md)

[<span data-ttu-id="ee1c8-130">Set-AzureAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="ee1c8-130">Set-AzureAutomationSchedule</span></span>](./Set-AzureAutomationSchedule.md)


