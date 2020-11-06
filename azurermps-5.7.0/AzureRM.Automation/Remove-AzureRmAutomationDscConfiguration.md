---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: 6389EE2A-12B5-46A1-A2B9-4B3CF5A55A30
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/remove-azurermautomationdscconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Remove-AzureRmAutomationDscConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Remove-AzureRmAutomationDscConfiguration.md
ms.openlocfilehash: c328dcbf912b5b907f0e27c902bc7eb3dc31a44e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93574440"
---
# <span data-ttu-id="5f3d3-101">Remove-AzureRmAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="5f3d3-101">Remove-AzureRmAutomationDscConfiguration</span></span>

## <span data-ttu-id="5f3d3-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="5f3d3-102">SYNOPSIS</span></span>
<span data-ttu-id="5f3d3-103">Tar bort DSC-konfigurationer från Automation.</span><span class="sxs-lookup"><span data-stu-id="5f3d3-103">Removes DSC configurations from Automation.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5f3d3-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="5f3d3-104">SYNTAX</span></span>

```
Remove-AzureRmAutomationDscConfiguration [-Name] <String> [-Force] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="5f3d3-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="5f3d3-105">DESCRIPTION</span></span>
<span data-ttu-id="5f3d3-106">Cmdleten **Remove-AzureRmAutomationDscConfiguration** tar bort DSC-konfigurationer (Desired State Configuration) från Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="5f3d3-106">The **Remove-AzureRmAutomationDscConfiguration** cmdlet removes APS Desired State Configuration (DSC) configurations from Azure Automation.</span></span>

## <span data-ttu-id="5f3d3-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="5f3d3-107">EXAMPLES</span></span>

## <span data-ttu-id="5f3d3-108">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="5f3d3-108">PARAMETERS</span></span>

### <span data-ttu-id="5f3d3-109">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="5f3d3-109">-AutomationAccountName</span></span>
<span data-ttu-id="5f3d3-110">Anger namnet på det Automation-konto som innehåller DSC-konfigurationer som den här cmdleten tar bort.</span><span class="sxs-lookup"><span data-stu-id="5f3d3-110">Specifies the name of the Automation account that contains DSC configurations that this cmdlet removes.</span></span>

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

### <span data-ttu-id="5f3d3-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5f3d3-111">-DefaultProfile</span></span>
<span data-ttu-id="5f3d3-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="5f3d3-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="5f3d3-113">-Force</span><span class="sxs-lookup"><span data-stu-id="5f3d3-113">-Force</span></span>
<span data-ttu-id="5f3d3-114">ps_force</span><span class="sxs-lookup"><span data-stu-id="5f3d3-114">ps_force</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5f3d3-115">-Namn</span><span class="sxs-lookup"><span data-stu-id="5f3d3-115">-Name</span></span>
<span data-ttu-id="5f3d3-116">Anger namnet på den DSC-konfiguration som denna cmdlet tar bort.</span><span class="sxs-lookup"><span data-stu-id="5f3d3-116">Specifies the name of the DSC configuration that this cmdlet removes.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ConfigurationName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5f3d3-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5f3d3-117">-ResourceGroupName</span></span>
<span data-ttu-id="5f3d3-118">Anger namnet på en resurs grupp för vilken denna cmdlet får DSC-konfigurationer.</span><span class="sxs-lookup"><span data-stu-id="5f3d3-118">Specifies the name of a resource group for which this cmdlet gets DSC configurations.</span></span>

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

### <span data-ttu-id="5f3d3-119">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="5f3d3-119">-Confirm</span></span>
<span data-ttu-id="5f3d3-120">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="5f3d3-120">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5f3d3-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5f3d3-121">-WhatIf</span></span>
<span data-ttu-id="5f3d3-122">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="5f3d3-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5f3d3-123">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="5f3d3-123">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5f3d3-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5f3d3-124">CommonParameters</span></span>
<span data-ttu-id="5f3d3-125">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5f3d3-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5f3d3-126">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5f3d3-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5f3d3-127">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="5f3d3-127">INPUTS</span></span>

### <span data-ttu-id="5f3d3-128">Ingen</span><span class="sxs-lookup"><span data-stu-id="5f3d3-128">None</span></span>
<span data-ttu-id="5f3d3-129">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="5f3d3-129">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="5f3d3-130">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="5f3d3-130">OUTPUTS</span></span>

## <span data-ttu-id="5f3d3-131">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="5f3d3-131">NOTES</span></span>

## <span data-ttu-id="5f3d3-132">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="5f3d3-132">RELATED LINKS</span></span>

[<span data-ttu-id="5f3d3-133">Exportera-AzureRmAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="5f3d3-133">Export-AzureRmAutomationDscConfiguration</span></span>](./Export-AzureRmAutomationDscConfiguration.md)

[<span data-ttu-id="5f3d3-134">Get-AzureRmAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="5f3d3-134">Get-AzureRmAutomationDscConfiguration</span></span>](./Get-AzureRmAutomationDscConfiguration.md)

[<span data-ttu-id="5f3d3-135">Import-AzureRmAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="5f3d3-135">Import-AzureRmAutomationDscConfiguration</span></span>](./Import-AzureRmAutomationDscConfiguration.md)


