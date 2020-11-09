---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/start-azautomationsourcecontrolsyncjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Start-AzAutomationSourceControlSyncJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Start-AzAutomationSourceControlSyncJob.md
ms.openlocfilehash: 1f685307ae1d6f9a030ac5c242af9fcec97c032b
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94322632"
---
# <span data-ttu-id="4b8b5-101">Start-AzAutomationSourceControlSyncJob</span><span class="sxs-lookup"><span data-stu-id="4b8b5-101">Start-AzAutomationSourceControlSyncJob</span></span>

## <span data-ttu-id="4b8b5-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="4b8b5-102">SYNOPSIS</span></span>
<span data-ttu-id="4b8b5-103">Startar en Azure Automation-synkroniseringsjobb.</span><span class="sxs-lookup"><span data-stu-id="4b8b5-103">Starts an Azure Automation source control sync job.</span></span>

## <span data-ttu-id="4b8b5-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="4b8b5-104">SYNTAX</span></span>

```
Start-AzAutomationSourceControlSyncJob -SourceControlName <String> [-JobId <Guid>]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4b8b5-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="4b8b5-105">DESCRIPTION</span></span>
<span data-ttu-id="4b8b5-106">Start-AzAutomationSourceControlSyncJob-cmdleten startar ett synkroniseringsjobb för Azure Automation för det angivna käll kontroll namnet.</span><span class="sxs-lookup"><span data-stu-id="4b8b5-106">The Start-AzAutomationSourceControlSyncJob cmdlet starts a Azure Automation source control sync job for the given source control name.</span></span>

## <span data-ttu-id="4b8b5-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="4b8b5-107">EXAMPLES</span></span>

### <span data-ttu-id="4b8b5-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="4b8b5-108">Example 1</span></span>
```powershell
PS C:\> Start-AzAutomationSourceControlSyncJob -ResourceGroupName "rg1" `
                                                    -AutomationAccountName "devAccount" `
                                                    -Name "VSTSNative"

SourceControlSyncJobId               SyncType Status  StartTime EndTime
----------------------               -------- ------  --------- -------
b51aed78-bef6-40d4-a966-cd45fd5af576 FullSync Running
```

## <span data-ttu-id="4b8b5-109">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="4b8b5-109">PARAMETERS</span></span>

### <span data-ttu-id="4b8b5-110">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="4b8b5-110">-AutomationAccountName</span></span>
<span data-ttu-id="4b8b5-111">Namnet på Automation-kontot.</span><span class="sxs-lookup"><span data-stu-id="4b8b5-111">The automation account name.</span></span>

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

### <span data-ttu-id="4b8b5-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4b8b5-112">-DefaultProfile</span></span>
<span data-ttu-id="4b8b5-113">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="4b8b5-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4b8b5-114">-JobId</span><span class="sxs-lookup"><span data-stu-id="4b8b5-114">-JobId</span></span>
<span data-ttu-id="4b8b5-115">Jobb-ID för käll kontroll.</span><span class="sxs-lookup"><span data-stu-id="4b8b5-115">The source control sync job id.</span></span>

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

### <span data-ttu-id="4b8b5-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4b8b5-116">-ResourceGroupName</span></span>
<span data-ttu-id="4b8b5-117">Resurs gruppens namn.</span><span class="sxs-lookup"><span data-stu-id="4b8b5-117">The resource group name.</span></span>

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

### <span data-ttu-id="4b8b5-118">-SourceControlName</span><span class="sxs-lookup"><span data-stu-id="4b8b5-118">-SourceControlName</span></span>
<span data-ttu-id="4b8b5-119">Namn på käll kontroll.</span><span class="sxs-lookup"><span data-stu-id="4b8b5-119">The source control name.</span></span>

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

### <span data-ttu-id="4b8b5-120">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="4b8b5-120">-Confirm</span></span>
<span data-ttu-id="4b8b5-121">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="4b8b5-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4b8b5-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4b8b5-122">-WhatIf</span></span>
<span data-ttu-id="4b8b5-123">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="4b8b5-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4b8b5-124">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="4b8b5-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4b8b5-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4b8b5-125">CommonParameters</span></span>
<span data-ttu-id="4b8b5-126">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4b8b5-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4b8b5-127">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4b8b5-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4b8b5-128">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="4b8b5-128">INPUTS</span></span>

### <span data-ttu-id="4b8b5-129">System. String</span><span class="sxs-lookup"><span data-stu-id="4b8b5-129">System.String</span></span>

## <span data-ttu-id="4b8b5-130">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="4b8b5-130">OUTPUTS</span></span>

### <span data-ttu-id="4b8b5-131">Microsoft. Azure. commands. Automation. Model. SourceControlSyncJob</span><span class="sxs-lookup"><span data-stu-id="4b8b5-131">Microsoft.Azure.Commands.Automation.Model.SourceControlSyncJob</span></span>

## <span data-ttu-id="4b8b5-132">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="4b8b5-132">NOTES</span></span>

## <span data-ttu-id="4b8b5-133">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="4b8b5-133">RELATED LINKS</span></span>
