---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: B39C4D6B-392A-4C8D-A6FB-886DA1A2BA58
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/get-azurermautomationjoboutput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRMAutomationJobOutput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRMAutomationJobOutput.md
ms.openlocfilehash: e2b965800c4f8307edaedf25b032767ca1784049
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93582848"
---
# <span data-ttu-id="c135e-101">Get-AzureRmAutomationJobOutput</span><span class="sxs-lookup"><span data-stu-id="c135e-101">Get-AzureRmAutomationJobOutput</span></span>

## <span data-ttu-id="c135e-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="c135e-102">SYNOPSIS</span></span>
<span data-ttu-id="c135e-103">Hämtar utdata från ett automations jobb.</span><span class="sxs-lookup"><span data-stu-id="c135e-103">Gets the output of an Automation job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c135e-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="c135e-104">SYNTAX</span></span>

```
Get-AzureRmAutomationJobOutput [-Id] <Guid> [-Stream <StreamType>] [-StartTime <DateTimeOffset>]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="c135e-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="c135e-105">DESCRIPTION</span></span>
<span data-ttu-id="c135e-106">Cmdleten **Get-AzureRmAutomationJobOutput** hämtar utdata från ett Azure Automation-jobb.</span><span class="sxs-lookup"><span data-stu-id="c135e-106">The **Get-AzureRmAutomationJobOutput** cmdlet gets the output of an Azure Automation job.</span></span>

## <span data-ttu-id="c135e-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="c135e-107">EXAMPLES</span></span>

### <span data-ttu-id="c135e-108">Exempel 1: få utdata från ett automations jobb</span><span class="sxs-lookup"><span data-stu-id="c135e-108">Example 1: Get the output of an Automation job</span></span>
```
PS C:\>Get-AzureRmAutomationJobOutput -AutomationAccountName "Contoso17" -Id 2989b069-24fe-40b9-b3bd-cb7e5eac4b64 -ResourceGroupName "ResourceGroup01" -Stream "Any"
```

<span data-ttu-id="c135e-109">Det här kommandot får alla utdata från jobbet som har angivet ID.</span><span class="sxs-lookup"><span data-stu-id="c135e-109">This command gets all of the output of the job that has the specified ID.</span></span>

## <span data-ttu-id="c135e-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="c135e-110">PARAMETERS</span></span>

### <span data-ttu-id="c135e-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="c135e-111">-AutomationAccountName</span></span>
<span data-ttu-id="c135e-112">Anger namnet på ett Automation-konto för vilket denna cmdlet får jobbets utdata.</span><span class="sxs-lookup"><span data-stu-id="c135e-112">Specifies the name of an Automation account for which this cmdlet gets job output.</span></span>

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

### <span data-ttu-id="c135e-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c135e-113">-DefaultProfile</span></span>
<span data-ttu-id="c135e-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="c135e-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c135e-115">-ID</span><span class="sxs-lookup"><span data-stu-id="c135e-115">-Id</span></span>
<span data-ttu-id="c135e-116">Anger ID för ett jobb för vilket denna cmdlet ska skriva ut.</span><span class="sxs-lookup"><span data-stu-id="c135e-116">Specifies the ID of a job for which this cmdlet gets output.</span></span>

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

### <span data-ttu-id="c135e-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c135e-117">-ResourceGroupName</span></span>
<span data-ttu-id="c135e-118">Anger namnet på en resurs grupp för vilken denna cmdlet får jobbets utdata.</span><span class="sxs-lookup"><span data-stu-id="c135e-118">Specifies the name of a resource group for which this cmdlet gets job output.</span></span>

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

### <span data-ttu-id="c135e-119">-StartTime</span><span class="sxs-lookup"><span data-stu-id="c135e-119">-StartTime</span></span>
<span data-ttu-id="c135e-120">Anger en start tid som ett **DateTimeOffset** -objekt.</span><span class="sxs-lookup"><span data-stu-id="c135e-120">Specifies a start time as a **DateTimeOffset** object.</span></span>
<span data-ttu-id="c135e-121">Du kan ange en sträng som kan konverteras till en giltig **DateTimeOffset**.</span><span class="sxs-lookup"><span data-stu-id="c135e-121">You can specify a string that can be converted to a valid **DateTimeOffset**.</span></span>
<span data-ttu-id="c135e-122">Cmdleten hämtar utdata som skapats efter den här tiden.</span><span class="sxs-lookup"><span data-stu-id="c135e-122">The cmdlet retrieves output created after this time.</span></span>

```yaml
Type: System.Nullable`1[System.DateTimeOffset]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c135e-123">-Stream</span><span class="sxs-lookup"><span data-stu-id="c135e-123">-Stream</span></span>
<span data-ttu-id="c135e-124">Anger typen av utdata.</span><span class="sxs-lookup"><span data-stu-id="c135e-124">Specifies the type of output.</span></span>
<span data-ttu-id="c135e-125">Giltiga värden är:</span><span class="sxs-lookup"><span data-stu-id="c135e-125">Valid values are:</span></span> 
- <span data-ttu-id="c135e-126">Eventuell</span><span class="sxs-lookup"><span data-stu-id="c135e-126">Any</span></span>
- <span data-ttu-id="c135e-127">Verk</span><span class="sxs-lookup"><span data-stu-id="c135e-127">Debug</span></span>
- <span data-ttu-id="c135e-128">Synkroniseringsfel</span><span class="sxs-lookup"><span data-stu-id="c135e-128">Error</span></span>
- <span data-ttu-id="c135e-129">Skriva</span><span class="sxs-lookup"><span data-stu-id="c135e-129">Output</span></span>
- <span data-ttu-id="c135e-130">Status</span><span class="sxs-lookup"><span data-stu-id="c135e-130">Progress</span></span>
- <span data-ttu-id="c135e-131">Utförlig</span><span class="sxs-lookup"><span data-stu-id="c135e-131">Verbose</span></span>
- <span data-ttu-id="c135e-132">Meddelandet</span><span class="sxs-lookup"><span data-stu-id="c135e-132">Warning</span></span>

```yaml
Type: Microsoft.Azure.Commands.Automation.Common.StreamType
Parameter Sets: (All)
Aliases:
Accepted values: Any, Progress, Output, Warning, Error, Debug, Verbose

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c135e-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c135e-133">CommonParameters</span></span>
<span data-ttu-id="c135e-134">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c135e-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c135e-135">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c135e-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c135e-136">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="c135e-136">INPUTS</span></span>

