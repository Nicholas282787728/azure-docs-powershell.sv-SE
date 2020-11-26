---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: BE1A9247-9F8E-45EA-9590-684A5A5662AC
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/stop-azautomationjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Stop-AzAutomationJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Stop-AzAutomationJob.md
ms.openlocfilehash: 451457cf4483d9af6d8a7aca8731b95dc5c95859
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94322626"
---
# <span data-ttu-id="e9f4f-101">Stop-AzAutomationJob</span><span class="sxs-lookup"><span data-stu-id="e9f4f-101">Stop-AzAutomationJob</span></span>

## <span data-ttu-id="e9f4f-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="e9f4f-102">SYNOPSIS</span></span>
<span data-ttu-id="e9f4f-103">Stoppar ett automatiserings jobb.</span><span class="sxs-lookup"><span data-stu-id="e9f4f-103">Stops an Automation job.</span></span>

## <span data-ttu-id="e9f4f-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="e9f4f-104">SYNTAX</span></span>

```
Stop-AzAutomationJob [-Id] <Guid> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e9f4f-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="e9f4f-105">DESCRIPTION</span></span>
<span data-ttu-id="e9f4f-106">Cmdleten **Stop-AzAutomationJob** stoppar ett Azure Automation-jobb.</span><span class="sxs-lookup"><span data-stu-id="e9f4f-106">The **Stop-AzAutomationJob** cmdlet stops an Azure Automation job.</span></span>
<span data-ttu-id="e9f4f-107">Ange ett automatiserings jobb som körs.</span><span class="sxs-lookup"><span data-stu-id="e9f4f-107">Specify a running Automation job.</span></span>

## <span data-ttu-id="e9f4f-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="e9f4f-108">EXAMPLES</span></span>

### <span data-ttu-id="e9f4f-109">Exempel 1: stoppa ett jobb</span><span class="sxs-lookup"><span data-stu-id="e9f4f-109">Example 1: Stop a job</span></span>
```
PS C:\>Stop-AzAutomationJob -AutomationAccountName "Contoso17" -Id 2989b069-24fe-40b9-b3bd-cb7e5eac4b64 -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="e9f4f-110">Det här kommandot stoppar det jobb som har angivet ID.</span><span class="sxs-lookup"><span data-stu-id="e9f4f-110">This command stops the job that has the specified ID.</span></span>

## <span data-ttu-id="e9f4f-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="e9f4f-111">PARAMETERS</span></span>

### <span data-ttu-id="e9f4f-112">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="e9f4f-112">-AutomationAccountName</span></span>
<span data-ttu-id="e9f4f-113">Anger namnet på ett Automation-konto där denna cmdlet stoppar ett jobb.</span><span class="sxs-lookup"><span data-stu-id="e9f4f-113">Specifies the name of an Automation account in which this cmdlet stops a job.</span></span>

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

### <span data-ttu-id="e9f4f-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e9f4f-114">-DefaultProfile</span></span>
<span data-ttu-id="e9f4f-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="e9f4f-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e9f4f-116">-ID</span><span class="sxs-lookup"><span data-stu-id="e9f4f-116">-Id</span></span>
<span data-ttu-id="e9f4f-117">Anger ID för ett jobb som denna cmdlet stoppar.</span><span class="sxs-lookup"><span data-stu-id="e9f4f-117">Specifies the ID of a job that this cmdlet stops.</span></span>

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

### <span data-ttu-id="e9f4f-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e9f4f-118">-ResourceGroupName</span></span>
<span data-ttu-id="e9f4f-119">Anger namnet på en resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="e9f4f-119">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="e9f4f-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e9f4f-120">CommonParameters</span></span>
<span data-ttu-id="e9f4f-121">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e9f4f-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e9f4f-122">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e9f4f-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e9f4f-123">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="e9f4f-123">INPUTS</span></span>

### <span data-ttu-id="e9f4f-124">System. GUID</span><span class="sxs-lookup"><span data-stu-id="e9f4f-124">System.Guid</span></span>

### <span data-ttu-id="e9f4f-125">System. String</span><span class="sxs-lookup"><span data-stu-id="e9f4f-125">System.String</span></span>

## <span data-ttu-id="e9f4f-126">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="e9f4f-126">OUTPUTS</span></span>

### <span data-ttu-id="e9f4f-127">System. Void</span><span class="sxs-lookup"><span data-stu-id="e9f4f-127">System.Void</span></span>

## <span data-ttu-id="e9f4f-128">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="e9f4f-128">NOTES</span></span>

## <span data-ttu-id="e9f4f-129">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="e9f4f-129">RELATED LINKS</span></span>

[<span data-ttu-id="e9f4f-130">Get-AzAutomationJob</span><span class="sxs-lookup"><span data-stu-id="e9f4f-130">Get-AzAutomationJob</span></span>](./Get-AzAutomationJob.md)

[<span data-ttu-id="e9f4f-131">Get-AzAutomationJobOutput</span><span class="sxs-lookup"><span data-stu-id="e9f4f-131">Get-AzAutomationJobOutput</span></span>](./Get-AzAutomationJobOutput.md)

[<span data-ttu-id="e9f4f-132">Resume-AzAutomationJob</span><span class="sxs-lookup"><span data-stu-id="e9f4f-132">Resume-AzAutomationJob</span></span>](./Resume-AzAutomationJob.md)

[<span data-ttu-id="e9f4f-133">Suspend-AzAutomationJob</span><span class="sxs-lookup"><span data-stu-id="e9f4f-133">Suspend-AzAutomationJob</span></span>](./Suspend-AzAutomationJob.md)

