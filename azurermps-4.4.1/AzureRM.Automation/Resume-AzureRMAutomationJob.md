---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: 9400E9EB-E927-44D5-8722-9706BDD92FD5
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Resume-AzureRMAutomationJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Resume-AzureRMAutomationJob.md
ms.openlocfilehash: 6d23fe3728b569cbb1a2aee498d560672ee75877
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93578511"
---
# <span data-ttu-id="5ed60-101">Resume-AzureRmAutomationJob</span><span class="sxs-lookup"><span data-stu-id="5ed60-101">Resume-AzureRmAutomationJob</span></span>

## <span data-ttu-id="5ed60-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="5ed60-102">SYNOPSIS</span></span>
<span data-ttu-id="5ed60-103">Återupptar ett uppehållet automatiserings jobb.</span><span class="sxs-lookup"><span data-stu-id="5ed60-103">Resumes a suspended Automation job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5ed60-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="5ed60-104">SYNTAX</span></span>

```
Resume-AzureRmAutomationJob [-Id] <Guid> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5ed60-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="5ed60-105">DESCRIPTION</span></span>
<span data-ttu-id="5ed60-106">Cmdleten **Resume-AzureRmAutomationJob** återupptar ett inaktiverat Azure Automation-jobb.</span><span class="sxs-lookup"><span data-stu-id="5ed60-106">The **Resume-AzureRmAutomationJob** cmdlet resumes a suspended Azure Automation job.</span></span>
<span data-ttu-id="5ed60-107">Ange det upphävda jobbet.</span><span class="sxs-lookup"><span data-stu-id="5ed60-107">Specify the suspended job.</span></span>

<span data-ttu-id="5ed60-108">Om du vill pausa ett jobb kan du använda Suspend-AzureRmAutomationJob cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5ed60-108">To suspend a job, use the Suspend-AzureRmAutomationJob cmdlet.</span></span>

## <span data-ttu-id="5ed60-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="5ed60-109">EXAMPLES</span></span>

### <span data-ttu-id="5ed60-110">Exempel 1: återuppta ett avbrutet jobb</span><span class="sxs-lookup"><span data-stu-id="5ed60-110">Example 1: Resume a suspended job</span></span>
```
PS C:\>Resume-AzureRmAutomationJob -AutomationAccountName "Contoso17" -Id 2989b069-24fe-40b9-b3bd-cb7e5eac4b64 -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="5ed60-111">Det här kommandot återupptar jobbet som har angivet ID.</span><span class="sxs-lookup"><span data-stu-id="5ed60-111">This command resumes the job that has the specified ID.</span></span>

## <span data-ttu-id="5ed60-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="5ed60-112">PARAMETERS</span></span>

### <span data-ttu-id="5ed60-113">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="5ed60-113">-AutomationAccountName</span></span>
<span data-ttu-id="5ed60-114">Anger namnet på ett Automation-konto där denna cmdlet fortsätter ett jobb.</span><span class="sxs-lookup"><span data-stu-id="5ed60-114">Specifies the name of an Automation account in which this cmdlet resume a job.</span></span>

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

### <span data-ttu-id="5ed60-115">-ID</span><span class="sxs-lookup"><span data-stu-id="5ed60-115">-Id</span></span>
<span data-ttu-id="5ed60-116">Anger ID för ett jobb som denna cmdlet fortsätter.</span><span class="sxs-lookup"><span data-stu-id="5ed60-116">Specifies the ID of a job that this cmdlet resumes.</span></span>

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

### <span data-ttu-id="5ed60-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5ed60-117">-ResourceGroupName</span></span>
<span data-ttu-id="5ed60-118">Anger namnet på en resurs grupp för vilken denna cmdlet återupptar ett jobb.</span><span class="sxs-lookup"><span data-stu-id="5ed60-118">Specifies the name of a resource group for which this cmdlet resumes a job.</span></span>

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

### <span data-ttu-id="5ed60-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5ed60-119">-DefaultProfile</span></span>
<span data-ttu-id="5ed60-120">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="5ed60-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5ed60-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5ed60-121">CommonParameters</span></span>
<span data-ttu-id="5ed60-122">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5ed60-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5ed60-123">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5ed60-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5ed60-124">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="5ed60-124">INPUTS</span></span>

## <span data-ttu-id="5ed60-125">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="5ed60-125">OUTPUTS</span></span>

## <span data-ttu-id="5ed60-126">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="5ed60-126">NOTES</span></span>

## <span data-ttu-id="5ed60-127">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="5ed60-127">RELATED LINKS</span></span>

[<span data-ttu-id="5ed60-128">Get-AzureRmAutomationJob</span><span class="sxs-lookup"><span data-stu-id="5ed60-128">Get-AzureRmAutomationJob</span></span>](./Get-AzureRMAutomationJob.md)

[<span data-ttu-id="5ed60-129">Get-AzureRmAutomationJobOutput</span><span class="sxs-lookup"><span data-stu-id="5ed60-129">Get-AzureRmAutomationJobOutput</span></span>](./Get-AzureRMAutomationJobOutput.md)

[<span data-ttu-id="5ed60-130">Stopp-AzureRmAutomationJob</span><span class="sxs-lookup"><span data-stu-id="5ed60-130">Stop-AzureRmAutomationJob</span></span>](./Stop-AzureRMAutomationJob.md)

[<span data-ttu-id="5ed60-131">Suspend-AzureRmAutomationJob</span><span class="sxs-lookup"><span data-stu-id="5ed60-131">Suspend-AzureRmAutomationJob</span></span>](./Suspend-AzureRMAutomationJob.md)


