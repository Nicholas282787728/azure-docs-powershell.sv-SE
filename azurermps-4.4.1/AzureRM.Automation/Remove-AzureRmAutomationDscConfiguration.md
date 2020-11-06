---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: 6389EE2A-12B5-46A1-A2B9-4B3CF5A55A30
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Remove-AzureRmAutomationDscConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Remove-AzureRmAutomationDscConfiguration.md
ms.openlocfilehash: 2cd60a70b057689cf7edf154df28253b86e110a1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93578519"
---
# <span data-ttu-id="991eb-101">Remove-AzureRmAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="991eb-101">Remove-AzureRmAutomationDscConfiguration</span></span>

## <span data-ttu-id="991eb-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="991eb-102">SYNOPSIS</span></span>
<span data-ttu-id="991eb-103">Tar bort DSC-konfigurationer från Automation.</span><span class="sxs-lookup"><span data-stu-id="991eb-103">Removes DSC configurations from Automation.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="991eb-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="991eb-104">SYNTAX</span></span>

```
Remove-AzureRmAutomationDscConfiguration [-Name] <String> [-Force] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="991eb-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="991eb-105">DESCRIPTION</span></span>
<span data-ttu-id="991eb-106">Cmdleten **Remove-AzureRmAutomationDscConfiguration** tar bort DSC-konfigurationer (Desired State Configuration) från Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="991eb-106">The **Remove-AzureRmAutomationDscConfiguration** cmdlet removes APS Desired State Configuration (DSC) configurations from Azure Automation.</span></span>

## <span data-ttu-id="991eb-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="991eb-107">EXAMPLES</span></span>

## <span data-ttu-id="991eb-108">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="991eb-108">PARAMETERS</span></span>

### <span data-ttu-id="991eb-109">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="991eb-109">-AutomationAccountName</span></span>
<span data-ttu-id="991eb-110">Anger namnet på det Automation-konto som innehåller DSC-konfigurationer som den här cmdleten tar bort.</span><span class="sxs-lookup"><span data-stu-id="991eb-110">Specifies the name of the Automation account that contains DSC configurations that this cmdlet removes.</span></span>

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

### <span data-ttu-id="991eb-111">-Force</span><span class="sxs-lookup"><span data-stu-id="991eb-111">-Force</span></span>
<span data-ttu-id="991eb-112">ps_force</span><span class="sxs-lookup"><span data-stu-id="991eb-112">ps_force</span></span>

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

### <span data-ttu-id="991eb-113">-Namn</span><span class="sxs-lookup"><span data-stu-id="991eb-113">-Name</span></span>
<span data-ttu-id="991eb-114">Anger namnet på den DSC-konfiguration som denna cmdlet tar bort.</span><span class="sxs-lookup"><span data-stu-id="991eb-114">Specifies the name of the DSC configuration that this cmdlet removes.</span></span>

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

### <span data-ttu-id="991eb-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="991eb-115">-ResourceGroupName</span></span>
<span data-ttu-id="991eb-116">Anger namnet på en resurs grupp för vilken denna cmdlet får DSC-konfigurationer.</span><span class="sxs-lookup"><span data-stu-id="991eb-116">Specifies the name of a resource group for which this cmdlet gets DSC configurations.</span></span>

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

### <span data-ttu-id="991eb-117">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="991eb-117">-Confirm</span></span>
<span data-ttu-id="991eb-118">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="991eb-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="991eb-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="991eb-119">-WhatIf</span></span>
<span data-ttu-id="991eb-120">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="991eb-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="991eb-121">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="991eb-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="991eb-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="991eb-122">-DefaultProfile</span></span>
<span data-ttu-id="991eb-123">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="991eb-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="991eb-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="991eb-124">CommonParameters</span></span>
<span data-ttu-id="991eb-125">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="991eb-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="991eb-126">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="991eb-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="991eb-127">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="991eb-127">INPUTS</span></span>

## <span data-ttu-id="991eb-128">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="991eb-128">OUTPUTS</span></span>

## <span data-ttu-id="991eb-129">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="991eb-129">NOTES</span></span>

## <span data-ttu-id="991eb-130">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="991eb-130">RELATED LINKS</span></span>

[<span data-ttu-id="991eb-131">Exportera-AzureRmAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="991eb-131">Export-AzureRmAutomationDscConfiguration</span></span>](./Export-AzureRmAutomationDscConfiguration.md)

[<span data-ttu-id="991eb-132">Get-AzureRmAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="991eb-132">Get-AzureRmAutomationDscConfiguration</span></span>](./Get-AzureRmAutomationDscConfiguration.md)

[<span data-ttu-id="991eb-133">Import-AzureRmAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="991eb-133">Import-AzureRmAutomationDscConfiguration</span></span>](./Import-AzureRmAutomationDscConfiguration.md)


