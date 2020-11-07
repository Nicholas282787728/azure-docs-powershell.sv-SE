---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: BBD37C4B-BB6F-4560-BDEE-F0440EC1938A
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/get-azautomationdscconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationDscConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationDscConfiguration.md
ms.openlocfilehash: b400efe3224a4fa4b014b9ac93786cd130d4ce6e
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93745586"
---
# <span data-ttu-id="f3113-101">Get-AzAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="f3113-101">Get-AzAutomationDscConfiguration</span></span>

## <span data-ttu-id="f3113-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="f3113-102">SYNOPSIS</span></span>
<span data-ttu-id="f3113-103">Hämtar DSC-konfigurationer från Automation.</span><span class="sxs-lookup"><span data-stu-id="f3113-103">Gets DSC configurations from Automation.</span></span>

## <span data-ttu-id="f3113-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="f3113-104">SYNTAX</span></span>

### <span data-ttu-id="f3113-105">ByAll (standard)</span><span class="sxs-lookup"><span data-stu-id="f3113-105">ByAll (Default)</span></span>
```
Get-AzAutomationDscConfiguration [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f3113-106">ByConfigurationName</span><span class="sxs-lookup"><span data-stu-id="f3113-106">ByConfigurationName</span></span>
```
Get-AzAutomationDscConfiguration [-Name] <String> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f3113-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="f3113-107">DESCRIPTION</span></span>
<span data-ttu-id="f3113-108">Cmdleten **Get-AzAutomationDscConfiguration** får APS-konfiguration (DSC-konfigurationer) från Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="f3113-108">The **Get-AzAutomationDscConfiguration** cmdlet gets APS Desired State Configuration (DSC) configurations from Azure Automation.</span></span>

## <span data-ttu-id="f3113-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="f3113-109">EXAMPLES</span></span>

### <span data-ttu-id="f3113-110">Exempel 1: Hämta alla DSC-konfigurationer</span><span class="sxs-lookup"><span data-stu-id="f3113-110">Example 1: Get all DSC configurations</span></span>
```
PS C:\>Get-AzAutomationDscConfiguration -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17"
```

<span data-ttu-id="f3113-111">Det här kommandot får metadata för alla DSC-konfigurationer i Automation-kontot med namnet Contoso17.</span><span class="sxs-lookup"><span data-stu-id="f3113-111">This command gets metadata for all DSC configurations in the Automation account named Contoso17.</span></span>

### <span data-ttu-id="f3113-112">Exempel 2: skaffa en DSC-konfiguration utifrån namn</span><span class="sxs-lookup"><span data-stu-id="f3113-112">Example 2: Get a DSC configuration by name</span></span>
```
PS C:\>Get-AzAutomationDscConfiguration -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17" -Name "ContosoConfiguration"
```

<span data-ttu-id="f3113-113">Det här kommandot får metadata för en DSC-konfiguration med namnet min konfiguration som heter Contoso17.</span><span class="sxs-lookup"><span data-stu-id="f3113-113">This command gets metadata for a DSC configuration named MyConfiguration in the Automation account named Contoso17.</span></span>

## <span data-ttu-id="f3113-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="f3113-114">PARAMETERS</span></span>

### <span data-ttu-id="f3113-115">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="f3113-115">-AutomationAccountName</span></span>
<span data-ttu-id="f3113-116">Anger namnet på det Automation-konto som innehåller DSC-konfigurationer som den här cmdleten får.</span><span class="sxs-lookup"><span data-stu-id="f3113-116">Specifies the name of the Automation account that contains DSC configurations that this cmdlet gets.</span></span>

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

### <span data-ttu-id="f3113-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f3113-117">-DefaultProfile</span></span>
<span data-ttu-id="f3113-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="f3113-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f3113-119">-Namn</span><span class="sxs-lookup"><span data-stu-id="f3113-119">-Name</span></span>
<span data-ttu-id="f3113-120">Anger namnet på den DSC-konfiguration som den här cmdleten får.</span><span class="sxs-lookup"><span data-stu-id="f3113-120">Specifies the name of the DSC configuration that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: ByConfigurationName
Aliases: ConfigurationName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f3113-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f3113-121">-ResourceGroupName</span></span>
<span data-ttu-id="f3113-122">Anger namnet på en resurs grupp för vilken denna cmdlet får DSC-konfigurationer.</span><span class="sxs-lookup"><span data-stu-id="f3113-122">Specifies the name of a resource group for which this cmdlet gets DSC configurations.</span></span>

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

### <span data-ttu-id="f3113-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f3113-123">CommonParameters</span></span>
<span data-ttu-id="f3113-124">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f3113-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f3113-125">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f3113-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f3113-126">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="f3113-126">INPUTS</span></span>

### <span data-ttu-id="f3113-127">System. String</span><span class="sxs-lookup"><span data-stu-id="f3113-127">System.String</span></span>

## <span data-ttu-id="f3113-128">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="f3113-128">OUTPUTS</span></span>

### <span data-ttu-id="f3113-129">Microsoft. Azure. commands. Automation. Model. DscConfiguration</span><span class="sxs-lookup"><span data-stu-id="f3113-129">Microsoft.Azure.Commands.Automation.Model.DscConfiguration</span></span>

## <span data-ttu-id="f3113-130">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="f3113-130">NOTES</span></span>

## <span data-ttu-id="f3113-131">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="f3113-131">RELATED LINKS</span></span>

[<span data-ttu-id="f3113-132">Exportera-AzAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="f3113-132">Export-AzAutomationDscConfiguration</span></span>](./Export-AzAutomationDscConfiguration.md)

[<span data-ttu-id="f3113-133">Import-AzAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="f3113-133">Import-AzAutomationDscConfiguration</span></span>](./Import-AzAutomationDscConfiguration.md)


