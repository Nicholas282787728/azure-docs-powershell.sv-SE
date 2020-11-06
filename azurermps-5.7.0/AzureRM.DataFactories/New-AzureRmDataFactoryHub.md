---
external help file: Microsoft.Azure.Commands.DataFactories.dll-Help.xml
Module Name: AzureRM.DataFactories
ms.assetid: B656B4C4-97DE-4F9F-937C-E115CB3F0E80
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datafactories/new-azurermdatafactoryhub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/New-AzureRmDataFactoryHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/New-AzureRmDataFactoryHub.md
ms.openlocfilehash: 1891ab463b007b2e4a1502579f0d0e0a48779ca3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93579568"
---
# <span data-ttu-id="5bf5c-101">New-AzureRmDataFactoryHub</span><span class="sxs-lookup"><span data-stu-id="5bf5c-101">New-AzureRmDataFactoryHub</span></span>

## <span data-ttu-id="5bf5c-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="5bf5c-102">SYNOPSIS</span></span>
<span data-ttu-id="5bf5c-103">Skapar ett nav för en Azure Data fabrik.</span><span class="sxs-lookup"><span data-stu-id="5bf5c-103">Creates a hub for an Azure Data Factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5bf5c-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="5bf5c-104">SYNTAX</span></span>

### <span data-ttu-id="5bf5c-105">ByFactoryName (standard)</span><span class="sxs-lookup"><span data-stu-id="5bf5c-105">ByFactoryName (Default)</span></span>
```
New-AzureRmDataFactoryHub [-Name] <String> [-File] <String> [-Force] [-DataFactoryName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="5bf5c-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="5bf5c-106">ByFactoryObject</span></span>
```
New-AzureRmDataFactoryHub [-Name] <String> [-File] <String> [-Force] [-DataFactory] <PSDataFactory>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5bf5c-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="5bf5c-107">DESCRIPTION</span></span>
<span data-ttu-id="5bf5c-108">Cmdleten **New-AzureRmDataFactoryHub** skapar ett nav för Azure Data Factory i den angivna Azure-resursen och i den angivna data fabriken med den angivna fil definitionen.</span><span class="sxs-lookup"><span data-stu-id="5bf5c-108">The **New-AzureRmDataFactoryHub** cmdlet creates a hub for Azure Data Factory in the specified Azure resource group and in the specified data factory with the specified file definition.</span></span>
<span data-ttu-id="5bf5c-109">När du har skapat navet kan du använda det för att lagra och hantera länkade tjänster i en grupp, och du kan lägga till rörledningar i navet.</span><span class="sxs-lookup"><span data-stu-id="5bf5c-109">After you create the hub, you can use it to store and manage linked services in a group, and you can add pipelines to the hub.</span></span>

## <span data-ttu-id="5bf5c-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="5bf5c-110">EXAMPLES</span></span>

### <span data-ttu-id="5bf5c-111">Exempel 1: skapa ett nav</span><span class="sxs-lookup"><span data-stu-id="5bf5c-111">Example 1: Create a hub</span></span>
```
PS C:\>New-AzureRmDataFactoryHub -ResourceGroupName "ADFResourceGroup" -DataFactoryName "ADFDataFactory" -Name "ContosoDataHub" -File "C:\Hub.json"
```

<span data-ttu-id="5bf5c-112">Det här kommandot skapar en hubb med namnet ContosoDataHub i resurs gruppen ADFResourceGroup och data fabriken med namnet ADFDataFactory.</span><span class="sxs-lookup"><span data-stu-id="5bf5c-112">This command creates a hub named ContosoDataHub in the resource group ADFResourceGroup and the data factory named ADFDataFactory.</span></span>

## <span data-ttu-id="5bf5c-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="5bf5c-113">PARAMETERS</span></span>

### <span data-ttu-id="5bf5c-114">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="5bf5c-114">-DataFactory</span></span>
<span data-ttu-id="5bf5c-115">Anger ett **PSDataFactory** -objekt.</span><span class="sxs-lookup"><span data-stu-id="5bf5c-115">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="5bf5c-116">Denna cmdlet skapar ett nav för data fabriken som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="5bf5c-116">This cmdlet creates a hub for the data factory that this parameter specifies.</span></span>

