---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: FF44BCD2-AD8E-4F5C-AB10-BD6BD69E7F45
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/suspend-azautomationjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Suspend-AzAutomationJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Suspend-AzAutomationJob.md
ms.openlocfilehash: 3aecdb18579f46722a73e3de538f5f3c929b606f
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94092380"
---
# <span data-ttu-id="1c748-101">Suspend-AzAutomationJob</span><span class="sxs-lookup"><span data-stu-id="1c748-101">Suspend-AzAutomationJob</span></span>

## <span data-ttu-id="1c748-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="1c748-102">SYNOPSIS</span></span>
<span data-ttu-id="1c748-103">Inaktiverar ett automatiserings jobb.</span><span class="sxs-lookup"><span data-stu-id="1c748-103">Suspends an Automation job.</span></span>

## <span data-ttu-id="1c748-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="1c748-104">SYNTAX</span></span>

```
Suspend-AzAutomationJob [-Id] <Guid> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1c748-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="1c748-105">DESCRIPTION</span></span>
<span data-ttu-id="1c748-106">Cmdleten **suspend-AzAutomationJob** inaktive ras ett Azure Automation-jobb.</span><span class="sxs-lookup"><span data-stu-id="1c748-106">The **Suspend-AzAutomationJob** cmdlet suspends an Azure Automation job.</span></span>
<span data-ttu-id="1c748-107">Ange ett automatiserings jobb som körs.</span><span class="sxs-lookup"><span data-stu-id="1c748-107">Specify a running Automation job.</span></span>
<span data-ttu-id="1c748-108">Om du vill återuppta ett avbrutet jobb kan du använda Resume-AzAutomationJob cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1c748-108">To resume a suspended job, use the Resume-AzAutomationJob cmdlet.</span></span>

## <span data-ttu-id="1c748-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="1c748-109">EXAMPLES</span></span>

### <span data-ttu-id="1c748-110">Exempel 1: pausa ett jobb</span><span class="sxs-lookup"><span data-stu-id="1c748-110">Example 1: Suspend a job</span></span>
```
PS C:\>Suspend-AzAutomationJob -AutomationAccountName "Contoso17" -Id 2989b069-24fe-40b9-b3bd-cb7e5eac4b64 -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="1c748-111">Det här kommandot avaktiverar det jobb som har angivet ID.</span><span class="sxs-lookup"><span data-stu-id="1c748-111">This command suspends the job that has the specified ID.</span></span>

## <span data-ttu-id="1c748-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="1c748-112">PARAMETERS</span></span>

### <span data-ttu-id="1c748-113">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="1c748-113">-AutomationAccountName</span></span>
<span data-ttu-id="1c748-114">Anger namnet på ett Automation-konto där denna cmdlet gör om ett jobb.</span><span class="sxs-lookup"><span data-stu-id="1c748-114">Specifies the name of an Automation account in which this cmdlet suspends a job.</span></span>

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

### <span data-ttu-id="1c748-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1c748-115">-DefaultProfile</span></span>
<span data-ttu-id="1c748-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="1c748-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="1c748-117">-ID</span><span class="sxs-lookup"><span data-stu-id="1c748-117">-Id</span></span>
<span data-ttu-id="1c748-118">Anger ID för ett jobb som denna cmdlet inaktive ras.</span><span class="sxs-lookup"><span data-stu-id="1c748-118">Specifies the ID of a job that this cmdlet suspends.</span></span>

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

### <span data-ttu-id="1c748-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1c748-119">-ResourceGroupName</span></span>
<span data-ttu-id="1c748-120">Anger ID för ett jobb som denna cmdlet inaktive ras.</span><span class="sxs-lookup"><span data-stu-id="1c748-120">Specifies the ID of a job that this cmdlet suspends.</span></span>

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

### <span data-ttu-id="1c748-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1c748-121">CommonParameters</span></span>
<span data-ttu-id="1c748-122">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1c748-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1c748-123">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1c748-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1c748-124">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="1c748-124">INPUTS</span></span>

### <span data-ttu-id="1c748-125">System. GUID</span><span class="sxs-lookup"><span data-stu-id="1c748-125">System.Guid</span></span>

### <span data-ttu-id="1c748-126">System. String</span><span class="sxs-lookup"><span data-stu-id="1c748-126">System.String</span></span>

## <span data-ttu-id="1c748-127">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="1c748-127">OUTPUTS</span></span>

### <span data-ttu-id="1c748-128">System. Void</span><span class="sxs-lookup"><span data-stu-id="1c748-128">System.Void</span></span>

## <span data-ttu-id="1c748-129">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="1c748-129">NOTES</span></span>

## <span data-ttu-id="1c748-130">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="1c748-130">RELATED LINKS</span></span>

[<span data-ttu-id="1c748-131">Get-AzAutomationJob</span><span class="sxs-lookup"><span data-stu-id="1c748-131">Get-AzAutomationJob</span></span>](./Get-AzAutomationJob.md)

[<span data-ttu-id="1c748-132">Get-AzAutomationJobOutput</span><span class="sxs-lookup"><span data-stu-id="1c748-132">Get-AzAutomationJobOutput</span></span>](./Get-AzAutomationJobOutput.md)

[<span data-ttu-id="1c748-133">Resume-AzAutomationJob</span><span class="sxs-lookup"><span data-stu-id="1c748-133">Resume-AzAutomationJob</span></span>](./Resume-AzAutomationJob.md)

[<span data-ttu-id="1c748-134">Stopp-AzAutomationJob</span><span class="sxs-lookup"><span data-stu-id="1c748-134">Stop-AzAutomationJob</span></span>](./Stop-AzAutomationJob.md)


