---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: 5F45A12C-BB50-4732-BE80-188491DEF8B5
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/remove-azurermautomationmodule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Remove-AzureRmAutomationModule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Remove-AzureRmAutomationModule.md
ms.openlocfilehash: 2ce97441769c15ed122dc7921554b4fa1c5a144f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93586400"
---
# <span data-ttu-id="8f364-101">Remove-AzureRmAutomationModule</span><span class="sxs-lookup"><span data-stu-id="8f364-101">Remove-AzureRmAutomationModule</span></span>

## <span data-ttu-id="8f364-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="8f364-102">SYNOPSIS</span></span>
<span data-ttu-id="8f364-103">Tar bort en modul från Automation.</span><span class="sxs-lookup"><span data-stu-id="8f364-103">Removes a module from Automation.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8f364-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="8f364-104">SYNTAX</span></span>

```
Remove-AzureRmAutomationModule [-Name] <String> [-Force] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="8f364-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="8f364-105">DESCRIPTION</span></span>
<span data-ttu-id="8f364-106">Cmdleten **Remove-AzureRmAutomationModule** tar bort en modul från ett Automation-konto i Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="8f364-106">The **Remove-AzureRmAutomationModule** cmdlet removes a module from an Automation account in Azure Automation.</span></span>

## <span data-ttu-id="8f364-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="8f364-107">EXAMPLES</span></span>

### <span data-ttu-id="8f364-108">Exempel 1: ta bort en modul</span><span class="sxs-lookup"><span data-stu-id="8f364-108">Example 1: Remove a module</span></span>
```
PS C:\>Remove-AzureRmAutomationModule -AutomationAccountName "Contoso17" -Name "ContosoModule" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="8f364-109">Det här kommandot tar bort en modul som heter ContosoModule från Automation-kontot med namnet Contoso17.</span><span class="sxs-lookup"><span data-stu-id="8f364-109">This command removes a module named ContosoModule from the Automation account named Contoso17.</span></span>

## <span data-ttu-id="8f364-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="8f364-110">PARAMETERS</span></span>

### <span data-ttu-id="8f364-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="8f364-111">-AutomationAccountName</span></span>
<span data-ttu-id="8f364-112">Anger namnet på det Automation-konto som den här cmdleten tar bort en modul från.</span><span class="sxs-lookup"><span data-stu-id="8f364-112">Specifies the name of the Automation account from which this cmdlet removes a module.</span></span>

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

### <span data-ttu-id="8f364-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8f364-113">-DefaultProfile</span></span>
<span data-ttu-id="8f364-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="8f364-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="8f364-115">-Force</span><span class="sxs-lookup"><span data-stu-id="8f364-115">-Force</span></span>
<span data-ttu-id="8f364-116">ps_force</span><span class="sxs-lookup"><span data-stu-id="8f364-116">ps_force</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8f364-117">-Namn</span><span class="sxs-lookup"><span data-stu-id="8f364-117">-Name</span></span>
<span data-ttu-id="8f364-118">Anger namnet på den modul som cmdleten tar bort.</span><span class="sxs-lookup"><span data-stu-id="8f364-118">Specifies the name of the module that this cmdlet removes.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8f364-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8f364-119">-ResourceGroupName</span></span>
<span data-ttu-id="8f364-120">Anger namnet på en resurs grupp där denna cmdlet tar bort en modul.</span><span class="sxs-lookup"><span data-stu-id="8f364-120">Specifies the name of a resource group in which this cmdlet removes a module.</span></span>

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

### <span data-ttu-id="8f364-121">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="8f364-121">-Confirm</span></span>
<span data-ttu-id="8f364-122">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="8f364-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8f364-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8f364-123">-WhatIf</span></span>
<span data-ttu-id="8f364-124">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="8f364-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8f364-125">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="8f364-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8f364-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8f364-126">CommonParameters</span></span>
<span data-ttu-id="8f364-127">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8f364-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8f364-128">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8f364-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8f364-129">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="8f364-129">INPUTS</span></span>

### <span data-ttu-id="8f364-130">Ingen</span><span class="sxs-lookup"><span data-stu-id="8f364-130">None</span></span>
<span data-ttu-id="8f364-131">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="8f364-131">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="8f364-132">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="8f364-132">OUTPUTS</span></span>

## <span data-ttu-id="8f364-133">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="8f364-133">NOTES</span></span>

## <span data-ttu-id="8f364-134">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="8f364-134">RELATED LINKS</span></span>

[<span data-ttu-id="8f364-135">Get-AzureRmAutomationModule</span><span class="sxs-lookup"><span data-stu-id="8f364-135">Get-AzureRmAutomationModule</span></span>](./Get-AzureRmAutomationModule.md)

[<span data-ttu-id="8f364-136">New-AzureRmAutomationModule</span><span class="sxs-lookup"><span data-stu-id="8f364-136">New-AzureRmAutomationModule</span></span>](./New-AzureRmAutomationModule.md)

[<span data-ttu-id="8f364-137">Set-AzureRmAutomationModule</span><span class="sxs-lookup"><span data-stu-id="8f364-137">Set-AzureRmAutomationModule</span></span>](./Set-AzureRmAutomationModule.md)


