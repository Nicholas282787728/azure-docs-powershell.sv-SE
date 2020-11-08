---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 6389EE2A-12B5-46A1-A2B9-4B3CF5A55A30
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/remove-azautomationdscconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationDscConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationDscConfiguration.md
ms.openlocfilehash: bd418037f29aefc27d92ccebe1f34024728c77c9
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94092660"
---
# <span data-ttu-id="b9662-101">Remove-AzAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="b9662-101">Remove-AzAutomationDscConfiguration</span></span>

## <span data-ttu-id="b9662-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="b9662-102">SYNOPSIS</span></span>
<span data-ttu-id="b9662-103">Tar bort DSC-konfigurationer från Automation.</span><span class="sxs-lookup"><span data-stu-id="b9662-103">Removes DSC configurations from Automation.</span></span>

## <span data-ttu-id="b9662-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="b9662-104">SYNTAX</span></span>

```
Remove-AzAutomationDscConfiguration [-Name] <String> [-Force] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="b9662-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="b9662-105">DESCRIPTION</span></span>
<span data-ttu-id="b9662-106">Cmdleten **Remove-AzAutomationDscConfiguration** tar bort DSC-konfigurationer (Desired State Configuration) från Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="b9662-106">The **Remove-AzAutomationDscConfiguration** cmdlet removes APS Desired State Configuration (DSC) configurations from Azure Automation.</span></span>

## <span data-ttu-id="b9662-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="b9662-107">EXAMPLES</span></span>

## <span data-ttu-id="b9662-108">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="b9662-108">PARAMETERS</span></span>

### <span data-ttu-id="b9662-109">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="b9662-109">-AutomationAccountName</span></span>
<span data-ttu-id="b9662-110">Anger namnet på det Automation-konto som innehåller DSC-konfigurationer som den här cmdleten tar bort.</span><span class="sxs-lookup"><span data-stu-id="b9662-110">Specifies the name of the Automation account that contains DSC configurations that this cmdlet removes.</span></span>

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

### <span data-ttu-id="b9662-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b9662-111">-DefaultProfile</span></span>
<span data-ttu-id="b9662-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="b9662-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b9662-113">-Force</span><span class="sxs-lookup"><span data-stu-id="b9662-113">-Force</span></span>
<span data-ttu-id="b9662-114">ps_force</span><span class="sxs-lookup"><span data-stu-id="b9662-114">ps_force</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b9662-115">-Namn</span><span class="sxs-lookup"><span data-stu-id="b9662-115">-Name</span></span>
<span data-ttu-id="b9662-116">Anger namnet på den DSC-konfiguration som denna cmdlet tar bort.</span><span class="sxs-lookup"><span data-stu-id="b9662-116">Specifies the name of the DSC configuration that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ConfigurationName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b9662-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b9662-117">-ResourceGroupName</span></span>
<span data-ttu-id="b9662-118">Anger namnet på en resurs grupp för vilken denna cmdlet får DSC-konfigurationer.</span><span class="sxs-lookup"><span data-stu-id="b9662-118">Specifies the name of a resource group for which this cmdlet gets DSC configurations.</span></span>

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

### <span data-ttu-id="b9662-119">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="b9662-119">-Confirm</span></span>
<span data-ttu-id="b9662-120">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="b9662-120">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b9662-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b9662-121">-WhatIf</span></span>
<span data-ttu-id="b9662-122">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="b9662-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b9662-123">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="b9662-123">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b9662-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b9662-124">CommonParameters</span></span>
<span data-ttu-id="b9662-125">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b9662-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b9662-126">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b9662-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b9662-127">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="b9662-127">INPUTS</span></span>

### <span data-ttu-id="b9662-128">System. String</span><span class="sxs-lookup"><span data-stu-id="b9662-128">System.String</span></span>

## <span data-ttu-id="b9662-129">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="b9662-129">OUTPUTS</span></span>

### <span data-ttu-id="b9662-130">System. Void</span><span class="sxs-lookup"><span data-stu-id="b9662-130">System.Void</span></span>

## <span data-ttu-id="b9662-131">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="b9662-131">NOTES</span></span>

## <span data-ttu-id="b9662-132">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="b9662-132">RELATED LINKS</span></span>

[<span data-ttu-id="b9662-133">Exportera-AzAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="b9662-133">Export-AzAutomationDscConfiguration</span></span>](./Export-AzAutomationDscConfiguration.md)

[<span data-ttu-id="b9662-134">Get-AzAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="b9662-134">Get-AzAutomationDscConfiguration</span></span>](./Get-AzAutomationDscConfiguration.md)

[<span data-ttu-id="b9662-135">Import-AzAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="b9662-135">Import-AzAutomationDscConfiguration</span></span>](./Import-AzAutomationDscConfiguration.md)


