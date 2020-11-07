---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: FF44BCD2-AD8E-4F5C-AB10-BD6BD69E7F45
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Suspend-AzureRMAutomationJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Suspend-AzureRMAutomationJob.md
ms.openlocfilehash: cc9f402400b0290d8cf36dc38d59a45e29ce770c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93757503"
---
# <span data-ttu-id="9994e-101">Suspend-AzureRmAutomationJob</span><span class="sxs-lookup"><span data-stu-id="9994e-101">Suspend-AzureRmAutomationJob</span></span>

## <span data-ttu-id="9994e-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="9994e-102">SYNOPSIS</span></span>
<span data-ttu-id="9994e-103">Inaktiverar ett automatiserings jobb.</span><span class="sxs-lookup"><span data-stu-id="9994e-103">Suspends an Automation job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9994e-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="9994e-104">SYNTAX</span></span>

```
Suspend-AzureRmAutomationJob [-Id] <Guid> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9994e-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="9994e-105">DESCRIPTION</span></span>
<span data-ttu-id="9994e-106">Cmdleten **suspend-AzureRmAutomationJob** inaktive ras ett Azure Automation-jobb.</span><span class="sxs-lookup"><span data-stu-id="9994e-106">The **Suspend-AzureRmAutomationJob** cmdlet suspends an Azure Automation job.</span></span>
<span data-ttu-id="9994e-107">Ange ett automatiserings jobb som körs.</span><span class="sxs-lookup"><span data-stu-id="9994e-107">Specify a running Automation job.</span></span>

<span data-ttu-id="9994e-108">Om du vill återuppta ett avbrutet jobb kan du använda Resume-AzureRmAutomationJob cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9994e-108">To resume a suspended job, use the Resume-AzureRmAutomationJob cmdlet.</span></span>

## <span data-ttu-id="9994e-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="9994e-109">EXAMPLES</span></span>

### <span data-ttu-id="9994e-110">Exempel 1: pausa ett jobb</span><span class="sxs-lookup"><span data-stu-id="9994e-110">Example 1: Suspend a job</span></span>
```
PS C:\>Suspend-AzureRmAutomationJob -AutomationAccountName "Contoso17" -Id 2989b069-24fe-40b9-b3bd-cb7e5eac4b64 -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="9994e-111">Det här kommandot avaktiverar det jobb som har angivet ID.</span><span class="sxs-lookup"><span data-stu-id="9994e-111">This command suspends the job that has the specified ID.</span></span>

## <span data-ttu-id="9994e-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="9994e-112">PARAMETERS</span></span>

### <span data-ttu-id="9994e-113">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="9994e-113">-AutomationAccountName</span></span>
<span data-ttu-id="9994e-114">Anger namnet på ett Automation-konto där denna cmdlet gör om ett jobb.</span><span class="sxs-lookup"><span data-stu-id="9994e-114">Specifies the name of an Automation account in which this cmdlet suspends a job.</span></span>

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

### <span data-ttu-id="9994e-115">-ID</span><span class="sxs-lookup"><span data-stu-id="9994e-115">-Id</span></span>
<span data-ttu-id="9994e-116">Anger ID för ett jobb som denna cmdlet inaktive ras.</span><span class="sxs-lookup"><span data-stu-id="9994e-116">Specifies the ID of a job that this cmdlet suspends.</span></span>

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

### <span data-ttu-id="9994e-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9994e-117">-ResourceGroupName</span></span>
<span data-ttu-id="9994e-118">Anger ID för ett jobb som denna cmdlet inaktive ras.</span><span class="sxs-lookup"><span data-stu-id="9994e-118">Specifies the ID of a job that this cmdlet suspends.</span></span>

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

### <span data-ttu-id="9994e-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9994e-119">-DefaultProfile</span></span>
<span data-ttu-id="9994e-120">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="9994e-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9994e-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9994e-121">CommonParameters</span></span>
<span data-ttu-id="9994e-122">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9994e-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9994e-123">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9994e-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9994e-124">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="9994e-124">INPUTS</span></span>

## <span data-ttu-id="9994e-125">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="9994e-125">OUTPUTS</span></span>

## <span data-ttu-id="9994e-126">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="9994e-126">NOTES</span></span>

## <span data-ttu-id="9994e-127">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="9994e-127">RELATED LINKS</span></span>

[<span data-ttu-id="9994e-128">Get-AzureRmAutomationJob</span><span class="sxs-lookup"><span data-stu-id="9994e-128">Get-AzureRmAutomationJob</span></span>](./Get-AzureRMAutomationJob.md)

[<span data-ttu-id="9994e-129">Get-AzureRmAutomationJobOutput</span><span class="sxs-lookup"><span data-stu-id="9994e-129">Get-AzureRmAutomationJobOutput</span></span>](./Get-AzureRMAutomationJobOutput.md)

[<span data-ttu-id="9994e-130">Resume-AzureRmAutomationJob</span><span class="sxs-lookup"><span data-stu-id="9994e-130">Resume-AzureRmAutomationJob</span></span>](./Resume-AzureRMAutomationJob.md)

[<span data-ttu-id="9994e-131">Stopp-AzureRmAutomationJob</span><span class="sxs-lookup"><span data-stu-id="9994e-131">Stop-AzureRmAutomationJob</span></span>](./Stop-AzureRMAutomationJob.md)


