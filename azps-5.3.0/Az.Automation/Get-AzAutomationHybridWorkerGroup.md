---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 9B0BBBB4-A7A0-4243-9264-362A00F5B399
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/get-azautomationhybridworkergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationHybridWorkerGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationHybridWorkerGroup.md
ms.openlocfilehash: d675c6e5b83f76451808f397427011ac3406e37a
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98524978"
---
# <span data-ttu-id="cc881-101">Get-AzAutomationHybridWorkerGroup</span><span class="sxs-lookup"><span data-stu-id="cc881-101">Get-AzAutomationHybridWorkerGroup</span></span>

## <span data-ttu-id="cc881-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="cc881-102">SYNOPSIS</span></span>
<span data-ttu-id="cc881-103">Får hybrid Runbook Worker-grupper.</span><span class="sxs-lookup"><span data-stu-id="cc881-103">Gets hybrid runbook worker groups.</span></span>

## <span data-ttu-id="cc881-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="cc881-104">SYNTAX</span></span>

### <span data-ttu-id="cc881-105">ByAll (standard)</span><span class="sxs-lookup"><span data-stu-id="cc881-105">ByAll (Default)</span></span>
```
Get-AzAutomationHybridWorkerGroup [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="cc881-106">ByName</span><span class="sxs-lookup"><span data-stu-id="cc881-106">ByName</span></span>
```
Get-AzAutomationHybridWorkerGroup [[-Name] <String>] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cc881-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="cc881-107">DESCRIPTION</span></span>
<span data-ttu-id="cc881-108">Cmdleten **Get-AzAutomationHybridWorkerGroup** får Azure Automation hybrid Runbook Worker-grupper.</span><span class="sxs-lookup"><span data-stu-id="cc881-108">The **Get-AzAutomationHybridWorkerGroup** cmdlet gets Azure Automation hybrid runbook worker groups.</span></span>
<span data-ttu-id="cc881-109">Ange namnet på en specifik grupp.</span><span class="sxs-lookup"><span data-stu-id="cc881-109">To get a specific group, specify its name.</span></span>

## <span data-ttu-id="cc881-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="cc881-110">EXAMPLES</span></span>

### <span data-ttu-id="cc881-111">Exempel 1: Hämta alla hybrid Runbook Worker-grupper</span><span class="sxs-lookup"><span data-stu-id="cc881-111">Example 1: Get all hybrid runbook worker groups</span></span>
```
PS C:\>Get-AzAutomationHybridWorkerGroup -ResourceGroupName "ResourceGroupName01" -AutomationAccountName "Contoso17"
```

<span data-ttu-id="cc881-112">Det här kommandot får alla hybrid Runbook Worker-grupper i Automation-kontot som heter Contoso17.</span><span class="sxs-lookup"><span data-stu-id="cc881-112">This command gets all hybrid runbook worker groups in the Automation account named Contoso17.</span></span>

### <span data-ttu-id="cc881-113">Exempel 2: skaffa en enda hybrid Runbook Worker-grupp</span><span class="sxs-lookup"><span data-stu-id="cc881-113">Example 2: Get a single hybrid runbook worker group</span></span>
```
PS C:\>Get-AzAutomationHybridWorkerGroup -ResourceGroupName "ResourceGroupName01" -AutomationAccountName "Contoso17" -Name "HybridRunbookWorkerGroup01"
```

<span data-ttu-id="cc881-114">Det här kommandot får hybrid Runbook Worker-gruppen som heter HybridRunbookWorkerGroup01 i Automation-kontot med namnet Contoso17.</span><span class="sxs-lookup"><span data-stu-id="cc881-114">This command gets the hybrid runbook worker group named HybridRunbookWorkerGroup01 in the Automation account named Contoso17.</span></span>

### <span data-ttu-id="cc881-115">Exempel 3: Hämta arbetare i en hybrid Runbook Worker-grupp</span><span class="sxs-lookup"><span data-stu-id="cc881-115">Example 3: Get the workers in a hybrid runbook worker group</span></span>
```
PS C:\>(Get-AzAutomationHybridWorker -ResourceGroupName ResourceGroupName01 -AutomationAccountName Contoso17 -Name "HybridRunbookWorkerGroup01" ).RunbookWorker
```

<span data-ttu-id="cc881-116">Det här kommandot får hybrid Runbook Worker i hybrid Runbook Worker-gruppen med namnet HybridRunbookWorkerGroup01 i Automation-kontot med namnet Contoso17.</span><span class="sxs-lookup"><span data-stu-id="cc881-116">This command gets the hybrid runbook workers in the hybrid runbook worker group named HybridRunbookWorkerGroup01 in the Automation account named Contoso17.</span></span>

## <span data-ttu-id="cc881-117">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="cc881-117">PARAMETERS</span></span>

### <span data-ttu-id="cc881-118">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="cc881-118">-AutomationAccountName</span></span>
<span data-ttu-id="cc881-119">Anger namnet på ett Automation-konto.</span><span class="sxs-lookup"><span data-stu-id="cc881-119">Specifies the name of an Automation account.</span></span>

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

### <span data-ttu-id="cc881-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cc881-120">-DefaultProfile</span></span>
<span data-ttu-id="cc881-121">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="cc881-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="cc881-122">-Namn</span><span class="sxs-lookup"><span data-stu-id="cc881-122">-Name</span></span>
<span data-ttu-id="cc881-123">Anger namnet på Hybrid Runbook Worker-gruppen.</span><span class="sxs-lookup"><span data-stu-id="cc881-123">Specifies the hybrid runbook worker group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases: Group

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="cc881-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cc881-124">-ResourceGroupName</span></span>
<span data-ttu-id="cc881-125">Anger namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="cc881-125">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="cc881-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cc881-126">CommonParameters</span></span>
<span data-ttu-id="cc881-127">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cc881-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cc881-128">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cc881-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cc881-129">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="cc881-129">INPUTS</span></span>

### <span data-ttu-id="cc881-130">System. String</span><span class="sxs-lookup"><span data-stu-id="cc881-130">System.String</span></span>

## <span data-ttu-id="cc881-131">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="cc881-131">OUTPUTS</span></span>

### <span data-ttu-id="cc881-132">Microsoft. Azure. commands. Automation. Model. HybridRunbookWorkerGroup</span><span class="sxs-lookup"><span data-stu-id="cc881-132">Microsoft.Azure.Commands.Automation.Model.HybridRunbookWorkerGroup</span></span>

## <span data-ttu-id="cc881-133">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="cc881-133">NOTES</span></span>

## <span data-ttu-id="cc881-134">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="cc881-134">RELATED LINKS</span></span>
