---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: F344D8D1-5593-4C09-A1CA-37579D2A3A61
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/set-azurermautomationvariable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Set-AzureRMAutomationVariable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Set-AzureRMAutomationVariable.md
ms.openlocfilehash: 7426f49d94e82865163320fecd85704aeeff14b8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93579664"
---
# <span data-ttu-id="3d90c-101">Set-AzureRmAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="3d90c-101">Set-AzureRmAutomationVariable</span></span>

## <span data-ttu-id="3d90c-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="3d90c-102">SYNOPSIS</span></span>
<span data-ttu-id="3d90c-103">Ändrar en automatiserings variabel.</span><span class="sxs-lookup"><span data-stu-id="3d90c-103">Modifies an Automation variable.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3d90c-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="3d90c-104">SYNTAX</span></span>

### <span data-ttu-id="3d90c-105">UpdateVariableValue</span><span class="sxs-lookup"><span data-stu-id="3d90c-105">UpdateVariableValue</span></span>
```
Set-AzureRmAutomationVariable [-Name] <String> -Encrypted <Boolean> -Value <Object>
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="3d90c-106">UpdateVariableDescription</span><span class="sxs-lookup"><span data-stu-id="3d90c-106">UpdateVariableDescription</span></span>
```
Set-AzureRmAutomationVariable [-Name] <String> -Description <String> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3d90c-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="3d90c-107">DESCRIPTION</span></span>
<span data-ttu-id="3d90c-108">Cmdleten **set-AzureRmAutomationVariable** ändrar värdet eller beskrivningen av en variabel i Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="3d90c-108">The **Set-AzureRmAutomationVariable** cmdlet modifies the value or description of a variable in Azure Automation.</span></span>
<span data-ttu-id="3d90c-109">Om du vill kryptera variabeln anger du den *krypterade* parametern.</span><span class="sxs-lookup"><span data-stu-id="3d90c-109">To encrypt the variable, specify the *Encrypted* parameter.</span></span>
<span data-ttu-id="3d90c-110">Du kan inte ändra det krypterade tillståndet för en variabel när du har skapat den.</span><span class="sxs-lookup"><span data-stu-id="3d90c-110">You cannot modify the encrypted state of a variable after creation.</span></span>
<span data-ttu-id="3d90c-111">Det går inte att ange *krypterade* för en befintlig, icke-krypterad variabel.</span><span class="sxs-lookup"><span data-stu-id="3d90c-111">Specifying *Encrypted* for an existing, non-encrypted, variable fails.</span></span>

## <span data-ttu-id="3d90c-112">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="3d90c-112">EXAMPLES</span></span>

### <span data-ttu-id="3d90c-113">Exempel 1: Ange värdet för en variabel</span><span class="sxs-lookup"><span data-stu-id="3d90c-113">Example 1: Set the value of a variable</span></span>
```
PS C:\>Set-AzureRmAutomationVariable -AutomationAccountName "Contoso17" -Name "StringVariable22" -ResourceGroupName "ResourceGroup01" -Value "New Value" -Encrypted $False
```

<span data-ttu-id="3d90c-114">Det här kommandot anger ett nytt värde för variabeln som heter StringVariable22 i Azure Automation-kontot med namnet Contoso17.</span><span class="sxs-lookup"><span data-stu-id="3d90c-114">This command sets a new value for the variable named StringVariable22 in the Azure Automation account named Contoso17.</span></span>

## <span data-ttu-id="3d90c-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="3d90c-115">PARAMETERS</span></span>

### <span data-ttu-id="3d90c-116">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="3d90c-116">-AutomationAccountName</span></span>
<span data-ttu-id="3d90c-117">Anger namnet på det Automation-konto där variabeln lagras.</span><span class="sxs-lookup"><span data-stu-id="3d90c-117">Specifies the name of the Automation account in which the variable is stored.</span></span>

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

### <span data-ttu-id="3d90c-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3d90c-118">-DefaultProfile</span></span>
<span data-ttu-id="3d90c-119">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="3d90c-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="3d90c-120">-Beskrivning</span><span class="sxs-lookup"><span data-stu-id="3d90c-120">-Description</span></span>
<span data-ttu-id="3d90c-121">Anger en beskrivning av variabeln.</span><span class="sxs-lookup"><span data-stu-id="3d90c-121">Specifies a description for the variable.</span></span>

```yaml
Type: String
Parameter Sets: UpdateVariableDescription
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3d90c-122">-Krypterade</span><span class="sxs-lookup"><span data-stu-id="3d90c-122">-Encrypted</span></span>
<span data-ttu-id="3d90c-123">Anger om cmdlet krypterar variabelns värde för lagring.</span><span class="sxs-lookup"><span data-stu-id="3d90c-123">Specifies whether cmdlet encrypts the value of the variable for storage.</span></span>

```yaml
Type: Boolean
Parameter Sets: UpdateVariableValue
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3d90c-124">-Namn</span><span class="sxs-lookup"><span data-stu-id="3d90c-124">-Name</span></span>
<span data-ttu-id="3d90c-125">Anger namnet på den variabel som denna cmdlet ändrar.</span><span class="sxs-lookup"><span data-stu-id="3d90c-125">Specifies the name of the variable that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="3d90c-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3d90c-126">-ResourceGroupName</span></span>
<span data-ttu-id="3d90c-127">Anger den resurs grupp för vilken denna cmdlet ändrar en variabel.</span><span class="sxs-lookup"><span data-stu-id="3d90c-127">Specifies the resource group for which this cmdlet modifies a variable.</span></span>

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

### <span data-ttu-id="3d90c-128">-Värde</span><span class="sxs-lookup"><span data-stu-id="3d90c-128">-Value</span></span>
<span data-ttu-id="3d90c-129">Anger ett värde för variabeln.</span><span class="sxs-lookup"><span data-stu-id="3d90c-129">Specifies a value for the variable.</span></span>

```yaml
Type: Object
Parameter Sets: UpdateVariableValue
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3d90c-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3d90c-130">CommonParameters</span></span>
<span data-ttu-id="3d90c-131">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3d90c-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3d90c-132">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3d90c-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3d90c-133">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="3d90c-133">INPUTS</span></span>

### <span data-ttu-id="3d90c-134">Ingen</span><span class="sxs-lookup"><span data-stu-id="3d90c-134">None</span></span>
<span data-ttu-id="3d90c-135">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="3d90c-135">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="3d90c-136">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="3d90c-136">OUTPUTS</span></span>

### <span data-ttu-id="3d90c-137">Microsoft. Azure. commands. Automation. Model. Variable</span><span class="sxs-lookup"><span data-stu-id="3d90c-137">Microsoft.Azure.Commands.Automation.Model.Variable</span></span>

## <span data-ttu-id="3d90c-138">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="3d90c-138">NOTES</span></span>

## <span data-ttu-id="3d90c-139">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="3d90c-139">RELATED LINKS</span></span>

[<span data-ttu-id="3d90c-140">Get-AzureRmAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="3d90c-140">Get-AzureRmAutomationVariable</span></span>](./Get-AzureRMAutomationVariable.md)

[<span data-ttu-id="3d90c-141">New-AzureRmAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="3d90c-141">New-AzureRmAutomationVariable</span></span>](./New-AzureRMAutomationVariable.md)

[<span data-ttu-id="3d90c-142">Remove-AzureRmAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="3d90c-142">Remove-AzureRmAutomationVariable</span></span>](./Remove-AzureRMAutomationVariable.md)


