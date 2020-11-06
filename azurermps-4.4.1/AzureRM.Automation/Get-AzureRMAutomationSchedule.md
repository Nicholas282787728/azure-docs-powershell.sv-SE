---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: 2908890B-7A46-41B7-931F-AE94638D1EDF
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRMAutomationSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRMAutomationSchedule.md
ms.openlocfilehash: 1252864be8e55638ec5e982bd075aec647b68a18
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93586260"
---
# <span data-ttu-id="458ca-101">Get-AzureRmAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="458ca-101">Get-AzureRmAutomationSchedule</span></span>

## <span data-ttu-id="458ca-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="458ca-102">SYNOPSIS</span></span>
<span data-ttu-id="458ca-103">Får ett Automation-schema.</span><span class="sxs-lookup"><span data-stu-id="458ca-103">Gets an Automation schedule.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="458ca-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="458ca-104">SYNTAX</span></span>

### <span data-ttu-id="458ca-105">ByAll (standard)</span><span class="sxs-lookup"><span data-stu-id="458ca-105">ByAll (Default)</span></span>
```
Get-AzureRmAutomationSchedule [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="458ca-106">ByName</span><span class="sxs-lookup"><span data-stu-id="458ca-106">ByName</span></span>
```
Get-AzureRmAutomationSchedule [-Name] <String> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="458ca-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="458ca-107">DESCRIPTION</span></span>
<span data-ttu-id="458ca-108">Cmdleten **Get-AzureRmAutomationSchedule** får ett Azure Automation-schema.</span><span class="sxs-lookup"><span data-stu-id="458ca-108">The **Get-AzureRmAutomationSchedule** cmdlet gets an Azure Automation schedule.</span></span>

## <span data-ttu-id="458ca-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="458ca-109">EXAMPLES</span></span>

### <span data-ttu-id="458ca-110">Exempel 1: få ett schema</span><span class="sxs-lookup"><span data-stu-id="458ca-110">Example 1: Get a schedule</span></span>
```
PS C:\>Get-AzureRmAutomationSchedule -AutomationAccountName "Contoso17" -Name "DailySchedule08" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="458ca-111">Det här kommandot får schemat med namnet DailySchedule08.</span><span class="sxs-lookup"><span data-stu-id="458ca-111">This command gets the schedule named DailySchedule08.</span></span>

## <span data-ttu-id="458ca-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="458ca-112">PARAMETERS</span></span>

### <span data-ttu-id="458ca-113">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="458ca-113">-AutomationAccountName</span></span>
<span data-ttu-id="458ca-114">Anger namnet på ett Automation-konto som denna cmdlet får ett schema för.</span><span class="sxs-lookup"><span data-stu-id="458ca-114">Specifies the name of an Automation account for which this cmdlet get a schedule.</span></span>

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

### <span data-ttu-id="458ca-115">-Namn</span><span class="sxs-lookup"><span data-stu-id="458ca-115">-Name</span></span>
<span data-ttu-id="458ca-116">Anger namnet på ett schema som den här cmdleten får.</span><span class="sxs-lookup"><span data-stu-id="458ca-116">Specifies the name of a schedule that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases: ScheduleName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="458ca-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="458ca-117">-ResourceGroupName</span></span>
<span data-ttu-id="458ca-118">Anger namnet på en resurs grupp för vilken denna cmdlet får ett schema.</span><span class="sxs-lookup"><span data-stu-id="458ca-118">Specifies the name of a resource group for which this cmdlet gets a schedule.</span></span>

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

### <span data-ttu-id="458ca-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="458ca-119">-DefaultProfile</span></span>
<span data-ttu-id="458ca-120">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="458ca-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="458ca-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="458ca-121">CommonParameters</span></span>
<span data-ttu-id="458ca-122">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="458ca-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="458ca-123">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="458ca-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="458ca-124">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="458ca-124">INPUTS</span></span>

## <span data-ttu-id="458ca-125">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="458ca-125">OUTPUTS</span></span>

### <span data-ttu-id="458ca-126">Microsoft. Azure. commands. Automation. Model. Schedule</span><span class="sxs-lookup"><span data-stu-id="458ca-126">Microsoft.Azure.Commands.Automation.Model.Schedule</span></span>

## <span data-ttu-id="458ca-127">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="458ca-127">NOTES</span></span>

## <span data-ttu-id="458ca-128">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="458ca-128">RELATED LINKS</span></span>

[<span data-ttu-id="458ca-129">New-AzureRmAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="458ca-129">New-AzureRmAutomationSchedule</span></span>](./New-AzureRMAutomationSchedule.md)

[<span data-ttu-id="458ca-130">Remove-AzureRmAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="458ca-130">Remove-AzureRmAutomationSchedule</span></span>](./Remove-AzureRMAutomationSchedule.md)

[<span data-ttu-id="458ca-131">Set-AzureRmAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="458ca-131">Set-AzureRmAutomationSchedule</span></span>](./Set-AzureRMAutomationSchedule.md)


