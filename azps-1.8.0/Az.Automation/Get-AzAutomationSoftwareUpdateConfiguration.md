---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/get-azautomationsoftwareupdateconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationSoftwareUpdateConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationSoftwareUpdateConfiguration.md
ms.openlocfilehash: 549818e8dfe04730ef8387779d38921fa965e8b7
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93754827"
---
# <span data-ttu-id="ab22c-101">Get-AzAutomationSoftwareUpdateConfiguration</span><span class="sxs-lookup"><span data-stu-id="ab22c-101">Get-AzAutomationSoftwareUpdateConfiguration</span></span>

## <span data-ttu-id="ab22c-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="ab22c-102">SYNOPSIS</span></span>
<span data-ttu-id="ab22c-103">Hämtar en lista över konfigurationer för Azure Automation-programuppdatering.</span><span class="sxs-lookup"><span data-stu-id="ab22c-103">Gets a list of azure automation software update configurations.</span></span>

## <span data-ttu-id="ab22c-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="ab22c-104">SYNTAX</span></span>

### <span data-ttu-id="ab22c-105">ByAll (standard)</span><span class="sxs-lookup"><span data-stu-id="ab22c-105">ByAll (Default)</span></span>
```
Get-AzAutomationSoftwareUpdateConfiguration [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ab22c-106">ByName</span><span class="sxs-lookup"><span data-stu-id="ab22c-106">ByName</span></span>
```
Get-AzAutomationSoftwareUpdateConfiguration -Name <String> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ab22c-107">ByVMId</span><span class="sxs-lookup"><span data-stu-id="ab22c-107">ByVMId</span></span>
```
Get-AzAutomationSoftwareUpdateConfiguration -AzureVMResourceId <String> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ab22c-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="ab22c-108">DESCRIPTION</span></span>
<span data-ttu-id="ab22c-109">Get-AzAutomationSoftwareUpdateConfiguration returnerar en lista med konfigurationer för program uppdatering.</span><span class="sxs-lookup"><span data-stu-id="ab22c-109">The Get-AzAutomationSoftwareUpdateConfiguration returns a list of software update configurations.</span></span> <span data-ttu-id="ab22c-110">Om du vill ha en specifik konfiguration för program uppdateringen anger du parametern name.</span><span class="sxs-lookup"><span data-stu-id="ab22c-110">To get a specific software update configuration, specify the name parameter.</span></span> <span data-ttu-id="ab22c-111">Du kan också lista de konfigurationer för program uppdateringar som riktar sig mot specifik Azure Virtual Machine genom att ange Azure Resource ID för den här virtuella datorn.</span><span class="sxs-lookup"><span data-stu-id="ab22c-111">You can also list software update configurations targeting specific azure virtual machine by specifying the azure resource Id for this virtual machine.</span></span>

## <span data-ttu-id="ab22c-112">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="ab22c-112">EXAMPLES</span></span>

### <span data-ttu-id="ab22c-113">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="ab22c-113">Example 1</span></span>
<span data-ttu-id="ab22c-114">Skaffa en konfiguration för Azure Automation-programuppdatering med namn.</span><span class="sxs-lookup"><span data-stu-id="ab22c-114">Get an azure automation software update configuration by name.</span></span>

```powershell
PS C:\> Get-AzAutomationSoftwareUpdateConfiguration -ResourceGroupName "mygroup" -AutomationAccountName "myaccount" -Name "MyWeeklySchedule"

UpdateConfiguration   : Microsoft.Azure.Commands.Automation.Model.UpdateManagement.UpdateConfiguration
ScheduleConfiguration : Microsoft.Azure.Commands.Automation.Model.Schedule
ProvisioningState     : Succeeded
ErrorInfo             :
ResourceGroupName     : mygroup
AutomationAccountName : myaccount
Name                  : MyWeeklySchedule
CreationTime          : 9/14/2018 3:53:27 AM +00:00
LastModifiedTime      : 9/14/2018 3:53:37 AM +00:00
Description           :
```

## <span data-ttu-id="ab22c-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="ab22c-115">PARAMETERS</span></span>

### <span data-ttu-id="ab22c-116">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="ab22c-116">-AutomationAccountName</span></span>
<span data-ttu-id="ab22c-117">Namnet på Automation-kontot.</span><span class="sxs-lookup"><span data-stu-id="ab22c-117">The automation account name.</span></span>

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

### <span data-ttu-id="ab22c-118">-AzureVMResourceId</span><span class="sxs-lookup"><span data-stu-id="ab22c-118">-AzureVMResourceId</span></span>
<span data-ttu-id="ab22c-119">Azure Resource ID för den virtuella datorn.</span><span class="sxs-lookup"><span data-stu-id="ab22c-119">Azure resource Id of the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVMId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ab22c-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ab22c-120">-DefaultProfile</span></span>
<span data-ttu-id="ab22c-121">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="ab22c-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ab22c-122">-Namn</span><span class="sxs-lookup"><span data-stu-id="ab22c-122">-Name</span></span>
<span data-ttu-id="ab22c-123">Namn på konfiguration av program uppdatering.</span><span class="sxs-lookup"><span data-stu-id="ab22c-123">Name of the software update configuration.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ab22c-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ab22c-124">-ResourceGroupName</span></span>
<span data-ttu-id="ab22c-125">Resurs gruppens namn.</span><span class="sxs-lookup"><span data-stu-id="ab22c-125">The resource group name.</span></span>

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

### <span data-ttu-id="ab22c-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ab22c-126">CommonParameters</span></span>
<span data-ttu-id="ab22c-127">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ab22c-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ab22c-128">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ab22c-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ab22c-129">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="ab22c-129">INPUTS</span></span>

### <span data-ttu-id="ab22c-130">System. String</span><span class="sxs-lookup"><span data-stu-id="ab22c-130">System.String</span></span>

## <span data-ttu-id="ab22c-131">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="ab22c-131">OUTPUTS</span></span>

### <span data-ttu-id="ab22c-132">Microsoft. Azure. commands. Automation. Model. UpdateManagement. SoftwareUpdateConfiguration</span><span class="sxs-lookup"><span data-stu-id="ab22c-132">Microsoft.Azure.Commands.Automation.Model.UpdateManagement.SoftwareUpdateConfiguration</span></span>

## <span data-ttu-id="ab22c-133">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="ab22c-133">NOTES</span></span>

## <span data-ttu-id="ab22c-134">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="ab22c-134">RELATED LINKS</span></span>
