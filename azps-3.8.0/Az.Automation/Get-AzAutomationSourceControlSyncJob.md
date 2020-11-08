---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/get-azautomationsourcecontrolsyncjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationSourceControlSyncJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationSourceControlSyncJob.md
ms.openlocfilehash: 5284f2ae8825f801e18752e21a5fe9b8cf43ac32
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94092719"
---
# <span data-ttu-id="c45a5-101">Get-AzAutomationSourceControlSyncJob</span><span class="sxs-lookup"><span data-stu-id="c45a5-101">Get-AzAutomationSourceControlSyncJob</span></span>

## <span data-ttu-id="c45a5-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="c45a5-102">SYNOPSIS</span></span>
<span data-ttu-id="c45a5-103">Hämtar synkroniseringsjobb för Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="c45a5-103">Gets Azure Automation source control sync jobs.</span></span>

## <span data-ttu-id="c45a5-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="c45a5-104">SYNTAX</span></span>

```
Get-AzAutomationSourceControlSyncJob -SourceControlName <String> [-JobId <Guid>] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c45a5-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="c45a5-105">DESCRIPTION</span></span>
<span data-ttu-id="c45a5-106">Get-AzAutomationSourceControlSyncJob cmdlet får synkroniseringsjobb för Azure Automation Source Control.</span><span class="sxs-lookup"><span data-stu-id="c45a5-106">The Get-AzAutomationSourceControlSyncJob cmdlet gets Azure Automation source control sync jobs.</span></span> <span data-ttu-id="c45a5-107">Om du vill hämta ett specifikt synkroniseringsjobb för käll kontroll anger du dess ID.</span><span class="sxs-lookup"><span data-stu-id="c45a5-107">To get a specific source control sync job, specify its id.</span></span>

## <span data-ttu-id="c45a5-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="c45a5-108">EXAMPLES</span></span>

### <span data-ttu-id="c45a5-109">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="c45a5-109">Example 1</span></span>
<span data-ttu-id="c45a5-110">Det här kommandot får alla synkroniseringsjobb för VSTSNative käll kontroll.</span><span class="sxs-lookup"><span data-stu-id="c45a5-110">This command gets all the Automation source control sync jobs for the source control VSTSNative.</span></span>


```powershell
PS C:\> Get-AzAutomationSourceControlSyncJob -ResourceGroupName "rg1" `
                                                  -AutomationAccountName "devAccount" `
                                                  -Name "VSTSNative"

SourceControlSyncJobId               SyncType Status StartTime           EndTime
----------------------               -------- ------ ---------           -------
08d6d266-27b6-463c-beea-bc48a67ace15 FullSync Failed 08/15/2018 09:17 AM 08/15/2018 09:18 AM
b566d564-878a-4641-8c44-25bf7850531e FullSync Failed 08/15/2018 09:09 AM 08/15/2018 09:10 AM
```

### <span data-ttu-id="c45a5-111">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="c45a5-111">Example 2</span></span>
<span data-ttu-id="c45a5-112">Det här kommandot hämtar synkroniseringsjobb för käll kontroll med ID-08d6d266-27b6-463c-Beea-bc48a67ace15 för VSTSNative för käll kontroll.</span><span class="sxs-lookup"><span data-stu-id="c45a5-112">This command gets the source control sync job with id 08d6d266-27b6-463c-beea-bc48a67ace15 for the source control VSTSNative.</span></span> 


```powershell
PS C:\> Get-AzAutomationSourceControlSyncJob -ResourceGroupName "rg1" `
                                                  -AutomationAccountName "devAccount" `
                                                  -Name "VSTSNative"
                                                  -Id "08d6d266-27b6-463c-beea-bc48a67ace15"

Status SyncType Exception
------ -------- ---------
Failed FullSync There were errors while syncing the user runbooks. Please see error streams for more information. (T...
```

## <span data-ttu-id="c45a5-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="c45a5-113">PARAMETERS</span></span>

### <span data-ttu-id="c45a5-114">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="c45a5-114">-AutomationAccountName</span></span>
<span data-ttu-id="c45a5-115">Namnet på Automation-kontot.</span><span class="sxs-lookup"><span data-stu-id="c45a5-115">The automation account name.</span></span>

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

### <span data-ttu-id="c45a5-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c45a5-116">-DefaultProfile</span></span>
<span data-ttu-id="c45a5-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="c45a5-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c45a5-118">-JobId</span><span class="sxs-lookup"><span data-stu-id="c45a5-118">-JobId</span></span>
<span data-ttu-id="c45a5-119">Jobb-ID för käll kontroll.</span><span class="sxs-lookup"><span data-stu-id="c45a5-119">The source control sync job id.</span></span>

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

### <span data-ttu-id="c45a5-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c45a5-120">-ResourceGroupName</span></span>
<span data-ttu-id="c45a5-121">Resurs gruppens namn.</span><span class="sxs-lookup"><span data-stu-id="c45a5-121">The resource group name.</span></span>

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

### <span data-ttu-id="c45a5-122">-SourceControlName</span><span class="sxs-lookup"><span data-stu-id="c45a5-122">-SourceControlName</span></span>
<span data-ttu-id="c45a5-123">Jobbets käll kontroll namn.</span><span class="sxs-lookup"><span data-stu-id="c45a5-123">The source control name of the job.</span></span>

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

### <span data-ttu-id="c45a5-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c45a5-124">CommonParameters</span></span>
<span data-ttu-id="c45a5-125">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c45a5-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c45a5-126">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c45a5-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c45a5-127">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="c45a5-127">INPUTS</span></span>

### <span data-ttu-id="c45a5-128">System. String</span><span class="sxs-lookup"><span data-stu-id="c45a5-128">System.String</span></span>

### <span data-ttu-id="c45a5-129">System. GUID</span><span class="sxs-lookup"><span data-stu-id="c45a5-129">System.Guid</span></span>

## <span data-ttu-id="c45a5-130">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="c45a5-130">OUTPUTS</span></span>

### <span data-ttu-id="c45a5-131">Microsoft. Azure. commands. Automation. Model. SourceControlSyncJob</span><span class="sxs-lookup"><span data-stu-id="c45a5-131">Microsoft.Azure.Commands.Automation.Model.SourceControlSyncJob</span></span>

### <span data-ttu-id="c45a5-132">Microsoft. Azure. commands. Automation. Model. SourceControlSyncJobRecord</span><span class="sxs-lookup"><span data-stu-id="c45a5-132">Microsoft.Azure.Commands.Automation.Model.SourceControlSyncJobRecord</span></span>

## <span data-ttu-id="c45a5-133">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="c45a5-133">NOTES</span></span>

## <span data-ttu-id="c45a5-134">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="c45a5-134">RELATED LINKS</span></span>
