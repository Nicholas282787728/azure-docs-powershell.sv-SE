---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: 515933DF-5DB1-452A-808B-0198A3A2EA8B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/remove-azurermautomationaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Remove-AzureRmAutomationAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Remove-AzureRmAutomationAccount.md
ms.openlocfilehash: 854a5bd2fb9644d6060810edba44ac7082eb6903
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93577261"
---
# <span data-ttu-id="a7ffb-101">Remove-AzureRmAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="a7ffb-101">Remove-AzureRmAutomationAccount</span></span>

## <span data-ttu-id="a7ffb-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="a7ffb-102">SYNOPSIS</span></span>
<span data-ttu-id="a7ffb-103">Tar bort ett Automation-konto.</span><span class="sxs-lookup"><span data-stu-id="a7ffb-103">Removes an Automation account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a7ffb-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="a7ffb-104">SYNTAX</span></span>

```
Remove-AzureRmAutomationAccount [-ResourceGroupName] <String> [-Name] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a7ffb-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="a7ffb-105">DESCRIPTION</span></span>
<span data-ttu-id="a7ffb-106">Cmdleten **Remove-AzureRmAutomationAccount** tar bort ett Azure Automation-konto från en resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="a7ffb-106">The **Remove-AzureRmAutomationAccount** cmdlet removes an Azure Automation account from a resource group.</span></span>

<span data-ttu-id="a7ffb-107">Mer information om automatiserings konton finns i New-AzureRmAutomationAccount cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a7ffb-107">For more information about Automation accounts, see the New-AzureRmAutomationAccount cmdlet.</span></span>

## <span data-ttu-id="a7ffb-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="a7ffb-108">EXAMPLES</span></span>

### <span data-ttu-id="a7ffb-109">Exempel 1: ta bort ett Automation-konto</span><span class="sxs-lookup"><span data-stu-id="a7ffb-109">Example 1: Remove an automation account</span></span>
```
PS C:\>Remove-AzureRmAutomationAccount -Name "ContosoAutomationAccount" -Force -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="a7ffb-110">Det här kommandot tar bort ett Automation-konto med namnet ContosoAutomationAccount utan att fråga efter användar verifiering.</span><span class="sxs-lookup"><span data-stu-id="a7ffb-110">This command removes an automation account named ContosoAutomationAccount without prompting for user validation.</span></span>

## <span data-ttu-id="a7ffb-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="a7ffb-111">PARAMETERS</span></span>

### <span data-ttu-id="a7ffb-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a7ffb-112">-DefaultProfile</span></span>
<span data-ttu-id="a7ffb-113">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="a7ffb-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a7ffb-114">-Force</span><span class="sxs-lookup"><span data-stu-id="a7ffb-114">-Force</span></span>
<span data-ttu-id="a7ffb-115">ps_force</span><span class="sxs-lookup"><span data-stu-id="a7ffb-115">ps_force</span></span>

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

### <span data-ttu-id="a7ffb-116">-Namn</span><span class="sxs-lookup"><span data-stu-id="a7ffb-116">-Name</span></span>
<span data-ttu-id="a7ffb-117">Anger namnet på Automation-kontot som cmdleten tar bort.</span><span class="sxs-lookup"><span data-stu-id="a7ffb-117">Specifies the name of the Automation account that this cmdlet removes.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: AutomationAccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a7ffb-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a7ffb-118">-ResourceGroupName</span></span>
<span data-ttu-id="a7ffb-119">Anger namnet på den resurs grupp från vilken denna cmdlet tar bort ett Automation-konto.</span><span class="sxs-lookup"><span data-stu-id="a7ffb-119">Specifies the name of the resource group from which this cmdlet removes an Automation account.</span></span>

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

### <span data-ttu-id="a7ffb-120">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="a7ffb-120">-Confirm</span></span>
<span data-ttu-id="a7ffb-121">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="a7ffb-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a7ffb-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a7ffb-122">-WhatIf</span></span>
<span data-ttu-id="a7ffb-123">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="a7ffb-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a7ffb-124">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="a7ffb-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a7ffb-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a7ffb-125">CommonParameters</span></span>
<span data-ttu-id="a7ffb-126">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a7ffb-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a7ffb-127">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a7ffb-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a7ffb-128">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="a7ffb-128">INPUTS</span></span>

### <span data-ttu-id="a7ffb-129">Ingen</span><span class="sxs-lookup"><span data-stu-id="a7ffb-129">None</span></span>
<span data-ttu-id="a7ffb-130">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="a7ffb-130">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="a7ffb-131">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="a7ffb-131">OUTPUTS</span></span>

### <span data-ttu-id="a7ffb-132">Microsoft. Azure. commands. Automation. Model. AutomationAccount</span><span class="sxs-lookup"><span data-stu-id="a7ffb-132">Microsoft.Azure.Commands.Automation.Model.AutomationAccount</span></span>

## <span data-ttu-id="a7ffb-133">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="a7ffb-133">NOTES</span></span>

## <span data-ttu-id="a7ffb-134">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="a7ffb-134">RELATED LINKS</span></span>

[<span data-ttu-id="a7ffb-135">Get-AzureRmAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="a7ffb-135">Get-AzureRmAutomationAccount</span></span>](./Get-AzureRmAutomationAccount.md)

[<span data-ttu-id="a7ffb-136">New-AzureRmAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="a7ffb-136">New-AzureRmAutomationAccount</span></span>](./New-AzureRmAutomationAccount.md)

[<span data-ttu-id="a7ffb-137">Set-AzureRmAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="a7ffb-137">Set-AzureRmAutomationAccount</span></span>](./Set-AzureRmAutomationAccount.md)


