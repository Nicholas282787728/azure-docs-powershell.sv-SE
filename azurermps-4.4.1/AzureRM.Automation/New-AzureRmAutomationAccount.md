---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: 2D5B16F0-0662-4D9F-A13F-808CE5EEBBA3
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/New-AzureRmAutomationAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/New-AzureRmAutomationAccount.md
ms.openlocfilehash: d40e79e53ccf2ddd9cb5c251328268da0bed76fd
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93756114"
---
# <span data-ttu-id="e1846-101">New-AzureRmAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="e1846-101">New-AzureRmAutomationAccount</span></span>

## <span data-ttu-id="e1846-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="e1846-102">SYNOPSIS</span></span>
<span data-ttu-id="e1846-103">Skapar ett Automation-konto.</span><span class="sxs-lookup"><span data-stu-id="e1846-103">Creates an Automation account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e1846-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="e1846-104">SYNTAX</span></span>

```
New-AzureRmAutomationAccount [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [-Plan <String>] [-Tags <IDictionary>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e1846-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="e1846-105">DESCRIPTION</span></span>
<span data-ttu-id="e1846-106">Cmdleten **New-AzureRmAutomationAccount** skapar ett Azure Automation-konto i en resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="e1846-106">The **New-AzureRmAutomationAccount** cmdlet creates an Azure Automation account in a resource group.</span></span>

<span data-ttu-id="e1846-107">Ett Automation-konto är en behållare för Automation-resurser som är isolerade från andra Automation-konton.</span><span class="sxs-lookup"><span data-stu-id="e1846-107">An Automation account is a container for Automation resources that is isolated from the resources of other Automation accounts.</span></span> <span data-ttu-id="e1846-108">Automatiserings resurser inkluderar Runbooks, önskad tillstånds konfiguration (DSC)-konfigurationer,-jobb och till gångar.</span><span class="sxs-lookup"><span data-stu-id="e1846-108">Automation resources include runbooks, Desired State Configuration (DSC) configurations, jobs, and assets.</span></span>

## <span data-ttu-id="e1846-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="e1846-109">EXAMPLES</span></span>

### <span data-ttu-id="e1846-110">Exempel 1: skapa ett Automation-konto</span><span class="sxs-lookup"><span data-stu-id="e1846-110">Example 1: Create an automation account</span></span>
```
PS C:\> New-AzureRmAutomationAccount -Name "ContosoAutomationAccount" -Location "East US" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="e1846-111">Det här kommandot skapar ett nytt Automation-konto med namnet ContosoAutomationAccount i USA-regionen.</span><span class="sxs-lookup"><span data-stu-id="e1846-111">This command creates a new automation account named ContosoAutomationAccount in the East US region.</span></span>

## <span data-ttu-id="e1846-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="e1846-112">PARAMETERS</span></span>

### <span data-ttu-id="e1846-113">-Plats</span><span class="sxs-lookup"><span data-stu-id="e1846-113">-Location</span></span>
<span data-ttu-id="e1846-114">Anger den plats där denna cmdlet skapar Automation-kontot.</span><span class="sxs-lookup"><span data-stu-id="e1846-114">Specifies the location in which this cmdlet creates the Automation account.</span></span>
<span data-ttu-id="e1846-115">Använd Get-AzureRMLocation cmdlet för att få giltiga platser.</span><span class="sxs-lookup"><span data-stu-id="e1846-115">To obtain valid locations, use the Get-AzureRMLocation cmdlet.</span></span>

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

### <span data-ttu-id="e1846-116">-Namn</span><span class="sxs-lookup"><span data-stu-id="e1846-116">-Name</span></span>
<span data-ttu-id="e1846-117">Anger ett namn för Automation-kontot.</span><span class="sxs-lookup"><span data-stu-id="e1846-117">Specifies a name for the Automation account.</span></span>

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

### <span data-ttu-id="e1846-118">-Planera</span><span class="sxs-lookup"><span data-stu-id="e1846-118">-Plan</span></span>
<span data-ttu-id="e1846-119">Anger abonnemanget för Automation-kontot.</span><span class="sxs-lookup"><span data-stu-id="e1846-119">Specifies the plan for the Automation account.</span></span>
<span data-ttu-id="e1846-120">Giltiga värden är:</span><span class="sxs-lookup"><span data-stu-id="e1846-120">Valid values are:</span></span>

- <span data-ttu-id="e1846-121">Basisk</span><span class="sxs-lookup"><span data-stu-id="e1846-121">Basic</span></span>
- <span data-ttu-id="e1846-122">Gratisutdelning</span><span class="sxs-lookup"><span data-stu-id="e1846-122">Free</span></span>

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

### <span data-ttu-id="e1846-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e1846-123">-ResourceGroupName</span></span>
<span data-ttu-id="e1846-124">Anger namnet på en resurs grupp där denna cmdlet lägger till ett Automation-konto.</span><span class="sxs-lookup"><span data-stu-id="e1846-124">Specifies the name of a resource group to which this cmdlet adds an Automation account.</span></span>

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

### <span data-ttu-id="e1846-125">-Taggar</span><span class="sxs-lookup"><span data-stu-id="e1846-125">-Tags</span></span>
<span data-ttu-id="e1846-126">Par med nyckelord i form av en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="e1846-126">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="e1846-127">Till exempel:</span><span class="sxs-lookup"><span data-stu-id="e1846-127">For example:</span></span>

<span data-ttu-id="e1846-128">@ {key0 = "value0"; KEY1 = $null; key2 = "värde2"}</span><span class="sxs-lookup"><span data-stu-id="e1846-128">@{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="e1846-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e1846-129">-DefaultProfile</span></span>
<span data-ttu-id="e1846-130">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="e1846-130">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e1846-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e1846-131">CommonParameters</span></span>
<span data-ttu-id="e1846-132">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e1846-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e1846-133">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e1846-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e1846-134">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="e1846-134">INPUTS</span></span>

## <span data-ttu-id="e1846-135">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="e1846-135">OUTPUTS</span></span>

### <span data-ttu-id="e1846-136">Microsoft. Azure. commands. Automation. Model. AutomationAccount</span><span class="sxs-lookup"><span data-stu-id="e1846-136">Microsoft.Azure.Commands.Automation.Model.AutomationAccount</span></span>

## <span data-ttu-id="e1846-137">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="e1846-137">NOTES</span></span>

## <span data-ttu-id="e1846-138">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="e1846-138">RELATED LINKS</span></span>

[<span data-ttu-id="e1846-139">Get-AzureRmAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="e1846-139">Get-AzureRmAutomationAccount</span></span>](./Get-AzureRmAutomationAccount.md)

[<span data-ttu-id="e1846-140">Remove-AzureRmAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="e1846-140">Remove-AzureRmAutomationAccount</span></span>](./Remove-AzureRmAutomationAccount.md)

[<span data-ttu-id="e1846-141">Set-AzureRmAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="e1846-141">Set-AzureRmAutomationAccount</span></span>](./Set-AzureRmAutomationAccount.md)
