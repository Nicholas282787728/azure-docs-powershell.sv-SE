---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: 9400E9EB-E927-44D5-8722-9706BDD92FD5
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/resume-azurermautomationjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Resume-AzureRMAutomationJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Resume-AzureRMAutomationJob.md
ms.openlocfilehash: 635b08c90ea87dab98b724110b2228f5b46d61fe
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93755270"
---
# <span data-ttu-id="dce6f-101">Resume-AzureRmAutomationJob</span><span class="sxs-lookup"><span data-stu-id="dce6f-101">Resume-AzureRmAutomationJob</span></span>

## <span data-ttu-id="dce6f-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="dce6f-102">SYNOPSIS</span></span>
<span data-ttu-id="dce6f-103">Återupptar ett uppehållet automatiserings jobb.</span><span class="sxs-lookup"><span data-stu-id="dce6f-103">Resumes a suspended Automation job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="dce6f-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="dce6f-104">SYNTAX</span></span>

```
Resume-AzureRmAutomationJob [-Id] <Guid> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="dce6f-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="dce6f-105">DESCRIPTION</span></span>
<span data-ttu-id="dce6f-106">Cmdleten **Resume-AzureRmAutomationJob** återupptar ett inaktiverat Azure Automation-jobb.</span><span class="sxs-lookup"><span data-stu-id="dce6f-106">The **Resume-AzureRmAutomationJob** cmdlet resumes a suspended Azure Automation job.</span></span>
<span data-ttu-id="dce6f-107">Ange det upphävda jobbet.</span><span class="sxs-lookup"><span data-stu-id="dce6f-107">Specify the suspended job.</span></span>

<span data-ttu-id="dce6f-108">Om du vill pausa ett jobb kan du använda Suspend-AzureRmAutomationJob cmdlet.</span><span class="sxs-lookup"><span data-stu-id="dce6f-108">To suspend a job, use the Suspend-AzureRmAutomationJob cmdlet.</span></span>

## <span data-ttu-id="dce6f-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="dce6f-109">EXAMPLES</span></span>

### <span data-ttu-id="dce6f-110">Exempel 1: återuppta ett avbrutet jobb</span><span class="sxs-lookup"><span data-stu-id="dce6f-110">Example 1: Resume a suspended job</span></span>
```
PS C:\>Resume-AzureRmAutomationJob -AutomationAccountName "Contoso17" -Id 2989b069-24fe-40b9-b3bd-cb7e5eac4b64 -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="dce6f-111">Det här kommandot återupptar jobbet som har angivet ID.</span><span class="sxs-lookup"><span data-stu-id="dce6f-111">This command resumes the job that has the specified ID.</span></span>

## <span data-ttu-id="dce6f-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="dce6f-112">PARAMETERS</span></span>

### <span data-ttu-id="dce6f-113">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="dce6f-113">-AutomationAccountName</span></span>
<span data-ttu-id="dce6f-114">Anger namnet på ett Automation-konto där denna cmdlet fortsätter ett jobb.</span><span class="sxs-lookup"><span data-stu-id="dce6f-114">Specifies the name of an Automation account in which this cmdlet resume a job.</span></span>

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

### <span data-ttu-id="dce6f-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dce6f-115">-DefaultProfile</span></span>
<span data-ttu-id="dce6f-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="dce6f-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="dce6f-117">-ID</span><span class="sxs-lookup"><span data-stu-id="dce6f-117">-Id</span></span>
<span data-ttu-id="dce6f-118">Anger ID för ett jobb som denna cmdlet fortsätter.</span><span class="sxs-lookup"><span data-stu-id="dce6f-118">Specifies the ID of a job that this cmdlet resumes.</span></span>

```yaml
Type: Guid
Parameter Sets: (All)
Aliases: JobId

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dce6f-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dce6f-119">-ResourceGroupName</span></span>
<span data-ttu-id="dce6f-120">Anger namnet på en resurs grupp för vilken denna cmdlet återupptar ett jobb.</span><span class="sxs-lookup"><span data-stu-id="dce6f-120">Specifies the name of a resource group for which this cmdlet resumes a job.</span></span>

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

### <span data-ttu-id="dce6f-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dce6f-121">CommonParameters</span></span>
<span data-ttu-id="dce6f-122">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dce6f-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dce6f-123">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dce6f-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dce6f-124">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="dce6f-124">INPUTS</span></span>

### <span data-ttu-id="dce6f-125">Ingen</span><span class="sxs-lookup"><span data-stu-id="dce6f-125">None</span></span>
<span data-ttu-id="dce6f-126">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="dce6f-126">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="dce6f-127">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="dce6f-127">OUTPUTS</span></span>

## <span data-ttu-id="dce6f-128">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="dce6f-128">NOTES</span></span>

## <span data-ttu-id="dce6f-129">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="dce6f-129">RELATED LINKS</span></span>

[<span data-ttu-id="dce6f-130">Get-AzureRmAutomationJob</span><span class="sxs-lookup"><span data-stu-id="dce6f-130">Get-AzureRmAutomationJob</span></span>](./Get-AzureRMAutomationJob.md)

[<span data-ttu-id="dce6f-131">Get-AzureRmAutomationJobOutput</span><span class="sxs-lookup"><span data-stu-id="dce6f-131">Get-AzureRmAutomationJobOutput</span></span>](./Get-AzureRMAutomationJobOutput.md)

[<span data-ttu-id="dce6f-132">Stopp-AzureRmAutomationJob</span><span class="sxs-lookup"><span data-stu-id="dce6f-132">Stop-AzureRmAutomationJob</span></span>](./Stop-AzureRMAutomationJob.md)

[<span data-ttu-id="dce6f-133">Suspend-AzureRmAutomationJob</span><span class="sxs-lookup"><span data-stu-id="dce6f-133">Suspend-AzureRmAutomationJob</span></span>](./Suspend-AzureRMAutomationJob.md)


