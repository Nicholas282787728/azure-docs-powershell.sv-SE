---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: B1897EFC-0184-4A8B-B8E4-203CC8E3B179
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/set-azurermautomationaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Set-AzureRmAutomationAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Set-AzureRmAutomationAccount.md
ms.openlocfilehash: bbb90e728c9c43c011c4610ee47273af1fdae668
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93579659"
---
# <span data-ttu-id="4f4e8-101">Set-AzureRmAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="4f4e8-101">Set-AzureRmAutomationAccount</span></span>

## <span data-ttu-id="4f4e8-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="4f4e8-102">SYNOPSIS</span></span>
<span data-ttu-id="4f4e8-103">Ändrar ett Automation-konto.</span><span class="sxs-lookup"><span data-stu-id="4f4e8-103">Modifies an Automation account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4f4e8-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="4f4e8-104">SYNTAX</span></span>

```
Set-AzureRmAutomationAccount [-ResourceGroupName] <String> [-Name] <String> [-Plan <String>]
 [-Tags <IDictionary>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4f4e8-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="4f4e8-105">DESCRIPTION</span></span>
<span data-ttu-id="4f4e8-106">Cmdleten **set-AzureRmAutomationAccount** ändrar ett Azure Automation-konto.</span><span class="sxs-lookup"><span data-stu-id="4f4e8-106">The **Set-AzureRmAutomationAccount** cmdlet modifies an Azure Automation account.</span></span>

<span data-ttu-id="4f4e8-107">Mer information om automatiserings konton finns i New-AzureRmAutomationAccount cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4f4e8-107">For more information about Automation accounts, see the New-AzureRmAutomationAccount cmdlet.</span></span>

## <span data-ttu-id="4f4e8-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="4f4e8-108">EXAMPLES</span></span>

### <span data-ttu-id="4f4e8-109">Exempel 1: Ange taggarna för ett Automation-konto</span><span class="sxs-lookup"><span data-stu-id="4f4e8-109">Example 1: Set the tags for an Automation account</span></span>
```
PS C:\>$Tags = @{"tag01"="value01";"tag02"="value02"}
PS C:\> Set-AzureRmAutomationAccount -Name "AutomationAccount01" -ResourceGroupName "ResourceGroup01" -Tags $Tags
```

<span data-ttu-id="4f4e8-110">Det första kommandot tilldelar två par tecken/värdepar till variabeln $Tags.</span><span class="sxs-lookup"><span data-stu-id="4f4e8-110">The first command assigns two key/value pairs to the $Tags variable.</span></span>

<span data-ttu-id="4f4e8-111">Det andra kommandot anger Taggar i $Tags för det Automation-konto som heter AutomationAccount01.</span><span class="sxs-lookup"><span data-stu-id="4f4e8-111">The second command sets tags in $Tags for the Automation account named AutomationAccount01.</span></span>

### <span data-ttu-id="4f4e8-112">Exempel 2: ändra abonnemanget för ett Automation-konto</span><span class="sxs-lookup"><span data-stu-id="4f4e8-112">Example 2: Change the plan for an Automation account</span></span>
```
PS C:\>Set-AzureRmAutomationAccount -Name "AutomationAccount01" -ResourceGroupName "ResourceGroup01" -Plan Basic
```

<span data-ttu-id="4f4e8-113">Det här kommandot ändrar planen till grundläggande för det Automation-konto som heter AutomationAccount01.</span><span class="sxs-lookup"><span data-stu-id="4f4e8-113">This command changes the plan to Basic for the Automation account named AutomationAccount01.</span></span>

## <span data-ttu-id="4f4e8-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="4f4e8-114">PARAMETERS</span></span>

### <span data-ttu-id="4f4e8-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4f4e8-115">-DefaultProfile</span></span>
<span data-ttu-id="4f4e8-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="4f4e8-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="4f4e8-117">-Namn</span><span class="sxs-lookup"><span data-stu-id="4f4e8-117">-Name</span></span>
<span data-ttu-id="4f4e8-118">Anger namnet på det Automation-konto som denna cmdlet ändrar.</span><span class="sxs-lookup"><span data-stu-id="4f4e8-118">Specifies the name of the Automation account that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="4f4e8-119">-Planera</span><span class="sxs-lookup"><span data-stu-id="4f4e8-119">-Plan</span></span>
<span data-ttu-id="4f4e8-120">Anger abonnemanget för Automation-kontot.</span><span class="sxs-lookup"><span data-stu-id="4f4e8-120">Specifies the plan for the Automation account.</span></span>
<span data-ttu-id="4f4e8-121">Giltiga värden är:</span><span class="sxs-lookup"><span data-stu-id="4f4e8-121">Valid values are:</span></span>

- <span data-ttu-id="4f4e8-122">Basisk</span><span class="sxs-lookup"><span data-stu-id="4f4e8-122">Basic</span></span>
- <span data-ttu-id="4f4e8-123">Gratisutdelning</span><span class="sxs-lookup"><span data-stu-id="4f4e8-123">Free</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Free, Basic

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4f4e8-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4f4e8-124">-ResourceGroupName</span></span>
<span data-ttu-id="4f4e8-125">Anger namnet på en resurs grupp som innehåller Automation-kontot som ändras av denna cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4f4e8-125">Specifies the name of a resource group that contains the Automation account that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="4f4e8-126">-Taggar</span><span class="sxs-lookup"><span data-stu-id="4f4e8-126">-Tags</span></span>
<span data-ttu-id="4f4e8-127">Par med nyckelord i form av en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="4f4e8-127">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="4f4e8-128">Till exempel:</span><span class="sxs-lookup"><span data-stu-id="4f4e8-128">For example:</span></span>

<span data-ttu-id="4f4e8-129">@ {key0 = "value0"; KEY1 = $null; key2 = "värde2"}</span><span class="sxs-lookup"><span data-stu-id="4f4e8-129">@{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: IDictionary
Parameter Sets: (All)
Aliases: Tag

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4f4e8-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4f4e8-130">CommonParameters</span></span>
<span data-ttu-id="4f4e8-131">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4f4e8-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4f4e8-132">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4f4e8-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4f4e8-133">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="4f4e8-133">INPUTS</span></span>

### <span data-ttu-id="4f4e8-134">Ingen</span><span class="sxs-lookup"><span data-stu-id="4f4e8-134">None</span></span>
<span data-ttu-id="4f4e8-135">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="4f4e8-135">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="4f4e8-136">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="4f4e8-136">OUTPUTS</span></span>

### <span data-ttu-id="4f4e8-137">Microsoft. Azure. commands. Automation. Model. AutomationAccount</span><span class="sxs-lookup"><span data-stu-id="4f4e8-137">Microsoft.Azure.Commands.Automation.Model.AutomationAccount</span></span>

## <span data-ttu-id="4f4e8-138">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="4f4e8-138">NOTES</span></span>

## <span data-ttu-id="4f4e8-139">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="4f4e8-139">RELATED LINKS</span></span>

[<span data-ttu-id="4f4e8-140">Get-AzureRmAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="4f4e8-140">Get-AzureRmAutomationAccount</span></span>](./Get-AzureRmAutomationAccount.md)

[<span data-ttu-id="4f4e8-141">New-AzureRmAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="4f4e8-141">New-AzureRmAutomationAccount</span></span>](./New-AzureRmAutomationAccount.md)

[<span data-ttu-id="4f4e8-142">Remove-AzureRmAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="4f4e8-142">Remove-AzureRmAutomationAccount</span></span>](./Remove-AzureRmAutomationAccount.md)
