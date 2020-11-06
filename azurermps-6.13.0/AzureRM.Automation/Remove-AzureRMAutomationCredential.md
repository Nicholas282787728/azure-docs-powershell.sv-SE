---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: B53B765F-5CFC-4BF8-A48A-E638A73E1FC5
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/remove-azurermautomationcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Remove-AzureRMAutomationCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Remove-AzureRMAutomationCredential.md
ms.openlocfilehash: 6c0fe1185bfa8d5233371788da87e7a13fe32c6f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93574045"
---
# <span data-ttu-id="8b0f9-101">Remove-AzureRmAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="8b0f9-101">Remove-AzureRmAutomationCredential</span></span>

## <span data-ttu-id="8b0f9-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="8b0f9-102">SYNOPSIS</span></span>
<span data-ttu-id="8b0f9-103">Tar bort en automatiserings autentiseringsuppgift.</span><span class="sxs-lookup"><span data-stu-id="8b0f9-103">Removes an Automation credential.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8b0f9-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="8b0f9-104">SYNTAX</span></span>

```
Remove-AzureRmAutomationCredential [-Name] <String> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="8b0f9-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="8b0f9-105">DESCRIPTION</span></span>
<span data-ttu-id="8b0f9-106">Cmdleten **Remove-AzureRmAutomationCredential** tar bort en autentiseringsuppgift från Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="8b0f9-106">The **Remove-AzureRmAutomationCredential** cmdlet removes a credential from Azure Automation.</span></span>

## <span data-ttu-id="8b0f9-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="8b0f9-107">EXAMPLES</span></span>

### <span data-ttu-id="8b0f9-108">Exempel 1: ta bort en autentiseringsuppgift</span><span class="sxs-lookup"><span data-stu-id="8b0f9-108">Example 1: Remove a credential</span></span>
```
PS C:\>Remove-AzureRmAutomationCredential -AutomationAccountName "Contoso17" -Name "ContosoCredential" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="8b0f9-109">Det här kommandot tar bort en autentiseringsuppgift som heter ContosoCredential i Azure Automation-kontot med namnet Contoso17.</span><span class="sxs-lookup"><span data-stu-id="8b0f9-109">This command removes a credential named ContosoCredential in the Azure Automation account named Contoso17.</span></span>

## <span data-ttu-id="8b0f9-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="8b0f9-110">PARAMETERS</span></span>

### <span data-ttu-id="8b0f9-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="8b0f9-111">-AutomationAccountName</span></span>
<span data-ttu-id="8b0f9-112">Anger namnet på det Automation-konto som den här cmdleten tar bort en autentiseringsuppgift från.</span><span class="sxs-lookup"><span data-stu-id="8b0f9-112">Specifies the name of the Automation account from which this cmdlet removes a credential.</span></span>

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

### <span data-ttu-id="8b0f9-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8b0f9-113">-DefaultProfile</span></span>
<span data-ttu-id="8b0f9-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="8b0f9-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="8b0f9-115">-Namn</span><span class="sxs-lookup"><span data-stu-id="8b0f9-115">-Name</span></span>
<span data-ttu-id="8b0f9-116">Anger namnet på den autentiseringsuppgift som denna cmdlet tar bort.</span><span class="sxs-lookup"><span data-stu-id="8b0f9-116">Specifies the name of the credential that this cmdlet removes.</span></span>

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

### <span data-ttu-id="8b0f9-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8b0f9-117">-ResourceGroupName</span></span>
<span data-ttu-id="8b0f9-118">Anger namnet på den resurs grupp som den här cmdleten tar bort en autentiseringsuppgift för.</span><span class="sxs-lookup"><span data-stu-id="8b0f9-118">Specifies the name of the resource group for which this cmdlet removes a credential.</span></span>

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

### <span data-ttu-id="8b0f9-119">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="8b0f9-119">-Confirm</span></span>
<span data-ttu-id="8b0f9-120">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="8b0f9-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8b0f9-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8b0f9-121">-WhatIf</span></span>
<span data-ttu-id="8b0f9-122">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="8b0f9-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8b0f9-123">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="8b0f9-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8b0f9-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8b0f9-124">CommonParameters</span></span>
<span data-ttu-id="8b0f9-125">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8b0f9-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8b0f9-126">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8b0f9-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8b0f9-127">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="8b0f9-127">INPUTS</span></span>

### <span data-ttu-id="8b0f9-128">System. String</span><span class="sxs-lookup"><span data-stu-id="8b0f9-128">System.String</span></span>

## <span data-ttu-id="8b0f9-129">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="8b0f9-129">OUTPUTS</span></span>

### <span data-ttu-id="8b0f9-130">System. Void</span><span class="sxs-lookup"><span data-stu-id="8b0f9-130">System.Void</span></span>

## <span data-ttu-id="8b0f9-131">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="8b0f9-131">NOTES</span></span>

## <span data-ttu-id="8b0f9-132">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="8b0f9-132">RELATED LINKS</span></span>

[<span data-ttu-id="8b0f9-133">Get-AzureRmAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="8b0f9-133">Get-AzureRmAutomationCredential</span></span>](./Get-AzureRMAutomationCredential.md)

[<span data-ttu-id="8b0f9-134">New-AzureRmAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="8b0f9-134">New-AzureRmAutomationCredential</span></span>](./New-AzureRMAutomationCredential.md)

[<span data-ttu-id="8b0f9-135">Set-AzureRmAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="8b0f9-135">Set-AzureRmAutomationCredential</span></span>](./Set-AzureRMAutomationCredential.md)


