---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: 2908890B-7A46-41B7-931F-AE94638D1EDF
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/get-azurermautomationschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRMAutomationSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRMAutomationSchedule.md
ms.openlocfilehash: 2b35281cd276be9149f2d4c4e17cb38f48eadc25
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93583699"
---
# <span data-ttu-id="aa5d9-101">Get-AzureRmAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="aa5d9-101">Get-AzureRmAutomationSchedule</span></span>

## <span data-ttu-id="aa5d9-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="aa5d9-102">SYNOPSIS</span></span>
<span data-ttu-id="aa5d9-103">Får ett Automation-schema.</span><span class="sxs-lookup"><span data-stu-id="aa5d9-103">Gets an Automation schedule.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="aa5d9-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="aa5d9-104">SYNTAX</span></span>

### <span data-ttu-id="aa5d9-105">ByAll (standard)</span><span class="sxs-lookup"><span data-stu-id="aa5d9-105">ByAll (Default)</span></span>
```
Get-AzureRmAutomationSchedule [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="aa5d9-106">ByName</span><span class="sxs-lookup"><span data-stu-id="aa5d9-106">ByName</span></span>
```
Get-AzureRmAutomationSchedule [-Name] <String> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="aa5d9-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="aa5d9-107">DESCRIPTION</span></span>
<span data-ttu-id="aa5d9-108">Cmdleten **Get-AzureRmAutomationSchedule** får ett Azure Automation-schema.</span><span class="sxs-lookup"><span data-stu-id="aa5d9-108">The **Get-AzureRmAutomationSchedule** cmdlet gets an Azure Automation schedule.</span></span>

## <span data-ttu-id="aa5d9-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="aa5d9-109">EXAMPLES</span></span>

### <span data-ttu-id="aa5d9-110">Exempel 1: få ett schema</span><span class="sxs-lookup"><span data-stu-id="aa5d9-110">Example 1: Get a schedule</span></span>
```
PS C:\>Get-AzureRmAutomationSchedule -AutomationAccountName "Contoso17" -Name "DailySchedule08" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="aa5d9-111">Det här kommandot får schemat med namnet DailySchedule08.</span><span class="sxs-lookup"><span data-stu-id="aa5d9-111">This command gets the schedule named DailySchedule08.</span></span>

## <span data-ttu-id="aa5d9-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="aa5d9-112">PARAMETERS</span></span>

### <span data-ttu-id="aa5d9-113">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="aa5d9-113">-AutomationAccountName</span></span>
<span data-ttu-id="aa5d9-114">Anger namnet på ett Automation-konto som denna cmdlet får ett schema för.</span><span class="sxs-lookup"><span data-stu-id="aa5d9-114">Specifies the name of an Automation account for which this cmdlet get a schedule.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="aa5d9-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aa5d9-115">-DefaultProfile</span></span>
<span data-ttu-id="aa5d9-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="aa5d9-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aa5d9-117">-Namn</span><span class="sxs-lookup"><span data-stu-id="aa5d9-117">-Name</span></span>
<span data-ttu-id="aa5d9-118">Anger namnet på ett schema som den här cmdleten får.</span><span class="sxs-lookup"><span data-stu-id="aa5d9-118">Specifies the name of a schedule that this cmdlet gets.</span></span>

```yaml
Type: String
Parameter Sets: ByName
Aliases: ScheduleName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="aa5d9-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="aa5d9-119">-ResourceGroupName</span></span>
<span data-ttu-id="aa5d9-120">Anger namnet på en resurs grupp för vilken denna cmdlet får ett schema.</span><span class="sxs-lookup"><span data-stu-id="aa5d9-120">Specifies the name of a resource group for which this cmdlet gets a schedule.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="aa5d9-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aa5d9-121">CommonParameters</span></span>
<span data-ttu-id="aa5d9-122">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="aa5d9-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aa5d9-123">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="aa5d9-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aa5d9-124">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="aa5d9-124">INPUTS</span></span>

### <span data-ttu-id="aa5d9-125">Ingen</span><span class="sxs-lookup"><span data-stu-id="aa5d9-125">None</span></span>
<span data-ttu-id="aa5d9-126">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="aa5d9-126">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="aa5d9-127">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="aa5d9-127">OUTPUTS</span></span>

### <span data-ttu-id="aa5d9-128">Microsoft. Azure. commands. Automation. Model. Schedule</span><span class="sxs-lookup"><span data-stu-id="aa5d9-128">Microsoft.Azure.Commands.Automation.Model.Schedule</span></span>

## <span data-ttu-id="aa5d9-129">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="aa5d9-129">NOTES</span></span>

## <span data-ttu-id="aa5d9-130">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="aa5d9-130">RELATED LINKS</span></span>

[<span data-ttu-id="aa5d9-131">New-AzureRmAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="aa5d9-131">New-AzureRmAutomationSchedule</span></span>](./New-AzureRMAutomationSchedule.md)

[<span data-ttu-id="aa5d9-132">Remove-AzureRmAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="aa5d9-132">Remove-AzureRmAutomationSchedule</span></span>](./Remove-AzureRMAutomationSchedule.md)

[<span data-ttu-id="aa5d9-133">Set-AzureRmAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="aa5d9-133">Set-AzureRmAutomationSchedule</span></span>](./Set-AzureRMAutomationSchedule.md)


