---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 32CF9BF7-519F-4B5D-9F2B-3CC556A77A48
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/start-azautomationdsccompilationjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Start-AzAutomationDscCompilationJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Start-AzAutomationDscCompilationJob.md
ms.openlocfilehash: 34f09ca41326b2f6686a41cdeba0910317bc7a2c
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94088302"
---
# <span data-ttu-id="aab1e-101">Start-AzAutomationDscCompilationJob</span><span class="sxs-lookup"><span data-stu-id="aab1e-101">Start-AzAutomationDscCompilationJob</span></span>

## <span data-ttu-id="aab1e-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="aab1e-102">SYNOPSIS</span></span>
<span data-ttu-id="aab1e-103">Sammanställer en DSC-konfiguration i Automation.</span><span class="sxs-lookup"><span data-stu-id="aab1e-103">Compiles a DSC configuration in Automation.</span></span>

## <span data-ttu-id="aab1e-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="aab1e-104">SYNTAX</span></span>

```
Start-AzAutomationDscCompilationJob [-ConfigurationName] <String> [-Parameters <IDictionary>]
 [-ConfigurationData <IDictionary>] [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-IncrementNodeConfigurationBuild] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="aab1e-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="aab1e-105">DESCRIPTION</span></span>
<span data-ttu-id="aab1e-106">Cmdleten **Start-AzAutomationDscCompilationJob** kompilerar en DSC-konfiguration (önskad tillstånds konfiguration) i Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="aab1e-106">The **Start-AzAutomationDscCompilationJob** cmdlet compiles an APS Desired State Configuration (DSC) configuration in Azure Automation.</span></span>

## <span data-ttu-id="aab1e-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="aab1e-107">EXAMPLES</span></span>

### <span data-ttu-id="aab1e-108">Exempel 1: Kompilera en Azure DSC-konfiguration i Automation</span><span class="sxs-lookup"><span data-stu-id="aab1e-108">Example 1: Compile an Azure DSC configuration in Automation</span></span>
```
PS C:\>$Params = @{"StringParam"="Hello World";"IntegerParam"=32}
PS C:\> Start-AzAutomationDscCompilationJob -ConfigurationName "Config01" -Parameters $Params -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="aab1e-109">Det första kommandot skapar en ord lista med parametrar och lagrar dem i $Params variabeln.</span><span class="sxs-lookup"><span data-stu-id="aab1e-109">The first command creates a dictionary of parameters, and stores them in the $Params variable.</span></span>
<span data-ttu-id="aab1e-110">Det andra kommandot kompilerar DSC-konfigurationen som heter Config01.</span><span class="sxs-lookup"><span data-stu-id="aab1e-110">The second command compiles the DSC configuration named Config01.</span></span>
<span data-ttu-id="aab1e-111">Kommandot inkluderar värdena i $Params för DSC-konfigurationsparametrar.</span><span class="sxs-lookup"><span data-stu-id="aab1e-111">The command includes the values in $Params for DSC configuration parameters.</span></span>

### <span data-ttu-id="aab1e-112">Exempel 2: Kompilera en Azure DSC-konfiguration i Automation med en ny version för nodkonfigurationer.</span><span class="sxs-lookup"><span data-stu-id="aab1e-112">Example 2: Compile an Azure DSC configuration in Automation with a new Node Configuration build version.</span></span>
```
PS C:\>$Params = @{"StringParam"="Hello World";"IntegerParam"=32}
PS C:\> Start-AzAutomationDscCompilationJob -ConfigurationName "Config01" -Parameters $Params -ResourceGroupName "ResourceGroup01" -IncrementNodeConfigurationBuild
```

<span data-ttu-id="aab1e-113">Precis som i det första exemplet skapar det första kommandot en ord lista med parametrar och lagrar dem i $Params variabeln.</span><span class="sxs-lookup"><span data-stu-id="aab1e-113">Similar to the first example, the first command creates a dictionary of parameters, and stores them in the $Params variable.</span></span>
<span data-ttu-id="aab1e-114">Det andra kommandot kompilerar DSC-konfigurationen som heter Config01.</span><span class="sxs-lookup"><span data-stu-id="aab1e-114">The second command compiles the DSC configuration named Config01.</span></span>
<span data-ttu-id="aab1e-115">Kommandot inkluderar värdena i $Params för DSC-konfigurationsparametrar.</span><span class="sxs-lookup"><span data-stu-id="aab1e-115">The command includes the values in $Params for DSC configuration parameters.</span></span>
<span data-ttu-id="aab1e-116">Den tidigare befintliga nodadressen åsidosätts inte genom att en ny noduppsättning skapas med namnet Config01 [<2>]. <NodeName> .</span><span class="sxs-lookup"><span data-stu-id="aab1e-116">It does not override the earlier existing Node Configuration by creating a new Node Configuration with the name Config01[<2>].<NodeName>.</span></span> <span data-ttu-id="aab1e-117">Versions numret är stegvis baserat på det befintliga versions numret.</span><span class="sxs-lookup"><span data-stu-id="aab1e-117">The version number is incremented based on the existing version number already present.</span></span>

