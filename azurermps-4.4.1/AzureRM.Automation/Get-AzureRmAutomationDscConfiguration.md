---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: BBD37C4B-BB6F-4560-BDEE-F0440EC1938A
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRmAutomationDscConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRmAutomationDscConfiguration.md
ms.openlocfilehash: 4ac549e53054d0650c0e64e45c662c6b184067b6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93579848"
---
# <span data-ttu-id="f0141-101">Get-AzureRmAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="f0141-101">Get-AzureRmAutomationDscConfiguration</span></span>

## <span data-ttu-id="f0141-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="f0141-102">SYNOPSIS</span></span>
<span data-ttu-id="f0141-103">Hämtar DSC-konfigurationer från Automation.</span><span class="sxs-lookup"><span data-stu-id="f0141-103">Gets DSC configurations from Automation.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f0141-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="f0141-104">SYNTAX</span></span>

### <span data-ttu-id="f0141-105">ByAll (standard)</span><span class="sxs-lookup"><span data-stu-id="f0141-105">ByAll (Default)</span></span>
```
Get-AzureRmAutomationDscConfiguration [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f0141-106">ByConfigurationName</span><span class="sxs-lookup"><span data-stu-id="f0141-106">ByConfigurationName</span></span>
```
Get-AzureRmAutomationDscConfiguration [-Name] <String> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f0141-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="f0141-107">DESCRIPTION</span></span>
<span data-ttu-id="f0141-108">Cmdleten **Get-AzureRmAutomationDscConfiguration** får APS-konfiguration (DSC-konfigurationer) från Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="f0141-108">The **Get-AzureRmAutomationDscConfiguration** cmdlet gets APS Desired State Configuration (DSC) configurations from Azure Automation.</span></span>

## <span data-ttu-id="f0141-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="f0141-109">EXAMPLES</span></span>

### <span data-ttu-id="f0141-110">Exempel 1: Hämta alla DSC-konfigurationer</span><span class="sxs-lookup"><span data-stu-id="f0141-110">Example 1: Get all DSC configurations</span></span>
```
PS C:\>Get-AzureRmAutomationDscConfiguration -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17"
```

<span data-ttu-id="f0141-111">Det här kommandot får metadata för alla DSC-konfigurationer i Automation-kontot med namnet Contoso17.</span><span class="sxs-lookup"><span data-stu-id="f0141-111">This command gets metadata for all DSC configurations in the Automation account named Contoso17.</span></span>

### <span data-ttu-id="f0141-112">Exempel 2: skaffa en DSC-konfiguration utifrån namn</span><span class="sxs-lookup"><span data-stu-id="f0141-112">Example 2: Get a DSC configuration by name</span></span>
```
PS C:\>Get-AzureRmAutomationDscConfiguration -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17" -Name "ContosoConfiguration"
```

<span data-ttu-id="f0141-113">Det här kommandot får metadata för en DSC-konfiguration med namnet min konfiguration som heter Contoso17.</span><span class="sxs-lookup"><span data-stu-id="f0141-113">This command gets metadata for a DSC configuration named MyConfiguration in the Automation account named Contoso17.</span></span>

## <span data-ttu-id="f0141-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="f0141-114">PARAMETERS</span></span>

### <span data-ttu-id="f0141-115">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="f0141-115">-AutomationAccountName</span></span>
<span data-ttu-id="f0141-116">Anger namnet på det Automation-konto som innehåller DSC-konfigurationer som den här cmdleten får.</span><span class="sxs-lookup"><span data-stu-id="f0141-116">Specifies the name of the Automation account that contains DSC configurations that this cmdlet gets.</span></span>

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

### <span data-ttu-id="f0141-117">-Namn</span><span class="sxs-lookup"><span data-stu-id="f0141-117">-Name</span></span>
<span data-ttu-id="f0141-118">Anger namnet på den DSC-konfiguration som den här cmdleten får.</span><span class="sxs-lookup"><span data-stu-id="f0141-118">Specifies the name of the DSC configuration that this cmdlet gets.</span></span>

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

### <span data-ttu-id="f0141-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f0141-119">-ResourceGroupName</span></span>
<span data-ttu-id="f0141-120">Anger namnet på en resurs grupp för vilken denna cmdlet får DSC-konfigurationer.</span><span class="sxs-lookup"><span data-stu-id="f0141-120">Specifies the name of a resource group for which this cmdlet gets DSC configurations.</span></span>

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

### <span data-ttu-id="f0141-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f0141-121">-DefaultProfile</span></span>
<span data-ttu-id="f0141-122">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="f0141-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f0141-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f0141-123">CommonParameters</span></span>
<span data-ttu-id="f0141-124">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f0141-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f0141-125">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f0141-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f0141-126">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="f0141-126">INPUTS</span></span>

## <span data-ttu-id="f0141-127">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="f0141-127">OUTPUTS</span></span>

### <span data-ttu-id="f0141-128">Microsoft. Azure. commands. Automation. Model. DscConfiguration</span><span class="sxs-lookup"><span data-stu-id="f0141-128">Microsoft.Azure.Commands.Automation.Model.DscConfiguration</span></span>

## <span data-ttu-id="f0141-129">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="f0141-129">NOTES</span></span>

## <span data-ttu-id="f0141-130">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="f0141-130">RELATED LINKS</span></span>

[<span data-ttu-id="f0141-131">Exportera-AzureRmAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="f0141-131">Export-AzureRmAutomationDscConfiguration</span></span>](./Export-AzureRmAutomationDscConfiguration.md)

[<span data-ttu-id="f0141-132">Import-AzureRmAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="f0141-132">Import-AzureRmAutomationDscConfiguration</span></span>](./Import-AzureRmAutomationDscConfiguration.md)


