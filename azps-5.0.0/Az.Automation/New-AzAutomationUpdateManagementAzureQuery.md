---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/new-azautomationupdatemanagementazurequery
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/New-AzAutomationUpdateManagementAzureQuery.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/New-AzAutomationUpdateManagementAzureQuery.md
ms.openlocfilehash: 68139ff184df62583b3077a38fbc2e26fd5eae09
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94321855"
---
# <span data-ttu-id="b3e96-101">New-AzAutomationUpdateManagementAzureQuery</span><span class="sxs-lookup"><span data-stu-id="b3e96-101">New-AzAutomationUpdateManagementAzureQuery</span></span>

## <span data-ttu-id="b3e96-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="b3e96-102">SYNOPSIS</span></span>
<span data-ttu-id="b3e96-103">Skapar Azure Automation-konfiguration av ett Azure Query-objekt.</span><span class="sxs-lookup"><span data-stu-id="b3e96-103">Creates azure automation software update configuration azure query object.</span></span>

## <span data-ttu-id="b3e96-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="b3e96-104">SYNTAX</span></span>

```
New-AzAutomationUpdateManagementAzureQuery -Scope <String[]> [-Location <String[]>] [-Tag <Hashtable>]
 [-FilterOperator <TagOperators>] [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b3e96-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="b3e96-105">DESCRIPTION</span></span>
<span data-ttu-id="b3e96-106">Skapar en konfiguration för Azure-frågor med program uppdatering som används för att skapa en konfiguration för program uppdatering som körs enligt ett schema för att uppdatera en lista över dynamiskt löst lista med virtuella Azure-datorer.</span><span class="sxs-lookup"><span data-stu-id="b3e96-106">Creates a software update configuration azure queries object that will be used to create a software update configuration which will runs on a schedule to update a list of dynamically resolved list of azure virtual machines.</span></span>

## <span data-ttu-id="b3e96-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="b3e96-107">EXAMPLES</span></span>

### <span data-ttu-id="b3e96-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="b3e96-108">Example 1</span></span>
```powershell
PS C:\>$query1Scope = @(        
"/subscriptions/22e2445a-0984-4fa5-86a4-0280d76c4b2c/resourceGroups/resourceGroupName",
"/subscriptions/32e2445a-0984-4fa5-86a4-0280d76c4b2d/"
    )
PS C:\>$query1Location =@("Japan East", "UK South")
PS C:\>$query1FilterOperator = "All"
PS C:\>$tag1 = @{"tag1"= @("tag1Value1", "tag1Value2")}
PS C:\>$tag1.add("tag2", "tag2Value")
PS C:\>$azq = New-AzAutomationUpdateManagementAzureQuery -ResourceGroupName "mygroup" `
                                       -AutomationAccountName "myaccount" `
                                       -Scope $query1Scope `
                                       -Location $query1Location `
                                       -Tag $tag1
PS C:\>$AzureQueries = @($azq)
PS C:\> $startTime = [DateTimeOffset]"2018-09-13T21:00"

PS C:\> $duration = New-TimeSpan -Hours 2
PS C:\> $schedule = New-AzAutomationSchedule -ResourceGroupName "mygroup" `
                                                  -AutomationAccountName "myaccount" `
                                                  -Name MyWeeklySchedule `
                                                  -StartTime $startTime `
                                                  -DaysOfWeek Saturday `
                                                  -WeekInterval 1 `
                                                  -ForUpdateConfiguration

New-AzAutomationSoftwareUpdateConfiguration -ResourceGroupName "mygroup" `
                                                 -AutomationAccountName "myaccount" `
                                                 -Schedule $schedule `
                                                 -Windows `                                                 
                                                 -AzureQuery $AzureQueries `
                                                 -IncludedUpdateClassification Critical `
                                                 -Duration $duration

UpdateConfiguration   : Microsoft.Azure.Commands.Automation.Model.UpdateManagement.UpdateConfiguration
ScheduleConfiguration : Microsoft.Azure.Commands.Automation.Model.Schedule
ProvisioningState     : Provisioning
ErrorInfo             :
ResourceGroupName     : mygroup
AutomationAccountName : myaccount
Name                  : MyWeeklySchedule
CreationTime          : 9/14/2018 3:53:27 AM +00:00
LastModifiedTime      : 9/14/2018 3:53:27 AM +00:00
Description           :

