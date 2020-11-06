---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: 5F45A12C-BB50-4732-BE80-188491DEF8B5
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Remove-AzureRmAutomationModule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Remove-AzureRmAutomationModule.md
ms.openlocfilehash: 42fc322e9f593ecad6c295952d46274eb2563799
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93578512"
---
# <span data-ttu-id="829fd-101">Remove-AzureRmAutomationModule</span><span class="sxs-lookup"><span data-stu-id="829fd-101">Remove-AzureRmAutomationModule</span></span>

## <span data-ttu-id="829fd-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="829fd-102">SYNOPSIS</span></span>
<span data-ttu-id="829fd-103">Tar bort en modul från Automation.</span><span class="sxs-lookup"><span data-stu-id="829fd-103">Removes a module from Automation.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="829fd-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="829fd-104">SYNTAX</span></span>

```
Remove-AzureRmAutomationModule [-Name] <String> [-Force] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="829fd-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="829fd-105">DESCRIPTION</span></span>
<span data-ttu-id="829fd-106">Cmdleten **Remove-AzureRmAutomationModule** tar bort en modul från ett Automation-konto i Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="829fd-106">The **Remove-AzureRmAutomationModule** cmdlet removes a module from an Automation account in Azure Automation.</span></span>

## <span data-ttu-id="829fd-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="829fd-107">EXAMPLES</span></span>

### <span data-ttu-id="829fd-108">Exempel 1: ta bort en modul</span><span class="sxs-lookup"><span data-stu-id="829fd-108">Example 1: Remove a module</span></span>
```
PS C:\>Remove-AzureRmAutomationModule -AutomationAccountName "Contoso17" -Name "ContosoModule" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="829fd-109">Det här kommandot tar bort en modul som heter ContosoModule från Automation-kontot med namnet Contoso17.</span><span class="sxs-lookup"><span data-stu-id="829fd-109">This command removes a module named ContosoModule from the Automation account named Contoso17.</span></span>

## <span data-ttu-id="829fd-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="829fd-110">PARAMETERS</span></span>

### <span data-ttu-id="829fd-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="829fd-111">-AutomationAccountName</span></span>
<span data-ttu-id="829fd-112">Anger namnet på det Automation-konto som den här cmdleten tar bort en modul från.</span><span class="sxs-lookup"><span data-stu-id="829fd-112">Specifies the name of the Automation account from which this cmdlet removes a module.</span></span>

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

### <span data-ttu-id="829fd-113">-Force</span><span class="sxs-lookup"><span data-stu-id="829fd-113">-Force</span></span>
<span data-ttu-id="829fd-114">ps_force</span><span class="sxs-lookup"><span data-stu-id="829fd-114">ps_force</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="829fd-115">-Namn</span><span class="sxs-lookup"><span data-stu-id="829fd-115">-Name</span></span>
<span data-ttu-id="829fd-116">Anger namnet på den modul som cmdleten tar bort.</span><span class="sxs-lookup"><span data-stu-id="829fd-116">Specifies the name of the module that this cmdlet removes.</span></span>

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

### <span data-ttu-id="829fd-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="829fd-117">-ResourceGroupName</span></span>
<span data-ttu-id="829fd-118">Anger namnet på en resurs grupp där denna cmdlet tar bort en modul.</span><span class="sxs-lookup"><span data-stu-id="829fd-118">Specifies the name of a resource group in which this cmdlet removes a module.</span></span>

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

### <span data-ttu-id="829fd-119">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="829fd-119">-Confirm</span></span>
<span data-ttu-id="829fd-120">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="829fd-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="829fd-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="829fd-121">-WhatIf</span></span>
<span data-ttu-id="829fd-122">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="829fd-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="829fd-123">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="829fd-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="829fd-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="829fd-124">-DefaultProfile</span></span>
<span data-ttu-id="829fd-125">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="829fd-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="829fd-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="829fd-126">CommonParameters</span></span>
<span data-ttu-id="829fd-127">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="829fd-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="829fd-128">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="829fd-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="829fd-129">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="829fd-129">INPUTS</span></span>

## <span data-ttu-id="829fd-130">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="829fd-130">OUTPUTS</span></span>

## <span data-ttu-id="829fd-131">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="829fd-131">NOTES</span></span>

## <span data-ttu-id="829fd-132">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="829fd-132">RELATED LINKS</span></span>

[<span data-ttu-id="829fd-133">Get-AzureRmAutomationModule</span><span class="sxs-lookup"><span data-stu-id="829fd-133">Get-AzureRmAutomationModule</span></span>](./Get-AzureRmAutomationModule.md)

[<span data-ttu-id="829fd-134">New-AzureRmAutomationModule</span><span class="sxs-lookup"><span data-stu-id="829fd-134">New-AzureRmAutomationModule</span></span>](./New-AzureRmAutomationModule.md)

[<span data-ttu-id="829fd-135">Set-AzureRmAutomationModule</span><span class="sxs-lookup"><span data-stu-id="829fd-135">Set-AzureRmAutomationModule</span></span>](./Set-AzureRmAutomationModule.md)


