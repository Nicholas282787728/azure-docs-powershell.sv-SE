---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: BBD37C4B-BB6F-4560-BDEE-F0440EC1938A
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/get-azurermautomationdscconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRmAutomationDscConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRmAutomationDscConfiguration.md
ms.openlocfilehash: 3d6d3628ba15fa4b775f4c747a29645ec0628402
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93586412"
---
# <span data-ttu-id="228e3-101">Get-AzureRmAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="228e3-101">Get-AzureRmAutomationDscConfiguration</span></span>

## <span data-ttu-id="228e3-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="228e3-102">SYNOPSIS</span></span>
<span data-ttu-id="228e3-103">Hämtar DSC-konfigurationer från Automation.</span><span class="sxs-lookup"><span data-stu-id="228e3-103">Gets DSC configurations from Automation.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="228e3-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="228e3-104">SYNTAX</span></span>

### <span data-ttu-id="228e3-105">ByAll (standard)</span><span class="sxs-lookup"><span data-stu-id="228e3-105">ByAll (Default)</span></span>
```
Get-AzureRmAutomationDscConfiguration [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="228e3-106">ByConfigurationName</span><span class="sxs-lookup"><span data-stu-id="228e3-106">ByConfigurationName</span></span>
```
Get-AzureRmAutomationDscConfiguration [-Name] <String> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="228e3-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="228e3-107">DESCRIPTION</span></span>
<span data-ttu-id="228e3-108">Cmdleten **Get-AzureRmAutomationDscConfiguration** får APS-konfiguration (DSC-konfigurationer) från Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="228e3-108">The **Get-AzureRmAutomationDscConfiguration** cmdlet gets APS Desired State Configuration (DSC) configurations from Azure Automation.</span></span>

## <span data-ttu-id="228e3-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="228e3-109">EXAMPLES</span></span>

### <span data-ttu-id="228e3-110">Exempel 1: Hämta alla DSC-konfigurationer</span><span class="sxs-lookup"><span data-stu-id="228e3-110">Example 1: Get all DSC configurations</span></span>
```
PS C:\>Get-AzureRmAutomationDscConfiguration -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17"
```

<span data-ttu-id="228e3-111">Det här kommandot får metadata för alla DSC-konfigurationer i Automation-kontot med namnet Contoso17.</span><span class="sxs-lookup"><span data-stu-id="228e3-111">This command gets metadata for all DSC configurations in the Automation account named Contoso17.</span></span>

### <span data-ttu-id="228e3-112">Exempel 2: skaffa en DSC-konfiguration utifrån namn</span><span class="sxs-lookup"><span data-stu-id="228e3-112">Example 2: Get a DSC configuration by name</span></span>
```
PS C:\>Get-AzureRmAutomationDscConfiguration -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17" -Name "ContosoConfiguration"
```

<span data-ttu-id="228e3-113">Det här kommandot får metadata för en DSC-konfiguration med namnet min konfiguration som heter Contoso17.</span><span class="sxs-lookup"><span data-stu-id="228e3-113">This command gets metadata for a DSC configuration named MyConfiguration in the Automation account named Contoso17.</span></span>

## <span data-ttu-id="228e3-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="228e3-114">PARAMETERS</span></span>

### <span data-ttu-id="228e3-115">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="228e3-115">-AutomationAccountName</span></span>
<span data-ttu-id="228e3-116">Anger namnet på det Automation-konto som innehåller DSC-konfigurationer som den här cmdleten får.</span><span class="sxs-lookup"><span data-stu-id="228e3-116">Specifies the name of the Automation account that contains DSC configurations that this cmdlet gets.</span></span>

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

### <span data-ttu-id="228e3-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="228e3-117">-DefaultProfile</span></span>
<span data-ttu-id="228e3-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="228e3-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="228e3-119">-Namn</span><span class="sxs-lookup"><span data-stu-id="228e3-119">-Name</span></span>
<span data-ttu-id="228e3-120">Anger namnet på den DSC-konfiguration som den här cmdleten får.</span><span class="sxs-lookup"><span data-stu-id="228e3-120">Specifies the name of the DSC configuration that this cmdlet gets.</span></span>

```yaml
Type: String
Parameter Sets: ByConfigurationName
Aliases: ConfigurationName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="228e3-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="228e3-121">-ResourceGroupName</span></span>
<span data-ttu-id="228e3-122">Anger namnet på en resurs grupp för vilken denna cmdlet får DSC-konfigurationer.</span><span class="sxs-lookup"><span data-stu-id="228e3-122">Specifies the name of a resource group for which this cmdlet gets DSC configurations.</span></span>

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

### <span data-ttu-id="228e3-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="228e3-123">CommonParameters</span></span>
<span data-ttu-id="228e3-124">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="228e3-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="228e3-125">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="228e3-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="228e3-126">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="228e3-126">INPUTS</span></span>

### <span data-ttu-id="228e3-127">Ingen</span><span class="sxs-lookup"><span data-stu-id="228e3-127">None</span></span>
<span data-ttu-id="228e3-128">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="228e3-128">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="228e3-129">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="228e3-129">OUTPUTS</span></span>

### <span data-ttu-id="228e3-130">Microsoft. Azure. commands. Automation. Model. DscConfiguration</span><span class="sxs-lookup"><span data-stu-id="228e3-130">Microsoft.Azure.Commands.Automation.Model.DscConfiguration</span></span>

## <span data-ttu-id="228e3-131">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="228e3-131">NOTES</span></span>

## <span data-ttu-id="228e3-132">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="228e3-132">RELATED LINKS</span></span>

[<span data-ttu-id="228e3-133">Exportera-AzureRmAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="228e3-133">Export-AzureRmAutomationDscConfiguration</span></span>](./Export-AzureRmAutomationDscConfiguration.md)

[<span data-ttu-id="228e3-134">Import-AzureRmAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="228e3-134">Import-AzureRmAutomationDscConfiguration</span></span>](./Import-AzureRmAutomationDscConfiguration.md)