## <span data-ttu-id="aab1e-118">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="aab1e-118">PARAMETERS</span></span>

### <span data-ttu-id="aab1e-119">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="aab1e-119">-AutomationAccountName</span></span>
<span data-ttu-id="aab1e-120">Anger namnet på det Automation-konto som innehåller DSC-konfigurationen som kompileras av denna cmdlet.</span><span class="sxs-lookup"><span data-stu-id="aab1e-120">Specifies the name of the Automation account that contains the DSC configuration that this cmdlet compiles.</span></span>

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

### <span data-ttu-id="aab1e-121">-ConfigurationData</span><span class="sxs-lookup"><span data-stu-id="aab1e-121">-ConfigurationData</span></span>
<span data-ttu-id="aab1e-122">Anger en ord lista med konfigurations data för DSC-konfiguration.</span><span class="sxs-lookup"><span data-stu-id="aab1e-122">Specifies a dictionary of configuration data for DSC configuration.</span></span>

```yaml
Type: System.Collections.IDictionary
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aab1e-123">-ConfigurationName</span><span class="sxs-lookup"><span data-stu-id="aab1e-123">-ConfigurationName</span></span>
<span data-ttu-id="aab1e-124">Anger namnet på den DSC-konfiguration som denna cmdlet kompilerar.</span><span class="sxs-lookup"><span data-stu-id="aab1e-124">Specifies the name of the DSC configuration that this cmdlet compiles.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="aab1e-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aab1e-125">-DefaultProfile</span></span>
<span data-ttu-id="aab1e-126">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="aab1e-126">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="aab1e-127">-IncrementNodeConfigurationBuild</span><span class="sxs-lookup"><span data-stu-id="aab1e-127">-IncrementNodeConfigurationBuild</span></span>
<span data-ttu-id="aab1e-128">Skapar en ny version för nodkonfigurationer.</span><span class="sxs-lookup"><span data-stu-id="aab1e-128">Creates a new Node Configuration build version.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aab1e-129">-Parametrar</span><span class="sxs-lookup"><span data-stu-id="aab1e-129">-Parameters</span></span>
<span data-ttu-id="aab1e-130">Anger en ord lista med parametrar som denna cmdlet använder för att kompilera DSC-konfigurationen.</span><span class="sxs-lookup"><span data-stu-id="aab1e-130">Specifies a dictionary of parameters that this cmdlet uses to compile the DSC configuration.</span></span>

```yaml
Type: System.Collections.IDictionary
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aab1e-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="aab1e-131">-ResourceGroupName</span></span>
<span data-ttu-id="aab1e-132">Anger namnet på en resurs grupp där denna cmdlet sammanställer en konfiguration.</span><span class="sxs-lookup"><span data-stu-id="aab1e-132">Specifies the name of a resource group in which this cmdlet compiles a configuration.</span></span>

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

### <span data-ttu-id="aab1e-133">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="aab1e-133">-Confirm</span></span>
<span data-ttu-id="aab1e-134">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="aab1e-134">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aab1e-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="aab1e-135">-WhatIf</span></span>
<span data-ttu-id="aab1e-136">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="aab1e-136">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="aab1e-137">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="aab1e-137">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aab1e-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aab1e-138">CommonParameters</span></span>
<span data-ttu-id="aab1e-139">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="aab1e-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aab1e-140">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="aab1e-140">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aab1e-141">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="aab1e-141">INPUTS</span></span>

### <span data-ttu-id="aab1e-142">System. String</span><span class="sxs-lookup"><span data-stu-id="aab1e-142">System.String</span></span>

## <span data-ttu-id="aab1e-143">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="aab1e-143">OUTPUTS</span></span>

### <span data-ttu-id="aab1e-144">Microsoft. Azure. commands. Automation. Model. CompilationJob</span><span class="sxs-lookup"><span data-stu-id="aab1e-144">Microsoft.Azure.Commands.Automation.Model.CompilationJob</span></span>

## <span data-ttu-id="aab1e-145">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="aab1e-145">NOTES</span></span>

## <span data-ttu-id="aab1e-146">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="aab1e-146">RELATED LINKS</span></span>

[<span data-ttu-id="aab1e-147">Get-AzAutomationDscCompilationJob</span><span class="sxs-lookup"><span data-stu-id="aab1e-147">Get-AzAutomationDscCompilationJob</span></span>](./Get-AzAutomationDscCompilationJob.md)

[<span data-ttu-id="aab1e-148">Get-AzAutomationDscCompilationJobOutput</span><span class="sxs-lookup"><span data-stu-id="aab1e-148">Get-AzAutomationDscCompilationJobOutput</span></span>](./Get-AzAutomationDscCompilationJobOutput.md)