```

## <span data-ttu-id="b3e96-109">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="b3e96-109">PARAMETERS</span></span>

### <span data-ttu-id="b3e96-110">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="b3e96-110">-AutomationAccountName</span></span>
<span data-ttu-id="b3e96-111">Namnet på Automation-kontot.</span><span class="sxs-lookup"><span data-stu-id="b3e96-111">The automation account name.</span></span>

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

### <span data-ttu-id="b3e96-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b3e96-112">-DefaultProfile</span></span>
<span data-ttu-id="b3e96-113">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="b3e96-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b3e96-114">-FilterOperator</span><span class="sxs-lookup"><span data-stu-id="b3e96-114">-FilterOperator</span></span>
<span data-ttu-id="b3e96-115">Tagg filter operator.</span><span class="sxs-lookup"><span data-stu-id="b3e96-115">Tag filter operator.</span></span>

```yaml
Type: TagOperators
Parameter Sets: (All)
Aliases:
Accepted values: All, Any

Required: False
Position: Named
Default value: None
Accept wildcard characters: False
```

### <span data-ttu-id="b3e96-116">-Plats</span><span class="sxs-lookup"><span data-stu-id="b3e96-116">-Location</span></span>
<span data-ttu-id="b3e96-117">Lista över platser för virtuella Azure-datorer.</span><span class="sxs-lookup"><span data-stu-id="b3e96-117">List of locations for azure virtual machines.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept wildcard characters: False
```

### <span data-ttu-id="b3e96-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b3e96-118">-ResourceGroupName</span></span>
<span data-ttu-id="b3e96-119">Resurs gruppens namn.</span><span class="sxs-lookup"><span data-stu-id="b3e96-119">The resource group name.</span></span>

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

### <span data-ttu-id="b3e96-120">-Omfattning</span><span class="sxs-lookup"><span data-stu-id="b3e96-120">-Scope</span></span>
<span data-ttu-id="b3e96-121">Resurs-ID för virtuella Azure-datorer.</span><span class="sxs-lookup"><span data-stu-id="b3e96-121">Resource Ids for azure virtual machines.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept wildcard characters: False
```

### <span data-ttu-id="b3e96-122">-Tagg</span><span class="sxs-lookup"><span data-stu-id="b3e96-122">-Tag</span></span>
<span data-ttu-id="b3e96-123">Tagga för virtuella Azure-datorer.</span><span class="sxs-lookup"><span data-stu-id="b3e96-123">Tag for azure virtual machines.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept wildcard characters: False
```

### <span data-ttu-id="b3e96-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b3e96-124">CommonParameters</span></span>
<span data-ttu-id="b3e96-125">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b3e96-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="b3e96-126">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b3e96-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b3e96-127">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="b3e96-127">INPUTS</span></span>

### <span data-ttu-id="b3e96-128">System. string []</span><span class="sxs-lookup"><span data-stu-id="b3e96-128">System.String[]</span></span>

### <span data-ttu-id="b3e96-129">System. Collections. hash</span><span class="sxs-lookup"><span data-stu-id="b3e96-129">System.Collections.Hashtable</span></span>

### <span data-ttu-id="b3e96-130">Microsoft. Azure. commands. Automation. Model. UpdateManagement. TagOperators</span><span class="sxs-lookup"><span data-stu-id="b3e96-130">Microsoft.Azure.Commands.Automation.Model.UpdateManagement.TagOperators</span></span>

### <span data-ttu-id="b3e96-131">System. String</span><span class="sxs-lookup"><span data-stu-id="b3e96-131">System.String</span></span>

## <span data-ttu-id="b3e96-132">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="b3e96-132">OUTPUTS</span></span>

### <span data-ttu-id="b3e96-133">Microsoft. Azure. commands. Automation. Model. UpdateManagement. AzureQueryProperties</span><span class="sxs-lookup"><span data-stu-id="b3e96-133">Microsoft.Azure.Commands.Automation.Model.UpdateManagement.AzureQueryProperties</span></span>

## <span data-ttu-id="b3e96-134">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="b3e96-134">NOTES</span></span>

## <span data-ttu-id="b3e96-135">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="b3e96-135">RELATED LINKS</span></span>