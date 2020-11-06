---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: 515933DF-5DB1-452A-808B-0198A3A2EA8B
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Remove-AzureRmAutomationAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Remove-AzureRmAutomationAccount.md
ms.openlocfilehash: 1b8e480a266459b21e6c357da156b4d4bc5165e8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93578528"
---
# <span data-ttu-id="9573d-101">Remove-AzureRmAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="9573d-101">Remove-AzureRmAutomationAccount</span></span>

## <span data-ttu-id="9573d-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="9573d-102">SYNOPSIS</span></span>
<span data-ttu-id="9573d-103">Tar bort ett Automation-konto.</span><span class="sxs-lookup"><span data-stu-id="9573d-103">Removes an Automation account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9573d-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="9573d-104">SYNTAX</span></span>

```
Remove-AzureRmAutomationAccount [-ResourceGroupName] <String> [-Name] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9573d-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="9573d-105">DESCRIPTION</span></span>
<span data-ttu-id="9573d-106">Cmdleten **Remove-AzureRmAutomationAccount** tar bort ett Azure Automation-konto från en resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="9573d-106">The **Remove-AzureRmAutomationAccount** cmdlet removes an Azure Automation account from a resource group.</span></span>

<span data-ttu-id="9573d-107">Mer information om automatiserings konton finns i New-AzureRmAutomationAccount cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9573d-107">For more information about Automation accounts, see the New-AzureRmAutomationAccount cmdlet.</span></span>

## <span data-ttu-id="9573d-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="9573d-108">EXAMPLES</span></span>

### <span data-ttu-id="9573d-109">Exempel 1: ta bort ett Automation-konto</span><span class="sxs-lookup"><span data-stu-id="9573d-109">Example 1: Remove an automation account</span></span>
```
PS C:\>Remove-AzureRmAutomationAccount -Name "ContosoAutomationAccount" -Force -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="9573d-110">Det här kommandot tar bort ett Automation-konto med namnet ContosoAutomationAccount utan att fråga efter användar verifiering.</span><span class="sxs-lookup"><span data-stu-id="9573d-110">This command removes an automation account named ContosoAutomationAccount without prompting for user validation.</span></span>

## <span data-ttu-id="9573d-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="9573d-111">PARAMETERS</span></span>

### <span data-ttu-id="9573d-112">-Force</span><span class="sxs-lookup"><span data-stu-id="9573d-112">-Force</span></span>
<span data-ttu-id="9573d-113">ps_force</span><span class="sxs-lookup"><span data-stu-id="9573d-113">ps_force</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9573d-114">-Namn</span><span class="sxs-lookup"><span data-stu-id="9573d-114">-Name</span></span>
<span data-ttu-id="9573d-115">Anger namnet på Automation-kontot som cmdleten tar bort.</span><span class="sxs-lookup"><span data-stu-id="9573d-115">Specifies the name of the Automation account that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AutomationAccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9573d-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9573d-116">-ResourceGroupName</span></span>
<span data-ttu-id="9573d-117">Anger namnet på den resurs grupp från vilken denna cmdlet tar bort ett Automation-konto.</span><span class="sxs-lookup"><span data-stu-id="9573d-117">Specifies the name of the resource group from which this cmdlet removes an Automation account.</span></span>

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

### <span data-ttu-id="9573d-118">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="9573d-118">-Confirm</span></span>
<span data-ttu-id="9573d-119">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="9573d-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9573d-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9573d-120">-WhatIf</span></span>
<span data-ttu-id="9573d-121">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="9573d-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9573d-122">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="9573d-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9573d-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9573d-123">-DefaultProfile</span></span>
<span data-ttu-id="9573d-124">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="9573d-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9573d-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9573d-125">CommonParameters</span></span>
<span data-ttu-id="9573d-126">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9573d-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9573d-127">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9573d-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9573d-128">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="9573d-128">INPUTS</span></span>

## <span data-ttu-id="9573d-129">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="9573d-129">OUTPUTS</span></span>

### <span data-ttu-id="9573d-130">Microsoft. Azure. commands. Automation. Model. AutomationAccount</span><span class="sxs-lookup"><span data-stu-id="9573d-130">Microsoft.Azure.Commands.Automation.Model.AutomationAccount</span></span>

## <span data-ttu-id="9573d-131">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="9573d-131">NOTES</span></span>

## <span data-ttu-id="9573d-132">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="9573d-132">RELATED LINKS</span></span>

[<span data-ttu-id="9573d-133">Get-AzureRmAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="9573d-133">Get-AzureRmAutomationAccount</span></span>](./Get-AzureRmAutomationAccount.md)

[<span data-ttu-id="9573d-134">New-AzureRmAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="9573d-134">New-AzureRmAutomationAccount</span></span>](./New-AzureRmAutomationAccount.md)

[<span data-ttu-id="9573d-135">Set-AzureRmAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="9573d-135">Set-AzureRmAutomationAccount</span></span>](./Set-AzureRmAutomationAccount.md)


