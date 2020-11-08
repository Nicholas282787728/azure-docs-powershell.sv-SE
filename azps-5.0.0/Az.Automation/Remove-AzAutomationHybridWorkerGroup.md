---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/remove-azautomationhybridworkergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationHybridWorkerGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationHybridWorkerGroup.md
ms.openlocfilehash: 78674e3245da1b8a58e099948bff23df9159efec
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94272340"
---
# <span data-ttu-id="7eddc-101">Remove-AzAutomationHybridWorkerGroup</span><span class="sxs-lookup"><span data-stu-id="7eddc-101">Remove-AzAutomationHybridWorkerGroup</span></span>

## <span data-ttu-id="7eddc-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="7eddc-102">SYNOPSIS</span></span>
<span data-ttu-id="7eddc-103">Tar bort hybrid Worker-gruppen från Automation.</span><span class="sxs-lookup"><span data-stu-id="7eddc-103">Removes hybrid worker group from Automation.</span></span>

## <span data-ttu-id="7eddc-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="7eddc-104">SYNTAX</span></span>

```
Remove-AzAutomationHybridWorkerGroup [-Name] <String> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="7eddc-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="7eddc-105">DESCRIPTION</span></span>
<span data-ttu-id="7eddc-106">Remove-AzAutomationHybridWorkerGroup-cmdleten tar bort en hybrid Worker-grupp från Automation.</span><span class="sxs-lookup"><span data-stu-id="7eddc-106">The Remove-AzAutomationHybridWorkerGroup cmdlet removes a hybrid worker group from Automation.</span></span>

## <span data-ttu-id="7eddc-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="7eddc-107">EXAMPLES</span></span>

### <span data-ttu-id="7eddc-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="7eddc-108">Example 1</span></span>
<span data-ttu-id="7eddc-109">Detta kommando tar bort en hybrid arbetare efter namn.</span><span class="sxs-lookup"><span data-stu-id="7eddc-109">This command removes a hybrid worker by name.</span></span>

```powershell
PS C:\> Remove-AzAutomationHybridWorkerGroup -ResourceGroupName "rg1" `
                                                  -AutomationAccountName "devAccount" `
                                                  -Name "GroupName" `
                                                  -Force
```

## <span data-ttu-id="7eddc-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="7eddc-110">PARAMETERS</span></span>

### <span data-ttu-id="7eddc-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="7eddc-111">-AutomationAccountName</span></span>
<span data-ttu-id="7eddc-112">Namnet på Automation-kontot.</span><span class="sxs-lookup"><span data-stu-id="7eddc-112">The automation account name.</span></span>

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

### <span data-ttu-id="7eddc-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7eddc-113">-DefaultProfile</span></span>
<span data-ttu-id="7eddc-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="7eddc-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7eddc-115">-Namn</span><span class="sxs-lookup"><span data-stu-id="7eddc-115">-Name</span></span>
<span data-ttu-id="7eddc-116">Hybrid arbetarens grupp namn.</span><span class="sxs-lookup"><span data-stu-id="7eddc-116">The hybrid worker group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Group

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7eddc-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7eddc-117">-ResourceGroupName</span></span>
<span data-ttu-id="7eddc-118">Resurs gruppens namn.</span><span class="sxs-lookup"><span data-stu-id="7eddc-118">The resource group name.</span></span>

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

### <span data-ttu-id="7eddc-119">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="7eddc-119">-Confirm</span></span>
<span data-ttu-id="7eddc-120">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="7eddc-120">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7eddc-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7eddc-121">-WhatIf</span></span>
<span data-ttu-id="7eddc-122">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="7eddc-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7eddc-123">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="7eddc-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7eddc-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7eddc-124">CommonParameters</span></span>
<span data-ttu-id="7eddc-125">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7eddc-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7eddc-126">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7eddc-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7eddc-127">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="7eddc-127">INPUTS</span></span>

### <span data-ttu-id="7eddc-128">System. String</span><span class="sxs-lookup"><span data-stu-id="7eddc-128">System.String</span></span>

## <span data-ttu-id="7eddc-129">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="7eddc-129">OUTPUTS</span></span>

### <span data-ttu-id="7eddc-130">System. Void</span><span class="sxs-lookup"><span data-stu-id="7eddc-130">System.Void</span></span>

## <span data-ttu-id="7eddc-131">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="7eddc-131">NOTES</span></span>

## <span data-ttu-id="7eddc-132">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="7eddc-132">RELATED LINKS</span></span>
