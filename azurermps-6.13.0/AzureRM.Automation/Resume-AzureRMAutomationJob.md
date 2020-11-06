---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: 9400E9EB-E927-44D5-8722-9706BDD92FD5
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/resume-azurermautomationjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Resume-AzureRMAutomationJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Resume-AzureRMAutomationJob.md
ms.openlocfilehash: 8e84f2f66703410b626769be8c2c2d5a57e531e9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93575348"
---
# <span data-ttu-id="02e5e-101">Resume-AzureRmAutomationJob</span><span class="sxs-lookup"><span data-stu-id="02e5e-101">Resume-AzureRmAutomationJob</span></span>

## <span data-ttu-id="02e5e-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="02e5e-102">SYNOPSIS</span></span>
<span data-ttu-id="02e5e-103">Återupptar ett uppehållet automatiserings jobb.</span><span class="sxs-lookup"><span data-stu-id="02e5e-103">Resumes a suspended Automation job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="02e5e-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="02e5e-104">SYNTAX</span></span>

```
Resume-AzureRmAutomationJob [-Id] <Guid> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="02e5e-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="02e5e-105">DESCRIPTION</span></span>
<span data-ttu-id="02e5e-106">Cmdleten **Resume-AzureRmAutomationJob** återupptar ett inaktiverat Azure Automation-jobb.</span><span class="sxs-lookup"><span data-stu-id="02e5e-106">The **Resume-AzureRmAutomationJob** cmdlet resumes a suspended Azure Automation job.</span></span>
<span data-ttu-id="02e5e-107">Ange det upphävda jobbet.</span><span class="sxs-lookup"><span data-stu-id="02e5e-107">Specify the suspended job.</span></span>
<span data-ttu-id="02e5e-108">Om du vill pausa ett jobb kan du använda Suspend-AzureRmAutomationJob cmdlet.</span><span class="sxs-lookup"><span data-stu-id="02e5e-108">To suspend a job, use the Suspend-AzureRmAutomationJob cmdlet.</span></span>

## <span data-ttu-id="02e5e-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="02e5e-109">EXAMPLES</span></span>

### <span data-ttu-id="02e5e-110">Exempel 1: återuppta ett avbrutet jobb</span><span class="sxs-lookup"><span data-stu-id="02e5e-110">Example 1: Resume a suspended job</span></span>
```
PS C:\>Resume-AzureRmAutomationJob -AutomationAccountName "Contoso17" -Id 2989b069-24fe-40b9-b3bd-cb7e5eac4b64 -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="02e5e-111">Det här kommandot återupptar jobbet som har angivet ID.</span><span class="sxs-lookup"><span data-stu-id="02e5e-111">This command resumes the job that has the specified ID.</span></span>

## <span data-ttu-id="02e5e-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="02e5e-112">PARAMETERS</span></span>

### <span data-ttu-id="02e5e-113">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="02e5e-113">-AutomationAccountName</span></span>
<span data-ttu-id="02e5e-114">Anger namnet på ett Automation-konto där denna cmdlet fortsätter ett jobb.</span><span class="sxs-lookup"><span data-stu-id="02e5e-114">Specifies the name of an Automation account in which this cmdlet resume a job.</span></span>

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

### <span data-ttu-id="02e5e-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="02e5e-115">-DefaultProfile</span></span>
<span data-ttu-id="02e5e-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="02e5e-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="02e5e-117">-ID</span><span class="sxs-lookup"><span data-stu-id="02e5e-117">-Id</span></span>
<span data-ttu-id="02e5e-118">Anger ID för ett jobb som denna cmdlet fortsätter.</span><span class="sxs-lookup"><span data-stu-id="02e5e-118">Specifies the ID of a job that this cmdlet resumes.</span></span>

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

### <span data-ttu-id="02e5e-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="02e5e-119">-ResourceGroupName</span></span>
<span data-ttu-id="02e5e-120">Anger namnet på en resurs grupp för vilken denna cmdlet återupptar ett jobb.</span><span class="sxs-lookup"><span data-stu-id="02e5e-120">Specifies the name of a resource group for which this cmdlet resumes a job.</span></span>

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

### <span data-ttu-id="02e5e-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="02e5e-121">CommonParameters</span></span>
<span data-ttu-id="02e5e-122">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="02e5e-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="02e5e-123">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="02e5e-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="02e5e-124">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="02e5e-124">INPUTS</span></span>

### <span data-ttu-id="02e5e-125">System. GUID</span><span class="sxs-lookup"><span data-stu-id="02e5e-125">System.Guid</span></span>

### <span data-ttu-id="02e5e-126">System. String</span><span class="sxs-lookup"><span data-stu-id="02e5e-126">System.String</span></span>

## <span data-ttu-id="02e5e-127">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="02e5e-127">OUTPUTS</span></span>

### <span data-ttu-id="02e5e-128">System. Void</span><span class="sxs-lookup"><span data-stu-id="02e5e-128">System.Void</span></span>

## <span data-ttu-id="02e5e-129">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="02e5e-129">NOTES</span></span>

## <span data-ttu-id="02e5e-130">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="02e5e-130">RELATED LINKS</span></span>

[<span data-ttu-id="02e5e-131">Get-AzureRmAutomationJob</span><span class="sxs-lookup"><span data-stu-id="02e5e-131">Get-AzureRmAutomationJob</span></span>](./Get-AzureRMAutomationJob.md)

[<span data-ttu-id="02e5e-132">Get-AzureRmAutomationJobOutput</span><span class="sxs-lookup"><span data-stu-id="02e5e-132">Get-AzureRmAutomationJobOutput</span></span>](./Get-AzureRMAutomationJobOutput.md)

[<span data-ttu-id="02e5e-133">Stopp-AzureRmAutomationJob</span><span class="sxs-lookup"><span data-stu-id="02e5e-133">Stop-AzureRmAutomationJob</span></span>](./Stop-AzureRMAutomationJob.md)

[<span data-ttu-id="02e5e-134">Suspend-AzureRmAutomationJob</span><span class="sxs-lookup"><span data-stu-id="02e5e-134">Suspend-AzureRmAutomationJob</span></span>](./Suspend-AzureRMAutomationJob.md)


