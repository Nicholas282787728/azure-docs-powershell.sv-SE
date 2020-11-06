---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: 16055879-C001-46E7-B8C3-1FE2A1A67AC4
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/remove-azurermautomationrunbook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Remove-AzureRMAutomationRunbook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Remove-AzureRMAutomationRunbook.md
ms.openlocfilehash: a4f65e20253ef979cba5d3907faeba3fb58e7fe6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93585172"
---
# <span data-ttu-id="d0c87-101">Remove-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="d0c87-101">Remove-AzureRmAutomationRunbook</span></span>

## <span data-ttu-id="d0c87-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="d0c87-102">SYNOPSIS</span></span>
<span data-ttu-id="d0c87-103">Tar bort en Runbook.</span><span class="sxs-lookup"><span data-stu-id="d0c87-103">Removes a runbook.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d0c87-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="d0c87-104">SYNTAX</span></span>

```
Remove-AzureRmAutomationRunbook [-Name] <String> [-Force] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="d0c87-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="d0c87-105">DESCRIPTION</span></span>
<span data-ttu-id="d0c87-106">Cmdleten **Remove-AzureRmAutomationRunbook** tar bort en Runbook från Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="d0c87-106">The **Remove-AzureRmAutomationRunbook** cmdlet removes a runbook from Azure Automation.</span></span>

## <span data-ttu-id="d0c87-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="d0c87-107">EXAMPLES</span></span>

### <span data-ttu-id="d0c87-108">Exempel 1: ta bort en Runbook</span><span class="sxs-lookup"><span data-stu-id="d0c87-108">Example 1: Remove a runbook</span></span>
```
PS C:\>Remove-AzureRmAutomationRunbook -AutomationAccountName "Contoso17" -Name "Runbook03" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="d0c87-109">Det här kommandot tar bort Runbook-flödet med namnet Runbook03 i Azure Automation-kontot med namnet Contoso17.</span><span class="sxs-lookup"><span data-stu-id="d0c87-109">This command removes the runbook named Runbook03 in the Azure Automation account named Contoso17.</span></span>

## <span data-ttu-id="d0c87-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="d0c87-110">PARAMETERS</span></span>

### <span data-ttu-id="d0c87-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="d0c87-111">-AutomationAccountName</span></span>
<span data-ttu-id="d0c87-112">Anger namnet på det Automation-konto som denna cmdlet tar bort en Runbook för.</span><span class="sxs-lookup"><span data-stu-id="d0c87-112">Specifies the name of the Automation account in which this cmdlet removes a runbook.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d0c87-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d0c87-113">-DefaultProfile</span></span>
<span data-ttu-id="d0c87-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="d0c87-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d0c87-115">-Force</span><span class="sxs-lookup"><span data-stu-id="d0c87-115">-Force</span></span>
<span data-ttu-id="d0c87-116">ps_force</span><span class="sxs-lookup"><span data-stu-id="d0c87-116">ps_force</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d0c87-117">-Namn</span><span class="sxs-lookup"><span data-stu-id="d0c87-117">-Name</span></span>
<span data-ttu-id="d0c87-118">Anger namnet på den Runbook som cmdleten tar bort.</span><span class="sxs-lookup"><span data-stu-id="d0c87-118">Specifies the name of the runbook that this cmdlet removes.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: RunbookName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d0c87-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d0c87-119">-ResourceGroupName</span></span>
<span data-ttu-id="d0c87-120">Anger namnet på den resurs grupp för vilken denna cmdlet publicerar en Runbook.</span><span class="sxs-lookup"><span data-stu-id="d0c87-120">Specifies the name of the resource group for which this cmdlet publishes a runbook.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d0c87-121">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="d0c87-121">-Confirm</span></span>
<span data-ttu-id="d0c87-122">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="d0c87-122">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d0c87-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d0c87-123">-WhatIf</span></span>
<span data-ttu-id="d0c87-124">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="d0c87-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d0c87-125">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="d0c87-125">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d0c87-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d0c87-126">CommonParameters</span></span>
<span data-ttu-id="d0c87-127">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d0c87-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d0c87-128">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d0c87-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d0c87-129">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="d0c87-129">INPUTS</span></span>

### <span data-ttu-id="d0c87-130">Ingen</span><span class="sxs-lookup"><span data-stu-id="d0c87-130">None</span></span>
<span data-ttu-id="d0c87-131">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="d0c87-131">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="d0c87-132">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="d0c87-132">OUTPUTS</span></span>

## <span data-ttu-id="d0c87-133">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="d0c87-133">NOTES</span></span>

## <span data-ttu-id="d0c87-134">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="d0c87-134">RELATED LINKS</span></span>

[<span data-ttu-id="d0c87-135">Exportera-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="d0c87-135">Export-AzureRmAutomationRunbook</span></span>](./Export-AzureRMAutomationRunbook.md)

[<span data-ttu-id="d0c87-136">Get-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="d0c87-136">Get-AzureRmAutomationRunbook</span></span>](./Get-AzureRMAutomationRunbook.md)

[<span data-ttu-id="d0c87-137">Import-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="d0c87-137">Import-AzureRmAutomationRunbook</span></span>](./Import-AzureRMAutomationRunbook.md)

[<span data-ttu-id="d0c87-138">New-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="d0c87-138">New-AzureRmAutomationRunbook</span></span>](./New-AzureRMAutomationRunbook.md)

[<span data-ttu-id="d0c87-139">New-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="d0c87-139">New-AzureRmAutomationRunbook</span></span>](./New-AzureRMAutomationRunbook.md)

[<span data-ttu-id="d0c87-140">Publicera – AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="d0c87-140">Publish-AzureRmAutomationRunbook</span></span>](./Publish-AzureRMAutomationRunbook.md)

[<span data-ttu-id="d0c87-141">Set-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="d0c87-141">Set-AzureRmAutomationRunbook</span></span>](./Set-AzureRMAutomationRunbook.md)

[<span data-ttu-id="d0c87-142">Start-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="d0c87-142">Start-AzureRmAutomationRunbook</span></span>](./Start-AzureRMAutomationRunbook.md)


