---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: B39C4D6B-392A-4C8D-A6FB-886DA1A2BA58
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/get-azautomationjoboutput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationJobOutput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationJobOutput.md
ms.openlocfilehash: 53ae09ba82de2a96bc9db17ad7ca538c48b23a47
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94090402"
---
# <span data-ttu-id="eaff8-101">Get-AzAutomationJobOutput</span><span class="sxs-lookup"><span data-stu-id="eaff8-101">Get-AzAutomationJobOutput</span></span>

## <span data-ttu-id="eaff8-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="eaff8-102">SYNOPSIS</span></span>
<span data-ttu-id="eaff8-103">Hämtar utdata från ett automations jobb.</span><span class="sxs-lookup"><span data-stu-id="eaff8-103">Gets the output of an Automation job.</span></span>

## <span data-ttu-id="eaff8-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="eaff8-104">SYNTAX</span></span>

```
Get-AzAutomationJobOutput [-Id] <Guid> [-Stream <StreamType>] [-StartTime <DateTimeOffset>]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="eaff8-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="eaff8-105">DESCRIPTION</span></span>
<span data-ttu-id="eaff8-106">Cmdleten **Get-AzAutomationJobOutput** hämtar utdata från ett Azure Automation-jobb.</span><span class="sxs-lookup"><span data-stu-id="eaff8-106">The **Get-AzAutomationJobOutput** cmdlet gets the output of an Azure Automation job.</span></span>

## <span data-ttu-id="eaff8-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="eaff8-107">EXAMPLES</span></span>

### <span data-ttu-id="eaff8-108">Exempel 1: få utdata från ett automations jobb</span><span class="sxs-lookup"><span data-stu-id="eaff8-108">Example 1: Get the output of an Automation job</span></span>
```
PS C:\>Get-AzAutomationJobOutput -AutomationAccountName "Contoso17" -Id 2989b069-24fe-40b9-b3bd-cb7e5eac4b64 -ResourceGroupName "ResourceGroup01" -Stream "Any"
```

<span data-ttu-id="eaff8-109">Det här kommandot får alla utdata från jobbet som har angivet ID.</span><span class="sxs-lookup"><span data-stu-id="eaff8-109">This command gets all of the output of the job that has the specified ID.</span></span>

## <span data-ttu-id="eaff8-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="eaff8-110">PARAMETERS</span></span>

### <span data-ttu-id="eaff8-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="eaff8-111">-AutomationAccountName</span></span>
<span data-ttu-id="eaff8-112">Anger namnet på ett Automation-konto för vilket denna cmdlet får jobbets utdata.</span><span class="sxs-lookup"><span data-stu-id="eaff8-112">Specifies the name of an Automation account for which this cmdlet gets job output.</span></span>

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

### <span data-ttu-id="eaff8-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eaff8-113">-DefaultProfile</span></span>
<span data-ttu-id="eaff8-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="eaff8-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="eaff8-115">-ID</span><span class="sxs-lookup"><span data-stu-id="eaff8-115">-Id</span></span>
<span data-ttu-id="eaff8-116">Anger ID för ett jobb för vilket denna cmdlet ska skriva ut.</span><span class="sxs-lookup"><span data-stu-id="eaff8-116">Specifies the ID of a job for which this cmdlet gets output.</span></span>

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

### <span data-ttu-id="eaff8-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="eaff8-117">-ResourceGroupName</span></span>
<span data-ttu-id="eaff8-118">Anger namnet på en resurs grupp för vilken denna cmdlet får jobbets utdata.</span><span class="sxs-lookup"><span data-stu-id="eaff8-118">Specifies the name of a resource group for which this cmdlet gets job output.</span></span>

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

### <span data-ttu-id="eaff8-119">-StartTime</span><span class="sxs-lookup"><span data-stu-id="eaff8-119">-StartTime</span></span>
<span data-ttu-id="eaff8-120">Anger en start tid som ett **DateTimeOffset** -objekt.</span><span class="sxs-lookup"><span data-stu-id="eaff8-120">Specifies a start time as a **DateTimeOffset** object.</span></span>
<span data-ttu-id="eaff8-121">Du kan ange en sträng som kan konverteras till en giltig **DateTimeOffset**.</span><span class="sxs-lookup"><span data-stu-id="eaff8-121">You can specify a string that can be converted to a valid **DateTimeOffset**.</span></span>
<span data-ttu-id="eaff8-122">Cmdleten hämtar utdata som skapats efter den här tiden.</span><span class="sxs-lookup"><span data-stu-id="eaff8-122">The cmdlet retrieves output created after this time.</span></span>

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

### <span data-ttu-id="eaff8-123">-Stream</span><span class="sxs-lookup"><span data-stu-id="eaff8-123">-Stream</span></span>
<span data-ttu-id="eaff8-124">Anger typen av utdata.</span><span class="sxs-lookup"><span data-stu-id="eaff8-124">Specifies the type of output.</span></span>
<span data-ttu-id="eaff8-125">Giltiga värden är:</span><span class="sxs-lookup"><span data-stu-id="eaff8-125">Valid values are:</span></span> 
- <span data-ttu-id="eaff8-126">Eventuell</span><span class="sxs-lookup"><span data-stu-id="eaff8-126">Any</span></span>
- <span data-ttu-id="eaff8-127">Verk</span><span class="sxs-lookup"><span data-stu-id="eaff8-127">Debug</span></span>
- <span data-ttu-id="eaff8-128">Synkroniseringsfel</span><span class="sxs-lookup"><span data-stu-id="eaff8-128">Error</span></span>
- <span data-ttu-id="eaff8-129">Skriva</span><span class="sxs-lookup"><span data-stu-id="eaff8-129">Output</span></span>
- <span data-ttu-id="eaff8-130">Status</span><span class="sxs-lookup"><span data-stu-id="eaff8-130">Progress</span></span>
- <span data-ttu-id="eaff8-131">Utförlig</span><span class="sxs-lookup"><span data-stu-id="eaff8-131">Verbose</span></span>
- <span data-ttu-id="eaff8-132">Meddelandet</span><span class="sxs-lookup"><span data-stu-id="eaff8-132">Warning</span></span>

```yaml
Type: Microsoft.Azure.Commands.Automation.Common.StreamType
Parameter Sets: (All)
Aliases:
Accepted values: Any, Progress, Output, Warning, Error, Verbose

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="eaff8-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eaff8-133">CommonParameters</span></span>
<span data-ttu-id="eaff8-134">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="eaff8-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eaff8-135">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="eaff8-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eaff8-136">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="eaff8-136">INPUTS</span></span>

