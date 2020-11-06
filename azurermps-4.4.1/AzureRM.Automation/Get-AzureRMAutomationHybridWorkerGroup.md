---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: 9B0BBBB4-A7A0-4243-9264-362A00F5B399
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRMAutomationHybridWorkerGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRMAutomationHybridWorkerGroup.md
ms.openlocfilehash: 1f2c82bc51cb5faba9f5b1dd0524e7aced2f0b84
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93581548"
---
# <span data-ttu-id="08961-101">Get-AzureRMAutomationHybridWorkerGroup</span><span class="sxs-lookup"><span data-stu-id="08961-101">Get-AzureRMAutomationHybridWorkerGroup</span></span>

## <span data-ttu-id="08961-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="08961-102">SYNOPSIS</span></span>
<span data-ttu-id="08961-103">Får hybrid Runbook Worker-grupper.</span><span class="sxs-lookup"><span data-stu-id="08961-103">Gets hybrid runbook worker groups.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="08961-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="08961-104">SYNTAX</span></span>

### <span data-ttu-id="08961-105">ByAll (standard)</span><span class="sxs-lookup"><span data-stu-id="08961-105">ByAll (Default)</span></span>
```
Get-AzureRMAutomationHybridWorkerGroup [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="08961-106">ByName</span><span class="sxs-lookup"><span data-stu-id="08961-106">ByName</span></span>
```
Get-AzureRMAutomationHybridWorkerGroup [[-Name] <String>] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="08961-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="08961-107">DESCRIPTION</span></span>
<span data-ttu-id="08961-108">Cmdleten **Get-AzureRmAutomationHybridWorkerGroup** får Azure Automation hybrid Runbook Worker-grupper.</span><span class="sxs-lookup"><span data-stu-id="08961-108">The **Get-AzureRmAutomationHybridWorkerGroup** cmdlet gets Azure Automation hybrid runbook worker groups.</span></span>
<span data-ttu-id="08961-109">Ange namnet på en specifik grupp.</span><span class="sxs-lookup"><span data-stu-id="08961-109">To get a specific group, specify its name.</span></span>

## <span data-ttu-id="08961-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="08961-110">EXAMPLES</span></span>

### <span data-ttu-id="08961-111">Exempel 1: Hämta alla hybrid Runbook Worker-grupper</span><span class="sxs-lookup"><span data-stu-id="08961-111">Example 1: Get all hybrid runbook worker groups</span></span>
```
PS C:\>Get-AzureRMAutomationHybridWorkerGroup -ResourceGroupName "ResourceGroupName01" -AutomationAccountName "Contoso17"
```

<span data-ttu-id="08961-112">Det här kommandot får alla hybrid Runbook Worker-grupper i Automation-kontot som heter Contoso17.</span><span class="sxs-lookup"><span data-stu-id="08961-112">This command gets all hybrid runbook worker groups in the Automation account named Contoso17.</span></span>

### <span data-ttu-id="08961-113">Exempel 2: skaffa en enda hybrid Runbook Worker-grupp</span><span class="sxs-lookup"><span data-stu-id="08961-113">Example 2: Get a single hybrid runbook worker group</span></span>
```
PS C:\>Get-AzureRMAutomationHybridWorkerGroup -ResourceGroupName "ResourceGroupName01" -AutomationAccountName "Contoso17" -Name "HybridRunbookWorkerGroup01"
```

<span data-ttu-id="08961-114">Det här kommandot får hybrid Runbook Worker-gruppen som heter HybridRunbookWorkerGroup01 i Automation-kontot med namnet Contoso17.</span><span class="sxs-lookup"><span data-stu-id="08961-114">This command gets the hybrid runbook worker group named HybridRunbookWorkerGroup01 in the Automation account named Contoso17.</span></span>

### <span data-ttu-id="08961-115">Exempel 3: Hämta arbetare i en hybrid Runbook Worker-grupp</span><span class="sxs-lookup"><span data-stu-id="08961-115">Example 3: Get the workers in a hybrid runbook worker group</span></span>
```
PS C:\>(Get-AzureRMAutomationHybridWorker -ResourceGroupName ResourceGroupName01 -AutomationAccountName Contoso17 -Name "HybridRunbookWorkerGroup01" ).RunbookWorker
```

<span data-ttu-id="08961-116">Det här kommandot får hybrid Runbook Worker i hybrid Runbook Worker-gruppen med namnet HybridRunbookWorkerGroup01 i Automation-kontot med namnet Contoso17.</span><span class="sxs-lookup"><span data-stu-id="08961-116">This command gets the hybrid runbook workers in the hybrid runbook worker group named HybridRunbookWorkerGroup01 in the Automation account named Contoso17.</span></span>

## <span data-ttu-id="08961-117">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="08961-117">PARAMETERS</span></span>

### <span data-ttu-id="08961-118">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="08961-118">-AutomationAccountName</span></span>
<span data-ttu-id="08961-119">Anger namnet på ett Automation-konto.</span><span class="sxs-lookup"><span data-stu-id="08961-119">Specifies the name of an Automation account.</span></span>

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

### <span data-ttu-id="08961-120">-Namn</span><span class="sxs-lookup"><span data-stu-id="08961-120">-Name</span></span>
<span data-ttu-id="08961-121">Anger namnet på Hybrid Runbook Worker-gruppen.</span><span class="sxs-lookup"><span data-stu-id="08961-121">Specifies the hybrid runbook worker group name.</span></span>

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

### <span data-ttu-id="08961-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="08961-122">-ResourceGroupName</span></span>
<span data-ttu-id="08961-123">Anger namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="08961-123">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="08961-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="08961-124">-DefaultProfile</span></span>
<span data-ttu-id="08961-125">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="08961-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="08961-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="08961-126">CommonParameters</span></span>
<span data-ttu-id="08961-127">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="08961-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="08961-128">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="08961-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="08961-129">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="08961-129">INPUTS</span></span>

### <span data-ttu-id="08961-130">Strängvärdet</span><span class="sxs-lookup"><span data-stu-id="08961-130">String</span></span>
<span data-ttu-id="08961-131">Parametern "name" accepterar värdet för typen String från pipeline</span><span class="sxs-lookup"><span data-stu-id="08961-131">Parameter 'Name' accepts value of type 'String' from the pipeline</span></span>

## <span data-ttu-id="08961-132">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="08961-132">OUTPUTS</span></span>

### <span data-ttu-id="08961-133">Microsoft. Azure. commands. Automation. Model. HybridRunbookWorker</span><span class="sxs-lookup"><span data-stu-id="08961-133">Microsoft.Azure.Commands.Automation.Model.HybridRunbookWorker</span></span>

## <span data-ttu-id="08961-134">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="08961-134">NOTES</span></span>

## <span data-ttu-id="08961-135">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="08961-135">RELATED LINKS</span></span>

