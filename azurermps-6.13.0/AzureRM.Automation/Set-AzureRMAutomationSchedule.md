---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: 6429C564-1995-4D9B-BF9B-963B4F5FB3BD
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/set-azurermautomationschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Set-AzureRMAutomationSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Set-AzureRMAutomationSchedule.md
ms.openlocfilehash: 76cc8117458db23f947a998d29de09a900bb6d42
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93755721"
---
# <span data-ttu-id="ed71d-101">Set-AzureRmAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="ed71d-101">Set-AzureRmAutomationSchedule</span></span>

## <span data-ttu-id="ed71d-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="ed71d-102">SYNOPSIS</span></span>
<span data-ttu-id="ed71d-103">Ändrar ett automations schema.</span><span class="sxs-lookup"><span data-stu-id="ed71d-103">Modifies an Automation schedule.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ed71d-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="ed71d-104">SYNTAX</span></span>

```
Set-AzureRmAutomationSchedule [-Name] <String> [-IsEnabled <Boolean>] [-Description <String>]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="ed71d-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="ed71d-105">DESCRIPTION</span></span>
<span data-ttu-id="ed71d-106">Cmdleten **set-AzureRmAutomationSchedule** ändrar ett schema i Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="ed71d-106">The **Set-AzureRmAutomationSchedule** cmdlet modifies a schedule in Azure Automation.</span></span>

## <span data-ttu-id="ed71d-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="ed71d-107">EXAMPLES</span></span>

### <span data-ttu-id="ed71d-108">Exempel 1: ändra ett schema</span><span class="sxs-lookup"><span data-stu-id="ed71d-108">Example 1: Modify a schedule</span></span>
```
PS C:\>Set-AzureRmAutomationSchedule -AutomationAccountName "Contoso17" -Name "Schedule01" -Description "Automation Schedule" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="ed71d-109">Det här kommandot ändrar beskrivningen av schemat som heter Schedule01.</span><span class="sxs-lookup"><span data-stu-id="ed71d-109">This command modifies the description of the schedule named Schedule01.</span></span>

## <span data-ttu-id="ed71d-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="ed71d-110">PARAMETERS</span></span>

### <span data-ttu-id="ed71d-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="ed71d-111">-AutomationAccountName</span></span>
<span data-ttu-id="ed71d-112">Anger namnet på ett Automation-konto som denna cmdlet ändrar ett schema för.</span><span class="sxs-lookup"><span data-stu-id="ed71d-112">Specifies the name of an Automation account for which this cmdlet modifies a schedule.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ed71d-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ed71d-113">-DefaultProfile</span></span>
<span data-ttu-id="ed71d-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="ed71d-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ed71d-115">-Beskrivning</span><span class="sxs-lookup"><span data-stu-id="ed71d-115">-Description</span></span>
<span data-ttu-id="ed71d-116">Anger en beskrivning av schemat.</span><span class="sxs-lookup"><span data-stu-id="ed71d-116">Specifies a description for the schedule.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ed71d-117">-IsEnabled</span><span class="sxs-lookup"><span data-stu-id="ed71d-117">-IsEnabled</span></span>
<span data-ttu-id="ed71d-118">Anger om denna cmdlet aktiverar schemat.</span><span class="sxs-lookup"><span data-stu-id="ed71d-118">Specifies whether this cmdlet enables the schedule.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ed71d-119">-Namn</span><span class="sxs-lookup"><span data-stu-id="ed71d-119">-Name</span></span>
<span data-ttu-id="ed71d-120">Anger namnet på det schema som den här cmdleten ändrar.</span><span class="sxs-lookup"><span data-stu-id="ed71d-120">Specifies the name for the schedule that this cmdlet modifies.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ed71d-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ed71d-121">-ResourceGroupName</span></span>
<span data-ttu-id="ed71d-122">Anger namnet på en resurs grupp för vilken denna cmdlet ändrar ett schema.</span><span class="sxs-lookup"><span data-stu-id="ed71d-122">Specifies the name of a resource group for which this cmdlet modifies a schedule.</span></span>

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

### <span data-ttu-id="ed71d-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ed71d-123">CommonParameters</span></span>
<span data-ttu-id="ed71d-124">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ed71d-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ed71d-125">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ed71d-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ed71d-126">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="ed71d-126">INPUTS</span></span>

### <span data-ttu-id="ed71d-127">System. String</span><span class="sxs-lookup"><span data-stu-id="ed71d-127">System.String</span></span>

### <span data-ttu-id="ed71d-128">System. Nullable ' 1 [[system. Boolean, mscorlib, version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="ed71d-128">System.Nullable\`1[[System.Boolean, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="ed71d-129">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="ed71d-129">OUTPUTS</span></span>

### <span data-ttu-id="ed71d-130">Microsoft. Azure. commands. Automation. Model. Schedule</span><span class="sxs-lookup"><span data-stu-id="ed71d-130">Microsoft.Azure.Commands.Automation.Model.Schedule</span></span>

## <span data-ttu-id="ed71d-131">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="ed71d-131">NOTES</span></span>

## <span data-ttu-id="ed71d-132">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="ed71d-132">RELATED LINKS</span></span>

[<span data-ttu-id="ed71d-133">Get-AzureRmAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="ed71d-133">Get-AzureRmAutomationSchedule</span></span>](./Get-AzureRMAutomationSchedule.md)

[<span data-ttu-id="ed71d-134">New-AzureRmAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="ed71d-134">New-AzureRmAutomationSchedule</span></span>](./New-AzureRMAutomationSchedule.md)

[<span data-ttu-id="ed71d-135">Remove-AzureRmAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="ed71d-135">Remove-AzureRmAutomationSchedule</span></span>](./Remove-AzureRMAutomationSchedule.md)


