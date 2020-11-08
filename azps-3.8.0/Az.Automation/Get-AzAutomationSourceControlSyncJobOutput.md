---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/get-azautomationsourcecontrolsyncjoboutput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationSourceControlSyncJobOutput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationSourceControlSyncJobOutput.md
ms.openlocfilehash: 6567d479ad0db7df959e4059155149f4fc06e1a3
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94092718"
---
# <span data-ttu-id="0d769-101">Get-AzAutomationSourceControlSyncJobOutput</span><span class="sxs-lookup"><span data-stu-id="0d769-101">Get-AzAutomationSourceControlSyncJobOutput</span></span>

## <span data-ttu-id="0d769-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="0d769-102">SYNOPSIS</span></span>
<span data-ttu-id="0d769-103">Hämtar utdata från ett synkroniseringsjobb för Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="0d769-103">Gets the output of an Azure Automation source control sync job.</span></span>

## <span data-ttu-id="0d769-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="0d769-104">SYNTAX</span></span>

```
Get-AzAutomationSourceControlSyncJobOutput -SourceControlName <String> -JobId <Guid>
 [-Stream <SourceControlSyncJobStreamType>] [-StreamId <String>] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0d769-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="0d769-105">DESCRIPTION</span></span>
<span data-ttu-id="0d769-106">Cmdleten **Get-AzAutomationSourceControlSyncJobOutput** hämtar utdata för ett synkroniseringsjobb för Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="0d769-106">The **Get-AzAutomationSourceControlSyncJobOutput** cmdlet gets the output for a Azure Automation source control sync job.</span></span>

## <span data-ttu-id="0d769-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="0d769-107">EXAMPLES</span></span>

### <span data-ttu-id="0d769-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="0d769-108">Example 1</span></span>
<span data-ttu-id="0d769-109">Det här kommandot får utdata från käll kontrollens synkroniseringsjobb med ID-08d6d266-27b6-463c-Beea-bc48a67ace15 för VSTSNative för käll kontroll.</span><span class="sxs-lookup"><span data-stu-id="0d769-109">This command gets the output of source control sync job with id 08d6d266-27b6-463c-beea-bc48a67ace15 for the source control VSTSNative.</span></span> 


```powershell
PS C:\> Get-AzAutomationSourceControlSyncJobOutput -ResourceGroupName "rg1" `
                                                        -AutomationAccountName "devAccount" `
                                                        -Name "VSTSNative"
                                                        -Id "08d6d266-27b6-463c-beea-bc48a67ace15" `
                                                        -Stream Output | ForEach-Object {$_.summary}

========================================================================================================

Azure Automation Source Control Public Preview.
Supported runbooks to sync: PowerShell Workflow, PowerShell Scripts, DSC Configurations, Graphical, and Python 2.
Setting AzureRmEnvironment.
Getting AzureRunAsConnection.
Logging in to Azure...
Source control information for syncing:
[RepoUrl = https://contoso.visualstudio.com/_git/GitDemo] [Branch  = master] [FolderPath = /]
Verifying url: https://fcontoso.visualstudio.com/_git/GitDemo
Connecting to VSTS...

Source Control Sync Summary:

2 files synced:
 - RunbookA.ps1
 - RunbookB.ps1

Failed to import runbook:
 - RunbookC.ps1

File is not a runbook:
 - README.md
 - text_file.txt

File size exceeds 1Mb:
 - RunbookD_GreatherThan1MB.ps1

Invalid runbook name:
 - RunbookZ_ĈĦŕĬŞ.ps1

========================================================================================================
```

## <span data-ttu-id="0d769-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="0d769-110">PARAMETERS</span></span>

### <span data-ttu-id="0d769-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="0d769-111">-AutomationAccountName</span></span>
<span data-ttu-id="0d769-112">Namnet på Automation-kontot.</span><span class="sxs-lookup"><span data-stu-id="0d769-112">The automation account name.</span></span>

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

### <span data-ttu-id="0d769-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0d769-113">-DefaultProfile</span></span>
<span data-ttu-id="0d769-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="0d769-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0d769-115">-JobId</span><span class="sxs-lookup"><span data-stu-id="0d769-115">-JobId</span></span>
<span data-ttu-id="0d769-116">Jobb-ID för käll kontroll.</span><span class="sxs-lookup"><span data-stu-id="0d769-116">The source control sync job id.</span></span>

```yaml
Type: System.Guid
Parameter Sets: (All)
Aliases: SourceControlSyncJobId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0d769-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0d769-117">-ResourceGroupName</span></span>
<span data-ttu-id="0d769-118">Resurs gruppens namn.</span><span class="sxs-lookup"><span data-stu-id="0d769-118">The resource group name.</span></span>

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

### <span data-ttu-id="0d769-119">-SourceControlName</span><span class="sxs-lookup"><span data-stu-id="0d769-119">-SourceControlName</span></span>
<span data-ttu-id="0d769-120">Namn på käll kontroll.</span><span class="sxs-lookup"><span data-stu-id="0d769-120">The source control name.</span></span>

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

### <span data-ttu-id="0d769-121">-Stream</span><span class="sxs-lookup"><span data-stu-id="0d769-121">-Stream</span></span>
<span data-ttu-id="0d769-122">Data Ströms typen.</span><span class="sxs-lookup"><span data-stu-id="0d769-122">The stream type.</span></span>
<span data-ttu-id="0d769-123">Standardvärden.</span><span class="sxs-lookup"><span data-stu-id="0d769-123">Defaults to Any.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Automation.Common.SourceControlSyncJobStreamType
Parameter Sets: (All)
Aliases:
Accepted values: Any, Output, Error

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0d769-124">-StreamId</span><span class="sxs-lookup"><span data-stu-id="0d769-124">-StreamId</span></span>
<span data-ttu-id="0d769-125">Ström-ID.</span><span class="sxs-lookup"><span data-stu-id="0d769-125">The stream id.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: SourceControlSyncJobStreamId

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0d769-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0d769-126">CommonParameters</span></span>
<span data-ttu-id="0d769-127">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0d769-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0d769-128">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0d769-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0d769-129">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="0d769-129">INPUTS</span></span>

### <span data-ttu-id="0d769-130">System. String</span><span class="sxs-lookup"><span data-stu-id="0d769-130">System.String</span></span>

### <span data-ttu-id="0d769-131">System. GUID</span><span class="sxs-lookup"><span data-stu-id="0d769-131">System.Guid</span></span>

### <span data-ttu-id="0d769-132">Microsoft. Azure. commands. Automation. Common. SourceControlSyncJobStreamType</span><span class="sxs-lookup"><span data-stu-id="0d769-132">Microsoft.Azure.Commands.Automation.Common.SourceControlSyncJobStreamType</span></span>

## <span data-ttu-id="0d769-133">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="0d769-133">OUTPUTS</span></span>

### <span data-ttu-id="0d769-134">Microsoft. Azure. commands. Automation. Model. SourceControlSyncJobStream</span><span class="sxs-lookup"><span data-stu-id="0d769-134">Microsoft.Azure.Commands.Automation.Model.SourceControlSyncJobStream</span></span>

### <span data-ttu-id="0d769-135">Microsoft. Azure. commands. Automation. Model. SourceControlSyncJobStreamRecord</span><span class="sxs-lookup"><span data-stu-id="0d769-135">Microsoft.Azure.Commands.Automation.Model.SourceControlSyncJobStreamRecord</span></span>

## <span data-ttu-id="0d769-136">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="0d769-136">NOTES</span></span>

## <span data-ttu-id="0d769-137">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="0d769-137">RELATED LINKS</span></span>
