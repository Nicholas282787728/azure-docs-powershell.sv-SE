---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/get-azurermautomationsourcecontrolsyncjoboutput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRmAutomationSourceControlSyncJobOutput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRmAutomationSourceControlSyncJobOutput.md
ms.openlocfilehash: 59de6fa12ef3c6bd774f05fe55d31d74bb9efa13
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93756714"
---
# <span data-ttu-id="a5ca3-101">Get-AzureRmAutomationSourceControlSyncJobOutput</span><span class="sxs-lookup"><span data-stu-id="a5ca3-101">Get-AzureRmAutomationSourceControlSyncJobOutput</span></span>

## <span data-ttu-id="a5ca3-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="a5ca3-102">SYNOPSIS</span></span>
<span data-ttu-id="a5ca3-103">Hämtar utdata från ett synkroniseringsjobb för Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="a5ca3-103">Gets the output of an Azure Automation source control sync job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a5ca3-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="a5ca3-104">SYNTAX</span></span>

```
Get-AzureRmAutomationSourceControlSyncJobOutput -SourceControlName <String> -JobId <Guid>
 [-Stream <SourceControlSyncJobStreamType>] [-StreamId <String>] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a5ca3-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="a5ca3-105">DESCRIPTION</span></span>
<span data-ttu-id="a5ca3-106">Cmdleten **Get-AzureRmAutomationSourceControlSyncJobOutput** hämtar utdata för ett synkroniseringsjobb för Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="a5ca3-106">The **Get-AzureRmAutomationSourceControlSyncJobOutput** cmdlet gets the output for a Azure Automation source control sync job.</span></span>

## <span data-ttu-id="a5ca3-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="a5ca3-107">EXAMPLES</span></span>

### <span data-ttu-id="a5ca3-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="a5ca3-108">Example 1</span></span>
<span data-ttu-id="a5ca3-109">Det här kommandot får utdata från käll kontrollens synkroniseringsjobb med ID-08d6d266-27b6-463c-Beea-bc48a67ace15 för VSTSNative för käll kontroll.</span><span class="sxs-lookup"><span data-stu-id="a5ca3-109">This command gets the output of source control sync job with id 08d6d266-27b6-463c-beea-bc48a67ace15 for the source control VSTSNative.</span></span> 


```powershell
PS C:\> Get-AzureRmAutomationSourceControlSyncJobOutput -ResourceGroupName "rg1" `
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

## <span data-ttu-id="a5ca3-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="a5ca3-110">PARAMETERS</span></span>

### <span data-ttu-id="a5ca3-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="a5ca3-111">-AutomationAccountName</span></span>
<span data-ttu-id="a5ca3-112">Namnet på Automation-kontot.</span><span class="sxs-lookup"><span data-stu-id="a5ca3-112">The automation account name.</span></span>

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

### <span data-ttu-id="a5ca3-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a5ca3-113">-DefaultProfile</span></span>
<span data-ttu-id="a5ca3-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="a5ca3-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a5ca3-115">-JobId</span><span class="sxs-lookup"><span data-stu-id="a5ca3-115">-JobId</span></span>
<span data-ttu-id="a5ca3-116">Jobb-ID för käll kontroll.</span><span class="sxs-lookup"><span data-stu-id="a5ca3-116">The source control sync job id.</span></span>

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

### <span data-ttu-id="a5ca3-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a5ca3-117">-ResourceGroupName</span></span>
<span data-ttu-id="a5ca3-118">Resurs gruppens namn.</span><span class="sxs-lookup"><span data-stu-id="a5ca3-118">The resource group name.</span></span>

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

### <span data-ttu-id="a5ca3-119">-SourceControlName</span><span class="sxs-lookup"><span data-stu-id="a5ca3-119">-SourceControlName</span></span>
<span data-ttu-id="a5ca3-120">Namn på käll kontroll.</span><span class="sxs-lookup"><span data-stu-id="a5ca3-120">The source control name.</span></span>

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

### <span data-ttu-id="a5ca3-121">-Stream</span><span class="sxs-lookup"><span data-stu-id="a5ca3-121">-Stream</span></span>
<span data-ttu-id="a5ca3-122">Data Ströms typen.</span><span class="sxs-lookup"><span data-stu-id="a5ca3-122">The stream type.</span></span>
<span data-ttu-id="a5ca3-123">Standardvärden.</span><span class="sxs-lookup"><span data-stu-id="a5ca3-123">Defaults to Any.</span></span>

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

### <span data-ttu-id="a5ca3-124">-StreamId</span><span class="sxs-lookup"><span data-stu-id="a5ca3-124">-StreamId</span></span>
<span data-ttu-id="a5ca3-125">Ström-ID.</span><span class="sxs-lookup"><span data-stu-id="a5ca3-125">The stream id.</span></span>

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

### <span data-ttu-id="a5ca3-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a5ca3-126">CommonParameters</span></span>
<span data-ttu-id="a5ca3-127">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a5ca3-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a5ca3-128">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a5ca3-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a5ca3-129">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="a5ca3-129">INPUTS</span></span>

### <span data-ttu-id="a5ca3-130">System. String</span><span class="sxs-lookup"><span data-stu-id="a5ca3-130">System.String</span></span>

### <span data-ttu-id="a5ca3-131">System. GUID</span><span class="sxs-lookup"><span data-stu-id="a5ca3-131">System.Guid</span></span>

### <span data-ttu-id="a5ca3-132">Microsoft. Azure. commands. Automation. Common. SourceControlSyncJobStreamType</span><span class="sxs-lookup"><span data-stu-id="a5ca3-132">Microsoft.Azure.Commands.Automation.Common.SourceControlSyncJobStreamType</span></span>

## <span data-ttu-id="a5ca3-133">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="a5ca3-133">OUTPUTS</span></span>

### <span data-ttu-id="a5ca3-134">Microsoft. Azure. commands. Automation. Model. SourceControlSyncJobStream</span><span class="sxs-lookup"><span data-stu-id="a5ca3-134">Microsoft.Azure.Commands.Automation.Model.SourceControlSyncJobStream</span></span>

### <span data-ttu-id="a5ca3-135">Microsoft. Azure. commands. Automation. Model. SourceControlSyncJobStreamRecord</span><span class="sxs-lookup"><span data-stu-id="a5ca3-135">Microsoft.Azure.Commands.Automation.Model.SourceControlSyncJobStreamRecord</span></span>

## <span data-ttu-id="a5ca3-136">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="a5ca3-136">NOTES</span></span>

## <span data-ttu-id="a5ca3-137">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="a5ca3-137">RELATED LINKS</span></span>
