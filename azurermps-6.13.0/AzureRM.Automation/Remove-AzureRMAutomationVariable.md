---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: 760C03A0-12DB-43C4-A180-B013FA77A513
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/remove-azurermautomationvariable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Remove-AzureRMAutomationVariable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Remove-AzureRMAutomationVariable.md
ms.openlocfilehash: b336104fea097b0f5adf0993853dd6fff7bba1f4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93756413"
---
# <span data-ttu-id="908b9-101">Remove-AzureRmAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="908b9-101">Remove-AzureRmAutomationVariable</span></span>

## <span data-ttu-id="908b9-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="908b9-102">SYNOPSIS</span></span>
<span data-ttu-id="908b9-103">Tar bort en Automation-variabel.</span><span class="sxs-lookup"><span data-stu-id="908b9-103">Removes an Automation variable.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="908b9-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="908b9-104">SYNTAX</span></span>

```
Remove-AzureRmAutomationVariable [-Name] <String> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="908b9-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="908b9-105">DESCRIPTION</span></span>
<span data-ttu-id="908b9-106">Cmdleten **Remove-AzureRmAutomationVariable** tar bort en variabel från Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="908b9-106">The **Remove-AzureRmAutomationVariable** cmdlet removes a variable from Azure Automation.</span></span>

## <span data-ttu-id="908b9-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="908b9-107">EXAMPLES</span></span>

### <span data-ttu-id="908b9-108">Exempel 1: ta bort en variabel</span><span class="sxs-lookup"><span data-stu-id="908b9-108">Example 1: Remove a variable</span></span>
```
PS C:\>Remove-AzureRmAutomationVariable -AutomationAccountName "Contoso17" -Name "StringVariable22" -Force -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="908b9-109">Det här kommandot tar bort en variabel som heter StringVariable22 i Automation-kontot med namnet Contoso17.</span><span class="sxs-lookup"><span data-stu-id="908b9-109">This command removes a variable named StringVariable22 in the Automation account named Contoso17.</span></span>
<span data-ttu-id="908b9-110">Det här kommandot anger parametern *Force* .</span><span class="sxs-lookup"><span data-stu-id="908b9-110">This command specifies the *Force* parameter.</span></span>
<span data-ttu-id="908b9-111">Därför behöver du inte bekräfta.</span><span class="sxs-lookup"><span data-stu-id="908b9-111">Therefore, it does not prompt you for confirmation.</span></span>

## <span data-ttu-id="908b9-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="908b9-112">PARAMETERS</span></span>

### <span data-ttu-id="908b9-113">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="908b9-113">-AutomationAccountName</span></span>
<span data-ttu-id="908b9-114">Anger namnet på det Automation-konto som innehåller den variabel som cmdleten tar bort.</span><span class="sxs-lookup"><span data-stu-id="908b9-114">Specifies the name of the Automation account that contains the variable that this cmdlet deletes.</span></span>

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

### <span data-ttu-id="908b9-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="908b9-115">-DefaultProfile</span></span>
<span data-ttu-id="908b9-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="908b9-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="908b9-117">-Namn</span><span class="sxs-lookup"><span data-stu-id="908b9-117">-Name</span></span>
<span data-ttu-id="908b9-118">Anger namnet på den variabel som denna cmdlet tar bort.</span><span class="sxs-lookup"><span data-stu-id="908b9-118">Specifies the name of the variable that this cmdlet deletes.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="908b9-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="908b9-119">-ResourceGroupName</span></span>
<span data-ttu-id="908b9-120">Anger den resurs grupp för vilken denna cmdlet tar bort en variabel.</span><span class="sxs-lookup"><span data-stu-id="908b9-120">Specifies the resource group for which this cmdlet deletes a variable.</span></span>

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

### <span data-ttu-id="908b9-121">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="908b9-121">-Confirm</span></span>
<span data-ttu-id="908b9-122">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="908b9-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="908b9-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="908b9-123">-WhatIf</span></span>
<span data-ttu-id="908b9-124">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="908b9-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="908b9-125">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="908b9-125">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="908b9-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="908b9-126">CommonParameters</span></span>
<span data-ttu-id="908b9-127">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="908b9-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="908b9-128">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="908b9-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="908b9-129">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="908b9-129">INPUTS</span></span>

### <span data-ttu-id="908b9-130">System. String</span><span class="sxs-lookup"><span data-stu-id="908b9-130">System.String</span></span>

## <span data-ttu-id="908b9-131">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="908b9-131">OUTPUTS</span></span>

### <span data-ttu-id="908b9-132">System. Void</span><span class="sxs-lookup"><span data-stu-id="908b9-132">System.Void</span></span>

## <span data-ttu-id="908b9-133">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="908b9-133">NOTES</span></span>

## <span data-ttu-id="908b9-134">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="908b9-134">RELATED LINKS</span></span>

[<span data-ttu-id="908b9-135">Get-AzureRmAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="908b9-135">Get-AzureRmAutomationVariable</span></span>](./Get-AzureRMAutomationVariable.md)

[<span data-ttu-id="908b9-136">New-AzureRmAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="908b9-136">New-AzureRmAutomationVariable</span></span>](./New-AzureRMAutomationVariable.md)

[<span data-ttu-id="908b9-137">Set-AzureRmAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="908b9-137">Set-AzureRmAutomationVariable</span></span>](./Set-AzureRMAutomationVariable.md)


