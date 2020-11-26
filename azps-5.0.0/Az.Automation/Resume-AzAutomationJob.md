---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 9400E9EB-E927-44D5-8722-9706BDD92FD5
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/resume-azautomationjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Resume-AzAutomationJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Resume-AzAutomationJob.md
ms.openlocfilehash: 731a2df87ce6ad575e9aa3e10eb124e52ec1b60b
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94325986"
---
# <span data-ttu-id="5945e-101">Resume-AzAutomationJob</span><span class="sxs-lookup"><span data-stu-id="5945e-101">Resume-AzAutomationJob</span></span>

## <span data-ttu-id="5945e-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="5945e-102">SYNOPSIS</span></span>
<span data-ttu-id="5945e-103">Återupptar ett uppehållet automatiserings jobb.</span><span class="sxs-lookup"><span data-stu-id="5945e-103">Resumes a suspended Automation job.</span></span>

## <span data-ttu-id="5945e-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="5945e-104">SYNTAX</span></span>

```
Resume-AzAutomationJob [-Id] <Guid> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5945e-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="5945e-105">DESCRIPTION</span></span>
<span data-ttu-id="5945e-106">Cmdleten **Resume-AzAutomationJob** återupptar ett inaktiverat Azure Automation-jobb.</span><span class="sxs-lookup"><span data-stu-id="5945e-106">The **Resume-AzAutomationJob** cmdlet resumes a suspended Azure Automation job.</span></span>
<span data-ttu-id="5945e-107">Ange det upphävda jobbet.</span><span class="sxs-lookup"><span data-stu-id="5945e-107">Specify the suspended job.</span></span>
<span data-ttu-id="5945e-108">Om du vill pausa ett jobb kan du använda Suspend-AzAutomationJob cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5945e-108">To suspend a job, use the Suspend-AzAutomationJob cmdlet.</span></span>

## <span data-ttu-id="5945e-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="5945e-109">EXAMPLES</span></span>

### <span data-ttu-id="5945e-110">Exempel 1: återuppta ett avbrutet jobb</span><span class="sxs-lookup"><span data-stu-id="5945e-110">Example 1: Resume a suspended job</span></span>
```
PS C:\>Resume-AzAutomationJob -AutomationAccountName "Contoso17" -Id 2989b069-24fe-40b9-b3bd-cb7e5eac4b64 -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="5945e-111">Det här kommandot återupptar jobbet som har angivet ID.</span><span class="sxs-lookup"><span data-stu-id="5945e-111">This command resumes the job that has the specified ID.</span></span>

## <span data-ttu-id="5945e-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="5945e-112">PARAMETERS</span></span>

### <span data-ttu-id="5945e-113">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="5945e-113">-AutomationAccountName</span></span>
<span data-ttu-id="5945e-114">Anger namnet på ett Automation-konto där denna cmdlet fortsätter ett jobb.</span><span class="sxs-lookup"><span data-stu-id="5945e-114">Specifies the name of an Automation account in which this cmdlet resume a job.</span></span>

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

### <span data-ttu-id="5945e-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5945e-115">-DefaultProfile</span></span>
<span data-ttu-id="5945e-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="5945e-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="5945e-117">-ID</span><span class="sxs-lookup"><span data-stu-id="5945e-117">-Id</span></span>
<span data-ttu-id="5945e-118">Anger ID för ett jobb som denna cmdlet fortsätter.</span><span class="sxs-lookup"><span data-stu-id="5945e-118">Specifies the ID of a job that this cmdlet resumes.</span></span>

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

### <span data-ttu-id="5945e-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5945e-119">-ResourceGroupName</span></span>
<span data-ttu-id="5945e-120">Anger namnet på en resurs grupp för vilken denna cmdlet återupptar ett jobb.</span><span class="sxs-lookup"><span data-stu-id="5945e-120">Specifies the name of a resource group for which this cmdlet resumes a job.</span></span>

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

### <span data-ttu-id="5945e-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5945e-121">CommonParameters</span></span>
<span data-ttu-id="5945e-122">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5945e-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5945e-123">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5945e-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5945e-124">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="5945e-124">INPUTS</span></span>

### <span data-ttu-id="5945e-125">System. GUID</span><span class="sxs-lookup"><span data-stu-id="5945e-125">System.Guid</span></span>

### <span data-ttu-id="5945e-126">System. String</span><span class="sxs-lookup"><span data-stu-id="5945e-126">System.String</span></span>

## <span data-ttu-id="5945e-127">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="5945e-127">OUTPUTS</span></span>

### <span data-ttu-id="5945e-128">System. Void</span><span class="sxs-lookup"><span data-stu-id="5945e-128">System.Void</span></span>

## <span data-ttu-id="5945e-129">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="5945e-129">NOTES</span></span>

## <span data-ttu-id="5945e-130">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="5945e-130">RELATED LINKS</span></span>

[<span data-ttu-id="5945e-131">Get-AzAutomationJob</span><span class="sxs-lookup"><span data-stu-id="5945e-131">Get-AzAutomationJob</span></span>](./Get-AzAutomationJob.md)

[<span data-ttu-id="5945e-132">Get-AzAutomationJobOutput</span><span class="sxs-lookup"><span data-stu-id="5945e-132">Get-AzAutomationJobOutput</span></span>](./Get-AzAutomationJobOutput.md)

[<span data-ttu-id="5945e-133">Stopp-AzAutomationJob</span><span class="sxs-lookup"><span data-stu-id="5945e-133">Stop-AzAutomationJob</span></span>](./Stop-AzAutomationJob.md)

[<span data-ttu-id="5945e-134">Suspend-AzAutomationJob</span><span class="sxs-lookup"><span data-stu-id="5945e-134">Suspend-AzAutomationJob</span></span>](./Suspend-AzAutomationJob.md)