```yaml
Type: PSDataFactory
Parameter Sets: ByFactoryObject
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5bf5c-117">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="5bf5c-117">-DataFactoryName</span></span>
<span data-ttu-id="5bf5c-118">Anger namnet på en data fabrik.</span><span class="sxs-lookup"><span data-stu-id="5bf5c-118">Specifies the name of a data factory.</span></span>
<span data-ttu-id="5bf5c-119">Denna cmdlet skapar ett nav för data fabriken som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="5bf5c-119">This cmdlet creates a hub for the data factory that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: ByFactoryName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5bf5c-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5bf5c-120">-DefaultProfile</span></span>
<span data-ttu-id="5bf5c-121">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="5bf5c-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="5bf5c-122">-Fil</span><span class="sxs-lookup"><span data-stu-id="5bf5c-122">-File</span></span>
<span data-ttu-id="5bf5c-123">Anger den fullständiga sökvägen till den JavaScript-fil som innehåller en beskrivning av navet.</span><span class="sxs-lookup"><span data-stu-id="5bf5c-123">Specifies the full path of the JavaScript Object Notation (JSON) file that contains the description of the hub.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5bf5c-124">-Force</span><span class="sxs-lookup"><span data-stu-id="5bf5c-124">-Force</span></span>
<span data-ttu-id="5bf5c-125">Anger att denna cmdlet ersätter en befintlig hubb utan att du behöver bekräfta.</span><span class="sxs-lookup"><span data-stu-id="5bf5c-125">Indicates that this cmdlet replaces an existing hub without prompting you for confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5bf5c-126">-Namn</span><span class="sxs-lookup"><span data-stu-id="5bf5c-126">-Name</span></span>
<span data-ttu-id="5bf5c-127">Anger namnet på navet som ska skapas.</span><span class="sxs-lookup"><span data-stu-id="5bf5c-127">Specifies the name of the hub to create.</span></span>

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

### <span data-ttu-id="5bf5c-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5bf5c-128">-ResourceGroupName</span></span>
<span data-ttu-id="5bf5c-129">Anger namnet på en Azure-adressresurs.</span><span class="sxs-lookup"><span data-stu-id="5bf5c-129">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="5bf5c-130">Denna cmdlet skapar ett nav som tillhör den grupp som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="5bf5c-130">This cmdlet creates a hub that belongs to the group that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: ByFactoryName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5bf5c-131">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="5bf5c-131">-Confirm</span></span>
<span data-ttu-id="5bf5c-132">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="5bf5c-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5bf5c-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5bf5c-133">-WhatIf</span></span>
<span data-ttu-id="5bf5c-134">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="5bf5c-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5bf5c-135">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="5bf5c-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5bf5c-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5bf5c-136">CommonParameters</span></span>
<span data-ttu-id="5bf5c-137">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5bf5c-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5bf5c-138">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5bf5c-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5bf5c-139">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="5bf5c-139">INPUTS</span></span>

### <span data-ttu-id="5bf5c-140">Ingen</span><span class="sxs-lookup"><span data-stu-id="5bf5c-140">None</span></span>
<span data-ttu-id="5bf5c-141">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="5bf5c-141">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="5bf5c-142">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="5bf5c-142">OUTPUTS</span></span>

### <span data-ttu-id="5bf5c-143">Microsoft. Azure. commands. DataFactories. Models. PSHub</span><span class="sxs-lookup"><span data-stu-id="5bf5c-143">Microsoft.Azure.Commands.DataFactories.Models.PSHub</span></span>

## <span data-ttu-id="5bf5c-144">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="5bf5c-144">NOTES</span></span>
* <span data-ttu-id="5bf5c-145">Nyckelord: Azure, azurerm, arm, resurs, hantering, chef, data, faktorer</span><span class="sxs-lookup"><span data-stu-id="5bf5c-145">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="5bf5c-146">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="5bf5c-146">RELATED LINKS</span></span>

[<span data-ttu-id="5bf5c-147">Get-AzureRmDataFactoryHub</span><span class="sxs-lookup"><span data-stu-id="5bf5c-147">Get-AzureRmDataFactoryHub</span></span>](./Get-AzureRmDataFactoryHub.md)

[<span data-ttu-id="5bf5c-148">Remove-AzureRmDataFactoryHub</span><span class="sxs-lookup"><span data-stu-id="5bf5c-148">Remove-AzureRmDataFactoryHub</span></span>](./Remove-AzureRmDataFactoryHub.md)


