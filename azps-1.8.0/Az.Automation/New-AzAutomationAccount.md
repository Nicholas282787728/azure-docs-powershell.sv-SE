---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 2D5B16F0-0662-4D9F-A13F-808CE5EEBBA3
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/new-azautomationaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/New-AzAutomationAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/New-AzAutomationAccount.md
ms.openlocfilehash: 4486301d6a7e39081e297d018f3aa244459d328b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93754805"
---
# <span data-ttu-id="7b03b-101">New-AzAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="7b03b-101">New-AzAutomationAccount</span></span>

## <span data-ttu-id="7b03b-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="7b03b-102">SYNOPSIS</span></span>
<span data-ttu-id="7b03b-103">Skapar ett Automation-konto.</span><span class="sxs-lookup"><span data-stu-id="7b03b-103">Creates an Automation account.</span></span>

## <span data-ttu-id="7b03b-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="7b03b-104">SYNTAX</span></span>

```
New-AzAutomationAccount [-ResourceGroupName] <String> [-Name] <String> [-Location] <String> [-Plan <String>]
 [-Tags <IDictionary>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7b03b-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="7b03b-105">DESCRIPTION</span></span>
<span data-ttu-id="7b03b-106">Cmdleten **New-AzAutomationAccount** skapar ett Azure Automation-konto i en resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="7b03b-106">The **New-AzAutomationAccount** cmdlet creates an Azure Automation account in a resource group.</span></span>
<span data-ttu-id="7b03b-107">Ett Automation-konto är en behållare för Automation-resurser som är isolerade från andra Automation-konton.</span><span class="sxs-lookup"><span data-stu-id="7b03b-107">An Automation account is a container for Automation resources that is isolated from the resources of other Automation accounts.</span></span> <span data-ttu-id="7b03b-108">Automatiserings resurser inkluderar Runbooks, önskad tillstånds konfiguration (DSC)-konfigurationer,-jobb och till gångar.</span><span class="sxs-lookup"><span data-stu-id="7b03b-108">Automation resources include runbooks, Desired State Configuration (DSC) configurations, jobs, and assets.</span></span>

## <span data-ttu-id="7b03b-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="7b03b-109">EXAMPLES</span></span>

### <span data-ttu-id="7b03b-110">Exempel 1: skapa ett Automation-konto</span><span class="sxs-lookup"><span data-stu-id="7b03b-110">Example 1: Create an automation account</span></span>
```
PS C:\> New-AzAutomationAccount -Name "ContosoAutomationAccount" -Location "East US" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="7b03b-111">Det här kommandot skapar ett nytt Automation-konto med namnet ContosoAutomationAccount i USA-regionen.</span><span class="sxs-lookup"><span data-stu-id="7b03b-111">This command creates a new automation account named ContosoAutomationAccount in the East US region.</span></span>

## <span data-ttu-id="7b03b-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="7b03b-112">PARAMETERS</span></span>

### <span data-ttu-id="7b03b-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7b03b-113">-DefaultProfile</span></span>
<span data-ttu-id="7b03b-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="7b03b-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="7b03b-115">-Plats</span><span class="sxs-lookup"><span data-stu-id="7b03b-115">-Location</span></span>
<span data-ttu-id="7b03b-116">Anger den plats där denna cmdlet skapar Automation-kontot.</span><span class="sxs-lookup"><span data-stu-id="7b03b-116">Specifies the location in which this cmdlet creates the Automation account.</span></span>
<span data-ttu-id="7b03b-117">Använd Get-AzLocation cmdlet för att få giltiga platser.</span><span class="sxs-lookup"><span data-stu-id="7b03b-117">To obtain valid locations, use the Get-AzLocation cmdlet.</span></span>

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

### <span data-ttu-id="7b03b-118">-Namn</span><span class="sxs-lookup"><span data-stu-id="7b03b-118">-Name</span></span>
<span data-ttu-id="7b03b-119">Anger ett namn för Automation-kontot.</span><span class="sxs-lookup"><span data-stu-id="7b03b-119">Specifies a name for the Automation account.</span></span>

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

### <span data-ttu-id="7b03b-120">-Planera</span><span class="sxs-lookup"><span data-stu-id="7b03b-120">-Plan</span></span>
<span data-ttu-id="7b03b-121">Anger abonnemanget för Automation-kontot.</span><span class="sxs-lookup"><span data-stu-id="7b03b-121">Specifies the plan for the Automation account.</span></span>
<span data-ttu-id="7b03b-122">Giltiga värden är:</span><span class="sxs-lookup"><span data-stu-id="7b03b-122">Valid values are:</span></span>
- <span data-ttu-id="7b03b-123">Basisk</span><span class="sxs-lookup"><span data-stu-id="7b03b-123">Basic</span></span>
- <span data-ttu-id="7b03b-124">Gratisutdelning</span><span class="sxs-lookup"><span data-stu-id="7b03b-124">Free</span></span>

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

### <span data-ttu-id="7b03b-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7b03b-125">-ResourceGroupName</span></span>
<span data-ttu-id="7b03b-126">Anger namnet på en resurs grupp där denna cmdlet lägger till ett Automation-konto.</span><span class="sxs-lookup"><span data-stu-id="7b03b-126">Specifies the name of a resource group to which this cmdlet adds an Automation account.</span></span>

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

### <span data-ttu-id="7b03b-127">-Taggar</span><span class="sxs-lookup"><span data-stu-id="7b03b-127">-Tags</span></span>
<span data-ttu-id="7b03b-128">Par med nyckelord i form av en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="7b03b-128">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="7b03b-129">Till exempel: @ {key0 = "value0"; KEY1 = $null; key2 = "värde2"}</span><span class="sxs-lookup"><span data-stu-id="7b03b-129">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="7b03b-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7b03b-130">CommonParameters</span></span>
<span data-ttu-id="7b03b-131">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7b03b-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7b03b-132">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7b03b-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7b03b-133">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="7b03b-133">INPUTS</span></span>

### <span data-ttu-id="7b03b-134">System. String</span><span class="sxs-lookup"><span data-stu-id="7b03b-134">System.String</span></span>

### <span data-ttu-id="7b03b-135">System. Collections. IDictionary</span><span class="sxs-lookup"><span data-stu-id="7b03b-135">System.Collections.IDictionary</span></span>

## <span data-ttu-id="7b03b-136">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="7b03b-136">OUTPUTS</span></span>

### <span data-ttu-id="7b03b-137">Microsoft. Azure. commands. Automation. Model. AutomationAccount</span><span class="sxs-lookup"><span data-stu-id="7b03b-137">Microsoft.Azure.Commands.Automation.Model.AutomationAccount</span></span>

## <span data-ttu-id="7b03b-138">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="7b03b-138">NOTES</span></span>

## <span data-ttu-id="7b03b-139">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="7b03b-139">RELATED LINKS</span></span>

[<span data-ttu-id="7b03b-140">Get-AzAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="7b03b-140">Get-AzAutomationAccount</span></span>](./Get-AzAutomationAccount.md)

[<span data-ttu-id="7b03b-141">Remove-AzAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="7b03b-141">Remove-AzAutomationAccount</span></span>](./Remove-AzAutomationAccount.md)

[<span data-ttu-id="7b03b-142">Set-AzAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="7b03b-142">Set-AzAutomationAccount</span></span>](./Set-AzAutomationAccount.md)
