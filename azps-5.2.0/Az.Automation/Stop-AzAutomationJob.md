---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: BE1A9247-9F8E-45EA-9590-684A5A5662AC
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/stop-azautomationjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Stop-AzAutomationJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Stop-AzAutomationJob.md
ms.openlocfilehash: 451457cf4483d9af6d8a7aca8731b95dc5c95859
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98401115"
---
# <span data-ttu-id="40d02-101">Stop-AzAutomationJob</span><span class="sxs-lookup"><span data-stu-id="40d02-101">Stop-AzAutomationJob</span></span>

## <span data-ttu-id="40d02-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="40d02-102">SYNOPSIS</span></span>
<span data-ttu-id="40d02-103">Stoppar ett automatiserings jobb.</span><span class="sxs-lookup"><span data-stu-id="40d02-103">Stops an Automation job.</span></span>

## <span data-ttu-id="40d02-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="40d02-104">SYNTAX</span></span>

```
Stop-AzAutomationJob [-Id] <Guid> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="40d02-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="40d02-105">DESCRIPTION</span></span>
<span data-ttu-id="40d02-106">Cmdleten **Stop-AzAutomationJob** stoppar ett Azure Automation-jobb.</span><span class="sxs-lookup"><span data-stu-id="40d02-106">The **Stop-AzAutomationJob** cmdlet stops an Azure Automation job.</span></span>
<span data-ttu-id="40d02-107">Ange ett automatiserings jobb som körs.</span><span class="sxs-lookup"><span data-stu-id="40d02-107">Specify a running Automation job.</span></span>

## <span data-ttu-id="40d02-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="40d02-108">EXAMPLES</span></span>

### <span data-ttu-id="40d02-109">Exempel 1: stoppa ett jobb</span><span class="sxs-lookup"><span data-stu-id="40d02-109">Example 1: Stop a job</span></span>
```
PS C:\>Stop-AzAutomationJob -AutomationAccountName "Contoso17" -Id 2989b069-24fe-40b9-b3bd-cb7e5eac4b64 -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="40d02-110">Det här kommandot stoppar det jobb som har angivet ID.</span><span class="sxs-lookup"><span data-stu-id="40d02-110">This command stops the job that has the specified ID.</span></span>

## <span data-ttu-id="40d02-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="40d02-111">PARAMETERS</span></span>

### <span data-ttu-id="40d02-112">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="40d02-112">-AutomationAccountName</span></span>
<span data-ttu-id="40d02-113">Anger namnet på ett Automation-konto där denna cmdlet stoppar ett jobb.</span><span class="sxs-lookup"><span data-stu-id="40d02-113">Specifies the name of an Automation account in which this cmdlet stops a job.</span></span>

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

### <span data-ttu-id="40d02-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="40d02-114">-DefaultProfile</span></span>
<span data-ttu-id="40d02-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="40d02-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="40d02-116">-ID</span><span class="sxs-lookup"><span data-stu-id="40d02-116">-Id</span></span>
<span data-ttu-id="40d02-117">Anger ID för ett jobb som denna cmdlet stoppar.</span><span class="sxs-lookup"><span data-stu-id="40d02-117">Specifies the ID of a job that this cmdlet stops.</span></span>

```yaml
Type: System.Guid
Parameter Sets: (All)
Aliases: JobId

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="40d02-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="40d02-118">-ResourceGroupName</span></span>
<span data-ttu-id="40d02-119">Anger namnet på en resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="40d02-119">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="40d02-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="40d02-120">CommonParameters</span></span>
<span data-ttu-id="40d02-121">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="40d02-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="40d02-122">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="40d02-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="40d02-123">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="40d02-123">INPUTS</span></span>

### <span data-ttu-id="40d02-124">System. GUID</span><span class="sxs-lookup"><span data-stu-id="40d02-124">System.Guid</span></span>

### <span data-ttu-id="40d02-125">System. String</span><span class="sxs-lookup"><span data-stu-id="40d02-125">System.String</span></span>

## <span data-ttu-id="40d02-126">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="40d02-126">OUTPUTS</span></span>

### <span data-ttu-id="40d02-127">System. Void</span><span class="sxs-lookup"><span data-stu-id="40d02-127">System.Void</span></span>

## <span data-ttu-id="40d02-128">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="40d02-128">NOTES</span></span>

## <span data-ttu-id="40d02-129">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="40d02-129">RELATED LINKS</span></span>

[<span data-ttu-id="40d02-130">Get-AzAutomationJob</span><span class="sxs-lookup"><span data-stu-id="40d02-130">Get-AzAutomationJob</span></span>](./Get-AzAutomationJob.md)

[<span data-ttu-id="40d02-131">Get-AzAutomationJobOutput</span><span class="sxs-lookup"><span data-stu-id="40d02-131">Get-AzAutomationJobOutput</span></span>](./Get-AzAutomationJobOutput.md)

[<span data-ttu-id="40d02-132">Resume-AzAutomationJob</span><span class="sxs-lookup"><span data-stu-id="40d02-132">Resume-AzAutomationJob</span></span>](./Resume-AzAutomationJob.md)

[<span data-ttu-id="40d02-133">Suspend-AzAutomationJob</span><span class="sxs-lookup"><span data-stu-id="40d02-133">Suspend-AzAutomationJob</span></span>](./Suspend-AzAutomationJob.md)


