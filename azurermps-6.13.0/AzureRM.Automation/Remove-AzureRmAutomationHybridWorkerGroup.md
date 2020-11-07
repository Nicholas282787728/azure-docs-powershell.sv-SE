---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/remove-azurermautomationdscnodeconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Remove-AzureRmAutomationHybridWorkerGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Remove-AzureRmAutomationHybridWorkerGroup.md
ms.openlocfilehash: b6f15bc55c2e9f9a05e60e7e6f2c139ddbb70454
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93755554"
---
# <span data-ttu-id="cbeec-101">Remove-AzureRmAutomationHybridWorkerGroup</span><span class="sxs-lookup"><span data-stu-id="cbeec-101">Remove-AzureRmAutomationHybridWorkerGroup</span></span>

## <span data-ttu-id="cbeec-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="cbeec-102">SYNOPSIS</span></span>
<span data-ttu-id="cbeec-103">Tar bort hybrid Worker-gruppen från Automation.</span><span class="sxs-lookup"><span data-stu-id="cbeec-103">Removes hybrid worker group from Automation.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="cbeec-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="cbeec-104">SYNTAX</span></span>

```
Remove-AzureRmAutomationHybridWorkerGroup [-Name] <String> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="cbeec-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="cbeec-105">DESCRIPTION</span></span>
<span data-ttu-id="cbeec-106">Remove-AzureRmAutomationHybridWorkerGroup-cmdleten tar bort en hybrid Worker-grupp från Automation.</span><span class="sxs-lookup"><span data-stu-id="cbeec-106">The Remove-AzureRmAutomationHybridWorkerGroup cmdlet removes a hybrid worker group from Automation.</span></span>

## <span data-ttu-id="cbeec-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="cbeec-107">EXAMPLES</span></span>

### <span data-ttu-id="cbeec-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="cbeec-108">Example 1</span></span>
<span data-ttu-id="cbeec-109">Detta kommando tar bort en hybrid arbetare efter namn.</span><span class="sxs-lookup"><span data-stu-id="cbeec-109">This command removes a hybrid worker by name.</span></span>

```powershell
PS C:\> Remove-AzureRmAutomationHybridWorkerGroup -ResourceGroupName "rg1" `
                                                  -AutomationAccountName "devAccount" `
                                                  -Name "GroupName" `
                                                  -Force
```

## <span data-ttu-id="cbeec-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="cbeec-110">PARAMETERS</span></span>

### <span data-ttu-id="cbeec-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="cbeec-111">-AutomationAccountName</span></span>
<span data-ttu-id="cbeec-112">Namnet på Automation-kontot.</span><span class="sxs-lookup"><span data-stu-id="cbeec-112">The automation account name.</span></span>

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

### <span data-ttu-id="cbeec-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cbeec-113">-DefaultProfile</span></span>
<span data-ttu-id="cbeec-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="cbeec-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cbeec-115">-Namn</span><span class="sxs-lookup"><span data-stu-id="cbeec-115">-Name</span></span>
<span data-ttu-id="cbeec-116">Hybrid arbetarens grupp namn.</span><span class="sxs-lookup"><span data-stu-id="cbeec-116">The hybrid worker group name.</span></span>

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

### <span data-ttu-id="cbeec-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cbeec-117">-ResourceGroupName</span></span>
<span data-ttu-id="cbeec-118">Resurs gruppens namn.</span><span class="sxs-lookup"><span data-stu-id="cbeec-118">The resource group name.</span></span>

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

### <span data-ttu-id="cbeec-119">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="cbeec-119">-Confirm</span></span>
<span data-ttu-id="cbeec-120">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="cbeec-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cbeec-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cbeec-121">-WhatIf</span></span>
<span data-ttu-id="cbeec-122">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="cbeec-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cbeec-123">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="cbeec-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cbeec-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cbeec-124">CommonParameters</span></span>
<span data-ttu-id="cbeec-125">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cbeec-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cbeec-126">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cbeec-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cbeec-127">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="cbeec-127">INPUTS</span></span>

### <span data-ttu-id="cbeec-128">System. String</span><span class="sxs-lookup"><span data-stu-id="cbeec-128">System.String</span></span>

## <span data-ttu-id="cbeec-129">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="cbeec-129">OUTPUTS</span></span>

### <span data-ttu-id="cbeec-130">System. Void</span><span class="sxs-lookup"><span data-stu-id="cbeec-130">System.Void</span></span>

## <span data-ttu-id="cbeec-131">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="cbeec-131">NOTES</span></span>

## <span data-ttu-id="cbeec-132">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="cbeec-132">RELATED LINKS</span></span>
