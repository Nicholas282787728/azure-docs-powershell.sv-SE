---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: 2D5B16F0-0662-4D9F-A13F-808CE5EEBBA3
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/new-azurermautomationaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/New-AzureRmAutomationAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/New-AzureRmAutomationAccount.md
ms.openlocfilehash: c82a68e7859945b1fdb91f6d44a1ebbcef6d2cff
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93574446"
---
# <span data-ttu-id="e4ef3-101">New-AzureRmAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="e4ef3-101">New-AzureRmAutomationAccount</span></span>

## <span data-ttu-id="e4ef3-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="e4ef3-102">SYNOPSIS</span></span>
<span data-ttu-id="e4ef3-103">Skapar ett Automation-konto.</span><span class="sxs-lookup"><span data-stu-id="e4ef3-103">Creates an Automation account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e4ef3-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="e4ef3-104">SYNTAX</span></span>

```
New-AzureRmAutomationAccount [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [-Plan <String>] [-Tags <IDictionary>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e4ef3-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="e4ef3-105">DESCRIPTION</span></span>
<span data-ttu-id="e4ef3-106">Cmdleten **New-AzureRmAutomationAccount** skapar ett Azure Automation-konto i en resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="e4ef3-106">The **New-AzureRmAutomationAccount** cmdlet creates an Azure Automation account in a resource group.</span></span>

<span data-ttu-id="e4ef3-107">Ett Automation-konto är en behållare för Automation-resurser som är isolerade från andra Automation-konton.</span><span class="sxs-lookup"><span data-stu-id="e4ef3-107">An Automation account is a container for Automation resources that is isolated from the resources of other Automation accounts.</span></span> <span data-ttu-id="e4ef3-108">Automatiserings resurser inkluderar Runbooks, önskad tillstånds konfiguration (DSC)-konfigurationer,-jobb och till gångar.</span><span class="sxs-lookup"><span data-stu-id="e4ef3-108">Automation resources include runbooks, Desired State Configuration (DSC) configurations, jobs, and assets.</span></span>

## <span data-ttu-id="e4ef3-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="e4ef3-109">EXAMPLES</span></span>

### <span data-ttu-id="e4ef3-110">Exempel 1: skapa ett Automation-konto</span><span class="sxs-lookup"><span data-stu-id="e4ef3-110">Example 1: Create an automation account</span></span>
```
PS C:\> New-AzureRmAutomationAccount -Name "ContosoAutomationAccount" -Location "East US" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="e4ef3-111">Det här kommandot skapar ett nytt Automation-konto med namnet ContosoAutomationAccount i USA-regionen.</span><span class="sxs-lookup"><span data-stu-id="e4ef3-111">This command creates a new automation account named ContosoAutomationAccount in the East US region.</span></span>

## <span data-ttu-id="e4ef3-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="e4ef3-112">PARAMETERS</span></span>

### <span data-ttu-id="e4ef3-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e4ef3-113">-DefaultProfile</span></span>
<span data-ttu-id="e4ef3-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="e4ef3-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e4ef3-115">-Plats</span><span class="sxs-lookup"><span data-stu-id="e4ef3-115">-Location</span></span>
<span data-ttu-id="e4ef3-116">Anger den plats där denna cmdlet skapar Automation-kontot.</span><span class="sxs-lookup"><span data-stu-id="e4ef3-116">Specifies the location in which this cmdlet creates the Automation account.</span></span>
<span data-ttu-id="e4ef3-117">Använd Get-AzureRMLocation cmdlet för att få giltiga platser.</span><span class="sxs-lookup"><span data-stu-id="e4ef3-117">To obtain valid locations, use the Get-AzureRMLocation cmdlet.</span></span>

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

### <span data-ttu-id="e4ef3-118">-Namn</span><span class="sxs-lookup"><span data-stu-id="e4ef3-118">-Name</span></span>
<span data-ttu-id="e4ef3-119">Anger ett namn för Automation-kontot.</span><span class="sxs-lookup"><span data-stu-id="e4ef3-119">Specifies a name for the Automation account.</span></span>

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

### <span data-ttu-id="e4ef3-120">-Planera</span><span class="sxs-lookup"><span data-stu-id="e4ef3-120">-Plan</span></span>
<span data-ttu-id="e4ef3-121">Anger abonnemanget för Automation-kontot.</span><span class="sxs-lookup"><span data-stu-id="e4ef3-121">Specifies the plan for the Automation account.</span></span>
<span data-ttu-id="e4ef3-122">Giltiga värden är:</span><span class="sxs-lookup"><span data-stu-id="e4ef3-122">Valid values are:</span></span>

- <span data-ttu-id="e4ef3-123">Basisk</span><span class="sxs-lookup"><span data-stu-id="e4ef3-123">Basic</span></span>
- <span data-ttu-id="e4ef3-124">Gratisutdelning</span><span class="sxs-lookup"><span data-stu-id="e4ef3-124">Free</span></span>

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

### <span data-ttu-id="e4ef3-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e4ef3-125">-ResourceGroupName</span></span>
<span data-ttu-id="e4ef3-126">Anger namnet på en resurs grupp där denna cmdlet lägger till ett Automation-konto.</span><span class="sxs-lookup"><span data-stu-id="e4ef3-126">Specifies the name of a resource group to which this cmdlet adds an Automation account.</span></span>

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

### <span data-ttu-id="e4ef3-127">-Taggar</span><span class="sxs-lookup"><span data-stu-id="e4ef3-127">-Tags</span></span>
<span data-ttu-id="e4ef3-128">Par med nyckelord i form av en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="e4ef3-128">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="e4ef3-129">Till exempel:</span><span class="sxs-lookup"><span data-stu-id="e4ef3-129">For example:</span></span>

<span data-ttu-id="e4ef3-130">@ {key0 = "value0"; KEY1 = $null; key2 = "värde2"}</span><span class="sxs-lookup"><span data-stu-id="e4ef3-130">@{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="e4ef3-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e4ef3-131">CommonParameters</span></span>
<span data-ttu-id="e4ef3-132">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e4ef3-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e4ef3-133">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e4ef3-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e4ef3-134">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="e4ef3-134">INPUTS</span></span>

### <span data-ttu-id="e4ef3-135">Ingen</span><span class="sxs-lookup"><span data-stu-id="e4ef3-135">None</span></span>
<span data-ttu-id="e4ef3-136">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="e4ef3-136">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="e4ef3-137">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="e4ef3-137">OUTPUTS</span></span>

### <span data-ttu-id="e4ef3-138">Microsoft. Azure. commands. Automation. Model. AutomationAccount</span><span class="sxs-lookup"><span data-stu-id="e4ef3-138">Microsoft.Azure.Commands.Automation.Model.AutomationAccount</span></span>

## <span data-ttu-id="e4ef3-139">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="e4ef3-139">NOTES</span></span>

## <span data-ttu-id="e4ef3-140">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="e4ef3-140">RELATED LINKS</span></span>

[<span data-ttu-id="e4ef3-141">Get-AzureRmAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="e4ef3-141">Get-AzureRmAutomationAccount</span></span>](./Get-AzureRmAutomationAccount.md)

[<span data-ttu-id="e4ef3-142">Remove-AzureRmAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="e4ef3-142">Remove-AzureRmAutomationAccount</span></span>](./Remove-AzureRmAutomationAccount.md)

[<span data-ttu-id="e4ef3-143">Set-AzureRmAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="e4ef3-143">Set-AzureRmAutomationAccount</span></span>](./Set-AzureRmAutomationAccount.md)
