---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: B1897EFC-0184-4A8B-B8E4-203CC8E3B179
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/set-azautomationaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Set-AzAutomationAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Set-AzAutomationAccount.md
ms.openlocfilehash: f32e9c0d76e88fba5475abb39595b0a6c4bea834
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94323436"
---
# <span data-ttu-id="92e72-101">Set-AzAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="92e72-101">Set-AzAutomationAccount</span></span>

## <span data-ttu-id="92e72-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="92e72-102">SYNOPSIS</span></span>
<span data-ttu-id="92e72-103">Ändrar ett Automation-konto.</span><span class="sxs-lookup"><span data-stu-id="92e72-103">Modifies an Automation account.</span></span>

## <span data-ttu-id="92e72-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="92e72-104">SYNTAX</span></span>

```
Set-AzAutomationAccount [-ResourceGroupName] <String> [-Name] <String> [-Plan <String>] [-Tags <IDictionary>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="92e72-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="92e72-105">DESCRIPTION</span></span>
<span data-ttu-id="92e72-106">Cmdleten **set-AzAutomationAccount** ändrar ett Azure Automation-konto.</span><span class="sxs-lookup"><span data-stu-id="92e72-106">The **Set-AzAutomationAccount** cmdlet modifies an Azure Automation account.</span></span>
<span data-ttu-id="92e72-107">Mer information om automatiserings konton finns i New-AzAutomationAccount cmdlet.</span><span class="sxs-lookup"><span data-stu-id="92e72-107">For more information about Automation accounts, see the New-AzAutomationAccount cmdlet.</span></span>

## <span data-ttu-id="92e72-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="92e72-108">EXAMPLES</span></span>

### <span data-ttu-id="92e72-109">Exempel 1: Ange taggarna för ett Automation-konto</span><span class="sxs-lookup"><span data-stu-id="92e72-109">Example 1: Set the tags for an Automation account</span></span>
```
PS C:\>$Tags = @{"tag01"="value01";"tag02"="value02"}
PS C:\> Set-AzAutomationAccount -Name "AutomationAccount01" -ResourceGroupName "ResourceGroup01" -Tags $Tags
```

<span data-ttu-id="92e72-110">Det första kommandot tilldelar två par tecken/värdepar till variabeln $Tags.</span><span class="sxs-lookup"><span data-stu-id="92e72-110">The first command assigns two key/value pairs to the $Tags variable.</span></span>
<span data-ttu-id="92e72-111">Det andra kommandot anger Taggar i $Tags för det Automation-konto som heter AutomationAccount01.</span><span class="sxs-lookup"><span data-stu-id="92e72-111">The second command sets tags in $Tags for the Automation account named AutomationAccount01.</span></span>

### <span data-ttu-id="92e72-112">Exempel 2: ändra abonnemanget för ett Automation-konto</span><span class="sxs-lookup"><span data-stu-id="92e72-112">Example 2: Change the plan for an Automation account</span></span>
```
PS C:\>Set-AzAutomationAccount -Name "AutomationAccount01" -ResourceGroupName "ResourceGroup01" -Plan Basic
```

<span data-ttu-id="92e72-113">Det här kommandot ändrar planen till grundläggande för det Automation-konto som heter AutomationAccount01.</span><span class="sxs-lookup"><span data-stu-id="92e72-113">This command changes the plan to Basic for the Automation account named AutomationAccount01.</span></span>

## <span data-ttu-id="92e72-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="92e72-114">PARAMETERS</span></span>

### <span data-ttu-id="92e72-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="92e72-115">-DefaultProfile</span></span>
<span data-ttu-id="92e72-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="92e72-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="92e72-117">-Namn</span><span class="sxs-lookup"><span data-stu-id="92e72-117">-Name</span></span>
<span data-ttu-id="92e72-118">Anger namnet på det Automation-konto som denna cmdlet ändrar.</span><span class="sxs-lookup"><span data-stu-id="92e72-118">Specifies the name of the Automation account that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="92e72-119">-Planera</span><span class="sxs-lookup"><span data-stu-id="92e72-119">-Plan</span></span>
<span data-ttu-id="92e72-120">Anger abonnemanget för Automation-kontot.</span><span class="sxs-lookup"><span data-stu-id="92e72-120">Specifies the plan for the Automation account.</span></span>
<span data-ttu-id="92e72-121">Giltiga värden är:</span><span class="sxs-lookup"><span data-stu-id="92e72-121">Valid values are:</span></span>
- <span data-ttu-id="92e72-122">Basisk</span><span class="sxs-lookup"><span data-stu-id="92e72-122">Basic</span></span>
- <span data-ttu-id="92e72-123">Gratisutdelning</span><span class="sxs-lookup"><span data-stu-id="92e72-123">Free</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Free, Basic

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="92e72-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="92e72-124">-ResourceGroupName</span></span>
<span data-ttu-id="92e72-125">Anger namnet på en resurs grupp som innehåller Automation-kontot som ändras av denna cmdlet.</span><span class="sxs-lookup"><span data-stu-id="92e72-125">Specifies the name of a resource group that contains the Automation account that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="92e72-126">-Taggar</span><span class="sxs-lookup"><span data-stu-id="92e72-126">-Tags</span></span>
<span data-ttu-id="92e72-127">Par med nyckelord i form av en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="92e72-127">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="92e72-128">Till exempel: @ {key0 = "value0"; KEY1 = $null; key2 = "värde2"}</span><span class="sxs-lookup"><span data-stu-id="92e72-128">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: System.Collections.IDictionary
Parameter Sets: (All)
Aliases: Tag

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="92e72-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="92e72-129">CommonParameters</span></span>
<span data-ttu-id="92e72-130">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="92e72-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="92e72-131">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="92e72-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="92e72-132">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="92e72-132">INPUTS</span></span>

### <span data-ttu-id="92e72-133">System. String</span><span class="sxs-lookup"><span data-stu-id="92e72-133">System.String</span></span>

### <span data-ttu-id="92e72-134">System. Collections. IDictionary</span><span class="sxs-lookup"><span data-stu-id="92e72-134">System.Collections.IDictionary</span></span>

## <span data-ttu-id="92e72-135">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="92e72-135">OUTPUTS</span></span>

### <span data-ttu-id="92e72-136">Microsoft. Azure. commands. Automation. Model. AutomationAccount</span><span class="sxs-lookup"><span data-stu-id="92e72-136">Microsoft.Azure.Commands.Automation.Model.AutomationAccount</span></span>

## <span data-ttu-id="92e72-137">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="92e72-137">NOTES</span></span>

## <span data-ttu-id="92e72-138">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="92e72-138">RELATED LINKS</span></span>

[<span data-ttu-id="92e72-139">Get-AzAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="92e72-139">Get-AzAutomationAccount</span></span>](./Get-AzAutomationAccount.md)

[<span data-ttu-id="92e72-140">New-AzAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="92e72-140">New-AzAutomationAccount</span></span>](./New-AzAutomationAccount.md)

[<span data-ttu-id="92e72-141">Remove-AzAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="92e72-141">Remove-AzAutomationAccount</span></span>](./Remove-AzAutomationAccount.md)