### <span data-ttu-id="eaff8-137">System. GUID</span><span class="sxs-lookup"><span data-stu-id="eaff8-137">System.Guid</span></span>

### <span data-ttu-id="eaff8-138">Microsoft. Azure. commands. Automation. Common. StreamType</span><span class="sxs-lookup"><span data-stu-id="eaff8-138">Microsoft.Azure.Commands.Automation.Common.StreamType</span></span>

### <span data-ttu-id="eaff8-139">System. Nullable ' 1 [[system. DateTimeOffset, system. Private. CoreLib, version = 4.0.0.0, Culture = neutralt, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="eaff8-139">System.Nullable\`1[[System.DateTimeOffset, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="eaff8-140">System. String</span><span class="sxs-lookup"><span data-stu-id="eaff8-140">System.String</span></span>

## <span data-ttu-id="eaff8-141">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="eaff8-141">OUTPUTS</span></span>

### <span data-ttu-id="eaff8-142">Microsoft. Azure. commands. Automation. Model. JobStream</span><span class="sxs-lookup"><span data-stu-id="eaff8-142">Microsoft.Azure.Commands.Automation.Model.JobStream</span></span>

## <span data-ttu-id="eaff8-143">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="eaff8-143">NOTES</span></span>

## <span data-ttu-id="eaff8-144">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="eaff8-144">RELATED LINKS</span></span>

[<span data-ttu-id="eaff8-145">Get-AzAutomationJob</span><span class="sxs-lookup"><span data-stu-id="eaff8-145">Get-AzAutomationJob</span></span>](./Get-AzAutomationJob.md)

[<span data-ttu-id="eaff8-146">Resume-AzAutomationJob</span><span class="sxs-lookup"><span data-stu-id="eaff8-146">Resume-AzAutomationJob</span></span>](./Resume-AzAutomationJob.md)

[<span data-ttu-id="eaff8-147">Stopp-AzAutomationJob</span><span class="sxs-lookup"><span data-stu-id="eaff8-147">Stop-AzAutomationJob</span></span>](./Stop-AzAutomationJob.md)

[<span data-ttu-id="eaff8-148">Suspend-AzAutomationJob</span><span class="sxs-lookup"><span data-stu-id="eaff8-148">Suspend-AzAutomationJob</span></span>](./Suspend-AzAutomationJob.md)


