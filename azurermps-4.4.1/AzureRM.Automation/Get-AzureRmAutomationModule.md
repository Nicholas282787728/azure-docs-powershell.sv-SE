---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: A73B388A-E859-40D3-BA63-0E231CF1E81D
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRmAutomationModule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRmAutomationModule.md
ms.openlocfilehash: dcd84c47ff9a6dae06daaf05bde6dd6f4af86553
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93578559"
---
# <span data-ttu-id="bc3b7-101">Get-AzureRmAutomationModule</span><span class="sxs-lookup"><span data-stu-id="bc3b7-101">Get-AzureRmAutomationModule</span></span>

## <span data-ttu-id="bc3b7-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="bc3b7-102">SYNOPSIS</span></span>
<span data-ttu-id="bc3b7-103">Hämtar metadata för moduler från Automation.</span><span class="sxs-lookup"><span data-stu-id="bc3b7-103">Gets metadata for modules from Automation.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bc3b7-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="bc3b7-104">SYNTAX</span></span>

### <span data-ttu-id="bc3b7-105">ByAll (standard)</span><span class="sxs-lookup"><span data-stu-id="bc3b7-105">ByAll (Default)</span></span>
```
Get-AzureRmAutomationModule [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="bc3b7-106">ByName</span><span class="sxs-lookup"><span data-stu-id="bc3b7-106">ByName</span></span>
```
Get-AzureRmAutomationModule [-Name] <String> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bc3b7-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="bc3b7-107">DESCRIPTION</span></span>
<span data-ttu-id="bc3b7-108">Cmdleten **Get-AzureRmAutomationModule** hämtar metadata för moduler från Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="bc3b7-108">The **Get-AzureRmAutomationModule** cmdlet gets metadata for modules from Azure Automation.</span></span>

## <span data-ttu-id="bc3b7-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="bc3b7-109">EXAMPLES</span></span>

### <span data-ttu-id="bc3b7-110">Exempel 1: Hämta alla moduler</span><span class="sxs-lookup"><span data-stu-id="bc3b7-110">Example 1: Get all modules</span></span>
```
PS C:\>Get-AzureRmAutomationModule -AutomationAccountName "Contoso17" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="bc3b7-111">Det här kommandot får alla moduler i Automation-kontot som heter Contoso17.</span><span class="sxs-lookup"><span data-stu-id="bc3b7-111">This command gets all modules in the Automation account named Contoso17.</span></span>

### <span data-ttu-id="bc3b7-112">Exempel 2: Hämta en modul</span><span class="sxs-lookup"><span data-stu-id="bc3b7-112">Example 2: Get a module</span></span>
```
PS C:\>Get-AzureRmAutomationModule -AutomationAccountName "Contoso17" -Name "ContosoModule" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="bc3b7-113">Det här kommandot hämtar en modul som heter ContosoModule i Automation-kontot med namnet Contoso17.</span><span class="sxs-lookup"><span data-stu-id="bc3b7-113">This command gets a module named ContosoModule in the Automation account named Contoso17.</span></span>

## <span data-ttu-id="bc3b7-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="bc3b7-114">PARAMETERS</span></span>

### <span data-ttu-id="bc3b7-115">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="bc3b7-115">-AutomationAccountName</span></span>
<span data-ttu-id="bc3b7-116">Anger namnet på det Automation-konto som denna cmdlet får modulens metadata för.</span><span class="sxs-lookup"><span data-stu-id="bc3b7-116">Specifies the name of the Automation account for which this cmdlet gets module metadata.</span></span>

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

### <span data-ttu-id="bc3b7-117">-Namn</span><span class="sxs-lookup"><span data-stu-id="bc3b7-117">-Name</span></span>
<span data-ttu-id="bc3b7-118">Anger namnet på den modul där denna cmdlet får metadata.</span><span class="sxs-lookup"><span data-stu-id="bc3b7-118">Specifies the name of the module for which this cmdlet gets metadata.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bc3b7-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bc3b7-119">-ResourceGroupName</span></span>
<span data-ttu-id="bc3b7-120">Anger namnet på en resurs grupp för vilken denna cmdlet får modulens metadata.</span><span class="sxs-lookup"><span data-stu-id="bc3b7-120">Specifies the name of a resource group for which this cmdlet gets module metadata.</span></span>

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

### <span data-ttu-id="bc3b7-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bc3b7-121">-DefaultProfile</span></span>
<span data-ttu-id="bc3b7-122">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="bc3b7-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bc3b7-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bc3b7-123">CommonParameters</span></span>
<span data-ttu-id="bc3b7-124">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bc3b7-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bc3b7-125">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bc3b7-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bc3b7-126">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="bc3b7-126">INPUTS</span></span>

## <span data-ttu-id="bc3b7-127">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="bc3b7-127">OUTPUTS</span></span>

### <span data-ttu-id="bc3b7-128">Microsoft. Azure. commands. Automation. Model. modul</span><span class="sxs-lookup"><span data-stu-id="bc3b7-128">Microsoft.Azure.Commands.Automation.Model.Module</span></span>

## <span data-ttu-id="bc3b7-129">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="bc3b7-129">NOTES</span></span>

## <span data-ttu-id="bc3b7-130">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="bc3b7-130">RELATED LINKS</span></span>

[<span data-ttu-id="bc3b7-131">New-AzureRmAutomationModule</span><span class="sxs-lookup"><span data-stu-id="bc3b7-131">New-AzureRmAutomationModule</span></span>](./New-AzureRmAutomationModule.md)

[<span data-ttu-id="bc3b7-132">Remove-AzureRmAutomationModule</span><span class="sxs-lookup"><span data-stu-id="bc3b7-132">Remove-AzureRmAutomationModule</span></span>](./Remove-AzureRmAutomationModule.md)

[<span data-ttu-id="bc3b7-133">Set-AzureRmAutomationModule</span><span class="sxs-lookup"><span data-stu-id="bc3b7-133">Set-AzureRmAutomationModule</span></span>](./Set-AzureRmAutomationModule.md)


