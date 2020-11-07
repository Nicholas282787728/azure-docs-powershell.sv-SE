---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: B53B765F-5CFC-4BF8-A48A-E638A73E1FC5
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/remove-azurermautomationcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Remove-AzureRMAutomationCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Remove-AzureRMAutomationCredential.md
ms.openlocfilehash: 11b6772325c3e5170c697b21d25092fd96f3e2e9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93757955"
---
# <span data-ttu-id="9fb52-101">Remove-AzureRmAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="9fb52-101">Remove-AzureRmAutomationCredential</span></span>

## <span data-ttu-id="9fb52-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="9fb52-102">SYNOPSIS</span></span>
<span data-ttu-id="9fb52-103">Tar bort en automatiserings autentiseringsuppgift.</span><span class="sxs-lookup"><span data-stu-id="9fb52-103">Removes an Automation credential.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9fb52-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="9fb52-104">SYNTAX</span></span>

```
Remove-AzureRmAutomationCredential [-Name] <String> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="9fb52-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="9fb52-105">DESCRIPTION</span></span>
<span data-ttu-id="9fb52-106">Cmdleten **Remove-AzureRmAutomationCredential** tar bort en autentiseringsuppgift från Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="9fb52-106">The **Remove-AzureRmAutomationCredential** cmdlet removes a credential from Azure Automation.</span></span>

## <span data-ttu-id="9fb52-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="9fb52-107">EXAMPLES</span></span>

### <span data-ttu-id="9fb52-108">Exempel 1: ta bort en autentiseringsuppgift</span><span class="sxs-lookup"><span data-stu-id="9fb52-108">Example 1: Remove a credential</span></span>
```
PS C:\>Remove-AzureRmAutomationCredential -AutomationAccountName "Contoso17" -Name "ContosoCredential" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="9fb52-109">Det här kommandot tar bort en autentiseringsuppgift som heter ContosoCredential i Azure Automation-kontot med namnet Contoso17.</span><span class="sxs-lookup"><span data-stu-id="9fb52-109">This command removes a credential named ContosoCredential in the Azure Automation account named Contoso17.</span></span>

## <span data-ttu-id="9fb52-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="9fb52-110">PARAMETERS</span></span>

### <span data-ttu-id="9fb52-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="9fb52-111">-AutomationAccountName</span></span>
<span data-ttu-id="9fb52-112">Anger namnet på det Automation-konto som den här cmdleten tar bort en autentiseringsuppgift från.</span><span class="sxs-lookup"><span data-stu-id="9fb52-112">Specifies the name of the Automation account from which this cmdlet removes a credential.</span></span>

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

### <span data-ttu-id="9fb52-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9fb52-113">-DefaultProfile</span></span>
<span data-ttu-id="9fb52-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="9fb52-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="9fb52-115">-Namn</span><span class="sxs-lookup"><span data-stu-id="9fb52-115">-Name</span></span>
<span data-ttu-id="9fb52-116">Anger namnet på den autentiseringsuppgift som denna cmdlet tar bort.</span><span class="sxs-lookup"><span data-stu-id="9fb52-116">Specifies the name of the credential that this cmdlet removes.</span></span>

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

### <span data-ttu-id="9fb52-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9fb52-117">-ResourceGroupName</span></span>
<span data-ttu-id="9fb52-118">Anger namnet på den resurs grupp som den här cmdleten tar bort en autentiseringsuppgift för.</span><span class="sxs-lookup"><span data-stu-id="9fb52-118">Specifies the name of the resource group for which this cmdlet removes a credential.</span></span>

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

### <span data-ttu-id="9fb52-119">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="9fb52-119">-Confirm</span></span>
<span data-ttu-id="9fb52-120">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="9fb52-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9fb52-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9fb52-121">-WhatIf</span></span>
<span data-ttu-id="9fb52-122">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="9fb52-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9fb52-123">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="9fb52-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9fb52-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9fb52-124">CommonParameters</span></span>
<span data-ttu-id="9fb52-125">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9fb52-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9fb52-126">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9fb52-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9fb52-127">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="9fb52-127">INPUTS</span></span>

### <span data-ttu-id="9fb52-128">Ingen</span><span class="sxs-lookup"><span data-stu-id="9fb52-128">None</span></span>
<span data-ttu-id="9fb52-129">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="9fb52-129">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="9fb52-130">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="9fb52-130">OUTPUTS</span></span>

## <span data-ttu-id="9fb52-131">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="9fb52-131">NOTES</span></span>

## <span data-ttu-id="9fb52-132">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="9fb52-132">RELATED LINKS</span></span>

[<span data-ttu-id="9fb52-133">Get-AzureRmAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="9fb52-133">Get-AzureRmAutomationCredential</span></span>](./Get-AzureRMAutomationCredential.md)

[<span data-ttu-id="9fb52-134">New-AzureRmAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="9fb52-134">New-AzureRmAutomationCredential</span></span>](./New-AzureRMAutomationCredential.md)

[<span data-ttu-id="9fb52-135">Set-AzureRmAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="9fb52-135">Set-AzureRmAutomationCredential</span></span>](./Set-AzureRMAutomationCredential.md)


