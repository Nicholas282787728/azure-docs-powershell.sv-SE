---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/get-azurermautomationsourcecontrolsyncjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRmAutomationSourceControlSyncJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRmAutomationSourceControlSyncJob.md
ms.openlocfilehash: 213df264e4ecd458c8505d521556f49265577333
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93581795"
---
# <span data-ttu-id="2561f-101">Get-AzureRmAutomationSourceControlSyncJob</span><span class="sxs-lookup"><span data-stu-id="2561f-101">Get-AzureRmAutomationSourceControlSyncJob</span></span>

## <span data-ttu-id="2561f-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="2561f-102">SYNOPSIS</span></span>
<span data-ttu-id="2561f-103">Hämtar synkroniseringsjobb för Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="2561f-103">Gets Azure Automation source control sync jobs.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2561f-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="2561f-104">SYNTAX</span></span>

```
Get-AzureRmAutomationSourceControlSyncJob -SourceControlName <String> [-JobId <Guid>]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="2561f-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="2561f-105">DESCRIPTION</span></span>
<span data-ttu-id="2561f-106">Get-AzureRmAutomationSourceControlSyncJob cmdlet får synkroniseringsjobb för Azure Automation Source Control.</span><span class="sxs-lookup"><span data-stu-id="2561f-106">The Get-AzureRmAutomationSourceControlSyncJob cmdlet gets Azure Automation source control sync jobs.</span></span> <span data-ttu-id="2561f-107">Om du vill hämta ett specifikt synkroniseringsjobb för käll kontroll anger du dess ID.</span><span class="sxs-lookup"><span data-stu-id="2561f-107">To get a specific source control sync job, specify its id.</span></span>

## <span data-ttu-id="2561f-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="2561f-108">EXAMPLES</span></span>

### <span data-ttu-id="2561f-109">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="2561f-109">Example 1</span></span>
<span data-ttu-id="2561f-110">Det här kommandot får alla synkroniseringsjobb för VSTSNative käll kontroll.</span><span class="sxs-lookup"><span data-stu-id="2561f-110">This command gets all the Automation source control sync jobs for the source control VSTSNative.</span></span>


```powershell
PS C:\> Get-AzureRmAutomationSourceControlSyncJob -ResourceGroupName "rg1" `
                                                  -AutomationAccountName "devAccount" `
                                                  -Name "VSTSNative"

SourceControlSyncJobId               SyncType Status StartTime           EndTime
----------------------               -------- ------ ---------           -------
08d6d266-27b6-463c-beea-bc48a67ace15 FullSync Failed 08/15/2018 09:17 AM 08/15/2018 09:18 AM
b566d564-878a-4641-8c44-25bf7850531e FullSync Failed 08/15/2018 09:09 AM 08/15/2018 09:10 AM
```

### <span data-ttu-id="2561f-111">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="2561f-111">Example 2</span></span>
<span data-ttu-id="2561f-112">Det här kommandot hämtar synkroniseringsjobb för käll kontroll med ID-08d6d266-27b6-463c-Beea-bc48a67ace15 för VSTSNative för käll kontroll.</span><span class="sxs-lookup"><span data-stu-id="2561f-112">This command gets the source control sync job with id 08d6d266-27b6-463c-beea-bc48a67ace15 for the source control VSTSNative.</span></span> 


```powershell
PS C:\> Get-AzureRmAutomationSourceControlSyncJob -ResourceGroupName "rg1" `
                                                  -AutomationAccountName "devAccount" `
                                                  -Name "VSTSNative"
                                                  -Id "08d6d266-27b6-463c-beea-bc48a67ace15"

Status SyncType Exception
------ -------- ---------
Failed FullSync There were errors while syncing the user runbooks. Please see error streams for more information. (T...
```

## <span data-ttu-id="2561f-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="2561f-113">PARAMETERS</span></span>

### <span data-ttu-id="2561f-114">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="2561f-114">-AutomationAccountName</span></span>
<span data-ttu-id="2561f-115">Namnet på Automation-kontot.</span><span class="sxs-lookup"><span data-stu-id="2561f-115">The automation account name.</span></span>

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

### <span data-ttu-id="2561f-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2561f-116">-DefaultProfile</span></span>
<span data-ttu-id="2561f-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="2561f-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2561f-118">-JobId</span><span class="sxs-lookup"><span data-stu-id="2561f-118">-JobId</span></span>
<span data-ttu-id="2561f-119">Jobb-ID för käll kontroll.</span><span class="sxs-lookup"><span data-stu-id="2561f-119">The source control sync job id.</span></span>

```yaml
Type: System.Guid
Parameter Sets: (All)
Aliases: SourceControlSyncJobId

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2561f-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2561f-120">-ResourceGroupName</span></span>
<span data-ttu-id="2561f-121">Resurs gruppens namn.</span><span class="sxs-lookup"><span data-stu-id="2561f-121">The resource group name.</span></span>

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

### <span data-ttu-id="2561f-122">-SourceControlName</span><span class="sxs-lookup"><span data-stu-id="2561f-122">-SourceControlName</span></span>
<span data-ttu-id="2561f-123">Jobbets käll kontroll namn.</span><span class="sxs-lookup"><span data-stu-id="2561f-123">The source control name of the job.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2561f-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2561f-124">CommonParameters</span></span>
<span data-ttu-id="2561f-125">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2561f-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2561f-126">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2561f-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2561f-127">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="2561f-127">INPUTS</span></span>

### <span data-ttu-id="2561f-128">System. String</span><span class="sxs-lookup"><span data-stu-id="2561f-128">System.String</span></span>

### <span data-ttu-id="2561f-129">System. GUID</span><span class="sxs-lookup"><span data-stu-id="2561f-129">System.Guid</span></span>

## <span data-ttu-id="2561f-130">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="2561f-130">OUTPUTS</span></span>

### <span data-ttu-id="2561f-131">Microsoft. Azure. commands. Automation. Model. SourceControlSyncJob</span><span class="sxs-lookup"><span data-stu-id="2561f-131">Microsoft.Azure.Commands.Automation.Model.SourceControlSyncJob</span></span>

### <span data-ttu-id="2561f-132">Microsoft. Azure. commands. Automation. Model. SourceControlSyncJobRecord</span><span class="sxs-lookup"><span data-stu-id="2561f-132">Microsoft.Azure.Commands.Automation.Model.SourceControlSyncJobRecord</span></span>

## <span data-ttu-id="2561f-133">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="2561f-133">NOTES</span></span>

## <span data-ttu-id="2561f-134">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="2561f-134">RELATED LINKS</span></span>
