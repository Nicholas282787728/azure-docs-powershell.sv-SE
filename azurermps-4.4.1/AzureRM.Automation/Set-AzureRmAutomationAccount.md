---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: B1897EFC-0184-4A8B-B8E4-203CC8E3B179
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Set-AzureRmAutomationAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Set-AzureRmAutomationAccount.md
ms.openlocfilehash: 8ad63c37c366c0f9c7693585f3a3c2fd57de4fdd
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93575036"
---
# <span data-ttu-id="d0568-101">Set-AzureRmAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="d0568-101">Set-AzureRmAutomationAccount</span></span>

## <span data-ttu-id="d0568-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="d0568-102">SYNOPSIS</span></span>
<span data-ttu-id="d0568-103">Ändrar ett Automation-konto.</span><span class="sxs-lookup"><span data-stu-id="d0568-103">Modifies an Automation account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d0568-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="d0568-104">SYNTAX</span></span>

```
Set-AzureRmAutomationAccount [-ResourceGroupName] <String> [-Name] <String> [-Plan <String>]
 [-Tags <IDictionary>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d0568-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="d0568-105">DESCRIPTION</span></span>
<span data-ttu-id="d0568-106">Cmdleten **set-AzureRmAutomationAccount** ändrar ett Azure Automation-konto.</span><span class="sxs-lookup"><span data-stu-id="d0568-106">The **Set-AzureRmAutomationAccount** cmdlet modifies an Azure Automation account.</span></span>

<span data-ttu-id="d0568-107">Mer information om automatiserings konton finns i New-AzureRmAutomationAccount cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d0568-107">For more information about Automation accounts, see the New-AzureRmAutomationAccount cmdlet.</span></span>

## <span data-ttu-id="d0568-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="d0568-108">EXAMPLES</span></span>

### <span data-ttu-id="d0568-109">Exempel 1: Ange taggarna för ett Automation-konto</span><span class="sxs-lookup"><span data-stu-id="d0568-109">Example 1: Set the tags for an Automation account</span></span>
```
PS C:\>$Tags = @{"tag01"="value01";"tag02"="value02"}
PS C:\> Set-AzureRmAutomationAccount -Name "AutomationAccount01" -ResourceGroupName "ResourceGroup01" -Tags $Tags
```

<span data-ttu-id="d0568-110">Det första kommandot tilldelar två par tecken/värdepar till variabeln $Tags.</span><span class="sxs-lookup"><span data-stu-id="d0568-110">The first command assigns two key/value pairs to the $Tags variable.</span></span>

<span data-ttu-id="d0568-111">Det andra kommandot anger Taggar i $Tags för det Automation-konto som heter AutomationAccount01.</span><span class="sxs-lookup"><span data-stu-id="d0568-111">The second command sets tags in $Tags for the Automation account named AutomationAccount01.</span></span>

### <span data-ttu-id="d0568-112">Exempel 2: ändra abonnemanget för ett Automation-konto</span><span class="sxs-lookup"><span data-stu-id="d0568-112">Example 2: Change the plan for an Automation account</span></span>
```
PS C:\>Set-AzureRmAutomationAccount -Name "AutomationAccount01" -ResourceGroupName "ResourceGroup01" -Plan Basic
```

<span data-ttu-id="d0568-113">Det här kommandot ändrar planen till grundläggande för det Automation-konto som heter AutomationAccount01.</span><span class="sxs-lookup"><span data-stu-id="d0568-113">This command changes the plan to Basic for the Automation account named AutomationAccount01.</span></span>

## <span data-ttu-id="d0568-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="d0568-114">PARAMETERS</span></span>

### <span data-ttu-id="d0568-115">-Namn</span><span class="sxs-lookup"><span data-stu-id="d0568-115">-Name</span></span>
<span data-ttu-id="d0568-116">Anger namnet på det Automation-konto som denna cmdlet ändrar.</span><span class="sxs-lookup"><span data-stu-id="d0568-116">Specifies the name of the Automation account that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="d0568-117">-Planera</span><span class="sxs-lookup"><span data-stu-id="d0568-117">-Plan</span></span>
<span data-ttu-id="d0568-118">Anger abonnemanget för Automation-kontot.</span><span class="sxs-lookup"><span data-stu-id="d0568-118">Specifies the plan for the Automation account.</span></span>
<span data-ttu-id="d0568-119">Giltiga värden är:</span><span class="sxs-lookup"><span data-stu-id="d0568-119">Valid values are:</span></span>

- <span data-ttu-id="d0568-120">Basisk</span><span class="sxs-lookup"><span data-stu-id="d0568-120">Basic</span></span>
- <span data-ttu-id="d0568-121">Gratisutdelning</span><span class="sxs-lookup"><span data-stu-id="d0568-121">Free</span></span>

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

### <span data-ttu-id="d0568-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d0568-122">-ResourceGroupName</span></span>
<span data-ttu-id="d0568-123">Anger namnet på en resurs grupp som innehåller Automation-kontot som ändras av denna cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d0568-123">Specifies the name of a resource group that contains the Automation account that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="d0568-124">-Taggar</span><span class="sxs-lookup"><span data-stu-id="d0568-124">-Tags</span></span>
<span data-ttu-id="d0568-125">Par med nyckelord i form av en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="d0568-125">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="d0568-126">Till exempel:</span><span class="sxs-lookup"><span data-stu-id="d0568-126">For example:</span></span>

<span data-ttu-id="d0568-127">@ {key0 = "value0"; KEY1 = $null; key2 = "värde2"}</span><span class="sxs-lookup"><span data-stu-id="d0568-127">@{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="d0568-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d0568-128">-DefaultProfile</span></span>
<span data-ttu-id="d0568-129">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="d0568-129">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d0568-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d0568-130">CommonParameters</span></span>
<span data-ttu-id="d0568-131">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d0568-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d0568-132">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d0568-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d0568-133">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="d0568-133">INPUTS</span></span>

## <span data-ttu-id="d0568-134">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="d0568-134">OUTPUTS</span></span>

### <span data-ttu-id="d0568-135">Microsoft. Azure. commands. Automation. Model. AutomationAccount</span><span class="sxs-lookup"><span data-stu-id="d0568-135">Microsoft.Azure.Commands.Automation.Model.AutomationAccount</span></span>

## <span data-ttu-id="d0568-136">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="d0568-136">NOTES</span></span>

## <span data-ttu-id="d0568-137">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="d0568-137">RELATED LINKS</span></span>

[<span data-ttu-id="d0568-138">Get-AzureRmAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="d0568-138">Get-AzureRmAutomationAccount</span></span>](./Get-AzureRmAutomationAccount.md)

[<span data-ttu-id="d0568-139">New-AzureRmAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="d0568-139">New-AzureRmAutomationAccount</span></span>](./New-AzureRmAutomationAccount.md)

[<span data-ttu-id="d0568-140">Remove-AzureRmAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="d0568-140">Remove-AzureRmAutomationAccount</span></span>](./Remove-AzureRmAutomationAccount.md)
