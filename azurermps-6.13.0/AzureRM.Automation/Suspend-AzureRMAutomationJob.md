---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: FF44BCD2-AD8E-4F5C-AB10-BD6BD69E7F45
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/suspend-azurermautomationjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Suspend-AzureRMAutomationJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Suspend-AzureRMAutomationJob.md
ms.openlocfilehash: 0820905ff8a4673c9abae56be2f7792912095e76
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93576332"
---
# <span data-ttu-id="51ea8-101">Suspend-AzureRmAutomationJob</span><span class="sxs-lookup"><span data-stu-id="51ea8-101">Suspend-AzureRmAutomationJob</span></span>

## <span data-ttu-id="51ea8-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="51ea8-102">SYNOPSIS</span></span>
<span data-ttu-id="51ea8-103">Inaktiverar ett automatiserings jobb.</span><span class="sxs-lookup"><span data-stu-id="51ea8-103">Suspends an Automation job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="51ea8-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="51ea8-104">SYNTAX</span></span>

```
Suspend-AzureRmAutomationJob [-Id] <Guid> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="51ea8-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="51ea8-105">DESCRIPTION</span></span>
<span data-ttu-id="51ea8-106">Cmdleten **suspend-AzureRmAutomationJob** inaktive ras ett Azure Automation-jobb.</span><span class="sxs-lookup"><span data-stu-id="51ea8-106">The **Suspend-AzureRmAutomationJob** cmdlet suspends an Azure Automation job.</span></span>
<span data-ttu-id="51ea8-107">Ange ett automatiserings jobb som körs.</span><span class="sxs-lookup"><span data-stu-id="51ea8-107">Specify a running Automation job.</span></span>
<span data-ttu-id="51ea8-108">Om du vill återuppta ett avbrutet jobb kan du använda Resume-AzureRmAutomationJob cmdlet.</span><span class="sxs-lookup"><span data-stu-id="51ea8-108">To resume a suspended job, use the Resume-AzureRmAutomationJob cmdlet.</span></span>

## <span data-ttu-id="51ea8-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="51ea8-109">EXAMPLES</span></span>

### <span data-ttu-id="51ea8-110">Exempel 1: pausa ett jobb</span><span class="sxs-lookup"><span data-stu-id="51ea8-110">Example 1: Suspend a job</span></span>
```
PS C:\>Suspend-AzureRmAutomationJob -AutomationAccountName "Contoso17" -Id 2989b069-24fe-40b9-b3bd-cb7e5eac4b64 -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="51ea8-111">Det här kommandot avaktiverar det jobb som har angivet ID.</span><span class="sxs-lookup"><span data-stu-id="51ea8-111">This command suspends the job that has the specified ID.</span></span>

## <span data-ttu-id="51ea8-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="51ea8-112">PARAMETERS</span></span>

### <span data-ttu-id="51ea8-113">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="51ea8-113">-AutomationAccountName</span></span>
<span data-ttu-id="51ea8-114">Anger namnet på ett Automation-konto där denna cmdlet gör om ett jobb.</span><span class="sxs-lookup"><span data-stu-id="51ea8-114">Specifies the name of an Automation account in which this cmdlet suspends a job.</span></span>

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

### <span data-ttu-id="51ea8-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="51ea8-115">-DefaultProfile</span></span>
<span data-ttu-id="51ea8-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="51ea8-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="51ea8-117">-ID</span><span class="sxs-lookup"><span data-stu-id="51ea8-117">-Id</span></span>
<span data-ttu-id="51ea8-118">Anger ID för ett jobb som denna cmdlet inaktive ras.</span><span class="sxs-lookup"><span data-stu-id="51ea8-118">Specifies the ID of a job that this cmdlet suspends.</span></span>

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

### <span data-ttu-id="51ea8-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="51ea8-119">-ResourceGroupName</span></span>
<span data-ttu-id="51ea8-120">Anger ID för ett jobb som denna cmdlet inaktive ras.</span><span class="sxs-lookup"><span data-stu-id="51ea8-120">Specifies the ID of a job that this cmdlet suspends.</span></span>

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

### <span data-ttu-id="51ea8-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="51ea8-121">CommonParameters</span></span>
<span data-ttu-id="51ea8-122">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="51ea8-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="51ea8-123">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="51ea8-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="51ea8-124">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="51ea8-124">INPUTS</span></span>

### <span data-ttu-id="51ea8-125">System. GUID</span><span class="sxs-lookup"><span data-stu-id="51ea8-125">System.Guid</span></span>

### <span data-ttu-id="51ea8-126">System. String</span><span class="sxs-lookup"><span data-stu-id="51ea8-126">System.String</span></span>

## <span data-ttu-id="51ea8-127">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="51ea8-127">OUTPUTS</span></span>

### <span data-ttu-id="51ea8-128">System. Void</span><span class="sxs-lookup"><span data-stu-id="51ea8-128">System.Void</span></span>

## <span data-ttu-id="51ea8-129">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="51ea8-129">NOTES</span></span>

## <span data-ttu-id="51ea8-130">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="51ea8-130">RELATED LINKS</span></span>

[<span data-ttu-id="51ea8-131">Get-AzureRmAutomationJob</span><span class="sxs-lookup"><span data-stu-id="51ea8-131">Get-AzureRmAutomationJob</span></span>](./Get-AzureRMAutomationJob.md)

[<span data-ttu-id="51ea8-132">Get-AzureRmAutomationJobOutput</span><span class="sxs-lookup"><span data-stu-id="51ea8-132">Get-AzureRmAutomationJobOutput</span></span>](./Get-AzureRMAutomationJobOutput.md)

[<span data-ttu-id="51ea8-133">Resume-AzureRmAutomationJob</span><span class="sxs-lookup"><span data-stu-id="51ea8-133">Resume-AzureRmAutomationJob</span></span>](./Resume-AzureRMAutomationJob.md)

[<span data-ttu-id="51ea8-134">Stopp-AzureRmAutomationJob</span><span class="sxs-lookup"><span data-stu-id="51ea8-134">Stop-AzureRmAutomationJob</span></span>](./Stop-AzureRMAutomationJob.md)


