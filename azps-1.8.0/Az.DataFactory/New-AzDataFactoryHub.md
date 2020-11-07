---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactories.dll-Help.xml
Module Name: Az.DataFactory
ms.assetid: B656B4C4-97DE-4F9F-937C-E115CB3F0E80
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/new-azdatafactoryhub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/New-AzDataFactoryHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/New-AzDataFactoryHub.md
ms.openlocfilehash: c121834f618dacdb1c2116852b7537f88d323bd4
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93754370"
---
# <span data-ttu-id="26ca3-101">New-AzDataFactoryHub</span><span class="sxs-lookup"><span data-stu-id="26ca3-101">New-AzDataFactoryHub</span></span>

## <span data-ttu-id="26ca3-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="26ca3-102">SYNOPSIS</span></span>
<span data-ttu-id="26ca3-103">Skapar ett nav för en Azure Data fabrik.</span><span class="sxs-lookup"><span data-stu-id="26ca3-103">Creates a hub for an Azure Data Factory.</span></span>

## <span data-ttu-id="26ca3-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="26ca3-104">SYNTAX</span></span>

### <span data-ttu-id="26ca3-105">ByFactoryName (standard)</span><span class="sxs-lookup"><span data-stu-id="26ca3-105">ByFactoryName (Default)</span></span>
```
New-AzDataFactoryHub [-Name] <String> [-File] <String> [-Force] [-DataFactoryName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="26ca3-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="26ca3-106">ByFactoryObject</span></span>
```
New-AzDataFactoryHub [-Name] <String> [-File] <String> [-Force] [-DataFactory] <PSDataFactory>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="26ca3-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="26ca3-107">DESCRIPTION</span></span>
<span data-ttu-id="26ca3-108">Cmdleten **New-AzDataFactoryHub** skapar ett nav för Azure Data Factory i den angivna Azure-resursen och i den angivna data fabriken med den angivna fil definitionen.</span><span class="sxs-lookup"><span data-stu-id="26ca3-108">The **New-AzDataFactoryHub** cmdlet creates a hub for Azure Data Factory in the specified Azure resource group and in the specified data factory with the specified file definition.</span></span>
<span data-ttu-id="26ca3-109">När du har skapat navet kan du använda det för att lagra och hantera länkade tjänster i en grupp, och du kan lägga till rörledningar i navet.</span><span class="sxs-lookup"><span data-stu-id="26ca3-109">After you create the hub, you can use it to store and manage linked services in a group, and you can add pipelines to the hub.</span></span>

## <span data-ttu-id="26ca3-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="26ca3-110">EXAMPLES</span></span>

### <span data-ttu-id="26ca3-111">Exempel 1: skapa ett nav</span><span class="sxs-lookup"><span data-stu-id="26ca3-111">Example 1: Create a hub</span></span>
```
PS C:\>New-AzDataFactoryHub -ResourceGroupName "ADFResourceGroup" -DataFactoryName "ADFDataFactory" -Name "ContosoDataHub" -File "C:\Hub.json"
```

<span data-ttu-id="26ca3-112">Det här kommandot skapar en hubb med namnet ContosoDataHub i resurs gruppen ADFResourceGroup och data fabriken med namnet ADFDataFactory.</span><span class="sxs-lookup"><span data-stu-id="26ca3-112">This command creates a hub named ContosoDataHub in the resource group ADFResourceGroup and the data factory named ADFDataFactory.</span></span>

## <span data-ttu-id="26ca3-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="26ca3-113">PARAMETERS</span></span>

