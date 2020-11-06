---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/start-azurermautomationsourcecontrolsyncjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Start-AzureRmAutomationSourceControlSyncJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Start-AzureRmAutomationSourceControlSyncJob.md
ms.openlocfilehash: 4a5864e9572a21442a5333232fe5f705fb1b5687
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93572956"
---
# <span data-ttu-id="c5a0c-101">Start-AzureRmAutomationSourceControlSyncJob</span><span class="sxs-lookup"><span data-stu-id="c5a0c-101">Start-AzureRmAutomationSourceControlSyncJob</span></span>

## <span data-ttu-id="c5a0c-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="c5a0c-102">SYNOPSIS</span></span>
<span data-ttu-id="c5a0c-103">Startar en Azure Automation-synkroniseringsjobb.</span><span class="sxs-lookup"><span data-stu-id="c5a0c-103">Starts an Azure Automation source control sync job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c5a0c-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="c5a0c-104">SYNTAX</span></span>

```
Start-AzureRmAutomationSourceControlSyncJob -SourceControlName <String> [-JobId <Guid>]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c5a0c-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="c5a0c-105">DESCRIPTION</span></span>
<span data-ttu-id="c5a0c-106">Start-AzureRmAutomationSourceControlSyncJob cmdlet startar ett synkroniseringsjobb för Azure Automation-kontroll för det angivna käll kontroll namnet.</span><span class="sxs-lookup"><span data-stu-id="c5a0c-106">The Start-AzureRmAutomationSourceControlSyncJob cmdlet starts a Azure Automation souce control sync job for the given source control name.</span></span>

## <span data-ttu-id="c5a0c-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="c5a0c-107">EXAMPLES</span></span>

### <span data-ttu-id="c5a0c-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="c5a0c-108">Example 1</span></span>
```powershell
PS C:\> Start-AzureRmAutomationSourceControlSyncJob -ResourceGroupName "rg1" `
                                                    -AutomationAccountName "devAccount" `
                                                    -Name "VSTSNative"

SourceControlSyncJobId               SyncType Status  StartTime EndTime
----------------------               -------- ------  --------- -------
b51aed78-bef6-40d4-a966-cd45fd5af576 FullSync Running
```

## <span data-ttu-id="c5a0c-109">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="c5a0c-109">PARAMETERS</span></span>

### <span data-ttu-id="c5a0c-110">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="c5a0c-110">-AutomationAccountName</span></span>
<span data-ttu-id="c5a0c-111">Namnet på Automation-kontot.</span><span class="sxs-lookup"><span data-stu-id="c5a0c-111">The automation account name.</span></span>

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

### <span data-ttu-id="c5a0c-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c5a0c-112">-DefaultProfile</span></span>
<span data-ttu-id="c5a0c-113">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="c5a0c-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c5a0c-114">-JobId</span><span class="sxs-lookup"><span data-stu-id="c5a0c-114">-JobId</span></span>
<span data-ttu-id="c5a0c-115">Jobb-ID för käll kontroll.</span><span class="sxs-lookup"><span data-stu-id="c5a0c-115">The source control sync job id.</span></span>

```yaml
Type: System.Guid
Parameter Sets: (All)
Aliases: SourceControlSyncJobId

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c5a0c-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c5a0c-116">-ResourceGroupName</span></span>
<span data-ttu-id="c5a0c-117">Resurs gruppens namn.</span><span class="sxs-lookup"><span data-stu-id="c5a0c-117">The resource group name.</span></span>

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

### <span data-ttu-id="c5a0c-118">-SourceControlName</span><span class="sxs-lookup"><span data-stu-id="c5a0c-118">-SourceControlName</span></span>
<span data-ttu-id="c5a0c-119">Namn på käll kontroll.</span><span class="sxs-lookup"><span data-stu-id="c5a0c-119">The source control name.</span></span>

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

### <span data-ttu-id="c5a0c-120">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="c5a0c-120">-Confirm</span></span>
<span data-ttu-id="c5a0c-121">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="c5a0c-121">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c5a0c-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c5a0c-122">-WhatIf</span></span>
<span data-ttu-id="c5a0c-123">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="c5a0c-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c5a0c-124">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="c5a0c-124">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c5a0c-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c5a0c-125">CommonParameters</span></span>
<span data-ttu-id="c5a0c-126">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c5a0c-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c5a0c-127">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c5a0c-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c5a0c-128">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="c5a0c-128">INPUTS</span></span>

### <span data-ttu-id="c5a0c-129">System. String</span><span class="sxs-lookup"><span data-stu-id="c5a0c-129">System.String</span></span>

## <span data-ttu-id="c5a0c-130">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="c5a0c-130">OUTPUTS</span></span>

### <span data-ttu-id="c5a0c-131">Microsoft. Azure. commands. Automation. Model. SourceControlSyncJob</span><span class="sxs-lookup"><span data-stu-id="c5a0c-131">Microsoft.Azure.Commands.Automation.Model.SourceControlSyncJob</span></span>

## <span data-ttu-id="c5a0c-132">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="c5a0c-132">NOTES</span></span>

## <span data-ttu-id="c5a0c-133">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="c5a0c-133">RELATED LINKS</span></span>