### <span data-ttu-id="c135e-137">System. GUID</span><span class="sxs-lookup"><span data-stu-id="c135e-137">System.Guid</span></span>

### <span data-ttu-id="c135e-138">Microsoft. Azure. commands. Automation. Common. StreamType</span><span class="sxs-lookup"><span data-stu-id="c135e-138">Microsoft.Azure.Commands.Automation.Common.StreamType</span></span>

### <span data-ttu-id="c135e-139">System. Nullable ' 1 [[system. DateTimeOffset, mscorlib, version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="c135e-139">System.Nullable\`1[[System.DateTimeOffset, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

### <span data-ttu-id="c135e-140">System. String</span><span class="sxs-lookup"><span data-stu-id="c135e-140">System.String</span></span>

## <span data-ttu-id="c135e-141">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="c135e-141">OUTPUTS</span></span>

### <span data-ttu-id="c135e-142">Microsoft. Azure. commands. Automation. Model. JobStream</span><span class="sxs-lookup"><span data-stu-id="c135e-142">Microsoft.Azure.Commands.Automation.Model.JobStream</span></span>

## <span data-ttu-id="c135e-143">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="c135e-143">NOTES</span></span>

## <span data-ttu-id="c135e-144">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="c135e-144">RELATED LINKS</span></span>

[<span data-ttu-id="c135e-145">Get-AzureRmAutomationJob</span><span class="sxs-lookup"><span data-stu-id="c135e-145">Get-AzureRmAutomationJob</span></span>](./Get-AzureRMAutomationJob.md)

[<span data-ttu-id="c135e-146">Resume-AzureRmAutomationJob</span><span class="sxs-lookup"><span data-stu-id="c135e-146">Resume-AzureRmAutomationJob</span></span>](./Resume-AzureRMAutomationJob.md)

[<span data-ttu-id="c135e-147">Stopp-AzureRmAutomationJob</span><span class="sxs-lookup"><span data-stu-id="c135e-147">Stop-AzureRmAutomationJob</span></span>](./Stop-AzureRMAutomationJob.md)

[<span data-ttu-id="c135e-148">Suspend-AzureRmAutomationJob</span><span class="sxs-lookup"><span data-stu-id="c135e-148">Suspend-AzureRmAutomationJob</span></span>](./Suspend-AzureRMAutomationJob.md)