### <span data-ttu-id="26ca3-114">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="26ca3-114">-DataFactory</span></span>
<span data-ttu-id="26ca3-115">Anger ett **PSDataFactory** -objekt.</span><span class="sxs-lookup"><span data-stu-id="26ca3-115">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="26ca3-116">Denna cmdlet skapar ett nav för data fabriken som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="26ca3-116">This cmdlet creates a hub for the data factory that this parameter specifies.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory
Parameter Sets: ByFactoryObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="26ca3-117">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="26ca3-117">-DataFactoryName</span></span>
<span data-ttu-id="26ca3-118">Anger namnet på en data fabrik.</span><span class="sxs-lookup"><span data-stu-id="26ca3-118">Specifies the name of a data factory.</span></span>
<span data-ttu-id="26ca3-119">Denna cmdlet skapar ett nav för data fabriken som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="26ca3-119">This cmdlet creates a hub for the data factory that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="26ca3-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="26ca3-120">-DefaultProfile</span></span>
<span data-ttu-id="26ca3-121">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="26ca3-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="26ca3-122">-Fil</span><span class="sxs-lookup"><span data-stu-id="26ca3-122">-File</span></span>
<span data-ttu-id="26ca3-123">Anger den fullständiga sökvägen till den JavaScript-fil som innehåller en beskrivning av navet.</span><span class="sxs-lookup"><span data-stu-id="26ca3-123">Specifies the full path of the JavaScript Object Notation (JSON) file that contains the description of the hub.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="26ca3-124">-Force</span><span class="sxs-lookup"><span data-stu-id="26ca3-124">-Force</span></span>
<span data-ttu-id="26ca3-125">Anger att denna cmdlet ersätter en befintlig hubb utan att du behöver bekräfta.</span><span class="sxs-lookup"><span data-stu-id="26ca3-125">Indicates that this cmdlet replaces an existing hub without prompting you for confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="26ca3-126">-Namn</span><span class="sxs-lookup"><span data-stu-id="26ca3-126">-Name</span></span>
<span data-ttu-id="26ca3-127">Anger namnet på navet som ska skapas.</span><span class="sxs-lookup"><span data-stu-id="26ca3-127">Specifies the name of the hub to create.</span></span>

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

### <span data-ttu-id="26ca3-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="26ca3-128">-ResourceGroupName</span></span>
<span data-ttu-id="26ca3-129">Anger namnet på en Azure-adressresurs.</span><span class="sxs-lookup"><span data-stu-id="26ca3-129">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="26ca3-130">Denna cmdlet skapar ett nav som tillhör den grupp som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="26ca3-130">This cmdlet creates a hub that belongs to the group that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="26ca3-131">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="26ca3-131">-Confirm</span></span>
<span data-ttu-id="26ca3-132">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="26ca3-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="26ca3-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="26ca3-133">-WhatIf</span></span>
<span data-ttu-id="26ca3-134">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="26ca3-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="26ca3-135">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="26ca3-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="26ca3-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="26ca3-136">CommonParameters</span></span>
<span data-ttu-id="26ca3-137">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="26ca3-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="26ca3-138">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="26ca3-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="26ca3-139">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="26ca3-139">INPUTS</span></span>

### <span data-ttu-id="26ca3-140">System. String</span><span class="sxs-lookup"><span data-stu-id="26ca3-140">System.String</span></span>

### <span data-ttu-id="26ca3-141">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="26ca3-141">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span></span>

## <span data-ttu-id="26ca3-142">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="26ca3-142">OUTPUTS</span></span>

### <span data-ttu-id="26ca3-143">Microsoft. Azure. commands. DataFactories. Models. PSHub</span><span class="sxs-lookup"><span data-stu-id="26ca3-143">Microsoft.Azure.Commands.DataFactories.Models.PSHub</span></span>

## <span data-ttu-id="26ca3-144">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="26ca3-144">NOTES</span></span>
* <span data-ttu-id="26ca3-145">Nyckelord: Azure, azurerm, arm, resurs, hantering, chef, data, faktorer</span><span class="sxs-lookup"><span data-stu-id="26ca3-145">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="26ca3-146">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="26ca3-146">RELATED LINKS</span></span>

[<span data-ttu-id="26ca3-147">Get-AzDataFactoryHub</span><span class="sxs-lookup"><span data-stu-id="26ca3-147">Get-AzDataFactoryHub</span></span>](./Get-AzDataFactoryHub.md)

[<span data-ttu-id="26ca3-148">Remove-AzDataFactoryHub</span><span class="sxs-lookup"><span data-stu-id="26ca3-148">Remove-AzDataFactoryHub</span></span>](./Remove-AzDataFactoryHub.md)


