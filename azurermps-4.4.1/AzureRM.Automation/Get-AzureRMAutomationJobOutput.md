---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: B39C4D6B-392A-4C8D-A6FB-886DA1A2BA58
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRMAutomationJobOutput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRMAutomationJobOutput.md
ms.openlocfilehash: dd80c745c99c98d6ea5b551ab454661d4370cebd
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93758299"
---
# <span data-ttu-id="523b0-101">Get-AzureRmAutomationJobOutput</span><span class="sxs-lookup"><span data-stu-id="523b0-101">Get-AzureRmAutomationJobOutput</span></span>

## <span data-ttu-id="523b0-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="523b0-102">SYNOPSIS</span></span>
<span data-ttu-id="523b0-103">Hämtar utdata från ett automations jobb.</span><span class="sxs-lookup"><span data-stu-id="523b0-103">Gets the output of an Automation job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="523b0-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="523b0-104">SYNTAX</span></span>

```
Get-AzureRmAutomationJobOutput [-Id] <Guid> [-Stream <StreamType>] [-StartTime <DateTimeOffset>]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="523b0-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="523b0-105">DESCRIPTION</span></span>
<span data-ttu-id="523b0-106">Cmdleten **Get-AzureRmAutomationJobOutput** hämtar utdata från ett Azure Automation-jobb.</span><span class="sxs-lookup"><span data-stu-id="523b0-106">The **Get-AzureRmAutomationJobOutput** cmdlet gets the output of an Azure Automation job.</span></span>

## <span data-ttu-id="523b0-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="523b0-107">EXAMPLES</span></span>

### <span data-ttu-id="523b0-108">Exempel 1: få utdata från ett automations jobb</span><span class="sxs-lookup"><span data-stu-id="523b0-108">Example 1: Get the output of an Automation job</span></span>
```
PS C:\>Get-AzureRmAutomationJobOutput -AutomationAccountName "Contoso17" -Id 2989b069-24fe-40b9-b3bd-cb7e5eac4b64 -ResourceGroupName "ResourceGroup01" -Stream "Any"
```

<span data-ttu-id="523b0-109">Det här kommandot får alla utdata från jobbet som har angivet ID.</span><span class="sxs-lookup"><span data-stu-id="523b0-109">This command gets all of the output of the job that has the specified ID.</span></span>

## <span data-ttu-id="523b0-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="523b0-110">PARAMETERS</span></span>

### <span data-ttu-id="523b0-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="523b0-111">-AutomationAccountName</span></span>
<span data-ttu-id="523b0-112">Anger namnet på ett Automation-konto för vilket denna cmdlet får jobbets utdata.</span><span class="sxs-lookup"><span data-stu-id="523b0-112">Specifies the name of an Automation account for which this cmdlet gets job output.</span></span>

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

### <span data-ttu-id="523b0-113">-ID</span><span class="sxs-lookup"><span data-stu-id="523b0-113">-Id</span></span>
<span data-ttu-id="523b0-114">Anger ID för ett jobb för vilket denna cmdlet ska skriva ut.</span><span class="sxs-lookup"><span data-stu-id="523b0-114">Specifies the ID of a job for which this cmdlet gets output.</span></span>

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

### <span data-ttu-id="523b0-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="523b0-115">-ResourceGroupName</span></span>
<span data-ttu-id="523b0-116">Anger namnet på en resurs grupp för vilken denna cmdlet får jobbets utdata.</span><span class="sxs-lookup"><span data-stu-id="523b0-116">Specifies the name of a resource group for which this cmdlet gets job output.</span></span>

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

### <span data-ttu-id="523b0-117">-StartTime</span><span class="sxs-lookup"><span data-stu-id="523b0-117">-StartTime</span></span>
<span data-ttu-id="523b0-118">Anger en start tid som ett **DateTimeOffset** -objekt.</span><span class="sxs-lookup"><span data-stu-id="523b0-118">Specifies a start time as a **DateTimeOffset** object.</span></span>
<span data-ttu-id="523b0-119">Du kan ange en sträng som kan konverteras till en giltig **DateTimeOffset**.</span><span class="sxs-lookup"><span data-stu-id="523b0-119">You can specify a string that can be converted to a valid **DateTimeOffset**.</span></span>
<span data-ttu-id="523b0-120">Cmdleten hämtar utdata som skapats efter den här tiden.</span><span class="sxs-lookup"><span data-stu-id="523b0-120">The cmdlet retrieves output created after this time.</span></span>

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

### <span data-ttu-id="523b0-121">-Stream</span><span class="sxs-lookup"><span data-stu-id="523b0-121">-Stream</span></span>
<span data-ttu-id="523b0-122">Anger typen av utdata.</span><span class="sxs-lookup"><span data-stu-id="523b0-122">Specifies the type of output.</span></span>
<span data-ttu-id="523b0-123">Giltiga värden är:</span><span class="sxs-lookup"><span data-stu-id="523b0-123">Valid values are:</span></span> 

- <span data-ttu-id="523b0-124">Eventuell</span><span class="sxs-lookup"><span data-stu-id="523b0-124">Any</span></span>
- <span data-ttu-id="523b0-125">Verk</span><span class="sxs-lookup"><span data-stu-id="523b0-125">Debug</span></span>
- <span data-ttu-id="523b0-126">Synkroniseringsfel</span><span class="sxs-lookup"><span data-stu-id="523b0-126">Error</span></span>
- <span data-ttu-id="523b0-127">Skriva</span><span class="sxs-lookup"><span data-stu-id="523b0-127">Output</span></span>
- <span data-ttu-id="523b0-128">Status</span><span class="sxs-lookup"><span data-stu-id="523b0-128">Progress</span></span>
- <span data-ttu-id="523b0-129">Utförlig</span><span class="sxs-lookup"><span data-stu-id="523b0-129">Verbose</span></span>
- <span data-ttu-id="523b0-130">Meddelandet</span><span class="sxs-lookup"><span data-stu-id="523b0-130">Warning</span></span>

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

### <span data-ttu-id="523b0-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="523b0-131">-DefaultProfile</span></span>
<span data-ttu-id="523b0-132">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="523b0-132">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="523b0-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="523b0-133">CommonParameters</span></span>
<span data-ttu-id="523b0-134">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="523b0-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="523b0-135">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="523b0-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="523b0-136">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="523b0-136">INPUTS</span></span>

## <span data-ttu-id="523b0-137">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="523b0-137">OUTPUTS</span></span>

### <span data-ttu-id="523b0-138">Microsoft. Azure. commands. Automation. Model. JobStream</span><span class="sxs-lookup"><span data-stu-id="523b0-138">Microsoft.Azure.Commands.Automation.Model.JobStream</span></span>

## <span data-ttu-id="523b0-139">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="523b0-139">NOTES</span></span>

## <span data-ttu-id="523b0-140">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="523b0-140">RELATED LINKS</span></span>

[<span data-ttu-id="523b0-141">Get-AzureRmAutomationJob</span><span class="sxs-lookup"><span data-stu-id="523b0-141">Get-AzureRmAutomationJob</span></span>](./Get-AzureRMAutomationJob.md)

[<span data-ttu-id="523b0-142">Resume-AzureRmAutomationJob</span><span class="sxs-lookup"><span data-stu-id="523b0-142">Resume-AzureRmAutomationJob</span></span>](./Resume-AzureRMAutomationJob.md)

[<span data-ttu-id="523b0-143">Stopp-AzureRmAutomationJob</span><span class="sxs-lookup"><span data-stu-id="523b0-143">Stop-AzureRmAutomationJob</span></span>](./Stop-AzureRMAutomationJob.md)

[<span data-ttu-id="523b0-144">Suspend-AzureRmAutomationJob</span><span class="sxs-lookup"><span data-stu-id="523b0-144">Suspend-AzureRmAutomationJob</span></span>](./Suspend-AzureRMAutomationJob.md)


