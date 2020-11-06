---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: BE1A9247-9F8E-45EA-9590-684A5A5662AC
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/stop-azurermautomationjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Stop-AzureRMAutomationJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Stop-AzureRMAutomationJob.md
ms.openlocfilehash: 0eedf88ed078c3532eb60a00b87733937344bafa
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93575729"
---
# <span data-ttu-id="56ed7-101">Stop-AzureRmAutomationJob</span><span class="sxs-lookup"><span data-stu-id="56ed7-101">Stop-AzureRmAutomationJob</span></span>

## <span data-ttu-id="56ed7-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="56ed7-102">SYNOPSIS</span></span>
<span data-ttu-id="56ed7-103">Stoppar ett automatiserings jobb.</span><span class="sxs-lookup"><span data-stu-id="56ed7-103">Stops an Automation job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="56ed7-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="56ed7-104">SYNTAX</span></span>

```
Stop-AzureRmAutomationJob [-Id] <Guid> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="56ed7-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="56ed7-105">DESCRIPTION</span></span>
<span data-ttu-id="56ed7-106">Cmdleten **Stop-AzureRmAutomationJob** stoppar ett Azure Automation-jobb.</span><span class="sxs-lookup"><span data-stu-id="56ed7-106">The **Stop-AzureRmAutomationJob** cmdlet stops an Azure Automation job.</span></span>
<span data-ttu-id="56ed7-107">Ange ett automatiserings jobb som körs.</span><span class="sxs-lookup"><span data-stu-id="56ed7-107">Specify a running Automation job.</span></span>

## <span data-ttu-id="56ed7-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="56ed7-108">EXAMPLES</span></span>

### <span data-ttu-id="56ed7-109">Exempel 1: stoppa ett jobb</span><span class="sxs-lookup"><span data-stu-id="56ed7-109">Example 1: Stop a job</span></span>
```
PS C:\>Stop-AzureRmAutomationJob -AutomationAccountName "Contoso17" -Id 2989b069-24fe-40b9-b3bd-cb7e5eac4b64 -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="56ed7-110">Det här kommandot stoppar det jobb som har angivet ID.</span><span class="sxs-lookup"><span data-stu-id="56ed7-110">This command stops the job that has the specified ID.</span></span>

## <span data-ttu-id="56ed7-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="56ed7-111">PARAMETERS</span></span>

### <span data-ttu-id="56ed7-112">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="56ed7-112">-AutomationAccountName</span></span>
<span data-ttu-id="56ed7-113">Anger namnet på ett Automation-konto där denna cmdlet stoppar ett jobb.</span><span class="sxs-lookup"><span data-stu-id="56ed7-113">Specifies the name of an Automation account in which this cmdlet stops a job.</span></span>

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

### <span data-ttu-id="56ed7-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="56ed7-114">-DefaultProfile</span></span>
<span data-ttu-id="56ed7-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="56ed7-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="56ed7-116">-ID</span><span class="sxs-lookup"><span data-stu-id="56ed7-116">-Id</span></span>
<span data-ttu-id="56ed7-117">Anger ID för ett jobb som denna cmdlet stoppar.</span><span class="sxs-lookup"><span data-stu-id="56ed7-117">Specifies the ID of a job that this cmdlet stops.</span></span>

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

### <span data-ttu-id="56ed7-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="56ed7-118">-ResourceGroupName</span></span>
<span data-ttu-id="56ed7-119">Anger namnet på en resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="56ed7-119">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="56ed7-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="56ed7-120">CommonParameters</span></span>
<span data-ttu-id="56ed7-121">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="56ed7-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="56ed7-122">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="56ed7-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="56ed7-123">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="56ed7-123">INPUTS</span></span>

### <span data-ttu-id="56ed7-124">Ingen</span><span class="sxs-lookup"><span data-stu-id="56ed7-124">None</span></span>
<span data-ttu-id="56ed7-125">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="56ed7-125">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="56ed7-126">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="56ed7-126">OUTPUTS</span></span>

## <span data-ttu-id="56ed7-127">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="56ed7-127">NOTES</span></span>

## <span data-ttu-id="56ed7-128">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="56ed7-128">RELATED LINKS</span></span>

[<span data-ttu-id="56ed7-129">Get-AzureRmAutomationJob</span><span class="sxs-lookup"><span data-stu-id="56ed7-129">Get-AzureRmAutomationJob</span></span>](./Get-AzureRMAutomationJob.md)

[<span data-ttu-id="56ed7-130">Get-AzureRmAutomationJobOutput</span><span class="sxs-lookup"><span data-stu-id="56ed7-130">Get-AzureRmAutomationJobOutput</span></span>](./Get-AzureRMAutomationJobOutput.md)

[<span data-ttu-id="56ed7-131">Resume-AzureRmAutomationJob</span><span class="sxs-lookup"><span data-stu-id="56ed7-131">Resume-AzureRmAutomationJob</span></span>](./Resume-AzureRMAutomationJob.md)

[<span data-ttu-id="56ed7-132">Suspend-AzureRmAutomationJob</span><span class="sxs-lookup"><span data-stu-id="56ed7-132">Suspend-AzureRmAutomationJob</span></span>](./Suspend-AzureRMAutomationJob.md)


